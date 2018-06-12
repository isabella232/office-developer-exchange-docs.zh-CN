---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: SearchItemKind 元素指示 FindMailboxStatisticsByKeyword 操作搜索的项目的类型。
ms.openlocfilehash: 1c099fc49ec882c1672b265ff0e3aa2c71c5f95b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827298"
---
# <a name="searchitemkind"></a><span data-ttu-id="8bc0e-103">SearchItemKind</span><span class="sxs-lookup"><span data-stu-id="8bc0e-103">SearchItemKind</span></span>

<span data-ttu-id="8bc0e-104">**SearchItemKind**元素指示**FindMailboxStatisticsByKeyword**操作搜索的项目的类型。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-104">The **SearchItemKind** element indicates the type of items that are searched for a **FindMailboxStatisticsByKeyword** operation.</span></span> 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 <span data-ttu-id="8bc0e-105">**SearchItemKindType**</span><span class="sxs-lookup"><span data-stu-id="8bc0e-105">**SearchItemKindType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8bc0e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8bc0e-106">Attributes and elements</span></span>

<span data-ttu-id="8bc0e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8bc0e-108">属性</span><span class="sxs-lookup"><span data-stu-id="8bc0e-108">Attributes</span></span>

<span data-ttu-id="8bc0e-109">无。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8bc0e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8bc0e-110">Child elements</span></span>

<span data-ttu-id="8bc0e-111">无。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8bc0e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8bc0e-112">Parent elements</span></span>

[<span data-ttu-id="8bc0e-113">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="8bc0e-113">MessageTypes</span></span>](messagetypes.md)
  
## <a name="text-value"></a><span data-ttu-id="8bc0e-114">文本值</span><span class="sxs-lookup"><span data-stu-id="8bc0e-114">Text value</span></span>

<span data-ttu-id="8bc0e-115">**SearchItemKind**元素的文本值是项目的关键字搜索的类型。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-115">The text value of the **SearchItemKind** element is the type of item that is searched for keywords.</span></span> <span data-ttu-id="8bc0e-116">以下列表包含可在**SearchItemKind**元素中的文本值。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-116">The following list contains the text values that can be used in the **SearchItemKind** element.</span></span> 
  
- <span data-ttu-id="8bc0e-117">**电子邮件**-指示要搜索的关键字的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-117">**Email** - Indicates that email messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-118">**会议**-指示要搜索的关键字的会议。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-118">**Meetings** - Indicates that meetings are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-119">**任务**-指示要搜索的关键字的任务。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-119">**Tasks** - Indicates that tasks are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-120">**Notes** -指示说明要搜索的关键字。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-120">**Notes** - Indicates that notes are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-121">**文档**-指示要搜索的关键字的文档。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-121">**Docs** - Indicates that documents are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-122">**日志**-指示要搜索的关键字的日志。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-122">**Journals** - Indicates that journals are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-123">**联系人**-指示要搜索的关键字的联系人。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-123">**Contacts** - Indicates that contacts are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-124">**Im** -指示要搜索的关键字的即时消息。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-124">**Im** - Indicates that instant messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-125">**语音邮件**-指示要搜索的关键字的语音邮件。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-125">**Voicemail** - Indicates that voice mails are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-126">**传真**-指示要搜索的关键字的传真。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-126">**Faxes** - Indicates that faxes are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-127">**文章**-指示要搜索的关键字的文章。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-127">**Posts** - Indicates that posts are searched for keywords.</span></span> 
    
- <span data-ttu-id="8bc0e-128">**Rssfeeds** -指示要搜索的关键字的 RSS 源。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-128">**Rssfeeds** - Indicates that RSS feeds are searched for keywords.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8bc0e-129">备注</span><span class="sxs-lookup"><span data-stu-id="8bc0e-129">Remarks</span></span>

<span data-ttu-id="8bc0e-130">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8bc0e-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8bc0e-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8bc0e-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="8bc0e-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8bc0e-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="8bc0e-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8bc0e-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="8bc0e-134">Schema name</span></span>  <br/> |<span data-ttu-id="8bc0e-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="8bc0e-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="8bc0e-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="8bc0e-136">Validation file</span></span>  <br/> |<span data-ttu-id="8bc0e-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8bc0e-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8bc0e-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="8bc0e-138">Can be empty</span></span>  <br/> ||
   

