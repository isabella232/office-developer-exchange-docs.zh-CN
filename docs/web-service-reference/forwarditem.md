---
title: ForwardItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardItem
api_type:
- schema
ms.assetid: 97786086-8b91-4471-8af8-d21e8d66de87
description: ForwardItem 元素包含要转发给收件人的 Exchange 存储项。
ms.openlocfilehash: dcc9a3eb2bf1cdd80680ef9142d22f5281437922
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461315"
---
# <a name="forwarditem"></a><span data-ttu-id="8862d-103">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="8862d-103">ForwardItem</span></span>

<span data-ttu-id="8862d-104">**ForwardItem**元素包含要转发给收件人的 Exchange 存储项。</span><span class="sxs-lookup"><span data-stu-id="8862d-104">The **ForwardItem** element contains an Exchange store item to forward to recipients.</span></span> 
  
```xml
<ForwardItem>
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
</ForwardItem>
```

<span data-ttu-id="8862d-105">**ForwardItemType**</span><span class="sxs-lookup"><span data-stu-id="8862d-105">**ForwardItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8862d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8862d-106">Attributes and elements</span></span>

<span data-ttu-id="8862d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8862d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8862d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8862d-108">Attributes</span></span>

<span data-ttu-id="8862d-109">无。</span><span class="sxs-lookup"><span data-stu-id="8862d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8862d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8862d-110">Child elements</span></span>

|<span data-ttu-id="8862d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8862d-111">**Element**</span></span>|<span data-ttu-id="8862d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8862d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8862d-113">主题</span><span class="sxs-lookup"><span data-stu-id="8862d-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="8862d-114">表示 Exchange 存储项的 subject 属性。</span><span class="sxs-lookup"><span data-stu-id="8862d-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="8862d-115">Body</span><span class="sxs-lookup"><span data-stu-id="8862d-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="8862d-116">表示邮件的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="8862d-116">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="8862d-117">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="8862d-117">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="8862d-118">包含项目的一组收件人。</span><span class="sxs-lookup"><span data-stu-id="8862d-118">Contains a set of recipients of an item.</span></span> <span data-ttu-id="8862d-119">这是一项主要收件人。</span><span class="sxs-lookup"><span data-stu-id="8862d-119">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="8862d-120">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="8862d-120">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="8862d-121">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="8862d-121">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="8862d-122">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="8862d-122">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="8862d-123">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="8862d-123">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="8862d-124">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="8862d-124">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="8862d-125">指示项目的发件人是否请求已读回执。</span><span class="sxs-lookup"><span data-stu-id="8862d-125">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="8862d-126">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="8862d-126">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="8862d-127">指示项目的发件人是否请求送达回执。</span><span class="sxs-lookup"><span data-stu-id="8862d-127">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="8862d-128">From</span><span class="sxs-lookup"><span data-stu-id="8862d-128">From</span></span>](from.md) <br/> |<span data-ttu-id="8862d-129">表示发送邮件的地址。</span><span class="sxs-lookup"><span data-stu-id="8862d-129">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="8862d-130">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="8862d-130">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="8862d-131">标识 response 对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="8862d-131">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="8862d-132">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="8862d-132">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="8862d-133">表示邮件的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="8862d-133">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="8862d-134">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="8862d-134">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="8862d-135">标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="8862d-135">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="8862d-136">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8862d-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="8862d-137">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="8862d-137">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="8862d-138">标识代理访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="8862d-138">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="8862d-139">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8862d-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8862d-140">父元素</span><span class="sxs-lookup"><span data-stu-id="8862d-140">Parent elements</span></span>

|<span data-ttu-id="8862d-141">**元素**</span><span class="sxs-lookup"><span data-stu-id="8862d-141">**Element**</span></span>|<span data-ttu-id="8862d-142">**说明**</span><span class="sxs-lookup"><span data-stu-id="8862d-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8862d-143">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="8862d-143">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="8862d-144">描述与会议时间相邻的所有项目。</span><span class="sxs-lookup"><span data-stu-id="8862d-144">Describes all items that are adjacent to a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="8862d-145">下面是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="8862d-145">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="8862d-146">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="8862d-146">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="8862d-147">描述与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="8862d-147">Describes all items that conflict with a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="8862d-148">下面是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="8862d-148">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="8862d-149">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="8862d-149">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="8862d-150">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="8862d-150">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="8862d-151">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="8862d-151">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="8862d-152">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="8862d-152">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8862d-153">备注</span><span class="sxs-lookup"><span data-stu-id="8862d-153">Remarks</span></span>

<span data-ttu-id="8862d-154">如果某个项目由代理人转发，则应将[From](from.md)元素设置为主体的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="8862d-154">The [From](from.md) element should be set to the e-mail address of the principal if an item is forwarded by a delegate.</span></span> <span data-ttu-id="8862d-155">如果代理未设置[From](from.md)属性，则该项目将显示为直接从代理的邮箱发送。</span><span class="sxs-lookup"><span data-stu-id="8862d-155">If the delegate does not set the [From](from.md) property, the item will appear to have been sent directly from the delegate's mailbox.</span></span> 
  
<span data-ttu-id="8862d-156">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8862d-156">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8862d-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="8862d-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8862d-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="8862d-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8862d-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="8862d-159">Schema Name</span></span>  <br/> |<span data-ttu-id="8862d-160">类型架构</span><span class="sxs-lookup"><span data-stu-id="8862d-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="8862d-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="8862d-161">Validation File</span></span>  <br/> |<span data-ttu-id="8862d-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8862d-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8862d-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="8862d-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="8862d-164">False</span><span class="sxs-lookup"><span data-stu-id="8862d-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8862d-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8862d-165">See also</span></span>

- [<span data-ttu-id="8862d-166">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8862d-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

