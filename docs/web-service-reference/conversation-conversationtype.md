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
description: 对话元素均表示一个对话。
ms.openlocfilehash: e1ae055d6a77fc5a9b483341830b978e0c1a5b5a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753580"
---
# <a name="conversation-conversationtype"></a><span data-ttu-id="a8bc0-103">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-103">Conversation (ConversationType)</span></span>

<span data-ttu-id="a8bc0-104">**对话**元素均表示一个对话。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-104">The **Conversation** element represents a single conversation.</span></span> 
  
[<span data-ttu-id="a8bc0-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="a8bc0-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="a8bc0-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="a8bc0-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="a8bc0-107">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
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

 <span data-ttu-id="a8bc0-108">**ConversationType**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-108">**ConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8bc0-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a8bc0-109">Attributes and elements</span></span>

<span data-ttu-id="a8bc0-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8bc0-111">属性</span><span class="sxs-lookup"><span data-stu-id="a8bc0-111">Attributes</span></span>

<span data-ttu-id="a8bc0-112">无。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8bc0-113">子元素</span><span class="sxs-lookup"><span data-stu-id="a8bc0-113">Child elements</span></span>

|<span data-ttu-id="a8bc0-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-114">**Element**</span></span>|<span data-ttu-id="a8bc0-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8bc0-116">ConversationId</span><span class="sxs-lookup"><span data-stu-id="a8bc0-116">ConversationId</span></span>](conversationid.md) <br/> |<span data-ttu-id="a8bc0-117">表示对话的标识符。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-117">Represents the identifier of a conversation.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-118">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="a8bc0-118">ConversationTopic</span></span>](conversationtopic.md) <br/> |<span data-ttu-id="a8bc0-119">代表对话主题。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-119">Represents the conversation topic.</span></span> <span data-ttu-id="a8bc0-120">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-120">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-121">UniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="a8bc0-121">UniqueRecipients</span></span>](uniquerecipients.md) <br/> |<span data-ttu-id="a8bc0-122">包含特定文件夹从聚合对话的收件人列表。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-122">Contains the recipient list of a conversation aggregated from a particular folder.</span></span> <span data-ttu-id="a8bc0-123">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-123">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-124">GlobalUniqueRecipients</span><span class="sxs-lookup"><span data-stu-id="a8bc0-124">GlobalUniqueRecipients</span></span>](globaluniquerecipients.md) <br/> |<span data-ttu-id="a8bc0-125">包含跨邮箱聚合对话的收件人列表。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-125">Contains the recipient list of a conversation aggregated across a mailbox.</span></span> <span data-ttu-id="a8bc0-126">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-126">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-127">UniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="a8bc0-127">UniqueUnreadSenders</span></span>](uniqueunreadsenders.md) <br/> |<span data-ttu-id="a8bc0-128">包含所有已发送邮件的当前文件夹中的此对话中当前未读的人员列表。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-128">Contains a list of all the people who have sent messages that are currently unread in this conversation in the current folder.</span></span> <span data-ttu-id="a8bc0-129">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-129">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-130">GlobalUniqueUnreadSenders</span><span class="sxs-lookup"><span data-stu-id="a8bc0-130">GlobalUniqueUnreadSenders</span></span>](globaluniqueunreadsenders.md) <br/> |<span data-ttu-id="a8bc0-131">包含所有已发送邮件的邮箱中的所有文件夹中的当前未读此对话中的人员列表。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-131">Contains a list of all the people who have sent messages that are currently unread in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-132">UniqueSenders</span><span class="sxs-lookup"><span data-stu-id="a8bc0-132">UniqueSenders</span></span>](uniquesenders.md) <br/> |<span data-ttu-id="a8bc0-133">包含当前文件夹中的会话项目的所有发件人的列表。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-133">Contains a list of all the senders of conversation items in the current folder.</span></span> <span data-ttu-id="a8bc0-134">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-134">This element is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-135">GlobalUniqueSenders</span><span class="sxs-lookup"><span data-stu-id="a8bc0-135">GlobalUniqueSenders</span></span>](globaluniquesenders.md) <br/> |<span data-ttu-id="a8bc0-136">包含所有发件人的邮箱中的会话项目的列表。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-136">Contains a list of all the senders of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-137">LastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="a8bc0-137">LastDeliveryTime</span></span>](lastdeliverytime.md) <br/> |<span data-ttu-id="a8bc0-138">包含上次当前文件夹中的此对话中收到的邮件的传递时间。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-138">Contains the delivery time of the message that was last received in this conversation in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-139">GlobalLastDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="a8bc0-139">GlobalLastDeliveryTime</span></span>](globallastdeliverytime.md) <br/> |<span data-ttu-id="a8bc0-140">包含在邮箱中的所有文件夹上次此对话中收到的邮件的传递时间。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-140">Contains the delivery time of the message that was last received in this conversation across all folders in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-141">类别</span><span class="sxs-lookup"><span data-stu-id="a8bc0-141">Categories</span></span>](categories-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a8bc0-142">包含字符串标识应用于当前文件夹中的所有对话项目的类别的集合。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-142">Contains a collection of strings that identify the categories that are applied to all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-143">GlobalCategories</span><span class="sxs-lookup"><span data-stu-id="a8bc0-143">GlobalCategories</span></span>](globalcategories.md) <br/> |<span data-ttu-id="a8bc0-144">包含在邮箱中的所有对话项目类别列表。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-144">Contains the category list for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-145">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="a8bc0-145">FlagStatus</span></span>](flagstatus.md) <br/> |<span data-ttu-id="a8bc0-146">包含当前文件夹中的会话项目的聚合的标志状态。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-146">Contains the aggregated flag status for conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-147">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="a8bc0-147">GlobalFlagStatus</span></span>](globalflagstatus.md) <br/> |<span data-ttu-id="a8bc0-148">包含聚合的标志状态的邮箱中的所有对话项。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-148">Contains the aggregated flag status for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-149">HasAttachments</span><span class="sxs-lookup"><span data-stu-id="a8bc0-149">HasAttachments</span></span>](hasattachments.md) <br/> |<span data-ttu-id="a8bc0-150">包含一个值，指示当前文件夹中的至少一个对话项目是否包含附件。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-150">Contains a value that indicates whether at least one conversation item in the current folder has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-151">GlobalHasAttachments</span><span class="sxs-lookup"><span data-stu-id="a8bc0-151">GlobalHasAttachments</span></span>](globalhasattachments.md) <br/> |<span data-ttu-id="a8bc0-152">包含一个值，指示是否为邮箱中的至少一个对话项目包含附件。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-152">Contains a value that indicates whether at least one conversation item in a mailbox has an attachment.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-153">MessageCount</span><span class="sxs-lookup"><span data-stu-id="a8bc0-153">MessageCount</span></span>](messagecount.md) <br/> |<span data-ttu-id="a8bc0-154">包含当前文件夹中的会话项目的总数。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-154">Contains the total number of conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-155">GlobalMessageCount</span><span class="sxs-lookup"><span data-stu-id="a8bc0-155">GlobalMessageCount</span></span>](globalmessagecount.md) <br/> |<span data-ttu-id="a8bc0-156">包含邮箱中的对话项目的总数。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-156">Contains the total number of conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-157">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="a8bc0-157">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="a8bc0-158">包含文件夹中的未读的对话项目的计数。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-158">Contains the count of unread conversation items within a folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-159">GlobalUnreadCount</span><span class="sxs-lookup"><span data-stu-id="a8bc0-159">GlobalUnreadCount</span></span>](globalunreadcount.md) <br/> |<span data-ttu-id="a8bc0-160">包含邮箱中的所有未读的对话项目的计数。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-160">Contains a count of all the unread conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-161">Size</span><span class="sxs-lookup"><span data-stu-id="a8bc0-161">Size</span></span>](size.md) <br/> |<span data-ttu-id="a8bc0-162">包含来自当前文件夹中的所有对话项目的大小计算出的对话大小。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-162">Contains the conversation size calculated from the size of all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-163">GlobalSize</span><span class="sxs-lookup"><span data-stu-id="a8bc0-163">GlobalSize</span></span>](globalsize.md) <br/> |<span data-ttu-id="a8bc0-164">包含计算从邮箱中的所有对话项目的大小的对话的大小。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-164">Contains the size of the conversation calculated from the size of all conversation items in the mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-165">ItemClasses (ArrayOfItemClassType)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-165">ItemClasses (ArrayOfItemClassType)</span></span>](itemclasses-arrayofitemclasstype.md) <br/> |<span data-ttu-id="a8bc0-166">包含列表项类的值，该值代表当前文件夹中的会话项目的所有项类。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-166">Contains a list of item classes that represents all the item classes of the conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-167">GlobalItemClasses</span><span class="sxs-lookup"><span data-stu-id="a8bc0-167">GlobalItemClasses</span></span>](globalitemclasses.md) <br/> |<span data-ttu-id="a8bc0-168">包含列表项类的值，该值代表的邮箱中的会话项目的所有项类。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-168">Contains a list of item classes that represents all the item classes of the conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-169">Importance</span><span class="sxs-lookup"><span data-stu-id="a8bc0-169">Importance</span></span>](importance.md) <br/> |<span data-ttu-id="a8bc0-170">包含当前文件夹中的所有对话项目的聚合的重要性。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-170">Contains the aggregated importance for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-171">GlobalImportance</span><span class="sxs-lookup"><span data-stu-id="a8bc0-171">GlobalImportance</span></span>](globalimportance.md) <br/> |<span data-ttu-id="a8bc0-172">包含聚合的邮箱中的所有对话项目的重要性。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-172">Contains the aggregated importance for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-173">ItemIds</span><span class="sxs-lookup"><span data-stu-id="a8bc0-173">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="a8bc0-174">包含当前文件夹中的所有对话项目的项标识符的集合。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-174">Contains the collection of item identifiers for all conversation items in the current folder.</span></span>  <br/> |
|[<span data-ttu-id="a8bc0-175">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="a8bc0-175">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="a8bc0-176">包含的项标识符的邮箱中的所有对话项的集合。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-176">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a8bc0-177">父元素</span><span class="sxs-lookup"><span data-stu-id="a8bc0-177">Parent elements</span></span>

|<span data-ttu-id="a8bc0-178">**元素**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-178">**Element**</span></span>|<span data-ttu-id="a8bc0-179">**说明**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-179">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8bc0-180">Conversations</span><span class="sxs-lookup"><span data-stu-id="a8bc0-180">Conversations</span></span>](conversations-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a8bc0-181">包含数组**FindConversation**响应中返回的对话。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-181">Contains an array of conversations that are returned in the **FindConversation** response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a8bc0-182">文本值</span><span class="sxs-lookup"><span data-stu-id="a8bc0-182">Text value</span></span>

<span data-ttu-id="a8bc0-183">无。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-183">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8bc0-184">备注</span><span class="sxs-lookup"><span data-stu-id="a8bc0-184">Remarks</span></span>

<span data-ttu-id="a8bc0-185">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a8bc0-185">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8bc0-186">元素信息</span><span class="sxs-lookup"><span data-stu-id="a8bc0-186">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8bc0-187">命名空间</span><span class="sxs-lookup"><span data-stu-id="a8bc0-187">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8bc0-188">架构名称</span><span class="sxs-lookup"><span data-stu-id="a8bc0-188">Schema name</span></span>  <br/> |<span data-ttu-id="a8bc0-189">类型架构</span><span class="sxs-lookup"><span data-stu-id="a8bc0-189">Types schema</span></span>  <br/> |
|<span data-ttu-id="a8bc0-190">验证文件</span><span class="sxs-lookup"><span data-stu-id="a8bc0-190">Validation file</span></span>  <br/> |<span data-ttu-id="a8bc0-191">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a8bc0-191">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8bc0-192">可以为空</span><span class="sxs-lookup"><span data-stu-id="a8bc0-192">Can be empty</span></span>  <br/> |<span data-ttu-id="a8bc0-193">False</span><span class="sxs-lookup"><span data-stu-id="a8bc0-193">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8bc0-194">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a8bc0-194">See also</span></span>



[<span data-ttu-id="a8bc0-195">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="a8bc0-195">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="a8bc0-196">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="a8bc0-196">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="a8bc0-197">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="a8bc0-197">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

