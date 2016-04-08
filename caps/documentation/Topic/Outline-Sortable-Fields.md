---
title: Outline Sortable Fields
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dff6b69d-9a36-42b4-a7cc-422726e8ea85
---
# Outline Sortable Fields
`<!-- # Outline Sortable Fields -->`

When working with outlines such as with the API

`GET` _baseUri_`/v1/Projects/`_projectId_`/Outlines?parentId=`_outlineContainerId_`&sortBy=`_sortField_`&sortOrder=`asc|desc`&skip=`_skipCount_`&take=`_takeCount_`&selection=`full|summary

Outlines can be sorted by the following fields. Note that the `display_order` field is _not_ available for sorting, so you must sort on the client side if you need this ordering.

_sortField_ Value    | Type
------------    | ----
`created_at`      | date
`created_by`      | string
`default_locale`  | string
`entity_id`       | string
`entity_type`     | string
`locale`          | string
`name`            | string
`name_lower_case` | string
`parent_id`       | string
`repository_id`   | string
`revision`        | long
`updated_at`      | date
`updated_by`      | string

> From email: "contact Jiahua Chen or Jason Zhu for adding fields which you have strong reason of to be sorted"