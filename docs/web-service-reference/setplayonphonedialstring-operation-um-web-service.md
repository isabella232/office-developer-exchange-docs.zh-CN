---
title: SetPlayOnPhoneDialString 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: SetPlayOnPhoneDialString 操作将拨号串设置为用作 PlayOnPhone 操作 (UM Web 服务) 和 PlayOnPhoneGreeting 操作 (UM Web 服务) 的默认值。
ms.openlocfilehash: 89f83d7b0a1d56cb0adeccbf4fa0bb67f1197253
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531907"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a>SetPlayOnPhoneDialString 操作（UM Web 服务）

SetPlayOnPhoneDialString 操作将拨号串设置为用作 [PlayOnPhone ](playonphone-operation-um-web-service.md) 操作 (UM Web 服务) 和 [PlayOnPhoneGreeting ](playonphonegreeting-operation-um-web-service.md)操作 (UM Web 服务) 的默认值。
  
## <a name="setplayonphonedialstring-request-example"></a>SetPlayOnPhoneDialString 请求示例

### <a name="description"></a>说明

SetPlayOnPhoneDialString 请求的以下示例显示如何形成设置邮箱的默认拨号字符串的请求。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a>成功的 SetPlayOnPhoneDialString 响应示例

### <a name="description"></a>说明

SetPlayOnePhoneDialString 响应的以下示例显示对 SetPlayOnPhoneDialString 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[SetPlayOnPhoneDialString（UM Web 服务）](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse（UM Web 服务）](setplayonphonedialstringresponse-um-web-service.md)
  
[dialString（UM Web 服务）](dialstring-um-web-service.md)

