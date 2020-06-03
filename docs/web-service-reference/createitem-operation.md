---
title: CreateItem 操作
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
description: CreateItem 操作在 Exchange 存储中创建项目。
ms.openlocfilehash: f6aaa9ed8e8257f19780492d6137fb015c1b6136
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458864"
---
# <a name="createitem-operation"></a><span data-ttu-id="7c3ea-103">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="7c3ea-103">CreateItem operation</span></span>

<span data-ttu-id="7c3ea-104">CreateItem 操作在 Exchange 存储中创建项目。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-104">The CreateItem operation creates items in the Exchange store.</span></span>
  
## <a name="using-the-createitem-operation"></a><span data-ttu-id="7c3ea-105">使用 CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="7c3ea-105">Using the CreateItem Operation</span></span>

<span data-ttu-id="7c3ea-106">您可以使用 CreateItem 操作创建以下内容：</span><span class="sxs-lookup"><span data-stu-id="7c3ea-106">You can use the CreateItem operation to create the following:</span></span>
  
- <span data-ttu-id="7c3ea-107">日历项目</span><span class="sxs-lookup"><span data-stu-id="7c3ea-107">Calendar items</span></span>
    
- <span data-ttu-id="7c3ea-108">电子邮件</span><span class="sxs-lookup"><span data-stu-id="7c3ea-108">E-mail messages</span></span>
    
- <span data-ttu-id="7c3ea-109">会议请求</span><span class="sxs-lookup"><span data-stu-id="7c3ea-109">Meeting requests</span></span>
    
- <span data-ttu-id="7c3ea-110">任务</span><span class="sxs-lookup"><span data-stu-id="7c3ea-110">Tasks</span></span>
    
- <span data-ttu-id="7c3ea-111">联系人</span><span class="sxs-lookup"><span data-stu-id="7c3ea-111">Contacts</span></span>
    
<span data-ttu-id="7c3ea-112">有关详细信息，请参阅[CreateItem 操作（日历项目）](createitem-operation-calendar-item.md)、 [CreateItem 操作（电子邮件）](createitem-operation-email-message.md)、 [CreateItem 操作（会议请求）](createitem-operation-meeting-request.md)、 [CreateItem 操作（任务）](createitem-operation-task.md)和[CreateItem 操作（联系人）](createitem-operation-contact.md)。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-112">For more information, see [CreateItem operation (calendar item)](createitem-operation-calendar-item.md), [CreateItem operation (email message)](createitem-operation-email-message.md), [CreateItem operation (meeting request)](createitem-operation-meeting-request.md), [CreateItem operation (task)](createitem-operation-task.md), and [CreateItem operation (contact)](createitem-operation-contact.md).</span></span>
  
<span data-ttu-id="7c3ea-113">CreateItem 操作支持使用 response 对象。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-113">The CreateItem operation supports the use of response objects.</span></span> <span data-ttu-id="7c3ea-114">Response 对象支持会议的接受和拒绝，以及处理标准电子邮件中包含的投票按钮。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-114">Response objects support the acceptance and rejection of meetings and the handling of voting buttons that are included in a standard e-mail message.</span></span> <span data-ttu-id="7c3ea-115">下表列出了在 CreateItem 操作中处理的响应对象。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-115">The following table lists the response objects that are handled in the CreateItem operation.</span></span>
  
|<span data-ttu-id="7c3ea-116">**Response 对象**</span><span class="sxs-lookup"><span data-stu-id="7c3ea-116">**Response object**</span></span>|<span data-ttu-id="7c3ea-117">**Action**</span><span class="sxs-lookup"><span data-stu-id="7c3ea-117">**Action**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c3ea-118">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="7c3ea-118">AcceptItem</span></span>  <br/> |<span data-ttu-id="7c3ea-119">接受会议请求。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-119">Accept a meeting request.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-120">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="7c3ea-120">CancelCalendarItem</span></span>  <br/> |<span data-ttu-id="7c3ea-121">取消会议。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-121">Cancel a meeting.</span></span> <span data-ttu-id="7c3ea-122">这与删除所有与会者的方法不同，因为它也会删除组织者的会议。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-122">This differs from deleting all attendees because it deletes the meeting for the organizer also.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-123">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="7c3ea-123">DeclineItem</span></span>  <br/> |<span data-ttu-id="7c3ea-124">拒绝会议请求。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-124">Decline a meeting request.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-125">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="7c3ea-125">ForwardItem</span></span>  <br/> |<span data-ttu-id="7c3ea-126">将会议请求作为会议请求发送给其他人。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-126">Send a meeting request to another person as a meeting request.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="7c3ea-127">RemoveItem</span></span>  <br/> |<span data-ttu-id="7c3ea-128">从日历中删除取消的会议。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-128">Remove a canceled meeting from the calendar.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-129">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="7c3ea-129">ReplyAllToItem</span></span>  <br/> |<span data-ttu-id="7c3ea-130">向会议的所有与会者发送包含原始会议请求正文的邮件。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-130">Send a message that includes the body of the original meeting request to all attendees of the meeting.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-131">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="7c3ea-131">ReplyToItem</span></span>  <br/> |<span data-ttu-id="7c3ea-132">将包含原始会议请求正文的邮件发送给会议请求的发件人。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-132">Send a message that includes the body of the original meeting request to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-133">SendReadReceipt</span><span class="sxs-lookup"><span data-stu-id="7c3ea-133">SendReadReceipt</span></span>  <br/> |<span data-ttu-id="7c3ea-134">将 "已读" 回执发送给会议请求的发件人。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-134">Send a read receipt to the sender of the meeting request.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-135">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="7c3ea-135">TentativelyAcceptItem</span></span>  <br/> |<span data-ttu-id="7c3ea-136">暂时接受会议请求。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-136">Tentatively accept a meeting request.</span></span>  <br/> |
   
<span data-ttu-id="7c3ea-137">CreateItem 操作还支持其他会议对象。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-137">The CreateItem operation also supports additional meeting objects.</span></span> <span data-ttu-id="7c3ea-138">下表列出了 CreateItem 操作支持的其他对象。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-138">The following table lists additional objects that the CreateItem operation supports.</span></span>
  
|<span data-ttu-id="7c3ea-139">**会议对象**</span><span class="sxs-lookup"><span data-stu-id="7c3ea-139">**Meeting object**</span></span>|<span data-ttu-id="7c3ea-140">**说明**</span><span class="sxs-lookup"><span data-stu-id="7c3ea-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c3ea-141">会议邮件</span><span class="sxs-lookup"><span data-stu-id="7c3ea-141">Meeting Message</span></span>  <br/> |<span data-ttu-id="7c3ea-142">表示 Exchange 存储中的会议邮件。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-142">Represents a meeting message in the Exchange store.</span></span> <span data-ttu-id="7c3ea-143">这是其他会议对象的基本对象。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-143">This is the base object for the other meeting objects.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-144">会议要求</span><span class="sxs-lookup"><span data-stu-id="7c3ea-144">Meeting Request</span></span>  <br/> |<span data-ttu-id="7c3ea-145">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-145">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-146">会议响应</span><span class="sxs-lookup"><span data-stu-id="7c3ea-146">Meeting Response</span></span>  <br/> |<span data-ttu-id="7c3ea-147">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-147">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|<span data-ttu-id="7c3ea-148">会议取消</span><span class="sxs-lookup"><span data-stu-id="7c3ea-148">Meeting Cancellation</span></span>  <br/> |<span data-ttu-id="7c3ea-149">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="7c3ea-149">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7c3ea-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7c3ea-150">See also</span></span>



[<span data-ttu-id="7c3ea-151">CreateItem 操作（日历项目）</span><span class="sxs-lookup"><span data-stu-id="7c3ea-151">CreateItem operation (calendar item)</span></span>](createitem-operation-calendar-item.md)
  
[<span data-ttu-id="7c3ea-152">CreateItem 操作（联系人）</span><span class="sxs-lookup"><span data-stu-id="7c3ea-152">CreateItem operation (contact)</span></span>](createitem-operation-contact.md)
  
[<span data-ttu-id="7c3ea-153">CreateItem 操作（电子邮件）</span><span class="sxs-lookup"><span data-stu-id="7c3ea-153">CreateItem operation (email message)</span></span>](createitem-operation-email-message.md)
  
[<span data-ttu-id="7c3ea-154">CreateItem 操作（会议请求）</span><span class="sxs-lookup"><span data-stu-id="7c3ea-154">CreateItem operation (meeting request)</span></span>](createitem-operation-meeting-request.md)
  
[<span data-ttu-id="7c3ea-155">CreateItem 操作（任务）</span><span class="sxs-lookup"><span data-stu-id="7c3ea-155">CreateItem operation (task)</span></span>](createitem-operation-task.md)
  
 <span data-ttu-id="7c3ea-156">**CreateItemType**</span><span class="sxs-lookup"><span data-stu-id="7c3ea-156">**CreateItemType**</span></span>

