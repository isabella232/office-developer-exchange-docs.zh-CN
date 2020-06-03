---
title: 重复周期（RecurrenceType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recurrence
api_type:
- schema
ms.assetid: 3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12
description: 定期元素包含日历项目和会议请求的定期模式。
ms.openlocfilehash: d00445c75fb35c3bb99eeed06e30cb1cf2883597
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529887"
---
# <a name="recurrence-recurrencetype"></a>重复周期（RecurrenceType）

**定期**元素包含日历项目和会议请求的定期模式。 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

**RecurrenceType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |介绍相对年定期模式。  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |代表每年定期模式。  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |描述定期日历项的相对月定期模式。  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |表示每月重复模式。  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |描述频率（以周为单位）以及日历项目或任务的重复发生日期。  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |描述日历项目或任务重复发生的频率（以天为单位）。  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |介绍没有定义的结束日期的定期模式。  <br/> 使用此元素不包括[EndDateRecurrence](enddaterecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |描述项目定期模式的开始日期和结束日期。  <br/> 使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |描述定期项目的开始日期和发生次数。  <br/> 使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[EndDateRecurrence](enddaterecurrence.md)元素的使用。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求  <br/> |
   
## <a name="remarks"></a>备注

如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

