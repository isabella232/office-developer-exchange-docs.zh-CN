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
description: GlobalImportance 元素包含邮箱中所有会话项目的合计重要性。
ms.openlocfilehash: c760168afa3edac20ca0ae7bc677610d8456d178
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459445"
---
# <a name="globalimportance"></a><span data-ttu-id="77df8-103">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="77df8-103">GlobalImportance</span></span>

<span data-ttu-id="77df8-104">**GlobalImportance**元素包含邮箱中所有会话项目的合计重要性。</span><span class="sxs-lookup"><span data-stu-id="77df8-104">The **GlobalImportance** element contains the aggregated importance for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="77df8-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="77df8-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="77df8-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="77df8-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="77df8-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="77df8-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="77df8-108">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="77df8-108">GlobalImportance</span></span>](globalimportance.md)
  
```XML
<GlobalImportance> Low | Normal | High </GlobalImportance>
```

 <span data-ttu-id="77df8-109">**ImportanceChoicesType**</span><span class="sxs-lookup"><span data-stu-id="77df8-109">**ImportanceChoicesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="77df8-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="77df8-110">Attributes and elements</span></span>

<span data-ttu-id="77df8-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="77df8-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77df8-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="77df8-112">Attributes</span></span>

<span data-ttu-id="77df8-113">无。</span><span class="sxs-lookup"><span data-stu-id="77df8-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="77df8-114">子元素</span><span class="sxs-lookup"><span data-stu-id="77df8-114">Child elements</span></span>

<span data-ttu-id="77df8-115">无。</span><span class="sxs-lookup"><span data-stu-id="77df8-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="77df8-116">父元素</span><span class="sxs-lookup"><span data-stu-id="77df8-116">Parent elements</span></span>

|<span data-ttu-id="77df8-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="77df8-117">**Element**</span></span>|<span data-ttu-id="77df8-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="77df8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77df8-119">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="77df8-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="77df8-120">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="77df8-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="77df8-121">文本值</span><span class="sxs-lookup"><span data-stu-id="77df8-121">Text value</span></span>

<span data-ttu-id="77df8-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="77df8-122">A text value is required.</span></span> <span data-ttu-id="77df8-123">以下是此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="77df8-123">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="77df8-124">低</span><span class="sxs-lookup"><span data-stu-id="77df8-124">Low</span></span>
    
- <span data-ttu-id="77df8-125">一般</span><span class="sxs-lookup"><span data-stu-id="77df8-125">Normal</span></span>
    
- <span data-ttu-id="77df8-126">高</span><span class="sxs-lookup"><span data-stu-id="77df8-126">High</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77df8-127">备注</span><span class="sxs-lookup"><span data-stu-id="77df8-127">Remarks</span></span>

<span data-ttu-id="77df8-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="77df8-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="77df8-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="77df8-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77df8-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="77df8-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="77df8-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="77df8-131">Schema name</span></span>  <br/> |<span data-ttu-id="77df8-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="77df8-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="77df8-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="77df8-133">Validation file</span></span>  <br/> |<span data-ttu-id="77df8-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="77df8-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="77df8-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="77df8-135">Can be empty</span></span>  <br/> |<span data-ttu-id="77df8-136">False</span><span class="sxs-lookup"><span data-stu-id="77df8-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77df8-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="77df8-137">See also</span></span>



[<span data-ttu-id="77df8-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="77df8-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="77df8-139">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="77df8-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="77df8-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="77df8-140">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

