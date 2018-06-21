---
title: GlobalFlagStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalFlagStatus
api_type:
- schema
ms.assetid: 3ba300f3-3355-4cab-9e77-0dcc2902e712
description: GlobalFlagStatus 元素包含聚合的标志状态的邮箱中的所有对话项。
ms.openlocfilehash: 0c560c065463b8b619f96ecef73d1120b216ca35
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2018
ms.locfileid: "19825713"
---
# <a name="globalflagstatus"></a><span data-ttu-id="61c92-103">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="61c92-103">GlobalFlagStatus</span></span>

<span data-ttu-id="61c92-104">**GlobalFlagStatus**元素包含聚合的标志状态的邮箱中的所有对话项。</span><span class="sxs-lookup"><span data-stu-id="61c92-104">The **GlobalFlagStatus** element contains the aggregated flag status for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="61c92-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="61c92-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="61c92-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="61c92-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="61c92-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="61c92-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="61c92-108">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="61c92-108">GlobalFlagStatus</span></span>](globalflagstatus.md)
  
```XML
<GlobalFlagStatus> NotFlagged | Flagged | Complete </GlobalFlagStatus>
```

 <span data-ttu-id="61c92-109">**FlagStatusType**</span><span class="sxs-lookup"><span data-stu-id="61c92-109">**FlagStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61c92-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="61c92-110">Attributes and elements</span></span>

<span data-ttu-id="61c92-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="61c92-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61c92-112">属性</span><span class="sxs-lookup"><span data-stu-id="61c92-112">Attributes</span></span>

<span data-ttu-id="61c92-113">无。</span><span class="sxs-lookup"><span data-stu-id="61c92-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61c92-114">子元素</span><span class="sxs-lookup"><span data-stu-id="61c92-114">Child elements</span></span>

<span data-ttu-id="61c92-115">无。</span><span class="sxs-lookup"><span data-stu-id="61c92-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="61c92-116">父元素</span><span class="sxs-lookup"><span data-stu-id="61c92-116">Parent elements</span></span>

|<span data-ttu-id="61c92-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="61c92-117">**Element**</span></span>|<span data-ttu-id="61c92-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="61c92-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61c92-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="61c92-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="61c92-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="61c92-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="61c92-121">文本值</span><span class="sxs-lookup"><span data-stu-id="61c92-121">Text value</span></span>

<span data-ttu-id="61c92-122">**GlobalFlagStatus**元素的文本值是当前文件夹中的会话项目的聚合的标志状态。</span><span class="sxs-lookup"><span data-stu-id="61c92-122">The text value of the **GlobalFlagStatus** element is the aggregated flag status for conversation items in the current folder.</span></span> <span data-ttu-id="61c92-123">以下是可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="61c92-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="61c92-124">**NotFlagged** -指示不标记状态。</span><span class="sxs-lookup"><span data-stu-id="61c92-124">**NotFlagged** - Indicates the not-flagged status.</span></span> 
    
- <span data-ttu-id="61c92-125">已**完成 2 已标记**的指示已标记的状态。</span><span class="sxs-lookup"><span data-stu-id="61c92-125">**Flagged** - Indicates the flagged status.</span></span> 
    
- <span data-ttu-id="61c92-126">**完整**-指示完成标记状态。</span><span class="sxs-lookup"><span data-stu-id="61c92-126">**Complete** - Indicates the complete flag status.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="61c92-127">备注</span><span class="sxs-lookup"><span data-stu-id="61c92-127">Remarks</span></span>

<span data-ttu-id="61c92-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="61c92-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61c92-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="61c92-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61c92-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="61c92-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="61c92-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="61c92-131">Schema name</span></span>  <br/> |<span data-ttu-id="61c92-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="61c92-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="61c92-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="61c92-133">Validation file</span></span>  <br/> |<span data-ttu-id="61c92-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="61c92-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="61c92-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="61c92-135">Can be empty</span></span>  <br/> |<span data-ttu-id="61c92-136">False</span><span class="sxs-lookup"><span data-stu-id="61c92-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61c92-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="61c92-137">See also</span></span>



[<span data-ttu-id="61c92-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="61c92-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="61c92-139">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="61c92-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="61c92-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="61c92-140">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

