---
title: ConversationNodes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c8a35b8-a940-4b3e-8768-9ba95766fd79
description: ConversationNodes 元素指定会话节点的集合。
ms.openlocfilehash: 62ec061f6d03abb9db7e511722e5570e70d65772
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753598"
---
# <a name="conversationnodes"></a><span data-ttu-id="b0e45-103">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="b0e45-103">ConversationNodes</span></span>

<span data-ttu-id="b0e45-104">**ConversationNodes**元素指定会话节点的集合。</span><span class="sxs-lookup"><span data-stu-id="b0e45-104">The **ConversationNodes** element specifies a collection of conversation nodes.</span></span> 
  
```XML
<ConversationNodes>
    <ConversationNode></ConversationNode>
</ConversationNodes>
```

 <span data-ttu-id="b0e45-105">**ArrayOfConversationNodesType**</span><span class="sxs-lookup"><span data-stu-id="b0e45-105">**ArrayOfConversationNodesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0e45-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b0e45-106">Attributes and elements</span></span>

<span data-ttu-id="b0e45-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b0e45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0e45-108">属性</span><span class="sxs-lookup"><span data-stu-id="b0e45-108">Attributes</span></span>

<span data-ttu-id="b0e45-109">无。</span><span class="sxs-lookup"><span data-stu-id="b0e45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0e45-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b0e45-110">Child elements</span></span>

|<span data-ttu-id="b0e45-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0e45-111">**Element**</span></span>|<span data-ttu-id="b0e45-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0e45-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0e45-113">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="b0e45-113">ConversationNode</span></span>](conversationnode.md) <br/> |<span data-ttu-id="b0e45-114">在对话中指定的节点。</span><span class="sxs-lookup"><span data-stu-id="b0e45-114">Specifies a node in a conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b0e45-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b0e45-115">Parent elements</span></span>

|<span data-ttu-id="b0e45-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0e45-116">**Element**</span></span>|<span data-ttu-id="b0e45-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0e45-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0e45-118">对话 (ConversationResponseType)</span><span class="sxs-lookup"><span data-stu-id="b0e45-118">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="b0e45-119">表示**GetConversationItems**响应中返回单个对话。</span><span class="sxs-lookup"><span data-stu-id="b0e45-119">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0e45-120">备注</span><span class="sxs-lookup"><span data-stu-id="b0e45-120">Remarks</span></span>

<span data-ttu-id="b0e45-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b0e45-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b0e45-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b0e45-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0e45-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="b0e45-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0e45-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="b0e45-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0e45-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="b0e45-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b0e45-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="b0e45-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="b0e45-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="b0e45-127">Validation File</span></span>  <br/> |<span data-ttu-id="b0e45-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0e45-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0e45-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="b0e45-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b0e45-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b0e45-130">See also</span></span>



- [<span data-ttu-id="b0e45-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b0e45-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

