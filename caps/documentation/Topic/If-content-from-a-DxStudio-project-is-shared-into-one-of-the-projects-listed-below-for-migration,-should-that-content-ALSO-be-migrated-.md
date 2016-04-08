---
title: If content from a DxStudio project is shared into one of the projects listed below for migration, should that content ALSO be migrated?
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4da4ee71-ef7b-4875-b5f1-3f85efd6579c
robots: noindex,nofollow
---
# If content from a DxStudio project is shared into one of the projects listed below for migration, should that content ALSO be migrated?
**Because that seems to be the problem here. We removed one of the Dx projects from the migration list because the content was shared into another project already on the list.**

The goal of identifying a content set for migration is to identify all the Dx projects that contribute to the content set.

This is why the migration report calls out links to topics in projects that are not part of the list of projects to be migrated.


The list of projects for a content set should include the publishing projects for that set of content as well as all source projects used to share topics into those pub projects.

Any projects that have topics shared into a content set should be included in the list of projects to migrate, or the shared instance of those topics should be removed prior to migration

This is done to ensure that when content is migrated to CAPS all referenced topics actually exist in the CAPS database so that the references can be properly mapped during migration.