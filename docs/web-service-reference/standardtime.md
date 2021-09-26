---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: StandardTime 元素表示相对于协调世界时 (UTC) （由 Bias (UTC) 元素表示）的时间偏移。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。
ms.openlocfilehash: ceddc511bf1883078c88dee240fc308d02024220
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544659"
---
# <a name="standardtime"></a>StandardTime

**StandardTime** 元素表示相对于协调世界时 (UTC) 的时间的偏移量，该时间由 Bias (UTC [)](bias-utc.md)元素表示。 此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。 
  
- [TimeZone (Availability)](timezone-availability.md)
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
|[偏置](bias.md) <br/> |表示与 UTC 偏移的偏移量，该偏移由标准时间和夏令时 [ (UTC) 元素 ](bias-utc.md) 标识。 此值以分钟为单位。  <br/> |
|[Time](time.md) <br/> |表示一天中与标准时间和夏令时之间的转换时间。  <br/> |
|[DayOrder](dayorder.md) <br/> |代表_n_th [DayOfWeek ](dayofweek-timezone.md) (TimeZone) 元素中指定的日期，该元素表示从标准时间和夏令时转换的日期。  <br/> |
|[Month](month.md) <br/> |表示与标准时间和夏令时之间的一年中的转换月份。  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |表示在标准时间和夏令时之间转换的一周中的一天。  <br/> |
|[Year](year.md) <br/> |定义根据年份更改的时区。 此元素为可选。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeZone (Availability)](timezone-availability.md) <br/> | 包含标识时区信息的元素。 此元素还包含有关标准时间和夏令时之间的转换的信息。 <br/><br/>下面是此元素的 XPath 表达式： <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a>注解

**StandardTime** 元素表示由 UTC 元素的 Bias [ (表示)](bias-utc.md)时间。 当子 [Bias](bias.md) 元素等于 0 时，标准时间等于从 UTC 的偏置偏移量（由 UTC ([表示）) ](bias-utc.md) 偏移。 
  
## <a name="example"></a>示例

以下示例显示观测到夏令时的区域。 从夏令时到标准时间之间的转换观测到上午 2 点。 在第十个月的第五个星期日。
  
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

