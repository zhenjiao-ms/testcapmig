---
title: Permissions
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 92ddb7ed-73d2-4ea8-a706-3d4bed94c975
---
# Permissions
You can see your permissions by going to CAPS client and click on **Settings**. Permissions can be granted to an individual user, a Security Group, or to a Distribution Group. While CAPS accepts Security Groups without e-mail associated, we advice to use a SG with mail associated, so it is compatible with other systems, like TFS or Git Repos for code snippets.

Here are the standard permissions in CAPS. Organization administrators can create customized permission sets if needed for a given organization as needed. Note that a user can be assigned to more than one **Permission set**.

|Permission set|Scope|Rights|
|------------------|---------|----------|
|System administrator|Global|Manage users and organizations and grant permission on global level:<br /><br />-   Create, delete, and update users.<br />-   Create, delete, and update organizations.<br />-   Assign users to permission sets.|
|Organization administrator|Organization|Manage permission sets, delete portfolios, grant permissions and have full control on all projects under the organization:<br /><br />-   Create and delete portfolios.<br />-   Create, delete, and update permission sets.<br />-   Assign users to permission sets.<br />-   Create, edit, and delete topics, images and tokens.<br />-   Manage docsets.<br />-   Manage reflection.<br />-   Create docsets, and publish contents to staging and live.|
|Portfolio administrator|Portfolio|Grant permission and have full control at portfolio level:<br /><br />-   Assign users to permission sets.<br />-   Create, edit, and delete topics, images and tokens.<br />-   Create docsets, and publish contents to staging and live.<br />-   Manage docsets.<br />-   Manage reflection.<br />-   Create localization handoffs and hand backs.<br />-   Create offline builds.|
|Author|Portfolio|-   Create, edit, and delete topics, images and tokens.<br />-   Create offline builds.<br />-   Manage reflection.|
|Localization|Portfolio|-   Create localization handoffs and hand backs.<br />-   Create offline builds.|
|Publisher|Portfolio|-   Create docsets, and publish contents to staging and live.<br />-   Create offline builds.|
|Guest/Read-only|Portfolio|-   View content.<br />-   Create offline builds. **Tip:** We don’t have separated ‘read-only’ permission level on portfolio scope at this moment.Current solution, you can add any AAD Secure Group and Users into any test project of Sanbox, Devint or PROD, these users/group will be imported into CAPS as Read-Only guest. The users are shared across all organization and tenants so you don’t have to add users as read-only in each environment.|
