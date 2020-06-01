---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: SearchItemKind 元素指示要在其中搜索 FindMailboxStatisticsByKeyword 操作的项目的类型。
ms.openlocfilehash: e0625ac169c3083702494c094da15d38d220fe67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463998"
---
# <a name="searchitemkind"></a><span data-ttu-id="e0ca4-103">SearchItemKind</span><span class="sxs-lookup"><span data-stu-id="e0ca4-103">SearchItemKind</span></span>

<span data-ttu-id="e0ca4-104">**SearchItemKind**元素指示要在其中搜索**FindMailboxStatisticsByKeyword**操作的项目的类型。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-104">The **SearchItemKind** element indicates the type of items that are searched for a **FindMailboxStatisticsByKeyword** operation.</span></span> 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 <span data-ttu-id="e0ca4-105">**SearchItemKindType**</span><span class="sxs-lookup"><span data-stu-id="e0ca4-105">**SearchItemKindType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0ca4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e0ca4-106">Attributes and elements</span></span>

<span data-ttu-id="e0ca4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0ca4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e0ca4-108">Attributes</span></span>

<span data-ttu-id="e0ca4-109">无。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0ca4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e0ca4-110">Child elements</span></span>

<span data-ttu-id="e0ca4-111">无。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e0ca4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e0ca4-112">Parent elements</span></span>

[<span data-ttu-id="e0ca4-113">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="e0ca4-113">MessageTypes</span></span>](messagetypes.md)
  
## <a name="text-value"></a><span data-ttu-id="e0ca4-114">文本值</span><span class="sxs-lookup"><span data-stu-id="e0ca4-114">Text value</span></span>

<span data-ttu-id="e0ca4-115">**SearchItemKind**元素的文本值是要搜索关键字的项的类型。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-115">The text value of the **SearchItemKind** element is the type of item that is searched for keywords.</span></span> <span data-ttu-id="e0ca4-116">以下列表包含可在**SearchItemKind**元素中使用的文本值。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-116">The following list contains the text values that can be used in the **SearchItemKind** element.</span></span> 
  
- <span data-ttu-id="e0ca4-117">**电子**邮件-指示将搜索电子邮件中的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-117">**Email** - Indicates that email messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-118">**会议**-指示搜索会议的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-118">**Meetings** - Indicates that meetings are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-119">**任务**-指示搜索任务的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-119">**Tasks** - Indicates that tasks are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-120">**备注**-指示搜索笔记中的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-120">**Notes** - Indicates that notes are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-121">**文档**-指示搜索文档中的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-121">**Docs** - Indicates that documents are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-122">"**日记**"-指示搜索日记以查找关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-122">**Journals** - Indicates that journals are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-123">**联系人**-表示搜索联系人的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-123">**Contacts** - Indicates that contacts are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-124">**Im** -指示搜索即时消息中的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-124">**Im** - Indicates that instant messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-125">**语音邮件**-指示搜索语音邮件中的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-125">**Voicemail** - Indicates that voice mails are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-126">"**传真**"-指示搜索传真以查找关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-126">**Faxes** - Indicates that faxes are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-127">**帖子**-表示搜索帖子中的关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-127">**Posts** - Indicates that posts are searched for keywords.</span></span> 
    
- <span data-ttu-id="e0ca4-128">**Rssfeeds** -指示将搜索 RSS 源以查找关键字。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-128">**Rssfeeds** - Indicates that RSS feeds are searched for keywords.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e0ca4-129">备注</span><span class="sxs-lookup"><span data-stu-id="e0ca4-129">Remarks</span></span>

<span data-ttu-id="e0ca4-130">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e0ca4-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e0ca4-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0ca4-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="e0ca4-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0ca4-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="e0ca4-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e0ca4-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="e0ca4-134">Schema name</span></span>  <br/> |<span data-ttu-id="e0ca4-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="e0ca4-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="e0ca4-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="e0ca4-136">Validation file</span></span>  <br/> |<span data-ttu-id="e0ca4-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e0ca4-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e0ca4-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="e0ca4-138">Can be empty</span></span>  <br/> ||
   

