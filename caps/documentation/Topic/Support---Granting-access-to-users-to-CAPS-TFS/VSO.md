---
title: Support - Granting access to users to CAPS TFS/VSO
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8212b3dc-bf05-4a74-b421-2c479d7718cd
---
# Support - Granting access to users to CAPS TFS/VSO
Right now, if users need access to TFS/VSO, they will follow the instructions in the following pages:

* [How to file a Live Site Issue (LSI) in TFS](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-us/library/468cf100-8e42-47b2-9373-f61ceeb5c2f9.aspx)
* [How to file a Bug in TFS](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-us/library/3e9fb2cb-3e43-4fe7-b328-4768101d03cc.aspx)
* [How to file a Feature Request in TFS](https://sandboxmsdnstage.redmond.corp.microsoft.com/en-us/library/7601a5e7-ac5f-41b2-a668-c685505a382c.aspx)

The support team will also answer any questions regarding permissions. Some common problems:
* Users try to access CAPS with their non-corporate account, for example, hotmail. Ask them to send a screenshot of the issue.
* Users try to open a bug, query, or other item before logging into [CAPS TFS landing page](https://capservice.visualstudio.com/DefaultCollection/CAPS/) for the first time.
* Users need to be be connected to corpnet to access CAPS TFS. 

##How to grant permissions

In order to grant permissions to people, users need to be an Admin in TFS:
1. Go to [CAPS work items](https://capservice.visualstudio.com/DefaultCollection/CAPS/_workitems).
2. Click on the Settings icon on the top-right corner: 
![CAPS Settings Icon](../Image/CAPS-Settings-Icon.png)
This takes you to the **Overview** tab.
3. Click on **Partners**.
4. Under **Members**, click on **Add - Add user**.
5. In **Identities**, type the UPN of the user.
	* Users must be added to VSO using their UPN. In the majority of the cases, users alias@microsoft.com is their UPN, but in some cases it is not, it is always safer to lookup for the user UPN. 
	* You can look up the UPN for a user by visiting [http://mysetup/](http://mysetup/) and typing the alias in the lower-left to perform a lookup (it can take a minute or two for this page to respond).
6. Notify the user. Add this info in the mail:
	* Make sure to access CAPS with your corporate account. If you have issues, send us a screenshot with the error.
	* Before opening a bug, query, or other item, log in with your corpnet account to the [CAPS TFS landing page](https://capservice.visualstudio.com/DefaultCollection/CAPS/).
	
##VSO FAQ
If the user is having trouble connecting, you can use the [VSO FAQ](https://1eswiki.com/index.php?title=VSO_FAQ) to find out what the problem is and the solution. 