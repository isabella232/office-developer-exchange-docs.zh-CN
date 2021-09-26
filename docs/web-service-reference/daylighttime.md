---
title: DaylightTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DaylightTime
api_type:
- schema
ms.assetid: 9f551ee4-d945-477c-b981-9554b197d26d
description: DaylightTime 元素表示相对于协调世界时 (UTC) 的时差，该时间由观测到夏令时的区域中的 Bias (UTC) 元素表示。 此元素还包含有关何时从标准时间转换到夏令时的信息。
ms.openlocfilehash: 95d09fe01602f2d55d1a39dc7164a3f60a328f2a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543427"
---
# <a name="daylighttime"></a>DaylightTime

**DaylightTime** 元素表示相对于协调世界时 (UTC) 的时差，该时间由观测到夏令时的区域中的 Bias [ (UTC)](bias-utc.md)元素表示。 此元素还包含有关何时从标准时间转换到夏令时的信息。 
  
- [TimeZone (Availability)](timezone-availability.md) 
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
|[偏置](bias.md) <br/> |表示与 UTC 偏移的偏移量，该偏移由标准时间和夏令时 [ (UTC) 元素 ](bias-utc.md) 标识。 此值以分钟为单位。  <br/> |
|[Time](time.md) <br/> |表示一天中与标准时间和夏令时之间的转换时间。  <br/> |
|[DayOrder](dayorder.md) <br/> |代表_n_th [DayOfWeek ](dayofweek-timezone.md) (TimeZone) 元素中指定的日期，该元素表示从标准时间和夏令时转换的日期。  <br/> |
|[Month](month.md) <br/> |表示与标准时间和夏令时之间的一年中的转换月份。  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |表示在标准时间和夏令时之间转换的一周中的一天。  <br/> |
|[Year](year.md) <br/> |用于定义根据年份更改的时区。 此元素为可选。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeZone (Availability)](timezone-availability.md) <br/> | 包含标识时区信息的元素。<br/><br/>此元素还包含有关标准时间和夏令时之间的转换的信息。<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="example"></a>示例

以下部分 GetUserAvailability 请求表示识别夏令时的位置中的客户端应用程序。
  
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

