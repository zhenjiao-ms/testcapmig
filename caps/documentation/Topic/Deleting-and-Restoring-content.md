---
title: Deleting and Restoring content
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d2f9a618-0f33-4cb8-ba97-8a12787b4d4c
---
# Deleting and Restoring content
The soft deletion is done by moving items to the **Trash** folder. Only these items can be sent to the **Trash** folder and restored.

* Topics
* Images
* Tokens

Not yet supported (if you need to delete any of them, please open a [Live Site Issue](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-US/library/468cf100-8e42-47b2-9373-f61ceeb5c2f9.aspx)):
* Docset
* Portfolio
* Handoff
* Hand back

[!Warning] **Only soft deletion is supported in CAPS right now. Removing items from the Trash folder is not supported.**

## Deleting an asset
[!NOTE] You should not delete a topic if it is published to MTPS. Before moving the topic  to Trash folder you should pave it over. See [Retiring content](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-us/library/8ff7e00d-fd2a-433f-a550-c3556d2c5c87.aspx).

1. Right-click on the asset
2. Click on **Delete**

[!Warning] **You cannot delete an asset if it has a dependency in another asset. For example, a token referenced in a topic. This is to avoid having broken references or missing content in the documentation.** 

 

## Restoring an asset
1. Got to the **Trash** folder
2. Right-click on the asset
3. Click on **Cut**
4. Right-click on the area where you want to put the asset back
5. Click on **Paste**
