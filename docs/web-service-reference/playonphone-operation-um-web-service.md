---
title: PlayOnPhone 操作（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: PlayOnPhone 操作发出出站呼叫，并通过电话播放由 DialString 元素指定的指定消息。
ms.openlocfilehash: 4d18727da18c36e6410c3cc6ab3bbf873993be72
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516562"
---
# <a name="playonphone-operation-um-web-service"></a>PlayOnPhone 操作（UM Web 服务）

PlayOnPhone 操作发出出站呼叫，并通过电话播放由 **DialString** 元素指定的指定消息。 
  
## <a name="playonphone-request-example"></a>PlayOnPhone 请求示例

### <a name="description"></a>Description

PlayOnPhone 请求的以下示例显示如何形成发出出站呼叫和播放消息的请求。
  
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

以下 PlayOnPhone 响应示例显示对 PlayOnPhone 请求的响应。
  
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



[PlayOnPhone（UM Web 服务）](playonphone-um-web-service.md)
  
[PlayOnPhoneResponse（UM Web 服务）](playonphoneresponse-um-web-service.md)
  
[PlayOnPhoneGreeting 操作（UM Web 服务）](playonphonegreeting-operation-um-web-service.md)

