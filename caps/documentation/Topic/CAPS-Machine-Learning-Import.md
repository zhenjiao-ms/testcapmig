---
title: CAPS Machine Learning Import
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a2721081-f438-4d83-bde7-d685dc836050
---
# CAPS Machine Learning Import
#MLCapsImport#
##Tool Description##
The MLCapsImport tool is a little tool which import Machine Learning file into CAPS to blk import automatically. The input for the tool comes from Machine Learning files and separate machine learning .aml files detailed below. The machine learning import capability was imported into the CAPS after it was converted. The main purpose of the tool is to import and migrate PS projects. 

##Command Line Syntax##
The command line syntax for Machine Learning import is as follows:

##Usage:## 
```
MLCapsImport /s [<drive>:]<path> /n <Tenant Name> /p <Portfolio Name> /d <Docset Name> /switchif <true, false>
		
where
/s [<drive>:]<path> (required)
The name and location json or markdown files will be imported.

/n <Tenant Name> (required)
Provide a tenant name, like devint/ sandbox/ prod.

/p <Portfolio Name> (required)
Provide a portfolio name and please make sure the portfolio name has been already exist before run the tool.

/d <Docset Name> (required)
		Provide a docset name (system will create a new one if it does not exist).

	/switchif <true, false> (optional)
		Check if the topic need to be updated when the same GUID is exist…. Default is false.
```
##Examples:##
```
{1} /s D:\Dxplatform\Personal\v-matwin\MLCapsImport\MLCapsImport\TestML /n devint /p "Test" /d "Test" /switchif true
```
[CAPS API Refference](CAPS-API-Reference.md)