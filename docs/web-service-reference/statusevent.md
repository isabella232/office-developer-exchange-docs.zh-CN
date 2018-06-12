---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: StatusEvent 元素均表示没有新的活动发生的邮箱中的通知。
ms.openlocfilehash: e214918f9795e9e29061d4aac72ab144d2b24267
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827592"
---
# <a name="statusevent"></a>StatusEvent

**StatusEvent**元素均表示没有新的活动发生的邮箱中的通知。 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 **BaseNotificationEventType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[水印](watermark.md) <br/> |表示订阅的最后一个有效水印。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[通知](notification-ex15websvcsotherref.md) <br/> |包含有关订阅和自上次通知以来发生的事件的信息。  <br/> |
   
## <a name="remarks"></a>备注

**StatusEvent**元素返回在通知中的以下原因之一： 
  
- 提取客户端发出 GetEvents 请求上订阅处于不活动状态。
    
- 已达到[StatusFrequency](statusfrequency.md)时，推送客户端在队列中具有没有事件。 
    
客户端应用程序中其他事件类型水印相同的方式使用**StatusEvent**[水印](watermark.md)。 但是， **StatusEvent**的水印不是用于其他事件水印相同。 例如，订阅已事件水印 1，2，3 和这些事件已成功指出在通知中。 停止活动一段时间，发生此事件，并发送一个**GetEvents**请求。 客户端访问服务器 (CAS) 返回状态事件，并包括最后一个水印，3，为[PreviousWatermark](previouswatermark.md)和当前[水印](watermark.md)。
  
水印将保持不变在所有情况下。 30 天维护事件项。 若要维护的活动订阅，CAS 定期更新订阅队列的水印。 更新的水印发送到客户端，以维护的活动订阅。
  
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

