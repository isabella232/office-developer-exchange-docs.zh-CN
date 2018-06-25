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
description: ReceivedBy 元素标识委派访问方案中的委托。
ms.openlocfilehash: 7918fa3320223e5cf02dd225912adfae3181e29c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826969"
---
# <a name="receivedby"></a><span data-ttu-id="7b14e-103">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="7b14e-103">ReceivedBy</span></span>

<span data-ttu-id="7b14e-104">**ReceivedBy**元素标识委派访问方案中的委托。</span><span class="sxs-lookup"><span data-stu-id="7b14e-104">The **ReceivedBy** element identifies the delegate in a delegate access scenario.</span></span> 
  
```xml
<ReceivedBy>
   <Mailbox/>
</ReceivedBy>
```

 <span data-ttu-id="7b14e-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="7b14e-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b14e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7b14e-106">Attributes and elements</span></span>

<span data-ttu-id="7b14e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7b14e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b14e-108">属性</span><span class="sxs-lookup"><span data-stu-id="7b14e-108">Attributes</span></span>

<span data-ttu-id="7b14e-109">无。</span><span class="sxs-lookup"><span data-stu-id="7b14e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b14e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7b14e-110">Child elements</span></span>

|<span data-ttu-id="7b14e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b14e-111">**Element**</span></span>|<span data-ttu-id="7b14e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b14e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b14e-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="7b14e-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="7b14e-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="7b14e-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b14e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7b14e-115">Parent elements</span></span>

|<span data-ttu-id="7b14e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b14e-116">**Element**</span></span>|<span data-ttu-id="7b14e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b14e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b14e-118">Message</span><span class="sxs-lookup"><span data-stu-id="7b14e-118">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="7b14e-119">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="7b14e-119">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-120">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="7b14e-120">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="7b14e-121">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="7b14e-121">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-122">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="7b14e-122">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="7b14e-123">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="7b14e-123">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-124">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="7b14e-124">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="7b14e-125">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="7b14e-125">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-126">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="7b14e-126">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="7b14e-127">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="7b14e-127">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-128">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="7b14e-128">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="7b14e-129">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="7b14e-129">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-130">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="7b14e-130">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="7b14e-131">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="7b14e-131">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-132">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="7b14e-132">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="7b14e-133">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="7b14e-133">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-134">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="7b14e-134">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="7b14e-135">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="7b14e-135">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-136">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="7b14e-136">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="7b14e-137">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="7b14e-137">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-138">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="7b14e-138">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="7b14e-139">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="7b14e-139">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="7b14e-140">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="7b14e-140">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="7b14e-141">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="7b14e-141">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b14e-142">备注</span><span class="sxs-lookup"><span data-stu-id="7b14e-142">Remarks</span></span>

<span data-ttu-id="7b14e-143">**ReceivedRepresenting**元素与**从**结合使用并**ReceivedBy**元素中的委派访问方案。</span><span class="sxs-lookup"><span data-stu-id="7b14e-143">The **ReceivedRepresenting** element is used together with the **From** and **ReceivedBy** elements in delegate access scenarios.</span></span> <span data-ttu-id="7b14e-144">下表列出了这些元素表示委派访问方案中的实体。</span><span class="sxs-lookup"><span data-stu-id="7b14e-144">The following table lists the entities that these elements represent in a delegate access scenario.</span></span> 
  
<span data-ttu-id="7b14e-145">**委派访问方案中的元素**</span><span class="sxs-lookup"><span data-stu-id="7b14e-145">**Elements in a delegate access scenario**</span></span>

|<span data-ttu-id="7b14e-146">**元素**</span><span class="sxs-lookup"><span data-stu-id="7b14e-146">**Element**</span></span>|<span data-ttu-id="7b14e-147">**元素表示的实体**</span><span class="sxs-lookup"><span data-stu-id="7b14e-147">**Entity that the element represent**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b14e-148">发件人</span><span class="sxs-lookup"><span data-stu-id="7b14e-148">From</span></span>](from.md) <br/> |<span data-ttu-id="7b14e-149">第三方</span><span class="sxs-lookup"><span data-stu-id="7b14e-149">ThirdParty</span></span>  <br/> |
|[<span data-ttu-id="7b14e-150">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="7b14e-150">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="7b14e-151">委托</span><span class="sxs-lookup"><span data-stu-id="7b14e-151">Delegate</span></span>  <br/> |
|[<span data-ttu-id="7b14e-152">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="7b14e-152">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="7b14e-153">Principal</span><span class="sxs-lookup"><span data-stu-id="7b14e-153">Principal</span></span>  <br/> |
   
<span data-ttu-id="7b14e-154">在委派访问方案中，如果第三方将会议请求发送到的主体拥有代理人，代理人将看到新的会议请求。</span><span class="sxs-lookup"><span data-stu-id="7b14e-154">In a delegate access scenario, if a ThirdParty sends a meeting request to a Principal who has a Delegate, the Delegate will see a new meeting request.</span></span> <span data-ttu-id="7b14e-155">这些元素启用代理人来区分直接向他们发送的邮件和消息发送给他们由于代理人转接规则。</span><span class="sxs-lookup"><span data-stu-id="7b14e-155">These elements enable delegates to distinguish between messages that are sent directly to them and messages that are sent to them because of a delegate forwarding rule.</span></span>
  
<span data-ttu-id="7b14e-156">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7b14e-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b14e-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="7b14e-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b14e-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="7b14e-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7b14e-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="7b14e-159">Schema Name</span></span>  <br/> |<span data-ttu-id="7b14e-160">类型架构</span><span class="sxs-lookup"><span data-stu-id="7b14e-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="7b14e-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="7b14e-161">Validation File</span></span>  <br/> |<span data-ttu-id="7b14e-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7b14e-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7b14e-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="7b14e-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="7b14e-164">False</span><span class="sxs-lookup"><span data-stu-id="7b14e-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b14e-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b14e-165">See also</span></span>



- [<span data-ttu-id="7b14e-166">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7b14e-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

