---
title: CancelCalendarItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CancelCalendarItem
api_type:
- schema
ms.assetid: a2046402-a176-44d5-b4b3-adb696581935
description: CancelCalendarItem 元素表示用于取消会议响应对象。
ms.openlocfilehash: 262f60db33abac36156b069dc85e1fccb3522d5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753432"
---
# <a name="cancelcalendaritem"></a><span data-ttu-id="83594-103">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="83594-103">CancelCalendarItem</span></span>

<span data-ttu-id="83594-104">**CancelCalendarItem**元素表示用于取消会议响应对象。</span><span class="sxs-lookup"><span data-stu-id="83594-104">The **CancelCalendarItem** element represents the response object that is used to cancel a meeting.</span></span> 
  
```xml
<CancelCalendarItem>
   <Subject/>
   <Body/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ReferenceItemId/>
   <NewBodyContent/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</CancelCalendarItem>
```

 <span data-ttu-id="83594-105">**CancelCalendarItemType**</span><span class="sxs-lookup"><span data-stu-id="83594-105">**CancelCalendarItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="83594-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="83594-106">Attributes and elements</span></span>

<span data-ttu-id="83594-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="83594-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="83594-108">属性</span><span class="sxs-lookup"><span data-stu-id="83594-108">Attributes</span></span>

<span data-ttu-id="83594-109">无。</span><span class="sxs-lookup"><span data-stu-id="83594-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83594-110">子元素</span><span class="sxs-lookup"><span data-stu-id="83594-110">Child elements</span></span>

|<span data-ttu-id="83594-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="83594-111">**Element**</span></span>|<span data-ttu-id="83594-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="83594-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83594-113">Subject</span><span class="sxs-lookup"><span data-stu-id="83594-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="83594-114">代表 Exchange 存储项目的 subject 属性。</span><span class="sxs-lookup"><span data-stu-id="83594-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="83594-115">Body</span><span class="sxs-lookup"><span data-stu-id="83594-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="83594-116">不使用**CancelCalendarItem**。</span><span class="sxs-lookup"><span data-stu-id="83594-116">Not used by **CancelCalendarItem**.</span></span> <span data-ttu-id="83594-117">使用[NewBodyContent](newbodycontent.md)属性设置的正文内容。</span><span class="sxs-lookup"><span data-stu-id="83594-117">Use the [NewBodyContent](newbodycontent.md) property to set the body content.</span></span>  <br/> |
|[<span data-ttu-id="83594-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="83594-118">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="83594-119">包含一组项目的收件人。</span><span class="sxs-lookup"><span data-stu-id="83594-119">Contains a set of recipients of an item.</span></span> <span data-ttu-id="83594-120">这是一项主要收件人。</span><span class="sxs-lookup"><span data-stu-id="83594-120">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="83594-121">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="83594-121">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="83594-122">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="83594-122">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="83594-123">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="83594-123">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="83594-124">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="83594-124">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="83594-125">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="83594-125">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="83594-126">指示项目的发件人是否请求已读的回执。</span><span class="sxs-lookup"><span data-stu-id="83594-126">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="83594-127">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="83594-127">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="83594-128">指示项目的发件人是否请求回执。</span><span class="sxs-lookup"><span data-stu-id="83594-128">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="83594-129">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="83594-129">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="83594-130">标识响应对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="83594-130">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="83594-131">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="83594-131">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="83594-132">表示一条消息的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="83594-132">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="83594-133">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="83594-133">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="83594-134">标识委派访问方案中的委托。</span><span class="sxs-lookup"><span data-stu-id="83594-134">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="83594-135">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="83594-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="83594-136">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="83594-136">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="83594-137">标识委派访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="83594-137">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="83594-138">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="83594-138">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="83594-139">父元素</span><span class="sxs-lookup"><span data-stu-id="83594-139">Parent elements</span></span>

|<span data-ttu-id="83594-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="83594-140">**Element**</span></span>|<span data-ttu-id="83594-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="83594-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="83594-142">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="83594-142">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="83594-143">介绍彼此相邻的会议时间的所有项目。</span><span class="sxs-lookup"><span data-stu-id="83594-143">Describes all items that are adjacent to a meeting time.</span></span><br/><br/> <span data-ttu-id="83594-144">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="83594-144">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="83594-145">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="83594-145">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="83594-146">介绍与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="83594-146">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="83594-147">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="83594-147">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="83594-148">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="83594-148">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="83594-149">包含与 Exchange 存储中的项相关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="83594-149">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="83594-150">项目 (NonEmptyArrayOfAllItemsType)</span><span class="sxs-lookup"><span data-stu-id="83594-150">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="83594-151">包含在由[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="83594-151">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83594-152">注解</span><span class="sxs-lookup"><span data-stu-id="83594-152">Remarks</span></span>

<span data-ttu-id="83594-153">由组织者仅查看**CancelCalendarItem**元素。</span><span class="sxs-lookup"><span data-stu-id="83594-153">The **CancelCalendarItem** element is only viewed by the organizer.</span></span> <span data-ttu-id="83594-154">它仅适用于组织者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="83594-154">It only applies to the organizer's calendar item.</span></span> 
  
<span data-ttu-id="83594-155">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="83594-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="83594-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="83594-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83594-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="83594-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="83594-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="83594-158">Schema Name</span></span>  <br/> |<span data-ttu-id="83594-159">类型架构</span><span class="sxs-lookup"><span data-stu-id="83594-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="83594-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="83594-160">Validation File</span></span>  <br/> |<span data-ttu-id="83594-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="83594-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="83594-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="83594-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="83594-163">False</span><span class="sxs-lookup"><span data-stu-id="83594-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83594-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="83594-164">See also</span></span>

- [<span data-ttu-id="83594-165">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="83594-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

