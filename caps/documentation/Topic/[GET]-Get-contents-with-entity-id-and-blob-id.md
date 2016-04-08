---
title: [GET] Get contents with entity id and blob id
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: bdd2dd1a-af90-4abd-b06b-589c141b1181
---
# [GET] Get contents with entity id and blob id

**Description:** Get contents with entity id and blob id  

**URL:** [https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/{entityid}/blobs/{blobtype}/{blobid}/content?locale={locale}](https://caps-contentrepository-devint.cloudapp.net/v1/repositories/{repositoryid}/entities/{entityid}/blobs/{blobtype}/{blobid}/content?locale={locale})  

**URL Parameters:**  

	RepositoryId: (project id in CAPS)  
	Entityid: (article id in CAPS)  
	Blobid:  
	Blobtype:  
	Locale:  

  
**Note:** RepositoryId, Entityid, Blobid, blobtype, locale are required  

  
**Sample Request 1:**  

	Get https://caps-contentrepository-devint.cloudapp.net/v1/repositories/60202b11-04dc-4e03-a0b5-9bc2c39a8377/entities/example-60822377-da7a-40b8-0089-d185d1509344/blobs/Source/499d1afb-f6ff-48db-ae82-e674e34c11c5/content?locale=en-US  

**Sample Response 1:** 

	…  
	Content  
	…  