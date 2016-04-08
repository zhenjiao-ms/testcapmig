---
title: [GET] Get a tenant info with tenant id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a2b99e4-0799-4960-b756-4805b136a9fa
---
# [GET] Get a tenant info with tenant id

**Description:** Get a tenant info with tenant id  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/tenants/694eacb19e664adc83d36c50cb0c996d](https://caps-contentrepository-devint.cloudapp.net/v1/tenants/694eacb19e664adc83d36c50cb0c996d)  

**URL Parameters:** Tenant id  

**Sample Request 1:**   

	Get https://caps-contentrepository-devint.cloudapp.net/v1/tenants/694eacb19e664adc83d36c50cb0c996d  

**Sample Response 1:**

    [  
     {  
      "tenant_id": "694eacb19e664adc83d36c50cb0c996d",  
      "tenant_name": "devint",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:15:54.5425092Z",  
      "created_at": "2014-07-30T03:15:54.5425092Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     }  
    ]