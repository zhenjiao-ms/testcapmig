---
title: [GET] Get publish state info
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0a2e880b-49e5-4e60-be82-b5dada133f64
---
# [GET] Get publish state info
**Description:** Get publish state info by bulidjobid

**API type:** GET

**URI:** v1/Projects/{Projectid}/BuildJobs/{bulidjobid}/properties?locale={locale}

**Parameters:**  

	ProjectId  
	bulidjobid
    locale

	
**Note:**  ProjectId and bulidjobid,locale are required.
  
**Sample Request 1:** 

	GET https://caps-api-devint.azurewebsites.net/v1/Projects/5deff363-2bde-473e-8479-ea9ce1c4a6bc/BuildJobs/da180f8a-6d2e-4c09-88e5-da8372be2936--promote/properties?locale=en-US 
 

**Sample Response 1:** 

    {
      "job_status": "Succeeded",
      "is_incremental": false,
      "is_on_demand": true,
      "is_scheduled": null,
      "message": "Succeeded in 00:00:08.3037704 seconds.",
      "triggered_by": "v-diluo@microsoft.com",
      "started_at": "2015-10-20T05:38:05.7249287+00:00",
      "ended_at": "2015-10-20T05:38:13.9064588+00:00",
      "cancelable": false,
      "total_count": 10,
      "successful_count": 10,
      "failed_count": 0,
      "job_progress": 1,
      "source_entities": [
    "{\"project_id\":\"5deff363-2bde-473e-8479-ea9ce1c4a6bc\",\"entity_id\":\"da180f8a-6d2e-4c09-88e5-da8372be2936\",\"entity_type\":\"Container\",\"locale\":\"en-US\"}"
     ],
      "latest_blob_id": "8587562874004887117",
      "categorized_count": "{\"Outline\":{\"total_count\":3,\"successful_count\":3,\"failed_count\":0},\"Article\":{\"total_count\":7,\"successful_count\":7,\"failed_count\":0}}",
      "job_type": "Live",
      "job_level": "DocSet",
      "staged_locales": null,
      "promoted_locales": null,
      "locales": [
    "en-US"
      ],
      "entity_id": "da180f8a-6d2e-4c09-88e5-da8372be2936--promote",
      "project_id": "5deff363-2bde-473e-8479-ea9ce1c4a6bc",
      "parent_id": "66216db2-b1c1-4036-8d0a-d624f0d932f3",
      "organization_id": "ffabd50649854ead8b30a42798aeb2ed",
      "name": null,
      "revision": 145,
      "locale": "en-US",
      "default_locale": "en-US",
      "entity_type": "BuildJob",
      "assigned_to": null,
      "created_at": "2015-08-28T02:03:03Z",
      "updated_by": "4422b87327c34d3b84941e0fd91a5a2a",
      "attributes": null,
      "readonly_fields": null,
      "e_tag": "W/\"datetime'2015-10-20T05%3A38%3A13.2311349Z'\"",
      "group_revisions": {
    "Localizable": 0
      }
    }



**Code Example:** 
```
     
```