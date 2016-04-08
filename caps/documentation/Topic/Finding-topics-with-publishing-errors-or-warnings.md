---
title: Finding topics with publishing errors or warnings
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb3a9217-9653-4cf7-870c-6b16218da32f
author: Msstevenpo
---
# Finding topics with publishing errors or warnings


Sometimes, when you publish content, you'll get warnings or errors in the publishing report. And while you can scroll through the lengthy XML publishing report, there's an easier way to find the topics that didn't publish successfully: Staging Status.

Just create a query to find the topics that have issues:

![Create a new query](../Image/Create-Query-1.png)

<br/>
<br/>

And then query by Staging Status:

![enter image description here](../Image/queryForStagingIssues.png)
<br/>

Notes 
---



To find  |Query for  
---------|---------
Topics with warnings     | Staging Status = SucceededWithWarning         
Topics with errors       | Staging Status = Failed         


