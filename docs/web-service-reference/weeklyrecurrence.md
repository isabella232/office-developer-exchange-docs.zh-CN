---
title: WeeklyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRecurrence
api_type:
- schema
ms.assetid: 69c41dd5-597c-45bc-be3f-e2f2b5615aa3
description: WeeklyRecurrence 元素描述每周定期模式。
ms.openlocfilehash: 5006238590c4cd7556a92fb1fbe13292383412b8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530364"
---
# <a name="weeklyrecurrence"></a>WeeklyRecurrence

**WeeklyRecurrence**元素描述每周定期模式。 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 **WeeklyRecurrencePatternType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Interval](interval.md) <br/> |定义两个连续的每周定期模式项目之间的时间间隔（以周为单位）。 该值可以介于1到99之间。  <br/> |
|[DaysOfWeek （DaysOfWeekType）](daysofweek-daysofweektype.md) <br/> |介绍周中的哪几天在每周定期模式中。  <br/> |
|[FirstDayOfWeek](firstdayofweek.md) <br/> |指定一周的第一天。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[重复周期（TaskRecurrenceType）](recurrence-taskrecurrencetype.md) <br/> |包含定期任务的定期信息。  <br/> |
|[重复周期（RecurrenceType）](recurrence-recurrencetype.md) <br/> |包含日历项目和会议请求的定期模式。  <br/> |
   
## <a name="text-value"></a>文本值

无。
  
## <a name="remarks"></a>说明

如果定期主项目的[开始](start.md)和[结束](end-ex15websvcsotherref.md)日期不具有与每周定期模式的第一个匹配项相等的日期，则将丢失时区偏移信息。 
  
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

