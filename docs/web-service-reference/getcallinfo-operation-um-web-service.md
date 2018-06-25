---
title: GetCallInfo 操作 （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfo
api_type:
- schema
ms.assetid: 6bccd418-caf7-4eb9-8a6f-410e56a635c3
description: GetCallInfo 操作返回由 CallId （UM web 服务） 指定的出站呼叫的状态。
ms.openlocfilehash: 36f9cba3690520ebb457a4cb2bfbcde3fea4b8dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754475"
---
# <a name="getcallinfo-operation-um-web-service"></a>GetCallInfo 操作 （UM web 服务）

GetCallInfo 操作返回由[CallId （UM web 服务）](callid-um-web-service.md)指定的出站呼叫的状态。
  
## <a name="getcallinfo-request-example"></a>GetCallInfo 请求示例

### <a name="description"></a>说明

GetCallInfo 请求的下面的示例演示如何以形成一个请求以获取有关指定的出站呼叫的信息。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a>成功 GetCallInfo 响应示例

### <a name="description"></a>说明

GetCallInfo 响应的下面的示例演示 GetCallInfo 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetCallInfoResponse>
        <CallState>Connected</CallState> 
        <EventCause>None</EventCause> 
      </GetCallInfoResponse>
    </GetCallInfoResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[GetCallInfo （UM web 服务）](getcallinfo-um-web-service.md)
  
[GetCallInfoResponse （UM web 服务）](getcallinforesponse-um-web-service.md)
  
[CallId （UM web 服务）](callid-um-web-service.md)
  
[CallState （UM web 服务）](callstate-um-web-service.md)
  
[EventCause （UM web 服务）](eventcause-um-web-service.md)

