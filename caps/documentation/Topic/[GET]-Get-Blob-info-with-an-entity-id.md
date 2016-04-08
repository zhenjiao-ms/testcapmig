---
title: [GET] Get Blob info with an entity id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64d92d11-4542-449b-9a9a-637a5dfc2f13
---
# [GET] Get Blob info with an entity id

Get blob info with an entity id  

## URL Route
```
https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/{entityid}/blobs/{blobtype}?locale={locale}
```
## URL Parameters

| URL Parameter | Required | Description |
| --- | --- |
| **{repositoryid}** | yes | Project id in CAPS |  
| **{entityid}**     | yes | Article id in CAPS |  
| **{blobtype}**     | yes | <code>Source</code> |  
| **{locale}**       | yes | <code>en-US</code> (default)  |


## Sample Request
**Note —** Request headers have been omitted.
```
GET https://caps-contentrepository-devint.cloudapp.net/v1/repositories/60202b11-04dc-4e03-a0b5-9bc2c39a8377/entities/96457381-18ff-48e5-a9b9-2d451fd6bf10/blobs/Source?locale=en-US  
```

## Sample Response 
```
[
    {
        "entity_id": "96457381-18ff-48e5-a9b9-2d451fd6bf10",
        "locale": "en-US",
        "is_deleted": false,
        "entity_type": "Article",
        "blobs": [
            {
                "blob_id": "fbcc0e78-212a-4d3b-a28c-eb14678d35d2",
                "blob_type": "Source",
                "revision": 1,
                "property_revision": 4,
                "updated_by": "afb4736e-f853-49db-b42c-db391da18e9e",
                "updated_at": "2015-07-29T09:56:16Z",
                "created_at": "2015-07-29T09:56:16Z",
                "created_by": "afb4736e-f853-49db-b42c-db391da18e9e",
                "properties": {
                    "filename": "123.xml",
                    "filesize": 900,
                    "word_count": 351
                },
                "e_tag": "W/\"datetime'2015-08-12T02%3A28%3A23.2677901Z'\"",
                "snapshot_time": "2015-07-29T09:56:17.4624194+00:00"
            }
        ]
    }
]
```