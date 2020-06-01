---
title: TimeStamp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeStamp
api_type:
- schema
ms.assetid: 5eae859a-5a74-4bf6-b196-d1b2fd38501a
description: Timestamp 元素表示邮箱事件的时间戳。
ms.openlocfilehash: f2280d4eab67b603963c4f0a7468bf35a2b63a88
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459887"
---
# <a name="timestamp"></a>TimeStamp

**Timestamp**元素表示邮箱事件的时间戳。 
  
```xml
<TimeStamp/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |代表复制项目或文件夹的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |代表在其中创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示一个事件，其中的项或文件夹被删除。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示一个事件，其中的项或文件夹被修改。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示将项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的新邮件项目触发的事件。  <br/> |
   
## <a name="text-value"></a>文本值

此属性是只读的。
  
## <a name="remarks"></a>备注

此元素主要可用于确定事件频率的客户端。 [StatusEvent](statusevent.md)中不存在这种情况。
  
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

