---
title: DaylightTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaylightTime
api_type:
- schema
ms.assetid: 9f551ee4-d945-477c-b981-9554b197d26d
description: DaylightTime 元素表示相对于协调世界时（UTC）的时间的偏移量，该时间由观察到夏时制的区域中的偏置（UTC）元素表示。 此元素还包含有关何时从标准时间转换到夏令时的信息。
ms.openlocfilehash: 350fcb4ce278f423c62fcc5ecaa160eda71e4a2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455651"
---
# <a name="daylighttime"></a>DaylightTime

**DaylightTime**元素表示相对于协调世界时（utc）的时间的偏移量，该时间由观察到夏时制的区域中的[偏置（utc）](bias-utc.md)元素表示。 此元素还包含有关何时从标准时间转换到夏令时的信息。 
  
- [时区（可用性）](timezone-availability.md) 
- [DaylightTime](daylighttime.md)
  
```xml
<DaylightTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</DaylightTime>
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
|[Year](year.md) <br/> |用于定义根据年份变化的时区。 此元素为可选。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[时区（可用性）](timezone-availability.md) <br/> | 包含标识时区信息的元素。<br/><br/>此元素还包含有关标准时间和夏时制之间转换的信息。<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="example"></a>示例

下面的部分 GetUserAvailability 请求代表一个可识别夏时制的位置的客户端应用程序。
  
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

