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
ms.openlocfilehash: 79d593d99762aedc6290578b5458f9ac3cad3d26
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466701"
---
# <a name="searchmailboxesresult"></a><span data-ttu-id="4886f-103">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="4886f-103">SearchMailboxesResult</span></span>

<span data-ttu-id="4886f-104">**SearchMailboxesResult**元素包含**SearchMailboxes**请求的结果。</span><span class="sxs-lookup"><span data-stu-id="4886f-104">The **SearchMailboxesResult** element contains the result of the **SearchMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="4886f-105">**SearchMailboxesResultType**</span><span class="sxs-lookup"><span data-stu-id="4886f-105">**SearchMailboxesResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4886f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4886f-106">Attributes and elements</span></span>

<span data-ttu-id="4886f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4886f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4886f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4886f-108">Attributes</span></span>

<span data-ttu-id="4886f-109">无。</span><span class="sxs-lookup"><span data-stu-id="4886f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4886f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4886f-110">Child elements</span></span>

<span data-ttu-id="4886f-111">[SearchQueries](searchqueries.md)  | [ResultType](resulttype.md)  | [ItemCount](itemcount.md)  | [大小（long）](size-long.md)  | [PageItemCount](pageitemcount.md)  | [PageItemSize](pageitemsize.md)  | [KeywordStats](keywordstats.md)  | [项目（ArrayOfSearchPreviewItemsType）](items-arrayofsearchpreviewitemstype.md)  | [FailedMailboxes](failedmailboxes.md)  | [精简条件](refiners.md)  | [MailboxStats](mailboxstats.md)</span><span class="sxs-lookup"><span data-stu-id="4886f-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md) | [PageItemCount](pageitemcount.md) | [PageItemSize](pageitemsize.md) | [KeywordStats](keywordstats.md) | [Items (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md) | [FailedMailboxes](failedmailboxes.md) | [Refiners](refiners.md) | [MailboxStats](mailboxstats.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4886f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4886f-112">Parent elements</span></span>

[<span data-ttu-id="4886f-113">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4886f-113">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="4886f-114">备注</span><span class="sxs-lookup"><span data-stu-id="4886f-114">Remarks</span></span>

<span data-ttu-id="4886f-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4886f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4886f-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4886f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4886f-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="4886f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4886f-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="4886f-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4886f-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="4886f-119">Schema name</span></span>  <br/> |<span data-ttu-id="4886f-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="4886f-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4886f-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="4886f-121">Validation file</span></span>  <br/> |<span data-ttu-id="4886f-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4886f-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4886f-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="4886f-123">Can be empty</span></span>  <br/> |<span data-ttu-id="4886f-124">false</span><span class="sxs-lookup"><span data-stu-id="4886f-124">false</span></span>  <br/> |
   

