---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: StatusEvent 元素表示邮箱中未发生新活动的通知。
ms.openlocfilehash: 777d5cd22e47fea6e7bf7432e58e5d58d1ef67a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543973"
---
# <a name="statusevent"></a>StatusEvent

**StatusEvent** 元素表示邮箱中未发生新活动的通知。 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 **BaseNotificationEventType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |表示订阅的最后一个有效水印。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来已发生事件的信息。  <br/> |
   
## <a name="remarks"></a>注解

**由于以下一个原因，StatusEvent** 元素在通知中返回： 
  
- 拉取客户端对没有活动的订阅发送 GetEvents 请求。
    
- 当达到 [StatusFrequency](statusfrequency.md) 时，推送客户端在队列中没有任何事件。 
    
**客户端应用程序使用 StatusEvent**[水](watermark.md)印的方式与其他事件类型水印相同。 但是 **，StatusEvent** 水印与其他事件所使用的水印不同。 例如，订阅具有具有水印 1、2 和 3 的事件，并且这些事件已在通知中成功传达。 将发生不活动期，并发送 **GetEvents** 请求。 CAS 客户端访问 (CAS) 返回状态事件，并包括最后一个水印 3，作为 Previous [Watermarkmark](previouswatermark.md) 和当前 [水印](watermark.md)。
  
水印不会在所有情况下都保持不变。 事件条目将保留 30 天。 若要维护活动订阅，CAS 会定期更新订阅队列水印。 更新后水印将发送给客户端以维护活动订阅。
  
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

