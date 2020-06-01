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
description: StandardTime 元素表示相对于由偏差（UTC）元素表示的协调世界时（UTC）的时间的偏移量。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。
ms.openlocfilehash: 793f058840d4fd9216f03e660f5be0f7564906cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456400"
---
# <a name="standardtime"></a>StandardTime

**StandardTime**元素表示相对于由[偏差（utc）](bias-utc.md)元素表示的协调世界时（utc）的时间的偏移量。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。 
  
- [时区（可用性）](timezone-availability.md)
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

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[偏置](bias.md) <br/> |表示从 UTC 偏移量（由标准时间和夏令时的[偏置（UTC）](bias-utc.md)元素标识）的偏移量。 此值以分钟为单位。  <br/> |
|[Time](time.md) <br/> |表示从标准时间到夏令时和夏时制的过渡时间。  <br/> |
|[DayOrder](dayorder.md) <br/> |表示在 DayOfWeek （时区）元素中指定的、表示从到标准时间和夏时制转换的日期的[（时区）](dayofweek-timezone.md)元素中指定的日期的 _n_th 事件。  <br/> |
|[Month](month.md) <br/> |表示一年的转换月份和标准时间以及夏时制。  <br/> |
|[DayOfWeek （时区）](dayofweek-timezone.md) <br/> |表示从标准时间和夏时制转换到的一周中的某一天。  <br/> |
|[Year](year.md) <br/> |定义根据年份变化的时区。 此元素为可选。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[时区（可用性）](timezone-availability.md) <br/> | 包含标识时区信息的元素。 此元素还包含有关标准时间和夏时制之间转换的信息。 <br/><br/>下面是此元素的 XPath 表达式： <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a>备注

**StandardTime**元素表示由[偏置（UTC）](bias-utc.md)元素表示的偏移时间。 当子[偏移](bias.md)元素等于0时，标准时间等于由[偏置（UTC）](bias-utc.md)元素表示的 UTC 偏差偏移量。 
  
## <a name="example"></a>示例

下面的示例展示了夏时制时间遵循的区域。 从夏时制转换到标准时间的时间为凌晨2点。 第十个月的第五个星期日。
  
```xml
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [GetUserAvailability 操作](getuseravailability-operation.md)
- [获取用户可用性](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

