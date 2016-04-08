---
title: [POST] Create Handoff using live-revision via localization service API
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2dfb9b11-7b07-4d86-8762-00c4f33363dd
---
# [POST] Create Handoff using live-revision via localization service API
**Description:** Create a Handoff using live-revision via localization service API   

**API type:** POST

**URI:** v2/Projects/{ProjectID}/Handoffs

**Parameters:**  

	ProjectId
	  
	Request body:  
	 {  
    "name":"HandoffNameToAdd",
    "triggered_by":"aliasToAdd@microsoft.com",
    "parent_id":"HandoffContainerIdToAdd",
    "locales":[  
      "ja-JP",
      "zh-CN"
    ],
    "handoff_categories":[  
      "ArticleContent",
      "ArticleMetadata",
      "MediaContentContent",
      "MediaContentMetadata",
      "TokenContent"
    ],
    "aggregate_request":{  
       "container_id":null,
       "query_string":{ 
          "IsAnd":true,
          "ConditionGroups":null,
           "Conditions":[  
            {  
               "metadata":"locale",
               "operator":"EQ",
               "value":"en-US"
            },
            {  
               "metadata":"project_id",
               "operator":"EQ",
               "value":"ProjectIdToAdd"
            },            
            {  
               "metadata":"outline_id",
               "operator":"UNDER",
               "value":"OutlineIdToAdd"
            }
         ]
      },
      "query_type":"Article",
      "query_tenant":"TenantIdToAdd",
      "translation_type":"HumanTranslation",
      "force_handoff":true,
      "with_dependency":true,
      "handoff_revision_option":1
   }
}

 

**Note:**   

**Sample Request 1:** 

	POST https://caps-api-devint.azurewebsites.net/v2/Projects/60202b11-04dc-4e03-a0b5-9bc2c39a8377/Handoffs
	  
	Body:
	{
    "name": "Test",
    "triggered_by": "v-yingdh@microsoft.com",
    "parent_id": "d2c4075c-d5e4-45ae-a789-6171bc87e7a1",
    "locales": [
    "zh-CN"
    ],
    "handoff_categories": [
     "ArticleContent",
      "ArticleMetadata",
      "MediaContentContent",
      "MediaContentMetadata",
      "TokenContent"
    ],
    "aggregate_request": {
    "container_id": null,
    "query_string": {},
    "query_type": "Article",
    "query_tenant": "ffabd50649854ead8b30a42798aeb2ed",
    "translation_type": "MachineTranslation",
    "force_handoff": true,
    "with_dependency": true,
    "handoff_revision_option": 1
    },
    "intellisense_only": true
    }


**Sample Response 1:** 

    {
        "entity_id": "a03b1ac9-3033-4e90-8618-77cbdead1669",
        "name": "sample string 1",
        "triggered_by": "afb4736e-f853-49db-b42c-db391da18e9e","
        "project_id": "60202b11-04dc-4e03-a0b5-9bc2c39a8377",
        "parent_id": "d2c4075c-d5e4-45ae-a789-6171bc87e7a1",
        "locales": [
            "zh-CN"
            ],
            "handoff_categories": [
            "ArticleContent",
            "ArticleMetadata",
            "MediaContentContent",
            "MediaContentMetadata",
            "TokenContent"
            ]
    }



**Code Example:** 
```
coming soon
```