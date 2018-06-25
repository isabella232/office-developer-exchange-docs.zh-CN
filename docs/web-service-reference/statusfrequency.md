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
description: StatusFrequency 元素表示最大超时值，以分钟为单位，由服务器尝试重试。
ms.openlocfilehash: 402f8978c0ec6b377dfa020f23595c8954509a07
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827589"
---
# <a name="statusfrequency"></a>StatusFrequency

**StatusFrequency**元素表示最大超时值，以分钟为单位，由服务器尝试重试。 
  
[订阅](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[StatusFrequency](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 **SubscriptionStatusFrequencyType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |代表对基于推送的事件通知订阅的订阅。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要表示一个整数的文本值。 此元素的可能值是 1 到 1440 之间，非独占。 此元素是可选的。 默认值为 30 分钟。
  
## <a name="remarks"></a>注解

服务器使用**StatusFrequency**值时不会收到来自客户端的推送通知或状态 ping 响应重试推送通知。 如果服务器未收到响应，它重试停止发送通知前几次发送通知。 Ews，默认重试时间间隔为 30 秒，并且后续重试次数总是 double 最后一个重试时间间隔的时间。 重试次数并不精确，与他们可以延迟由于服务器上的其他负载。 下表显示了如何分配的默认**StatusFrequency**值 （假定服务器不会遇到任何延迟） 在 30 分钟内发生的重试间隔。 
  
|**重试**|**秒**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |初始同步  <br/> |
|1  <br/> |30  <br/> |00:30  <br/> |
|2  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4  <br/> |240  <br/> |04:00  <br/> |
|5  <br/> |480  <br/> |08:00  <br/> |
|6  <br/> |960  <br/> |16:00  <br/> |
|7  <br/> |1920  <br/> |32:00- **StatusFrequency**默认值为 30 超过，未发送的重试  <br/> |
   
如果客户端未收到通知消息从服务器的一段时间超过两次**StatusFrequency**指定的时间，客户端应采取的操作，如重新创建订阅。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[取消操作](unsubscribe-operation.md)
  
[水印](watermark.md)

