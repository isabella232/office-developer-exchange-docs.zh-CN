---
title: PushSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: PushSubscriptionRequest 元素表示对基于推送的事件通知订阅的订阅。
ms.openlocfilehash: dcdb767ed175468aa4ec940f3147c164e4707e40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465511"
---
# <a name="pushsubscriptionrequest"></a>PushSubscriptionRequest

**PushSubscriptionRequest**元素表示对基于推送的事件通知订阅的订阅。 
  
[订阅](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
```XML
<PushSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
   <Watermark/>
   <StatusFrequency/>
   <URL/>
</PushSubscriptionRequest>
```

 **PushSubscriptionRequestType**
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
|[Watermark](watermark.md) <br/> |表示邮箱事件表中的事件书签。 这用于创建从水印所代表的事件开始的订阅。 如果找不到订阅请求中的水印，将向客户端返回错误响应。 如果水印的时间超过30天或者水印从未出现在邮箱中，则可能会出现这种情况。  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |表示在没有事件发生时，通知邮件将发送到客户端的频率（以分钟为单位）。  <br/> |
|[Url](url-ex15websvcsotherref.md) <br/> |表示用于推送通知的客户端 Web 服务的位置。  <br/> |
   
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



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[取消订阅操作](unsubscribe-operation.md)

