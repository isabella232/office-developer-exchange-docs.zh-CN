---
title: ConversationNode
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b7f7acd3-ed65-441e-9976-8b4ed5f12c0b
description: ConversationNode 元素指定会话中的节点。
ms.openlocfilehash: 074209c1b5669db8dd1ea4ba7f9dea064628afbd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462701"
---
# <a name="conversationnode"></a><span data-ttu-id="acb13-103">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="acb13-103">ConversationNode</span></span>

<span data-ttu-id="acb13-104">**ConversationNode**元素指定会话中的节点。</span><span class="sxs-lookup"><span data-stu-id="acb13-104">The **ConversationNode** element specifies a node in a conversation.</span></span> 
  
```XML
<ConversationNode>
    <InternetMessageId></InternetMessageId>
    <ParentInternetMessageId></ParentInternetMessageId>
    <Items></Items>
</ConversationNode>
```

 <span data-ttu-id="acb13-105">**ConversationNodeType**</span><span class="sxs-lookup"><span data-stu-id="acb13-105">**ConversationNodeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="acb13-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="acb13-106">Attributes and elements</span></span>

<span data-ttu-id="acb13-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="acb13-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acb13-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="acb13-108">Attributes</span></span>

<span data-ttu-id="acb13-109">无。</span><span class="sxs-lookup"><span data-stu-id="acb13-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acb13-110">子元素</span><span class="sxs-lookup"><span data-stu-id="acb13-110">Child elements</span></span>

|<span data-ttu-id="acb13-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="acb13-111">**Element**</span></span>|<span data-ttu-id="acb13-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="acb13-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acb13-113">InternetMessageId</span><span class="sxs-lookup"><span data-stu-id="acb13-113">InternetMessageId</span></span>](internetmessageid.md) <br/> |<span data-ttu-id="acb13-114">表示项目的 Internet 邮件标识符。</span><span class="sxs-lookup"><span data-stu-id="acb13-114">Represents the Internet message identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="acb13-115">ParentInternetMessageId</span><span class="sxs-lookup"><span data-stu-id="acb13-115">ParentInternetMessageId</span></span>](parentinternetmessageid.md) <br/> |<span data-ttu-id="acb13-116">指定父 Internet 邮件的标识符。</span><span class="sxs-lookup"><span data-stu-id="acb13-116">Specifies the identifier of the parent Internet message.</span></span>  <br/> |
|[<span data-ttu-id="acb13-117">ItemIds (NonEmptyArrayOfItemIdsType)</span><span class="sxs-lookup"><span data-stu-id="acb13-117">ItemIds (NonEmptyArrayOfItemIdsType)</span></span>](itemids-nonemptyarrayofitemidstype.md) <br/> |<span data-ttu-id="acb13-118">指定对话节点中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="acb13-118">Specifies all the items in the conversation node.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="acb13-119">父元素</span><span class="sxs-lookup"><span data-stu-id="acb13-119">Parent elements</span></span>

|<span data-ttu-id="acb13-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="acb13-120">**Element**</span></span>|<span data-ttu-id="acb13-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="acb13-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acb13-122">ConversationNodes</span><span class="sxs-lookup"><span data-stu-id="acb13-122">ConversationNodes</span></span>](conversationnodes.md) <br/> |<span data-ttu-id="acb13-123">指定会话节点的集合。</span><span class="sxs-lookup"><span data-stu-id="acb13-123">Specifies a collection of conversation nodes.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acb13-124">备注</span><span class="sxs-lookup"><span data-stu-id="acb13-124">Remarks</span></span>

<span data-ttu-id="acb13-125">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="acb13-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="acb13-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="acb13-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acb13-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="acb13-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acb13-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="acb13-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="acb13-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="acb13-129">Schema Name</span></span>  <br/> |<span data-ttu-id="acb13-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="acb13-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="acb13-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="acb13-131">Validation File</span></span>  <br/> |<span data-ttu-id="acb13-132">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="acb13-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="acb13-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="acb13-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="acb13-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="acb13-134">See also</span></span>



- [<span data-ttu-id="acb13-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="acb13-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

