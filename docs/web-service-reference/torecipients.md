---
title: ToRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ToRecipients
api_type:
- schema
ms.assetid: 72dc3be8-30bb-4ae1-acf4-fb94ff490631
description: ToRecipients元素中包含收件人的项的数组。这是一项主要收件人。
ms.openlocfilehash: 39ee359e1eaf3d0b6455fb1734222e78054dc7f3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467541"
---
# <a name="torecipients"></a><span data-ttu-id="3a848-104">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="3a848-104">ToRecipients</span></span>

<span data-ttu-id="3a848-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **ToRecipients**元素中包含收件人的项的数组。这是一项主要收件人。</span><span class="sxs-lookup"><span data-stu-id="3a848-p102">The **ToRecipients** element contains an array of recipients of an item. These are the primary recipients of an item.</span></span> 
  
```xml
<ToRecipients>
   <Mailbox/>
</ToRecipients>
```

 <span data-ttu-id="3a848-107">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="3a848-107">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a848-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3a848-108">Attributes and elements</span></span>

<span data-ttu-id="3a848-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3a848-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a848-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="3a848-110">Attributes</span></span>

<span data-ttu-id="3a848-111">无。</span><span class="sxs-lookup"><span data-stu-id="3a848-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a848-112">子元素</span><span class="sxs-lookup"><span data-stu-id="3a848-112">Child elements</span></span>

|<span data-ttu-id="3a848-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3a848-113">**Element**</span></span>|<span data-ttu-id="3a848-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3a848-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a848-115">Mailbox</span><span class="sxs-lookup"><span data-stu-id="3a848-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="3a848-116">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="3a848-116">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a848-117">父元素</span><span class="sxs-lookup"><span data-stu-id="3a848-117">Parent elements</span></span>

|<span data-ttu-id="3a848-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="3a848-118">**Element**</span></span>|<span data-ttu-id="3a848-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="3a848-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a848-120">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="3a848-120">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="3a848-121">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="3a848-121">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a848-122">Message</span><span class="sxs-lookup"><span data-stu-id="3a848-122">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3a848-123">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="3a848-123">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="3a848-124">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="3a848-124">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="3a848-125">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="3a848-125">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a848-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3a848-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3a848-127">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="3a848-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a848-128">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="3a848-128">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="3a848-129">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="3a848-129">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a848-130">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="3a848-130">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="3a848-131">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="3a848-131">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a848-132">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="3a848-132">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="3a848-133">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="3a848-133">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3a848-134">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="3a848-134">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="3a848-135">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="3a848-135">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3a848-136">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="3a848-136">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="3a848-137">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="3a848-137">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3a848-138">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="3a848-138">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="3a848-139">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="3a848-139">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a848-140">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="3a848-140">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="3a848-141">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="3a848-141">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3a848-142">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="3a848-142">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="3a848-143">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="3a848-143">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="3a848-144">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="3a848-144">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="3a848-145">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="3a848-145">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a848-146">备注</span><span class="sxs-lookup"><span data-stu-id="3a848-146">Remarks</span></span>

<span data-ttu-id="3a848-p103">您无法通过使用 FindItem 请求获取 **ToRecipients** 。使用一个 GetItem 请求来获取 **ToRecipients**。</span><span class="sxs-lookup"><span data-stu-id="3a848-p103">You cannot get **ToRecipients** by using a FindItem request. Use a GetItem request to get the **ToRecipients**.</span></span>
  
<span data-ttu-id="3a848-149">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3a848-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a848-150">元素信息</span><span class="sxs-lookup"><span data-stu-id="3a848-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a848-151">命名空间</span><span class="sxs-lookup"><span data-stu-id="3a848-151">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3a848-152">架构名称</span><span class="sxs-lookup"><span data-stu-id="3a848-152">Schema Name</span></span>  <br/> |<span data-ttu-id="3a848-153">类型架构</span><span class="sxs-lookup"><span data-stu-id="3a848-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="3a848-154">验证文件</span><span class="sxs-lookup"><span data-stu-id="3a848-154">Validation File</span></span>  <br/> |<span data-ttu-id="3a848-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3a848-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3a848-156">可以为空</span><span class="sxs-lookup"><span data-stu-id="3a848-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="3a848-157">False</span><span class="sxs-lookup"><span data-stu-id="3a848-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a848-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a848-158">See also</span></span>



- [<span data-ttu-id="3a848-159">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3a848-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

