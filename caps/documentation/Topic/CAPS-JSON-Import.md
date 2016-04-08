---
title: CAPS JSON Import
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b99b19a3-25b5-4777-adcb-1a3a1f58408f
---
# CAPS JSON Import
#RESTImport Plus#
##Tool Description##
The RESTImport+ tool is a little tool which imports content into CAPS to bulk import automatically. The input for the tool comes from swagger json files or markdown files. The RESTImport+ tool supports ddue and markdown conversion. The main purpose of the tool is to convert swagger json files to ddue or markdown and import content into CAPS after it was converted.


##Usage:## 
```
PestImport /s [<drive>:]<path> /n <Tenant Name> /p <Portfolio Name> /d <Docset Name> /t <Topic Template>
		
where
/s [<drive>:]<path> (required)
The name and location json or markdown files will be imported.

/n <Tenant Name> (required)
Provide a tenant name, like devint/ sandbox/ prod.

/p <Portfolio Name> (required)
Provide a portfolio name and please make sure the portfolio name has been already exist before run the tool.

/d <Docset Name> (required)
		Provide a docset name (system will create a new one if it does not exist).

/t <Topic Template> (optional)
The Support to import content templates, like DDUE.Conceptual/ Markdown.GFM/ …. Default is DDUE.Conceptual.
```
##Examples:##
```
{1} /s E:\RestImport\TestJSON /n devint /p MattWingTest /d TestDocset1 /t Markdown.GFM
```

[CAPS API Refference](CAPS-API-Reference.md)