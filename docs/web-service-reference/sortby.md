---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: SortBy 元素包含用于对搜索结果进行排序的项属性。
ms.openlocfilehash: 8718bad3749a0409be2715b0e03001b97a4fb87e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544687"
---
# <a name="sortby"></a>SortBy

**SortBy** 元素包含用于对搜索结果进行排序的项属性。 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 **FieldOrderType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|Order  <br/> |**Order** 属性的文本值是排序顺序。 文本值 **Ascending** 指示结果按升序排序。 Descending **的文本** 值指示结果按降序排列。  <br/> |
   
### <a name="child-elements"></a>子元素

[FieldURI](fielduri.md)  | [IndexedFieldURI](indexedfielduri.md)
  
### <a name="parent-elements"></a>父元素

[SearchMailboxes](searchmailboxes.md)
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> ||
   

