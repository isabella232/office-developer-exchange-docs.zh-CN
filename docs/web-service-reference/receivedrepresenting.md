---
title: ReceivedRepresenting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceivedRepresenting
api_type:
- schema
ms.assetid: 1157b042-6dce-4cdc-9700-e22b749da39f
description: ReceivedRepresenting 元素标识代理访问方案中的主体。
ms.openlocfilehash: f444fb88be9c0df174f0c1490cf7c499cc0c0539
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468220"
---
# <a name="receivedrepresenting"></a><span data-ttu-id="dc3b1-103">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="dc3b1-103">ReceivedRepresenting</span></span>

<span data-ttu-id="dc3b1-104">**ReceivedRepresenting**元素标识代理访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-104">The **ReceivedRepresenting** element identifies the principal in a delegate access scenario.</span></span> 
  
```xml
<ReceivedRepresenting>
   <Mailbox/>
</ReceivedRepresenting>
```

 <span data-ttu-id="dc3b1-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="dc3b1-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc3b1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc3b1-106">Attributes and elements</span></span>

<span data-ttu-id="dc3b1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc3b1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dc3b1-108">Attributes</span></span>

<span data-ttu-id="dc3b1-109">无。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc3b1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dc3b1-110">Child elements</span></span>

|<span data-ttu-id="dc3b1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc3b1-111">**Element**</span></span>|<span data-ttu-id="dc3b1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc3b1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc3b1-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="dc3b1-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="dc3b1-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc3b1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="dc3b1-115">Parent elements</span></span>

|<span data-ttu-id="dc3b1-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc3b1-116">**Element**</span></span>|<span data-ttu-id="dc3b1-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc3b1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc3b1-118">Message</span><span class="sxs-lookup"><span data-stu-id="dc3b1-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="dc3b1-119">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="dc3b1-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="dc3b1-121">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="dc3b1-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="dc3b1-123">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="dc3b1-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="dc3b1-125">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="dc3b1-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="dc3b1-127">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="dc3b1-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="dc3b1-129">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="dc3b1-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="dc3b1-131">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="dc3b1-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="dc3b1-133">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="dc3b1-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="dc3b1-135">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="dc3b1-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="dc3b1-137">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="dc3b1-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="dc3b1-139">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="dc3b1-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="dc3b1-141">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc3b1-142">备注</span><span class="sxs-lookup"><span data-stu-id="dc3b1-142">Remarks</span></span>

<span data-ttu-id="dc3b1-143">**ReceivedRepresenting**元素与代理访问方案中的**From**和**ReceivedBy**元素一起使用。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="dc3b1-144">下表列出了这些元素在代理访问方案中表示的实体。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="dc3b1-145">**代理访问方案中的元素**</span><span class="sxs-lookup"><span data-stu-id="dc3b1-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="dc3b1-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc3b1-146">**Element**</span></span>|<span data-ttu-id="dc3b1-147">**元素所表示的实体**</span><span class="sxs-lookup"><span data-stu-id="dc3b1-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc3b1-148">From</span><span class="sxs-lookup"><span data-stu-id="dc3b1-148">From</span></span>](from.md) <br/> |<span data-ttu-id="dc3b1-149">ThirdParty</span><span class="sxs-lookup"><span data-stu-id="dc3b1-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="dc3b1-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="dc3b1-151">委派用户</span><span class="sxs-lookup"><span data-stu-id="dc3b1-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="dc3b1-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="dc3b1-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="dc3b1-153">校长</span><span class="sxs-lookup"><span data-stu-id="dc3b1-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="dc3b1-154">在代理访问方案中，如果 ThirdParty 向具有代理的主体发送会议请求，则代理将看到一个新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="dc3b1-155">这些元素使代理能够区分直接发送给他们的邮件和发送给他们的邮件，因为它是一个代理转发规则。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="dc3b1-156">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc3b1-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc3b1-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc3b1-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc3b1-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc3b1-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc3b1-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc3b1-159">Schema Name</span></span>  <br/> |<span data-ttu-id="dc3b1-160">类型架构</span><span class="sxs-lookup"><span data-stu-id="dc3b1-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc3b1-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc3b1-161">Validation File</span></span>  <br/> |<span data-ttu-id="dc3b1-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc3b1-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc3b1-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc3b1-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="dc3b1-164">False</span><span class="sxs-lookup"><span data-stu-id="dc3b1-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc3b1-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc3b1-165">See also</span></span>



- [<span data-ttu-id="dc3b1-166">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dc3b1-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

