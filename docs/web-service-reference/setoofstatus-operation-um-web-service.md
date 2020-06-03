---
title: SetOofStatus 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: SetOofStatus 操作设置一个值，该值指示是否应为发出请求的用户播放外出（OOF）问候语。
ms.openlocfilehash: 2311b6137ac25d15ad3d06668450c1d0f7ec1fad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467352"
---
# <a name="setoofstatus-operation-um-web-service"></a>SetOofStatus 操作（UM web 服务）

SetOofStatus 操作设置一个值，该值指示是否应为发出请求的用户播放外出（OOF）问候语。
  
## <a name="setoofstatus-request-example"></a>SetOofStatus 请求示例

### <a name="description"></a>Description

以下示例的 SetOofStatus 请求显示了如何形成请求以启用邮箱的 "外出" 问候语。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a>成功的 SetOofStatus 响应示例

### <a name="description"></a>Description

下面的 SetOofStatus 响应示例显示对 SetOofStatus 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[SetOofStatus （UM web 服务）](setoofstatus-um-web-service.md)
  
[SetOofStatusResponse （UM web 服务）](setoofstatusresponse-um-web-service.md)
  
[Status （UM web 服务-SetOofStatus）](status-um-web-servicesetoofstatus.md)

