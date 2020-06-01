---
title: ResponseObjects
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseObjects
api_type:
- schema
ms.assetid: ad29e064-3f3d-4b7b-aa4c-9ec27326381d
description: ResponseObjects 元素包含与 Exchange 存储中的项目关联的所有响应对象的集合。
ms.openlocfilehash: 675bfda4addb38535736efc0c790577ff4739108
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457436"
---
# <a name="responseobjects"></a><span data-ttu-id="5f4f1-103">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="5f4f1-103">ResponseObjects</span></span>

<span data-ttu-id="5f4f1-104">**ResponseObjects**元素包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-104">The **ResponseObjects** element contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span> 
  
```XML
<ResponseObjects>
   <AcceptItem/>
   <TentativelyAcceptItem/>
   <DeclineItem/>
   <ReplyToItem/>
   <ForwardItem/>
   <ReplyAllToItem/>
   <CancelCalendarItem/>
   <RemoveItem/>
   <PostReplyItem/>
   <SuppressReadReceipt/>
   <AcceptSharingInvitation/>
</ResponseObjects>
```

 <span data-ttu-id="5f4f1-105">**NonEmptyArrayOfResponseObjectsType**</span><span class="sxs-lookup"><span data-stu-id="5f4f1-105">**NonEmptyArrayOfResponseObjectsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f4f1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5f4f1-106">Attributes and elements</span></span>

<span data-ttu-id="5f4f1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f4f1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5f4f1-108">Attributes</span></span>

<span data-ttu-id="5f4f1-109">无。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f4f1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5f4f1-110">Child elements</span></span>

|<span data-ttu-id="5f4f1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f4f1-111">**Element**</span></span>|<span data-ttu-id="5f4f1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f4f1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f4f1-113">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-113">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="5f4f1-114">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-114">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-115">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-115">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="5f4f1-116">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-116">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-117">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-117">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="5f4f1-118">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-118">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-119">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-119">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="5f4f1-120">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-120">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-121">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-121">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="5f4f1-122">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-122">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-123">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-123">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="5f4f1-124">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-124">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-125">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-125">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="5f4f1-126">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-126">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-127">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="5f4f1-128">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-128">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-129">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-129">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="5f4f1-130">包含对帖子项的答复。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-130">Contains a reply to a post item.</span></span> <span data-ttu-id="5f4f1-131">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-132">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="5f4f1-132">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="5f4f1-133">用于禁止阅读回执请求。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-133">Used to suppress read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-134">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="5f4f1-134">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="5f4f1-135">用于接受允许访问其他用户的 "日历" 或 "联系人" 数据的邀请。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-135">Used to accept an invitation that allows access to another user's calendar or contacts data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f4f1-136">父元素</span><span class="sxs-lookup"><span data-stu-id="5f4f1-136">Parent elements</span></span>

|<span data-ttu-id="5f4f1-137">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f4f1-137">**Element**</span></span>|<span data-ttu-id="5f4f1-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f4f1-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f4f1-139">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-139">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5f4f1-140">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-140">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-141">Contact</span><span class="sxs-lookup"><span data-stu-id="5f4f1-141">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5f4f1-142">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-142">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-143">DistributionList</span><span class="sxs-lookup"><span data-stu-id="5f4f1-143">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="5f4f1-144">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-144">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-145">项目</span><span class="sxs-lookup"><span data-stu-id="5f4f1-145">Item</span></span>](item.md) <br/> |<span data-ttu-id="5f4f1-146">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-146">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="5f4f1-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="5f4f1-148">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-149">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="5f4f1-149">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="5f4f1-150">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-150">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-151">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5f4f1-151">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5f4f1-152">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-152">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-153">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="5f4f1-153">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="5f4f1-154">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-154">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-155">Message</span><span class="sxs-lookup"><span data-stu-id="5f4f1-155">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5f4f1-156">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-156">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-157">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="5f4f1-157">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="5f4f1-158">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-158">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5f4f1-159">任务</span><span class="sxs-lookup"><span data-stu-id="5f4f1-159">Task</span></span>](task.md) <br/> |<span data-ttu-id="5f4f1-160">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-160">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f4f1-161">说明</span><span class="sxs-lookup"><span data-stu-id="5f4f1-161">Remarks</span></span>

<span data-ttu-id="5f4f1-162">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5f4f1-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f4f1-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="5f4f1-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f4f1-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="5f4f1-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f4f1-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="5f4f1-165">Schema Name</span></span>  <br/> |<span data-ttu-id="5f4f1-166">类型架构</span><span class="sxs-lookup"><span data-stu-id="5f4f1-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f4f1-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="5f4f1-167">Validation File</span></span>  <br/> |<span data-ttu-id="5f4f1-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f4f1-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f4f1-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="5f4f1-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="5f4f1-170">False</span><span class="sxs-lookup"><span data-stu-id="5f4f1-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f4f1-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f4f1-171">See also</span></span>



- [<span data-ttu-id="5f4f1-172">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5f4f1-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

