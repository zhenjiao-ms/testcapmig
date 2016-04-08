---
title: Managing docsets
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc59db49-77a4-4227-878a-8bf2e8ae4575
---
# Managing docsets
Note that not all users can create or manage docsets. Please see [Permissions](../Topic/Permissions.md).

In this topic:

-   [Creating a docset](#CreatingDocset)

-   [Updating docset metadata](#updatedocsetmetadata)

-   [Sharing a docset](#SharingDocset)

-   [Referencing to another topic in a different portfolio (or outside CAPS)](#ReferencingExternalTOC)

## <a name="CreatingDocset"></a>Creating a docset

1.  Click to create a new docset. Note that in the same docset you can have both DDUEML and Markdown content.

    ![](../Image/CreateNewDocset.png)

2.  Select Conceptual or Mref and give the docset a meaningful name (for mref, you will be asked to provide additional information -- see [Reflection and Comment Import](../Topic/Reflection-and-Comment-Import.md)).

3.  Click **Create**.

4.  Your new docset will appear in the list of docsets. The docset is created with three subfolders:

    1.  **TOC** - These topics will be published to the MSDN/Technet Table of Contents.

    2.  **Not in TOC** - These topics will be published and can be linked to, but will not be in the TOC.

    3.  **Retired content**s - These topics will be retired from MDSN/TechNet.

5.  You can now add topics to your docset.

## <a name="updatedocsetmetadata"></a>Updating docset metadata
First, check out [Docset Metadata](../Topic/Docset-Metadata.md) to understand what you can and should set with regard to docset metadata. Most important of all metadata settings at the docset level is the **Product Family** and **Product Family Version**. Make sure you get these two right.

Ok, now you're ready to set some metadata:

1.  In CAPS, click the docset you want to set metadata for.

2.  You'll see the following Publishing metadata information:

    ![](../Image/Docset-metadata.PNG)

3.  Make your changes - set the metadata values - and then click **Save**.

Ta da. Docset metadata, handled.

## <a name="SharingDocset"></a>Sharing a docset
You share one docset into another docset by adding a reference to the shared docset.

![](../Image/SharingDocset.png)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|Expand the TOC for the docset that you want to share another docset into|
|![](../Image/Numbered-Callouts/callout2.png)|Right-click a topic in the TOC where you want   the shared docset to appear, and then select a command to add the docset as a node: **Add node as a child**, **Add node before**, or **Add node after**.|
|![](../Image/Numbered-Callouts/callout3.png)|In the **Add** dialog box, click **Docset**.|
|![](../Image/Numbered-Callouts/callout4.png)|Select the docset that you want to share in.|
|![](../Image/Numbered-Callouts/callout5.png)|Select one of the root nodes in the docset, and click **Add**.|

## <a name="ReferencingExternalTOC"></a>Referencing to another topic in a different portfolio (or outside CAPS)
You can point to another topic in a different portfolio or outside CAPS. If the topic has children, all the children will be included as a reference in the TOC. Here is how.

![](../Image/Link-to-external-content.png)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|Expand the TOC for the docset that you want to share another docset into|
|![](../Image/Numbered-Callouts/callout2.png)|Right-click a topic in the TOC where you want   the shared docset to appear, and then select a command to add the docset as a node: **Add node as a child**, **Add node before**, or **Add node after**.|
|![](../Image/Numbered-Callouts/callout3.png)|In the **Add** dialog box, click **External topic**.|
|![](../Image/Numbered-Callouts/callout4.png)|**Name** - Enter the name for the target topic. CAPS cannot resolve the topic title for you, so enter the name as it will show in the TOC.|
|![](../Image/Numbered-Callouts/callout5.png)|**Topic GUID** - This is the GUID of the target topic.|
|![](../Image/Numbered-Callouts/callout6.png)|**TOC GUID** - This is the TOC GUID of the target topic.|
|![](../Image/Numbered-Callouts/callout7.png)|**Product Family** - The product family of the target topic.|
|![](../Image/Numbered-Callouts/callout8.png)|**Product Version** - The product family version of the target topic.|
|![](../Image/Numbered-Callouts/callout9.png)|Click **Add** when you are finished.|
