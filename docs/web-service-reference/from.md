---
title: From
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- From
api_type:
- schema
ms.assetid: 5a52d644-3677-4049-874c-12bd5c3080dc
description: 从元素均表示从其发送邮件的地址。
ms.openlocfilehash: 39c8c8ef84ff445e8f44ebb9f2285ccfc42353a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754438"
---
# <a name="from"></a><span data-ttu-id="84dfd-103">From</span><span class="sxs-lookup"><span data-stu-id="84dfd-103">From</span></span>

<span data-ttu-id="84dfd-104">**从**元素均表示从其发送邮件的地址。</span><span class="sxs-lookup"><span data-stu-id="84dfd-104">The **From** element represents the address from which the message was sent.</span></span> 
  
```xml
<From>
   <Mailbox/>
</From>
```

 <span data-ttu-id="84dfd-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="84dfd-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84dfd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84dfd-106">Attributes and elements</span></span>

<span data-ttu-id="84dfd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84dfd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84dfd-108">属性</span><span class="sxs-lookup"><span data-stu-id="84dfd-108">Attributes</span></span>

<span data-ttu-id="84dfd-109">无。</span><span class="sxs-lookup"><span data-stu-id="84dfd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84dfd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="84dfd-110">Child elements</span></span>

|<span data-ttu-id="84dfd-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="84dfd-111">**Element**</span></span>|<span data-ttu-id="84dfd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="84dfd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84dfd-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="84dfd-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="84dfd-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="84dfd-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="84dfd-115">父元素</span><span class="sxs-lookup"><span data-stu-id="84dfd-115">Parent elements</span></span>

|<span data-ttu-id="84dfd-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="84dfd-116">**Element**</span></span>|<span data-ttu-id="84dfd-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="84dfd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84dfd-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="84dfd-119">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="84dfd-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-120">Message</span><span class="sxs-lookup"><span data-stu-id="84dfd-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="84dfd-121">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="84dfd-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="84dfd-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="84dfd-123">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="84dfd-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="84dfd-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="84dfd-125">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="84dfd-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="84dfd-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="84dfd-127">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="84dfd-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="84dfd-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="84dfd-129">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="84dfd-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="84dfd-131">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="84dfd-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="84dfd-133">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="84dfd-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="84dfd-135">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="84dfd-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="84dfd-137">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="84dfd-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="84dfd-139">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="84dfd-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="84dfd-141">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="84dfd-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="84dfd-143">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="84dfd-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="84dfd-144">PostItem</span><span class="sxs-lookup"><span data-stu-id="84dfd-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="84dfd-145">代表一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="84dfd-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="84dfd-146">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="84dfd-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84dfd-147">注解</span><span class="sxs-lookup"><span data-stu-id="84dfd-147">Remarks</span></span>

<span data-ttu-id="84dfd-148">此元素用于"代表发送"电子邮件。</span><span class="sxs-lookup"><span data-stu-id="84dfd-148">This element is used for "send on behalf of" e-mails.</span></span>
  
<span data-ttu-id="84dfd-149">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="84dfd-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="84dfd-150">元素信息</span><span class="sxs-lookup"><span data-stu-id="84dfd-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84dfd-151">命名空间</span><span class="sxs-lookup"><span data-stu-id="84dfd-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84dfd-152">架构名称</span><span class="sxs-lookup"><span data-stu-id="84dfd-152">Schema Name</span></span>  <br/> |<span data-ttu-id="84dfd-153">类型架构</span><span class="sxs-lookup"><span data-stu-id="84dfd-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="84dfd-154">验证文件</span><span class="sxs-lookup"><span data-stu-id="84dfd-154">Validation File</span></span>  <br/> |<span data-ttu-id="84dfd-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="84dfd-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84dfd-156">可以为空</span><span class="sxs-lookup"><span data-stu-id="84dfd-156">Can be Empty</span></span>  <br/> |<span data-ttu-id="84dfd-157">False</span><span class="sxs-lookup"><span data-stu-id="84dfd-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84dfd-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84dfd-158">See also</span></span>



- [<span data-ttu-id="84dfd-159">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="84dfd-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

