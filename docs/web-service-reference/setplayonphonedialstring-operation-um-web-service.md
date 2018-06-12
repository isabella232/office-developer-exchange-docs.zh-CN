---
title: SetPlayOnPhoneDialString 操作 （UM web 服务）
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
description: SetPlayOnPhoneDialString 操作设置为默认值用于 PlayOnPhone 操作 （UM web 服务） 和 PlayOnPhoneGreeting 操作 （UM web 服务） 的拨号字符串。
ms.openlocfilehash: 0d1a879784740777e5eab0cbd5f85e59a6479461
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827446"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a>SetPlayOnPhoneDialString 操作 （UM web 服务）

SetPlayOnPhoneDialString 操作设置为默认值用于[PlayOnPhone 操作 （UM web 服务）](playonphone-operation-um-web-service.md)和[PlayOnPhoneGreeting 操作 （UM web 服务）](playonphonegreeting-operation-um-web-service.md)的拨号字符串。
  
## <a name="setplayonphonedialstring-request-example"></a>SetPlayOnPhoneDialString 请求示例

### <a name="description"></a>说明

SetPlayOnPhoneDialString 请求的下面的示例演示如何窗体设置邮箱的默认拨号串的请求。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a>成功 SetPlayOnPhoneDialString 响应示例

### <a name="description"></a>说明

SetPlayOnePhoneDialString 响应的下面的示例演示 SetPlayOnPhoneDialString 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[SetPlayOnPhoneDialString （UM web 服务）](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse （UM web 服务）](setplayonphonedialstringresponse-um-web-service.md)
  
[dialString （UM web 服务）](dialstring-um-web-service.md)

