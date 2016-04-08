---
title: [DELETE] Delete a specify repository with repository id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e33e948-499b-436f-8e23-21f54f47db8f
---
# [DELETE] Delete a specify repository with repository id

**Description:** Delete a repository with repository id  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/repositories/7f593941-7ce0-442f-873b-cf50ad1f5a2c](https://caps-contentrepository-devint.cloudapp.net/v1/repositories/7f593941-7ce0-442f-873b-cf50ad1f5a2c)  

**URL Parameters:** repositoryId (project id in CAPS)  

**Note:** Be care it will delete the portfolio in CAPS.   

**Sample Request 1:**  

	Delete https://caps-contentrepository-devint.cloudapp.net/v1/repositories/7f593941-7ce0-442f-873b-cf50ad1f5a2c  

**Sample Response 1:**	  

    [  
     {  
      "repository_id": "7f593941-7ce0-442f-873b-cf50ad1f5a2c",  
      "partition_id": null,  
      "is_success": true  
     }  
    ]  