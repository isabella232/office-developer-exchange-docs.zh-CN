---
title: SearchMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5d8c367a-67e9-43b3-8be0-6362d2152431
description: SearchMailboxes 元素指示 SearchMailboxes 请求的开始。
ms.openlocfilehash: 3c734e49869a17fa58252668ddae606d702f3047
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521591"
---
# <a name="searchmailboxes"></a>SearchMailboxes

**SearchMailboxes** 元素指示 **SearchMailboxes** 请求的开始。 
  
```XML
<SearchMailboxes>
   <SearchQueries/>
   <ResultType/>
   <PreviewItemResponseShape/>
   <SortBy/>
   <Language/>
   <Deduplication/>
   <PageSize/>
   <PageItemReference/>
   <PageDirection/>
</SearchMailboxes>
```

 **SearchMailboxesType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[SearchQueries](searchqueries.md)  | [ResultType](resulttype.md)  | [PreviewItemResponseShape](previewitemresponseshape.md)  | [SortBy](sortby.md)  | [语言](language.md)  | [重复数据删除](deduplication.md)  | [PageSize](pagesize.md)  | [PageItemReference](pageitemreference.md)  | [PageDirection](pagedirection.md)
  
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>注解

Exchange Server 2013 中引入了此元素。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |false  <br/> |
   

