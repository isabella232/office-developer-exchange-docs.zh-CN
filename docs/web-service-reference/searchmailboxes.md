---
title: SearchMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d8c367a-67e9-43b3-8be0-6362d2152431
description: SearchMailboxes 元素指示 SearchMailboxes 请求的开头。
ms.openlocfilehash: 7ccc94157ef6bde7b6ba86e70c16ef6e90d712fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456799"
---
# <a name="searchmailboxes"></a><span data-ttu-id="1c116-103">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="1c116-103">SearchMailboxes</span></span>

<span data-ttu-id="1c116-104">**SearchMailboxes**元素指示**SearchMailboxes**请求的开头。</span><span class="sxs-lookup"><span data-stu-id="1c116-104">The **SearchMailboxes** element indicates the beginning of the **SearchMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="1c116-105">**SearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="1c116-105">**SearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c116-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1c116-106">Attributes and elements</span></span>

<span data-ttu-id="1c116-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1c116-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c116-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1c116-108">Attributes</span></span>

<span data-ttu-id="1c116-109">无。</span><span class="sxs-lookup"><span data-stu-id="1c116-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c116-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1c116-110">Child elements</span></span>

<span data-ttu-id="1c116-111">[SearchQueries](searchqueries.md)  | [ResultType](resulttype.md)  | [PreviewItemResponseShape](previewitemresponseshape.md)  | [SortBy](sortby.md)  | [语言](language.md)  | [删除](deduplication.md)  | [PageSize](pagesize.md)  | [PageItemReference](pageitemreference.md)  | [PageDirection](pagedirection.md)</span><span class="sxs-lookup"><span data-stu-id="1c116-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [PreviewItemResponseShape](previewitemresponseshape.md) | [SortBy](sortby.md) | [Language](language.md) | [Deduplication](deduplication.md) | [PageSize](pagesize.md) | [PageItemReference](pageitemreference.md) | [PageDirection](pagedirection.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1c116-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1c116-112">Parent elements</span></span>

<span data-ttu-id="1c116-113">无。</span><span class="sxs-lookup"><span data-stu-id="1c116-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1c116-114">说明</span><span class="sxs-lookup"><span data-stu-id="1c116-114">Remarks</span></span>

<span data-ttu-id="1c116-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1c116-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1c116-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1c116-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1c116-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1c116-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c116-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1c116-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1c116-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1c116-119">Schema name</span></span>  <br/> |<span data-ttu-id="1c116-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="1c116-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1c116-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1c116-121">Validation file</span></span>  <br/> |<span data-ttu-id="1c116-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1c116-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1c116-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1c116-123">Can be empty</span></span>  <br/> |<span data-ttu-id="1c116-124">false</span><span class="sxs-lookup"><span data-stu-id="1c116-124">false</span></span>  <br/> |
   

