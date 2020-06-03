---
title: DeclineItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeclineItem
api_type:
- schema
ms.assetid: 2d8d2389-924e-4d03-a324-35d56cf0d6b1
description: DeclineItem 元素表示对会议请求的拒绝答复。
ms.openlocfilehash: a3fb2b62ea2fa895a664034d2150f46a3099f6c1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457429"
---
# <a name="declineitem"></a><span data-ttu-id="3e28e-103">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="3e28e-103">DeclineItem</span></span>

<span data-ttu-id="3e28e-104">**DeclineItem**元素表示对会议请求的拒绝答复。</span><span class="sxs-lookup"><span data-stu-id="3e28e-104">The **DeclineItem** element represents a Decline reply to a meeting request.</span></span> 
  
```xml
<DeclineItem>
   <ItemClass/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <InternetMessageHeaders/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ReferenceItemId/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <ProposedStart/>
   <ProposedEnd/>
</DeclineItem>
```

<span data-ttu-id="3e28e-105">**DeclineItemType**</span><span class="sxs-lookup"><span data-stu-id="3e28e-105">**DeclineItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3e28e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3e28e-106">Attributes and elements</span></span>

<span data-ttu-id="3e28e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3e28e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e28e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3e28e-108">Attributes</span></span>

<span data-ttu-id="3e28e-109">无。</span><span class="sxs-lookup"><span data-stu-id="3e28e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e28e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3e28e-110">Child elements</span></span>

|<span data-ttu-id="3e28e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3e28e-111">**Element**</span></span>|<span data-ttu-id="3e28e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3e28e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e28e-113">ItemClass</span><span class="sxs-lookup"><span data-stu-id="3e28e-113">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="3e28e-114">表示项目的邮件类。</span><span class="sxs-lookup"><span data-stu-id="3e28e-114">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-115">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="3e28e-115">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="3e28e-116">指示项的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="3e28e-116">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-117">Body</span><span class="sxs-lookup"><span data-stu-id="3e28e-117">Body</span></span>](body.md) <br/> |<span data-ttu-id="3e28e-118">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="3e28e-118">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-119">附件</span><span class="sxs-lookup"><span data-stu-id="3e28e-119">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="3e28e-120">包含附加到 Exchange 存储中的项目的项目或文件。</span><span class="sxs-lookup"><span data-stu-id="3e28e-120">Contains the item or file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-121">Message</span><span class="sxs-lookup"><span data-stu-id="3e28e-121">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="3e28e-122">表示标头集合中给定标头的 Internet 邮件头名称。</span><span class="sxs-lookup"><span data-stu-id="3e28e-122">Represents the Internet message header name for a given header within the headers collection.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-123">发件人</span><span class="sxs-lookup"><span data-stu-id="3e28e-123">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="3e28e-124">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="3e28e-124">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-125">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="3e28e-125">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="3e28e-126">包含项目的一组收件人。</span><span class="sxs-lookup"><span data-stu-id="3e28e-126">Contains a set of recipients of an item.</span></span> <span data-ttu-id="3e28e-127">这是一项主要收件人。</span><span class="sxs-lookup"><span data-stu-id="3e28e-127">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-128">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="3e28e-128">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="3e28e-129">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="3e28e-129">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-130">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="3e28e-130">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="3e28e-131">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="3e28e-131">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-132">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="3e28e-132">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="3e28e-133">指示项目的发件人是否请求已读回执。</span><span class="sxs-lookup"><span data-stu-id="3e28e-133">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-134">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="3e28e-134">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="3e28e-135">指示项目的发件人是否请求送达回执。</span><span class="sxs-lookup"><span data-stu-id="3e28e-135">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-136">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="3e28e-136">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="3e28e-137">标识 response 对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="3e28e-137">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-138">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="3e28e-138">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="3e28e-139">标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="3e28e-139">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="3e28e-140">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3e28e-140">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="3e28e-141">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="3e28e-141">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="3e28e-142">标识代理访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="3e28e-142">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="3e28e-143">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3e28e-143">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-144">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="3e28e-144">ProposedStart</span></span>](proposedstart.md) <br/> |<span data-ttu-id="3e28e-145">指定会议的建议开始时间。</span><span class="sxs-lookup"><span data-stu-id="3e28e-145">Specifies the proposed start time of the meeting.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-146">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="3e28e-146">ProposedEnd</span></span>](proposedend.md) <br/> |<span data-ttu-id="3e28e-147">指定会议的建议结束时间。</span><span class="sxs-lookup"><span data-stu-id="3e28e-147">Specifies the proposed end time of the meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3e28e-148">父元素</span><span class="sxs-lookup"><span data-stu-id="3e28e-148">Parent elements</span></span>

|<span data-ttu-id="3e28e-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="3e28e-149">**Element**</span></span>|<span data-ttu-id="3e28e-150">**说明**</span><span class="sxs-lookup"><span data-stu-id="3e28e-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e28e-151">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="3e28e-151">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="3e28e-152">描述与会议时间相邻的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3e28e-152">Describes all items that are adjacent to a meeting time.</span></span><br/><br/><span data-ttu-id="3e28e-153">下面是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="3e28e-153">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="3e28e-154">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="3e28e-154">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="3e28e-155">描述与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="3e28e-155">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="3e28e-156">下面是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="3e28e-156">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="3e28e-157">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="3e28e-157">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="3e28e-158">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="3e28e-158">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="3e28e-159">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="3e28e-159">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="3e28e-160">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="3e28e-160">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e28e-161">备注</span><span class="sxs-lookup"><span data-stu-id="3e28e-161">Remarks</span></span>

<span data-ttu-id="3e28e-162">描述此元素的架构位于安装了客户端访问服务器角色的 Exchange 服务器的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3e28e-162">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e28e-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="3e28e-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e28e-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="3e28e-164">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e28e-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="3e28e-165">Schema Name</span></span>  <br/> |<span data-ttu-id="3e28e-166">类型架构</span><span class="sxs-lookup"><span data-stu-id="3e28e-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="3e28e-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="3e28e-167">Validation File</span></span>  <br/> |<span data-ttu-id="3e28e-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3e28e-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3e28e-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="3e28e-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e28e-170">False</span><span class="sxs-lookup"><span data-stu-id="3e28e-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e28e-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3e28e-171">See also</span></span>

- [<span data-ttu-id="3e28e-172">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3e28e-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

