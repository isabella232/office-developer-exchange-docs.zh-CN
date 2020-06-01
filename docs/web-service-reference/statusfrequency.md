---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: StatusFrequency 元素表示服务器尝试重试的最大超时值（以分钟为单位）。
ms.openlocfilehash: db14ecfd54584188b3da16bb369db6c8089c70f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468241"
---
# <a name="statusfrequency"></a>StatusFrequency

**StatusFrequency**元素表示服务器尝试重试的最大超时值（以分钟为单位）。 
  
[订阅](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[StatusFrequency](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 **SubscriptionStatusFrequencyType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |表示对基于推送的事件通知订阅的订阅。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个表示整数的文本值。 此元素的可能值为1到1440（包含这两个值）。 此元素为可选。 默认值为 30 分钟。
  
## <a name="remarks"></a>备注

当服务器未收到对推送通知或来自客户端的状态 ping 的响应时，服务器使用**StatusFrequency**值重试推送通知。 如果服务器没有收到响应，则在停止发送通知之前，它会多次重试发送通知。 在 EWS 中，默认重试间隔为30秒，随后重试次数始终为上次重试间隔的时间的两倍。 重试次数并不完全取决于服务器上的其他负载是否会延迟。 下表显示了在由默认**StatusFrequency**值（假定服务器未遇到任何延迟）分配的30分钟内重试间隔的发生方式。 
  
|**重试**|**秒**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |初始同步  <br/> |
|1   <br/> |30  <br/> |00:30  <br/> |
|双面  <br/> |60  <br/> |01:00  <br/> |
|第三章  <br/> |120  <br/> |02:00  <br/> |
|4   <br/> |240  <br/> |04:00  <br/> |
|5   <br/> |480  <br/> |08:00  <br/> |
|6   <br/> |960  <br/> |16:00  <br/> |
|7   <br/> |1920  <br/> |32:00-超过**StatusFrequency**的默认值30，不发送重试  <br/> |
   
如果客户端在超过**StatusFrequency**指定时间的一段时间内未收到来自服务器的通知消息，客户端应执行重新创建订阅等操作。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[取消订阅操作](unsubscribe-operation.md)
  
[Watermark](watermark.md)

