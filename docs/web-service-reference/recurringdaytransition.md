---
title: RecurringDayTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDayTransition
api_type:
- schema
ms.assetid: 1ae28d14-c2b8-4084-9e76-e2e347a884ce
description: RecurringDayTransition 元素表示每年在同一天发生的时区转换。
ms.openlocfilehash: 44c2a6ec4dbaaa52a2772cb5c35a84b14dd77f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468465"
---
# <a name="recurringdaytransition"></a>RecurringDayTransition

**RecurringDayTransition**元素表示每年在同一天发生的时区转换。 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 **RecurringDayTransitionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[To](to.md) <br/> |指定作为时区转换目标的[时间段](period.md)或[TransitionsGroup](transitionsgroup.md) 。  <br/> |
|[TimeOffset](timeoffset.md) <br/> |表示时区转换与协调世界时（UTC）之间的持续时间偏移量。  <br/> |
|[Month （时区转换）](month-time-zone-transition.md) <br/> |表示发生时区转换的月份。  <br/> |
|[DayOfWeek （时区）](dayofweek-timezone.md) <br/> |表示发生时区转换的一周中的某一天。  <br/> |
|[事件（时区转换）](occurrence-time-zone-transition.md) <br/> |表示发生时区转换的月份中的一周中的某一天的匹配项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[移交](transitions.md) <br/> |表示时区转换的集合。  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |表示时区转换的集合。  <br/> |
   
## <a name="remarks"></a>备注

[RecurringDayTransition](recurringdaytransition.md)元素可以表示的时区转换的一个示例是每年2月的第二个星期二发生的转换。 
  
描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

