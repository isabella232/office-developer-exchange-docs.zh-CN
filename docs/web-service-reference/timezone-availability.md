---
title: TimeZone （可用性）
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
description: TimeZone 元素包含标识时区信息的元素。 此元素还包含有关标准时间和夏时制之间的转换的信息。
ms.openlocfilehash: dc2466e8039819edc82294ff05f1746ada64cb43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838253"
---
# <a name="timezone-availability"></a>TimeZone （可用性）

**TimeZone**元素包含标识时区信息的元素。 此元素还包含有关标准时间和夏时制之间的转换的信息。 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 **SerializableTimeZone**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[斜线 (UTC)](bias-utc.md) <br/> |从协调世界时 (UTC) 表示的常规的偏移量。 此值以分钟为单位。  <br/> |
|[StandardTime](standardtime.md) <br/> |表示与相对于 UTC（由 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关从观测到夏令时的区域中的夏令时转换为标准时间的信息。  <br/> |
|[DaylightTime](daylighttime.md) <br/> |表示与相对于 UTC（由观测到夏令时的区域的 [偏置 (UTC)](bias-utc.md) 元素表示）的时间的时差。此元素还包含有关何时从标准时间转换到夏令时的信息。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |包含用于获取用户的可用性信息的参数。 这是根元素。  <br/> GetUserAvailabilityRequest 消息中的**TimeZone**元素表示请求中的日期时间值指定的时区。 可用性服务返回的 DateTime 值也是在此所在的时区。  <br/> 以下是此元素的 XPath:  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |表示所在的时区设置和请求的邮箱用户的工作时间。  <br/> GetUserAvailabilityResponse 消息中的**TimeZone**元素表示请求的邮箱用户所在的时区设置。  <br/> 以下是此元素的 XPath:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a>注解

此元素是[GetUserAvailabilityRequest](getuseravailabilityrequest.md)元素中必需的。 此元素发生最一次或至少零次时的父元素是[WorkingHours](workinghours-ex15websvcsotherref.md)元素。 
  
## <a name="example"></a>示例

下面的示例演示标识与客户端应用程序中的 8 小时的 UTC 偏移量 XML 请求的一部分。
  
```XML
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetUserAvailability 操作](getuseravailability-operation.md)
  
[Bias](bias.md)


[Getting User Availability](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

