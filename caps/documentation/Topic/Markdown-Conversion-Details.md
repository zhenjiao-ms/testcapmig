---
title: Markdown Conversion Details
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 80671242-655c-4575-8e46-a3a08ea11f70
---
# Markdown Conversion Details
The CAPS migration team has provided a tool to convert DDUEML content to Markdown. Conversion happens in place -- it is not a migration. Upon conversion, a new version is created of each converted topic. The previous DDUEML version is still stored in the topic history. The tool also provides a rollback function.

This topic provides more detailed guidance for writers about preparing DDUEML content for effective conversion.

* [MarkDown Conversion Spec](https://microsoft.sharepoint.com/teams/Visual_Studio_China/ALPS/_layouts/15/WopiFrame.aspx?sourcedoc=%7b9362e70c-943f-4c73-98fb-8ec8364c692c%7d&action=edit&wd=target%28Feature%2Eone%7C8D9B85A8-F756-469A-BCEC-E0D72934BF12%2FMarkdown%20Conversion%20Spec%7C181BFC33-FD79-4F7A-AA60-E550298C5E60%2F%29). This spec lists the DDUEML source elements and their Markdown equivalents.

* [CAPS Markdown HTML whitelist](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-us/library/mt256124(msdn.10).aspx):  The CAPS Markdown implementation leverages the Github HTML whitelist to avoid security risks and other issues that can be caused by insecure or over-complicated HTML.

**NOTE:** if a topic contains more than 1 issue, the issues are reported on the same line, separated by ";" for example..
> **Warning: Some newlines were converted to \<br/>;** Warning: contains list in table; **Warning: contains note in table;** Skip: contains complicated table

## Quick Key
**Skipped:** The conversion tool leaves it in DDUML because converting to Markdown would result in content loss or garbage. Topics must be cleaned up before conversion. 
**Warning:** The conversion tool applies a workaround, such as converting notes to simple text, but topics should be reviewed if possible because content experience may be suboptimal. 
**Failure:** Conversion failed for some reason and needs investigation by VSC. These are rare, only been a few so far, all in VS. 

## SKIPS
Message  | Description / Action  
---------|---------
**Skip: Conversion can't resolve codeEntityReference** M:ReportService2010.ReportingService2010.GetProperties(System.String,ReportService2010.Property[]); | This was likley from an older report.  The tool has changed and we think this is now flagged as warning only and there is no action needed.         
**Skip: Have Reference Topic b65c74b6-889b-4323-9240-90827a70ab0e With Illegal Name**. Please remove / or \ in the name; | In MD, the topic name becomes the filename. The topic contains a link to another file whose name is bad.  For example " For more information, see Create/Edit Relationship Dialog Box (Analysis Services - Multidimensional Data)."  It seems like a good before running conversion reports to search the docsets for topic names with /. Another example found was "Lesson 4: Running the Application (VB/VC#)" changed that one to a -.         
**Skip: contains complicated table** | This results from nested tables. Edit the topic so there is only one level of tables         
**Skip: Have Reference Topic With Duplicated Name**. NamePath: [CREATE FUNCTION &#40;SQL Server   |   your topic links to a topic that is a duplicate title (but guids likely are unique Markdown does not allow duplicate titles (because title is filename of MD file). Update the title of one of targets    
Skip: contains token in \<code>     |  remove the token  
Skip: TopicId-f198afd7-a574-4029-bdad-e2f3c334a1d4-Locale-en-US is already MarkDown.     |    no action required    
Skip: Superscript     | as of 3/10/2016 - should not see these anymore. The tool has been updated so it actually converts in MD using HTML.
Skip: TopicId-034e8ae9-1979-4976-b0dd-755009f7aa3a-Locale-en-US mref is not supported.     |    correct - no action      

## WARNINGS

Message  | Description / Action  
---------|---------
Warning: Some newlines were converted to \<br/>;  | loc wants as many BRs as possible, review result.  common cause was when converting lists. Also, some older content contains a BR tag ![old_line_break](/Image/old_line_break.png)        
Warning: contains CodeEntity reference     |     Converts to regular links but in MD we lose the extra attributes that were possible in CAPS, IF ANY were used. The conversion is not detecting there were extra - unsupported attributes used so he warning is just letting you know in case you want to review.   
Warning: contains list in table    | change the list to just para or remove the table structure         
Warning: Unexpected link format detected: [TEXT]: LINK     |   ??      
Warning: contains note in table     |  process converts to normal para in bold.  warning is just an awareness so you can review how the result looks.   
Warning: contains not supported tag     |   how to identify the specific tag??   MEGAN is submitting a bug so the error message is updated or something else is added so we know what to fix.     
 
## Other issues, not flagged by pre-conversion
* Tables in MD require a header row.
