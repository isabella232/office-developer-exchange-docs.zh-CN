---
title: CallId（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- CallId
api_type:
- schema
ms.assetid: 2e044109-8bf3-488c-a654-459ac62fa1e7
description: CallId 元素包含一个值，该值代表 GetCallInfo (UM Web 服务中的呼叫标识符) 请求或 Disconnect (UM Web) 请求。
ms.openlocfilehash: c19f1061d81bf7683fd2c84fb1c6968826046be6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522028"
---
# <a name="callid-um-web-service"></a>CallId（UM Web 服务）

**CallId** 元素包含一个值，该值代表 [GetCallInfo (UM Web](getcallinfo-um-web-service.md)服务中的呼叫标识符) 请求或 [Disconnect (UM Web)](disconnect-um-web-service.md)请求。 
  
[GetCallInfo（UM Web 服务）](getcallinfo-um-web-service.md)
  
[CallId（UM Web 服务）](callid-um-web-service.md)
  
[Disconnect（UM Web 服务）](disconnect-um-web-service.md)
  
[CallId（UM Web 服务）](callid-um-web-service.md)
  
```xml
<CallId/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetCallInfo（UM Web 服务）](getcallinfo-um-web-service.md) <br/> |定义一个请求，用于获取有关呼叫的信息。  <br/> |
|[Disconnect（UM Web 服务）](disconnect-um-web-service.md) <br/> |定义断开呼叫连接的请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值表示调用的标识符。
  
## <a name="remarks"></a>注解

若要初始化呼叫，请使用 UM Web 服务 ([PlayOnPhone ](playonphone-operation-um-web-service.md)) 或 [PlayOnPhoneGreeting ](playonphonegreeting-operation-um-web-service.md)操作 (UM Web) 。 使用 [PlayOnPhoneResponse (UM Web 服务)](playonphoneresponse-um-web-service.md) 或 [PlayOnPhoneGreetingResponse (UM Web 服务)](playonphonegreetingresponse-um-web-service.md) 元素中返回的文本值作为 **CallId** 元素文本值。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作（UM Web 服务）](getcallinfo-operation-um-web-service.md)
  
[Disconnect 操作（UM Web 服务）](disconnect-operation-um-web-service.md)
  
[PlayOnPhone 操作（UM Web 服务）](playonphone-operation-um-web-service.md)
  
[PlayOnPhoneGreeting 操作（UM Web 服务）](playonphonegreeting-operation-um-web-service.md)

