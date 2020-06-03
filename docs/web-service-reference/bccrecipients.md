---
title: BccRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BccRecipients
api_type:
- schema
ms.assetid: c4e05168-d36b-4740-a526-4b7da53553c1
description: BccRecipients元素表示要接收电子邮件的密件抄送 (Bcc) 的收件人的集合。
ms.openlocfilehash: 96070415c6d92a893f6c560884d9d191c7d5f15b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529502"
---
# <a name="bccrecipients"></a><span data-ttu-id="e6cd2-103">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="e6cd2-103">BccRecipients</span></span>

<span data-ttu-id="e6cd2-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **BccRecipients**元素表示要接收电子邮件的密件抄送 (Bcc) 的收件人的集合。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-104">The **BccRecipients** element represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span> 
  
```xml
<BccRecipients>
   <Mailbox/>
</BccRecipients>
```

 <span data-ttu-id="e6cd2-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="e6cd2-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6cd2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e6cd2-106">Attributes and elements</span></span>

<span data-ttu-id="e6cd2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6cd2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e6cd2-108">Attributes</span></span>

<span data-ttu-id="e6cd2-109">无。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6cd2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e6cd2-110">Child elements</span></span>

|<span data-ttu-id="e6cd2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e6cd2-111">**Element**</span></span>|<span data-ttu-id="e6cd2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6cd2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6cd2-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="e6cd2-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="e6cd2-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6cd2-115">父元素</span><span class="sxs-lookup"><span data-stu-id="e6cd2-115">Parent elements</span></span>

|<span data-ttu-id="e6cd2-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e6cd2-116">**Element**</span></span>|<span data-ttu-id="e6cd2-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6cd2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6cd2-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="e6cd2-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="e6cd2-119">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-120">Message</span><span class="sxs-lookup"><span data-stu-id="e6cd2-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e6cd2-121">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="e6cd2-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="e6cd2-123">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e6cd2-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e6cd2-125">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="e6cd2-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="e6cd2-127">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="e6cd2-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="e6cd2-129">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="e6cd2-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="e6cd2-131">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-131">Represents an accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="e6cd2-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="e6cd2-133">表示暂时接受的会议请求答复。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-133">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="e6cd2-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="e6cd2-135">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-135">Represents a decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="e6cd2-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="e6cd2-137">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="e6cd2-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="e6cd2-139">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="e6cd2-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="e6cd2-141">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="e6cd2-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="e6cd2-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="e6cd2-143">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6cd2-144">备注</span><span class="sxs-lookup"><span data-stu-id="e6cd2-144">Remarks</span></span>

<span data-ttu-id="e6cd2-p101">您无法通过使用 FindItem 请求获取 **BccRecipients** 。使用一个 GetItem 请求来获取 **BccRecipients**。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-p101">You cannot get **BccRecipients** by using a FindItem request. Use a GetItem request to get **BccRecipients**.</span></span>
  
<span data-ttu-id="e6cd2-147">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e6cd2-147">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6cd2-148">元素信息</span><span class="sxs-lookup"><span data-stu-id="e6cd2-148">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6cd2-149">命名空间</span><span class="sxs-lookup"><span data-stu-id="e6cd2-149">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e6cd2-150">架构名称</span><span class="sxs-lookup"><span data-stu-id="e6cd2-150">Schema Name</span></span>  <br/> |<span data-ttu-id="e6cd2-151">类型架构</span><span class="sxs-lookup"><span data-stu-id="e6cd2-151">Types schema</span></span>  <br/> |
|<span data-ttu-id="e6cd2-152">验证文件</span><span class="sxs-lookup"><span data-stu-id="e6cd2-152">Validation File</span></span>  <br/> |<span data-ttu-id="e6cd2-153">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e6cd2-153">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e6cd2-154">可以为空</span><span class="sxs-lookup"><span data-stu-id="e6cd2-154">Can be Empty</span></span>  <br/> |<span data-ttu-id="e6cd2-155">False</span><span class="sxs-lookup"><span data-stu-id="e6cd2-155">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6cd2-156">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6cd2-156">See also</span></span>



- [<span data-ttu-id="e6cd2-157">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e6cd2-157">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

