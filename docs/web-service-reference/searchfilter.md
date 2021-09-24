---
title: SearchFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1a7ee364-b7da-4197-aab2-57134537109a
description: SearchFilter 元素包含查询字符串，用于筛选从 GetSearchableMailboxes 请求返回的邮箱。
ms.openlocfilehash: 19bb3109942c9a3064cbeaae4a19380d97c94feb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509355"
---
# <a name="searchfilter"></a>SearchFilter

**SearchFilter** 元素包含查询字符串，用于筛选从 **GetSearchableMailboxes** 请求返回的邮箱。 
  
```XML
<SearchFilter></SearchFilter>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetSearchableMailboxes](getsearchablemailboxes.md)
  
## <a name="text-value"></a>文本值

**SearchFilter** 元素的文本值是一个查询字符串，用于筛选邮箱以用于发现搜索。 
  
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
   

