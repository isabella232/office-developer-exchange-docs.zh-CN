---
title: DayOfWeek （时区）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 416e8892-ebb1-4fac-82cf-e27549a6c175
description: DayOfWeek 元素表示发生时区转换的一周中的某一天。
ms.openlocfilehash: 7bc05f417268ccfb20adae12e2694d8360023ab2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457842"
---
# <a name="dayofweek-timezone"></a>DayOfWeek （时区）

**DayOfWeek**元素表示发生时区转换的一周中的某一天。 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

**DayOfWeekType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | 表示相对于[偏差（utc）](bias-utc.md)元素表示的协调世界时（utc）的时间的偏移量。<br/><br/>此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | 表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。<br/><br/>此元素还包含有关何时从标准时间转换到夏令时的信息。<br/><br/>下面是此元素的 XPath 表达式：<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 该文本值由具有以下可能值的枚举表示：
  
- 星期日    
- 星期一    
- 星期二    
- 星期三    
- 星期四    
- 星期五    
- 星期六    
- Day    
- 工作日   
- WeekendDay
    
## <a name="remarks"></a>备注

包含值为5的[DayOrder](dayorder.md)元素、值为10的[Month](month.md)元素以及值为周日的**DayOfWeek**元素的[StandardTime](standardtime.md)元素，表示从标准时间到夏时制的转换发生在第十个月的第五个星期日。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [获取用户可用性](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

