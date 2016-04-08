---
title: EndPoint: https://caps-contentrepository-devint.cloudapp.net
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 74741107-7699-4d52-8667-09d90891f640
---
# EndPoint: https://caps-contentrepository-devint.cloudapp.net
#EndPoint: https://caps-contentrepository-devint.cloudapp.net 
Wednesday, August 12, 2015    
9:09 AM   

Each web request on this end point requires the following headers:
```
Authorization: [_user authorization spec _]  
X-CAPS-AccessKey: [_access key_]  
X-CAPS-PageSize: 0
Content-Type: application/json;charset=utf-8
TokenType: jwt  
Accept: json
```

>Note: The **TokenType** header's value is variable. For some CAPS APIs this is **sas**.
