---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: SortOrder 元素指定用于 GetConversationItems 请求的结果的排序顺序。
ms.openlocfilehash: 397aead62d32e72f991af783bff02e79a6e4b0fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827520"
---
# <a name="sortorder-conversationnodesortorder"></a><span data-ttu-id="e3e55-103">SortOrder (ConversationNodeSortOrder)</span><span class="sxs-lookup"><span data-stu-id="e3e55-103">SortOrder (ConversationNodeSortOrder)</span></span>

<span data-ttu-id="e3e55-104">**SortOrder**元素指定用于**GetConversationItems**请求的结果的排序顺序。</span><span class="sxs-lookup"><span data-stu-id="e3e55-104">The **SortOrder** element specifies the sort order used for the result of a **GetConversationItems** request.</span></span> 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 <span data-ttu-id="e3e55-105">**ConversationNodeSortOrder**</span><span class="sxs-lookup"><span data-stu-id="e3e55-105">**ConversationNodeSortOrder**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3e55-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3e55-106">Attributes and elements</span></span>

<span data-ttu-id="e3e55-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3e55-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3e55-108">属性</span><span class="sxs-lookup"><span data-stu-id="e3e55-108">Attributes</span></span>

<span data-ttu-id="e3e55-109">无。</span><span class="sxs-lookup"><span data-stu-id="e3e55-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3e55-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e3e55-110">Child elements</span></span>

<span data-ttu-id="e3e55-111">无。</span><span class="sxs-lookup"><span data-stu-id="e3e55-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3e55-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e3e55-112">Parent elements</span></span>

[<span data-ttu-id="e3e55-113">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="e3e55-113">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="text-value"></a><span data-ttu-id="e3e55-114">文本值</span><span class="sxs-lookup"><span data-stu-id="e3e55-114">Text value</span></span>

<span data-ttu-id="e3e55-115">**SortOrder**元素的文本值是在其中对话排序的顺序。</span><span class="sxs-lookup"><span data-stu-id="e3e55-115">The text value of the **SortOrder** element is the order in which conversations ordered.</span></span> <span data-ttu-id="e3e55-116">**TreeOrderAscending**文本值指示对话了排序根据升序排序的对话树。</span><span class="sxs-lookup"><span data-stu-id="e3e55-116">A text value of **TreeOrderAscending** indicates that the conversations are ordered according to the conversation tree in ascending order.</span></span> <span data-ttu-id="e3e55-117">**TreeOrderDescending**文本值指示对话了排序根据按降序顺序的对话树。</span><span class="sxs-lookup"><span data-stu-id="e3e55-117">A text value of **TreeOrderDescending** indicates that the conversations are ordered according to the conversation tree in descending order.</span></span> <span data-ttu-id="e3e55-118">**DateOrderAscending**文本值指示对话进行排序以升序对话 date。</span><span class="sxs-lookup"><span data-stu-id="e3e55-118">A text value of **DateOrderAscending** indicates that the conversations are ordered according to the conversation date in ascending order.</span></span> <span data-ttu-id="e3e55-119">**DateOrderDescending**文本值指示对话了排序按降序顺序对话 date。</span><span class="sxs-lookup"><span data-stu-id="e3e55-119">A text value of **DateOrderDescending** indicates that the conversations are ordered according to the conversation date in descending order.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e3e55-120">备注</span><span class="sxs-lookup"><span data-stu-id="e3e55-120">Remarks</span></span>

<span data-ttu-id="e3e55-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e3e55-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e3e55-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e3e55-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3e55-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3e55-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3e55-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3e55-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e3e55-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3e55-125">Schema name</span></span>  <br/> |<span data-ttu-id="e3e55-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="e3e55-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e3e55-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3e55-127">Validation file</span></span>  <br/> |<span data-ttu-id="e3e55-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e3e55-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3e55-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3e55-129">Can be empty</span></span>  <br/> ||
   

