---
title: Overview of Queries
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 10f87c2e-82de-446f-81b9-b470d415c191
---
# Overview of Queries

Queries are stored hierarchically in containers for a project (portfolio).

In the following examples, _baseUri_ is the base URI for the CAPS API endpoint you're working with. For DEVINT, this is always `https://caps-api-devint.azurewebsites.net`.

## Get the id for the project's root Query container

Enumerate the children of the project:

`GET` *baseUri*``/v1/projects/``*projectId*`:(children)`

From the returned children, get the `entity_id` for the container with `"class": "Query"`. This is the project's root query container.

## Walk the tree of queries and containers

The project's Query container is the root of a tree of containers. At each level, the children are a mix of containers (branch nodes) and queries (leaf nodes). The containers have `entity_type`=`Container`. The queries have `entity_type`=`Query`.

Get the children of the project's query container:

`GET` *baseUri*`/v1/projects/`*projectId*`/Containers/`*queryContainer*`:(children)`

The JSON result adds the `"children"` member to the root query container.

#### Example Response

```
[
  {
    "children": [
      {
        "entity_type": "Container",
        "name": "__??@RootPrivateQueryFolder@d9af4dfa-fb56-443a-8fc6-376363f83610@??__",
        "class": "Query",
        "entity_class": "Container",
        "has_children": true,
        "entity_id": "5167681c-5aa2-461c-81c7-0006dad14d7b",
        // ... more attributes
      },
      {
        "entity_type": "Query",
        "name": "All My Art",
        "entity_id": "59b9685a-0fa1-4af1-b7b7-1281eca512b3",
        "blob_id": "0afbe9ad-5e37-4475-b7b1-d7d9772cd315",
        "blob_revision": 1,
        // ... more attributes
      },
      {
        "entity_type": "Query",
        "name": "English contents promoted in the last 7 days",
        "entity_id": "5da5d4ed-7265-40d2-93fa-de19db911ee7",
        "blob_id": "316862b7-6286-4d29-81e7-e4c1b29c6afe",
        "blob_revision": 1,
        // ... more attributes
      }
      
      // ... more containers and queries
    ]
    // ...   
  }
]
```

[!NOTE] Your private queries are stored under the container with the fancy name: **`__??@RootPrivateQueryFolder@`**_userId_**`@??__`**

For each container (`entity_type` == `Container`), you can dig into it's children (and so on). Just pick up the container's id and use the same URI route:

`GET` _baseUri_`/v1/projects/`*projectId*`/Containers/`*queryContainer*`:(children)`

## Get the Query Definition

To get the actual definition of the query, you need the usual project id, plus the query entity id, the blob id, and the blob revision number.

The URI template to get the query definition is:

`GET` _baseUri_`/v1/projects/`*projectId*`/queries/`_queryId_`/Blobs/`_blobId_`/Contents?BlobType=Source&Revision=`_blobRevision_

The response is the definition of the query in JSON format.

> **Note** It seems to work fine without supplying the **Revision** parameter.

## Execute a Query

To execute a query, you do not use the CAPS API end point. Instead there is a "search" endpoint. For `devint` for example, there is the corresponding `caps-search-devint.azurewebsites.net` end point. This end point does not use the same authentication as the CAPS API end point. Instead you need the following header:
```
Authorization: YWRtaW5pc3RyYXRvcjojQnVnc2ZvciQ=
```
</br>
### To execute an article query:

`POST` `/`_orgId_`/Article/search?$top=`_count_`&$skip=`_position_

The post body is the query definition.

Parameter | Required | Default | Description
--- | --- | --- | --- |
_orgId_ | yes | - | Id of the organization (A.K.A. tenant)
_count_ | ? | 50? | Count of items to return. The `$top` parameter is equivalent to `take` in other CAPS APIs.
_position_ | no | 0 | Starting position in the results. 

## Update a Query

{{$TODO: Anyone know how to update an existing query? Presumably a PUT of the query def JSON. }}

## Create A Query

{{$TODO: Anyone know how to create a query? Beyond the mechanics of uploading, what's the query language? }}
