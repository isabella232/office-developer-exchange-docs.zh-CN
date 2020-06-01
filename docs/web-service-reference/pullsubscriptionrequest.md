---
title: PullSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PullSubscriptionRequest
api_type:
- schema
ms.assetid: 145c5cc7-a894-4f0b-a6ea-358cddfb5c33
description: PullSubscriptionRequest 元素表示对基于请求的事件通知订阅的订阅。
ms.openlocfilehash: fb9712c9e1481678c2821ee344052783d5c25bf9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468864"
---
# <a name="pullsubscriptionrequest"></a>PullSubscriptionRequest

**PullSubscriptionRequest**元素表示对基于请求的事件通知订阅的订阅。 
  
[订阅](subscribe.md)
  
[PullSubscriptionRequest](pullsubscriptionrequest.md)
  
```XML
<PullSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <Timeout/>
</PullSubscriptionRequest>
```

 **PullSubscriptionRequestType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |指示是否订阅所有可用的文件夹。 此特性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |包含用于标识要监视其事件通知的文件夹的文件夹标识符的数组。  <br/> |
|[EventTypes](eventtypes.md) <br/> |包含用于创建订阅的事件通知的集合。  <br/> |
|[Watermark](watermark.md) <br/> |表示邮箱事件表中的事件书签。 这用于创建在由水印表示的事件处启动的订阅。 如果找不到订阅请求中的水印，将向客户端返回错误响应。 如果水印的时间超过30天或者水印从未出现在邮箱中，则可能会出现此错误。  <br/> |
|[Timeout](timeout.md) <br/> |表示订阅可以保持空闲状态的持续时间（以分钟为单位），而无需客户端的 GetEvents 请求。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[订阅](subscribe.md) <br/> |包含用于创建订阅的属性。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[取消订阅操作](unsubscribe-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

