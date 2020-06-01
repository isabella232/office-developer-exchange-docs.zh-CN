---
title: Month
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Month
api_type:
- schema
ms.assetid: b12ac64f-b230-4573-be05-c86a428c4965
description: Month 元素表示从标准时间和夏时制的年转换月数。
ms.openlocfilehash: f102dca4ed9e833b9742844cfd612c81dfd05e70
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468619"
---
# <a name="month"></a>Month

**Month**元素表示从标准时间和夏时制的年转换月数。 
  
```xml
<Month>...</Month>
```

 **简洁**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | 表示相对于[偏差（utc）](bias-utc.md)元素表示的协调世界时（utc）的时间的偏移量。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。 <br/> <br/>  下面是 [StandardTime](standardtime.md) 元素的 XPath 表达式： <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | 表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  <br/><br/>  下面是 [DaylightTime](daylighttime.md) 元素的 XPath 表达式：  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 值表示月份的序号排名，并且必须是介于1和12之间的数字。 这是一个短整型数据类型。
  
## <a name="remarks"></a>备注

一个[StandardTime](standardtime.md)元素，其中包含值为5的[DayOrder](dayorder.md)元素、值为10的**月份**元素以及值为周日的[DayOfWeek （时区）](dayofweek-timezone.md)元素。第十个月的第五个星期日发生从标准时间转换为夏时制。 
  
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

