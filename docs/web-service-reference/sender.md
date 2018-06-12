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
description: 发件人元素标识的项目的发件人。
ms.openlocfilehash: a7b06543fadd7cf7ae05f7ae8f86122138e11076
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827323"
---
# <a name="sender"></a><span data-ttu-id="3bed2-103">发件人</span><span class="sxs-lookup"><span data-stu-id="3bed2-103">Sender</span></span>

<span data-ttu-id="3bed2-104">**发件人**元素标识的项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="3bed2-104">The **Sender** element identifies the sender of an item.</span></span> 
  
```xml
<Sender>
   <Mailbox/>
</Sender>
```

 <span data-ttu-id="3bed2-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="3bed2-105">**SingleRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3bed2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3bed2-106">Attributes and elements</span></span>

<span data-ttu-id="3bed2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3bed2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3bed2-108">属性</span><span class="sxs-lookup"><span data-stu-id="3bed2-108">Attributes</span></span>

<span data-ttu-id="3bed2-109">无。</span><span class="sxs-lookup"><span data-stu-id="3bed2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3bed2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3bed2-110">Child elements</span></span>

|<span data-ttu-id="3bed2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3bed2-111">**Element**</span></span>|<span data-ttu-id="3bed2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3bed2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bed2-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="3bed2-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="3bed2-114">标识标识发件人的邮件启用 Active Directory 对象。</span><span class="sxs-lookup"><span data-stu-id="3bed2-114">Identifies a mail enabled Active Directory object that identifies the sender.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3bed2-115">父元素</span><span class="sxs-lookup"><span data-stu-id="3bed2-115">Parent elements</span></span>

|<span data-ttu-id="3bed2-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="3bed2-116">**Element**</span></span>|<span data-ttu-id="3bed2-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="3bed2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3bed2-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="3bed2-119">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="3bed2-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-120">Message</span><span class="sxs-lookup"><span data-stu-id="3bed2-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3bed2-121">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="3bed2-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="3bed2-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="3bed2-123">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="3bed2-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="3bed2-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="3bed2-125">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="3bed2-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="3bed2-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="3bed2-127">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="3bed2-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="3bed2-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="3bed2-129">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="3bed2-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="3bed2-131">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="3bed2-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="3bed2-133">表示暂时接受的会议请求答复。</span><span class="sxs-lookup"><span data-stu-id="3bed2-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="3bed2-135">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="3bed2-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="3bed2-137">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="3bed2-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="3bed2-139">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="3bed2-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="3bed2-141">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="3bed2-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="3bed2-143">代表用来取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="3bed2-143">Represents the response object used to cancel a meeting.</span></span>  <br/> |
|[<span data-ttu-id="3bed2-144">PostItem</span><span class="sxs-lookup"><span data-stu-id="3bed2-144">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="3bed2-145">代表一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="3bed2-145">Represents a post item in the Exchange store.</span></span> <span data-ttu-id="3bed2-146">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3bed2-146">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bed2-147">备注</span><span class="sxs-lookup"><span data-stu-id="3bed2-147">Remarks</span></span>

<span data-ttu-id="3bed2-148">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3bed2-148">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3bed2-149">元素信息</span><span class="sxs-lookup"><span data-stu-id="3bed2-149">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bed2-150">命名空间</span><span class="sxs-lookup"><span data-stu-id="3bed2-150">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3bed2-151">架构名称</span><span class="sxs-lookup"><span data-stu-id="3bed2-151">Schema Name</span></span>  <br/> |<span data-ttu-id="3bed2-152">类型架构</span><span class="sxs-lookup"><span data-stu-id="3bed2-152">Types schema</span></span>  <br/> |
|<span data-ttu-id="3bed2-153">验证文件</span><span class="sxs-lookup"><span data-stu-id="3bed2-153">Validation File</span></span>  <br/> |<span data-ttu-id="3bed2-154">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3bed2-154">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3bed2-155">可以为空</span><span class="sxs-lookup"><span data-stu-id="3bed2-155">Can be Empty</span></span>  <br/> |<span data-ttu-id="3bed2-156">False</span><span class="sxs-lookup"><span data-stu-id="3bed2-156">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3bed2-157">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3bed2-157">See also</span></span>



- [<span data-ttu-id="3bed2-158">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3bed2-158">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

