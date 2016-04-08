---
title: Walking the Outline Tree
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f4fee8e0-511e-49f2-9bd7-42bf401d8f15
---
# Walking the Outline Tree
`<!-- # Walking the Outline Tree -->`

The TOC and non-TOC content of a portfolio (including "pave-over" content) is known in the API as an **outline**. Outlines are stored hierarchically, so the process of enumerating the tree of items is recursive. Each DocSet has an outline container with three children, one each for **Toc**, **NotInToc**, and **PaveOver**. The outline nodes are entities that may also have children, so they also function as containers.

This topic begins assuming that you know the id of the DocSet you want to enumerate. Enumerating the DocSets in a Portfolio is covered elsewhere.

## Get the child containers of the DocSet

`GET` _baseUri_`/v1/Projects/`_projectId_`/Containers/`_docSetId_`:(children)`

From the returned containers, select the one with `class` = `Outline`.

You can also fetch container children in continuation-style paged fashion using:

`GET` _baseUri_`/v1/Projects/`_projectId_`/Containers/`_docSetId_`/Children?locale=en-US&pageSize=`_itemCount_`&pageToken=`_token_

The _token_ value is null/empty on the first call. You then feed the token from the `next_page_token` value of the result to the next call, and so on until a null `next_page_token` is received with the last page of results.

From the returned containers, select the one with `class` = `Outline`.

##  Get the Toc, NotInToc, and PaveOver containers.

[!Note] The **PaveOver** container is named **Retired Contents** in the CAPS UI. 

Call the same API route to get the children of the Outline container:

`GET` _baseUri_`/v1/Projects/`_projectId_`/Containers/`_outlineContainerId_`:(children)`

This will return containers named `Toc`, `NotInToc`, and `PaverOver`. These are each the parent for the corresponding tree of outlines.

## Get Outlines

`GET` _baseUri_`/v1/Projects/`_projectId_`/Outlines?parentId=`_outlineId_`&sortBy=`_sortByField_`&skip=`_skipCount_`&take=`_takeCount_`&sortOrder=`_order_`&selection=`_detail_

Parameter | Required | Description
--- | --- | ---
_projectId_ | yes | Id of the project (Portfolio).
_outlineId_ | yes | Id of the outline.
_sortByField_ | no | Name of the field to sort by.  See [Outline Sortable Fields](Outline-Sortable-Fields.md) for the available names.
_skipCount_ | yes | Number of items to skip.
_takeCount_ | yes | Maximum nmber of items to return.
_order_ | no | The ordering of the results. One of (`asc`, `desc`).
_detail_ | no | Level of detail in the result. One of (`full`, `summary`). 


For outlines with `has_children` = `true`, you can recursively get the item's child outlines by passing the node's `entity_id` in the `parentId` parameter.