---
title: EventCause（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- EventCause
api_type:
- schema
ms.assetid: 7b3c1db8-cad4-4050-a50d-b06f065db530
description: EventCause 元素包含一个值，该值指示响应 UM Web 服务请求的 GetCallInfo 操作时 (事件) 原因。
ms.openlocfilehash: 203cefa1a70294bec4d6f4b41aa157da6e639fce
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546572"
---
# <a name="eventcause-um-web-service"></a>EventCause（UM Web 服务）

**EventCause** 元素包含一个值，该值指示响应 UM Web 服务请求的 [GetCallInfo](getcallinfo-operation-um-web-service.md)操作时 (调用) 原因。 
  
[GetCallInfoResponse（UM Web 服务）](getcallinforesponse-um-web-service.md)
  
[EventCause（UM Web 服务）](eventcause-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMEventCause**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetCallInfoResponse（UM Web 服务）](getcallinforesponse-um-web-service.md) <br/> |定义对 UM Web 服务请求 ([GetCallInfo) ](getcallinfo-operation-um-web-service.md) 的响应。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- 无
    
- UserBusy
    
- NoAnswer
    
- 其他
    
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作（UM Web 服务）](getcallinfo-operation-um-web-service.md)
  
[GetCallInfoResponse（UM Web 服务）](getcallinforesponse-um-web-service.md)

