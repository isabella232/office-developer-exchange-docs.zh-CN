---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: DayOrder 元素表示 DayOfWeek (TimeZone) 元素中指定的第 n 天，该元素表示从标准时间和夏令时转换到的日期。
ms.openlocfilehash: bc216984a92fef58ac6f46dc4646a0deca837563
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543441"
---
# <a name="dayorder"></a>DayOrder

**DayOrder** 元素表示 _n_th [DayOfWeek (TimeZone)](dayofweek-timezone.md)元素中指定的日期，该元素表示从标准时间和夏令时转换的日期。 
  
```xml
<DayOrder>...</DayOrder>
```

**short**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | 表示相对于协调世界时与 UTC (UTC) 由偏置 ([UTC) ](bias-utc.md) 时偏移。<br/><br/>此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。<br/><br/>下面是 [StandardTime](standardtime.md) 元素的 XPath 表达式：<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | 表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。<br/><br/>此元素还包含有关何时从标准时间转换到夏令时的信息。<br/><br/>下面是 [DaylightTime](daylighttime.md) 元素的 XPath 表达式：<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 **DayOrder** 元素的值可以是 1 到 5。 此元素的最大值可以是 4 或 5，具体取决于月份和年份。 
  
## <a name="remarks"></a>注解

[StandardTime](standardtime.md)元素，包含值为 5 的 **DayOrder** 元素、值为 10 的 [Month](month.md)元素和值为 Sunday 的 [DayOfWeek (TimeZone)](dayofweek-timezone.md)元素，这意味着从标准时间到夏令时的转换发生在第十个月的第五个星期日。 
  
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

