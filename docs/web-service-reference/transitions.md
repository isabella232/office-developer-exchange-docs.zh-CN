---
title: 移交
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transitions
api_type:
- schema
ms.assetid: 26f38f1c-96a3-440e-805c-1437886d11c5
description: 转换元素表示时区转换的数组。
ms.openlocfilehash: d48fb8872b2f7e052f733c32e5dd1c9b4d04d898
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467436"
---
# <a name="transitions"></a>移交

**转换**元素表示时区转换的数组。 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 **ArrayOfTransitionsType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Id  <br/> |表示时区定义的唯一标识符。  <br/> |
   
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |表示在特定日期和特定时间发生的时区转换。  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |表示时区转换发生在每年的同一天。  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |表示在指定的一年中的某一天发生的时区转换。  <br/> |
|[移交](transition.md) <br/> |表示时区转换。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[StartTimeZone](starttimezone.md) <br/> |定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)的开始时间的时区。  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)的结束时间的时区。  <br/> |
|[TimeZoneDefinition](timezonedefinition.md) <br/> |定义时区。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

