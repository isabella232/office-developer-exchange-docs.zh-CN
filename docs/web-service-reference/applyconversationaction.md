---
title: ApplyConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ApplyConversationAction
api_type:
- schema
ms.assetid: e0ee8f30-529b-4d87-8bc0-b6616e75fb6b
description: ApplyConversationAction 元素定义要应用于对话中的项目的操作的请求。
ms.openlocfilehash: 1b672c6e6d2f60e50215417be7100e9cd77e2a58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753239"
---
# <a name="applyconversationaction"></a><span data-ttu-id="a6fa4-103">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="a6fa4-103">ApplyConversationAction</span></span>

<span data-ttu-id="a6fa4-104">**ApplyConversationAction**元素定义要应用于对话中的项目的操作的请求。</span><span class="sxs-lookup"><span data-stu-id="a6fa4-104">The **ApplyConversationAction** element defines a request to apply actions to items in a conversation.</span></span> 
  
[<span data-ttu-id="a6fa4-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="a6fa4-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
```XML
<ApplyConversationAction>
   <ConversationActions/>
</ApplyConversationAction>
```

 <span data-ttu-id="a6fa4-106">**ApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="a6fa4-106">**ApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6fa4-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a6fa4-107">Attributes and elements</span></span>

<span data-ttu-id="a6fa4-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a6fa4-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6fa4-109">属性</span><span class="sxs-lookup"><span data-stu-id="a6fa4-109">Attributes</span></span>

<span data-ttu-id="a6fa4-110">无。</span><span class="sxs-lookup"><span data-stu-id="a6fa4-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6fa4-111">子元素</span><span class="sxs-lookup"><span data-stu-id="a6fa4-111">Child elements</span></span>

|<span data-ttu-id="a6fa4-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="a6fa4-112">**Element**</span></span>|<span data-ttu-id="a6fa4-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="a6fa4-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6fa4-114">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="a6fa4-114">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="a6fa4-115">包含对话和适用于它们的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="a6fa4-115">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a6fa4-116">父元素</span><span class="sxs-lookup"><span data-stu-id="a6fa4-116">Parent elements</span></span>

<span data-ttu-id="a6fa4-117">无。</span><span class="sxs-lookup"><span data-stu-id="a6fa4-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="a6fa4-118">文本值</span><span class="sxs-lookup"><span data-stu-id="a6fa4-118">Text value</span></span>

<span data-ttu-id="a6fa4-119">无。</span><span class="sxs-lookup"><span data-stu-id="a6fa4-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6fa4-120">备注</span><span class="sxs-lookup"><span data-stu-id="a6fa4-120">Remarks</span></span>

<span data-ttu-id="a6fa4-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a6fa4-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6fa4-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="a6fa4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6fa4-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="a6fa4-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a6fa4-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="a6fa4-124">Schema Name</span></span>  <br/> |<span data-ttu-id="a6fa4-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="a6fa4-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a6fa4-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="a6fa4-126">Validation File</span></span>  <br/> |<span data-ttu-id="a6fa4-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a6fa4-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a6fa4-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="a6fa4-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6fa4-129">False</span><span class="sxs-lookup"><span data-stu-id="a6fa4-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6fa4-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6fa4-130">See also</span></span>

- [<span data-ttu-id="a6fa4-131">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="a6fa4-131">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="a6fa4-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a6fa4-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

