---
title: DDUEML schema differences between DxStudio and CAPS
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8335ebd2-dac3-452f-a162-84c56a496326
---
# DDUEML schema differences between DxStudio and CAPS
DxStudio and CAPS shared pretty much the same DDUEML schema, although there are some differences as per the table below. These differences were the result of schema discussions and agreements during CLiX development and they have been inherited in CAPS.

|Schema file|CAPS DDUEML schema (v1.5)|DxStudio DDUEML schema (v1.3)|
|---------------|-----------------------------|---------------------------------|
|baseConditional.xsd|New element &lt;description&gt;||
|blockCommon.xsd|New element &lt;tokenblock&gt;||
|blockSoftware.xsd||Support &lt;token&gt; under &lt;codeElement&gt;|
|developer.xsd|Support &lt;tokenBlock&gt; under &lt;developerHowToDocumentType&gt;<br /><br />Support &lt;description&gt; under &lt;developerConceptualDocumentType&gt;<br /><br />Support for PowerShell: under &lt;cmdletParameter&gt; add **workflowParameters** optional Boolean attribute||
|structure.xsd|Support &lt;tokenBlock&gt; under group **structureGroup**|Group **structureGroup** (seems not used)|
|structureTable.xsd|These Elements under &lt;table&gt; are different:<br /><br />&lt;caption&gt;<br /><br />&lt;thead&gt;&lt;tbody&gt;<br /><br />New attribute **border**|&lt;title&gt;<br /><br />&lt;tableHeader&gt;<br /><br />&lt;row&gt;|
