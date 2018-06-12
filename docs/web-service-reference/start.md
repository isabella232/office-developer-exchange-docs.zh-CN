---
title: 入门
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Start
api_type:
- schema
ms.assetid: 7cfe9979-c893-4f9b-b3a1-8f9e17515a4b
description: 开始元素表示持续时间的开始。
ms.openlocfilehash: 8d013990e650b497abfa947938a69eed3fed7474
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827545"
---
# <a name="start"></a>入门

**启动**元素均表示持续时间的开始。 
  
```xml
<Start/>
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
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[DeletedOccurrence](deletedoccurrence.md) <br/> |代表定期日历项目的已删除的匹配项。  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |代表定期日历项目的第一个匹配项。  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |代表定期日历项目的最后一个实例。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[匹配项](occurrence.md) <br/> |代表定期日历项目的一个已修改匹配项。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示持续时间的开始。
  
## <a name="remarks"></a>备注

UpdateItem 操作可以设置 Exchange 存储项目的[开始](start.md)和[结束](end-ex15websvcsotherref.md)时间。 在 UpdateItem 请求中，可以没有还设置的**结束**时间设置**开始**时间。 如果**开始**时间晚于的**结束**时间，这会导致错误。 注意客户端应用程序必须执行**结束**时间的**开始**时间才能保留持续时间的更改时调整。 
  
> [!NOTE]
> 如果没有等于每周定期模式的第一个匹配项的日期的定期主项目的[开始](start.md)和[结束](end-ex15websvcsotherref.md)日期，所在的时区偏移的信息将丢失。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [WeeklyRecurrence](weeklyrecurrence.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

