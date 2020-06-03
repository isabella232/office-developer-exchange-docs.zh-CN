---
title: Action （ConversationActionTypeType）
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
description: Action 元素包含要对 ConversationId 元素指定的会话执行的操作。
ms.openlocfilehash: f97b04b98cdc29bee9aff5fa1fc6f37400b8314c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527542"
---
# <a name="action-conversationactiontypetype"></a><span data-ttu-id="49bf7-103">Action （ConversationActionTypeType）</span><span class="sxs-lookup"><span data-stu-id="49bf7-103">Action (ConversationActionTypeType)</span></span>

<span data-ttu-id="49bf7-104">**Action**元素包含要对[ConversationId](conversationid.md)元素指定的会话执行的操作。</span><span class="sxs-lookup"><span data-stu-id="49bf7-104">The **Action** element contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> 
  
- [<span data-ttu-id="49bf7-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="49bf7-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
- [<span data-ttu-id="49bf7-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="49bf7-106">ConversationActions</span></span>](conversationactions.md)
  
- [<span data-ttu-id="49bf7-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="49bf7-107">ConversationAction</span></span>](conversationaction.md)
  
- [<span data-ttu-id="49bf7-108">Action （ConversationActionTypeType）</span><span class="sxs-lookup"><span data-stu-id="49bf7-108">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 <span data-ttu-id="49bf7-109">**ConversationActionTypeType**</span><span class="sxs-lookup"><span data-stu-id="49bf7-109">**ConversationActionTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49bf7-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="49bf7-110">Attributes and elements</span></span>

<span data-ttu-id="49bf7-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="49bf7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49bf7-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="49bf7-112">Attributes</span></span>

<span data-ttu-id="49bf7-113">无。</span><span class="sxs-lookup"><span data-stu-id="49bf7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49bf7-114">子元素</span><span class="sxs-lookup"><span data-stu-id="49bf7-114">Child elements</span></span>

<span data-ttu-id="49bf7-115">无。</span><span class="sxs-lookup"><span data-stu-id="49bf7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="49bf7-116">父元素</span><span class="sxs-lookup"><span data-stu-id="49bf7-116">Parent elements</span></span>

|<span data-ttu-id="49bf7-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="49bf7-117">**Element**</span></span>|<span data-ttu-id="49bf7-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="49bf7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49bf7-119">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="49bf7-119">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="49bf7-120">包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="49bf7-120">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="49bf7-121">文本值</span><span class="sxs-lookup"><span data-stu-id="49bf7-121">Text value</span></span>

<span data-ttu-id="49bf7-122">**Action**元素的文本值指示将对对话执行的操作。</span><span class="sxs-lookup"><span data-stu-id="49bf7-122">The text value of the **Action** element indicates which action will be performed on a conversation.</span></span> <span data-ttu-id="49bf7-123">以下是可能的文本值和相应的操作：</span><span class="sxs-lookup"><span data-stu-id="49bf7-123">The following are the possible text values and the corresponding actions:</span></span> 
  
- <span data-ttu-id="49bf7-124">**AlwaysCategorize** -将自动使用在 "[类别](categories-ex15websvcsotherref.md)" 元素中标识的类别设置对话中的当前项目和新项目。</span><span class="sxs-lookup"><span data-stu-id="49bf7-124">**AlwaysCategorize** - The current items and new items in the conversation will automatically be set with the categories identified in the [Categories](categories-ex15websvcsotherref.md) element.</span></span> 
    
- <span data-ttu-id="49bf7-125">**AlwaysDelete** -将自动删除对话中的当前项目和新项目。</span><span class="sxs-lookup"><span data-stu-id="49bf7-125">**AlwaysDelete** - The current items and new items in the conversation will automatically be deleted.</span></span> <span data-ttu-id="49bf7-126">删除模式由[DeleteType](deletetype.md)元素设置。</span><span class="sxs-lookup"><span data-stu-id="49bf7-126">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="49bf7-127">**AlwaysMove** -将自动将对话中的当前项目和新项目移至[DestinationFolderId](destinationfolderid.md)元素所标识的文件夹。</span><span class="sxs-lookup"><span data-stu-id="49bf7-127">**AlwaysMove** - The current items and new items in the conversation will automatically be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> 
    
- <span data-ttu-id="49bf7-128">**删除**-对话中的当前项目将被删除。</span><span class="sxs-lookup"><span data-stu-id="49bf7-128">**Delete** - The current items in the conversation will be deleted.</span></span> <span data-ttu-id="49bf7-129">会话中的后续项目不会被删除。</span><span class="sxs-lookup"><span data-stu-id="49bf7-129">Subsequent items in the conversation will not be deleted.</span></span> <span data-ttu-id="49bf7-130">删除模式由[DeleteType](deletetype.md)元素设置。</span><span class="sxs-lookup"><span data-stu-id="49bf7-130">The deletion mode is set by the [DeleteType](deletetype.md) element.</span></span> 
    
- <span data-ttu-id="49bf7-131">**Move** -对话中的当前项目将被移动到由[DestinationFolderId](destinationfolderid.md)元素标识的文件夹。</span><span class="sxs-lookup"><span data-stu-id="49bf7-131">**Move** - The current items in the conversation will be moved to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="49bf7-132">会话中的后续项目将不会移动。</span><span class="sxs-lookup"><span data-stu-id="49bf7-132">Subsequent items in the conversation will not be moved.</span></span> 
    
- <span data-ttu-id="49bf7-133">**复制**-将对话中的当前项目复制到由[DestinationFolderId](destinationfolderid.md)元素标识的文件夹。</span><span class="sxs-lookup"><span data-stu-id="49bf7-133">**Copy** - The current items in the conversation will be copied to the folder identified by the [DestinationFolderId](destinationfolderid.md) element.</span></span> <span data-ttu-id="49bf7-134">会话中的后续项目不会被复制。</span><span class="sxs-lookup"><span data-stu-id="49bf7-134">Subsequent items in the conversation will not be copied.</span></span> 
    
- <span data-ttu-id="49bf7-135">**SetReadState** -对话中的当前项目将设置为其读取状态。</span><span class="sxs-lookup"><span data-stu-id="49bf7-135">**SetReadState** - The current items in the conversation will have their read state set.</span></span> <span data-ttu-id="49bf7-136">读取状态由[IsRead](isread.md)元素设置。</span><span class="sxs-lookup"><span data-stu-id="49bf7-136">The read state is set by the [IsRead](isread.md) element.</span></span> 
    
- <span data-ttu-id="49bf7-137">**标记**-对话中的当前项目的[标志元素所](flag.md)定义的标志。</span><span class="sxs-lookup"><span data-stu-id="49bf7-137">**Flag** - The current items in the conversation will have a flag set as defined by the [Flag](flag.md) element.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="49bf7-138">备注</span><span class="sxs-lookup"><span data-stu-id="49bf7-138">Remarks</span></span>

<span data-ttu-id="49bf7-139">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="49bf7-139">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49bf7-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="49bf7-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49bf7-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="49bf7-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49bf7-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="49bf7-142">Schema Name</span></span>  <br/> |<span data-ttu-id="49bf7-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="49bf7-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="49bf7-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="49bf7-144">Validation File</span></span>  <br/> |<span data-ttu-id="49bf7-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="49bf7-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49bf7-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="49bf7-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="49bf7-147">False</span><span class="sxs-lookup"><span data-stu-id="49bf7-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49bf7-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="49bf7-148">See also</span></span>

- [<span data-ttu-id="49bf7-149">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="49bf7-149">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)
- [<span data-ttu-id="49bf7-150">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="49bf7-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

