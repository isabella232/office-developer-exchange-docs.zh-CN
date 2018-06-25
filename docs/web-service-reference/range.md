---
title: Range
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: 范围元素指定各种重复的日历项目的日历项目发生次数。
ms.openlocfilehash: 0264c541604808b46a50e292b8ff75f205796295
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826946"
---
# <a name="range"></a>Range

**范围**元素指定各种重复的日历项目的日历项目发生次数。 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**Start** <br/> |**启动**属性的文本值是定期项目范围的开始日期。 这是**dateTime**值。  <br/> |
|**End** <br/> |**End**属性的文本值是定期项目范围的结束日期。 这是**dateTime**值。  <br/> |
|**Count** <br/> |**计数**属性的文本值是定期项目的次数。 这是一个**整数**值。  <br/> |
|**CompareOriginalStartTime** <br/> |文本值为**true**的**CompareOriginalStartTime**属性指示客户端应比较使用新的开始时间的原始开始时间。 如果值为**false**指示客户端不需要比较使用新的开始时间的原始开始时间。  <br/> |
   
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

