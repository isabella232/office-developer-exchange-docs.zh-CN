---
title: ReceivedBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceivedBy
api_type:
- schema
ms.assetid: ac84c9c5-d2fe-4b6f-bf4d-0444131d835b
description: ReceivedBy 元素标识代理访问方案中的委派。
ms.openlocfilehash: 7cee996c15e81f77d71f42e052b14b1d21772ba1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468248"
---
# <a name="receivedby"></a><span data-ttu-id="a7d56-103">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="a7d56-103">ReceivedBy</span></span>

<span data-ttu-id="a7d56-104">**ReceivedBy**元素标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="a7d56-104">The **ReceivedBy** element identifies the delegate in a delegate access scenario.</span></span> 
  
```xml
<ReceivedBy>
   <Mailbox/>
</ReceivedBy>
```

 <span data-ttu-id="a7d56-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="a7d56-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7d56-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a7d56-106">Attributes and elements</span></span>

<span data-ttu-id="a7d56-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a7d56-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7d56-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a7d56-108">Attributes</span></span>

<span data-ttu-id="a7d56-109">无。</span><span class="sxs-lookup"><span data-stu-id="a7d56-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7d56-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a7d56-110">Child elements</span></span>

|<span data-ttu-id="a7d56-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7d56-111">**Element**</span></span>|<span data-ttu-id="a7d56-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7d56-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7d56-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="a7d56-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="a7d56-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="a7d56-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7d56-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a7d56-115">Parent elements</span></span>

|<span data-ttu-id="a7d56-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7d56-116">**Element**</span></span>|<span data-ttu-id="a7d56-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7d56-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7d56-118">Message</span><span class="sxs-lookup"><span data-stu-id="a7d56-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a7d56-119">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="a7d56-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="a7d56-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="a7d56-121">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="a7d56-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a7d56-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a7d56-123">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="a7d56-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="a7d56-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="a7d56-125">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="a7d56-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="a7d56-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="a7d56-127">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="a7d56-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="a7d56-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="a7d56-129">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="a7d56-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="a7d56-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="a7d56-131">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="a7d56-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="a7d56-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="a7d56-133">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="a7d56-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="a7d56-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="a7d56-135">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="a7d56-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="a7d56-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="a7d56-137">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="a7d56-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="a7d56-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="a7d56-139">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="a7d56-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="a7d56-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="a7d56-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="a7d56-141">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="a7d56-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7d56-142">备注</span><span class="sxs-lookup"><span data-stu-id="a7d56-142">Remarks</span></span>

<span data-ttu-id="a7d56-143">**ReceivedRepresenting**元素与代理访问方案中的**From**和**ReceivedBy**元素一起使用。</span><span class="sxs-lookup"><span data-stu-id="a7d56-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="a7d56-144">下表列出了这些元素在代理访问方案中表示的实体。</span><span class="sxs-lookup"><span data-stu-id="a7d56-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="a7d56-145">**代理访问方案中的元素**</span><span class="sxs-lookup"><span data-stu-id="a7d56-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="a7d56-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7d56-146">**Element**</span></span>|<span data-ttu-id="a7d56-147">**元素所表示的实体**</span><span class="sxs-lookup"><span data-stu-id="a7d56-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7d56-148">From</span><span class="sxs-lookup"><span data-stu-id="a7d56-148">From</span></span>](from.md) <br/> |<span data-ttu-id="a7d56-149">ThirdParty</span><span class="sxs-lookup"><span data-stu-id="a7d56-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="a7d56-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="a7d56-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="a7d56-151">委派用户</span><span class="sxs-lookup"><span data-stu-id="a7d56-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="a7d56-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="a7d56-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="a7d56-153">校长</span><span class="sxs-lookup"><span data-stu-id="a7d56-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="a7d56-154">在代理访问方案中，如果 ThirdParty 向具有代理的主体发送会议请求，则代理将看到一个新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="a7d56-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="a7d56-155">这些元素使代理能够区分直接发送给他们的邮件和发送给他们的邮件，因为它是一个代理转发规则。</span><span class="sxs-lookup"><span data-stu-id="a7d56-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="a7d56-156">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a7d56-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7d56-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="a7d56-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7d56-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="a7d56-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7d56-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="a7d56-159">Schema Name</span></span>  <br/> |<span data-ttu-id="a7d56-160">类型架构</span><span class="sxs-lookup"><span data-stu-id="a7d56-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7d56-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="a7d56-161">Validation File</span></span>  <br/> |<span data-ttu-id="a7d56-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a7d56-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7d56-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="a7d56-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7d56-164">False</span><span class="sxs-lookup"><span data-stu-id="a7d56-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7d56-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a7d56-165">See also</span></span>



- [<span data-ttu-id="a7d56-166">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a7d56-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

