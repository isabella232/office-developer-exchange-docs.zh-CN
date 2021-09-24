---
title: SearchArchiveOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cce5344c-b622-44d4-bc14-a0de346c9335
description: SearchArchiveOnly 元素指示是否仅搜索存档邮箱中的不可索引项目。
ms.openlocfilehash: a4766e101394bb83a0dcebdfe5b92f576f4a4160
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521675"
---
# <a name="searcharchiveonly"></a>SearchArchiveOnly

**SearchArchiveOnly** 元素指示是否仅搜索存档邮箱中的不可索引项目。 
  
```xml
<SearchArchiveOnly>true | false</SearchArchiveOnly>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) ？ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)
  
## <a name="text-value"></a>文本值

**SearchArchiveOnly** 元素的文本值 **true** 指示仅对存档邮箱执行不可编制索引的项目搜索。 文本值 **false** 表示对主邮箱和存档邮箱执行搜索。 
  
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
   

