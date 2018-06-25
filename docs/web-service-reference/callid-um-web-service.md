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
description: CallId 元素包含表示 GetCallInfo （UM web 服务） 请求或断开连接 （UM web 服务） 请求中的呼叫的标识符的值。
ms.openlocfilehash: 49690f41b9a002b05c7c9b1a1240073c7230ab92
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753430"
---
# <a name="callid-um-web-service"></a>CallId （UM web 服务）

**CallId**元素包含表示[GetCallInfo （UM web 服务）](getcallinfo-um-web-service.md)请求或[断开连接 （UM web 服务）](disconnect-um-web-service.md)请求中的呼叫的标识符的值。 
  
[GetCallInfo （UM web 服务）](getcallinfo-um-web-service.md)
  
[CallId （UM web 服务）](callid-um-web-service.md)
  
[断开连接 （UM web 服务）](disconnect-um-web-service.md)
  
[CallId （UM web 服务）](callid-um-web-service.md)
  
```xml
<CallId/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetCallInfo （UM web 服务）](getcallinfo-um-web-service.md) <br/> |定义一个请求以获取有关调用的信息。  <br/> |
|[断开连接 （UM web 服务）](disconnect-um-web-service.md) <br/> |定义要断开呼叫的请求。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 文本值表示呼叫的标识符。
  
## <a name="remarks"></a>注解

若要初始呼叫，请使用[PlayOnPhone 操作 （UM web 服务）](playonphone-operation-um-web-service.md)或[PlayOnPhoneGreeting 操作 （UM web 服务）](playonphonegreeting-operation-um-web-service.md)。 使用**CallId**元素文本值的[PlayOnPhoneResponse （UM web 服务）](playonphoneresponse-um-web-service.md)或[PlayOnPhoneGreetingResponse （UM web 服务）](playonphonegreetingresponse-um-web-service.md)元素中返回的文本值。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)
  
[断开连接操作 （UM web 服务）](disconnect-operation-um-web-service.md)
  
[PlayOnPhone 操作 （UM web 服务）](playonphone-operation-um-web-service.md)
  
[PlayOnPhoneGreeting 操作 （UM web 服务）](playonphonegreeting-operation-um-web-service.md)

