---
title: PlayOnPhoneGreetingResponse（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhoneGreetingResponse
api_type:
- schema
ms.assetid: 7189d69a-9288-4fc8-8d78-4977ee1a7253
description: PlayOnPhoneGreetingResponse 元素定义对 UM Web 服务 (PlayOnPhoneGreeting 操作) 的响应。
ms.openlocfilehash: f8370d8ed93cc18eb29df100e68bddaa22c35fca
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512630"
---
# <a name="playonphonegreetingresponse-um-web-service"></a>PlayOnPhoneGreetingResponse（UM Web 服务）

**PlayOnPhoneGreetingResponse** 元素定义对 UM Web 服务 ([PlayOnPhoneGreeting](playonphonegreeting-operation-um-web-service.md)操作) 的响应。 
  
[PlayOnPhoneGreetingResponse（UM Web 服务）](playonphonegreetingresponse-um-web-service.md)
  
```xml
<PlayOnPhoneGreetingResponse />
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

文本值是必需的。 文本值包含在[GetCallInfo](getcallinfo-operation-um-web-service.md)操作[ (UM Web](callid-um-web-service.md)服务) ) 请求或 Disconnect 操作 (UM Web 服务) 请求中 CallId ([UM Web 服务) ](disconnect-operation-um-web-service.md)的值。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[PlayOnPhoneGreeting 操作（UM Web 服务）](playonphonegreeting-operation-um-web-service.md)
  
[CallId（UM Web 服务）](callid-um-web-service.md)
  
[GetCallInfo 操作（UM Web 服务）](getcallinfo-operation-um-web-service.md)
  
[Disconnect 操作（UM Web 服务）](disconnect-operation-um-web-service.md)

