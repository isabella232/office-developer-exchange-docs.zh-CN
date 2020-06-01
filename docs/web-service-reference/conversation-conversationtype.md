---
title: 对话 (ConversationType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Conversation
api_type:
- schema
ms.assetid: 59d014cd-5886-49ea-8d36-ba5de7e675de
description: 会话元素表示单个对话。
ms.openlocfilehash: 9969a6cfe1f977b1c24e03771f231f4eb03d1ac6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458934"
---
# <a name="conversation-conversationtype"></a><span data-ttu-id="54cd0-103">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="54cd0-103">Conversation (ConversationType)</span></span>

<span data-ttu-id="54cd0-104">**会话**元素表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="54cd0-104">The **Conversation** element represents a single conversation.</span></span> 
  
[<span data-ttu-id="54cd0-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="54cd0-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="54cd0-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="54cd0-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="54cd0-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="54cd0-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
```XML
<Conversation>
   <ConversationId/>
   <ConversationTopic/>
   <UniqueRecipients/>
   <GlobalUniqueRecipients/>
   <UniqueUnreadSenders/>
   <GlobalUniqueUnreadSenders/>
   <UniqueSenders/>
   <GlobalUniqueSenders/>
   <LastDeliveryTime/>
   <GlobalLastDeliveryTime/>
   <Categories/>
   <GlobalCategories/>
   <FlagStatus/>
   <GlobalFlagStatus/>
   <HasAttachments/>
   <GlobalHasAttachments/>
   <MessageCount/>
   <GlobalMessageCount/>
   <UnreadCount/>
   <GlobalUnreadCount/>
   <Size/>   <GlobalSize/>
   <ItemClasses/>
   <GlobalItemClasses/>
   <Importance/>
   <GlobalImportance/>
   <ItemIds/>
   <GlobalItemIds/>
</Conversation>
```

 <span data-ttu-id="54cd0-108">**ConversationType**</span><span class="sxs-lookup"><span data-stu-id="54cd0-108">**ConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="54cd0-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="54cd0-109">Attributes and elements</span></span>

<span data-ttu-id="54cd0-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="54cd0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54cd0-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="54cd0-111">Attributes</span></span>

<span data-ttu-id="54cd0-112">无。</span><span class="sxs-lookup"><span data-stu-id="54cd0-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54cd0-113">子元素</span><span class="sxs-lookup"><span data-stu-id="54cd0-113">Child elements</span></span>

|<span data-ttu-id="54cd0-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="54cd0-114">**Element**</span></span>|<span data-ttu-id="54cd0-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="54cd0-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54cd0-116">ConversationId</span><span class="sxs-lookup"><span data-stu-id="54cd0-116">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="54cd0-117">表示对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="54cd0-117">Represents the identifier of a conversation.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-118">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="54cd0-118">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="54cd0-119">代表 "对话" 主题。</span><span class="sxs-lookup"><span data-stu-id="54cd0-119">Represents the conversation topic.</span></span> <span data-ttu-id="54cd0-120">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="54cd0-120">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-121">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="54cd0-121">UniqueRecipients</span></span>](uniquerecipients.md) <br/> |<span data-ttu-id="54cd0-122">包含从特定文件夹聚合的对话的收件人列表。</span><span class="sxs-lookup"><span data-stu-id="54cd0-122">Contains the recipient list of a conversation aggregated from a particular folder.</span></span> <span data-ttu-id="54cd0-123">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="54cd0-123">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-124">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="54cd0-124">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md) <br/> |<span data-ttu-id="54cd0-125">包含在邮箱中聚合的对话的收件人列表。</span><span class="sxs-lookup"><span data-stu-id="54cd0-125">Contains the recipient list of a conversation aggregated across a mailbox.</span></span> <span data-ttu-id="54cd0-126">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="54cd0-126">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-127">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="54cd0-127">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md) <br/> |<span data-ttu-id="54cd0-128">包含已发送当前文件夹中此对话中当前未读邮件的所有人员的列表。</span><span class="sxs-lookup"><span data-stu-id="54cd0-128">Contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="54cd0-129">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="54cd0-129">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-130">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="54cd0-130">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md) <br/> |<span data-ttu-id="54cd0-131">包含所有已在此对话中的所有文件夹中发送当前未读邮件的人员的列表。</span><span class="sxs-lookup"><span data-stu-id="54cd0-131">Contains a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-132">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="54cd0-132">UniqueSenders</span></span>](uniquesenders.md) <br/> |<span data-ttu-id="54cd0-133">包含当前文件夹中会话项目的所有发件人的列表。</span><span class="sxs-lookup"><span data-stu-id="54cd0-133">Contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="54cd0-134">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="54cd0-134">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-135">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="54cd0-135">GlobalUniqueSenders</span></span>](globaluniquesenders.md) <br/> |<span data-ttu-id="54cd0-136">包含邮箱中对话项目的所有发件人的列表。</span><span class="sxs-lookup"><span data-stu-id="54cd0-136">Contains a list of all the senders of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-137">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="54cd0-137">LastDeliveryTime</span></span>](lastdeliverytime.md) <br/> |<span data-ttu-id="54cd0-138">包含此对话中的当前文件夹中上次收到的邮件的传递时间。</span><span class="sxs-lookup"><span data-stu-id="54cd0-138">Contains the delivery time of the message that was last received in this conversation in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-139">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="54cd0-139">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md) <br/> |<span data-ttu-id="54cd0-140">包含此对话中的邮件在邮箱中的所有文件夹中最后一次接收的传递时间。</span><span class="sxs-lookup"><span data-stu-id="54cd0-140">Contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-141">类别</span><span class="sxs-lookup"><span data-stu-id="54cd0-141">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="54cd0-142">包含标识应用于当前文件夹中的所有会话项的类别的字符串的集合。</span><span class="sxs-lookup"><span data-stu-id="54cd0-142">Contains a collection of strings that identify the categories that are applied to all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-143">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="54cd0-143">GlobalCategories</span></span>](globalcategories.md) <br/> |<span data-ttu-id="54cd0-144">包含邮箱中所有会话项目的类别列表。</span><span class="sxs-lookup"><span data-stu-id="54cd0-144">Contains the category list for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-145">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="54cd0-145">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="54cd0-146">包含当前文件夹中的会话项目的聚合标志状态。</span><span class="sxs-lookup"><span data-stu-id="54cd0-146">Contains the aggregated flag status for conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-147">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="54cd0-147">GlobalFlagStatus</span></span>](globalflagstatus.md) <br/> |<span data-ttu-id="54cd0-148">包含邮箱中所有会话项目的聚合标志状态。</span><span class="sxs-lookup"><span data-stu-id="54cd0-148">Contains the aggregated flag status for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-149">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="54cd0-149">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="54cd0-150">包含一个值，该值指示当前文件夹中是否至少有一个对话项包含附件。</span><span class="sxs-lookup"><span data-stu-id="54cd0-150">Contains a value that indicates whether at least one conversation item in the current folder has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-151">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="54cd0-151">GlobalHasAttachments</span></span>](globalhasattachments.md) <br/> |<span data-ttu-id="54cd0-152">包含一个值，该值指示邮箱中是否至少有一个对话项目具有附件。</span><span class="sxs-lookup"><span data-stu-id="54cd0-152">Contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-153">MessageCount</span><span class="sxs-lookup"><span data-stu-id="54cd0-153">MessageCount</span></span>](messagecount.md) <br/> |<span data-ttu-id="54cd0-154">包含当前文件夹中的对话项目总数。</span><span class="sxs-lookup"><span data-stu-id="54cd0-154">Contains the total number of conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-155">GlobalMessageCount</span><span class="sxs-lookup"><span data-stu-id="54cd0-155">GlobalMessageCount</span></span>](globalmessagecount.md) <br/> |<span data-ttu-id="54cd0-156">包含邮箱中的对话项目总数。</span><span class="sxs-lookup"><span data-stu-id="54cd0-156">Contains the total number of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="54cd0-157">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="54cd0-158">包含文件夹中未读对话项的计数。</span><span class="sxs-lookup"><span data-stu-id="54cd0-158">Contains the count of unread conversation items within a folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-159">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="54cd0-159">GlobalUnreadCount</span></span>](globalunreadcount.md) <br/> |<span data-ttu-id="54cd0-160">包含邮箱中所有未读对话项的计数。</span><span class="sxs-lookup"><span data-stu-id="54cd0-160">Contains a count of all the unread conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-161">大小</span><span class="sxs-lookup"><span data-stu-id="54cd0-161">Size</span></span>](size.md) <br/> |<span data-ttu-id="54cd0-162">包含从当前文件夹中所有会话项目的大小计算得出的对话大小。</span><span class="sxs-lookup"><span data-stu-id="54cd0-162">Contains the conversation size calculated from the size of all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-163">GlobalSize</span><span class="sxs-lookup"><span data-stu-id="54cd0-163">GlobalSize</span></span>](globalsize.md) <br/> |<span data-ttu-id="54cd0-164">包含从邮箱中所有会话项目的大小计算出的对话的大小。</span><span class="sxs-lookup"><span data-stu-id="54cd0-164">Contains the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-165">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="54cd0-165">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md) <br/> |<span data-ttu-id="54cd0-166">包含项类的列表，这些类表示当前文件夹中的会话项的所有项类。</span><span class="sxs-lookup"><span data-stu-id="54cd0-166">Contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-167">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="54cd0-167">GlobalItemClasses</span></span>](globalitemclasses.md) <br/> |<span data-ttu-id="54cd0-168">包含表示邮箱中会话项目的所有项目类别的项目类别的列表。</span><span class="sxs-lookup"><span data-stu-id="54cd0-168">Contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-169">Importance</span><span class="sxs-lookup"><span data-stu-id="54cd0-169">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="54cd0-170">包含当前文件夹中所有会话项目的合计重要性。</span><span class="sxs-lookup"><span data-stu-id="54cd0-170">Contains the aggregated importance for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-171">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="54cd0-171">GlobalImportance</span></span>](globalimportance.md) <br/> |<span data-ttu-id="54cd0-172">包含邮箱中所有会话项目的合计重要性。</span><span class="sxs-lookup"><span data-stu-id="54cd0-172">Contains the aggregated importance for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-173">ItemIds</span><span class="sxs-lookup"><span data-stu-id="54cd0-173">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="54cd0-174">包含当前文件夹中所有会话项的项标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="54cd0-174">Contains the collection of item identifiers for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="54cd0-175">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="54cd0-175">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="54cd0-176">包含邮箱中所有会话项目的项标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="54cd0-176">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="54cd0-177">父元素</span><span class="sxs-lookup"><span data-stu-id="54cd0-177">Parent elements</span></span>

|<span data-ttu-id="54cd0-178">**元素**</span><span class="sxs-lookup"><span data-stu-id="54cd0-178">**Element**</span></span>|<span data-ttu-id="54cd0-179">**说明**</span><span class="sxs-lookup"><span data-stu-id="54cd0-179">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54cd0-180">对话</span><span class="sxs-lookup"><span data-stu-id="54cd0-180">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="54cd0-181">包含在**FindConversation**响应中返回的一组对话。</span><span class="sxs-lookup"><span data-stu-id="54cd0-181">Contains an array of conversations that are returned in the **FindConversation** response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="54cd0-182">文本值</span><span class="sxs-lookup"><span data-stu-id="54cd0-182">Text value</span></span>

<span data-ttu-id="54cd0-183">无。</span><span class="sxs-lookup"><span data-stu-id="54cd0-183">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54cd0-184">说明</span><span class="sxs-lookup"><span data-stu-id="54cd0-184">Remarks</span></span>

<span data-ttu-id="54cd0-185">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="54cd0-185">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54cd0-186">元素信息</span><span class="sxs-lookup"><span data-stu-id="54cd0-186">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54cd0-187">命名空间</span><span class="sxs-lookup"><span data-stu-id="54cd0-187">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="54cd0-188">架构名称</span><span class="sxs-lookup"><span data-stu-id="54cd0-188">Schema name</span></span>  <br/> |<span data-ttu-id="54cd0-189">类型架构</span><span class="sxs-lookup"><span data-stu-id="54cd0-189">Types schema</span></span>  <br/> |
|<span data-ttu-id="54cd0-190">验证文件</span><span class="sxs-lookup"><span data-stu-id="54cd0-190">Validation file</span></span>  <br/> |<span data-ttu-id="54cd0-191">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="54cd0-191">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="54cd0-192">可以为空</span><span class="sxs-lookup"><span data-stu-id="54cd0-192">Can be empty</span></span>  <br/> |<span data-ttu-id="54cd0-193">False</span><span class="sxs-lookup"><span data-stu-id="54cd0-193">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54cd0-194">另请参阅</span><span class="sxs-lookup"><span data-stu-id="54cd0-194">See also</span></span>



[<span data-ttu-id="54cd0-195">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="54cd0-195">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="54cd0-196">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="54cd0-196">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="54cd0-197">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="54cd0-197">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

