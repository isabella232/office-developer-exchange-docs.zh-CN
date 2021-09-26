---
title: StreamingSubscriptionRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StreamingSubscriptionRequest
api_type:
- schema
ms.assetid: d18f3b60-ebb6-4133-b895-a6ec8942d039
description: StreamingSubscriptionRequest 元素表示对流式事件通知订阅的订阅。
ms.openlocfilehash: 9789329f3f59cb543861dca0232207669f0711b8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544547"
---
# <a name="streamingsubscriptionrequest"></a>StreamingSubscriptionRequest

**StreamingSubscriptionRequest** 元素表示对流式事件通知订阅的订阅。 
  
[Subscribe](subscribe.md)
  
[StreamingSubscriptionRequest](streamingsubscriptionrequest.md)
  
```xml
<StreamingSubscriptionRequest SubscribeToAllFolders="">
   <FolderIds/>
   <EventTypes/>
</StreamingSubscriptionRequest>
```

 **StreamingSubscriptionRequest**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**SubscribeToAllFolders** <br/> |指示服务器是否将订阅用户邮箱中所有文件夹。 值为 **true** 表示服务器将订阅。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |包含一个文件夹标识符数组，用于标识要监视的事件通知的文件夹。  <br/> |
|[EventTypes](eventtypes.md) <br/> |包含用于创建订阅的事件通知的集合。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Subscribe](subscribe.md) <br/> |包含用于创建订阅的属性。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
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
  
[GetStreamingEvents 操作](getstreamingevents-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)

