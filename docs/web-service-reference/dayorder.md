---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: DayOrder 元素表示，表示转换 from 和 to 标准时间和夏时制的日期 (TimeZone) DayOfWeek 元素中指定的天的第 n 个匹配项。
ms.openlocfilehash: 03ee678611a6cf58a7256ded67ab4d0a8a06a7ee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753766"
---
# <a name="dayorder"></a>DayOrder

**DayOrder**元素表示，表示转换 from 和 to 标准时间和夏时制的日期[(TimeZone) DayOfWeek](dayofweek-timezone.md)元素中指定的天的 _n_th 匹配项。 
  
```xml
<DayOrder>...</DayOrder>
```

**短**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | 表示从时间相对于协调世界时 (UTC)[斜线 (UTC)](bias-utc.md)元素所表示的偏移量。<br/><br/>此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。<br/><br/>下面是 [StandardTime](standardtime.md) 元素的 XPath 表达式：<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | 表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。<br/><br/>此元素还包含有关何时从标准时间转换到夏令时的信息。<br/><br/>下面是 [DaylightTime](daylighttime.md) 元素的 XPath 表达式：<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 **DayOrder**元素的值可以是 1 到 5。 此元素的最大值可以是 4 或 5，具体取决于的月和年。 
  
## <a name="remarks"></a>注解

[StandardTime](standardtime.md)元素，其中包含的值为 5 **DayOrder**元素的值为 10， [Month](month.md)元素和的值为星期日[(TimeZone) DayOfWeek](dayofweek-timezone.md)元素是指从标准时间的转换第十个月的第五个星期日发生夏时制。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

