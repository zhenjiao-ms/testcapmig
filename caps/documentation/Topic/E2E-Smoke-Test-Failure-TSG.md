---
title: E2E Smoke Test Failure TSG
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d9195759-a152-48ca-af9a-1b6c289fabf0
---
# E2E Smoke Test Failure TSG
Steps when receive E2E test failure:<br/>
Firstly, manually go through the [case work flow](E2E-Test-Case-Workflow.xml) in the web browser to see if it is a case issue or production issue.
- If the feature failed by manual testing. Please evaluate the priority and create bug according to its area:

Bug area  | Assign to
------------- | -------------
Build and Publish  | Jessie Huang
MRef | Xuan Zhou
Client  | Su Shi
Experience | Shuang
Not Clear | Su Shi

-	If the feature fails at a certain probability. Also create bug.
-	If can`t manually reproduce the failure. Create bug to E2E test owner (Shuang).
- If the bug is high priority and worth to call engineering team, find on call person on [IcM](https://icm.ad.msft.net/imp/CurrentOnCall.aspx?teamId=23958&tenantId=20342&incdep=0&incvirt=1&mode=oneshift), and call.







  
