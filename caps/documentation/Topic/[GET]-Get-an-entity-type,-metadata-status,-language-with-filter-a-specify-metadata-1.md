---
title: [GET] Get an entity type, metadata status, language with filter a specify metadata 1
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 58616cb9-a966-4f95-9aa0-7bec3dadcae0
---
# [GET] Get an entity type, metadata status, language with filter a specify metadata 1

**Description:** Get an entity info with filter a specify metadata  

**URL:** [http://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryId}/entities/{entityIds}?filter={filter}&locale={locale}](http://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryId}/entities/{entityIds}?filter={filter}&locale={locale})   

**URL Parameters:**  

	Repositoryid: (project id in CAPS)  
	Entityid: (Article id/ Outline id/ source id in CAPS)  
	Filter: a metadata for this entity   
	Locale: en-US (default)  

**Note:** Repositoryid, Entityid, Filter are required  

**Sample Request 1:**  

	Get https://caps-contentrepository-devint.cloudapp.net/v1/repositories/7f593941-7ce0-442f-873b-cf50ad1f5a2c/entities/ed98b4c8-2df4-429a-8679-3b7719236e94?filter={filter}&locale=en-us  

**Sample Response 1:** 

    [  
     {  
      "entity_id": "ed98b4c8-2df4-429a-8679-3b7719236e94",  
      "locale": "en-US",  
      "is_deleted": false,  
      "entity_type": "Container"  
     }  
    ] 