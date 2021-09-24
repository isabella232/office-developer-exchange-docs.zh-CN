---
title: 范围
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ee2891e4-3aa6-4258-9727-1f2ee9622508
description: Range 元素指定重复日历项目的日历项目发生次数范围。
ms.openlocfilehash: 0d16dad24dda48f084b3011d7b96eb719431d9da
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519098"
---
# <a name="range"></a>范围

**Range** 元素指定重复日历项目的日历项目发生次数范围。 
  
```XML
<Range Start="" End="" Count="" CompareOriginalStartTime=""/>
```

 **OccurrencesRangeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Start** <br/> |**Start** 属性的文本值是定期项目范围的开始日期。 这是 **dateTime** 值。  <br/> |
|**End** <br/> |**End** 属性的文本值是定期项目范围的结束日期。 这是 **dateTime** 值。  <br/> |
|**Count** <br/> |**Count** 属性的文本值是定期项目出现次数。 这是一个 **整数** 值。  <br/> |
|**CompareOriginalStartTime** <br/> |**CompareOriginalStartTime** 属性的文本值 **true** 指示客户端应比较原始开始时间和新开始时间。 false **值表示** 客户端不需要将原始开始时间与新的开始时间进行比较。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[Ranges](ranges.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> ||
   

