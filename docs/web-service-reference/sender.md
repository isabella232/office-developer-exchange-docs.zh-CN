---
title: 发件人
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Sender
api_type:
- schema
ms.assetid: 26d1a46e-e1d3-44b8-a02d-fa6f83aa5cda
description: Sender 元素标识项目的发件人。
ms.openlocfilehash: f056fefdd5c5832d4b5bf20416e07e376f6a03de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530577"
---
# <a name="sender"></a><span data-ttu-id="15d4d-103">发件人</span><span class="sxs-lookup"><span data-stu-id="15d4d-103">Sender</span></span>

<span data-ttu-id="15d4d-104">**Sender**元素标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="15d4d-104">The **Sender** element identifies the sender of an item.</span></span> 
  
```xml
<Sender>
   <Mailbox/>
</Sender>
```

 <span data-ttu-id="15d4d-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="15d4d-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15d4d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="15d4d-106">Attributes and elements</span></span>

<span data-ttu-id="15d4d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15d4d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15d4d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="15d4d-108">Attributes</span></span>

<span data-ttu-id="15d4d-109">无。</span><span class="sxs-lookup"><span data-stu-id="15d4d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15d4d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="15d4d-110">Child elements</span></span>

|<span data-ttu-id="15d4d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="15d4d-111">**Element**</span></span>|<span data-ttu-id="15d4d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="15d4d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15d4d-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="15d4d-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="15d4d-114">标识已启用邮件的 Active Directory 对象，用于标识发件人。</span><span class="sxs-lookup"><span data-stu-id="15d4d-114">Identifies a mail enabled Active Directory object that identifies the sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15d4d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="15d4d-115">Parent elements</span></span>

|<span data-ttu-id="15d4d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="15d4d-116">**Element**</span></span>|<span data-ttu-id="15d4d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="15d4d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15d4d-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="15d4d-119">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="15d4d-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-120">Message</span><span class="sxs-lookup"><span data-stu-id="15d4d-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="15d4d-121">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="15d4d-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="15d4d-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="15d4d-123">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="15d4d-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="15d4d-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="15d4d-125">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="15d4d-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="15d4d-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="15d4d-127">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="15d4d-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="15d4d-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="15d4d-129">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="15d4d-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="15d4d-131">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="15d4d-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="15d4d-133">表示暂时接受的会议请求答复。</span><span class="sxs-lookup"><span data-stu-id="15d4d-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="15d4d-135">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="15d4d-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="15d4d-137">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="15d4d-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="15d4d-139">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="15d4d-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="15d4d-141">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="15d4d-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="15d4d-143">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="15d4d-143">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="15d4d-144">PostItem</span><span class="sxs-lookup"><span data-stu-id="15d4d-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="15d4d-145">表示 Exchange 存储中的公告项。</span><span class="sxs-lookup"><span data-stu-id="15d4d-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="15d4d-146">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="15d4d-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15d4d-147">说明</span><span class="sxs-lookup"><span data-stu-id="15d4d-147">Remarks</span></span>

<span data-ttu-id="15d4d-148">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="15d4d-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15d4d-149">元素信息</span><span class="sxs-lookup"><span data-stu-id="15d4d-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15d4d-150">命名空间</span><span class="sxs-lookup"><span data-stu-id="15d4d-150">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15d4d-151">架构名称</span><span class="sxs-lookup"><span data-stu-id="15d4d-151">Schema Name</span></span>  <br/> |<span data-ttu-id="15d4d-152">类型架构</span><span class="sxs-lookup"><span data-stu-id="15d4d-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="15d4d-153">验证文件</span><span class="sxs-lookup"><span data-stu-id="15d4d-153">Validation File</span></span>  <br/> |<span data-ttu-id="15d4d-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="15d4d-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="15d4d-155">可以为空</span><span class="sxs-lookup"><span data-stu-id="15d4d-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="15d4d-156">False</span><span class="sxs-lookup"><span data-stu-id="15d4d-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="15d4d-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15d4d-157">See also</span></span>



- [<span data-ttu-id="15d4d-158">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="15d4d-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

