---
title: CAPS Bulk Topic Stubbing
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b4769395-6b16-4c04-9809-82d9ffe7e7ae
---
# CAPS Bulk Topic Stubbing
##CapsTopicStubbing Process##
###Tool Description###
The CapsTopicStubbing tool is a little tool which will bulk create topics of required GUID, title, content if provided in CAPS. The input for the tool comes from definitions of GUID, title, content in the manifest file. The main purpose of the tool is to stub topics of GUID and title. 
Command Line Syntax
The command line syntax for CapsTopicSubbing is as follows:

###Usage:### 
```
CapsTopicStubbing /n <Tenant Name> /p <Portfolio Name> /d <DocSet Name> /m <Manifest Name the specified>
```
		
###where###
```
/n <Tenant Name> (required)
Provide a tenant name, like devint/ sandbox/ prod.

/p <Portfolio Name> (required)
Provide a portfolio name and please make sure the portfolio name has been already exist before run the tool.

/d <Docset Name> (required)
Provide a docset name and please make sure the docset name has been already exist before run the tool.

/m < Manifest Name the specified > (required)
Provide a manifest name you specified and please make sure the specified file is existing before run the tool. In the manifest file, you can add title, GUID, path for topics definition you wanted. 
```
###Example:###
```
{1} /n devint /p Yingda.Test /d Testing0820 /m "DocSetName.CreateManifest.xml"
```
[CAPS API Refference](CAPS-API-Reference.md)