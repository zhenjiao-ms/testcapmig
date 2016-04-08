---
title: Content Repository Structure
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bc1dc7ff-dddf-48b0-9218-f3c5c4765c8a
---
# Content Repository Structure

A basic hierarchy of Content Repository looks like:  

	• Tenant  
	• Tenant  
		○ Repository  
		○ Repository  
			§ Entity  
			§ Entity  
				□ …  
					® Entity  
					® Entity  
						◊ Blob  
						◊ Blob  
  
A **tenant** definition looks like:  

      {  
        "id": "00000000-0000-0000-0000-00000000000a",  
	    "tenant_id": "00000000-0000-0000-0000-00000000000a",  
    	"name": "Test2",  
    	"tenant_name": "Test2",  
    	"updated_by": "Sysadmin",  
    	"updated_at": "2014-07-02T17:33:11Z"  
      }  

A **repository** definition looks like:  

      {  
    	"id": "0024043f-85ed-4ffd-b910-002e15453ab1",  
    	"repository_id": "0024043f-85ed-4ffd-b910-002e15453ab1",  
    	"name": "Data_0024043f-85ed-4ffd-b910-002e15453ab1",  
    	"repository_name": "Data_0024043f-85ed-4ffd-b910-002e15453ab1",  
    	"type": "Data",  
    	"repository_type": "Data",  
    	"updated_by": "DALTestUserId",  
    	"updated_at": "2014-07-04T05:49:05.3158159Z",  
    	"tenant_id": "00000000-0000-0000-0000-00000000000a",  
    	"properties": {  
    	  "metadata5": "metadata1value2"  
    	},  
      }  