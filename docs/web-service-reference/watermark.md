---
title: Watermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: 水印元素表示邮箱事件队列中的事件书签。
ms.openlocfilehash: a717196101fea698b0b8c66f92a3d420fda9a421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459761"
---
# <a name="watermark"></a>Watermark

**水印**元素表示邮箱事件队列中的事件书签。 
  
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
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |表示对基于请求的事件通知订阅的订阅。  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |表示对基于推送的事件通知订阅的订阅。  <br/> |
|[GetEvents](getevents.md) <br/> |表示由拉客户端用来从服务器请求通知的操作。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |代表复制项目或文件夹的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |代表在其中创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示一个事件，其中的项或文件夹被删除。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示一个事件，其中的项或文件夹被修改。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示将项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的新邮件项目触发的事件。  <br/> |
|[StatusEvent](statusevent.md) <br/> |表示未在邮箱中发生任何新活动的通知。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含订阅请求的状态和结果。  <br/> |
   
## <a name="text-value"></a>文本值

文本值可能是必需的，也可能是可选的，具体取决于此元素的使用方式。
  
## <a name="remarks"></a>备注

如果订阅请求包含水印，将从水印向前创建订阅。 如果订阅请求包含在邮箱事件表中找不到的水印， `ErrorInvalidWatermark` 则会向客户端应用程序返回一个错误。 如果水印太旧，并且已从事件表的30天窗口中删除，或者在事件表中不存在该水印，则可能会出现这种情况。 例如，如果水印是从其他数据库中的邮箱的不同订阅获取的，则可能会发生这种情况。 
  
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
  
[取消订阅操作](unsubscribe-operation.md)

