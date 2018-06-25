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
description: ResponseObjects 元素包含与 Exchange 存储中的项相关联的所有响应对象的集合。
ms.openlocfilehash: b1d95063439f5089665d2aad97d747665caef0ca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827197"
---
# <a name="responseobjects"></a><span data-ttu-id="8fa9d-103">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="8fa9d-103">ResponseObjects</span></span>

<span data-ttu-id="8fa9d-104">**ResponseObjects**元素包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-104">The **ResponseObjects** element contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span> 
  
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

 <span data-ttu-id="8fa9d-105">**NonEmptyArrayOfResponseObjectsType**</span><span class="sxs-lookup"><span data-stu-id="8fa9d-105">**NonEmptyArrayOfResponseObjectsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8fa9d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8fa9d-106">Attributes and elements</span></span>

<span data-ttu-id="8fa9d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8fa9d-108">属性</span><span class="sxs-lookup"><span data-stu-id="8fa9d-108">Attributes</span></span>

<span data-ttu-id="8fa9d-109">无。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8fa9d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8fa9d-110">Child elements</span></span>

|<span data-ttu-id="8fa9d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8fa9d-111">**Element**</span></span>|<span data-ttu-id="8fa9d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8fa9d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fa9d-113">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-113">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="8fa9d-114">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-114">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-115">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-115">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="8fa9d-116">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-116">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-117">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-117">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="8fa9d-118">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-118">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-119">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-119">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="8fa9d-120">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-120">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-121">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-121">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="8fa9d-122">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-122">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-123">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-123">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="8fa9d-124">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-124">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-125">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-125">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="8fa9d-126">代表用来取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-126">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-127">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-127">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="8fa9d-128">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-128">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-129">PostReplyItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-129">PostReplyItem</span></span>](postreplyitem.md) <br/> |<span data-ttu-id="8fa9d-130">包含一个公告项目答复。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-130">Contains a reply to a post item.</span></span> <span data-ttu-id="8fa9d-131">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-132">SuppressReadReceipt</span><span class="sxs-lookup"><span data-stu-id="8fa9d-132">SuppressReadReceipt</span></span>](suppressreadreceipt.md) <br/> |<span data-ttu-id="8fa9d-133">用于取消读的回执请求。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-133">Used to suppress read receipt requests.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-134">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="8fa9d-134">AcceptSharingInvitation</span></span>](acceptsharinginvitation.md) <br/> |<span data-ttu-id="8fa9d-135">用于接受邀请，允许访问其他用户的日历或联系人数据。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-135">Used to accept an invitation that allows access to another user's calendar or contacts data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8fa9d-136">父元素</span><span class="sxs-lookup"><span data-stu-id="8fa9d-136">Parent elements</span></span>

|<span data-ttu-id="8fa9d-137">**元素**</span><span class="sxs-lookup"><span data-stu-id="8fa9d-137">**Element**</span></span>|<span data-ttu-id="8fa9d-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="8fa9d-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fa9d-139">日历项目</span><span class="sxs-lookup"><span data-stu-id="8fa9d-139">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8fa9d-140">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-140">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-141">联系人</span><span class="sxs-lookup"><span data-stu-id="8fa9d-141">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="8fa9d-142">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-142">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-143">DistributionList</span><span class="sxs-lookup"><span data-stu-id="8fa9d-143">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="8fa9d-144">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-144">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-145">项目</span><span class="sxs-lookup"><span data-stu-id="8fa9d-145">Item</span></span>](item.md) <br/> |<span data-ttu-id="8fa9d-146">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-146">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-147">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="8fa9d-147">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="8fa9d-148">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-148">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-149">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="8fa9d-149">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="8fa9d-150">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-150">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-151">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8fa9d-151">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8fa9d-152">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-152">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-153">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="8fa9d-153">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="8fa9d-154">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-154">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-155">Message</span><span class="sxs-lookup"><span data-stu-id="8fa9d-155">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="8fa9d-156">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-156">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-157">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="8fa9d-157">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="8fa9d-158">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-158">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8fa9d-159">任务</span><span class="sxs-lookup"><span data-stu-id="8fa9d-159">Task</span></span>](task.md) <br/> |<span data-ttu-id="8fa9d-160">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-160">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8fa9d-161">备注</span><span class="sxs-lookup"><span data-stu-id="8fa9d-161">Remarks</span></span>

<span data-ttu-id="8fa9d-162">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8fa9d-162">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8fa9d-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="8fa9d-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8fa9d-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="8fa9d-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8fa9d-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="8fa9d-165">Schema Name</span></span>  <br/> |<span data-ttu-id="8fa9d-166">类型架构</span><span class="sxs-lookup"><span data-stu-id="8fa9d-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="8fa9d-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="8fa9d-167">Validation File</span></span>  <br/> |<span data-ttu-id="8fa9d-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8fa9d-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8fa9d-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="8fa9d-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="8fa9d-170">False</span><span class="sxs-lookup"><span data-stu-id="8fa9d-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fa9d-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8fa9d-171">See also</span></span>



- [<span data-ttu-id="8fa9d-172">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8fa9d-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

