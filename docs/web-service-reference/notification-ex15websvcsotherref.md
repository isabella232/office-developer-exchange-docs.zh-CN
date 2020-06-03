---
title: 通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notification
api_type:
- schema
ms.assetid: c9070936-0930-438e-839c-91127256a6c8
description: Notification 元素包含有关订阅的信息以及自上次通知之后发生的事件。
ms.openlocfilehash: c4a5206c14985ec46cf40162a9ce4eaec68242ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530385"
---
# <a name="notification"></a>通知

**Notification**元素包含有关订阅的信息以及自上次通知之后发生的事件。 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CreatedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <DeletedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <ModifiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <MovedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <NewMailEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <StatusEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <FreeBusyChangedEvent/>
</Notification>
```

**NotificationType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SubscriptionId （GetEvents）](subscriptionid-getevents.md) <br/> |表示订阅的标识符。  <br/> |
|[PreviousWatermark](previouswatermark.md) <br/> |表示成功传递给订阅客户端的最新事件的水印。  <br/> |
|[MoreEvents](moreevents.md) <br/> |指示队列中是否存在要传递到客户端的更多事件。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示在其中复制项目或文件夹的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |代表在其中创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |代表在其中删除项目或文件夹的事件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示在其中修改项或文件夹的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |代表将项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |代表由邮箱中的新邮件项目触发的事件。  <br/> |
|[StatusEvent](statusevent.md) <br/> |表示未在邮箱中发生任何新活动的通知。  <br/> |
|[FreeBusyChangedEvent](freebusychangedevent.md) <br/> |表示项目的忙/闲时间已更改的事件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |包含单个 GetEvents 请求的状态和结果。  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |包含单个 SendNotification 请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [订阅操作](subscribe-operation.md) 
- [GetEvents 操作](getevents-operation.md) 
- [GetStreamingEvents 操作](getstreamingevents-operation.md) 
- [取消订阅操作](unsubscribe-operation.md)

