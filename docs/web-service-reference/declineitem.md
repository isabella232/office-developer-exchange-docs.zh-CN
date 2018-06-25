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
description: DeclineItem 元素均表示拒绝答复会议请求。
ms.openlocfilehash: d7076708248bf1ddc0472b802e4de94a436dcde8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753777"
---
# <a name="declineitem"></a><span data-ttu-id="0969f-103">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="0969f-103">DeclineItem</span></span>

<span data-ttu-id="0969f-104">**DeclineItem**元素均表示拒绝答复会议请求。</span><span class="sxs-lookup"><span data-stu-id="0969f-104">The **DeclineItem** element represents a Decline reply to a meeting request.</span></span> 
  
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

<span data-ttu-id="0969f-105">**DeclineItemType**</span><span class="sxs-lookup"><span data-stu-id="0969f-105">**DeclineItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0969f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0969f-106">Attributes and elements</span></span>

<span data-ttu-id="0969f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0969f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0969f-108">属性</span><span class="sxs-lookup"><span data-stu-id="0969f-108">Attributes</span></span>

<span data-ttu-id="0969f-109">无。</span><span class="sxs-lookup"><span data-stu-id="0969f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0969f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0969f-110">Child elements</span></span>

|<span data-ttu-id="0969f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0969f-111">**Element**</span></span>|<span data-ttu-id="0969f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0969f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0969f-113">ItemClass</span><span class="sxs-lookup"><span data-stu-id="0969f-113">ItemClass</span></span>](itemclass.md) <br/> |<span data-ttu-id="0969f-114">表示项目的消息类。</span><span class="sxs-lookup"><span data-stu-id="0969f-114">Represents the message class of an item.</span></span>  <br/> |
|[<span data-ttu-id="0969f-115">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="0969f-115">Sensitivity</span></span>](sensitivity.md) <br/> |<span data-ttu-id="0969f-116">指示项目的敏感度级别。</span><span class="sxs-lookup"><span data-stu-id="0969f-116">Indicates the sensitivity level of an item.</span></span>  <br/> |
|[<span data-ttu-id="0969f-117">Body</span><span class="sxs-lookup"><span data-stu-id="0969f-117">Body</span></span>](body.md) <br/> |<span data-ttu-id="0969f-118">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="0969f-118">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="0969f-119">附件</span><span class="sxs-lookup"><span data-stu-id="0969f-119">Attachments</span></span>](attachments-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0969f-120">包含的项目或附加到 Exchange 存储中的项的文件。</span><span class="sxs-lookup"><span data-stu-id="0969f-120">Contains the item or file that is attached to an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0969f-121">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="0969f-121">InternetMessageHeaders</span></span>](internetmessageheaders.md) <br/> |<span data-ttu-id="0969f-122">表示给定标题的标头集合中的 Internet 消息标头名称。</span><span class="sxs-lookup"><span data-stu-id="0969f-122">Represents the Internet message header name for a given header within the headers collection.</span></span>  <br/> |
|[<span data-ttu-id="0969f-123">发件人</span><span class="sxs-lookup"><span data-stu-id="0969f-123">Sender</span></span>](sender.md) <br/> |<span data-ttu-id="0969f-124">标识项目的发件人。</span><span class="sxs-lookup"><span data-stu-id="0969f-124">Identifies the sender of an item.</span></span>  <br/> |
|[<span data-ttu-id="0969f-125">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="0969f-125">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="0969f-126">包含一组项目的收件人。</span><span class="sxs-lookup"><span data-stu-id="0969f-126">Contains a set of recipients of an item.</span></span> <span data-ttu-id="0969f-127">这是一项主要收件人。</span><span class="sxs-lookup"><span data-stu-id="0969f-127">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="0969f-128">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="0969f-128">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="0969f-129">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="0969f-129">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="0969f-130">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="0969f-130">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="0969f-131">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="0969f-131">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="0969f-132">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="0969f-132">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="0969f-133">指示项目的发件人是否请求已读的回执。</span><span class="sxs-lookup"><span data-stu-id="0969f-133">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="0969f-134">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="0969f-134">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="0969f-135">指示项目的发件人是否请求回执。</span><span class="sxs-lookup"><span data-stu-id="0969f-135">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="0969f-136">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="0969f-136">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="0969f-137">标识响应对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="0969f-137">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="0969f-138">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="0969f-138">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="0969f-139">标识委派访问方案中的委托。</span><span class="sxs-lookup"><span data-stu-id="0969f-139">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="0969f-140">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0969f-140">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="0969f-141">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="0969f-141">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="0969f-142">标识委派访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="0969f-142">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="0969f-143">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0969f-143">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="0969f-144">ProposedStart</span><span class="sxs-lookup"><span data-stu-id="0969f-144">ProposedStart</span></span>](proposedstart.md) <br/> |<span data-ttu-id="0969f-145">指定会议建议的开始的时间。</span><span class="sxs-lookup"><span data-stu-id="0969f-145">Specifies the proposed start time of the meeting.</span></span>  <br/> |
|[<span data-ttu-id="0969f-146">ProposedEnd</span><span class="sxs-lookup"><span data-stu-id="0969f-146">ProposedEnd</span></span>](proposedend.md) <br/> |<span data-ttu-id="0969f-147">指定会议建议的结束时间。</span><span class="sxs-lookup"><span data-stu-id="0969f-147">Specifies the proposed end time of the meeting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0969f-148">父元素</span><span class="sxs-lookup"><span data-stu-id="0969f-148">Parent elements</span></span>

|<span data-ttu-id="0969f-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="0969f-149">**Element**</span></span>|<span data-ttu-id="0969f-150">**说明**</span><span class="sxs-lookup"><span data-stu-id="0969f-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0969f-151">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="0969f-151">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="0969f-152">介绍彼此相邻的会议时间的所有项目。</span><span class="sxs-lookup"><span data-stu-id="0969f-152">Describes all items that are adjacent to a meeting time.</span></span><br/><br/><span data-ttu-id="0969f-153">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="0969f-153">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="0969f-154">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="0969f-154">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="0969f-155">介绍与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="0969f-155">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="0969f-156">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="0969f-156">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="0969f-157">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="0969f-157">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="0969f-158">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="0969f-158">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="0969f-159">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="0969f-159">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="0969f-160">包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="0969f-160">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0969f-161">注解</span><span class="sxs-lookup"><span data-stu-id="0969f-161">Remarks</span></span>

<span data-ttu-id="0969f-162">描述此元素的架构位于 Exchange 服务器已安装了客户端访问服务器角色的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0969f-162">The schema that describes this element is located in the EWS virtual directory of the Exchange server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0969f-163">元素信息</span><span class="sxs-lookup"><span data-stu-id="0969f-163">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0969f-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="0969f-164">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0969f-165">架构名称</span><span class="sxs-lookup"><span data-stu-id="0969f-165">Schema Name</span></span>  <br/> |<span data-ttu-id="0969f-166">类型架构</span><span class="sxs-lookup"><span data-stu-id="0969f-166">Types schema</span></span>  <br/> |
|<span data-ttu-id="0969f-167">验证文件</span><span class="sxs-lookup"><span data-stu-id="0969f-167">Validation File</span></span>  <br/> |<span data-ttu-id="0969f-168">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0969f-168">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0969f-169">可以为空</span><span class="sxs-lookup"><span data-stu-id="0969f-169">Can be Empty</span></span>  <br/> |<span data-ttu-id="0969f-170">False</span><span class="sxs-lookup"><span data-stu-id="0969f-170">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0969f-171">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0969f-171">See also</span></span>

- [<span data-ttu-id="0969f-172">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0969f-172">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

