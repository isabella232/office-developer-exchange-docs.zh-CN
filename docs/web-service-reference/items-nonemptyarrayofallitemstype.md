---
title: 项目（NonEmptyArrayOfAllItemsType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Items
api_type:
- schema
ms.assetid: d61ef1cc-ddfc-480a-9625-7b436cb33ae0
description: Items 元素包含要创建的一组项目。
ms.openlocfilehash: 0f70f1fe4348b5b74cef6be6414618af1e3de260
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459852"
---
# <a name="items-nonemptyarrayofallitemstype"></a><span data-ttu-id="ae9a2-103">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="ae9a2-103">Items (NonEmptyArrayOfAllItemsType)</span></span>

<span data-ttu-id="ae9a2-104">**Items**元素包含要创建的一组项目。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-104">The **Items** element contains a set of items to create.</span></span> 
  
```XML
<Items>
   <Item/>
   <Message/>
   <CalendarItem/>
   <Contact/>
   <DistributionList/>
   <MeetingMessage/>
   <MeetingRequest/>
   <MeetingResponse/>
   <MeetingCancellation/>
   <Task/>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</Items>
```

 <span data-ttu-id="ae9a2-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="ae9a2-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae9a2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae9a2-106">Attributes and elements</span></span>

<span data-ttu-id="ae9a2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae9a2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ae9a2-108">Attributes</span></span>

<span data-ttu-id="ae9a2-109">无。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae9a2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ae9a2-110">Child elements</span></span>

|<span data-ttu-id="ae9a2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae9a2-111">**Element**</span></span>|<span data-ttu-id="ae9a2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae9a2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae9a2-113">项目</span><span class="sxs-lookup"><span data-stu-id="ae9a2-113">Item</span></span>](item.md) <br/> |<span data-ttu-id="ae9a2-114">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-114">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-115">消息</span><span class="sxs-lookup"><span data-stu-id="ae9a2-115">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ae9a2-116">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-116">Represents an Exchange email message.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ae9a2-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-119">Contact</span><span class="sxs-lookup"><span data-stu-id="ae9a2-119">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="ae9a2-120">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-120">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-121">DistributionList</span><span class="sxs-lookup"><span data-stu-id="ae9a2-121">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="ae9a2-122">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-122">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-123">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="ae9a2-123">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="ae9a2-124">表示 Exchange 存储中的会议邮件。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-124">Represents a meeting message in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-125">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ae9a2-125">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ae9a2-126">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-126">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-127">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ae9a2-127">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="ae9a2-128">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-128">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-129">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="ae9a2-129">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="ae9a2-130">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-130">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-131">任务</span><span class="sxs-lookup"><span data-stu-id="ae9a2-131">Task</span></span>](task.md) <br/> |<span data-ttu-id="ae9a2-132">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-132">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-133">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-133">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="ae9a2-134">包含对 Exchange 存储中某个项目的发件人的答复。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-134">Contains a reply to the sender of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-135">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-135">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="ae9a2-136">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-136">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-137">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-137">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="ae9a2-138">包含对发件人和 Exchange 存储中某个项目的所有已标识收件人的答复。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-138">Contains a reply to the sender and all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-139">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-139">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="ae9a2-140">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-140">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-141">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-141">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="ae9a2-142">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-142">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-143">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-143">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="ae9a2-144">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-144">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-145">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-145">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="ae9a2-146">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-146">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-147">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-147">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="ae9a2-148">表示一个 response 对象，该对象用于在收到 MeetingCancellation 邮件时删除会议项目。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-148">Represents a response object that is used to remove a meeting item when a MeetingCancellation message is received.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-149">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-149">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="ae9a2-150">包含对帖子项的答复。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-150">Contains a reply to a post item.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-151">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="ae9a2-151">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="ae9a2-152">用于禁止已读回执。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-152">Used to suppress read receipts.</span></span>  <br/> |
|[<span data-ttu-id="ae9a2-153">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="ae9a2-153">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="ae9a2-154">用于接受允许访问其他用户的 "日历" 或 "联系人" 数据的邀请。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-154">Used to accept an invitation that allows access to another user's calendar or contacts data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae9a2-155">父元素</span><span class="sxs-lookup"><span data-stu-id="ae9a2-155">Parent elements</span></span>

|<span data-ttu-id="ae9a2-156">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae9a2-156">**Element**</span></span>|<span data-ttu-id="ae9a2-157">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae9a2-157">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae9a2-158">CreateItem</span><span class="sxs-lookup"><span data-stu-id="ae9a2-158">CreateItem</span></span>](createitem.md) <br/> |<span data-ttu-id="ae9a2-159">定义在 Exchange 存储中创建项目的请求。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-159">Defines the request to create an item in the Exchange store.</span></span>  <br/> <span data-ttu-id="ae9a2-160">下面是此元素的 XPath 表达式:  `/CreateItem`</span><span class="sxs-lookup"><span data-stu-id="ae9a2-160">The following is the XPath expression to this element:  `/CreateItem`</span></span> <br/> |
|[<span data-ttu-id="ae9a2-161">ConversationNode</span><span class="sxs-lookup"><span data-stu-id="ae9a2-161">ConversationNode</span></span>](conversationnode.md) <br/> |<span data-ttu-id="ae9a2-162">标识对话中的单个节点。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-162">Identifies a single node in a conversation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae9a2-163">说明</span><span class="sxs-lookup"><span data-stu-id="ae9a2-163">Remarks</span></span>

<span data-ttu-id="ae9a2-164">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ae9a2-164">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae9a2-165">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae9a2-165">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae9a2-166">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae9a2-166">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ae9a2-167">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae9a2-167">Schema Name</span></span>  <br/> |<span data-ttu-id="ae9a2-168">消息架构</span><span class="sxs-lookup"><span data-stu-id="ae9a2-168">Message schema</span></span>  <br/> |
|<span data-ttu-id="ae9a2-169">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae9a2-169">Validation File</span></span>  <br/> |<span data-ttu-id="ae9a2-170">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ae9a2-170">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae9a2-171">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae9a2-171">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae9a2-172">False</span><span class="sxs-lookup"><span data-stu-id="ae9a2-172">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae9a2-173">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae9a2-173">See also</span></span>



[<span data-ttu-id="ae9a2-174">CreateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="ae9a2-174">CreateFolder operation</span></span>](createfolder-operation.md)
  
[<span data-ttu-id="ae9a2-175">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="ae9a2-175">CreateItem operation</span></span>](createitem-operation.md)


[<span data-ttu-id="ae9a2-176">Creating Folders (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="ae9a2-176">Creating Folders (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

