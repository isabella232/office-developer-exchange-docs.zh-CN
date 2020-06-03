---
title: RelativeYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeYearlyRecurrence
api_type:
- schema
ms.assetid: 25b67876-9979-4a30-a637-357ea10a93b8
description: RelativeYearlyRecurrence 元素描述相对年定期模式。
ms.openlocfilehash: 2abe09ddfe52c24211ef5d0a392ddecaf15bf7bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456724"
---
# <a name="relativeyearlyrecurrence"></a>RelativeYearlyRecurrence

**RelativeYearlyRecurrence**元素描述相对年定期模式。 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 **RelativeYearlyRecurrencePatternType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DaysOfWeek （DayOfWeekType）](daysofweek-dayofweektype.md) <br/> |介绍在项目定期模式中使用的一周中的各天。  <br/> |
|[DayOfWeekIndex](dayofweekindex.md) <br/> |介绍在相对年定期模式中使用某个月中的哪一周。  <br/> |
|[月（项目定期）](month-item-recurrence.md) <br/> |描述每年定期项目发生的月份。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[重复周期（TaskRecurrenceType）](recurrence-taskrecurrencetype.md) <br/> |包含定期任务的定期信息。  <br/> |
|[重复周期（RecurrenceType）](recurrence-recurrencetype.md) <br/> |包含日历项目和会议请求的定期模式。  <br/> |
|[标准](standard.md) <br/> |表示当时间从夏令时更改为标准时间时的日期和时间。  <br/> |
|[夏时制](daylight.md) <br/> |表示时间从标准时间更改为夏时制的日期和时间。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

