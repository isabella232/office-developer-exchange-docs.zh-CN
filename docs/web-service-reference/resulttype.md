---
title: ResultType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 488ee828-343f-4382-a5e8-eed1005f5dbc
description: ResultType 元素包含要执行搜索的类型。 搜索类型只能是统计信息或仅预览。
ms.openlocfilehash: 65227a8f79a7abd597653b646a7c3985c3e38ac9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509453"
---
# <a name="resulttype"></a>ResultType

**ResultType** 元素包含要执行搜索的类型。 搜索类型只能是统计信息或仅预览。 
  
```XML
<ResultType>StatisticsOnly | PreviewOnly</ResultType>
```

 **SearchResultType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[SearchMailboxesResult](searchmailboxesresult.md)  | [SearchMailboxes](searchmailboxes.md)
  
## <a name="text-value"></a>文本值

**ResultType** 元素的文本值是为发现搜索返回的结果类型。 **StatisticsOnly 的文本值** 将返回搜索统计信息。 **PreviewOnly 的文本值** 将返回项目预览信息。 
  
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
   

