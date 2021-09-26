---
title: EventType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EventType
api_type:
- schema
ms.assetid: 04b70f9e-c226-4130-958e-0db0275cf58b
description: EventType 元素用于创建订阅并标识通知中要报告的事件类型。
ms.openlocfilehash: 7378ba45b155281df9e00ad635b7c6970a270f2c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545214"
---
# <a name="eventtype"></a>EventType

**EventType** 元素用于创建订阅并标识通知中要报告的事件类型。 
  
```xml
<EventType/>
```

 **NotificationEventTypeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[EventTypes](eventtypes.md) <br/> |包含用于创建订阅的事件通知事件类型的集合。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- CopiedEvent
    
- CreatedEvent
    
- DeletedEvent
    
- ModifiedEvent
    
- MovedEvent
    
- NewMailEvent
    
- FreeBusyChangedEvent
    
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
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

