---
title: [GET] Get an entity type, metadata status, language with filter a specify metadata 4
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d8cf99e-d358-4268-9ec5-b5095b5a6053
---
# [GET] Get an entity type, metadata status, language with filter a specify metadata 4

**Description:** Get an entity info with filter a specify property key  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/{entityid}/properties/{propertykey}?locale={locale}](https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/{entityid}/properties/{propertykey}?locale={locale})  

**URL Parameters:**  

	Repositoryid: (project id in CAPS)  
	Entityid: (Article id/ Outline id/ source id in CAPS)  
	Property key: metadata in CAPS   
	Locale: en-US (default)  

**Note:** Repositoryid, Entityid, property key are required  

**Sample Request 1:** 

	Get https://caps-contentrepository-devint.cloudapp.net/v1/repositories/300d6d81-8c27-4d2b-8872-04a4c11e13f2/entities/b4398762-98d6-4a0c-acfc-bf70422bd8cb/properties/is_deleted?locale=en-us  

**Sample Response 1:** 

    [  
     {  
      "entity_id": "b4398762-98d6-4a0c-acfc-bf70422bd8cb",  
      "locale": "en-US",  
      "is_deleted": false,  
      "entity_type": "Container"  
     }  
    ]  