---
title: AbsoluteYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteYearlyRecurrence
api_type:
- schema
ms.assetid: 96f53e2c-3893-4f6e-a78a-ac179f45c5db
description: AbsoluteYearlyRecurrence 元素表示每年定期模式。
ms.openlocfilehash: 205da336a6a6ca4fd39120e83ab264e1543354e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754236"
---
# <a name="absoluteyearlyrecurrence"></a>AbsoluteYearlyRecurrence

**AbsoluteYearlyRecurrence**元素表示每年定期模式。 
  
```xml
<AbsoluteYearlyRecurrence>
   <DayOfMonth/>
   <Month/>
</AbsoluteYearlyRecurrence>
```

 **AbsoluteYearlyRecurrencePatternType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DayOfMonth](dayofmonth.md) <br/> |描述定期项目出现在其一个月中的一天。 此属性的值范围为 1 到 31。 如果特定月此值大于当月的天数，相应月份的最后一天则假定此属性。  <br/> |
|[每月 （项重复）](month-item-recurrence.md) <br/> |介绍每年定期项目发生的月份。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[定期 (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |包含定期周期性任务信息。  <br/> |
|[定期 (RecurrenceType)](recurrence-recurrencetype.md) <br/> |包含日历项和会议请求的定期模式。  <br/> |
   
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

