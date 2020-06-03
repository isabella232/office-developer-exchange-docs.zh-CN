---
title: End
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- End
api_type:
- schema
ms.assetid: 72329821-32ff-495d-b6e5-fdc011003c2e
description: End 元素表示持续时间的结束。
ms.openlocfilehash: d36f555d2ac9c0c1d82053029720ec17a53f2d92
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456141"
---
# <a name="end"></a>End

**End**元素表示持续时间的结束。 
  
```xml
<End/>
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
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |表示定期日历项目的第一个匹配项。  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |表示定期日历项目的最后一个事件。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[重复](occurrence.md) <br/> |代表定期日历项目的单个修改事件。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示工期的结束。
  
## <a name="remarks"></a>备注

UpdateItem 操作可以设置 Exchange 存储项的[开始](start.md)和**结束**时间。 在 UpdateItem 请求中，可以设置[开始](start.md)时间，而无需同时设置**结束**时间。 如果[开始](start.md)时间晚于**结束**时间，这可能会导致错误。 请注意，客户端应用程序必须在[开始](start.md)时间更改时对**结束**时间进行调整，以便保留持续时间。 
  
 **注释**如果定期主项目的[开始](start.md)和**结束**日期不具有与每周定期模式的第一个匹配项相等的日期，则将丢失时区偏移信息。 
  
描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[WeeklyRecurrence](weeklyrecurrence.md)
  
 **End**


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

