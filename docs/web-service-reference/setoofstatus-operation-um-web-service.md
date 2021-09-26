---
title: SetOofStatus 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: SetOofStatus 操作设置一个值，该值指示是否应该为提出请求的用户Office (Out of) OOF 问候语。
ms.openlocfilehash: ce736e7d7bea39f65843923187af3ae616ae1c86
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544750"
---
# <a name="setoofstatus-operation-um-web-service"></a>SetOofStatus 操作（UM Web 服务）

SetOofStatus 操作设置一个值，该值指示是否应该为提出请求的用户Office (Out of) OOF 问候语。
  
## <a name="setoofstatus-request-example"></a>SetOofStatus 请求示例

### <a name="description"></a>说明

SetOofStatus 请求的以下示例显示如何形成请求以启用邮箱的外出Office问候语。
  
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

### <a name="description"></a>说明

SetOofStatus 响应的以下示例显示对 SetOofStatus 请求的响应。
  
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



[SetOofStatus（UM Web 服务）](setoofstatus-um-web-service.md)
  
[SetOofStatusResponse（UM Web 服务）](setoofstatusresponse-um-web-service.md)
  
[Status（UM Web 服务 - SetOofStatus）](status-um-web-servicesetoofstatus.md)

