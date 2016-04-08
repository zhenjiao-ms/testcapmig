---
title: [POST] Create an article with specify GUID
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 517cac34-ff41-4acd-b6bd-39dfae5cd593
---
# [POST] Create an article with specify GUID

Wednesday, August 12, 2015  
4:28 PM


**Description:** Create an article with specify GUID  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities](https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities)  

**URL Parameters:**  

    Repositoryid: (project id in CAPS)  
 	  
    Request body:  
    [  
      {  
       "entity_id": "IDToAdd",  
       "locale": "en-US",  
       "entity_type": "Article",  
       "parent_id": "parentIdToAdd",  
       "default_locale": "en-US",  
       "default_blob_type": "DDUE",  
       "properties": {  
         "name": "nameToAdd",  
         "ready_to_stage": false,  
         "ready_for_localizaion": true,  
         "ready_to_promote": false,  
         "status": "writing not started",  
         "is_deleted": false,  
         "is_mtps_no_follow": false,  
         "is_mtps_no_index": false,  
         "is_not_in_toc": false,  
         "is_pave_over": false,  
         "is_root": false  
       },  
       "blobs": [  
    	 {  
    	   "blob_id": "blobIdToAdd",  
    	   "blob_type": "Source",  
    	 "filename": "123.xml",  
    	 "filesize": 9000  
     	  }  
        ]  
      }  
    ]  
	  
**Note:** Make sure the GUID does not existing in the repository  

**Sample Request 1:** 

	POST https://caps-contentrepository-devint.cloudapp.net/v1/repositories/60202b11-04dc-4e03-a0b5-9bc2c39a8377/entities  
    	  
	Body:  
    [  
      {  
        "entity_id": "Example-60822377-DA7A-40B8-0089-D185D1509344",  
    	"locale": "en-US",  
    	"entity_type": "Article",  
    	"parent_id": "6b203de9-c4de-46ab-a4ff-b9c696e75bff",   
    	"default_locale": "en-US",  
    	"default_blob_type": "DDUE",  
    	"properties": {  
    	  "name": "ML Example",   
    	  "ready_to_stage": false,  
    	  "writer": "520f844609a04431b66642169a3954a7",  
    	  "ready_for_localizaion": true,  
    	  "ready_to_promote": false,  
    	  "status": "writing not started",  
    	  "assigned_to": "520f844609a04431b66642169a3954a7",  
          "is_deleted": false,  
    	  "is_mtps_no_follow": false,  
    	  "is_mtps_no_index": false,  
    	  "is_not_in_toc": false,  
    	  "is_pave_over": false,  
    	  "is_root": false  
    	},  
    	"blobs": [  
    	  {  
    	    "blob_id": "499d1afb-f6ff-48db-ae82-e674e34c11c5",   
    	    "blob_type": "Source"  
    	  }  
    	]  
      }  
   	]  
    	  
**Sample Response 1:** 

    [  
      {  
        "entity_id": "d921f79b-16f4-45ec-8c2f-d725e1d7d33a",  
        "locale": "en-US",  
        "is_success": "true"  
      }  
    ]  