---
title: SearchMailboxesResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddb276c4-6c8a-46ef-a2eb-46b6a0bfce09
description: SearchMailboxesResult 元素包含 SearchMailboxes 请求的结果。
ms.openlocfilehash: 93e5837216ef8942b77ac2a91f5ef5f0ad001756
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827300"
---
# <a name="searchmailboxesresult"></a><span data-ttu-id="8a0bd-103">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="8a0bd-103">SearchMailboxesResult</span></span>

<span data-ttu-id="8a0bd-104">**SearchMailboxesResult**元素包含**SearchMailboxes**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="8a0bd-104">The **SearchMailboxesResult** element contains the result of the **SearchMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="8a0bd-105">**SearchMailboxesResultType**</span><span class="sxs-lookup"><span data-stu-id="8a0bd-105">**SearchMailboxesResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a0bd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a0bd-106">Attributes and elements</span></span>

<span data-ttu-id="8a0bd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a0bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a0bd-108">属性</span><span class="sxs-lookup"><span data-stu-id="8a0bd-108">Attributes</span></span>

<span data-ttu-id="8a0bd-109">无。</span><span class="sxs-lookup"><span data-stu-id="8a0bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a0bd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8a0bd-110">Child elements</span></span>

<span data-ttu-id="8a0bd-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [ItemCount](itemcount.md) | [大小 (long)](size-long.md) | [PageItemCount](pageitemcount.md) | [PageItemSize](pageitemsize.md) | [KeywordStats](keywordstats.md) | [项目 （ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md) | [FailedMailboxes](failedmailboxes.md) | [精简程序](refiners.md) | [MailboxStats](mailboxstats.md)</span><span class="sxs-lookup"><span data-stu-id="8a0bd-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md) | [PageItemCount](pageitemcount.md) | [PageItemSize](pageitemsize.md) | [KeywordStats](keywordstats.md) | [Items (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md) | [FailedMailboxes](failedmailboxes.md) | [Refiners](refiners.md) | [MailboxStats](mailboxstats.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a0bd-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8a0bd-112">Parent elements</span></span>

[<span data-ttu-id="8a0bd-113">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8a0bd-113">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="8a0bd-114">备注</span><span class="sxs-lookup"><span data-stu-id="8a0bd-114">Remarks</span></span>

<span data-ttu-id="8a0bd-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8a0bd-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8a0bd-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a0bd-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a0bd-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a0bd-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a0bd-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a0bd-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a0bd-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a0bd-119">Schema name</span></span>  <br/> |<span data-ttu-id="8a0bd-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="8a0bd-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8a0bd-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a0bd-121">Validation file</span></span>  <br/> |<span data-ttu-id="8a0bd-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8a0bd-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a0bd-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a0bd-123">Can be empty</span></span>  <br/> |<span data-ttu-id="8a0bd-124">false</span><span class="sxs-lookup"><span data-stu-id="8a0bd-124">false</span></span>  <br/> |
   

