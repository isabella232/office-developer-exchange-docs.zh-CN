---
title: PlayOnPhone 操作（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: PlayOnPhone 操作发出出站呼叫，并通过 DialString 元素指定的电话播放指定的邮件。
ms.openlocfilehash: c5ff82bcd822aa2c659d1782ea4a1349d198bc80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466232"
---
# <a name="playonphone-operation-um-web-service"></a>PlayOnPhone 操作（UM web 服务）

PlayOnPhone 操作发出出站呼叫，并通过**DialString**元素指定的电话播放指定的邮件。 
  
## <a name="playonphone-request-example"></a>PlayOnPhone 请求示例

### <a name="description"></a>Description

以下示例的 PlayOnPhone 请求显示如何形成发出出站呼叫和播放邮件的请求。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhone xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <entryId>AAAAAGsd2rbQLVtLobUGbrq/9IUHAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAACxVpEl+KVVLl957wp//x6UAGAetcDUAAA==</entryId>
      <DialString>12345</DialString>
    </PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphone-response-example"></a>成功的 PlayOnPhone 响应示例

### <a name="description"></a>Description

下面的 PlayOnPhone 响应示例显示对 PlayOnPhone 请求的响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PlayOnPhoneResponse>NDEzYjEzNmMtZTE2Zi00NTJlLWI3YzctNDhkMTE3MDE3YjlmQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneResponse> 
    </PlayOnPhoneResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅



[PlayOnPhone （UM web 服务）](playonphone-um-web-service.md)
  
[PlayOnPhoneResponse （UM web 服务）](playonphoneresponse-um-web-service.md)
  
[PlayOnPhoneGreeting 操作（UM web 服务）](playonphonegreeting-operation-um-web-service.md)

