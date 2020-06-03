---
title: 范围
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: Range 元素指定重复日历项目的日历项目发生的范围。
ms.openlocfilehash: b5fb41709905290326b47e2662383031c34fd9c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465308"
---
# <a name="range"></a>范围

**Range**元素指定重复日历项目的日历项目发生的范围。 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Start** <br/> |**Start**属性的文本值是定期项目范围的开始日期。 这是一个**日期/时间**值。  <br/> |
|**End** <br/> |**End**属性的文本值是定期项目范围的结束日期。 这是一个**日期/时间**值。  <br/> |
|**Count** <br/> |**Count**属性的文本值是定期项目的次数。 这是**整数**值。  <br/> |
|**CompareOriginalStartTime** <br/> |如果**CompareOriginalStartTime**属性的文本值为**true，则**表示客户端应将原始开始时间与新的开始时间进行比较。 **如果值为 false** ，则表示客户端无需将原始开始时间与新开始时间进行比较。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[Ranges](ranges.md)
  
## <a name="remarks"></a>备注

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

