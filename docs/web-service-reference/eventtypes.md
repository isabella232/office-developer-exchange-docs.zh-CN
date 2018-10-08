---
title: EventTypes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventTypes
api_type:
- schema
ms.assetid: 29ded9e5-f191-4aa3-bc3e-500de2fc8818
description: EventTypes 元素包含用于创建订阅事件通知类型的集合。
ms.openlocfilehash: 7ea783dc0bf73abf992616b1f86c7621c5b36fc8
ms.sourcegitcommit: 25cbbc6707e4ec0621c5c46baf7fe49be42d3297
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/07/2018
ms.locfileid: "25440835"
---
# <a name="eventtypes"></a>EventTypes

**EventTypes**元素包含用于创建订阅事件通知类型的集合。 
  
```xml
<EventTypes>
   <EventType/>
</EventTypes>
```

 **NonEmptyArrayOfNotificationEventTypesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[EventType](eventtype.md) <br/> |表示用于创建订阅请求的事件通知类型。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |代表对基于请求的事件通知订阅的订阅。  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |代表对基于推送的事件通知订阅的订阅。  <br/> |
|[StreamingSubscriptionRequest](streamingsubscriptionrequest.md) <br/> |代表对流式处理的事件通知订阅的订阅。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[Subscribe 操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[GetStreamingEvents 操作](getstreamingevents-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)

