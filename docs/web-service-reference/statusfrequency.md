---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: StatusFrequency 元素表示服务器尝试重试的最大超时值（分钟）。
ms.openlocfilehash: f0359bab58167bbe7be5cce8c250240bebc7cc08
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525531"
---
# <a name="statusfrequency"></a>StatusFrequency

**StatusFrequency** 元素表示服务器尝试重试的最大超时值（分钟）。 
  
[Subscribe](subscribe.md)
  
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

如果使用此元素，则代表整数的文本值是必需的。 此元素的可能值为 1 到 1440（包括 1 和 1440）。 此元素为可选。 默认值为 30 分钟。
  
## <a name="remarks"></a>注解

当服务器未收到来自客户端的推送通知响应或状态 ping 时，它使用 **StatusFrequency** 值重试推送通知。 如果服务器未收到响应，它会在停止发送通知之前多次重试发送通知。 在 EWS 中，默认重试间隔为 30 秒，后续重试时间始终为上次重试间隔的两倍。 重试时间并不精确，因为它们可能会由于服务器上其他负载而延迟。 下表显示了在 30 分钟内重试间隔如何发生，该间隔由默认 **StatusFrequency** 值 (假定服务器未遇到任何延迟) 。 
  
|**重试**|**秒**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |初始同步  <br/> |
|1  <br/> |30  <br/> |00:30  <br/> |
|2  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4   <br/> |240  <br/> |04:00  <br/> |
|5  <br/> |480  <br/> |08:00  <br/> |
|6   <br/> |960  <br/> |16:00  <br/> |
|7   <br/> |1920  <br/> |32：00 - **StatusFrequency** 默认值超过 30，未发送重试  <br/> |
   
如果客户端在超过 **StatusFrequency** 指定的两倍的时间的一段时间内没有收到来自服务器的通知消息，则客户端应执行一些操作，如重新创建订阅。 
  
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
  
[Unsubscribe 操作](unsubscribe-operation.md)
  
[Watermark](watermark.md)

