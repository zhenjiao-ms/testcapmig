---
title: [DELETE] Delete an entity from a repository
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1ff89622-a2be-43a1-b1a5-2c962a46420d
---
# [DELETE] Delete an entity from a repository
  
**Description:** Delete an entity from a repository  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/{entityid}](https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/{entityid})  

**URL Parameters:**  

	Repositoryid: (project id in CAPS)  
	Entityids: (Article id/ Outline id/ source id in CAPS)  
	  
**Note:** This GUID cannot be used ever in this repository.  

**Sample Request 1:** 

	Delete https://caps-contentrepository-devint.cloudapp.net/v1/repositories/300d6d81-8c27-4d2b-8872-04a4c11e13f2/entities/b4398762-98d6-4a0c-acfc-bf70422bd8cb  

**Sample Response 1:** 

    [  
     {  
      "entity_id": "b4398762-98d6-4a0c-acfc-bf70422bd8cb",  
      "locale": null,  
      "is_success": true  
     }  
    ] 