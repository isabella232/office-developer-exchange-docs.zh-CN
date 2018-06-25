---
title: GlobalItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalItemIds
api_type:
- schema
ms.assetid: b0f03ce0-a4c3-47de-9360-a880a3606e42
description: GlobalItemIds 元素包含项标识符的邮箱中的所有对话项的集合。
ms.openlocfilehash: 064ebc4c612aaf569eafa56e57a27cf7153f2130
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825737"
---
# <a name="globalitemids"></a><span data-ttu-id="cda38-103">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="cda38-103">GlobalItemIds</span></span>

<span data-ttu-id="cda38-104">**GlobalItemIds**元素包含项标识符的邮箱中的所有对话项的集合。</span><span class="sxs-lookup"><span data-stu-id="cda38-104">The **GlobalItemIds** element contains the collection of item identifiers for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="cda38-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="cda38-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="cda38-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="cda38-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="cda38-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="cda38-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="cda38-108">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="cda38-108">GlobalItemIds</span></span>](globalitemids.md)
  
```XML
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

 <span data-ttu-id="cda38-109">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="cda38-109">**NonEmptyArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cda38-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cda38-110">Attributes and elements</span></span>

<span data-ttu-id="cda38-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cda38-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cda38-112">属性</span><span class="sxs-lookup"><span data-stu-id="cda38-112">Attributes</span></span>

<span data-ttu-id="cda38-113">无。</span><span class="sxs-lookup"><span data-stu-id="cda38-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cda38-114">子元素</span><span class="sxs-lookup"><span data-stu-id="cda38-114">Child elements</span></span>

|<span data-ttu-id="cda38-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="cda38-115">**Element**</span></span>|<span data-ttu-id="cda38-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="cda38-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cda38-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="cda38-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="cda38-118">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="cda38-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="cda38-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="cda38-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="cda38-120">标识定期项目的一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="cda38-120">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="cda38-121">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="cda38-121">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="cda38-122">标识通过其相关的匹配项的标识符之一确定定期主项目。</span><span class="sxs-lookup"><span data-stu-id="cda38-122">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cda38-123">父元素</span><span class="sxs-lookup"><span data-stu-id="cda38-123">Parent elements</span></span>

|<span data-ttu-id="cda38-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="cda38-124">**Element**</span></span>|<span data-ttu-id="cda38-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="cda38-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cda38-126">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="cda38-126">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="cda38-127">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="cda38-127">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cda38-128">文本值</span><span class="sxs-lookup"><span data-stu-id="cda38-128">Text value</span></span>

<span data-ttu-id="cda38-129">无。</span><span class="sxs-lookup"><span data-stu-id="cda38-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cda38-130">备注</span><span class="sxs-lookup"><span data-stu-id="cda38-130">Remarks</span></span>

<span data-ttu-id="cda38-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cda38-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cda38-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="cda38-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cda38-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="cda38-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cda38-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="cda38-134">Schema name</span></span>  <br/> |<span data-ttu-id="cda38-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="cda38-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="cda38-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="cda38-136">Validation file</span></span>  <br/> |<span data-ttu-id="cda38-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cda38-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cda38-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="cda38-138">Can be empty</span></span>  <br/> |<span data-ttu-id="cda38-139">False</span><span class="sxs-lookup"><span data-stu-id="cda38-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cda38-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cda38-140">See also</span></span>



[<span data-ttu-id="cda38-141">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="cda38-141">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="cda38-142">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="cda38-142">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="cda38-143">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="cda38-143">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

