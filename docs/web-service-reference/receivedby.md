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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468248"
---
# <a name="receivedby"></a><span data-ttu-id="626a9-103">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="626a9-103">ReceivedBy</span></span>

<span data-ttu-id="626a9-104">**ReceivedBy**元素标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="626a9-104">The **ReceivedBy** element identifies the delegate in a delegate access scenario.</span></span> 
  
```xml
<ReceivedBy>
   <Mailbox/>
</ReceivedBy>
```

 <span data-ttu-id="626a9-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="626a9-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="626a9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="626a9-106">Attributes and elements</span></span>

<span data-ttu-id="626a9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="626a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="626a9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="626a9-108">Attributes</span></span>

<span data-ttu-id="626a9-109">无。</span><span class="sxs-lookup"><span data-stu-id="626a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="626a9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="626a9-110">Child elements</span></span>

|<span data-ttu-id="626a9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="626a9-111">**Element**</span></span>|<span data-ttu-id="626a9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="626a9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="626a9-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="626a9-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="626a9-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="626a9-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="626a9-115">父元素</span><span class="sxs-lookup"><span data-stu-id="626a9-115">Parent elements</span></span>

|<span data-ttu-id="626a9-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="626a9-116">**Element**</span></span>|<span data-ttu-id="626a9-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="626a9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="626a9-118">Message</span><span class="sxs-lookup"><span data-stu-id="626a9-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="626a9-119">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="626a9-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="626a9-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="626a9-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="626a9-121">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="626a9-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="626a9-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="626a9-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="626a9-123">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="626a9-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="626a9-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="626a9-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="626a9-125">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="626a9-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="626a9-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="626a9-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="626a9-127">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="626a9-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="626a9-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="626a9-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="626a9-129">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="626a9-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="626a9-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="626a9-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="626a9-131">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="626a9-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="626a9-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="626a9-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="626a9-133">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="626a9-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="626a9-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="626a9-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="626a9-135">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="626a9-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="626a9-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="626a9-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="626a9-137">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="626a9-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="626a9-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="626a9-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="626a9-139">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="626a9-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="626a9-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="626a9-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="626a9-141">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="626a9-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="626a9-142">备注</span><span class="sxs-lookup"><span data-stu-id="626a9-142">Remarks</span></span>

<span data-ttu-id="626a9-143">**ReceivedRepresenting**元素与代理访问方案中的**From**和**ReceivedBy**元素一起使用。</span><span class="sxs-lookup"><span data-stu-id="626a9-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="626a9-144">下表列出了这些元素在代理访问方案中表示的实体。</span><span class="sxs-lookup"><span data-stu-id="626a9-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="626a9-145">**代理访问方案中的元素**</span><span class="sxs-lookup"><span data-stu-id="626a9-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="626a9-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="626a9-146">**Element**</span></span>|<span data-ttu-id="626a9-147">**元素所表示的实体**</span><span class="sxs-lookup"><span data-stu-id="626a9-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="626a9-148">From</span><span class="sxs-lookup"><span data-stu-id="626a9-148">From</span></span>](from.md) <br/> |<span data-ttu-id="626a9-149">ThirdParty</span><span class="sxs-lookup"><span data-stu-id="626a9-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="626a9-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="626a9-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="626a9-151">委派用户</span><span class="sxs-lookup"><span data-stu-id="626a9-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="626a9-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="626a9-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="626a9-153">校长</span><span class="sxs-lookup"><span data-stu-id="626a9-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="626a9-154">在代理访问方案中，如果 ThirdParty 向具有代理的主体发送会议请求，则代理将看到一个新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="626a9-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="626a9-155">这些元素使代理能够区分直接发送给他们的邮件和发送给他们的邮件，因为它是一个代理转发规则。</span><span class="sxs-lookup"><span data-stu-id="626a9-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="626a9-156">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="626a9-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="626a9-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="626a9-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="626a9-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="626a9-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="626a9-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="626a9-159">Schema Name</span></span>  <br/> |<span data-ttu-id="626a9-160">类型架构</span><span class="sxs-lookup"><span data-stu-id="626a9-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="626a9-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="626a9-161">Validation File</span></span>  <br/> |<span data-ttu-id="626a9-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="626a9-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="626a9-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="626a9-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="626a9-164">False</span><span class="sxs-lookup"><span data-stu-id="626a9-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="626a9-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="626a9-165">See also</span></span>



- [<span data-ttu-id="626a9-166">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="626a9-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

