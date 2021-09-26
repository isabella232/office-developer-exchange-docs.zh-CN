---
title: AbsoluteMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AbsoluteMonthlyRecurrence
api_type:
- schema
ms.assetid: 178fa0ae-9dfc-417f-933c-d657d31c2161
description: AbsoluteMonthlyRecurrence 元素表示每月定期模式。
ms.openlocfilehash: 7fcc1811a7c42fc653344fb3c052adac820d6a5d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546915"
---
# <a name="absolutemonthlyrecurrence"></a>AbsoluteMonthlyRecurrence

**AbsoluteMonthlyRecurrence** 元素表示每月定期模式。 
  
```xml
<AbsoluteMonthlyRecurrence>
   <Interval/>
   <DayOfMonth/>
</AbsoluteMonthlyRecurrence>
```

 **AbsoluteMonthlyRecurrencePatternType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[DayOfMonth](dayofmonth.md) <br/> |描述定期项目在一个月内发生的那一天。 此属性的值的范围为 1 到 31。 如果对于某个特定月份，此值大于月份中的天数，则假定此属性为月的最后一天。  <br/> |
|[Interval](interval.md) <br/> |定义两个连续定期项目之间的间隔。 例如，如果 **Interval** 元素的值为 5，则定期项目每 5 个月发生一次。 有效值的范围是 1 到 99。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Recurrence (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |包含定期任务的定期信息。  <br/> |
|[Recurrence (RecurrenceType)](recurrence-recurrencetype.md) <br/> |包含定期模式项和会议请求的联系人。  <br/> |
   
## <a name="remarks"></a>说明

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

