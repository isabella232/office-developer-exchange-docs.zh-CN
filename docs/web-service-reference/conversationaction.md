---
title: ConversationAction
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationAction
api_type:
- schema
ms.assetid: 9ecea41a-3860-4569-8e9b-284b451fc4e0
description: ConversationAction 元素包含要应用于单个对话的单个操作。
ms.openlocfilehash: cb7d874f787b105d5185749dfaf1e940d2411d89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529250"
---
# <a name="conversationaction"></a><span data-ttu-id="df0f0-103">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="df0f0-103">ConversationAction</span></span>

<span data-ttu-id="df0f0-104">**ConversationAction**元素包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="df0f0-104">The **ConversationAction** element contains a single action to be applied to a single conversation.</span></span> 
  
[<span data-ttu-id="df0f0-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="df0f0-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="df0f0-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="df0f0-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="df0f0-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="df0f0-107">ConversationAction</span></span>](conversationaction.md)
  
```XML
<ConversationAction>
   <Action/>
   <ConversationId/>
   <ContextFolderId/>
   <ConversationLastSyncTime/>
   <ProcessRightAway/>
   <DestinationFolderId/>
   <Categories/>
   <EnableAlwaysDelete/>
   <IsRead/>
   <DeleteType/>
</ConversationAction>
```

 <span data-ttu-id="df0f0-108">**ConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="df0f0-108">**ConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df0f0-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="df0f0-109">Attributes and elements</span></span>

<span data-ttu-id="df0f0-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="df0f0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df0f0-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="df0f0-111">Attributes</span></span>

<span data-ttu-id="df0f0-112">无。</span><span class="sxs-lookup"><span data-stu-id="df0f0-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df0f0-113">子元素</span><span class="sxs-lookup"><span data-stu-id="df0f0-113">Child elements</span></span>

|<span data-ttu-id="df0f0-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="df0f0-114">**Element**</span></span>|<span data-ttu-id="df0f0-115">**描述**</span><span class="sxs-lookup"><span data-stu-id="df0f0-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df0f0-116">Action （ConversationActionTypeType）</span><span class="sxs-lookup"><span data-stu-id="df0f0-116">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md) <br/> |<span data-ttu-id="df0f0-117">包含要对[ConversationId](conversationid.md)元素指定的会话执行的操作。</span><span class="sxs-lookup"><span data-stu-id="df0f0-117">Contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> <span data-ttu-id="df0f0-118">此元素必须存在。</span><span class="sxs-lookup"><span data-stu-id="df0f0-118">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-119">ConversationId</span><span class="sxs-lookup"><span data-stu-id="df0f0-119">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="df0f0-120">包含会话的标识符，该会话将具有应用于对话中项目的[操作（ConversationActionTypeType）](action-conversationactiontypetype.md)元素指定的操作。</span><span class="sxs-lookup"><span data-stu-id="df0f0-120">Contains the identifier of the conversation that will have the action specified by the [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) element applied to items in the conversation.</span></span> <span data-ttu-id="df0f0-121">此元素必须存在。</span><span class="sxs-lookup"><span data-stu-id="df0f0-121">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-122">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="df0f0-122">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="df0f0-123">指示针对使用文件夹的操作的文件夹。</span><span class="sxs-lookup"><span data-stu-id="df0f0-123">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="df0f0-124">在复制、删除、移动和设置目标文件夹中会话项的读取状态时，必须存在此元素。</span><span class="sxs-lookup"><span data-stu-id="df0f0-124">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-125">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="df0f0-125">ConversationLastSyncTime</span></span>](conversationlastsynctime.md) <br/> |<span data-ttu-id="df0f0-126">包含上次同步会话的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="df0f0-126">Contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="df0f0-127">在尝试删除会话中的所有已收到指定时间的项目时，必须存在此元素。</span><span class="sxs-lookup"><span data-stu-id="df0f0-127">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-128">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="df0f0-128">ProcessRightAway</span></span>](processrightaway.md) <br/> |<span data-ttu-id="df0f0-129">指示是否在操作在服务器上开始处理时立即发送响应，或者在操作完成后是否发送响应。</span><span class="sxs-lookup"><span data-stu-id="df0f0-129">Indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="df0f0-130">必须存在此元素，才能将异步向请求的操作发送异步响应。</span><span class="sxs-lookup"><span data-stu-id="df0f0-130">This element must be present for the response to be sent asynchronous to the requested action.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-131">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="df0f0-131">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="df0f0-132">指示复制和移动操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="df0f0-132">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-133">类别</span><span class="sxs-lookup"><span data-stu-id="df0f0-133">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="df0f0-134">包含一个字符串集合，这些字符串标识对话中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="df0f0-134">Contains a collection of strings that identify the categories to which items in a conversation belong.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-135">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="df0f0-135">EnableAlwaysDelete</span></span>](enablealwaysdelete.md) <br/> |<span data-ttu-id="df0f0-136">指定对对话中的所有新项目启用删除的标志。</span><span class="sxs-lookup"><span data-stu-id="df0f0-136">Specifies a flag that enables deletion for all new items in a conversation.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-137">IsRead</span><span class="sxs-lookup"><span data-stu-id="df0f0-137">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="df0f0-138">指示是否已阅读邮件。</span><span class="sxs-lookup"><span data-stu-id="df0f0-138">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="df0f0-139">DeleteType</span><span class="sxs-lookup"><span data-stu-id="df0f0-139">DeleteType</span></span>](deletetype.md) <br/> |<span data-ttu-id="df0f0-140">指示如何删除对话中的项目。</span><span class="sxs-lookup"><span data-stu-id="df0f0-140">Indicates how items in a conversation are deleted.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="df0f0-141">父元素</span><span class="sxs-lookup"><span data-stu-id="df0f0-141">Parent elements</span></span>

|<span data-ttu-id="df0f0-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="df0f0-142">**Element**</span></span>|<span data-ttu-id="df0f0-143">**描述**</span><span class="sxs-lookup"><span data-stu-id="df0f0-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df0f0-144">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="df0f0-144">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="df0f0-145">包含对话的集合以及要应用于它们的操作。</span><span class="sxs-lookup"><span data-stu-id="df0f0-145">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="df0f0-146">文本值</span><span class="sxs-lookup"><span data-stu-id="df0f0-146">Text value</span></span>

<span data-ttu-id="df0f0-147">**ConversationAction 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="df0f0-147">**ConversationAction element text values**</span></span>

|<span data-ttu-id="df0f0-148">**值**</span><span class="sxs-lookup"><span data-stu-id="df0f0-148">**Value**</span></span>|<span data-ttu-id="df0f0-149">**说明**</span><span class="sxs-lookup"><span data-stu-id="df0f0-149">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df0f0-150">AlwaysCategorize</span><span class="sxs-lookup"><span data-stu-id="df0f0-150">AlwaysCategorize</span></span>  <br/> |<span data-ttu-id="df0f0-151">始终对对话进行分类。</span><span class="sxs-lookup"><span data-stu-id="df0f0-151">Always categorize the conversation.</span></span>  <br/> |
|<span data-ttu-id="df0f0-152">AlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="df0f0-152">AlwaysDelete</span></span>  <br/> |<span data-ttu-id="df0f0-153">始终删除对话。</span><span class="sxs-lookup"><span data-stu-id="df0f0-153">Always delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="df0f0-154">AlwaysMove</span><span class="sxs-lookup"><span data-stu-id="df0f0-154">AlwaysMove</span></span>  <br/> |<span data-ttu-id="df0f0-155">始终移动对话。</span><span class="sxs-lookup"><span data-stu-id="df0f0-155">Always move the conversation.</span></span>  <br/> |
|<span data-ttu-id="df0f0-156">Delete</span><span class="sxs-lookup"><span data-stu-id="df0f0-156">Delete</span></span>  <br/> |<span data-ttu-id="df0f0-157">删除对话。</span><span class="sxs-lookup"><span data-stu-id="df0f0-157">Delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="df0f0-158">移动</span><span class="sxs-lookup"><span data-stu-id="df0f0-158">Move</span></span>  <br/> |<span data-ttu-id="df0f0-159">移动对话。</span><span class="sxs-lookup"><span data-stu-id="df0f0-159">Move the conversation.</span></span>  <br/> |
|<span data-ttu-id="df0f0-160">复制</span><span class="sxs-lookup"><span data-stu-id="df0f0-160">Copy</span></span>  <br/> |<span data-ttu-id="df0f0-161">复制对话。</span><span class="sxs-lookup"><span data-stu-id="df0f0-161">Copy the conversation.</span></span>  <br/> |
|<span data-ttu-id="df0f0-162">SetReadState</span><span class="sxs-lookup"><span data-stu-id="df0f0-162">SetReadState</span></span>  <br/> |<span data-ttu-id="df0f0-163">设置对话的读取状态。</span><span class="sxs-lookup"><span data-stu-id="df0f0-163">Set the read state of the conversation.</span></span>  <br/> |
|<span data-ttu-id="df0f0-164">SetRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="df0f0-164">SetRetentionPolicy</span></span>  <br/> |<span data-ttu-id="df0f0-165">设置会话的保留策略。</span><span class="sxs-lookup"><span data-stu-id="df0f0-165">Set the retention policy for the conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df0f0-166">备注</span><span class="sxs-lookup"><span data-stu-id="df0f0-166">Remarks</span></span>

<span data-ttu-id="df0f0-167">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="df0f0-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df0f0-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="df0f0-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df0f0-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="df0f0-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="df0f0-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="df0f0-170">Schema Name</span></span>  <br/> |<span data-ttu-id="df0f0-171">类型架构</span><span class="sxs-lookup"><span data-stu-id="df0f0-171">Types schema</span></span>  <br/> |
|<span data-ttu-id="df0f0-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="df0f0-172">Validation File</span></span>  <br/> |<span data-ttu-id="df0f0-173">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="df0f0-173">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="df0f0-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="df0f0-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="df0f0-175">False</span><span class="sxs-lookup"><span data-stu-id="df0f0-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df0f0-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="df0f0-176">See also</span></span>



[<span data-ttu-id="df0f0-177">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="df0f0-177">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="df0f0-178">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="df0f0-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

