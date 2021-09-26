---
title: Recurrence (RecurrenceType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Recurrence
api_type:
- schema
ms.assetid: 3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12
description: Recurrence 元素包含定期模式和会议请求的组。
ms.openlocfilehash: 00dc47fd869f86cbd235ecd54085dbbfa510b18d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543994"
---
# <a name="recurrence-recurrencetype"></a>Recurrence (RecurrenceType)

**Recurrence** 元素包含定期模式和会议请求的组。 
  
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
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |描述相对每年定期模式。  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |代表每年定期模式。  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |描述定期日历定期模式相对每月日历项目。  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |表示每月重复模式。  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |描述日历项目或任务重复出现的频率（以周和天表示）。  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |描述日历项目或任务重复出现的频率（以天表示）。  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |描述定期模式没有定义的结束日期的约会。  <br/> 使用此元素将排除 [EndDateRecurrence](enddaterecurrence.md) 和 [NumberedRecurrence 元素](numberedrecurrence.md) 的使用。  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |描述项目的开始日期和结束日期定期模式。  <br/> 使用此元素不会使用 [NoEndRecurrence](noendrecurrence.md) 和 [NumberedRecurrence](numberedrecurrence.md) 元素。  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |描述开始日期和定期项目的发生次数。  <br/> 使用此元素将不使用 [NoEndRecurrence](noendrecurrence.md) 和 [EndDateRecurrence](enddaterecurrence.md) 元素。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示会议存储中的Exchange请求  <br/> |
   
## <a name="remarks"></a>注解

如果 [CalendarItemType](calendaritemtype.md) 具有 RecurringMaster 值，则此元素有效。 
  
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

