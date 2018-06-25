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
description: ConversationAction 元素包含要应用于单个会话的单个操作。
ms.openlocfilehash: 45cd6df3aba94062bd5aa0ddf9367e8cf118dc6b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753579"
---
# <a name="conversationaction"></a><span data-ttu-id="f99c9-103">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="f99c9-103">ConversationAction</span></span>

<span data-ttu-id="f99c9-104">**ConversationAction**元素包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="f99c9-104">The **ConversationAction** element contains a single action to be applied to a single conversation.</span></span> 
  
[<span data-ttu-id="f99c9-105">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="f99c9-105">ApplyConversationAction</span></span>](applyconversationaction.md)
  
[<span data-ttu-id="f99c9-106">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="f99c9-106">ConversationActions</span></span>](conversationactions.md)
  
[<span data-ttu-id="f99c9-107">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="f99c9-107">ConversationAction</span></span>](conversationaction.md)
  
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

 <span data-ttu-id="f99c9-108">**ConversationActionType**</span><span class="sxs-lookup"><span data-stu-id="f99c9-108">**ConversationActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f99c9-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f99c9-109">Attributes and elements</span></span>

<span data-ttu-id="f99c9-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f99c9-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f99c9-111">属性</span><span class="sxs-lookup"><span data-stu-id="f99c9-111">Attributes</span></span>

<span data-ttu-id="f99c9-112">无。</span><span class="sxs-lookup"><span data-stu-id="f99c9-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f99c9-113">子元素</span><span class="sxs-lookup"><span data-stu-id="f99c9-113">Child elements</span></span>

|<span data-ttu-id="f99c9-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="f99c9-114">**Element**</span></span>|<span data-ttu-id="f99c9-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="f99c9-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f99c9-116">操作 (ConversationActionTypeType)</span><span class="sxs-lookup"><span data-stu-id="f99c9-116">Action (ConversationActionTypeType)</span></span>](action-conversationactiontypetype.md) <br/> |<span data-ttu-id="f99c9-117">包含要执行对话[ConversationId](conversationid.md)元素所指定的操作。</span><span class="sxs-lookup"><span data-stu-id="f99c9-117">Contains the action to perform on the conversation specified by the [ConversationId](conversationid.md) element.</span></span> <span data-ttu-id="f99c9-118">此元素必须存在。</span><span class="sxs-lookup"><span data-stu-id="f99c9-118">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-119">ConversationId</span><span class="sxs-lookup"><span data-stu-id="f99c9-119">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="f99c9-120">包含将具有指定应用于对话中的项目的[操作 (ConversationActionTypeType)](action-conversationactiontypetype.md)元素的操作的会话的标识符。</span><span class="sxs-lookup"><span data-stu-id="f99c9-120">Contains the identifier of the conversation that will have the action specified by the [Action (ConversationActionTypeType)](action-conversationactiontypetype.md) element applied to items in the conversation.</span></span> <span data-ttu-id="f99c9-121">此元素必须存在。</span><span class="sxs-lookup"><span data-stu-id="f99c9-121">This element must be present.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-122">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="f99c9-122">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="f99c9-123">指示使用文件夹的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="f99c9-123">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="f99c9-124">此元素必须存在时复制、 删除、 移动和目标文件夹中的对话项目上设置只读的状态。</span><span class="sxs-lookup"><span data-stu-id="f99c9-124">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-125">ConversationLastSyncTime</span><span class="sxs-lookup"><span data-stu-id="f99c9-125">ConversationLastSyncTime</span></span>](conversationlastsynctime.md) <br/> |<span data-ttu-id="f99c9-126">包含的日期和对话上次同步的时间。</span><span class="sxs-lookup"><span data-stu-id="f99c9-126">Contains the date and time that a conversation was last synchronized.</span></span> <span data-ttu-id="f99c9-127">此元素必须存在时尝试删除接收到指定的时间过去的对话中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="f99c9-127">This element must be present when trying to delete all items in a conversation that were received up to the specified time.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-128">ProcessRightAway</span><span class="sxs-lookup"><span data-stu-id="f99c9-128">ProcessRightAway</span></span>](processrightaway.md) <br/> |<span data-ttu-id="f99c9-129">指示是否将响应发送只要操作对服务器或是否将响应发送操作完成后启动处理。</span><span class="sxs-lookup"><span data-stu-id="f99c9-129">Indicates whether the response is sent as soon as the action starts processing on the server or whether the response is sent after the action has completed.</span></span> <span data-ttu-id="f99c9-130">此元素必须存在以响应发送异步到请求的操作。</span><span class="sxs-lookup"><span data-stu-id="f99c9-130">This element must be present for the response to be sent asynchronous to the requested action.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-131">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="f99c9-131">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="f99c9-132">指示副本的目标文件夹，并移动操作。</span><span class="sxs-lookup"><span data-stu-id="f99c9-132">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-133">类别</span><span class="sxs-lookup"><span data-stu-id="f99c9-133">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="f99c9-134">包含字符串标识会话中的项目所属的类别的集合。</span><span class="sxs-lookup"><span data-stu-id="f99c9-134">Contains a collection of strings that identify the categories to which items in a conversation belong.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-135">EnableAlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="f99c9-135">EnableAlwaysDelete</span></span>](enablealwaysdelete.md) <br/> |<span data-ttu-id="f99c9-136">指定允许的所有新项目在对话中删除的标志。</span><span class="sxs-lookup"><span data-stu-id="f99c9-136">Specifies a flag that enables deletion for all new items in a conversation.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-137">IsRead</span><span class="sxs-lookup"><span data-stu-id="f99c9-137">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="f99c9-138">指示是否已读取一条消息。</span><span class="sxs-lookup"><span data-stu-id="f99c9-138">Indicates whether a message has been read.</span></span>  <br/> |
|[<span data-ttu-id="f99c9-139">DeleteType</span><span class="sxs-lookup"><span data-stu-id="f99c9-139">DeleteType</span></span>](deletetype.md) <br/> |<span data-ttu-id="f99c9-140">指示如何删除会话中的项目。</span><span class="sxs-lookup"><span data-stu-id="f99c9-140">Indicates how items in a conversation are deleted.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f99c9-141">父元素</span><span class="sxs-lookup"><span data-stu-id="f99c9-141">Parent elements</span></span>

|<span data-ttu-id="f99c9-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="f99c9-142">**Element**</span></span>|<span data-ttu-id="f99c9-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="f99c9-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f99c9-144">ConversationActions</span><span class="sxs-lookup"><span data-stu-id="f99c9-144">ConversationActions</span></span>](conversationactions.md) <br/> |<span data-ttu-id="f99c9-145">包含对话和适用于它们的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="f99c9-145">Contains a collection of conversations and the actions to apply to them.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f99c9-146">文本值</span><span class="sxs-lookup"><span data-stu-id="f99c9-146">Text value</span></span>

<span data-ttu-id="f99c9-147">**ConversationAction 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="f99c9-147">**ConversationAction element text values**</span></span>

|<span data-ttu-id="f99c9-148">**值**</span><span class="sxs-lookup"><span data-stu-id="f99c9-148">**Value**</span></span>|<span data-ttu-id="f99c9-149">**说明**</span><span class="sxs-lookup"><span data-stu-id="f99c9-149">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f99c9-150">AlwaysCategorize</span><span class="sxs-lookup"><span data-stu-id="f99c9-150">AlwaysCategorize</span></span>  <br/> |<span data-ttu-id="f99c9-151">始终对对话进行分类。</span><span class="sxs-lookup"><span data-stu-id="f99c9-151">Always categorize the conversation.</span></span>  <br/> |
|<span data-ttu-id="f99c9-152">AlwaysDelete</span><span class="sxs-lookup"><span data-stu-id="f99c9-152">AlwaysDelete</span></span>  <br/> |<span data-ttu-id="f99c9-153">始终删除对话。</span><span class="sxs-lookup"><span data-stu-id="f99c9-153">Always delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="f99c9-154">AlwaysMove</span><span class="sxs-lookup"><span data-stu-id="f99c9-154">AlwaysMove</span></span>  <br/> |<span data-ttu-id="f99c9-155">总是移动对话。</span><span class="sxs-lookup"><span data-stu-id="f99c9-155">Always move the conversation.</span></span>  <br/> |
|<span data-ttu-id="f99c9-156">Delete</span><span class="sxs-lookup"><span data-stu-id="f99c9-156">Delete</span></span>  <br/> |<span data-ttu-id="f99c9-157">删除对话。</span><span class="sxs-lookup"><span data-stu-id="f99c9-157">Delete the conversation.</span></span>  <br/> |
|<span data-ttu-id="f99c9-158">移动</span><span class="sxs-lookup"><span data-stu-id="f99c9-158">Move</span></span>  <br/> |<span data-ttu-id="f99c9-159">移动对话。</span><span class="sxs-lookup"><span data-stu-id="f99c9-159">Move the conversation.</span></span>  <br/> |
|<span data-ttu-id="f99c9-160">复制</span><span class="sxs-lookup"><span data-stu-id="f99c9-160">Copy</span></span>  <br/> |<span data-ttu-id="f99c9-161">复制对话。</span><span class="sxs-lookup"><span data-stu-id="f99c9-161">Copy the conversation.</span></span>  <br/> |
|<span data-ttu-id="f99c9-162">SetReadState</span><span class="sxs-lookup"><span data-stu-id="f99c9-162">SetReadState</span></span>  <br/> |<span data-ttu-id="f99c9-163">设置读的对话状态。</span><span class="sxs-lookup"><span data-stu-id="f99c9-163">Set the read state of the conversation.</span></span>  <br/> |
|<span data-ttu-id="f99c9-164">SetRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f99c9-164">SetRetentionPolicy</span></span>  <br/> |<span data-ttu-id="f99c9-165">设置对话的保留策略。</span><span class="sxs-lookup"><span data-stu-id="f99c9-165">Set the retention policy for the conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f99c9-166">备注</span><span class="sxs-lookup"><span data-stu-id="f99c9-166">Remarks</span></span>

<span data-ttu-id="f99c9-167">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f99c9-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f99c9-168">元素信息</span><span class="sxs-lookup"><span data-stu-id="f99c9-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f99c9-169">命名空间</span><span class="sxs-lookup"><span data-stu-id="f99c9-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f99c9-170">架构名称</span><span class="sxs-lookup"><span data-stu-id="f99c9-170">Schema Name</span></span>  <br/> |<span data-ttu-id="f99c9-171">类型架构</span><span class="sxs-lookup"><span data-stu-id="f99c9-171">Types schema</span></span>  <br/> |
|<span data-ttu-id="f99c9-172">验证文件</span><span class="sxs-lookup"><span data-stu-id="f99c9-172">Validation File</span></span>  <br/> |<span data-ttu-id="f99c9-173">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f99c9-173">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f99c9-174">可以为空</span><span class="sxs-lookup"><span data-stu-id="f99c9-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="f99c9-175">False</span><span class="sxs-lookup"><span data-stu-id="f99c9-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f99c9-176">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f99c9-176">See also</span></span>



[<span data-ttu-id="f99c9-177">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="f99c9-177">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


- [<span data-ttu-id="f99c9-178">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f99c9-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

