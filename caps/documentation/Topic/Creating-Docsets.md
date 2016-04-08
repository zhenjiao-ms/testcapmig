---
title: Creating Docsets
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5cdc77c2-4e2d-41e2-9bce-308ea3e15572
---
# Creating Docsets
The following guidelines summarize key considerations and steps for creating a new docset in CAPS.

## Creating a new docset
Use the following steps when you start a new docset.

#### Steps for new docsets

1.  Decide which portfolio is appropriate. See  [Creating Portfolios](../Topic/Creating-Portfolios.md).

2.  Decide whether to use an existing docset vs. create a new one:

    -   TOC hierarchy is managed at the docset level, so consider ease of TOC management. Creating too many docsets makes it more difficult to find content and manage TOC hierarchy.

    -   Consider the logical publishing group -- what content would you want to promote all together, and what TOC areas would you want to update and promote independently?

    -   Create a new docset if you want to publish content to a different product family or version than existing docsets.

    -   Create a new docset if you want to publish content to a different site than existing docsets. If you have content that needs to go to two different sites, you’d likely want to put that into a docset that’s shared into two parents.

    -   For mref, create a docset for each set of assemblies that get reflected together (in the same reflection folder).

    -   Consider size of the docset – if it’s too large, you will have extra steps to coordinate publishing with MSDN (&gt;50K changed topics, including metadata changes). Note that when multiple docsets publish together for the full top-level TOC, it could also constitute a large publish event that requires additional coordination.

3.  Name your docset.

    -   Discuss any naming conventions with your team’s portfolio admin.

    -   Don’t feel tied to old naming conventions from prior publishing systems. For example, you can use spaces in your names, so consider “Visual Studio Tools for Applications” instead of “dv_VSTA”

4.  Set metadata. See [Docset Metadata](../Topic/Docset-Metadata.md) and [Choosing the Right Product Family and Version](../Topic/Choosing-the-Right-Product-Family-and-Version.md).

5.  Add the docset to the TOC.

    -   Coordinate with your team’s portfolio admin to determine appropriate placement in the overall TOC hierarchy.

    -   If it is a top-level docset, you need to publish it to MTPS before you can hook up the TOC.

    -   File a ticket to PubDesk for TOC placement. See [New or Update TOC Node (Menu)](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-us/library/ecc96c9e-6016-438f-a176-47e915a43990).

6.  Inform localization about the new docset.

## Publishing docsets
Keep these dependencies in mind when you publish docsets:

-   Docsets that are child TOC nodes should publish before the parent TOC node to ensure the TOC is built correctly (from leaves to trunk).

-   When you publish a docset, all topics marked as Ready to Stage/Live will be published. If a topic isn’t marked Ready, it won’t be published or have a TOC entry.

-   You need to coordinate large or time-sensitive publishing events with MSDN. Contact [James Collins](mailto:jamcol) to get on the [MTPS Content Publishing Calendar](https://microsoft.sharepoint.com/teams/DD_VSCS/msdnpartner/Lists/test%20calendar/calendar.aspx).

For details on how to publish content in CAPS, see [Publishing a full docset to MTPS](../Topic/Publishing-a-full-docset-to-MTPS.md).

