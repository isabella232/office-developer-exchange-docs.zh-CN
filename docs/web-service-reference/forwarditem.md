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
description: ForwardItem 元素包含一个 Exchange 存储项目，以将转发给收件人。
ms.openlocfilehash: 8a82ff28ad1d0dc965a3284c1d0eac9b2fa38301
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754410"
---
# <a name="forwarditem"></a><span data-ttu-id="572b7-103">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="572b7-103">ForwardItem</span></span>

<span data-ttu-id="572b7-104">**ForwardItem**元素包含一个 Exchange 存储项目，以将转发给收件人。</span><span class="sxs-lookup"><span data-stu-id="572b7-104">The **ForwardItem** element contains an Exchange store item to forward to recipients.</span></span> 
  
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

<span data-ttu-id="572b7-105">**ForwardItemType**</span><span class="sxs-lookup"><span data-stu-id="572b7-105">**ForwardItemType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="572b7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="572b7-106">Attributes and elements</span></span>

<span data-ttu-id="572b7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="572b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="572b7-108">属性</span><span class="sxs-lookup"><span data-stu-id="572b7-108">Attributes</span></span>

<span data-ttu-id="572b7-109">无。</span><span class="sxs-lookup"><span data-stu-id="572b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="572b7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="572b7-110">Child elements</span></span>

|<span data-ttu-id="572b7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="572b7-111">**Element**</span></span>|<span data-ttu-id="572b7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="572b7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="572b7-113">Subject</span><span class="sxs-lookup"><span data-stu-id="572b7-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="572b7-114">代表 Exchange 存储项目的 subject 属性。</span><span class="sxs-lookup"><span data-stu-id="572b7-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="572b7-115">Body</span><span class="sxs-lookup"><span data-stu-id="572b7-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="572b7-116">表示一条消息的实际正文内容。</span><span class="sxs-lookup"><span data-stu-id="572b7-116">Represents the actual body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="572b7-117">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="572b7-117">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="572b7-118">包含一组项目的收件人。</span><span class="sxs-lookup"><span data-stu-id="572b7-118">Contains a set of recipients of an item.</span></span> <span data-ttu-id="572b7-119">这是一项主要收件人。</span><span class="sxs-lookup"><span data-stu-id="572b7-119">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="572b7-120">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="572b7-120">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="572b7-121">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="572b7-121">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="572b7-122">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="572b7-122">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="572b7-123">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="572b7-123">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="572b7-124">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="572b7-124">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="572b7-125">指示项目的发件人是否请求已读的回执。</span><span class="sxs-lookup"><span data-stu-id="572b7-125">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="572b7-126">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="572b7-126">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="572b7-127">指示项目的发件人是否请求回执。</span><span class="sxs-lookup"><span data-stu-id="572b7-127">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="572b7-128">发件人</span><span class="sxs-lookup"><span data-stu-id="572b7-128">From</span></span>](from.md) <br/> |<span data-ttu-id="572b7-129">代表从中发送邮件的地址。</span><span class="sxs-lookup"><span data-stu-id="572b7-129">Represents the address from which the message was sent.</span></span>  <br/> |
|[<span data-ttu-id="572b7-130">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="572b7-130">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="572b7-131">标识响应对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="572b7-131">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="572b7-132">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="572b7-132">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="572b7-133">表示一条消息的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="572b7-133">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="572b7-134">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="572b7-134">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="572b7-135">标识委派访问方案中的委托。</span><span class="sxs-lookup"><span data-stu-id="572b7-135">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="572b7-136">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="572b7-136">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="572b7-137">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="572b7-137">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="572b7-138">标识委派访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="572b7-138">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="572b7-139">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="572b7-139">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="572b7-140">父元素</span><span class="sxs-lookup"><span data-stu-id="572b7-140">Parent elements</span></span>

|<span data-ttu-id="572b7-141">**元素**</span><span class="sxs-lookup"><span data-stu-id="572b7-141">**Element**</span></span>|<span data-ttu-id="572b7-142">**说明**</span><span class="sxs-lookup"><span data-stu-id="572b7-142">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="572b7-143">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="572b7-143">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="572b7-144">介绍彼此相邻的会议时间的所有项目。</span><span class="sxs-lookup"><span data-stu-id="572b7-144">Describes all items that are adjacent to a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="572b7-145">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="572b7-145">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="572b7-146">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="572b7-146">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="572b7-147">介绍与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="572b7-147">Describes all items that conflict with a meeting time.</span></span>  <br/><br/>  <span data-ttu-id="572b7-148">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="572b7-148">The following are some of the XPath expressions to this element:</span></span> <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="572b7-149">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="572b7-149">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="572b7-150">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="572b7-150">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="572b7-151">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="572b7-151">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="572b7-152">包含由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="572b7-152">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="572b7-153">备注</span><span class="sxs-lookup"><span data-stu-id="572b7-153">Remarks</span></span>

<span data-ttu-id="572b7-154">[从](from.md)元素应设置为主体的电子邮件地址，如果由代理人转发项目。</span><span class="sxs-lookup"><span data-stu-id="572b7-154">The [From](from.md) element should be set to the e-mail address of the principal if an item is forwarded by a delegate.</span></span> <span data-ttu-id="572b7-155">如果代理不会设置[From](from.md)属性，将显示项目已发送直接从代理人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="572b7-155">If the delegate does not set the [From](from.md) property, the item will appear to have been sent directly from the delegate's mailbox.</span></span> 
  
<span data-ttu-id="572b7-156">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="572b7-156">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="572b7-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="572b7-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="572b7-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="572b7-158">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="572b7-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="572b7-159">Schema Name</span></span>  <br/> |<span data-ttu-id="572b7-160">类型架构</span><span class="sxs-lookup"><span data-stu-id="572b7-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="572b7-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="572b7-161">Validation File</span></span>  <br/> |<span data-ttu-id="572b7-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="572b7-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="572b7-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="572b7-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="572b7-164">False</span><span class="sxs-lookup"><span data-stu-id="572b7-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="572b7-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="572b7-165">See also</span></span>

- [<span data-ttu-id="572b7-166">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="572b7-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

