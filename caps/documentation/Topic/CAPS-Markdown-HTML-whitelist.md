---
title: CAPS Markdown HTML whitelist
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1022bb31-3550-4960-a5ca-d8edce025e2b
---
# CAPS Markdown HTML whitelist
The CAPS Markdown implementation leverages the Github HTML whitelist to avoid security risks and other issues that can be caused by insecure or over-complicated HTML. 

The Github HTML whitelist that forms the basis of the CAPS whitelist can be found here: [HTML sanitation](https://github.com/jch/html-pipeline/blob/master/lib/html/pipeline/sanitization_filter.rb) 

While CAPS has the ability to support the entire Gihub Markdown whitelist, the whitelist is configured to allow, warn, or error (blocking checkin) based on content guidelines set by the organization. 

The following shows the Github HTML whitelist with the default rules for CAPS. Note that HTML not in the whitlist is not allowed in CAPS and will block checkin.


Type  |Element(s)  |CAP Default Rule
---------|---------|--------
Headings     |  h1, h2, h3, h4, h5, h6, h7, h8  |**Error**. Use Markdown headings heads (e.g. ## H2) instead.     
Prose     |  p | Warn. If possible, use Markdown returns.
Prose | div, blockquote |**Error**. Use Markdown blocks (>) instead.      
Formatted     |   pre  | Warn. Avoid.   
Inline | strong, em | Allowed. These are the recommended tags for bold and italic text within HTML segments. Outside of HTML, you should use standard Markdown for bold and italics.
Inline | b, i | Warn. Within HTML, use strong and em. Outside HTML, use standard Markdown.
Inline     |     tt, samp, q | **Error**. Use standard Markdown formatting instead.
Inline | ins, del, kbd, var  | Warn. Use standard Markdown when possible.
Inline | code, sup, sub | Allowed.
Lists     |   ol, ul, li, dl, dt, dd  | Warn. Use simple Markdown lists when possible.    
Tables     | table, thead, tbody, tfoot, tr, td, th   | Warn. Use simple Markdown tables when possible.     
Breaks     |   br | **Error**, except in Markdown tables.
Breaks | hr    | Allowed (?)  
Ruby (East Asian)     |   ruby, rt, rp     | **Error**. 



The following attributes, organized by element, are whitelisted for Github. The CAPS rules are shown below.



Element  |Attributes  | CAPS Default Rule
---------|--------- |-------
a     |      href (http://, https://, mailto://, github-windows://, and github-mac:// URI schemes and relative paths only)   | Allowed.
img     |     src (http:// and https:// URI schemes and relative paths only)    |**Error**. img is not allowed.
div     |     itemscope, itemtype    | **Error**. div is not allowed.
All     |     abbr, accept, accept-charset, accesskey, action, align, alt, axis, border, cellpadding, cellspacing, char, charoff, charset, checked, cite, clear, cols, colspan, color, compact, coords, datetime, dir, disabled, enctype, for, frame, headers, height, hreflang, hspace, ismap, label, lang, longdesc, maxlength, media, method, multiple, name, nohref, noshade, nowrap, prompt, readonly, rel, rev, rows, rowspan, rules, scope, selected, shape, size, span, start, summary, tabindex, target, title, type, usemap, valign, value, vspace, width, itemprop  | **Error**. Not allowed.  

  

Note that the id attribute is not whitelisted.

  
