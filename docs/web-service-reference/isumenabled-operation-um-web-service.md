---
title: IsUMEnabled 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: IsUMEnabled 操作确定是否为邮箱启用统一消息。
ms.openlocfilehash: b1478f5a113059251fe1b036ac7d77e5a4ab4f50
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458234"
---
# <a name="isumenabled-operation-um-web-service"></a>IsUMEnabled 操作（UM web 服务）

IsUMEnabled 操作确定是否为邮箱启用统一消息。
  
## <a name="isumenabled-request-example"></a>IsUMEnabled 请求示例

### <a name="description"></a>Description

以下示例的 IsUMEnabled 请求显示了如何形成一个请求，以确定是否为统一消息启用了邮箱。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a>成功的 IsUMEnabled 响应示例

### <a name="description"></a>Description

下面的示例演示对 IsUMEnabled 请求的成功响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[IsUMEnabled （UM web 服务）](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse （UM web 服务）](isumenabledresponse-um-web-service.md)


[Exchange 的统一消息 web 服务 XML 元素](unified-messaging-web-service-xml-elements-for-exchange.md)

