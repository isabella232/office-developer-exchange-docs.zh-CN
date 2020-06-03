---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: AggregationRestriction 元素指定应用于由 FindPeople 请求生成的一组角色属性的值，并根据指定的限制筛选结果。
ms.openlocfilehash: f07e54235cf13b43da26ed1c56596d3c7c357bf2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463522"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

**AggregationRestriction**元素指定应用于由 FindPeople 请求生成的一组角色属性的值，并根据指定的限制筛选结果。 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[SearchExpression](searchexpression.md)
  
### <a name="parent-elements"></a>父元素

[FindPeople](findpeople.md)
  
## <a name="remarks"></a>备注

**AggregationRestriction**元素可以包含使用**SearchExpression**替换组的任何子元素。 作为**SearchExpression**替换组的一部分的元素为： [Contains](contains.md)、不[包括](excludes.md)、 [Exists](exists.md)、 [Not](not.md)、 [Or](or.md)、 [And](and.md)、 [IsEqualTo](isequalto.md)、 [IsNotEqualTo](isnotequalto.md)、 [IsGreaterThan](isgreaterthan.md)、 [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)、 [IsLessThan](islessthan.md)和[IsLessThanOrEqualTo](islessthanorequalto.md)。
  
Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |消息 .xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

