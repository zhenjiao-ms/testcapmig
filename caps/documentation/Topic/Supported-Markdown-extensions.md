---
title: Supported Markdown extensions
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7555b849-f6b7-4f96-a3ce-b740cf202146
---
# Supported Markdown extensions
This topic describes the extensions to Github Flavored Markdown supported by CAPS. CAPS supports both general and Azure (when applicable) extension syntax, shown below. Currently, general and Azure syntax render the same when built from CAPS, but this may change in the future. S 

## Alerts
Alerts create highlight a block of text to draw the reader's attention to important information.

Use a note to  highlight neutral or positive information that emphasizes or supplements key points of the main text.
```
> [!NOTE] Note text goes here
> [AZURE.NOTE] Note Text goes here
```

> [!NOTE] This is what a note looks like when built out of CAPS.

Use warnings to alert the user to a condition that might cause a problem in the future. For example, selecting a certain option might permanently lock the user into a particular scenario.

```
> [!CAUTION] Warning text goes here
> [AZURE.WARNING] Warning text goes here
```

>  [!CAUTION] This is a CAPS warning.

Use tips to help users apply the techniques and procedures described in the text to their specific needs. A tip might also suggest alternative methods that may not be obvious. Tips are not essential to the basic understanding of the text.

```
> [!TIP] Tip text goes here
> [AZURE.TIP] Tip text goes here

```
> [!TIP] Here's a tip!

Use important to provide information that is essential to the completion of a task.

```
> [!IMPORTANT] Important text goes here
> [AZURE.IMPORTANT] Important text goes here

```
> [!IMPORTANT]  This is important.

You can include multiple paragraphs in an alert as follows:


```
> [!NOTE] This is the first paragraph! Next add a line with just ">", as follows:
>
> Then add your second paragraph.
```

It renders like this:

> [!NOTE] This is the first paragraph! Next add a line with just ">", as follows:
>
> Then add your second paragraph.

