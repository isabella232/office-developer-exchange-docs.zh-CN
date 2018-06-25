---
title: ConversationNode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b7f7acd3-ed65-441e-9976-8b4ed5f12c0b
description: ConversationNode 元素指定在对话中的节点。
ms.openlocfilehash: c8289e5f30bfd25eb12d54e3be0c561786308dc6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753589"
---
# <a name="conversationnode"></a><span data-ttu-id="c8354-103">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="c8354-103">ConversationNode</span></span>

<span data-ttu-id="c8354-104">**ConversationNode**元素指定在对话中的节点。</span><span class="sxs-lookup"><span data-stu-id="c8354-104">The **ConversationNode** element specifies a node in a conversation.</span></span> 
  
```XML
<ConversationNode>
    <InternetMessageId></InternetMessageId>
    <ParentInternetMessageId></ParentInternetMessageId>
    <Items></Items>
</ConversationNode>
```

 <span data-ttu-id="c8354-105">**ConversationNodeType**</span><span class="sxs-lookup"><span data-stu-id="c8354-105">**ConversationNodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8354-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c8354-106">Attributes and elements</span></span>

<span data-ttu-id="c8354-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c8354-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8354-108">属性</span><span class="sxs-lookup"><span data-stu-id="c8354-108">Attributes</span></span>

<span data-ttu-id="c8354-109">无。</span><span class="sxs-lookup"><span data-stu-id="c8354-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8354-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c8354-110">Child elements</span></span>

|<span data-ttu-id="c8354-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c8354-111">**Element**</span></span>|<span data-ttu-id="c8354-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c8354-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8354-113">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="c8354-113">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="c8354-114">表示项目的 Internet 消息标识符。</span><span class="sxs-lookup"><span data-stu-id="c8354-114">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="c8354-115">ParentInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="c8354-115">ParentInternetMessageId</span></span>](parentinternetmessageid.md) <br/> |<span data-ttu-id="c8354-116">指定父 Internet 消息的标识符。</span><span class="sxs-lookup"><span data-stu-id="c8354-116">Specifies the identifier of the parent Internet message.</span></span>  <br/> |
|[<span data-ttu-id="c8354-117">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="c8354-117">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="c8354-118">在对话节点中指定的所有项目。</span><span class="sxs-lookup"><span data-stu-id="c8354-118">Specifies all the items in the conversation node.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8354-119">父元素</span><span class="sxs-lookup"><span data-stu-id="c8354-119">Parent elements</span></span>

|<span data-ttu-id="c8354-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="c8354-120">**Element**</span></span>|<span data-ttu-id="c8354-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="c8354-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8354-122">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="c8354-122">ConversationNodes</span></span>](conversationnodes.md) <br/> |<span data-ttu-id="c8354-123">指定会话节点的集合。</span><span class="sxs-lookup"><span data-stu-id="c8354-123">Specifies a collection of conversation nodes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8354-124">备注</span><span class="sxs-lookup"><span data-stu-id="c8354-124">Remarks</span></span>

<span data-ttu-id="c8354-125">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c8354-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c8354-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c8354-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8354-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="c8354-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8354-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="c8354-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8354-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="c8354-129">Schema Name</span></span>  <br/> |<span data-ttu-id="c8354-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="c8354-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="c8354-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="c8354-131">Validation File</span></span>  <br/> |<span data-ttu-id="c8354-132">types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8354-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8354-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="c8354-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c8354-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c8354-134">See also</span></span>



- [<span data-ttu-id="c8354-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c8354-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

