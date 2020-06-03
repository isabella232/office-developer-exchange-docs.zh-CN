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
ms.openlocfilehash: 39ffb97f1004535e2fc70b58f8d56afe129e8ee2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461392"
---
# <a name="conversationnodes"></a><span data-ttu-id="5d718-103">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="5d718-103">ConversationNodes</span></span>

<span data-ttu-id="5d718-104">**ConversationNodes**元素指定会话节点的集合。</span><span class="sxs-lookup"><span data-stu-id="5d718-104">The **ConversationNodes** element specifies a collection of conversation nodes.</span></span> 
  
```XML
<ConversationNodes>
    <ConversationNode></ConversationNode>
</ConversationNodes>
```

 <span data-ttu-id="5d718-105">**ArrayOfConversationNodesType**</span><span class="sxs-lookup"><span data-stu-id="5d718-105">**ArrayOfConversationNodesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d718-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5d718-106">Attributes and elements</span></span>

<span data-ttu-id="5d718-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5d718-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d718-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5d718-108">Attributes</span></span>

<span data-ttu-id="5d718-109">无。</span><span class="sxs-lookup"><span data-stu-id="5d718-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d718-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5d718-110">Child elements</span></span>

|<span data-ttu-id="5d718-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d718-111">**Element**</span></span>|<span data-ttu-id="5d718-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d718-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d718-113">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="5d718-113">ConversationNode</span></span>](conversationnode.md) <br/> |<span data-ttu-id="5d718-114">指定对话中的节点。</span><span class="sxs-lookup"><span data-stu-id="5d718-114">Specifies a node in a conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d718-115">父元素</span><span class="sxs-lookup"><span data-stu-id="5d718-115">Parent elements</span></span>

|<span data-ttu-id="5d718-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d718-116">**Element**</span></span>|<span data-ttu-id="5d718-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d718-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d718-118">对话（ConversationResponseType）</span><span class="sxs-lookup"><span data-stu-id="5d718-118">Conversation (ConversationResponseType)</span></span>](conversation-conversationresponsetype.md) <br/> |<span data-ttu-id="5d718-119">代表**GetConversationItems**响应中返回的单个对话。</span><span class="sxs-lookup"><span data-stu-id="5d718-119">Represents a single conversation returned in a **GetConversationItems** response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d718-120">备注</span><span class="sxs-lookup"><span data-stu-id="5d718-120">Remarks</span></span>

<span data-ttu-id="5d718-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5d718-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5d718-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5d718-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d718-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="5d718-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d718-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="5d718-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d718-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="5d718-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5d718-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="5d718-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="5d718-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="5d718-127">Validation File</span></span>  <br/> |<span data-ttu-id="5d718-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="5d718-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d718-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="5d718-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5d718-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d718-130">See also</span></span>



- [<span data-ttu-id="5d718-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5d718-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

