---
title: GetCallInfoResponse（UM Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetCallInfoResponse
api_type:
- schema
ms.assetid: aa5196bf-f5f3-455c-94ea-304fb7920c79
description: GetCallInfoResponse 元素定义对 UM Web 服务请求 (GetCallInfo) 的响应。
ms.openlocfilehash: 4b631bdee87e57c1612e906c725adabb9f9ce63e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526187"
---
# <a name="getcallinforesponse-um-web-service"></a>GetCallInfoResponse（UM Web 服务）

**GetCallInfoResponse** 元素定义对 UM Web 服务请求 ([GetCallInfo)](getcallinfo-operation-um-web-service.md)的响应。 
  
[GetCallInfoResponse（UM Web 服务）](getcallinforesponse-um-web-service.md)
  
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
|CallState  <br/> |包含一个值，该值指示 UM Web 服务中 [GetCallInfo ](getcallinfo-operation-um-web-service.md) 操作 (请求) 呼叫的状态。  <br/> |
|EventCause  <br/> |包含一个值，该值指示调用事件的原因，该调用的 [GetCallInfo ](getcallinfo-operation-um-web-service.md) 操作 (UM Web) 所请求的信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="text-value"></a>文本值

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetCallInfo 操作（UM Web 服务）](getcallinfo-operation-um-web-service.md)
  
[CallState（UM Web 服务）](callstate-um-web-service.md)
  
[EventCause（UM Web 服务）](eventcause-um-web-service.md)

