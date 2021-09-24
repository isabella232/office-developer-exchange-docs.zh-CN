---
title: SearchMailboxesResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ddb276c4-6c8a-46ef-a2eb-46b6a0bfce09
description: SearchMailboxesResult 元素包含 SearchMailboxes 请求的结果。
ms.openlocfilehash: dee1e12a6d083ca3f8d3ddb509775b454e3e8fc0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534403"
---
# <a name="searchmailboxesresult"></a>SearchMailboxesResult

**SearchMailboxesResult** 元素包含 **SearchMailboxes** 请求的结果。 
  
```XML
<SearchMailboxesResult>
   <SearchQueries/>
   <ResultType/>
   <ItemCount/>
   <Size/>
   <PageItemCount/>
   <PageItemSize/>
   <KeywordStats/>
   <Items/>
   <FailedMailboxes/>
   <Refiners/>
   <MailboxStats/>
</SearchMailboxesResult>
```

 **SearchMailboxesResultType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

[SearchQueries](searchqueries.md)  | [ResultType](resulttype.md)  | [ItemCount](itemcount.md)  | [长 (大小) ](size-long.md)  | [PageItemCount](pageitemcount.md)  | [PageItemSize](pageitemsize.md)  | [KeywordStats](keywordstats.md)  | [ArrayOfSearchPreviewItemsType (项) ](items-arrayofsearchpreviewitemstype.md)  | [FailedMailboxes](failedmailboxes.md)  | [精简条件](refiners.md)  | [MailboxStats](mailboxstats.md)
  
### <a name="parent-elements"></a>父元素

[SearchMailboxesResponseMessage](searchmailboxesresponsemessage.md)
  
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
   

