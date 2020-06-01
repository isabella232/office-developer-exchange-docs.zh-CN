---
title: GetCallInfoResponse （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: GetCallInfoResponse 元素定义对 GetCallInfo 操作（UM web 服务）请求的响应。
ms.openlocfilehash: 6e54ec61a9a5ebecd96bbd39dad68f8cc011b8a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461203"
---
# <a name="getcallinforesponse-um-web-service"></a>GetCallInfoResponse （UM web 服务）

**GetCallInfoResponse**元素定义对[GETCALLINFO 操作（UM web 服务）](getcallinfo-operation-um-web-service.md)请求的响应。 
  
[GetCallInfoResponse （UM web 服务）](getcallinforesponse-um-web-service.md)
  
```xml
<GetCallInfoResponse>
  <CallState/>
  <EventCause/>
</GetCallInfoResponse>
```

 **UMCallInfo**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|CallState  <br/> |包含一个值，该值指示[GetCallInfo 操作（UM web 服务）](getcallinfo-operation-um-web-service.md)请求的信息的调用的状态。  <br/> |
|EventCause  <br/> |包含一个值，该值指示对[GetCallInfo 操作（UM web 服务）](getcallinfo-operation-um-web-service.md)请求的信息进行的事件的原因。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作（UM web 服务）](getcallinfo-operation-um-web-service.md)
  
[CallState （UM web 服务）](callstate-um-web-service.md)
  
[EventCause （UM web 服务）](eventcause-um-web-service.md)

