---
title: 定期 (TaskRecurrenceType)
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
ms.assetid: 99f8414a-9110-4721-a6e5-ebf225d7ed0a
description: Recurrence 元素包含定期周期性任务信息。
ms.openlocfilehash: ae2bb35e89a0a50c7ca67cb0e580427150afb99e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827006"
---
# <a name="recurrence-taskrecurrencetype"></a>定期 (TaskRecurrenceType)

**Recurrence**元素包含定期周期性任务信息。 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 **TaskRecurrenceType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |描述定期任务的相对于每年定期模式。  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |代表每年定期模式的定期任务。  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |介绍的相对每月定期模式的定期任务。  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |代表每月定期模式的定期任务。  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |介绍频率，周和任务重复的天数。  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |描述任务重复出现的频率（以天为单位）。  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |介绍多少天后完成当前任务的下一个匹配项将到期。  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |介绍多少周后完成当前任务的下一个匹配项将到期。  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |介绍多少个月后完成当前任务的下一个匹配项将到期。  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |介绍如何许多年后完成当前任务的下一个匹配项将到期。  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |介绍没有定义的结束日期的定期模式。  <br/> 使用此元素不包括[EndDateRecurrence](enddaterecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |介绍的开始日期和结束日期的项目定期模式。  <br/> 使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[NumberedRecurrence](numberedrecurrence.md)元素的使用。  <br/> [EndDateRecurrence](enddaterecurrence.md)无法一起再生模式。  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |介绍的开始日期和定期项目的次数。  <br/> 使用此元素不包括[NoEndRecurrence](noendrecurrence.md)和[EndDateRecurrence](enddaterecurrence.md)元素的使用。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

