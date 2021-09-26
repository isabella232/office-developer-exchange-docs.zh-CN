---
title: PlayOnPhoneGreeting 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: PlayOnPhoneGreeting 操作进行出站呼叫，并通过电话播放两条问候语消息之一。
ms.openlocfilehash: 540cd44d35e70e2588446996aec19aeab17f83e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543133"
---
# <a name="playonphonegreeting-operation-um-web-service"></a>PlayOnPhoneGreeting 操作（UM Web 服务）

PlayOnPhoneGreeting 操作进行出站呼叫，并通过电话播放两条问候语消息之一。
  
## <a name="playonphonegreeting-request-example"></a>PlayOnPhoneGreeting 请求示例

### <a name="description"></a>说明

PlayOnPhoneGreeting 请求的以下示例显示如何形成发出出站呼叫的请求，以及如何在电话上播放常规问候语消息。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhoneGreeting xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GreetingType>NormalCustom</GreetingType>
      <DialString>12345</DialString>
    </PlayOnPhoneGreeting>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphonegreeting-response-example"></a>成功的 PlayOnPhoneGreeting 响应示例

### <a name="description"></a>说明

PlayOnPhoneGreeting 响应的以下示例显示对 PlayOnPhoneGreeting 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneGreetingResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <PlayOnPhoneGreetingResponse>MjA4MTQ5MmItMTBmZC00ZGFmLThiMzEtNDllNDJjM2Y3MjIxQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneGreetingResponse> 
    </PlayOnPhoneGreetingResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[PlayOnPhoneGreeting（UM Web 服务）](playonphonegreeting-um-web-service.md)
  
[PlayOnPhoneGreetingResponse（UM Web 服务）](playonphonegreetingresponse-um-web-service.md)
  
[GreetingType（UM Web 服务）](greetingtype-um-web-service.md)
  
[dialString（UM Web 服务）](dialstring-um-web-service.md)

