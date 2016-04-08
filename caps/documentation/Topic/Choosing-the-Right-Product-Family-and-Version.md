---
title: Choosing the Right Product Family and Version
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 640aab10-edc6-419b-891f-66e3d321976f
---
# Choosing the Right Product Family and Version
Product Family (PF) and Product Family Version (PFV) are publishing attributes in MTPS that help prevent content overwrites and support some multi-version content. The following guidelines summarize key considerations for choosing the correct PF/V.

## Key points about PF/V
Product Families are designed to prevent your content from getting overwritten by another group. MTPS looks for an AssetID (GUID, Namespace) or creates it for you if you don’t have one. Having PF ensures a unique ID for each asset, to address cases like System.String, which appears in content from 15 groups. The biggest risk is namespace, but there have been cases of GUIDs not being unique. PF is also intended to keep content associated with the team that built it. Once you publish content to MTPS with a particular PF, you can’t publish it to a new PF unless you do a PF migration -- this is a costly process, so it's important to choose carefully before you publish to MTPS. The first time an AssetID appears in a PF in MTPS DB, it trumps.

PFV is used for version control and to enable the version selector for product families that support versioning (for example, Visual Studio). Version 10 is the default. PFV can also be used for BI categorization. Publishing content to a new PFV does not require any migration, you simply change the version attribute.

## Guidelines for PF/V

-   If you don’t know which PF/V to choose, do not set or change it. Discuss with your team’s Portfolio Admin to determine the correct value.

-   New docsets most likely should have the same PF/V as other docsets in that portfolio.

-   Typically, you would only need to change PF in the following cases.

    -   Content was accidentally published to the wrong PF.

    -   A new org. owns the content and wants to publish to their own PF.

    -   The content should align with new product groupings (like MSDN.10 to CRM.6).

-   If a portfolio administrator decides we need to define a new PF, which should be very rare, file a ticket with PubDesk to get the value added to CAPS.

