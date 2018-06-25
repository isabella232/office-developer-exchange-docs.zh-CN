---
title: 时间戳
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
description: 时间戳元素均表示邮箱事件的时间戳。
ms.openlocfilehash: d020d9a4cf3a128d26e0ff2b83be9f3deb024339
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838279"
---
# <a name="timestamp"></a>时间戳

**时间戳**元素均表示邮箱事件的时间戳。 
  
```xml
<TimeStamp/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |表示复制的项或文件夹位置的事件。  <br/> |
|[CreatedEvent](createdevent.md) <br/> |表示在其中创建项目或文件夹的事件。  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |表示删除项或文件夹的事件。  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |表示修改项目或文件夹的事件。  <br/> |
|[MovedEvent](movedevent.md) <br/> |表示其中的项目或文件夹从一个父文件夹移到另一个父文件夹的事件。  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |表示由邮箱中的一个新的邮件项目触发的事件。  <br/> |
   
## <a name="text-value"></a>文本值

此属性是只读的。
  
## <a name="remarks"></a>注解

此元素是主要可供使用的事件频率的客户端确定中。 这是不存在于[StatusEvent](statusevent.md)中。
  
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

