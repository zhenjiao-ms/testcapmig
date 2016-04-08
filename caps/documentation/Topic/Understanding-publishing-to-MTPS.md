---
title: Understanding publishing to MTPS
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bd4bd301-db92-4484-a9a6-fa2469e73133
---
# Understanding publishing to MTPS
It is crucial to understand how publishing to MTPS works, and what are the limitations and some of the expected behaviors you will see.

**In this topic:**

* [CMS, Staging, and Live workflow](#PubWorkflow)
* [Publishing flags](#Publishingflags)
* [IMPORTANT differences regarding publishing the TOC to stage vs. publishing to live](#PublishingStageLive)
* [Submission to publishing vs. publishing](#SubmissionVsPublishing)
* [Topic title disambiguation](#TopicDisambiguation) 
* [Hooking up the docsets into the MSDN/TN TOCs](#HxTHookup)
* [Publishing timeout](#PublishingTimeout)

## <a name="PubWorkflow">CMS, Staging, and Live workflow</a>
The content follows this workflow:
CMS  -> Staging server -> Live

* CMS - Content is checked-in for English / handed back for localization)
* Staging - All content needs to go to staging first.
* Live - Only the content that is on stage will go live. 

Thus, in order to publish a new topic or an updated version of an existing topic to live, it has first to be checked-in/handed back, then published to stage, and then published to live. 

## <a name="Publishingflags">Publishing flags</a>
Publishing flags work differently than in DxStudio and there are some limitations between what can be done in CAPS and what it cannot be done. Thus, here is a list of how the publishing flags work. 

Publishing option  |Ready to stage flag required?  |Ready to stage flag reset after publishing?  |Ready to live flag required?  |Ready to live flag reset after publishing?  
---------|---------|---------|---------|---------
**TOC and content**     |  Yes *(but only for topic)*       | No        |  Yes *(but only for topic)*       |       Yes  
**TOC only**     |  No       |   No      |    No     |  No       
**Content only**     |    Yes     |   No      |  Yes       |    Yes

## <a name="PublishingStageLive">IMPORTANT differences regarding publishing the TOC to stage vs. publishing to live</a>
> [!Caution] Use caution when publishing the TOC!! The TOC title of a topic and its children and siblings can only be promoted all together, or not promoted at all. You cannot choose to promote the TOC titles for some of them.
Note that grand children are not affected.

This is because publishing to stage is fully controlled by the CMS (i.e. CAPS) whereas publishing to live is controlled by MTPS. This section explains the behavior you will see.

The key differences between stage and live are:
1.	For stage, we have some intelligent algorithms to simplify publish workflow. For example,
	* When you publish a node, we will update its title in its parent’s TOC
	* If a children is never published, it will not show up in its parent’s TOC
2.	For live, none of these rules apply. For the TOC, We simply promote what’s in staging to live. The basic unit for live is all child nodes of a parent node.

Examples:

### TOC updated for all siblings

1.	Create a tree like this:

         a		 
	|--b		 
	|--c
2.	Publish to stage and live the whole tree
3.	Rename b to d. Change the topic content.
4.	Rename c to e. Change the topic content.
5.       Your structure in CAPS looks like this:

         a		 
	|--d		 
	|--e
6.	Select d, publish to stage
7.	You’ll see on staging the TOC becomes:

         a		 
		 |--d		 
		 |--c
		 
     Which is expected, since you only published d. 
8.	Publish e, the TOC on staging will match the CMS:

         a		 
		 |--d		 
		 |--e
9.	Then select d only and publish live, the TOC on live will be:

         a		 
		 |--d		 
		 |--**e**
		 
This means that the TOC for **e** has been published live, even this topic was not submitted for publishing.

Note that the contents for **e** do not get published in live.

### Publish parent, all children TOCs are updated
1.	Create a tree like this:

         a                     
         |--b                       
         |--c
2.	Publish to stage and live the whole tree
3.	Rename a to z. Change the topic content. 
4.	Rename b to d. Change the topic content.
5.	Rename c to e. Change the topic content.
6.	Your structure in CAPS looks like this:

         z         
         |--d         
         |--e
7.	Select z, publish to stage. 
8.	You’ll see on staging the TOC becomes: (children topic TOCs are updated)

         z  (updated topic is on stage)                 
         |--**d** (content is not updated on stage)                      
         |--**e** (content is not updated on stage) 
      
9.	Then select z only and publish live, the TOC on live will be:
         z                     
         |--**d**  (content is not updated on live)                     
         |--**e**  (content is not updated on live)                    
                           
Result:
* When publishing a parent, all the children TOC get updated to stage and live as well. 

## <a name="SubmissionVsPublishing">Submission to publishing vs. publishing</a>
 
Right now, CAPS does not have a way to see whether the content is published to MTPS. Instead, it only receives information that the content has been submitted. Thus, if you do not see the content published you will need to wait as your content might be in the publishing queue. 


## <a name="TopicDisambiguation">Topic title disambiguation</a>

In DxStudio, anything in brackets was removed at build time. Brackets were added to allow for topics with the same name and the bracket was adding the disambiguation. In CAPS, you can have multiple topics with the same name in a docset. Thus, if you add brackets in the topic title, they will get published. So what you see, is what you get!

## <a name="HxTHookup">Hooking up the docsets into the MSDN/TN TOCs</a>
Unless you are sharing your docset into another docset, you need to hook up the docset into an HxT in MSDN. This is not something CAPS can do for you. If you are in CSI, file a ticket with Pubdesk to [Hookup TOC](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-us/library/dn940589).  

## <a name="PublishingTimeout">Publishing timeout</a>
Publishing jobs need to be process in 60 minutes. If publishing submission takes more than 60 minutes you will get an error in the publishing report. However this might be unlikely for MTPS publishing. Docset publish request is divided into small topic publish so one hour should be long enough for a single topic. But for offline build, we treat the whole docset as a single publish so one hour will be a problem if a docset is too big.