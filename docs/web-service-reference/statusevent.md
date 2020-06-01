---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: StatusEvent 元素表示在邮箱中未发生任何新活动的通知。
ms.openlocfilehash: 8158a47937a810be2ea22346384b4e61da56ac48
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468255"
---
# <a name="statusevent"></a>StatusEvent

**StatusEvent**元素表示在邮箱中未发生任何新活动的通知。 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 **BaseNotificationEventType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |表示订阅的最后一个有效的水印。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅以及上次通知之后发生的事件的信息。  <br/> |
   
## <a name="remarks"></a>备注

由于以下原因之一，在通知中返回**StatusEvent**元素： 
  
- "拉" 客户端在没有活动的订阅上发出 GetEvents 请求。
    
- 当已到达[StatusFrequency](statusfrequency.md)时，推送客户端在队列中没有事件。 
    
客户端应用程序使用**StatusEvent**[水印](watermark.md)的方式与其他事件类型的水印的使用方式相同。 但是， **StatusEvent**的水印与用于其他事件的水印不同。 例如，订阅具有水印1、2和3的事件，并且这些事件已在通知中成功传递。 发生不活动的一段时间，并发送**GetEvents**请求。 客户端访问服务器（CAS）返回一个状态事件，并包括最后一个水印3，作为[PreviousWatermark](previouswatermark.md)和当前的[水印](watermark.md)。
  
在所有情况下，水印不会保持相同。 事件条目的维护时间为30天。 为了维护活动订阅，CAS 会定期更新订阅队列的水印。 更新的水印将发送到客户端，以维护活动订阅。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
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

