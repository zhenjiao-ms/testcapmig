---
title: [GET] Get an entity type, metadata status, language with filter a specify metadata 2
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b858dcd-6c72-496c-938f-caf87f578ab8
---
# [GET] Get an entity type, metadata status, language with filter a specify metadata 2

**Description:** Get an entity info with filter a specify metadata  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/repositories/%7brepositoryid%7d/entities/%7bentityid%7d:(%7bfilter%7d)?locale=en-us](https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/{entityid}:{filter}?locale=en-us)  

**URL Parameters:**  

	Repositoryid: (project id in CAPS)  
	Entityid: (Article id/ Outline id/ source id in CAPS)  
	Filter: a metadata for this entity   
	Locale: en-US (default)  

**Note:** Repositoryid, Entityid, Filter are required  

**Sample Request 1:**  

    Get https://caps-contentrepository-devint.cloudapp.net/v1/repositories/300d6d81-8c27-4d2b-8872-04a4c11e13f2/entities/b4398762-98d6-4a0c-acfc-bf70422bd8cb:({filter})?locale=en-us  

  
**Sample Response 1:** 

    [  
     {  
      "entity_id": "b4398762-98d6-4a0c-acfc-bf70422bd8cb",  
      "locale": "en-US",  
      "is_deleted": false,  
      "entity_type": "Container"  
     }  
    ]  