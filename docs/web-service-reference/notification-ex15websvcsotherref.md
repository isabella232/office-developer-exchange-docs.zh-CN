---
title: 通知
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Notification
api_type:
- schema
ms.assetid: c9070936-0930-438e-839c-91127256a6c8
description: Notification 元素包含有关订阅和自上次通知以来已发生事件的信息。
ms.openlocfilehash: affd44bb4c1f16029d6da92419908aeac3c26a44
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515409"
---
# <a name="notification"></a>通知

**Notification** 元素包含有关订阅和自上次通知以来已发生事件的信息。 
  
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
|[SubscriptionId (GetEvents)](subscriptionid-getevents.md) <br/> |表示订阅的标识符。  <br/> |
|[PreviousWatermark](previouswatermark.md) <br/> |表示已成功向客户端传递订阅的最新事件水印。  <br/> |
|[MoreEvents](moreevents.md) <br/> |指示队列中是否有更多要传递到客户端的事件。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示复制项目或文件夹的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |表示创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示一个删除项目或文件夹的事件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示项目或文件夹被修改的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示一个事件，其中项目或文件夹从一个父文件夹移动到另一个父文件夹。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的新邮件项目触发的事件。  <br/> |
|[StatusEvent](statusevent.md) <br/> |表示邮箱中未发生新活动的通知。  <br/> |
|[FreeBusyChangedEvent](freebusychangedevent.md) <br/> |表示项目的忙/闲时间已更改的事件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |包含单个 GetEvents 请求的状态和结果。  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |包含单个 SendNotification 请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

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
- [Unsubscribe 操作](unsubscribe-operation.md)

