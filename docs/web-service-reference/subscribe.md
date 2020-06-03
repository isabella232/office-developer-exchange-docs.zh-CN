---
title: 订阅
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subscribe
api_type:
- schema
ms.assetid: 6c2ee57d-e216-4a94-92db-faa3cb0e244a
description: 订阅元素包含用于创建订阅的属性。
ms.openlocfilehash: f60e67654fb6af76e8081036a3463f5be401862d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530956"
---
# <a name="subscribe"></a>订阅

**订阅**元素包含用于创建订阅的属性。 
  
```XML
<Subscribe>
   <PullSubscriptionRequest/>
   <PushSubscriptionRequest/>
   <StreamingSubscriptionRequest/>
</Subscribe>
```

 **SubscribeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |表示对基于请求的事件通知的订阅。  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |表示对基于推送的事件通知的订阅。  <br/> |
|[StreamingSubscriptionRequest](streamingsubscriptionrequest.md) <br/> |表示对流式事件通知的订阅。  <br/> |
   
### <a name="parent-elements"></a>父元素

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
  
[GetStreamingEvents 操作](getstreamingevents-operation.md)
  
[取消订阅操作](unsubscribe-operation.md)

