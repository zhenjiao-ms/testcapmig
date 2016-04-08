---
title: Publishing individual topics to MTPS
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1cfa3651-93d1-454d-8c03-685028a04adf
---
# Publishing individual topics to MTPS
> [!IMPORTANT]
> Before you can publish topics, make sure you set up the mandatory attributes. See [Publishing a full docset to MTPS](../Topic/Publishing-a-full-docset-to-MTPS.md).

## <a name="TopicAttributes"></a>Understanding attributes and topic publishing
This section contains information about how to set up the topic attributes and an explanation of the publishing options.

### How to set the topic attributes

1.  Select the topic or topics you would like to publish.

2.  If the topic is a parent topic and you would like to publish all its children, click on **Select Child Nodes**.

3.  Go to the  **Publishing** section.

4.  You can set different attributes at the topic level, individually or in bulk. The following is not an exhaustive list, just the mandatory attributes and those to watch out for.  For a full description of the available attributes, please see [Topic Metadata](../Topic/Topic-Metadata.md).

    |Attribute name|Optional or required for MTPS publishing|
    |------------------|--------------------------------------------|
    |**Ready to Stage**|Required if you are publishing content to stage|
    |**Ready to Publish Live**|Required if you are publishing content to live|
    |ms.devlang|Required|
    |ms.topic|Required|
    |Preferred Site|Optional. It is recommended you set up this attribute at the docset level.|
    |Preferred Library|Optional. It is recommended you set up this attribute at the docset level.|

5.  Click **Save** to make sure you save your changes before publishing.

### <a name="PubTopic"></a>Understanding the publishing options

1.  Under **Content** the only option available is **Seleted topic(s)**. This will publish all the topics selected and their TOC information.

2.  Under **Publish to** select

    -   **Staging** - To publish the topic(s) to staging.

    -   **Live** - To publish the topic(s) to live.

3.  **Publish all changed and unchanged topics**

    -   *Unchecked* - To publish only the topics that changed since the last time that were published last.

    -   *Checked* - To publish all the topics regardless of whether they have changed or not since they were published last. This is useful when the content does not get published to MTPS even if it has changed.

4.  Under **Locales** select

    -   **en-us** - To publish English content.

    -   **Non en-us** - To publish localized content. Then select the locales you would like to publish.

5.  **Force ready**. This is only show if you select a different locale than en-us.

    -   *Unchecked* - To publish to stage or live only the topics that have the corresponding **Ready to Stage** or **Ready to publish live** option turned on.

    -   *Checked* - To override the corresponding **Ready to Stage** or **Ready to publish live** flag  and publish all the topics in the docset to stage or live, depending on your preference.

6.  Click **Publish** once you are ready to publish.

7.  You can see the publishing status in the topic **Publishing** panel, by clicking on View Details link next to **Topic in staging** or **Topic in live**.

8.  Download the publishing report if you need more details.

If publishing succeeds with warnings or if publishing fails, consider [Finding topics with publishing errors or warnings](../Topic/Finding-topics-with-publishing-errors-or-warnings.md).

## Topic publishing scenarios
This section contains information about different publishing scenarios

### Publishing a new or updated topic
You only need to publish the topic and the TOC contents of the new/updated topic. No need to publish the parent topic.

> [!NOTE]
> Describe Issue with TOC sssssssssssssssssssssssssssssssss

1.  Set topic attributes.

2.  Set **Ready to Stage** flag for new topic.

3.  Publish new topic  to stage.

4.  Validate your content on stage.

5.  Set **Ready to Publish Live** flag for new topic.

6.  Publish new topic to live.

7.  Validate content and TOC on live.

### Publishing a topic moved in the TOC
> [!NOTE]
> Describe Issue with TOC sssssssssssssssssssssssssssssssss

1.  Set topic attributes.

2.  Publish former parent TOC to stage.

    > [!NOTE]
    > You do not need to set the flag for TOC changes only. See [Understanding publishing to MTPS](../Topic/Understanding-publishing-to-MTPS.md).

3.  If topic content has changed, set **Ready to Stage** flag for moved topic.

4.  Publish topic to stage.

5.  Validate content an TOC on stage.

6.  Publish former parent TOC to live.

    > [!NOTE]
    > You do not need to set the flag for TOC changes only. See [Understanding publishing to MTPS](../Topic/Understanding-publishing-to-MTPS.md).

7.  Set **Ready to Live** flag for moved topic.

8.  Publish topic to live.

9. Validate content and TOC on live.

### Publishing a topic moved from the TOC to Not in TOC
> [!NOTE]
> You do not need to set the flag for TOC changes only. See [Understanding publishing to MTPS](../Topic/Understanding-publishing-to-MTPS.md).

1.  Move topic from TOC to Not In TOC.

2.  Publish former parent TOC to stage.

3.  Publish former parent TOC to live.

