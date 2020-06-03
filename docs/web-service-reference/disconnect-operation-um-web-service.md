---
title: 断开连接操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: 断开连接操作将终止由指定的 CallId （UM web 服务）标识的呼叫。
ms.openlocfilehash: a1268f9ea3d879f472e019bf1847fc13d65d1819
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529068"
---
# <a name="disconnect-operation-um-web-service"></a>断开连接操作（UM web 服务）

断开连接操作将终止由指定的[CallId （UM web 服务）](callid-um-web-service.md)标识的呼叫。
  
## <a name="disconnect-request-example"></a>断开连接请求示例

### <a name="description"></a>Description

下面的一个断开请求示例演示如何形成一个请求以断开呼叫。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a>成功的断开连接响应示例

### <a name="description"></a>Description

以下示例中的 "断开连接" 响应显示对断开连接请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅

- [断开连接（UM web 服务）](disconnect-um-web-service.md) 
- [DisconnectResponse （UM web 服务）](disconnectresponse-um-web-service.md) 
- [CallId （UM web 服务）](callid-um-web-service.md)

