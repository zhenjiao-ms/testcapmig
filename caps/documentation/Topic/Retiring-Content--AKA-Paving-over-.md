---
title: Retiring Content (AKA Paving over)
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8ff7e00d-fd2a-433f-a550-c3556d2c5c87
---
# Retiring Content (AKA Paving over)



Retiring content removes the topic content from MTPS and either redirects it to a specified URL or provides standard error text theat the topic is no longer available. With a single retiring content action, the content is retired from both Stage and Live for all locales.

You can manually retire any conceptual topic. For managed reference, topics are automatically moved to Retired when they are removed from DLLs and re-reflected; you cannot otherwise retire an mref topic.

Retiring content and deleting content is not the same. Retiring replaces the content in MTPS with a redirection or standard placeholder. Deletion is to remove the content form the CMS. See  [Deleting and Restoring content](../Topic/Deleting-and-Restoring-content.md).

> [!IMPORTANT] When you are in the Retired contents section, both the **General** and **Localization** tabs will be disabled,  so you cannot change topic or localization properties here.

You can only retire content if it has been published already. Otherwise, when attempting to retire, CAPS will return an error message in the publishing report indicating that the topic was not published, hence, cannot be retired. In that case, you can simply delete the topic from the CMS.

## Steps

1.  Select the topic(s) you would like to retire. 
2.  Right-click and select **Retire**. Click on **Yes** on the confirmation message. The topics get moved to the **Retired contents** section.
    > [!NOTE] If you are trying to retire a parent topic, the parent and all the children topic will be retired. If you would like only to retire the parent, move the children to the TOC section where they will be from now on, and then, move the parent topic to the **Retired contents** folder.

3.  Go to the **Retired contents** section.

4.  Select one ore more topics. An exclamation mark before the topics indicates that the topics have not been retired (via Publishing) yet.

5.  Click on **Publishing**. 

6. Select from the following options for **Redirect URL**:

    -   **None** - Text will be displayed indicating that the content is no longer available.

    -   **External URL** - Topic will be automatically redirected to the specified URL.

    -   **Internal Topic** - Topic will be automatically redirected to another topic within the portfolio.

6.  If you add or change a redirection URL, click **Save**.

7.  When you are ready, click  **Publish**. A message asking you to confirm the content retirement appears.

    -   The content will removed from stage and live at the same time.

    -   All locales will be retired at the same time.

8.  Validate contents look good on stage or live.


> [!IMPORTANT] This process does not update the TOC. So you need to select the TOC nodes that contained the topics you retired and publish the outline. You can do this before or after you retired the content from MTPS. The localized TOC should also publish their TOC, so please make sure you let the localization team know about this.

## See Also
[Unretiring Conceptual Topics](../Topic/Unretiring-Conceptual-Topics.md)

