---
title: 回复
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyTo
api_type:
- schema
ms.assetid: 6b6ae792-e2c4-4aa0-95cb-b49b446f1e08
description: 回复元素标识数组答复应发送到的地址。
ms.openlocfilehash: 0ceb4f5edb75bbfe52a7a7156da3c2a328bea346
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827115"
---
# <a name="replyto"></a><span data-ttu-id="30066-103">回复</span><span class="sxs-lookup"><span data-stu-id="30066-103">ReplyTo</span></span>

<span data-ttu-id="30066-104">**回复**元素标识数组答复应发送到的地址。</span><span class="sxs-lookup"><span data-stu-id="30066-104">The **ReplyTo** element identifies an array of addresses to which replies should be sent.</span></span> 
  
```xml
<ReplyTo>
   <Mailbox/>
</ReplyTo>
```

 <span data-ttu-id="30066-105">**ArrayOfRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="30066-105">**ArrayOfRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30066-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="30066-106">Attributes and elements</span></span>

<span data-ttu-id="30066-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="30066-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30066-108">属性</span><span class="sxs-lookup"><span data-stu-id="30066-108">Attributes</span></span>

<span data-ttu-id="30066-109">无。</span><span class="sxs-lookup"><span data-stu-id="30066-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30066-110">子元素</span><span class="sxs-lookup"><span data-stu-id="30066-110">Child elements</span></span>

|<span data-ttu-id="30066-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="30066-111">**Element**</span></span>|<span data-ttu-id="30066-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="30066-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30066-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="30066-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="30066-114">标识已启用邮件的 Active Directory 目录服务对象向其发送答复。</span><span class="sxs-lookup"><span data-stu-id="30066-114">Identifies a mail-enabled Active Directory directory service object to which a reply is sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="30066-115">父元素</span><span class="sxs-lookup"><span data-stu-id="30066-115">Parent elements</span></span>

|<span data-ttu-id="30066-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="30066-116">**Element**</span></span>|<span data-ttu-id="30066-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="30066-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30066-118">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="30066-118">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="30066-119">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="30066-119">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="30066-120">Message</span><span class="sxs-lookup"><span data-stu-id="30066-120">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="30066-121">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="30066-121">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="30066-122">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="30066-122">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="30066-123">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="30066-123">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="30066-124">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="30066-124">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="30066-125">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="30066-125">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="30066-126">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="30066-126">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="30066-127">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="30066-127">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="30066-128">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="30066-128">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="30066-129">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="30066-129">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="30066-130">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="30066-130">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="30066-131">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="30066-131">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="30066-132">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="30066-132">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="30066-133">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="30066-133">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="30066-134">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="30066-134">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="30066-135">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="30066-135">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="30066-136">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="30066-136">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="30066-137">包含对 Exchange 存储中的项的创建者的答复。</span><span class="sxs-lookup"><span data-stu-id="30066-137">Contains a reply to the creator of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="30066-138">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="30066-138">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="30066-139">包含对所有确定收件人的 Exchange 存储中的项的答复。</span><span class="sxs-lookup"><span data-stu-id="30066-139">Contains a reply to all identified recipients of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="30066-140">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="30066-140">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="30066-141">包含要转发给收件人的 Exchange 存储区项。</span><span class="sxs-lookup"><span data-stu-id="30066-141">Contains an Exchange store item to forward to recipients.</span></span>  <br/> |
|[<span data-ttu-id="30066-142">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="30066-142">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="30066-143">表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="30066-143">Represents the response object that is used to cancel a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30066-144">备注</span><span class="sxs-lookup"><span data-stu-id="30066-144">Remarks</span></span>

<span data-ttu-id="30066-145">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="30066-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30066-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="30066-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30066-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="30066-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="30066-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="30066-148">Schema Name</span></span>  <br/> |<span data-ttu-id="30066-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="30066-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="30066-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="30066-150">Validation File</span></span>  <br/> |<span data-ttu-id="30066-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="30066-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="30066-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="30066-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="30066-153">False</span><span class="sxs-lookup"><span data-stu-id="30066-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30066-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="30066-154">See also</span></span>



- [<span data-ttu-id="30066-155">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="30066-155">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

