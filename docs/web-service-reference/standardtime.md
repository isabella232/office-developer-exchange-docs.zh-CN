---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: StandardTime 元素表示的时间相对于协调世界时 (UTC) 表示斜线 (UTC) 元素的偏移量。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。
ms.openlocfilehash: 726c31ffba06c1c437711b88444ec5eba45b520d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827546"
---
# <a name="standardtime"></a>StandardTime

**StandardTime**元素表示的时间相对于协调世界时 (UTC) 表示[斜线 (UTC)](bias-utc.md)元素的偏移量。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。 
  
- [TimeZone （可用性）](timezone-availability.md)
- [StandardTime](standardtime.md)
  
```xml
<StandardTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</StandardTime>
```

 **SerializableTimeZoneTime**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Bias](bias.md) <br/> |表示从由标准时间和夏时制的[斜线 (UTC)](bias-utc.md)元素的 UTC 偏移的偏移量。 此值以分钟为单位。  <br/> |
|[Time](time.md) <br/> |标准时间和夏时制表示转换时间。  <br/> |
|[DayOrder](dayorder.md) <br/> |表示一天[(TimeZone) DayOfWeek](dayofweek-timezone.md)元素，表示转换 from 和 to 标准时间和夏时制的日期中指定的 _n_th 匹配项。  <br/> |
|[month](month.md) <br/> |标准时间和夏时制表示转换月份。  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |代表星期几切换到以及从标准时间和夏时制当发生。  <br/> |
|[year()](year.md) <br/> |定义更改这取决于一年的时区。 此元素是可选的。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeZone （可用性）](timezone-availability.md) <br/> | 包含标识时区信息的元素。 此元素还包含有关标准时间和夏时制之间的转换的信息。 <br/><br/>下面是此元素的 XPath 表达式： <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a>备注

**StandardTime**元素表示一个偏移的时间表示的[斜线 (UTC)](bias-utc.md)元素。 子[Bias](bias.md)元素等于 0，标准时间时等于从由[斜线 (UTC)](bias-utc.md)元素的 UTC 的偏向偏移量。 
  
## <a name="example"></a>示例

下面的示例演示一个区域夏时制观察到的位置。 从夏时制转换为标准时间观察到凌晨 2 在第十个月的第五个星期日。
  
```xml
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>5</DayOrder>
    <Month>10</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>4</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
```

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

