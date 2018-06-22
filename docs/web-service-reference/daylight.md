---
title: 夏时制
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Daylight
api_type:
- schema
ms.assetid: ea400839-fba8-4a5e-a5d1-9b677afc0ff9
description: 夏时制元素均表示的日期和时间更改时从标准时间到夏时制的时间。
ms.openlocfilehash: cdb6ed305f1d77a73b952f8c659991f3b2a8df7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753757"
---
# <a name="daylight"></a>夏时制

**夏时制**元素均表示的日期和时间更改时从标准时间到夏时制的时间。 
  
```xml
<Daylight TimeZoneName="">
   <Offset/>
   <RelativeYearlyRecurrence/>
   <Time/>
</Daylight>
```

```xml
<Daylight TimeZoneName="">
   <Offset/>
   <AbsoluteDate/>
   <Time/>
</Daylight>
```

**TimeChangeType**

## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**TimeZoneName** <br/> |介绍时区的名称。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Offset](offset.md) <br/> |介绍从[BaseOffset](baseoffset.md)的偏移量。 基线偏移除了此偏移量标识根据是否是标准或夏时制的时间。  <br/> |
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |介绍所在的时区转换日期模式相对每年定期模式。  <br/> |
|[AbsoluteDate](absolutedate.md) <br/> |表示从标准版或夏时制时间的更改时的日期。  <br/> |
|[时间 (TimeChangeType)](time-timechangetype.md) <br/> |介绍当时间更改标准时间和夏时制之间的时间。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[MeetingTimeZone](meetingtimezone.md) <br/> |表示时区的会议所在的位置。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

