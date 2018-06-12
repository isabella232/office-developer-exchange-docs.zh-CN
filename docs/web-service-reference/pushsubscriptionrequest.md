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
description: PushSubscriptionRequest 元素均表示对基于推送的事件通知订阅的订阅。
ms.openlocfilehash: 34717d37b8e5bb50c927e57088299fbcb18a2514
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826929"
---
# <a name="pushsubscriptionrequest"></a>PushSubscriptionRequest

**PushSubscriptionRequest**元素均表示对基于推送的事件通知订阅的订阅。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |指示是否订阅所有可用文件夹。 此属性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |包含用于标识要监视的事件通知文件夹的文件夹标识符的数组。  <br/> |
|[EventTypes](eventtypes.md) <br/> |包含用于创建订阅事件通知的集合。  <br/> |
|[水印](watermark.md) <br/> |代表邮箱事件表格中的事件书签。 这用于创建订阅开始由水印事件。 如果找不到订阅请求从水印，向客户端将返回错误响应。 如果水印已超过 30 天或水印从未存在的邮箱中，可能会出现此问题。  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |代表指定以分钟为单位，在的通知邮件将被发送到客户端时没有发生任何事件的频率。  <br/> |
|[Url](url-ex15websvcsotherref.md) <br/> |表示客户端推送通知的 Web 服务的位置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[订阅](subscribe.md) <br/> |包含用于创建订阅的属性。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[取消操作](unsubscribe-operation.md)

