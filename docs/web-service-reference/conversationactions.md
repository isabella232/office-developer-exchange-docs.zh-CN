---
title: ConversationActions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationActions
api_type:
- schema
ms.assetid: 3d6c663d-4bd9-4eec-b95a-cd683f592672
description: ConversationActions 元素包含对话和适用于它们的操作的集合。
ms.openlocfilehash: 3dff7ff66f758f1cd2eb3cd7b8126294d2799fc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753583"
---
# <a name="conversationactions"></a><span data-ttu-id="9b2f2-103">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="9b2f2-103">ConversationActions</span></span>

<span data-ttu-id="9b2f2-104">**ConversationActions**元素包含对话和适用于它们的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-104">The **ConversationActions** element contains a collection of conversations and the actions to apply to them.</span></span> 
  
[<span data-ttu-id="9b2f2-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="9b2f2-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="9b2f2-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="9b2f2-106">ConversationActions</span></span>](conversationactions.md)
  
```XML
<ConversationActions>
   <ConversationAction/>
</ConversationActions>
```

 <span data-ttu-id="9b2f2-107">**NonEmptyArrayOfApplyConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="9b2f2-107">**NonEmptyArrayOfApplyConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b2f2-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9b2f2-108">Attributes and elements</span></span>

<span data-ttu-id="9b2f2-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b2f2-110">属性</span><span class="sxs-lookup"><span data-stu-id="9b2f2-110">Attributes</span></span>

<span data-ttu-id="9b2f2-111">无。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9b2f2-112">子元素</span><span class="sxs-lookup"><span data-stu-id="9b2f2-112">Child elements</span></span>

|<span data-ttu-id="9b2f2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b2f2-113">**Element**</span></span>|<span data-ttu-id="9b2f2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b2f2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b2f2-115">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="9b2f2-115">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="9b2f2-116">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-116">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b2f2-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9b2f2-117">Parent elements</span></span>

|<span data-ttu-id="9b2f2-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b2f2-118">**Element**</span></span>|<span data-ttu-id="9b2f2-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b2f2-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b2f2-120">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="9b2f2-120">ApplyConversationAction</span></span>](applyconversationaction.md) <br/> |<span data-ttu-id="9b2f2-121">定义要应用于对话中的项目的操作的请求。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-121">Defines a request to apply actions to items in a conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9b2f2-122">文本值</span><span class="sxs-lookup"><span data-stu-id="9b2f2-122">Text value</span></span>

<span data-ttu-id="9b2f2-123">无。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9b2f2-124">备注</span><span class="sxs-lookup"><span data-stu-id="9b2f2-124">Remarks</span></span>

<span data-ttu-id="9b2f2-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9b2f2-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b2f2-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="9b2f2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b2f2-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="9b2f2-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9b2f2-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="9b2f2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="9b2f2-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="9b2f2-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9b2f2-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="9b2f2-130">Validation File</span></span>  <br/> |<span data-ttu-id="9b2f2-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9b2f2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9b2f2-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="9b2f2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b2f2-133">False</span><span class="sxs-lookup"><span data-stu-id="9b2f2-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b2f2-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9b2f2-134">See also</span></span>



[<span data-ttu-id="9b2f2-135">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="9b2f2-135">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)

