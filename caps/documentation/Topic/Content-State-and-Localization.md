---
title: Content State and Localization
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b77065e2-5e87-4a2b-b142-f337a780253f
---
# Content State and Localization
For CSI projects that will be localized, the localization team will primarily use publishing state to determine which topics should be included in a handoff. The model will vary according to whether the release is for a specific milestone (simship or non-simship release) or for continuous publishing (cpub). The following sections describe how loc. will determine the content to include in handoffs for each case.

## Milestone releases
When **Ready to Stage** is set to True, it indicates that the content is a reasonably solid draft that localization can use for early loc. handoffs during milestone releases. Files in this state don't have to be complete or polished, but they should not contain placeholder content or be in a clearly raw condition. The **Ready to Stage** = True setting indicates to loc. that the topic is in “decent enough” shape for at least an initial translation pass, even if the topic will continue to churn. Since the **Ready to Stage** flag stays True after staging, there is no further work item for writers. After a topic publishes live, the **Ready to Publish Live** flag resets back to **Ready to Stage** = True.

Due to cool CAPS functionality, loc. will only pick up topics that are new or updated since the last loc. handoff. CAPS also has built-in safeguards to prevent localized content from publishing until after the en-US version has published. As a result, loc. doesn't need to rely on topic workflow states like "Content Complete" to identify topics for handoff. They will simply pick up new versions of a topic when it changes, as long as it's set as ready to stage.

Note that in CAPS, you don't have to check in content to save draft work or preview it. You can save a copy of your file to the server cache instead, and access that copy from any machine. Localization will only use content for milestone releases that has been both checked in and marked as ready to stage.

### Non-simship releases
Writers can write until the day of release. Loc. will hand off all “ready to stage” content until the release date, and will then run a separate query for all content published to live on the release date to catch up on the last changes.

### Simship releases
Simship releases are very rare. When they do happen, loc. and the content owner will agree on a “lockdown/freeze” date, to allow localization to catch up localizing the content so it can go live on the same date.

## Continuous publishing releases
This is the most frequent type of release for localization. Loc. will pick up all topics that have been published to Live for en-US.  The CAPS FY16 Q1 release contains a new feature request that will allow loc. to query for these topics to find the published version of a topic (not the latest/newest, but the published version).

## See Also
[Understanding publishing to MTPS](../Topic/Understanding-publishing-to-MTPS.md)

