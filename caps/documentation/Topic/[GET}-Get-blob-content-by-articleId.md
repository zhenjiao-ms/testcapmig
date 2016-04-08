---
title: [GET} Get blob content by articleId
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5f52b847-fed7-4798-88bf-79c1847e1829
---
# [GET} Get blob content by articleId
**Status:** Exists (dependency).
 
**Dependency area:** ad hoc tooling.
 
**Impact:** CSI.
 
**API type:** GET.
 
**Data to pass/receive:**
``` 
input	Api url: /v1/Projects/{projectid}/Articles/{articleid}:(blobcontent({SourceType}))
```

**e.g. :**
``` 
#url
https://caps-api-devint.azurewebsites.net/v1/Projects/05f57908-75ce-4769-bd3d-1528c9cba379/Articles/6bd12c13-d9c3-4522-94d3-4aa44513af57:(blobcontent(Source))
```


**output**	Blob content
 
**Tool(s):** CapsBulkUpdate

**Example**

```
```


