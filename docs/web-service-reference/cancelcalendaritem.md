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
description: CancelCalendarItem 元素表示用于取消会议的响应对象。
ms.openlocfilehash: 45ad76d19bd43e2081aa9b9eb63547e091014803
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462253"
---
# <a name="cancelcalendaritem"></a><span data-ttu-id="27d55-103">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="27d55-103">CancelCalendarItem</span></span>

<span data-ttu-id="27d55-104">**CancelCalendarItem**元素表示用于取消会议的响应对象。</span><span class="sxs-lookup"><span data-stu-id="27d55-104">The **CancelCalendarItem** element represents the response object that is used to cancel a meeting.</span></span> 
  
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

 <span data-ttu-id="27d55-105">**CancelCalendarItemType**</span><span class="sxs-lookup"><span data-stu-id="27d55-105">**CancelCalendarItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="27d55-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="27d55-106">Attributes and elements</span></span>

<span data-ttu-id="27d55-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="27d55-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="27d55-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="27d55-108">Attributes</span></span>

<span data-ttu-id="27d55-109">无。</span><span class="sxs-lookup"><span data-stu-id="27d55-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="27d55-110">子元素</span><span class="sxs-lookup"><span data-stu-id="27d55-110">Child elements</span></span>

|<span data-ttu-id="27d55-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="27d55-111">**Element**</span></span>|<span data-ttu-id="27d55-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="27d55-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27d55-113">主题</span><span class="sxs-lookup"><span data-stu-id="27d55-113">Subject</span></span>](subject.md) <br/> |<span data-ttu-id="27d55-114">表示 Exchange 存储项的 subject 属性。</span><span class="sxs-lookup"><span data-stu-id="27d55-114">Represents the subject property of Exchange store items.</span></span>  <br/> |
|[<span data-ttu-id="27d55-115">Body</span><span class="sxs-lookup"><span data-stu-id="27d55-115">Body</span></span>](body.md) <br/> |<span data-ttu-id="27d55-116">不由**CancelCalendarItem**使用。</span><span class="sxs-lookup"><span data-stu-id="27d55-116">Not used by **CancelCalendarItem**.</span></span> <span data-ttu-id="27d55-117">使用[NewBodyContent](newbodycontent.md)属性来设置正文内容。</span><span class="sxs-lookup"><span data-stu-id="27d55-117">Use the [NewBodyContent](newbodycontent.md) property to set the body content.</span></span>  <br/> |
|[<span data-ttu-id="27d55-118">ToRecipients</span><span class="sxs-lookup"><span data-stu-id="27d55-118">ToRecipients</span></span>](torecipients.md) <br/> |<span data-ttu-id="27d55-119">包含项目的一组收件人。</span><span class="sxs-lookup"><span data-stu-id="27d55-119">Contains a set of recipients of an item.</span></span> <span data-ttu-id="27d55-120">这是一项主要收件人。</span><span class="sxs-lookup"><span data-stu-id="27d55-120">These are the primary recipients of an item.</span></span>  <br/> |
|[<span data-ttu-id="27d55-121">CcRecipients</span><span class="sxs-lookup"><span data-stu-id="27d55-121">CcRecipients</span></span>](ccrecipients.md) <br/> |<span data-ttu-id="27d55-122">表示将收到邮件副本的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="27d55-122">Represents a collection of recipients that will receive a copy of the message.</span></span>  <br/> |
|[<span data-ttu-id="27d55-123">BccRecipients</span><span class="sxs-lookup"><span data-stu-id="27d55-123">BccRecipients</span></span>](bccrecipients.md) <br/> |<span data-ttu-id="27d55-124">表示接收电子邮件的密件抄送 (Bcc) 的收件人集合。</span><span class="sxs-lookup"><span data-stu-id="27d55-124">Represents a collection of recipients to receive a blind carbon copy (Bcc) of an e-mail.</span></span>  <br/> |
|[<span data-ttu-id="27d55-125">IsReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="27d55-125">IsReadReceiptRequested</span></span>](isreadreceiptrequested.md) <br/> |<span data-ttu-id="27d55-126">指示项目的发件人是否请求已读回执。</span><span class="sxs-lookup"><span data-stu-id="27d55-126">Indicates whether the sender of an item requests a read receipt.</span></span>  <br/> |
|[<span data-ttu-id="27d55-127">IsDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="27d55-127">IsDeliveryReceiptRequested</span></span>](isdeliveryreceiptrequested.md) <br/> |<span data-ttu-id="27d55-128">指示项目的发件人是否请求送达回执。</span><span class="sxs-lookup"><span data-stu-id="27d55-128">Indicates whether the sender of an item requests a delivery receipt.</span></span>  <br/> |
|[<span data-ttu-id="27d55-129">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="27d55-129">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="27d55-130">标识 response 对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="27d55-130">Identifies the item to which the response object refers.</span></span>  <br/> |
|[<span data-ttu-id="27d55-131">NewBodyContent</span><span class="sxs-lookup"><span data-stu-id="27d55-131">NewBodyContent</span></span>](newbodycontent.md) <br/> |<span data-ttu-id="27d55-132">表示邮件的新正文内容。</span><span class="sxs-lookup"><span data-stu-id="27d55-132">Represents the new body content of a message.</span></span>  <br/> |
|[<span data-ttu-id="27d55-133">ReceivedBy</span><span class="sxs-lookup"><span data-stu-id="27d55-133">ReceivedBy</span></span>](receivedby.md) <br/> |<span data-ttu-id="27d55-134">标识代理访问方案中的委派。</span><span class="sxs-lookup"><span data-stu-id="27d55-134">Identifies the delegate in a delegate access scenario.</span></span> <span data-ttu-id="27d55-135">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="27d55-135">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="27d55-136">ReceivedRepresenting</span><span class="sxs-lookup"><span data-stu-id="27d55-136">ReceivedRepresenting</span></span>](receivedrepresenting.md) <br/> |<span data-ttu-id="27d55-137">标识代理访问方案中的主体。</span><span class="sxs-lookup"><span data-stu-id="27d55-137">Identifies the principal in a delegate access scenario.</span></span> <span data-ttu-id="27d55-138">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="27d55-138">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="27d55-139">父元素</span><span class="sxs-lookup"><span data-stu-id="27d55-139">Parent elements</span></span>

|<span data-ttu-id="27d55-140">**元素**</span><span class="sxs-lookup"><span data-stu-id="27d55-140">**Element**</span></span>|<span data-ttu-id="27d55-141">**说明**</span><span class="sxs-lookup"><span data-stu-id="27d55-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="27d55-142">AdjacentMeetings</span><span class="sxs-lookup"><span data-stu-id="27d55-142">AdjacentMeetings</span></span>](adjacentmeetings.md) <br/> | <span data-ttu-id="27d55-143">描述与会议时间相邻的所有项目。</span><span class="sxs-lookup"><span data-stu-id="27d55-143">Describes all items that are adjacent to a meeting time.</span></span><br/><br/> <span data-ttu-id="27d55-144">下面是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="27d55-144">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[<span data-ttu-id="27d55-145">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="27d55-145">ConflictingMeetings</span></span>](conflictingmeetings.md) <br/> | <span data-ttu-id="27d55-146">描述与会议时间冲突的所有项目。</span><span class="sxs-lookup"><span data-stu-id="27d55-146">Describes all items that conflict with a meeting time.</span></span><br/><br/><span data-ttu-id="27d55-147">下面是此元素的一些 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="27d55-147">The following are some of the XPath expressions to this element:</span></span><br/><br/>`/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[<span data-ttu-id="27d55-148">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="27d55-148">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="27d55-149">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="27d55-149">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="27d55-150">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="27d55-150">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="27d55-151">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="27d55-151">Contains an array of items to create in the folder identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27d55-152">备注</span><span class="sxs-lookup"><span data-stu-id="27d55-152">Remarks</span></span>

<span data-ttu-id="27d55-153">**CancelCalendarItem**元素仅由组织者查看。</span><span class="sxs-lookup"><span data-stu-id="27d55-153">The **CancelCalendarItem** element is only viewed by the organizer.</span></span> <span data-ttu-id="27d55-154">它仅适用于组织者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="27d55-154">It only applies to the organizer's calendar item.</span></span> 
  
<span data-ttu-id="27d55-155">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="27d55-155">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="27d55-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="27d55-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="27d55-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="27d55-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="27d55-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="27d55-158">Schema Name</span></span>  <br/> |<span data-ttu-id="27d55-159">类型架构</span><span class="sxs-lookup"><span data-stu-id="27d55-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="27d55-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="27d55-160">Validation File</span></span>  <br/> |<span data-ttu-id="27d55-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="27d55-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="27d55-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="27d55-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="27d55-163">False</span><span class="sxs-lookup"><span data-stu-id="27d55-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="27d55-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27d55-164">See also</span></span>

- [<span data-ttu-id="27d55-165">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="27d55-165">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

