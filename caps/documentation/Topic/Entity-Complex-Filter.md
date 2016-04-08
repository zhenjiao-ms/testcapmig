---
title: Entity Complex Filter
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3c4685a7-2c96-4e71-8542-1417e8791d96
---
# Entity Complex Filter
By using the Content Repository API, we have following serval methods to retrieve an entity / a list of entities:  

1. Get entities by entity ids:   
    `GET v1/repositories/{repositoryId}/entities/{entityIds}?locale={locale}`  

2. Get child entities by parent id:  
    `GET v1/repositories/{repositoryId}/entities/{entityId}/children?locale={locale}`  

	In many scenarios, we don't need the full information of the returned entities but just some aspects will be enough. In the previous release, we already provided some of the filter-like APIs which can be used to return partial entities (see attached email). In this preview, a full function unified filter syntax is added to support the complex filter scenarios.  

	>Notice:  
	>  
	>For entity filter getting operation, content repository will always return entity_id, locale and entity_type fields of entity.  
	For entity blob filter getting operation, content repository will always return blob_id and blob_type fields of blob.  

	The filter-enabled APIs are:  

3. Get entities by entity ids:   
    `GET v1/repositories/{repositoryId}/entities/{entityIds}:({filter})?locale={locale}`  
    	  
4. Get child entities by parent id:   
    `GET v1/repositories/{repositoryId}/entities/{entityIds}/children:({filter})?locale={locale}`  

5. Get child entities by repository id:  
	`GET v1/repositories/{repositoryId}/children:({filter})?locale={locale}`  

	A sample filter-enabled API call to retrieve entities by id (1 and 2) will be like:  
   
	`GET v1/repositories/repo_id/entities/1,2:(properties(p1,p2),blobs(blob_type[ddue,markdown],properties(blobp1,blobp2)))?locale=en-US`  
   
	Notice that the filter string is a flattened tree representation. If restored to a tree structure, it will be:  

	- Filter  
		- *revision*  
		- *updated_at*  
		- *updated_by*  
		- *created_at*  
		- *created_by*
		- *e_ta&#103;*
		- *tenant_id*  
		- *parent_id*  
		- *defualt_locale*  
		- **entity_type**  
		- *properties*  
			- *p1*  
			- *p2*  
		- *blobs*  
			- *revision*  
			- *properties_revision*  
			- *updated_at*  
			- *updated_by*  
			- *created_at*  
			- *created_by*  
			- *checkout_at*  
			- *checkout_by*  
			- *e_ta&#103;*  
			- *snapshot_time*  
			- **blob_id**  
			- **blob_type**  
			- *properties*  
				- *blobp1*  
				- *blobp2*  
	  
	So the above filter tree can be explained as: get entities with properties (key p1 and p2) and blobs (type equals to ddue or markdown, select properties blobp1 and blobp2).  
	   
	The () braces represent a column filter. E.g. properties(p1,p2). While the [] braces represent a row filter. E.g. blob_type[ddue, markdown]. Currently we are supporting following filters:  
	   
	- In the list above, the **bold** parts are row filter and the *italic* parts are column filter  
		- **entity_type**: column filter. If no entity type provided, all types of entity will be returned(get children)  
		- **properties**: column filter. Select the properties by property keys. If no keys provided, all properties will be returned.  
		- **blobs**: column filter. Select the blobs by sub filters. If no sub filters provided, all blobs will be returned.  
			- **blob_type**: row filter. Select the blobs by blob types.  
			- **blob_id**: row filter. Select the blobs by blob ids. Note: if the id filter is provided, the blob type filter must contains one and only one value, and the entity id must be one single value.  
		- **properties**: column filter. Select the blob’s properties by property keys. If no keys provided, all properties of the selected blobs will be returned.  
	  
	A few common samples:  

6. `:(tenant_id,parent_id,entity_type,default_locale,properties)`  
	select all properties and optional fields without any blobs  

7. `:(blobs)`  
	select all blobs without any entity properties or blob properties  

8. `:(blobs(properties))`  
	select all blobs (including blob properties) but without any entity properties   

9. `:(properties,blobs(properties))`  
	select all properties and blobs (the full entity)  

10. `:(properties(p1,p2),blobs(properties))`  
	select properties with key p1 and p2, and all full blobs  

11. `:(properties,blobs(blob_type[ddue,markdown],properties))`  
	select all properties, and full blobs typed ddue or markdown  

12. `:(properties,blobs(blob_type[ddue],blob_id[123,456],properties))`  
	select all properties, and full blobs typed ddue and id is 123 or 456  

13. `:(properties,blobs(blob_type[ddue,markdown],properties(bp1,bp2)))`  
	select all properties, and blobs typed ddue or markdown, with only bp1 and bp2 of the blob properties  

14. `:(properties,blobs(blob_type[ddue],blob_id[123,456],properties(bp1,bp2)))`  
	select all properties, and blobs typed ddue and id is 123 or 456, with only bp1 and bp2 of the blob properties  

15. `:(properties(p1,p2),blobs(blob_type[ddue],blob_id[123],properties(bp1,bp2)))`  
	select properties with key p1 and p2, and blobs typed ddue and id is 123, with only bp1 and bp2 of the blob properties