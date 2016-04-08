---
title: Creating offline content
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 85fe4253-30de-4ed8-9542-7a9d83cb941a
---
# Creating offline content
> [!IMPORTANT]
> Publishing will fail if it takes longer than an hour. This important to know when creating offline builds for large docsets, CAPS might return a timeout error.

**In this topic**

-   [Creating a CHM out of the full docset](#CHM)

-   [Creating a Word document out of the full docset](#Word)

## <a name="CHM"></a>Creating a CHM out of the full docset
CHM files can only be created at the docset level. You can only publish a docset at a time. You could share a docset into another docset and create a combined CHM. See [Sharing a docset](../Topic/Managing-docsets.md#SharingDocset).

1.  Select the docset

2.  Click on **Publishing**

3.  Click on **Publishing as  offline file**

4.  Under  **Content** select **CHM**.

5.  Select the locale you would like to publish

6.  Click on **Publish**

7.  The **Publishing** pane will show the progress of the CHM creation.

8.  Once it is finished, go to the  **Publishing status** section and expand **CHM**.

9. Click on **Download Report** to get the publishing report

10. To download the file, click on **Download**. The file is delivered in a ZIP file. Save the file to your machine and extract the CHM file from the ZIP file.

11. If you cannot see the file contents, right-click on the CHM file and select **Properties**. In the **General** tab, click Unblock and then **OK**.

## <a name="Word"></a>Creating a Word document out of the full docset
Word files can only be created at the docset level. You can only publish a docset at a time. You could share a docset into another docset and create a combined CHM. See [Sharing a docset](../Topic/Managing-docsets.md#SharingDocset).

To create a Word file for one topic only, see [Downloading a topic](../Topic/Managing-topics.md#bmkm_downloadtopic).

1.  Select the docset

2.  Click on **Publishing**

3.  Click on **Publishing as  offline file**

4.  Under  **Content** select **DOCX**.

5.  Under **TOC level**, select

    -   **entire** to create a full TOC within the Word document

    -   A number between 1 and 10 to indicate the depth level for the TOC within the Word document;

6.  The **Publishing** pane will show the progress of the CHM creation.

7.  Once it is finished, go to the  **Publishing status** section and expand **DOCX**.

8.  Click on **Download Report** to get the publishing report.

9. To download the file, click on **Download**. The file is delivered in a ZIP file. Save the file to your machine and extract the Word  file from the ZIP file to open it and see its contents.

