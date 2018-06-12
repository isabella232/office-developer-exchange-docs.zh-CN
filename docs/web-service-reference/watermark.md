---
title: 水印
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
description: 水印元素均表示邮箱事件队列中的事件书签。
ms.openlocfilehash: 1867aa781bc24f5eb3bdb4648fa494a2a7ea396a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838535"
---
# <a name="watermark"></a>水印

**水印**元素均表示邮箱事件队列中的事件书签。 
  
```xml
<Watermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |代表对基于请求的事件通知订阅的订阅。  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |代表对基于推送的事件通知订阅的订阅。  <br/> |
|[GetEvents](getevents.md) <br/> |表示从服务器请求通知使用拉客户端的操作。  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |表示复制的项或文件夹位置的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |表示在其中创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示删除项或文件夹的事件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示修改项目或文件夹的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示其中的项目或文件夹从一个父文件夹移到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的一个新的邮件项目触发的事件。  <br/> |
|[StatusEvent](statusevent.md) <br/> |表示没有新的活动发生的邮箱中的通知。  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |包含状态和 Subscribe 请求的结果。  <br/> |
   
## <a name="text-value"></a>文本值

必需或可选根据如何使用此元素是可能的文本值。
  
## <a name="remarks"></a>备注

如果的 Subscribe 请求包含水印，从水印转接创建订阅。 如果订阅请求包含邮箱事件表格中找不到水印`ErrorInvalidWatermark`错误返回给客户端应用程序。 这可能会发生如果水印太旧，已从事件表的 30 天窗口或如果水印未以往演示事件表格中。 可以这样做，例如，如果从其他数据库中邮箱的不同订阅获得水印。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
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
  
[取消操作](unsubscribe-operation.md)

