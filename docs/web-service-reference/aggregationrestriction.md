---
title: AggregationRestriction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d05044f9-d2ff-4aca-956c-20c9cb2f7709
description: AggregationRestriction 元素指定一个值，该值应用于由 FindPeople 请求生成的一组 Persona 属性，并按指定的限制筛选结果。
ms.openlocfilehash: 6a00035f87e0f365f4551df1a6ff570e01761770
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546789"
---
# <a name="aggregationrestriction"></a>AggregationRestriction

**AggregationRestriction** 元素指定一个值，该值应用于由 FindPeople 请求生成的一组 Persona 属性，并按指定的限制筛选结果。 
  
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
  
## <a name="remarks"></a>注解

**AggregationRestriction** 元素可以包含使用 **SearchExpression** 替换组的任何子元素。 属于 **SearchExpression** 替换组的元素包括：Contains、Excludes、Exists、Not、Or、And、IsEqualTo、IsNotEqualTo、IsGreaterThan、IsGreaterThanOrEqualTo、IsLessThan [](islessthan.md)和 [](excludes.md)[](isnotequalto.md)[IsLessThanOrEqualTo](islessthanorequalto.md)。 [](contains.md) [](exists.md) [](not.md) [](or.md) [](and.md) [](isequalto.md) [](isgreaterthan.md) [](isgreaterthanorequalto.md)
  
Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

