---
title: 时间间隔
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Interval
api_type:
- schema
ms.assetid: d0c97a5f-96be-40c6-b7d4-abf4c3870adf
description: Interval 元素定义两个连续周期性项目之间的间隔。
ms.openlocfilehash: 6df46865d7a89a0bfde9afc5f84ffdb78d956a30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541026"
---
# <a name="interval"></a>时间间隔

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Interval** 元素定义两个连续周期性项目之间的间隔。 
  
```xml
<Interval/>
```

 **int**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |表示每月重复模式。  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |描述任务重新生成的频率（以天为单位）。  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |描述任务重复出现的频率（以天为单位）。  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |描述任务重新生成的频率（以月为单位）。  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |描述周期性任务的每月相对模式。  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |描述任务重复出现的频率（以周或天为单位）。  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |描述任务重新生成的频率（以周为单位）。  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |描述任务重新生成的频率（以年为单位）。  <br/> |
   
## <a name="text-value"></a>文本值

需要表示整数的一个文本值。
  
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

