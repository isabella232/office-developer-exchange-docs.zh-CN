---
title: SetPlayOnPhoneDialString 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: SetPlayOnPhoneDialString 操作将拨号字符串设置为 PlayOnPhone 操作（UM web 服务）和 PlayOnPhoneGreeting 操作（UM web 服务）的默认值。
ms.openlocfilehash: 7df806eedc2d6d037394f31ec4ccbfe28aaf3372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458640"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a>SetPlayOnPhoneDialString 操作（UM web 服务）

SetPlayOnPhoneDialString 操作将拨号字符串设置为[PlayOnPhone 操作（um web 服务）](playonphone-operation-um-web-service.md)和[PLAYONPHONEGREETING 操作（um web 服务）](playonphonegreeting-operation-um-web-service.md)的默认值。
  
## <a name="setplayonphonedialstring-request-example"></a>SetPlayOnPhoneDialString 请求示例

### <a name="description"></a>说明

以下示例的 SetPlayOnPhoneDialString 请求显示如何形成请求以设置邮箱的默认拨号字符串。
  
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

下面的 SetPlayOnePhoneDialString 响应示例显示对 SetPlayOnPhoneDialString 请求的响应。
  
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



[SetPlayOnPhoneDialString （UM web 服务）](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse （UM web 服务）](setplayonphonedialstringresponse-um-web-service.md)
  
[dialString （UM web 服务）](dialstring-um-web-service.md)

