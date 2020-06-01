---
title: 时区（可用性）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZone
api_type:
- schema
ms.assetid: d662ffae-1f93-4c08-85a4-c69de2f7c681
description: 时区元素包含标识时区信息的元素。 此元素还包含有关标准时间和夏时制之间转换的信息。
ms.openlocfilehash: ba4b0a4805dba54450e01e89c5e9ef746404b716
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460272"
---
# <a name="timezone-availability"></a>时区（可用性）

**时区**元素包含标识时区信息的元素。 此元素还包含有关标准时间和夏时制之间转换的信息。 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 **SerializableTimeZone**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[偏差（UTC）](bias-utc.md) <br/> |表示与协调世界时（UTC）的常规偏移量。 此值以分钟为单位。  <br/> |
|[StandardTime](standardtime.md) <br/> |表示与相对于 UTC（由 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。  <br/> |
|[DaylightTime](daylighttime.md) <br/> |表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |包含用于获取用户可用性信息的参数。 这是一个根元素。  <br/> GetUserAvailabilityRequest 消息中的**时区**元素表示在其中指定请求中的 DateTime 值的时区。 可用性服务返回的日期/时间值也在此时区中。  <br/> 以下是此元素的 XPath：  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |表示所请求的邮箱用户的时区设置和工作时间。  <br/> GetUserAvailabilityResponse 消息中的**时区**元素表示请求的邮箱用户的时区设置。  <br/> 以下是此元素的 XPath：  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a>备注

在[GetUserAvailabilityRequest](getuseravailabilityrequest.md)元素中，此元素是必需的。 当 parent 元素是[WorkingHours](workinghours-ex15websvcsotherref.md)元素时，此元素最多执行一次或至少出现零次。 
  
## <a name="example"></a>示例

下面的示例显示了 XML 请求的一部分，它标识客户端应用程序中的 UTC 时间为8小时的偏移量。
  
```XML
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>11</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>2</DayOrder>
    <Month>3</Month>
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



[GetUserAvailability 操作](getuseravailability-operation.md)
  
[偏置](bias.md)


[Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

