---
title: SortOrder （ConversationNodeSortOrder）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: SortOrder 元素指定用于 GetConversationItems 请求结果的排序顺序。
ms.openlocfilehash: 69d362b9f769749bcc9692825b64ff486e8b60a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530963"
---
# <a name="sortorder-conversationnodesortorder"></a><span data-ttu-id="9fdc4-103">SortOrder （ConversationNodeSortOrder）</span><span class="sxs-lookup"><span data-stu-id="9fdc4-103">SortOrder (ConversationNodeSortOrder)</span></span>

<span data-ttu-id="9fdc4-104">**SortOrder**元素指定用于**GetConversationItems**请求结果的排序顺序。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-104">The **SortOrder** element specifies the sort order used for the result of a **GetConversationItems** request.</span></span> 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 <span data-ttu-id="9fdc4-105">**ConversationNodeSortOrder**</span><span class="sxs-lookup"><span data-stu-id="9fdc4-105">**ConversationNodeSortOrder**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9fdc4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9fdc4-106">Attributes and elements</span></span>

<span data-ttu-id="9fdc4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9fdc4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9fdc4-108">Attributes</span></span>

<span data-ttu-id="9fdc4-109">无。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9fdc4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9fdc4-110">Child elements</span></span>

<span data-ttu-id="9fdc4-111">无。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9fdc4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9fdc4-112">Parent elements</span></span>

[<span data-ttu-id="9fdc4-113">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="9fdc4-113">GetConversationItems</span></span>](getconversationitems.md)
  
## <a name="text-value"></a><span data-ttu-id="9fdc4-114">文本值</span><span class="sxs-lookup"><span data-stu-id="9fdc4-114">Text value</span></span>

<span data-ttu-id="9fdc4-115">**SortOrder**元素的文本值是排列对话的顺序。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-115">The text value of the **SortOrder** element is the order in which conversations ordered.</span></span> <span data-ttu-id="9fdc4-116">**TreeOrderAscending**的文本值表示按升序顺序对对话进行排序。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-116">A text value of **TreeOrderAscending** indicates that the conversations are ordered according to the conversation tree in ascending order.</span></span> <span data-ttu-id="9fdc4-117">**TreeOrderDescending**的文本值表示按降序顺序对对话进行排序。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-117">A text value of **TreeOrderDescending** indicates that the conversations are ordered according to the conversation tree in descending order.</span></span> <span data-ttu-id="9fdc4-118">**DateOrderAscending**的文本值表示按照按升序排序的会话日期对对话进行排序。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-118">A text value of **DateOrderAscending** indicates that the conversations are ordered according to the conversation date in ascending order.</span></span> <span data-ttu-id="9fdc4-119">**DateOrderDescending**的文本值表示根据会话日期的降序对对话进行排序。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-119">A text value of **DateOrderDescending** indicates that the conversations are ordered according to the conversation date in descending order.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9fdc4-120">备注</span><span class="sxs-lookup"><span data-stu-id="9fdc4-120">Remarks</span></span>

<span data-ttu-id="9fdc4-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9fdc4-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9fdc4-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9fdc4-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9fdc4-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9fdc4-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9fdc4-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9fdc4-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9fdc4-125">Schema name</span></span>  <br/> |<span data-ttu-id="9fdc4-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="9fdc4-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9fdc4-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9fdc4-127">Validation file</span></span>  <br/> |<span data-ttu-id="9fdc4-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9fdc4-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9fdc4-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9fdc4-129">Can be empty</span></span>  <br/> ||
   

