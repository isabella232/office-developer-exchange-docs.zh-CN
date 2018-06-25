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
description: RecurringDayTransition 元素均表示发生在同一天每年时区转换。
ms.openlocfilehash: 913345188547ce9903809fdc1cbbbe3e20ae7f36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827012"
---
# <a name="recurringdaytransition"></a>RecurringDayTransition

**RecurringDayTransition**元素均表示发生在同一天每年时区转换。 
  
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

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[To](to.md) <br/> |指定[时段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标。  <br/> |
|[TimeOffset](timeoffset.md) <br/> |代表所在的时区转换的持续时间偏移量与协调世界时 (UTC)。  <br/> |
|[每月 （所在的时区转换）](month-time-zone-transition.md) <br/> |代表所在的时区转换发生的月份。  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |表示在所在的时区转换发生一周中的某一天。  <br/> |
|[出现 （所在的时区转换）](occurrence-time-zone-transition.md) <br/> |代表星期几所在的时区转换发生月中的匹配项。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[切换](transitions.md) <br/> |表示所在的时区转换的集合。  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |表示所在的时区转换的集合。  <br/> |
   
## <a name="remarks"></a>注解

无法由[RecurringDayTransition](recurringdaytransition.md)元素所在的时区转换的一个示例是发生年 2 月的第二个星期二每年的转换。 
  
描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

