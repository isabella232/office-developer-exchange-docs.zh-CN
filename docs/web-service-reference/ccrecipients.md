---
title: CcRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CcRecipients
api_type:
- schema
ms.assetid: 5c20ec3a-0bee-4e67-b220-586ed0d601c9
description: CcRecipients元素代表将收到一份邮件的收件人的集合。
ms.openlocfilehash: 57d0e2d3b2c44fbd7bb30696002b27e83d1e274e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462204"
---
# <a name="ccrecipients"></a><span data-ttu-id="6d97e-103">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="6d97e-103">CcRecipients</span></span>

<span data-ttu-id="6d97e-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CcRecipients**元素代表将收到一份邮件的收件人的集合。</span><span class="sxs-lookup"><span data-stu-id="6d97e-104">The **CcRecipients** element represents a collection of recipients that will receive a copy of the message.</span></span> 
  
```xml
<CcRecipients>
   <Mailbox/>
</CcRecipients>
```

 <span data-ttu-id="6d97e-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="6d97e-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d97e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6d97e-106">Attributes and elements</span></span>

<span data-ttu-id="6d97e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6d97e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d97e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6d97e-108">Attributes</span></span>

<span data-ttu-id="6d97e-109">无。</span><span class="sxs-lookup"><span data-stu-id="6d97e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d97e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6d97e-110">Child elements</span></span>

|<span data-ttu-id="6d97e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6d97e-111">**Element**</span></span>|<span data-ttu-id="6d97e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6d97e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d97e-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="6d97e-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="6d97e-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="6d97e-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6d97e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6d97e-115">Parent elements</span></span>

|<span data-ttu-id="6d97e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6d97e-116">**Element**</span></span>|<span data-ttu-id="6d97e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6d97e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d97e-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="6d97e-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="6d97e-119">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="6d97e-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-120">Message</span><span class="sxs-lookup"><span data-stu-id="6d97e-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="6d97e-121">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="6d97e-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="6d97e-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="6d97e-123">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="6d97e-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="6d97e-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="6d97e-125">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="6d97e-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="6d97e-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="6d97e-127">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="6d97e-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="6d97e-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="6d97e-129">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="6d97e-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="6d97e-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="6d97e-131">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="6d97e-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="6d97e-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="6d97e-133">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="6d97e-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="6d97e-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="6d97e-135">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="6d97e-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="6d97e-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="6d97e-137">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="6d97e-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="6d97e-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="6d97e-139">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="6d97e-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="6d97e-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="6d97e-141">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="6d97e-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="6d97e-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="6d97e-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="6d97e-143">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="6d97e-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d97e-144">备注</span><span class="sxs-lookup"><span data-stu-id="6d97e-144">Remarks</span></span>

<span data-ttu-id="6d97e-p101">您无法通过使用 FindItem 请求获取 **CcRecipients** 。使用一个 GetItem 请求来获取 **CcRecipients**。</span><span class="sxs-lookup"><span data-stu-id="6d97e-p101">You cannot get **CcRecipients** by using a FindItem request. Use a GetItem request to get **CcRecipients**.</span></span>
  
<span data-ttu-id="6d97e-147">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6d97e-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d97e-148">元素信息</span><span class="sxs-lookup"><span data-stu-id="6d97e-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d97e-149">命名空间</span><span class="sxs-lookup"><span data-stu-id="6d97e-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6d97e-150">架构名称</span><span class="sxs-lookup"><span data-stu-id="6d97e-150">Schema Name</span></span>  <br/> |<span data-ttu-id="6d97e-151">类型架构</span><span class="sxs-lookup"><span data-stu-id="6d97e-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="6d97e-152">验证文件</span><span class="sxs-lookup"><span data-stu-id="6d97e-152">Validation File</span></span>  <br/> |<span data-ttu-id="6d97e-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6d97e-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6d97e-154">可以为空</span><span class="sxs-lookup"><span data-stu-id="6d97e-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="6d97e-155">False</span><span class="sxs-lookup"><span data-stu-id="6d97e-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d97e-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6d97e-156">See also</span></span>



- [<span data-ttu-id="6d97e-157">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6d97e-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

