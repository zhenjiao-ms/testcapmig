---
title: Creating and updating Markdown topics
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9a949b8c-f64e-4523-8aa6-b3bf19eed8d1
---
# Creating and updating Markdown topics
You can author in Markdown, using GitHub Flavor (GFM)! This is currently only supported for new conceptual topics that do not required localization.

In this topic

-   [Creating a Markdown topic](#CreatingMDtopic)

-   [Editing a Markdown topic](#EditingMDTopic)

-   [Authoring toolbar](#MDAuthoringToolbar)

-   [Floating help tool bar](#MDFloatingToolbar)

-   [Search and Replace](#MDSearchReplace)

-   [Inserting links in a topic](#MarkdownLinks)



-   [Inserting tokens in a topic](#MarkdownToken)

-   [Inserting videos in a topic](#MarkdownVideo)

-   [Inserting notes, warnings, etc.](#MarkdownNote)

-   [Basic MD validation upon check-in](#MDValidation)

## <a name="CreatingMDtopic"></a>Creating a Markdown topic
![](../Image/Create-Markdown-topic---1.png)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|If there are more topics in the docset, select a topic within a docset|
|![](../Image/Numbered-Callouts/callout2.png)|Click on **Add New**|
|![](../Image/Numbered-Callouts/callout3.png)|Select the location for the new topic with relation to the selected topic|
![](../Image/Create-Markdown-topic---2.png)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout4.png)|Select **New Topic**|
|![](../Image/Numbered-Callouts/callout5.png)|Give the topic a name|
|![](../Image/Numbered-Callouts/callout6.png)|In Template, select GFM.Markdown|
|![](../Image/Numbered-Callouts/callout7.png)|Click **Add**|

## <a name="EditingMDTopic"></a>Editing a Markdown topic
The new topic provides a readme to help author in Markdown. Replace the readme content with your own.

![](../Image/Editing-topic-Mardown---Toolbar-1.png)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|You can save a draft version of the topic to the server. Note that CAPS auto saves the topic every time you stop typing for 1 second.|
|![](../Image/Numbered-Callouts/callout2.png)|When you are ready to check-in your content into CAPS.|
|![](../Image/Numbered-Callouts/callout3.png)|If you do not want to check-in the content into CAPS.|
|![](../Image/Numbered-Callouts/callout4.png)|Click on **Switch View** to author the content in different ways. By default, you get the **Normal** view.|
|![](../Image/Numbered-Callouts/callout5.png)|**Side by Side** shows the editor on the left and the preview on the right. Preview gets updated as you type.|
|![](../Image/Numbered-Callouts/callout6.png)|**Full Size Editing** shows the editor in full screen|
|![](../Image/Numbered-Callouts/callout7.png)|**Full Size Preview** shows the preview in full screen. Ideal for topic review!|
You can use the toolbar for inserting elements quickly

You can also use the widget to see an online TOC, help syntax , or go to the top of the page.

## <a name="MDAuthoringToolbar"></a>Authoring toolbar
The authoring toolbar saves you time as it allows you to insert elements quickly, without having to type down the Markdown syntax.

![](../Image/MD-toolbar.png)

||||
|-|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|Setting text to bold|Ctrl+B|
|![](../Image/Numbered-Callouts/callout2.png)|Setting text to italic|Ctrl+I|
|![](../Image/Numbered-Callouts/callout3.png)|Inserting an internal or external link|Ctrl+Alt+L|
|![](../Image/Numbered-Callouts/callout4.png)|Inserting an image|Ctrl+Alt+G|
|![](../Image/Numbered-Callouts/callout5.png)|Inserting a token|Ctrl+Alt+P|
|![](../Image/Numbered-Callouts/callout6.png)|Inserting a table|Ctrl+Alt+T|
|![](../Image/Numbered-Callouts/callout7.png)|Inserting code sample|Ctrl+Alt+C|
|![](../Image/Numbered-Callouts/callout8.png)|Inserting a numbered list|Ctrl+Alt+O|
|![](../Image/Numbered-Callouts/callout9.png)|Inserting a bulleted list|Ctrl+Alt+U|
|![](../Image/Numbered-Callouts/callout10.png)|Inserting a horizontal line|Ctrl+Alt+R|
|![](../Image/Numbered-Callouts/callout11.png)|Insert headers|N/A as you need to choose which header to insert|
|![](../Image/Numbered-Callouts/callout12.png)|Undo the last action|Ctrl+Z|
|![](../Image/Numbered-Callouts/callout13.png)|Redo the last action|Ctrl+Y|

## <a name="MDFloatingToolbar"></a>Floating help tool bar
When you are authoring a Markdown topic in CAPS and **not using** the Normal view,  you get a floating toolbar with the following options. You can move the toolbar to any position you would like.

![](../Image/MD-floating-toolbar.png)

|||
|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|Markdown syntax help on most-common tasks|
|![](../Image/Numbered-Callouts/callout2.png)|In-topic Table of contents. You can click on any link to go to that section of the topic|
|![](../Image/Numbered-Callouts/callout3.png)|Go to the top of the topic|

## <a name="MDSearchReplace"></a>Search and Replace
In order to invoke the Search and replace dialog box, make sure you are in the editing window, otherwise you will bring up the Internet browser search window.

Press Crtl+F.

![](../Image/MD-Search-and-replace.png)

||||
|-|-|-|
|![](../Image/Numbered-Callouts/callout1.png)|Click on the arrow to open or close the Replace option|*Not available*|
|![](../Image/Numbered-Callouts/callout2.png)|Type the text to look for|*Not available*|
|![](../Image/Numbered-Callouts/callout3.png)|Click this option to enable or disable match case|*Not available*|
|![](../Image/Numbered-Callouts/callout4.png)|Click this option to enable or disable looking for the full word or not|*Not available*|
|![](../Image/Numbered-Callouts/callout5.png)|Click this option to enable of disable to use regular expressions in the **Find** text box|*Not available*|
|![](../Image/Numbered-Callouts/callout6.png)|Go to the previous match|Shift+F3|
|![](../Image/Numbered-Callouts/callout7.png)|Go to the next match|F3|
|![](../Image/Numbered-Callouts/callout8.png)|Click this option to search for only the content that is selected|*Not available*|
|![](../Image/Numbered-Callouts/callout9.png)|Type here the replacement text|*Not available*|
|![](../Image/Numbered-Callouts/callout10.png)|Click this option to replace the current match|*Not available*|
|![](../Image/Numbered-Callouts/callout11.png)|Click this option to replace all the matches|*Not available*|
|![](../Image/Numbered-Callouts/callout12.png)|Closes the Search and Replace dialog|*Not available*|

## <a name="MarkdownLinks"></a>Inserting links in a topic
To insert links to other topics and sites, click the link icon and select internal or external as appropriate.

To  create bookmarks to sections in the current topic or other topic, use link text. Bookmarks are added using this syntax: # &lt;a name="bookmark-name"&gt;Section Header &lt;/a&gt;

H2s (##) are automatically anchors, so you do not need to create bookmarks for them. The syntax for linking to H2s is link text.


## <a name="Inserting%links%to%images%in%a%topic"></a>Inserting images as links
You can insert an image that will be a live link when clicked. The syntax for linked images is:

[![image name](image-path)](link path)


## <a name="MarkdownToken"></a>Inserting tokens in a topic

1.  Make sure there is a token already created. See.

2.  Edit the topic.

3.  Insert the following: *[!TOKEN (../Token/&lt;tokenName&gt;.xml)]*, where *&lt;tokenName&gt;* is the name of the token.

    > [!TIP]
    > Token  name is case sensitive.

    > [!TIP]
    > If your token name has spaces, replace each  with a "+" sign.

    > [!TIP]
    > Example: *[!TOKEN (../Token/Visual+Studio+Long+Name.xml)]*

## <a name="MarkdownVideo"></a>Inserting videos in a topic
The current design support inserting YouTube video into markdown format by copying &amp; pasting embedded iframe from YouTube.

-   Go to the video in YouTube. For example [YouTube video](https://www.youtube.com/watch?v=iyT1uILEI2U).

-   In the YouTube page, click on **Embed** to get the corresponding iframe code.  In this case it would be *&lt;iframe width="420" height="315" src="https://www.youtube.com/embed/iyT1uILEI2U" frameborder="0" allowfullscreen&gt;&lt;/iframe&gt;*

-   Copy and paste the iframe and insert it directly into your Markdown topic to play the video directly in your content.

## <a name="MDValidation"></a>Basic MD validation upon check-in
We offer basic validation before check-in to ensure your content can publish and render correctly.  We will be adding more robust validation as we provide more support for Markdown in CAPS.

## <a name="MarkdownNote"></a>Inserting notes, warnings, etc.
There are different types of notes. The following is the syntax. The terms NOTE, WARNING, TIP, IMPORTANT and CAUTION, must be in **all capital letters**. In addition, do not indent the > more than three spaces.

The authoring:

```md
  > [!NOTE] Just a note to let you know...
 
  > [!WARNING] Do that again and I'll pout!
 
  > [!TIP] To write examples of markdown in markdown, use a code block (triple back tick).
 
  > [!IMPORTANT] This text is quite grand and notable.
 
  > [!CAUTION] This text is a little timid and is tiptoeing around.
```
Results in:

  > [!NOTE] Just a note to let you know...
  
  > [!WARNING] Do that again and I'll pout!

  > [!TIP] To write examples of markdown in markdown, use a code block (triple back tick).
 
  > [!IMPORTANT] This text is quite grand and notable.
  
  > [!CAUTION] This text is a little timid and is tiptoeing around.

## See also

-   [Managing topics](../Topic/Managing-topics.md)

-   [Grouping assets](../Topic/Grouping-assets.md)

-   [Deleting and Restoring content](../Topic/Deleting-and-Restoring-content.md)

