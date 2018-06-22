---
title: 操作 (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: Action 元素包含要执行对话 ConversationId 元素所指定的操作。
ms.openlocfilehash: b468eeaf0c2509bfa53cbd83f497f0bae20a7f68
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753091"
---
# <a name="action-conversationactiontypetype"></a><span data-ttu-id="34c79-103">操作 (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="34c79-103">Action (ConversationActionTypeType)</span></span>

<span data-ttu-id="34c79-104">**Action**元素包含要执行对话[ConversationId](conversationid.md)元素所指定的操作。</span><span class="sxs-lookup"><span data-stu-id="34c79-104">The **Action** element contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> 
  
- [<span data-ttu-id="34c79-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="34c79-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
- [<span data-ttu-id="34c79-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="34c79-106">ConversationActions</span></span>](conversationactions.md)
  
- [<span data-ttu-id="34c79-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="34c79-107">ConversationAction</span></span>](conversationaction.md)
  
- [<span data-ttu-id="34c79-108">操作 (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="34c79-108">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 <span data-ttu-id="34c79-109">**ConversationActionTypeType**</span><span class="sxs-lookup"><span data-stu-id="34c79-109">**ConversationActionTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="34c79-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="34c79-110">Attributes and elements</span></span>

<span data-ttu-id="34c79-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="34c79-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34c79-112">属性</span><span class="sxs-lookup"><span data-stu-id="34c79-112">Attributes</span></span>

<span data-ttu-id="34c79-113">无。</span><span class="sxs-lookup"><span data-stu-id="34c79-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34c79-114">子元素</span><span class="sxs-lookup"><span data-stu-id="34c79-114">Child elements</span></span>

<span data-ttu-id="34c79-115">无。</span><span class="sxs-lookup"><span data-stu-id="34c79-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="34c79-116">父元素</span><span class="sxs-lookup"><span data-stu-id="34c79-116">Parent elements</span></span>

|<span data-ttu-id="34c79-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="34c79-117">**Element**</span></span>|<span data-ttu-id="34c79-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="34c79-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34c79-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="34c79-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="34c79-120">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="34c79-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="34c79-121">文本值</span><span class="sxs-lookup"><span data-stu-id="34c79-121">Text value</span></span>

<span data-ttu-id="34c79-122">**Action**元素的文本值指示将会话上执行哪些操作。</span><span class="sxs-lookup"><span data-stu-id="34c79-122">The text value of the **Action** element indicates which action will be performed on a conversation.</span></span> <span data-ttu-id="34c79-123">以下是可能的文本值和相应的操作：</span><span class="sxs-lookup"><span data-stu-id="34c79-123">The following are the possible text values and the corresponding actions:</span></span> 
  
- <span data-ttu-id="34c79-124">[Categories](categories-ex15websvcsotherref.md)元素中标识的类别与将自动设置**AlwaysCategorize** -的当前项和会话中的新项目。</span><span class="sxs-lookup"><span data-stu-id="34c79-124">**AlwaysCategorize** - The current items and new items in the conversation will automatically be set with the categories identified in the [Categories](categories-ex15websvcsotherref.md) element.</span></span> 
    
- <span data-ttu-id="34c79-125">将自动删除**AlwaysDelete** -的当前项和会话中的新项目。</span><span class="sxs-lookup"><span data-stu-id="34c79-125">**AlwaysDelete** - The current items and new items in the conversation will automatically be deleted.</span></span> <span data-ttu-id="34c79-126">删除模式设置[DeleteType](deletetype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="34c79-126">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="34c79-127">**AlwaysMove** -的当前项和会话中的新项目将自动移动到[DestinationFolderId](destinationfolderid.md)元素标识的文件夹。</span><span class="sxs-lookup"><span data-stu-id="34c79-127">**AlwaysMove** - The current items and new items in the conversation will automatically be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> 
    
- <span data-ttu-id="34c79-128">**删除**-对话中的当前项将被删除。</span><span class="sxs-lookup"><span data-stu-id="34c79-128">**Delete** - The current items in the conversation will be deleted.</span></span> <span data-ttu-id="34c79-129">对话中的后续项目将不会被删除。</span><span class="sxs-lookup"><span data-stu-id="34c79-129">Subsequent items in the conversation will not be deleted.</span></span> <span data-ttu-id="34c79-130">删除模式设置[DeleteType](deletetype.md)元素。</span><span class="sxs-lookup"><span data-stu-id="34c79-130">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="34c79-131">**移动**-对话中的当前项目将移动到[DestinationFolderId](destinationfolderid.md)元素标识的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="34c79-131">**Move** - The current items in the conversation will be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="34c79-132">对话中的后续项目将不移动。</span><span class="sxs-lookup"><span data-stu-id="34c79-132">Subsequent items in the conversation will not be moved.</span></span> 
    
- <span data-ttu-id="34c79-133">**复制**-对话中的当前项将复制到由[DestinationFolderId](destinationfolderid.md)元素标识的文件夹。</span><span class="sxs-lookup"><span data-stu-id="34c79-133">**Copy** - The current items in the conversation will be copied to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="34c79-134">对话中的后续项目不会复制。</span><span class="sxs-lookup"><span data-stu-id="34c79-134">Subsequent items in the conversation will not be copied.</span></span> 
    
- <span data-ttu-id="34c79-135">**SetReadState** -对话中的当前项将有设置其只读的状态。</span><span class="sxs-lookup"><span data-stu-id="34c79-135">**SetReadState** - The current items in the conversation will have their read state set.</span></span> <span data-ttu-id="34c79-136">由[IsRead](isread.md)元素设置的只读的状态。</span><span class="sxs-lookup"><span data-stu-id="34c79-136">The read state is set by the [IsRead](isread.md) element.</span></span> 
    
- <span data-ttu-id="34c79-137">**标志**的对话中的当前项会设置由[标志](flag.md)元素定义的标志。</span><span class="sxs-lookup"><span data-stu-id="34c79-137">**Flag** - The current items in the conversation will have a flag set as defined by the [Flag](flag.md) element.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="34c79-138">备注</span><span class="sxs-lookup"><span data-stu-id="34c79-138">Remarks</span></span>

<span data-ttu-id="34c79-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="34c79-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34c79-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="34c79-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34c79-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="34c79-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="34c79-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="34c79-142">Schema Name</span></span>  <br/> |<span data-ttu-id="34c79-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="34c79-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="34c79-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="34c79-144">Validation File</span></span>  <br/> |<span data-ttu-id="34c79-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="34c79-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="34c79-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="34c79-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="34c79-147">False</span><span class="sxs-lookup"><span data-stu-id="34c79-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34c79-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="34c79-148">See also</span></span>

- [<span data-ttu-id="34c79-149">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="34c79-149">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="34c79-150">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="34c79-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

