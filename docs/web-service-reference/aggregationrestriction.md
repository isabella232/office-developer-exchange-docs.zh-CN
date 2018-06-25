---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: AggregationRestriction 元素指定的一组由 FindPeople 请求产生的个人属性应用于和筛选结果，根据指定限制的值。
ms.openlocfilehash: 8b4d5952dedb4de0201d2ecf2219c69f65f7dc09
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753135"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

**AggregationRestriction**元素指定的一组由 FindPeople 请求产生的个人属性应用于和筛选结果，根据指定限制的值。 
  
```XML
<AggregationRestriction>
   <SearchExpression/>
</AggregationRestriction>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

[SearchExpression](searchexpression.md)
  
### <a name="parent-elements"></a>父元素

[FindPeople](findpeople.md)
  
## <a name="remarks"></a>注解

**AggregationRestriction**元素可以包含使用**SearchExpression**替换组任何子元素。 属于**SearchExpression**替换组元素：[包含](contains.md)[排除](excludes.md)、 [Exists](exists.md)、[不](not.md)、[或](or.md)、[和](and.md)、 [IsEqualTo](isequalto.md)、 [IsNotEqualTo](isnotequalto.md)， [IsGreaterThan](isgreaterthan.md)， [IsGreaterThanOrEqualTo](isgreaterthanorequalto.md)、 [IsLessThan](islessthan.md)和[IsLessThanOrEqualTo](islessthanorequalto.md)。
  
Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

