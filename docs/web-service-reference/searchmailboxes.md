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
ms.openlocfilehash: cf8007be3201e2248f27371c2a80c960735a3ced
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827306"
---
# <a name="searchmailboxes"></a><span data-ttu-id="706f5-103">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="706f5-103">SearchMailboxes</span></span>

<span data-ttu-id="706f5-104">**SearchMailboxes**元素指示**SearchMailboxes**请求的开头。</span><span class="sxs-lookup"><span data-stu-id="706f5-104">The **SearchMailboxes** element indicates the beginning of the **SearchMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="706f5-105">**SearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="706f5-105">**SearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="706f5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="706f5-106">Attributes and elements</span></span>

<span data-ttu-id="706f5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="706f5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="706f5-108">属性</span><span class="sxs-lookup"><span data-stu-id="706f5-108">Attributes</span></span>

<span data-ttu-id="706f5-109">无。</span><span class="sxs-lookup"><span data-stu-id="706f5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="706f5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="706f5-110">Child elements</span></span>

<span data-ttu-id="706f5-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [PreviewItemResponseShape](previewitemresponseshape.md) | [SortBy](sortby.md) | [语言](language.md) | [消除](deduplication.md) | [PageSize](pagesize.md)  |  [PageItemReference](pageitemreference.md) | [PageDirection](pagedirection.md)</span><span class="sxs-lookup"><span data-stu-id="706f5-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [PreviewItemResponseShape](previewitemresponseshape.md) | [SortBy](sortby.md) | [Language](language.md) | [Deduplication](deduplication.md) | [PageSize](pagesize.md) | [PageItemReference](pageitemreference.md) | [PageDirection](pagedirection.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="706f5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="706f5-112">Parent elements</span></span>

<span data-ttu-id="706f5-113">无。</span><span class="sxs-lookup"><span data-stu-id="706f5-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="706f5-114">备注</span><span class="sxs-lookup"><span data-stu-id="706f5-114">Remarks</span></span>

<span data-ttu-id="706f5-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="706f5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="706f5-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="706f5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="706f5-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="706f5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="706f5-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="706f5-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="706f5-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="706f5-119">Schema name</span></span>  <br/> |<span data-ttu-id="706f5-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="706f5-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="706f5-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="706f5-121">Validation file</span></span>  <br/> |<span data-ttu-id="706f5-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="706f5-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="706f5-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="706f5-123">Can be empty</span></span>  <br/> |<span data-ttu-id="706f5-124">false</span><span class="sxs-lookup"><span data-stu-id="706f5-124">false</span></span>  <br/> |
   

