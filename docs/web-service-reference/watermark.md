---
title: Watermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: Watermark 元素表示邮箱事件队列中的事件书签。
ms.openlocfilehash: 959ae7369195a164d257b8805a8c985f1fdca53b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524397"
---
# <a name="watermark"></a>Watermark

**Watermark** 元素表示邮箱事件队列中的事件书签。 
  
```xml
<Watermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |表示对基于拉取的事件通知订阅的订阅。  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |表示对基于推送的事件通知订阅的订阅。  <br/> |
|[GetEvents](getevents.md) <br/> |表示拉取客户端用于从服务器请求通知的操作。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示复制项目或文件夹的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |表示创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示删除项目或文件夹的事件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示项目或文件夹被修改的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的新邮件项目触发的事件。  <br/> |
|[StatusEvent](statusevent.md) <br/> |表示邮箱中未发生新活动的通知。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含 Subscribe 请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

文本值可能是必需的或可选，具体取决于此元素的使用方式。
  
## <a name="remarks"></a>注解

如果 Subscribe 请求包含水印，则从水印向前创建订阅。 如果 Subscribe 请求包含未在邮箱事件表中找到水印，则向客户端应用程序  `ErrorInvalidWatermark` 返回错误。 如果水印太旧并且已从事件表的 30 天窗口中删除，或者事件表中曾经没有水印，则可能发生此情况。 例如，如果从不同数据库中邮箱的不同订阅获取水印，可能会发生这种情况。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[订阅操作](subscribe-operation.md)
  
[GetEvents 操作](getevents-operation.md)
  
[Unsubscribe 操作](unsubscribe-operation.md)

