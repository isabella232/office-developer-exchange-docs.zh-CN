---
title: ReplyToItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReplyToItem
api_type:
- schema
ms.assetid: 35ee751a-41c0-4216-ad8b-78f7ada43a2f
description: ReplyToItem 元素包含对 Exchange 存储中的项目的发件人的回复。
ms.openlocfilehash: 561ddc3b64ad6d2fe0ea3a3583c41faea36a4a5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827120"
---
# <a name="replytoitem"></a><span data-ttu-id="2abe9-103">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="2abe9-103">ReplyToItem</span></span>

<span data-ttu-id="2abe9-104">**ReplyToItem**元素包含对 Exchange 存储中的项目的发件人的回复。</span><span class="sxs-lookup"><span data-stu-id="2abe9-104">The **ReplyToItem** element contains a reply to the sender of an item in the Exchange store.</span></span> 
  
```xml
<ReplyToItem>
   <Subject/>
   <Body/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <From/>
   <ReferenceItemId/>
   <NewBodyContent/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</ReplyToItem>
```

<span data-ttu-id="2abe9-105">**ReplyToItemType**</span><span class="sxs-lookup"><span data-stu-id="2abe9-105">**ReplyToItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="2abe9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2abe9-106">Attributes and elements</span></span>

<span data-ttu-id="2abe9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2abe9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2abe9-108">属性</span><span class="sxs-lookup"><span data-stu-id="2abe9-108">Attributes</span></span>

<span data-ttu-id="2abe9-109">无。</span><span class="sxs-lookup"><span data-stu-id="2abe9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2abe9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2abe9-110">Child elements</span></span>

|<span data-ttu-id="2abe9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2abe9-111">**Element**</span></span>|<span data-ttu-id="2abe9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2abe9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2abe9-113">Subject</span><span class="sxs-lookup"><span data-stu-id="2abe9-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="2abe9-114">代表 Exchange 存储项目的 subject 属性。</span><span class="sxs-lookup"><span data-stu-id="2abe9-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-115">Body</span><span class="sxs-lookup"><span data-stu-id="2abe9-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="2abe9-116">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="2abe9-116">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-117">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="2abe9-117">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="2abe9-118">包含项目的收件人数组。</span><span class="sxs-lookup"><span data-stu-id="2abe9-118">Contains an array of recipients of an item.</span></span> <span data-ttu-id="2abe9-119">这是一项主要收件人。</span><span class="sxs-lookup"><span data-stu-id="2abe9-119">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-120">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="2abe9-120">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="2abe9-121">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="2abe9-121">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-122">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="2abe9-122">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="2abe9-123">表示要接收的电子邮件的密件抄送 (Bcc) 收件人的集合。</span><span class="sxs-lookup"><span data-stu-id="2abe9-123">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-124">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="2abe9-124">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="2abe9-125">指示项目的发件人是否请求已读的回执。</span><span class="sxs-lookup"><span data-stu-id="2abe9-125">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-126">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="2abe9-126">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="2abe9-127">指示项目的发件人是否请求回执。</span><span class="sxs-lookup"><span data-stu-id="2abe9-127">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-128">发件人</span><span class="sxs-lookup"><span data-stu-id="2abe9-128">From</span></span>](from.md) <br/> |<span data-ttu-id="2abe9-129">代表从中发送邮件的地址。</span><span class="sxs-lookup"><span data-stu-id="2abe9-129">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-130">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="2abe9-130">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="2abe9-131">标识响应对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="2abe9-131">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-132">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="2abe9-132">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="2abe9-133">表示一条消息的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="2abe9-133">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-134">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="2abe9-134">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="2abe9-135">标识委派访问方案中的委托。</span><span class="sxs-lookup"><span data-stu-id="2abe9-135">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="2abe9-136">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2abe9-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="2abe9-137">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="2abe9-137">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="2abe9-138">标识委派访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="2abe9-138">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="2abe9-139">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2abe9-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2abe9-140">父元素</span><span class="sxs-lookup"><span data-stu-id="2abe9-140">Parent elements</span></span>

|<span data-ttu-id="2abe9-141">**元素**</span><span class="sxs-lookup"><span data-stu-id="2abe9-141">**Element**</span></span>|<span data-ttu-id="2abe9-142">**说明**</span><span class="sxs-lookup"><span data-stu-id="2abe9-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2abe9-143">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="2abe9-143">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="2abe9-144">介绍彼此相邻的会议时间的所有项目。</span><span class="sxs-lookup"><span data-stu-id="2abe9-144">Describes all items that are adjacent to a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="2abe9-145">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="2abe9-145">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="2abe9-146">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="2abe9-146">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="2abe9-147">介绍与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="2abe9-147">Describes all items that conflict with a meeting time.</span></span> <br/> <br/>  <span data-ttu-id="2abe9-148">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="2abe9-148">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="2abe9-149">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="2abe9-149">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="2abe9-150">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="2abe9-150">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2abe9-151">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="2abe9-151">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="2abe9-152">包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="2abe9-152">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2abe9-153">备注</span><span class="sxs-lookup"><span data-stu-id="2abe9-153">Remarks</span></span>

<span data-ttu-id="2abe9-154">[从](from.md)元素应设置为主体的电子邮件地址回复项是否由代理。</span><span class="sxs-lookup"><span data-stu-id="2abe9-154">The [From](from.md) element should be set to the e-mail address of the principal if an item is a reply by a delegate.</span></span> <span data-ttu-id="2abe9-155">如果代理不会设置[From](from.md)属性，将显示项目已发送直接从代理人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="2abe9-155">If the delegate does not set the [From](from.md) property, the item will appear to have been sent directly from the delegate's mailbox.</span></span> 
  
<span data-ttu-id="2abe9-156">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2abe9-156">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2abe9-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="2abe9-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2abe9-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="2abe9-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2abe9-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="2abe9-159">Schema Name</span></span>  <br/> |<span data-ttu-id="2abe9-160">类型架构</span><span class="sxs-lookup"><span data-stu-id="2abe9-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="2abe9-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="2abe9-161">Validation File</span></span>  <br/> |<span data-ttu-id="2abe9-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2abe9-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2abe9-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="2abe9-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="2abe9-164">False</span><span class="sxs-lookup"><span data-stu-id="2abe9-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2abe9-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2abe9-165">See also</span></span>

- [<span data-ttu-id="2abe9-166">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2abe9-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

