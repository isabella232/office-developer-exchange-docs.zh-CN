---
title: IsUMEnabled 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: IsUMEnabled 操作确定是否为邮箱启用了统一消息。
ms.openlocfilehash: 2c637711fc34a1d1ccc484b14be3199632aaaaa3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514457"
---
# <a name="isumenabled-operation-um-web-service"></a>IsUMEnabled 操作（UM Web 服务）

IsUMEnabled 操作确定是否为邮箱启用了统一消息。
  
## <a name="isumenabled-request-example"></a>IsUMEnabled 请求示例

### <a name="description"></a>Description

IsUMEnabled 请求的以下示例显示如何形成请求以确定邮箱是否已启用统一消息。
  
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

以下示例显示了对 IsUMEnabled 请求的成功响应。
  
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



[IsUMEnabled（UM Web 服务）](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse（UM Web 服务）](isumenabledresponse-um-web-service.md)


[统一消息 Web 服务 XML 元素Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

