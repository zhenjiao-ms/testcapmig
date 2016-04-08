---
title: SLA for Live Site Issue(LSI)
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.assetid: fec51fbe-6afb-4603-93b4-159f997e137f
robots: noindex,nofollow
---
# SLA for Live Site Issue(LSI)

###SLA for Live Site Issue(LSI)

The Service Level Agreement(SLA) for Live Site Issue(LSI) that occurs with CAPS is defined as below: 


Priority  |Description/Examples  |SLA  
---------|---------|---------
Pri 0*     |  -Service is completely down; <br/>-Block major events; <br/>-Content data loss of the entire project(not a single topic)       |    **Detection** time: 5 minutes, <br/>**Response** time: 1 hour, <br/>**Mitigation** time: 1 business day    
Pri 1    | -One main scenario does not work but it does not block big content event and it does not block entire team <br/>-Consistently face performance issues for all services, but functionally still work <br/>-One client always crash, but not others  <br/> -Data loss of any topic or article    |   **Detection** time: 1 hour; <br/>**Response** time: 1 business day; <br/>**Mitigation** time: 5 business days        
Pri 2        | -Face some intermittent performance issue <br/>-Other scenarios fail, but there is a workaround  <br/> -Any other intermittent issue   |  **Detection** time: 2 hours; <br/>**Response** time: 5 business days; <br/>**Mitigation** time: 15 business days(one sprint)          
        
###On Call Rotation
You can find the current on call person at [here](https://icm.ad.msft.net/imp/CurrentOnCall.aspx?teamId=0&tenantId=20342&incdep=0&incvirt=1&mode=chain)

*Note that the current TFS does not allow enter Priority 0 bug and please use P1 instead, and send out email to ADSOps to raise priority of the issue.