---
title: [GET] Get all tenants infos
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 10f26966-1af4-459e-80a3-66756ae6c5db
---
# [GET] Get all tenants infos

**Description:**	Get all tenants infos  

**URL:**	[https://caps-contentrepository-devint.cloudapp.net/v1/tenants](https://caps-contentrepository-devint.cloudapp.net/v1/tenants)  

**URL Parameters:**	  

**Note:**	  

**Sample Request 1:**   
	  
	Get https://caps-contentrepository-devint.cloudapp.net/v1/tenants  

**Sample Response 1:**	  

    Cache-Control: no-cache  
    Pragma: no-cache  
    Content-Type: application/json; charset=utf-8  
    Expires: -1  
      
    [  
     {  
      "tenant_id": "0222d67c4146405497a70df65629e634",  
      "tenant_name": "e2e",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:34:57.2057641Z",  
      "created_at": "2014-07-30T03:34:57.2057641Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "1cd93a3c705f4e3d88b775fe38dc89dd",  
      "tenant_name": "migration1",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:27:07.9518434Z",  
      "created_at": "2014-07-30T03:27:07.9518434Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "2f20a035107e4c9ca37de05ea53b2802",  
      "tenant_name": "buildtest1",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:24:10.2940794Z",  
      "created_at": "2014-07-30T03:24:10.2940794Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "4e11ea77397a4d6493837e922c65556c",  
      "tenant_name": "buildtest2",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:24:10.2940794Z",  
      "created_at": "2014-07-30T03:24:10.2940794Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "55d6ece90f4b4e72aa9c9a2756ced67d",  
      "tenant_name": "clienttest",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:25:31.2341726Z",  
      "created_at": "2014-07-30T03:25:31.2341726Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "694eacb19e664adc83d36c50cb0c996d",  
      "tenant_name": "devint",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:15:54.5425092Z",  
      "created_at": "2014-07-30T03:15:54.5425092Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "8273eb6470fd4c7e901cedc6c53c753e",  
      "tenant_name": "migrationtest",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:27:07.9518434Z",  
      "created_at": "2014-07-30T03:27:07.9518434Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "950e523a33b54538824f57577374d39e",  
      "tenant_name": "dogfooding",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:34:57.2057641Z",  
      "created_at": "2014-07-30T03:34:57.2057641Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "a638963358e04feeb869fa59f632b904",  
      "tenant_name": "migration2",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:27:07.9518434Z",  
      "created_at": "2014-07-30T03:27:07.9518434Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "acf702779c45471fbcfe3604c3b396e7",  
      "tenant_name": "gendox",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2015-01-07T03:32:16Z",  
      "created_at": "2015-01-07T03:32:16Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "b9d8f95ae46340acbf1d43ecc85bc2c5",  
      "tenant_name": "reserved",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:15:54.5425092Z",  
      "created_at": "2014-07-30T03:15:54.5425092Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "bf502e13efbd4411b4fd879717f3c1ec",  
      "tenant_name": "perf",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:30:22.4432906Z",  
      "created_at": "2014-07-30T03:30:22.4432906Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "d0e83f810aef4eb9b47b0c7c901f3d45",  
      "tenant_name": "servicetest",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:32:16.0656517Z",  
      "created_at": "2014-07-30T03:32:16.0656517Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "dd7ca230dd164857b95795371b11af7a",  
      "tenant_name": "searchtest1",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:31:21.7842241Z",  
      "created_at": "2014-07-30T03:31:21.7842241Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "fc6dd7113991494d99e1e16a79023102",  
      "tenant_name": "searchtest2",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:31:21.7842241Z",  
      "created_at": "2014-07-30T03:31:21.7842241Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     },  
     {  
      "tenant_id": "ffabd50649854ead8b30a42798aeb2ed",  
      "tenant_name": "partner",  
      "updated_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058",  
      "updated_at": "2014-07-30T03:34:01.9482389Z",  
      "created_at": "2014-07-30T03:34:01.9482389Z",  
      "created_by": "a4d6e5ec-134d-4c5e-9932-e5efdd73c058"  
     }  
    ]  