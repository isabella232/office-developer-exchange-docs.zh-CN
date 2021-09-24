---
title: Periods
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Periods
api_type:
- schema
ms.assetid: 7920d81d-abba-4232-8bfe-49267b6c9a36
description: Periods 元素表示一个时间段数组，该数组定义时区的不同阶段的时间偏移。
ms.openlocfilehash: e4a614c71e7194dd85db740da1796b69d9f25d69
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515311"
---
# <a name="periods"></a>Periods

**Periods** 元素表示一个时间段数组，该数组定义时区的不同阶段的时间偏移。 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 **NonEmptyArrayOfPeriodsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[句号](period.md) <br/> |定义时区特定阶段的名称、时间偏移和唯一标识符。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[StartTimeZone](starttimezone.md) <br/> |定义 [CalendarItem](calendaritem.md) 或 [MeetingRequest](meetingrequest.md)的开始时间的时区。  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |定义 [CalendarItem](calendaritem.md) 或 [MeetingRequest](meetingrequest.md)的结束时间时区。  <br/> |
|[TimeZoneDefinition](timezonedefinition.md) <br/> |定义时区。  <br/> |
   
## <a name="remarks"></a>注解

描述此元素的架构位于运行已安装客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

