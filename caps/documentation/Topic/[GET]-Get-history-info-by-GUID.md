---
title: [GET] Get history info by GUID
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bb7001fe-2391-4399-9fc0-6e39a3a1640d
---
# [GET] Get history info by GUID
**Description:** Get history info by GUID

**API type:** GET

**URI:** v1/Projects/{ProjectID}/Articles/{ArticleID}/Histories?locale=en-US&pageSize=99999&pageToken= 


**Parameters:**  

	ProjectId  
	ArticleId

	
**Note:**  ProjectId and ArticleId are required.
  
**Sample Request 1:** 

	GET https://caps-api-devint.azurewebsites.net/v1/Projects/5deff363-2bde-473e-8479-ea9ce1c4a6bc/Articles/a03e3a69-7751-4658-8490-1eb4853f1662/Histories?locale=en-US&pageSize=99999&pageToken= 
 

**Sample Response 1:** 

    {
    "items": [
    {
      "changes": [
        {
          "previous_value": "2.84",
          "name": "publish_source_version",
          "updated_value": "3.84"
        }
      ],
      "revision": 587,
      "updated_at": "2015-08-17T07:19:38Z",
      "updated_by": "4422b87327c34d3b84941e0fd91a5a2a"
    },
    {
      "changes": [
        {
          "previous_value": "2.74",
          "name": "source_version",
          "updated_value": "3.74"
        }
      ],
      "revision": 586,
      "updated_at": "2015-08-17T07:19:38Z",
      "updated_by": "4422b87327c34d3b84941e0fd91a5a2a"
    }
    …
    ]
    }



**Code Example:** 
```
   Coming soon 
```