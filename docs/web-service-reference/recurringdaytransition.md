---
title: RecurringDayTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurringDayTransition
api_type:
- schema
ms.assetid: 1ae28d14-c2b8-4084-9e76-e2e347a884ce
description: RecurringDayTransition 元素表示在每年同一天发生的时区转换。
ms.openlocfilehash: 3b567e5b906ec00bd71deb1c85f8049bb6de8e3b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542881"
---
# <a name="recurringdaytransition"></a>RecurringDayTransition

**RecurringDayTransition** 元素表示在每年同一天发生的时区转换。 
  
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
|[To](to.md) <br/> |指定[作为时区](period.md)转换目标的 Period 或[TransitionsGroup。](transitionsgroup.md)  <br/> |
|[TimeOffset](timeoffset.md) <br/> |表示与时区转换的协调世界时 (UTC) 的持续时间偏移量。  <br/> |
|[Month (Time Zone Transition)](month-time-zone-transition.md) <br/> |表示时区转换发生的月份。  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |表示发生时区转换的一周中的哪一天。  <br/> |
|[Occurrence (Time Zone Transition)](occurrence-time-zone-transition.md) <br/> |表示发生时区转换的一周中的一天。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Transitions](transitions.md) <br/> |表示时区转换的集合。  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |表示时区转换的集合。  <br/> |
   
## <a name="remarks"></a>注解

由 [RecurringDayTransition](recurringdaytransition.md) 元素表示的时区转换示例是每年 2 月的第二个星期二发生的转换。 
  
描述此元素的架构位于运行安装了客户端访问服务器角色Microsoft Exchange Server的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

