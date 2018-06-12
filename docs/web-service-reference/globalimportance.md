---
title: GlobalImportance
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalImportance
api_type:
- schema
ms.assetid: 8bcec699-e771-4f38-b7d9-61f324af1b4e
description: GlobalImportance 元素包含聚合的邮箱中的所有对话项目的重要性。
ms.openlocfilehash: c9cdcf20fd3e6eca9ab501cbc747544a4d7b7ded
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825731"
---
# <a name="globalimportance"></a><span data-ttu-id="fce00-103">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="fce00-103">GlobalImportance</span></span>

<span data-ttu-id="fce00-104">**GlobalImportance**元素包含聚合的邮箱中的所有对话项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="fce00-104">The **GlobalImportance** element contains the aggregated importance for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="fce00-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="fce00-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="fce00-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="fce00-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="fce00-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="fce00-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="fce00-108">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="fce00-108">GlobalImportance</span></span>](globalimportance.md)
  
```XML
<GlobalImportance> Low | Normal | High </GlobalImportance>
```

 <span data-ttu-id="fce00-109">**ImportanceChoicesType**</span><span class="sxs-lookup"><span data-stu-id="fce00-109">**ImportanceChoicesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fce00-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fce00-110">Attributes and elements</span></span>

<span data-ttu-id="fce00-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fce00-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fce00-112">属性</span><span class="sxs-lookup"><span data-stu-id="fce00-112">Attributes</span></span>

<span data-ttu-id="fce00-113">无。</span><span class="sxs-lookup"><span data-stu-id="fce00-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fce00-114">子元素</span><span class="sxs-lookup"><span data-stu-id="fce00-114">Child elements</span></span>

<span data-ttu-id="fce00-115">无。</span><span class="sxs-lookup"><span data-stu-id="fce00-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fce00-116">父元素</span><span class="sxs-lookup"><span data-stu-id="fce00-116">Parent elements</span></span>

|<span data-ttu-id="fce00-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="fce00-117">**Element**</span></span>|<span data-ttu-id="fce00-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="fce00-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fce00-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="fce00-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="fce00-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="fce00-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fce00-121">文本值</span><span class="sxs-lookup"><span data-stu-id="fce00-121">Text value</span></span>

<span data-ttu-id="fce00-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="fce00-122">A text value is required.</span></span> <span data-ttu-id="fce00-123">此元素的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="fce00-123">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="fce00-124">Low</span><span class="sxs-lookup"><span data-stu-id="fce00-124">Low</span></span>
    
- <span data-ttu-id="fce00-125">常规</span><span class="sxs-lookup"><span data-stu-id="fce00-125">Normal</span></span>
    
- <span data-ttu-id="fce00-126">High</span><span class="sxs-lookup"><span data-stu-id="fce00-126">High</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fce00-127">备注</span><span class="sxs-lookup"><span data-stu-id="fce00-127">Remarks</span></span>

<span data-ttu-id="fce00-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fce00-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fce00-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="fce00-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fce00-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="fce00-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fce00-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="fce00-131">Schema name</span></span>  <br/> |<span data-ttu-id="fce00-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="fce00-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="fce00-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="fce00-133">Validation file</span></span>  <br/> |<span data-ttu-id="fce00-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fce00-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fce00-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="fce00-135">Can be empty</span></span>  <br/> |<span data-ttu-id="fce00-136">False</span><span class="sxs-lookup"><span data-stu-id="fce00-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fce00-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fce00-137">See also</span></span>



[<span data-ttu-id="fce00-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="fce00-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="fce00-139">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="fce00-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="fce00-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="fce00-140">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

