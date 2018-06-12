---
title: IsUMEnabled 操作 （UM web 服务）
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
description: IsUMEnabled 操作确定是否将邮箱启用了统一消息。
ms.openlocfilehash: 9d94a359d6b11e41762d21aa2fe5501bd9f7b577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826107"
---
# <a name="isumenabled-operation-um-web-service"></a>IsUMEnabled 操作 （UM web 服务）

IsUMEnabled 操作确定是否将邮箱启用了统一消息。
  
## <a name="isumenabled-request-example"></a>IsUMEnabled 请求示例

### <a name="description"></a>说明

IsUMEnabled 请求的下面的示例演示如何表单以确定是否将邮箱启用统一消息的请求。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a>成功 IsUMEnabled 响应示例

### <a name="description"></a>说明

下面的示例演示对 IsUMEnabled 请求成功响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[IsUMEnabled （UM web 服务）](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse （UM web 服务）](isumenabledresponse-um-web-service.md)


[Exchange 的统一的消息 web 服务 XML 元素](unified-messaging-web-service-xml-elements-for-exchange.md)

