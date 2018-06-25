---
title: EventCause （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: EventCause 元素包含一个值，指示 GetCallInfo 操作 （UM web 服务） 请求的响应中的呼叫事件的原因。
ms.openlocfilehash: dd73d93527bebb3b522ad0a6cdae5b9faee1a6a9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754161"
---
# <a name="eventcause-um-web-service"></a>EventCause （UM web 服务）

**EventCause**元素包含一个值，指示[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)请求的响应中的呼叫事件的原因。 
  
[GetCallInfoResponse （UM web 服务）](getcallinforesponse-um-web-service.md)
  
[EventCause （UM web 服务）](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMEventCause**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetCallInfoResponse （UM web 服务）](getcallinforesponse-um-web-service.md) <br/> |定义[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)请求的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- 无
    
- UserBusy
    
- NoAnswer
    
- 其他
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作 （UM web 服务）](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse （UM web 服务）](getcallinforesponse-um-web-service.md)

