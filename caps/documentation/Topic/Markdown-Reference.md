---
title: Markdown Reference
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fbe5a734-a026-46e4-a58b-80f44eabf731
---
# Markdown Reference

CAPS is using "GitHub Flavored Markdown" (GFM). This topic is a basic reference. For more details, see the following articles on GitHub: [Markdown Basics](https://help.github.com/articles/markdown-basics/), [Github Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/), [Online sample](http://github.github.com/github-flavored-markdown/sample_content.html)
  
### Quick Assistance
When you are authoring your Markdown content in CAPS, you can get assistance in different ways:
- Use Alt+F1 in IE or F1 in Chrome and Edge to open the **Command Palette**
- Use Ctrl+SPACE to open the **Insert** menu
- Use authoring tool bar on the top of the editor to help create your content

## Format your content

### Paragraphs
Paragraphs in Markdown are just one or more lines of consecutive text followed by one or more blank lines.
  
```
On July 2, an alien ship entered Earth's orbit and deployed several dozen saucer-shaped "destroyer" spacecraft, each 15 miles (24 km) wide.
  
On July 3, the Black Knights, a squadron of Marine Corps F/A-18 Hornets, participated 
```

### Headings  
Add a header using the dropdown list provided in the authoring toolbar, or add a '`---`' or '`===`' in the  line under your section title. You can also create a heading by adding one or more hash (`#`) symbols before the heading text. The number of hashes determines the heading level.

  ```

    ## The  largest in-topic heading (renders as <h2>)
    ...
    ###### The 6th largest heading (renders as <h6>)
  ```
Note that you cannot add H1s (#) within the Markdown topic in CAPS. H1 is a meaningful HTML tag for SEO, and only one is allowed per topic. In CAPS, this is built from the Name of the topic on the General tab.

### Block Quotes
Indicate block quotes with a `>`.
  ```
    In the words of Abraham Lincoln:
  
    > Pardon my French
    > Second line of the quote
  ```

### Styling Text
Make your text **Bold** or *italic*
  ```
    **This text will be bold**
    *This text will be italic*  
  ```
You can also use the authoring toolbar to achieve this.

### Lists
Create unordered list by preceding list items with `*` or `-`
  ```
  * Item
  * Item
  * Item
  
  - Item
  - Item
  - Item  
  ```
Create ordered lists by preceding list items with a number.
  ```
  1. Item 1
  2. Item 2
  3. Item 3  
  ```
Create nested lists by indenting list items by two spaces.
  ```
  1. Item 1
    1. A corollary to the above item.
    2. Yet another point to consider.
  2. Item 2
    * A corollary that does not need to be ordered.
      * This is indented four spaces, because it's two spaces further than the item above.
      * You might want to consider making a new list.
  3. Item 3 
  ```
 
### Code Formatting
Use triple ticks (```) to format text in a code block.
~~~~
Check out this neat program I wrote:  
```
  x = 0
  x = 2 + 2
  what is x
```
~~~~
is rendered as:

  Check out this neat program I wrote:  
  ```
    x = 0
    x = 2 + 2
    what is x
  ```

### Links
Create an inline link by wrapping link text in brackets `[Link Label]`, and then wrapping the link target in parentheses `(http://URL)`. For example:
``` 
  [Bing.com](http://www.bing.com)
```  

You can also create a link to an existing topic in CAPS with the authoring toolbar
  
### Images
Include an online image from an external resource by using `![Image Label]`, and then wrapping the image resource url in parentheses `(http://ImageURL)`
  
You can also insert an image from CAPS with the authoring toolbar.

### Tables
Create tables by defining a heading row, separating columns with a pipe `|` character.
```
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell
```
You can include inline Markdown in the cells such as links, bold, italics, or strike through. For example:
```
| Name | Description |
| ---- | ---- |
| Help | ~~Display the~~ help window.|
| Close | _Closes_ a window     |
```

More formatting control is obtained by including colons (`:`) within the header row. You can define text to be left-aligned, right-aligned, or center-aligned:
```
| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |
```
A colon on the **left-most** side indicates a left-aligned column; a colon on the **right-most** side indicates a right-aligned column; a colon on **both** sides indicates a center-aligned column.

### HTML
You can use a subset of HTML within your content. A full list of our supported tags and attributes can be found on GitHub [HTML Sanitization](https://github.com/github/markup/tree/master#html-sanitization)


  
