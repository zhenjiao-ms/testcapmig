---
title: [POST] Upload content into blob
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c9a6feae-fefe-4995-b447-5ef09def1ae1
---
# [POST] Upload content into blob

Wednesday, August 12, 2015  
5:55 PM

**Description:** Upload content into blobs  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/blobs/{blobid}?locale=en-US  
](https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/blobs/{blobid}?locale=en-US)  

**URL Parameters:**  

    Repositoryid: (project id in CAPS)  
    Blobid  
      
    -----------------------------7df25d1330476  
    Content-Disposition: form-data; name="BlobData"  
    …  
    Content  
    …  
    -----------------------------7df25d1330476--  

	  

**Note:**  

	Contenttype: multipart/form-data; boundary=---------------------------7df25d1330476  

  
**Sample Request 1:** 

	POST https://caps-contentrepository-devint.cloudapp.net/v1/repositories/811c88a0-c18f-497d-b20b-2185cc2bb79c/entities/blobs/ddb686e5-249e-4372-8af6-d3f5a4f3675c?locale=en-US  

**Sample Response 1:**  

	"ddb686e5-249e-4372-8af6-d3f5a4f3675c"