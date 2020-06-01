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
description: GlobalItemIds 元素包含邮箱中所有会话项目的项标识符的集合。
ms.openlocfilehash: aa656e7f2fb78dafe5bf6013c1f7ad14e2372ba1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459424"
---
# <a name="globalitemids"></a><span data-ttu-id="df8c5-103">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="df8c5-103">GlobalItemIds</span></span>

<span data-ttu-id="df8c5-104">**GlobalItemIds**元素包含邮箱中所有会话项目的项标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="df8c5-104">The **GlobalItemIds** element contains the collection of item identifiers for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="df8c5-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="df8c5-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="df8c5-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="df8c5-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="df8c5-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="df8c5-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="df8c5-108">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="df8c5-108">GlobalItemIds</span></span>](globalitemids.md)
  
```XML
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

 <span data-ttu-id="df8c5-109">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="df8c5-109">**NonEmptyArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df8c5-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="df8c5-110">Attributes and elements</span></span>

<span data-ttu-id="df8c5-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="df8c5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df8c5-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="df8c5-112">Attributes</span></span>

<span data-ttu-id="df8c5-113">无。</span><span class="sxs-lookup"><span data-stu-id="df8c5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df8c5-114">子元素</span><span class="sxs-lookup"><span data-stu-id="df8c5-114">Child elements</span></span>

|<span data-ttu-id="df8c5-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="df8c5-115">**Element**</span></span>|<span data-ttu-id="df8c5-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="df8c5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df8c5-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="df8c5-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="df8c5-118">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="df8c5-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="df8c5-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="df8c5-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="df8c5-120">标识定期项目的单个事件。</span><span class="sxs-lookup"><span data-stu-id="df8c5-120">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="df8c5-121">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="df8c5-121">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="df8c5-122">通过标识一个 "定期" 主项目的 "标识符" 标识该项目。</span><span class="sxs-lookup"><span data-stu-id="df8c5-122">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="df8c5-123">父元素</span><span class="sxs-lookup"><span data-stu-id="df8c5-123">Parent elements</span></span>

|<span data-ttu-id="df8c5-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="df8c5-124">**Element**</span></span>|<span data-ttu-id="df8c5-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="df8c5-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df8c5-126">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="df8c5-126">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="df8c5-127">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="df8c5-127">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="df8c5-128">文本值</span><span class="sxs-lookup"><span data-stu-id="df8c5-128">Text value</span></span>

<span data-ttu-id="df8c5-129">无。</span><span class="sxs-lookup"><span data-stu-id="df8c5-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df8c5-130">说明</span><span class="sxs-lookup"><span data-stu-id="df8c5-130">Remarks</span></span>

<span data-ttu-id="df8c5-131">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="df8c5-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df8c5-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="df8c5-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df8c5-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="df8c5-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="df8c5-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="df8c5-134">Schema name</span></span>  <br/> |<span data-ttu-id="df8c5-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="df8c5-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="df8c5-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="df8c5-136">Validation file</span></span>  <br/> |<span data-ttu-id="df8c5-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="df8c5-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="df8c5-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="df8c5-138">Can be empty</span></span>  <br/> |<span data-ttu-id="df8c5-139">False</span><span class="sxs-lookup"><span data-stu-id="df8c5-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df8c5-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="df8c5-140">See also</span></span>



[<span data-ttu-id="df8c5-141">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="df8c5-141">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="df8c5-142">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="df8c5-142">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="df8c5-143">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="df8c5-143">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

