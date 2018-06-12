---
title: PlayOnPhoneGreeting 操作 （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: PlayOnPhoneGreeting 操作创建出站呼叫，并在两个问候语消息之一电话上播放。
ms.openlocfilehash: 85ba76c7638911678c1ef1aef88f47fdab2c6a4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826828"
---
# <a name="playonphonegreeting-operation-um-web-service"></a>PlayOnPhoneGreeting 操作 （UM web 服务）

PlayOnPhoneGreeting 操作创建出站呼叫，并在两个问候语消息之一电话上播放。
  
## <a name="playonphonegreeting-request-example"></a>PlayOnPhoneGreeting 请求示例

### <a name="description"></a>说明

PlayOnPhoneGreeting 请求的下面的示例演示如何以形成发送出站呼叫和在电话上播放正常的问候语消息的请求。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhoneGreeting xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GreetingType>NormalCustom</GreetingType>
      <DialString>12345</DialString>
    </PlayOnPhoneGreeting>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphonegreeting-response-example"></a>成功 PlayOnPhoneGreeting 响应示例

### <a name="description"></a>说明

PlayOnPhoneGreeting 响应的下面的示例演示 PlayOnPhoneGreeting 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneGreetingResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <PlayOnPhoneGreetingResponse>MjA4MTQ5MmItMTBmZC00ZGFmLThiMzEtNDllNDJjM2Y3MjIxQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneGreetingResponse> 
    </PlayOnPhoneGreetingResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[PlayOnPhoneGreeting （UM web 服务）](playonphonegreeting-um-web-service.md)
  
[PlayOnPhoneGreetingResponse （UM web 服务）](playonphonegreetingresponse-um-web-service.md)
  
[GreetingType （UM web 服务）](greetingtype-um-web-service.md)
  
[dialString （UM web 服务）](dialstring-um-web-service.md)

