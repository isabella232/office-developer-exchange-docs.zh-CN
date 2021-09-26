---
title: Bias (UTC)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Bias
api_type:
- schema
ms.assetid: 15790d5a-5134-457b-8f2b-d9dee1f807a2
description: Bias 元素表示从协调世界时到 UTC (的) 。 此值以分钟为单位。
ms.openlocfilehash: c7dc50d13eecab72d06927ce02762e57ec2f8a3e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543651"
---
# <a name="bias-utc"></a>Bias (UTC)

**Bias** 元素表示从协调世界时到 UTC (的) 。 此值以分钟为单位。 
  
```xml
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
```

**int**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[TimeZone (Availability)](timezone-availability.md) <br/> | 标识请求的日期时间信息的容器。 此元素包含有关标准时间和夏令时之间的转换的信息。  <br/><br/>下面是此元素的 XPath 表达式：<br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。文本值表示一个整数。
  
## <a name="remarks"></a>说明

架构中的第二个 [Bias](bias.md) 元素表示从协调世界时到 UTC (偏移) 偏移。 
  
## <a name="example"></a>示例

以下示例显示标识客户端应用程序上与 UTC 的偏移量为 8 小时的 XML 请求的一部分。
  
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
- [偏置](bias.md)
- [Getting User Availability](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

