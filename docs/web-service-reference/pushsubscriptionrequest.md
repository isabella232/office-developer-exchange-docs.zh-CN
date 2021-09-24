---
title: PushSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PushSubscriptionRequest
api_type:
- schema
ms.assetid: 70caa0ca-40a1-421f-b4e6-0658f22d0b8e
description: PushSubscriptionRequest 元素表示对基于推送的事件通知订阅的订阅。
ms.openlocfilehash: 6eb76bba92e78e048ae97dbec5fc6c4d698a815f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523725"
---
# <a name="pushsubscriptionrequest"></a>PushSubscriptionRequest

**PushSubscriptionRequest** 元素表示对基于推送的事件通知订阅的订阅。 
  
[Subscribe](subscribe.md)
  
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
|**SubscribeToAllFolders** <br/> |指示是否订阅所有可用文件夹。 此特性是可选的。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |包含一个文件夹标识符数组，用于标识要监视的事件通知的文件夹。  <br/> |
|[EventTypes](eventtypes.md) <br/> |包含用于创建订阅的事件通知的集合。  <br/> |
|[Watermark](watermark.md) <br/> |表示邮箱事件表中的事件书签。 这用于创建从水印表示的事件开始订阅。 如果未找到 Subscribe 请求中的水印，则客户端将返回错误响应。 如果水印超过 30 天，或者邮箱中从未存在水印，则可能发生此情况。  <br/> |
|[StatusFrequency](statusfrequency.md) <br/> |表示在未发生任何事件时向客户端发送通知消息的频率（以分钟指定）。  <br/> |
|[Url ](url-ex15websvcsotherref.md) <br/> |表示推送通知的客户端 Web 服务的位置。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Subscribe](subscribe.md) <br/> |包含用于创建订阅的属性。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

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
  
[Unsubscribe 操作](unsubscribe-operation.md)

