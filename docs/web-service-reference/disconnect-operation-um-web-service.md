---
title: Disconnect 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: Disconnect 操作将终止由 UM Web 服务应用程序指定的 CallId (标识的) 。
ms.openlocfilehash: 42e069233fbfc255d43983571c0bb28475a1fe90
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522010"
---
# <a name="disconnect-operation-um-web-service"></a>Disconnect 操作（UM Web 服务）

Disconnect 操作终止由 UM Web 服务指定的[CallId (标识的) 。 ](callid-um-web-service.md)
  
## <a name="disconnect-request-example"></a>断开连接请求示例

### <a name="description"></a>Description

以下示例的 Disconnect 请求显示如何形成断开呼叫连接的请求。
  
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

## <a name="successful-disconnect-response-example"></a>成功断开连接响应示例

### <a name="description"></a>Description

以下示例的 Disconnect 响应显示对 Disconnect 请求的响应。
  
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

- [Disconnect（UM Web 服务）](disconnect-um-web-service.md) 
- [DisconnectResponse（UM Web 服务）](disconnectresponse-um-web-service.md) 
- [CallId（UM Web 服务）](callid-um-web-service.md)

