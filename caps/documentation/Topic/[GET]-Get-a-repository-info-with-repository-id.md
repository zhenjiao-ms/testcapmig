---
title: [GET] Get a repository info with repository id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 90037365-32b2-42c7-a0f0-ae09210ecd04
---
# [GET] Get a repository info with repository id

**Description:** Get a repository info with repository id  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/repositories/7f593941-7ce0-442f-873b-cf50ad1f5a2c](https://caps-contentrepository-devint.cloudapp.net/v1/repositories/7f593941-7ce0-442f-873b-cf50ad1f5a2c)  

**URL Parameters:** repositoryId (project id in CAPS)  

**Note:**   

**Sample Request 1:**  

	Get https://caps-contentrepository-devint.cloudapp.net/v1/repositories/7f593941-7ce0-442f-873b-cf50ad1f5a2c  

**Sample Response 1:**	  

    [  
     {  
      "repository_id": "7f593941-7ce0-442f-873b-cf50ad1f5a2c",  
      "repository_name": "484cfa8d-c06c-46ff-94ab-b309801fa6f0",  
      "repository_type": "Project",  
      "updated_by": "b8a16d4c-bf2f-4146-9b3a-197524a3a519",  
      "updated_at": "2015-06-10T05:47:04.9333993Z",  
      "created_at": "2015-06-10T05:47:04.9333993Z",  
      "created_by": "b8a16d4c-bf2f-4146-9b3a-197524a3a519",  
      "tenant_id": "ffabd50649854ead8b30a42798aeb2ed",  
      "partition_id": "97720d0ae867448db7db54c18b96706f",  
      "properties": {  
       "name": "CAPSTesting0610"  
      }  
     }  
    ] 