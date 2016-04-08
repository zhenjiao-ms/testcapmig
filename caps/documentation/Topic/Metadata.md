---
title: Metadata
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77a3185a-96e1-4a62-99a0-03be5c06300b
---
# Metadata
The following is an alphabetical list of metadata in CAPS.

To request additional drop-down values for metadata in this list, please [file a CAPS bug](How-to-file-a-Bug.md).

Field  | Value |  Location|Description  
---------|---------|---------|---------
Alternate text|Text|Image General tab|(Art) The text to display if the image cannot render and to use for screen readers.|
Applies to Product | Select from drop-down| Topic Publishing tab |(Content) Stubs boilerplate indicating which product the content applies to. This is different from ms.prod, which is used for BI.|      
Auto Stage Localization Content aT Handback|TRUE / FALSE |Docset Localization tab|Indicates whether the topics in the docset should be automatically staged when handed back from Loc. Staging can only succeed if en-US topics of the same version have already staged.|
Auto Live Localization Content At Handback| TRUE/ FALSE |Docset Localization tab|Indicates whether the topics in the docset should be automatically published live when handed back from Loc. Publishing can only succeed if en-US topics of the same version have already published live.|
Assigned To |A user from the MS address book, or none|Topic General tab  |(Workflow) The person to whom the topic is assigned. By default the writer; can be set manually for workflow tracking. |
Bilingual Publishing Value |Edit / NoEdit for HT / MT |Not visible in UI except as query field|(Loc) The value assigned to the localized topic for bilingual publishing. This value determines the disclaimer text that gets displayed in the topic and whether or not the topic can be edited via the Translation Wiki. The value is set via the the Set Locale dialog box off the topic-level Localization tab. |       
Bilingual: Edit Human Translation|This is a potential value for Bilingual Settings|Set Locales dialog off topic Localization tab |(Loc) Applies only to en-us content. To see which locales use this value, add the MT Qualityeditable Locales column to your query results. |    
Bilingual: Edit Machine Translation|This is a potential value for Bilingual Settings |Set Locales dialog off topic Localization tab |(Loc) Applies only to en-us content. You can only query for this value on an en-US topic. To see which locales use this value, add the MT Editable Locales column to your query results |         
Bilingual: NoEdit Human Translation|This is a potential value for Bilingual Settings  |Set Locales dialog off topic Localization tab |(Loc) // desc missing | 
Bilingual: NoEdit Machine Translation|This is a potential value for Bilingual Settings|Set Locales dialog off topic Localization tab|(Loc)|           
Comment |Text |Image General tab |(Art) Use to add a comment about an image.         
Community Content|Docset Publishing tab|TRUE / FALSE (default) |(Publishing) Specifies if customers can add discussion to the topic once published to MTPS.         |         
Contains Deprecated |Mref topic General tab |TRUE / FALSE| (Mref) Indicates that the topic contains one or more API that has been marked as deprecated in the DLL. Stubs the following boilerplate before the summary: **Note: This API is now obsolete.** This metadata is applied automatically in reflection based on the content of the DLLs. You cannot set it manually.       
Content Checked Out By |Topic General tab |A user from the ms address book, or none |(Workflow) The user, if any, who has the topic locked for exclusive editing.         
Content Checked Out Date |A date, or none | Topic General tab |(Workflow) The date of the current checkout, if applicable (indicates how long the topic has been checked out).         
Content Modified By |A user from the MS address book|Topic General tab|(History) The last user to check in a change to the topic, or a build account for system changes or changes via CAPS API.
Content Modified Date|A date |Topic General tab|(History) The last date a change was checked in to the topic.       
Customed Redirect URL  |A URL or topic ID |Retired topic Publishing tab |(Publishing) Add on the Publishing tab of retired topics to specify a redirect URL when the topic is paved over.         
Description  |Text (135 characters max) |Topic Publishing tab|(SEO) Enables users to add a short description to be published as the description HTML tag and returned in search engine results.
Designer|A user from the MS address book|Image General tab|(Art) The designer who worked on the image.         
Devlang  |Select from drop-down list (default=na)  |Topic Publishing tab | (Publishing) Used by F1 Help to build programming language specific in-product links to content. This is different from ms.devlang, which is used for BI. 
Editor |A user from the MS address book|General tab  |(Workflow) Specifies the editor of the topic.         
F1 Keyword |Text, hit return to separate into tags  |General tab | F1 keywords are used to link to topics via product UI. These are set manually for conceptual topics. For mref, they are generated by reflection and cannot be edited. //keywords are editable on both source and loc General tabs, but should never be edited in the UI for loc (included in xliff file as translatable segment.        
Footer token    |Token |Topic Publishing tab |Specifies a token (must already exist in portfolio) to build as footer text for the topic.         
Fully Qualified Name|Text|Mref General tab|The fully-qualified name (prefix, namespace, type, member) for an API. This is different from the name, which only includes the namespace, type, or member name.
GUID|A GUID|General tab|Specifies the unique identifier for the topic. GUID applies across locales (that is, the en-US and other locales of a topic have the same GUID). Created by CAPS at topic creation.|
 Handoff Candidate |Text |Topic Localization tab|Specifies the localization handoff(s) candidate the topic is assigned to. Bug: values should behave like tags, but don't.
Header token |Token |Topic Publishing tab |Specifies a token (must already exist in portfolio) to build as header text for the topic. |
Internal Only |TRUE / FALSE (default) | MRef General tab |Indicates that the topic has been flagged with the InternalOnly attribute. This attribute is set on the General tab for mref topics and stubs the following boilerplate before the summary: **This API supports the product infrastructure and is not intended to be used directly from your code.** This attribute must be set on individual topics. We originally requested a cascading attribute -- that is, if you set the attribute on the type topic, it would cascade to all child membvers. But this solution was costly and was deemed low priority because you can use bulk metadata update to add the attribute to all member topics under a type. //Question - is internalonly token also in use?
Last Handback Date | Date|Topic Localization tab|Specifies when the topic was handed back from localization last.Has different meanings for English and Loc. Last Handback date for en-US = the last time ANY locale was handed back; for locales = the last  time the CURRENT locale was handed back.|
Last Handoff Date |Date|Topic Localization tab|Specifies when the topic was handed off to localization last. Last Handoff date for en-US = the last time ANY locale was handed off; for locales = the last  time the CURRENT locale was handed off.
Last Handoff Name |Text|Topic Localization tab|Specifies the name of the last localization handoff. Last Handoff name for en-US = the name of the last handoff in ANY locale; for locales = the name of the last handoff for the CURRENT locale.
Last Reflected Date  |Date|Mref General tab |The last date managed reference reflection was run.
Live Status|One of several available states|Topic Publishing tab (source and Loc)|Specifies whether the topic was published live to MTPS successfully or not on the last attempt. Possible values: Cancelled; Failed; Paused; Pending; Processing; Succeeded; SucceededWithWarning //change UI name to "Published Live Status"
Locale  |Locale code, such as en-US or de-DE|Drop-down selector lets you switch between locales to preview|Specifies the locale of the topic. Locale is only available as a default query clause (the clauses in gray at the top of every query). You cannot currently add new default clauses or move or group default clauses.|
Locales Handed Back to Date|Locale codes|?|?|
Locales Handed Off For HT (source) |Locale codes|Topic|// WRONG: Per Zhen mail thread issue # 21246 : the display name “locales handed off for ht” of the metadata  is incorrect. The real name of the metadata is “human_translation_locales”, which means, this locale exists and the latest version is translated by human. Specifies which locales the topic has been handed off for human translation.
Locales Handed Off For MT (source) |Locale codes|Topic|Specifies which locales the topic has been handed off for machine translation.|
Locales in Last Hand Back (source)|Locale codes|Topic|Specifies the locale list which has been handed back with translation to the latest English source.
Locales in Translation (source) |Locale codes|Topic|Specifies the locale list which has been handed off, but not handed back (translation in progress based on latest English source.)
Locales Planned for Bilingual Pub (source) |Locale codes|Topic|Specifies which locales the bilingual setting is turned on.
Locales Planned for HT (source) |Locales|Topic|Locales that the topic is marked for human translation.|
Locals Planned for MT (source)|Loc|Topic|Locales that the topic is marked for machine translation.|
Localizable Metadata Version|Number|Topic|The version of the localizable metadata (Title, TOC, and F1 Keywords. This is the number after the dot in the purple status bar. Non-localizable metadata is not versioned.|
Manager  |A user in the MS address book|General tab|Specifies the manager of the writer who owns the topic.
Metadata Modified By (source and Loc)|A user in the MS address book|Topic|Specifies the user who modifies the topic metadata last. // not available as a column option - file bug|
Metadata Modified Date |Date|Topic|Specifies when the topic metadata was modified last.// not available as a column option - file bug // source publishing also updates loc metadata
ms.custom (source) |Text|Topic Publishing tab|(Workflow) Allows users to specify custom tags to help track content.  You can add multiple values.
ms.date|Date|Topic Publishing tab|(BI) The freshness date. This date is added manually by the writer to indicate that a topic has been recently updated or verified as still accurate and relevant ("fresh"). It stubs **Updated** boilerplate at the top of the published topic and is tracked as a key content metric by some teams.
ms.devlang (source) |Select from drop-down (default=na)|Topic Publishing tab|(BI) Specifies the programming language framework to which the topic applies.|
ms.prod (source) |Select from drop-down|Topic Publishing tab|(BI) Specifies the product to which the topic applies.|
ms.reviewer (source) |(Workflow) User(s) from the MS address book|Topic General tab|Specifies one or more reviewes of the content.
ms.service (source) |Select from drop-down|Topic Publishing tab|(BI) Specifies the service or feature to which the topic applies.
ms.suite (source)|Select from drop-down|Topic Publishing tab| (BI) The technology suite the topic belongs to.
ms.technology (source) |Select from drop-down (can be multi-valued)|Topic Publishing tab|(BI) Specifies on-premise service, feature, server role, etc.
ms.tgt_platform (source)|Select from drop-down|Topic Publishing tab|(BI) The development platform the content applies to.
ms.topic (source)|Select from drop-down|Topc Publishing tab |(BI) Specifies the type of topic, such as "get-started", "hero-article", etc., for content metrics.
MTPS Alias|Text|Topic Publishing tab|(SEO) Allows user to create a friendly URL as an alias to the topic. Lowercase letters, numbers, and hyphens are allowed, and periods for reference topics. No other characters (including uppercase letters) are allowed and there is an 80 character maximum. Format should be words of the friendly title separated by hyphens, e.g. caps-metadata-list for this topic. The topic will then be reachable by alias; in this case [https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/caps-metadata-list.aspx](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/caps-metadata-list.aspx).
Name |Text|General tab|(Content) The name (title) of the topic.|
No Follow (source)|TRUE / FASLE (default)|Topic Publishing tab|TRUE - specifies the content linked from this topic will NOT be followed by search engine crawlers; FALSE - specifies the content will be followed by search engine crawlers. Set to TRUE when paving over content.
No Index (source) |TRUE / FASLE (default)|Topic Publishing tab|TRUE - specifies the content should NOT be found by search engines; FALSE - specifies the content should be found by search engines. Set to FALSE when paving over content.
Preferred Library (source)|Select from drop-down |Docset Publishing tab|Select the library where you would like your content to appear. This text is used to build the canonical URL. The default value is "/library" to make sure that MTPS goes to either MSDN or TechNet library. MTPS builds ‘canonical URL’ by: Preferred Site + Preferred Library + content alias or shortId. 
Preferred Site (source) |Select from drop-down |Docset Publishing list|Select which site (mainly MSDN or TechNet) the content will be found via Search. By default, the content is set to be displayed in MSDN. MTPS builds ‘canonical URL’ by: Preferred Site + Preferred Library + content alias or shortId.|
Product Family (source)|Select from drop-down |Docset Publishing tab |(Publishing) The product family, such as Visual Studio, SQL Server, or Windows, that the docset belongs to.|
Product Family Version (source) |Select from drop-down |Docset Publishing tab |(Publishing) The product family version. | 
Published Date (source and locales) |Date|Topic Publishing tab|Manually set for content freshness. Stubs **Published** boilerplate at the top of the topic. // this field is little used and may be removed -- recommendation is to only use ms.date for freshness tracking
Published to Live Date (source and locales) |Date|Topic Publishing tab|Specifies the date when the topic was published live to MTPS. This comes from topic history and cannot be set manually.
Published to Stage Date (source and locales)|Date |Topic Publishing tab |Specifies the date when the topic was staged to MTPS. This comes from topic history and cannot be set manually.
Publishing Live Message (source and loc) |System text |Query field|Returns the status message for the last attempt to publish live. //examples 
Ready to Publish Live (source) |TRUE / FALSE (default) | Topic Publishing tab |TRUE = topic can go live; FALSE = topic cannot go live. Must be set on each topic for each live publishing job -- it is automatically flipped back to FALSE after publish to live. For loc, flag is not available. Localized topics can be published as long as version the same or lower than the en-US version.
Ready to Stage (source) |TRUE / FALSE (default) | Topic Publishing tab | TRUE = topic can be staged; FALSE = topic cannot be staged. This flag remains set after staging. For loc, flag is not available. Localized topic scan be published as long as version the same or lower than the en-US version.
Redirect URL Type (source) |Select option | Retired  topic Publishing tab| (Publishing) For paveover, select redirection option: None, External URL, or Internal Topic.| 
Reference Type (source and locales)| System text|Mref General tab|(Mref) The managed reference topic type, such as class, method, or property. 
Reflection ID |GUID |  Reflection tab|(Mref) The GUID that identifies a managed reference reflection. This GUID remains the same when reflection is updated.|
Retired (source and locales)| TRUE / FALSE|Query field only?|Indicates whether a topic has been retired (for paveover). Only source files can be retired; loc files inherit. You can query for retired topics in any locale.|
Search Keyword|Text (tags)|Topic Publishing tab|(SEO) Enables the user to add one or more keywords to populated the keywords HTML element for search engines.
Staging Message (source and locales) | | |//change to Publishing to Stage messages for consistency|
Staging Status (source and locales) |Publishing |Topic |Cancelled, Failed, PartiallySucceeded, Paused, Pending, Processing, Succeeded, SucceededWithWarning //need definitions of all these| 
Status (source) |Workflow|Topic|Indidcates the workflow status of the topic: Blocked, Content Complete, Revising, Updated By System, Writing, Writing Not Started //updated by system still there!
Tags (source) | | Topic|Free-form tags you can add on the general tab. To enter multiple tags at a time, separate by semi-colon.
To Be Localized (source)|TRUE / FALSE |Docset Localization tab (default); Topic Localization tab (override) |Indicates that the topic can be assigned to a locale for HO. To set the docset default, select a value on the Docset-level Localization tab. New topics in the docset will automatically take this value. To override the default for a topic, set a different value on the topic Localization tab.
To Be Promoted Locales |Loc |? | |
To Be Staged Locales |Loc |? | |
TOC Name (source and locales)|Content |Topic |Indicates the name of the topic in the TOC, if different from the actual topic name. If set in en-US, this string is handed off in the metadata file for localization, along with title and keywords.| 
Topic Folder | | |The folder under the top-level Docset node in the portfolio. You can query to return all topics under any folder. This can be a docset, a docset TOC, any node in a docset TOC, or a docset's Not in TOC or Retired folder.
Topic Type (source and locales)| | |The topic template, such as DDUE.Conceptual, DDUE.MRef, DDUE.PowerShell, Markdown.GFM
Updated By Reflection |MRef|Topic|Indicates that an MRef topic was last updated by reflection/comment import, as opposed to hand authoring in CAPS.|
Visible Index Keyword |Text (tags)|Topic General tab|Specifies keywords for building an index in an offline file (.chm).
Writer |A user from the MS address book|General tab|(Workflow) The writer of the topic.

