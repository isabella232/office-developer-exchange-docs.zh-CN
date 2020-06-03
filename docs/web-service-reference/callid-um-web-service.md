---
title: CallId （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- CallId
api_type:
- schema
ms.assetid: 2e044109-8bf3-488c-a654-459ac62fa1e7
description: CallId 元素包含一个值，该值表示 GetCallInfo （UM web 服务）请求或断开连接（UM web 服务）请求中的调用的标识符。
ms.openlocfilehash: 5d5f596d4a98cbfb4b53be04278dae2305fc10c3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529453"
---
# <a name="callid-um-web-service"></a>CallId （UM web 服务）

**CallId**元素包含一个值，该值表示[GetCallInfo （um web 服务）](getcallinfo-um-web-service.md)请求或[断开连接（um web 服务）](disconnect-um-web-service.md)请求中的调用的标识符。 
  
[GetCallInfo （UM web 服务）](getcallinfo-um-web-service.md)
  
[CallId （UM web 服务）](callid-um-web-service.md)
  
[断开连接（UM web 服务）](disconnect-um-web-service.md)
  
[CallId （UM web 服务）](callid-um-web-service.md)
  
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
|[GetCallInfo （UM web 服务）](getcallinfo-um-web-service.md) <br/> |定义获取有关调用的信息的请求。  <br/> |
|[断开连接（UM web 服务）](disconnect-um-web-service.md) <br/> |定义断开呼叫连接的请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值表示调用的标识符。
  
## <a name="remarks"></a>备注

若要初始呼叫，请使用[PlayOnPhone 操作（um web 服务）](playonphone-operation-um-web-service.md)或[PLAYONPHONEGREETING 操作（um web 服务）](playonphonegreeting-operation-um-web-service.md)。 使用**CallId**元素文本值的[PlayOnPhoneResponse （um web 服务）](playonphoneresponse-um-web-service.md)或[PlayOnPhoneGreetingResponse （um web 服务）](playonphonegreetingresponse-um-web-service.md)元素中返回的文本值。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作（UM web 服务）](getcallinfo-operation-um-web-service.md)
  
[断开连接操作（UM web 服务）](disconnect-operation-um-web-service.md)
  
[PlayOnPhone 操作（UM web 服务）](playonphone-operation-um-web-service.md)
  
[PlayOnPhoneGreeting 操作（UM web 服务）](playonphonegreeting-operation-um-web-service.md)

