---
title: [GET] Get blob info by article id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6b0663d0-2ccf-480e-8fc5-95bf00b1bff9
---
# [GET] Get blob info by article id
**Status:** Exists (dependency).
 
**Dependency area:** ad hoc tooling.
 
**Impact:** CSI.
 
**API type:** GET.
 
**Data to pass/receive:** 

**input	Api url:**
```
 /v1/Projects/{projectid}/Articles/(articleid}?locale=en-US
```
 
**e.g. :** 
```
https://caps-api-devint.azurewebsites.net/v1/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/Articles/guid5?locale=en-US
```
**output**
```
	[
  {
    "locales": [
      {
        "children_url": "https://caps-api-devint.azurewebsites.net/v1/projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/articles/guid5:(children)",
        "locale": "en-US",
        "default_locale": "en-US",
        "parent_id": "6c294e7c-1c1b-4562-bd08-b7ca24e2a957",
        "blobs": [
          {
            "blob_id": "guid5-521898563",
            "created_at": "2015-08-24T07:56:56Z",
            "created_by": "4422b87327c34d3b84941e0fd91a5a2a",
            "updated_at": "2015-08-24T07:57:02Z",
            "updated_by": "4422b87327c34d3b84941e0fd91a5a2a",
            "revision": 4,
            "blob_type": "BuildInternal",
            "filesize": 0,
            "word_count": 0,
            "content_url": "https://caps-api-devint.azurewebsites.net/v1/projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/articles/guid5:(blobcontent(BuildInternal))?locale=en-US"
          },
        ….
    ]
  }
]
 ```
**Tool(s):** MLCapsImport

**Example**
