---
title: DaysOfWeek (DayOfWeekType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DaysOfWeek
api_type:
- schema
ms.assetid: ba8f990d-d37d-403d-b31f-55e5208c8ad5
description: DaysOfWeek 元素描述项目定期模式中使用的星期几。
ms.openlocfilehash: f30184755117c7561b66e93491cbd68534064eeb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525104"
---
# <a name="daysofweek-dayofweektype"></a>DaysOfWeek (DayOfWeekType)

**DaysOfWeek** 元素描述项目定期模式中使用的星期几。 
  
```xml
<DaysOfWeek/>
```

**DayOfWeekType**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |描述相对每年定期模式。  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |描述相对每月定期模式。  <br/> |
   
## <a name="text-value"></a>文本值

文本值是必需的。 以下是可能的值：
  
- 星期日    
- 星期一    
- 星期二   
- 星期三    
- 星期四    
- 星期五    
- 星期六    
- TimeChangePatternTypes (中未使用的日)     
- Weekday (在 TimeChangePatternTypes 属性中)     
- WeekendDay (TimeChangePatternTypes 属性中) 
    
## <a name="remarks"></a>注解

描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

