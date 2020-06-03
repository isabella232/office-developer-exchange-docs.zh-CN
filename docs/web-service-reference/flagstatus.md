---
title: FlagStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FlagStatus
api_type:
- schema
ms.assetid: d5907ec5-3a60-4d83-bf85-406c54f95eb7
description: FlagStatus 元素包含当前文件夹中的会话项目的聚合标志状态。
ms.openlocfilehash: e65849c4909292c07450f8578fe7a7065c98ab44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466211"
---
# <a name="flagstatus"></a><span data-ttu-id="b62c1-103">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="b62c1-103">FlagStatus</span></span>

<span data-ttu-id="b62c1-104">**FlagStatus**元素包含当前文件夹中的会话项目的聚合标志状态。</span><span class="sxs-lookup"><span data-stu-id="b62c1-104">The **FlagStatus** element contains the aggregated flag status for conversation items in the current folder.</span></span> 
  
[<span data-ttu-id="b62c1-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="b62c1-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="b62c1-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="b62c1-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="b62c1-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="b62c1-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="b62c1-108">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="b62c1-108">FlagStatus</span></span>](flagstatus.md)
  
```XML
<FlagStatus> NotFlagged | Flagged | Complete </FlagStatus>
```

 <span data-ttu-id="b62c1-109">**FlagStatusType**</span><span class="sxs-lookup"><span data-stu-id="b62c1-109">**FlagStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b62c1-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b62c1-110">Attributes and elements</span></span>

<span data-ttu-id="b62c1-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b62c1-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b62c1-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="b62c1-112">Attributes</span></span>

<span data-ttu-id="b62c1-113">无。</span><span class="sxs-lookup"><span data-stu-id="b62c1-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b62c1-114">子元素</span><span class="sxs-lookup"><span data-stu-id="b62c1-114">Child elements</span></span>

<span data-ttu-id="b62c1-115">无。</span><span class="sxs-lookup"><span data-stu-id="b62c1-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b62c1-116">父元素</span><span class="sxs-lookup"><span data-stu-id="b62c1-116">Parent elements</span></span>

|<span data-ttu-id="b62c1-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="b62c1-117">**Element**</span></span>|<span data-ttu-id="b62c1-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="b62c1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b62c1-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="b62c1-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="b62c1-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="b62c1-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b62c1-121">文本值</span><span class="sxs-lookup"><span data-stu-id="b62c1-121">Text value</span></span>

<span data-ttu-id="b62c1-122">**FlagStatus**元素的文本值是当前文件夹中的会话项目的聚合标志状态。</span><span class="sxs-lookup"><span data-stu-id="b62c1-122">The text value of the **FlagStatus** element is the aggregated flag status for conversation items in the current folder.</span></span> <span data-ttu-id="b62c1-123">以下是可能的文本值：</span><span class="sxs-lookup"><span data-stu-id="b62c1-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="b62c1-124">**NotFlagged** -指示未标记的状态。</span><span class="sxs-lookup"><span data-stu-id="b62c1-124">**NotFlagged** - Indicates the not-flagged status.</span></span> 
    
- <span data-ttu-id="b62c1-125">已**标记**-指示已标记的状态。</span><span class="sxs-lookup"><span data-stu-id="b62c1-125">**Flagged** - Indicates the flagged status.</span></span> 
    
- <span data-ttu-id="b62c1-126">**完成**-指示完整的标志状态。</span><span class="sxs-lookup"><span data-stu-id="b62c1-126">**Complete** - Indicates the complete flag status.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b62c1-127">备注</span><span class="sxs-lookup"><span data-stu-id="b62c1-127">Remarks</span></span>

<span data-ttu-id="b62c1-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b62c1-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b62c1-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="b62c1-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b62c1-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="b62c1-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b62c1-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="b62c1-131">Schema name</span></span>  <br/> |<span data-ttu-id="b62c1-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="b62c1-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b62c1-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="b62c1-133">Validation file</span></span>  <br/> |<span data-ttu-id="b62c1-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b62c1-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b62c1-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="b62c1-135">Can be empty</span></span>  <br/> |<span data-ttu-id="b62c1-136">False</span><span class="sxs-lookup"><span data-stu-id="b62c1-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b62c1-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b62c1-137">See also</span></span>



[<span data-ttu-id="b62c1-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="b62c1-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="b62c1-139">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="b62c1-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="b62c1-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="b62c1-140">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

