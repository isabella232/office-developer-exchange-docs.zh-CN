---
title: GetCallInfo 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetCallInfo
api_type:
- schema
ms.assetid: 6bccd418-caf7-4eb9-8a6f-410e56a635c3
description: GetCallInfo 操作返回由 CallId 指定的出站呼叫的状态 (UM Web) 。
ms.openlocfilehash: 0563190ab267b3a48d7ccacbdb1e136c6e3da0b4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509941"
---
# <a name="getcallinfo-operation-um-web-service"></a>GetCallInfo 操作（UM Web 服务）

GetCallInfo 操作返回由 CallId 指定的出站呼叫的状态[ (UM Web 服务) 。 ](callid-um-web-service.md)
  
## <a name="getcallinfo-request-example"></a>GetCallInfo 请求示例

### <a name="description"></a>Description

GetCallInfo 请求的以下示例显示如何形成请求，以获取有关指定出站呼叫的信息。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a>成功的 GetCallInfo 响应示例

### <a name="description"></a>Description

GetCallInfo 响应的以下示例显示对 GetCallInfo 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GetCallInfoResponse>
        <CallState>Connected</CallState> 
        <EventCause>None</EventCause> 
      </GetCallInfoResponse>
    </GetCallInfoResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[GetCallInfo（UM Web 服务）](getcallinfo-um-web-service.md)
  
[GetCallInfoResponse（UM Web 服务）](getcallinforesponse-um-web-service.md)
  
[CallId（UM Web 服务）](callid-um-web-service.md)
  
[CallState（UM Web 服务）](callstate-um-web-service.md)
  
[EventCause（UM Web 服务）](eventcause-um-web-service.md)

