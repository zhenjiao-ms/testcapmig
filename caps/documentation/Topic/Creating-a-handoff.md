---
title: Creating a handoff
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f67aed1c-f43e-4bc1-b656-5e8141075133
---
# Creating a handoff

## Creating a handoff

1.  Select the topics that you would like to handoff. You can do that via query or doing single or multiple selection of the topics. Make sure you already run the steps listed in the [Identifying and marking content for localization](../Topic/Identifying-and-marking-content-for-localization.md) topic.

2.  Click on the **Localization** link.

3.  In the **PREPARE HANDOFF** section of the **Localization** Tab choose the handoff type, **Human Translation** or **Machine Translation**. Note:   You can do a handoff for either type but not both types at the same time.

4.  Select desired Dependency option.  Click on the **With Dependency** check box if you want your handoff to include the images and tokens your topic links to.  Linked topics are not included in the handoff unless they are already part of your handoff topic set.

5.  Select the **Force Handoff** checkbox if you want your handoff to include all topics and dependent Image and Token files even if they haven't been updated since the last handoff.

6.  Click on the **Scope Handoff** button to review your handoff information.  CAPS displays the handoff summary information below the **Scope Handoff** button in the **Localization** Tab. Note:  CAPS by default only includes files that have been updated since the last handoff.  Reviewing the summary information is important to make sure your handoff includes the desired files.

7.  Click on the **Download Details** button to download handoff details and review the handoff data if desired.

8.  Click on the **Create Handoff** button.

9. Give the handoff a name. Click on **Next**.

10. Verify that your handoff settings are correct - **Translation Type, With Dependency and Force Handoff**.

11. Select the locales you would like to handoff. Click on **Next**.

    In the next dialog, select which content you would like to include in your handoff:

    -   **All** - To handoff all the entities.

    -   **Topic** - To handoff the topic contents.

    -   **Topic metadata** - To handoff the topic metadata of the topics. Note that content and metadata are stored in a single file, so if you handoff topics and topic metadata, you will receive just one file per topic.

    -   **Image** - To handoff all the images referenced by the topics.

    -   **Image metadata** - To handoff the media metadata (Alternative Text: ALT Text).

    -   **Token** - To handoff the tokens referenced by the topics.

    > [!IMPORTANT]
    > -   Tokens do not have any metadata that needs localization, thus Token metadata is not presented as an option to handoff.

12. Once you have made your selection, click on **Create** button.

13. The handoff will be created in the **Handoff** section.

14. If nothing fails, the Handoff Status will be **Succeeded**. Otherwise, it might show errors. If that is the case, click on the **Download Report** link.

15. Click on **Download Package** link to copy the handoff package into your machine.

## Handoff package
The handoff package will be compressed in a ZIP file.

-   **Manifest.XML** - This is the file that contains all the contents of the handoff package.

-   handoff_name folder - This folder has all the contents of the handoff, structured in the following way:

    -   Locales  - you will see a folder per locale

        -   **topic** - this folder contains all the topics included in the handoff, in a flat structure.

        -   **image** - this folder contains the online file, the image metadata, and any source files if any.

        -   **token** - this folder contains the tokens in a flat structure.

