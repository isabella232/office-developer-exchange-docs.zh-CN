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
description: 通知元素包含有关订阅和自上次通知以来发生的事件的信息。
ms.openlocfilehash: a769d8988eb68d0fa0b02f3838cd891e714571b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826547"
---
# <a name="notification"></a>通知

**通知**元素包含有关订阅和自上次通知以来发生的事件的信息。 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

 **NotificationType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SubscriptionId (GetEvents)](subscriptionid-getevents.md) <br/> |表示订阅的标识符。  <br/> |
|[PreviousWatermark](previouswatermark.md) <br/> |表示对订阅的客户端的最新事件的成功传水印。  <br/> |
|[MoreEvents](moreevents.md) <br/> |指示队列传送到客户端中是否有多个事件。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示复制的项或文件夹的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |表示在其中创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示删除项或文件夹的事件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示在其中修改项目或文件夹的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的一个新的邮件项目触发的事件。  <br/> |
|[StatusEvent](statusevent.md) <br/> |表示没有新的活动发生的邮箱中的通知。  <br/> |
|[FreeBusyChangedEvent](freebusychangedevent.md) <br/> |表示项目的忙/闲时间已发生更改的事件。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |包含状态和单个 GetEvents 请求的结果。  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |包含状态和单个 SendNotification 请求的结果。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

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
  
[GetStreamingEvents 操作](getstreamingevents-operation.md)
  
[取消操作](unsubscribe-operation.md)

