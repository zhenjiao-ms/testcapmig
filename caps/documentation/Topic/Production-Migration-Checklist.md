---
title: Production Migration Checklist
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 153deb51-f819-4c81-8877-28f8dd1de737
---
# Production Migration Checklist
## CAPS Post Migration Checklist
Once English and localized content has been migrated to the CAPS production environment all future publishing of that content must be done from CAPS and the topics in DxStudio need to be locked. This checklist will help guide you through the process of completing the migration to production.

1. **TOC updates (if needed).** If content is published in DxStudio via HxS, the HxT hookup needs to be updated. Otherwise, MTPS will take the old TOC structure and does not update the new one. File a PubDesk task to do this work.
1. **Perform a final visual inspection of the content** – This is the same type of visual test pass that was performed during the test migrations however now it is done in the CAPS production environment. This is the last chance to verify that the migration was successful. From this point on any time this content is published it can go live on TechNet/MSDN.

  Topics for all migrated locales should be inspected to make sure that:
  1. Images appear as expected
  1. Links are rendered properly and still function
  1. Formatting of the topics is as expected
  1. Lists and tables are still intact
  1. Tokens are still valid
  1. Side-by-Side markup works as expected (if relevant)
  
  Doc Sets and Outlines should be inspected to make sure that:
  
  1. The hierarchy of topics from all projects migrated as expected
  1. The form of the TOC is still intact – note that the TOC for different locales may differ
  1. Expected build outputs (e.g. chm, docx) can be generated


  Topics should also be viewed on MSDNstage to make sure they render properly by the build system. The same items listed above should be verified in the rendered topics as well.
 
###Recommended publishing steps after migration from DxStudio to CAPS
Follow the recommended publishing steps below.
1.	Stage the entire content set (**topics and TOC**) in CAPS upon migration.
2.	File a ticket with Pubdesk to Hookup TOC (if required) in Stage environment.
3.	Review your content on msdnstage or tnstage.
4.	If there are no issues on stage and your topics and TOC look good, publish the entire content set (**topics and TOC**) live.
5.	Update the PubDesk ticket in step #2 above to push the changes to the TOC live.
6.	Review your content on msdnlive or tnlive. 

Notes
* Publishing the TOC only without the content will not refresh the TOC
* Be aware of the [publishing flags](Publishing-flags.md) behavior.

If publishing the full content set is not possible
1.	If there are only topic content changes, publish the topic(s) affected (content only).
2.	If there is TOC title change or there is a new topic in the TOC:
Recommended:
a.	Publish the whole docset (both topic and toc)
b.	Hook up TOC (if TOC ID is not migrated)
c.	Publish the TOC change of the topic whose TOC title changed
a and b only need to be done once.
Alternative (more complex but require publish less nodes):
a.	Publish *content* of changed topic and its siblings
b.	Publish *content and TOC* of the parent of the changed topic
Unlike recommended way, you may need to do this multiple times and this can only be done if TOC IDs are migrated.
3.	If a topic is moved within the TOC 
Recommended, same as recommended in #2 with one additional step:
a.	Publish the whole docset (both topic and toc)
b.	Hook up TOC (if TOC ID is not migrated)
c.	Publish the TOC of the topic you moved you want
d.	Publish the TOC of the old parent
Alternative, same as alternative in #2 with additional steps:
a.	Publish *content* of its old siblings
b.	Publish *content and TOC* of its old parent
c.	Publish *content* of changed topic and its siblings
d.	Publish *content and TOC* of the parent of the changed topic
4.	If a topic is new
Recommended:
a.	Publish the whole docset (both topic and toc)
b.	Hook up TOC (if TOC ID is not migrated)
c.	Publish the TOC and content change of the topic 
a and b only need to be done once.
Alternative (more complex but require publish less nodes):
c.	Publish *content* of changed topic and its siblings
d.	Publish *content and TOC* of the parent of the changed topic
Unlike recommended way, you may need to do this multiple times
And this can only be done if TOC IDs are migrated.
5.	If a topic is removed from the TOC (like pave over) 
Recommended:
a.	Publish the whole docset
b.	Hook up TOC (if TOC ID is not migrated)
c.	Publish TOC of old parent
Alternative:
a.	Publish *content* of the topic's siblings
b.	Publish *content and TOC* of its old parent
And this can only be done if TOC IDs are migrated.


The below tasks are more post-migration tasks: 
  
1. **Lock topics in DxStudio to prevent future publishing from DxPlatform** – File a Work Request with PubDesk to lock all of the migrated projects in DxStudio. The ticket must list the impacted database(s) and include all project names. Instructions are here.
1. **Localization Only** - file a work request with PubDesk to label Source Depot content for all relevant locales with “Migrated to CAPS”.  IPMs: close existing projects in LocServices
1. **Obtain the DxStudio output of each project's topic history.** CAPS does not keep the history dates from DxStudio but, instead, takes the dates when the content was migrated and checked-in to CAPS. This DxStudio output should include:
  1. Content check-in dates
  1. Localization handoff dates and targets 
1. **Production Migration Sign-off** - This is acknowledgement from the content owner and loc owner that they have inspected the content in the production environment and agree that it is ready to be used for live publishing to the web. Once this step is done, production migration is complete and the content is live on CAPS.

30 days post-migration - There should be a decision with respect to the following:
1. **Archive the DxStudio database.** Submit a ticket to PubDesk to archive the DxStudio database 30 days after migration to CAPS production.

