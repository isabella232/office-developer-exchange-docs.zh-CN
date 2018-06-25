---
title: CreateItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateItem
api_type:
- schema
ms.assetid: 78a52120-f1d0-4ed7-8748-436e554f75b6
description: CreateItem operation，在 Exchange 存储中创建项目。
ms.openlocfilehash: 7e1808c685cdbaa1e8867aa7425b2cc52218d001
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753665"
---
# <a name="createitem-operation"></a><span data-ttu-id="946f9-103">CreateItem Operation</span><span class="sxs-lookup"><span data-stu-id="946f9-103">CreateItem operation</span></span>

<span data-ttu-id="946f9-104">CreateItem operation，在 Exchange 存储中创建项目。</span><span class="sxs-lookup"><span data-stu-id="946f9-104">The CreateItem operation creates items in the Exchange store.</span></span>
  
## <a name="using-the-createitem-operation"></a><span data-ttu-id="946f9-105">使用 CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="946f9-105">Using the CreateItem Operation</span></span>

<span data-ttu-id="946f9-106">您可以使用 CreateItem 操作创建以下：</span><span class="sxs-lookup"><span data-stu-id="946f9-106">You can use the CreateItem operation to create the following:</span></span>
  
- <span data-ttu-id="946f9-107">日历项目</span><span class="sxs-lookup"><span data-stu-id="946f9-107">Calendar items</span></span>
    
- <span data-ttu-id="946f9-108">电子邮件</span><span class="sxs-lookup"><span data-stu-id="946f9-108">E-mail messages</span></span>
    
- <span data-ttu-id="946f9-109">会议要求</span><span class="sxs-lookup"><span data-stu-id="946f9-109">Meeting requests</span></span>
    
- <span data-ttu-id="946f9-110">任务</span><span class="sxs-lookup"><span data-stu-id="946f9-110">Tasks</span></span>
    
- <span data-ttu-id="946f9-111">联系人</span><span class="sxs-lookup"><span data-stu-id="946f9-111">Contacts</span></span>
    
<span data-ttu-id="946f9-112">有关详细信息，请参阅[CreateItem operation，（日历项）](createitem-operation-calendar-item.md)、 [CreateItem operation，（电子邮件）](createitem-operation-email-message.md)、 [CreateItem operation，（会议请求）](createitem-operation-meeting-request.md)、 [CreateItem operation，（任务）](createitem-operation-task.md)和[CreateItem operation，（联系人）](createitem-operation-contact.md).</span><span class="sxs-lookup"><span data-stu-id="946f9-112">For more information, see [CreateItem operation (calendar item)](createitem-operation-calendar-item.md), [CreateItem operation (email message)](createitem-operation-email-message.md), [CreateItem operation (meeting request)](createitem-operation-meeting-request.md), [CreateItem operation (task)](createitem-operation-task.md), and [CreateItem operation (contact)](createitem-operation-contact.md).</span></span>
  
<span data-ttu-id="946f9-113">CreateItem operation 支持响应对象的使用。</span><span class="sxs-lookup"><span data-stu-id="946f9-113">The CreateItem operation supports the use of response objects.</span></span> <span data-ttu-id="946f9-114">响应对象才支持可接受和拒绝会议和处理的标准电子邮件中包含的投票按钮。</span><span class="sxs-lookup"><span data-stu-id="946f9-114">Response objects support the acceptance and rejection of meetings and the handling of voting buttons that are included in a standard e-mail message.</span></span> <span data-ttu-id="946f9-115">下表列出 CreateItem 操作中处理的响应对象。</span><span class="sxs-lookup"><span data-stu-id="946f9-115">The following table lists the response objects that are handled in the CreateItem operation.</span></span>
  
|<span data-ttu-id="946f9-116">**响应对象**</span><span class="sxs-lookup"><span data-stu-id="946f9-116">**Response object**</span></span>|<span data-ttu-id="946f9-117">**Action**</span><span class="sxs-lookup"><span data-stu-id="946f9-117">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="946f9-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="946f9-118">AcceptItem</span></span>  <br/> |<span data-ttu-id="946f9-119">接受会议请求。</span><span class="sxs-lookup"><span data-stu-id="946f9-119">Accept a meeting request.</span></span>  <br/> |
|<span data-ttu-id="946f9-120">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="946f9-120">CancelCalendarItem</span></span>  <br/> |<span data-ttu-id="946f9-121">取消会议。</span><span class="sxs-lookup"><span data-stu-id="946f9-121">Cancel a meeting.</span></span> <span data-ttu-id="946f9-122">这不同于正在删除所有与会者，因为它也将删除会议组织者。</span><span class="sxs-lookup"><span data-stu-id="946f9-122">This differs from deleting all attendees because it deletes the meeting for the organizer also.</span></span>  <br/> |
|<span data-ttu-id="946f9-123">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="946f9-123">DeclineItem</span></span>  <br/> |<span data-ttu-id="946f9-124">拒绝会议请求。</span><span class="sxs-lookup"><span data-stu-id="946f9-124">Decline a meeting request.</span></span>  <br/> |
|<span data-ttu-id="946f9-125">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="946f9-125">ForwardItem</span></span>  <br/> |<span data-ttu-id="946f9-126">作为会议请求发送给其他人的会议请求。</span><span class="sxs-lookup"><span data-stu-id="946f9-126">Send a meeting request to another person as a meeting request.</span></span>  <br/> |
|<span data-ttu-id="946f9-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="946f9-127">RemoveItem</span></span>  <br/> |<span data-ttu-id="946f9-128">从日历中删除已取消的会议。</span><span class="sxs-lookup"><span data-stu-id="946f9-128">Remove a canceled meeting from the calendar.</span></span>  <br/> |
|<span data-ttu-id="946f9-129">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="946f9-129">ReplyAllToItem</span></span>  <br/> |<span data-ttu-id="946f9-130">发送一条消息，包括向所有与会者的会议的原始会议请求的正文。</span><span class="sxs-lookup"><span data-stu-id="946f9-130">Send a message that includes the body of the original meeting request to all attendees of the meeting.</span></span>  <br/> |
|<span data-ttu-id="946f9-131">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="946f9-131">ReplyToItem</span></span>  <br/> |<span data-ttu-id="946f9-132">发送一条消息，包括对会议要求的发件人的原始会议请求的正文。</span><span class="sxs-lookup"><span data-stu-id="946f9-132">Send a message that includes the body of the original meeting request to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="946f9-133">SendReadReceipt</span><span class="sxs-lookup"><span data-stu-id="946f9-133">SendReadReceipt</span></span>  <br/> |<span data-ttu-id="946f9-134">向会议请求的发件人发送已读的回执。</span><span class="sxs-lookup"><span data-stu-id="946f9-134">Send a read receipt to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="946f9-135">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="946f9-135">TentativelyAcceptItem</span></span>  <br/> |<span data-ttu-id="946f9-136">暂时接受会议请求。</span><span class="sxs-lookup"><span data-stu-id="946f9-136">Tentatively accept a meeting request.</span></span>  <br/> |
   
<span data-ttu-id="946f9-137">CreateItem operation，还支持其他会议对象。</span><span class="sxs-lookup"><span data-stu-id="946f9-137">The CreateItem operation also supports additional meeting objects.</span></span> <span data-ttu-id="946f9-138">下表列出 CreateItem operation 支持的其他对象。</span><span class="sxs-lookup"><span data-stu-id="946f9-138">The following table lists additional objects that the CreateItem operation supports.</span></span>
  
|<span data-ttu-id="946f9-139">**会议对象**</span><span class="sxs-lookup"><span data-stu-id="946f9-139">**Meeting object**</span></span>|<span data-ttu-id="946f9-140">**说明**</span><span class="sxs-lookup"><span data-stu-id="946f9-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="946f9-141">会议消息</span><span class="sxs-lookup"><span data-stu-id="946f9-141">Meeting Message</span></span>  <br/> |<span data-ttu-id="946f9-142">代表 Exchange 存储中的会议消息。</span><span class="sxs-lookup"><span data-stu-id="946f9-142">Represents a meeting message in the Exchange store.</span></span> <span data-ttu-id="946f9-143">这是其他会议对象的基对象。</span><span class="sxs-lookup"><span data-stu-id="946f9-143">This is the base object for the other meeting objects.</span></span>  <br/> |
|<span data-ttu-id="946f9-144">会议要求</span><span class="sxs-lookup"><span data-stu-id="946f9-144">Meeting Request</span></span>  <br/> |<span data-ttu-id="946f9-145">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="946f9-145">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="946f9-146">会议响应</span><span class="sxs-lookup"><span data-stu-id="946f9-146">Meeting Response</span></span>  <br/> |<span data-ttu-id="946f9-147">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="946f9-147">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="946f9-148">取消会议</span><span class="sxs-lookup"><span data-stu-id="946f9-148">Meeting Cancellation</span></span>  <br/> |<span data-ttu-id="946f9-149">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="946f9-149">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="946f9-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="946f9-150">See also</span></span>



[<span data-ttu-id="946f9-151">CreateItem operation，（日历项）</span><span class="sxs-lookup"><span data-stu-id="946f9-151">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)
  
[<span data-ttu-id="946f9-152">CreateItem operation，（联系人）</span><span class="sxs-lookup"><span data-stu-id="946f9-152">CreateItem operation (contact)</span></span>](createitem-operation-contact.md)
  
[<span data-ttu-id="946f9-153">CreateItem operation，（电子邮件）</span><span class="sxs-lookup"><span data-stu-id="946f9-153">CreateItem operation (email message)</span></span>](createitem-operation-email-message.md)
  
[<span data-ttu-id="946f9-154">CreateItem operation，（会议请求）</span><span class="sxs-lookup"><span data-stu-id="946f9-154">CreateItem operation (meeting request)</span></span>](createitem-operation-meeting-request.md)
  
[<span data-ttu-id="946f9-155">CreateItem operation，（任务）</span><span class="sxs-lookup"><span data-stu-id="946f9-155">CreateItem operation (task)</span></span>](createitem-operation-task.md)
  
 <span data-ttu-id="946f9-156">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="946f9-156">**CreateItemType**</span></span>

