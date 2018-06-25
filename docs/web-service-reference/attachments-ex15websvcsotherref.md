---
title: 附件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attachments
api_type:
- schema
ms.assetid: b470e614-34bb-44f0-8790-7ddbdcbbd29d
description: Attachments 元素包含的项或附加到 Exchange 存储中的项目文件。
ms.openlocfilehash: 8aa5c0849122f5ca83485459fce5d0fea449c974
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753282"
---
# <a name="attachments"></a><span data-ttu-id="a70a3-103">附件</span><span class="sxs-lookup"><span data-stu-id="a70a3-103">Attachments</span></span>

<span data-ttu-id="a70a3-104">**Attachments**元素包含的项或附加到 Exchange 存储中的项目文件。</span><span class="sxs-lookup"><span data-stu-id="a70a3-104">The **Attachments** element contains the items or files that are attached to an item in the Exchange store.</span></span> 
  
```xml
<Attachments>
   <ItemAttachment/>
   <FileAttachment/>
</Attachments>
```

 <span data-ttu-id="a70a3-105">**ArrayOfAttachmentsType**和**NonEmptyArrayOfAttachmentsType**</span><span class="sxs-lookup"><span data-stu-id="a70a3-105">**ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a70a3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a70a3-106">Attributes and elements</span></span>

<span data-ttu-id="a70a3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a70a3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a70a3-108">属性</span><span class="sxs-lookup"><span data-stu-id="a70a3-108">Attributes</span></span>

<span data-ttu-id="a70a3-109">无。</span><span class="sxs-lookup"><span data-stu-id="a70a3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a70a3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a70a3-110">Child elements</span></span>

|<span data-ttu-id="a70a3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a70a3-111">**Element**</span></span>|<span data-ttu-id="a70a3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a70a3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a70a3-113">ItemAttachment</span><span class="sxs-lookup"><span data-stu-id="a70a3-113">ItemAttachment</span></span>](itemattachment.md) <br/> |<span data-ttu-id="a70a3-114">代表附加到另一个 Exchange 项目的 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="a70a3-114">Represents an Exchange item that is attached to another Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="a70a3-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="a70a3-116">代表附加到 Exchange 存储中的项的文件。</span><span class="sxs-lookup"><span data-stu-id="a70a3-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a70a3-117">父元素</span><span class="sxs-lookup"><span data-stu-id="a70a3-117">Parent elements</span></span>

|<span data-ttu-id="a70a3-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="a70a3-118">**Element**</span></span>|<span data-ttu-id="a70a3-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="a70a3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a70a3-120">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="a70a3-120">CreateAttachment</span></span>](createattachment.md) <br/> |<span data-ttu-id="a70a3-121">定义在 Exchange 存储中创建项目附件的请求。</span><span class="sxs-lookup"><span data-stu-id="a70a3-121">Defines a request to create an attachment to an item in the Exchange store.</span></span><br/><br/> <span data-ttu-id="a70a3-122">下面是此元素的 XPath 表达式:  `/CreateAttachment`</span><span class="sxs-lookup"><span data-stu-id="a70a3-122">The following is the XPath expression to this element:  `/CreateAttachment`</span></span> <br/> |
|[<span data-ttu-id="a70a3-123">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="a70a3-123">AcceptItem</span></span>](acceptitem.md) <br/> | <span data-ttu-id="a70a3-124">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="a70a3-124">Represents an Accept reply to a meeting request.</span></span><br/><br/><span data-ttu-id="a70a3-125">下面是一些到此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a70a3-125">The following are some of the XPath expressions to this element:</span></span><ul><li>`/CreateItem/Items`</li><li>`/MeetingRequest/ConflictingMeetings` </li><li>`/SetItemField/CalendarItem/ConflictingMeetings`</li><li>`/AppendToItemField/CalendarItem/ConflictingMeetings`</li><li>`/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings`</li><li>`/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li><li>`/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li></ul> |
|[<span data-ttu-id="a70a3-126">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="a70a3-126">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="a70a3-127">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="a70a3-127">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-128">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="a70a3-128">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="a70a3-129">表示一个暂定答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="a70a3-129">Represents a Tentative reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-130">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="a70a3-130">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="a70a3-131">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="a70a3-131">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-132">Item</span><span class="sxs-lookup"><span data-stu-id="a70a3-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="a70a3-133">表示的泛型 Exchange 项目。</span><span class="sxs-lookup"><span data-stu-id="a70a3-133">Represents a generic Exchange item.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-134">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="a70a3-134">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="a70a3-135">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="a70a3-135">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-136">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a70a3-136">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a70a3-137">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="a70a3-137">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-138">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="a70a3-138">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="a70a3-139">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="a70a3-139">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-140">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="a70a3-140">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="a70a3-141">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="a70a3-141">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-142">Message</span><span class="sxs-lookup"><span data-stu-id="a70a3-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a70a3-143">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="a70a3-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-144">任务</span><span class="sxs-lookup"><span data-stu-id="a70a3-144">Task</span></span>](task.md) <br/> |<span data-ttu-id="a70a3-145">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="a70a3-145">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-146">日历项目</span><span class="sxs-lookup"><span data-stu-id="a70a3-146">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a70a3-147">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="a70a3-147">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-148">联系人</span><span class="sxs-lookup"><span data-stu-id="a70a3-148">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="a70a3-149">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="a70a3-149">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-150">DistributionList</span><span class="sxs-lookup"><span data-stu-id="a70a3-150">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="a70a3-151">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="a70a3-151">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-152">CreateAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a70a3-152">CreateAttachmentResponseMessage</span></span>](createattachmentresponsemessage.md) <br/> |<span data-ttu-id="a70a3-153">包含状态和单个 CreateAttachment 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="a70a3-153">Contains the status and result of a single CreateAttachment request.</span></span>  <br/> |
|[<span data-ttu-id="a70a3-154">GetAttachmentResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a70a3-154">GetAttachmentResponseMessage</span></span>](getattachmentresponsemessage.md) <br/> |<span data-ttu-id="a70a3-155">包含状态和 GetAttachment 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="a70a3-155">Contains the status and result of a GetAttachment request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a70a3-156">注解</span><span class="sxs-lookup"><span data-stu-id="a70a3-156">Remarks</span></span>

<span data-ttu-id="a70a3-157">**Attachments**元素具有相同的子元素，但基于不同类型： **ArrayOfAttachmentsType**和**NonEmptyArrayOfAttachmentsType**。</span><span class="sxs-lookup"><span data-stu-id="a70a3-157">The **Attachments** elements have the same child elements but are based on different types: **ArrayOfAttachmentsType** and **NonEmptyArrayOfAttachmentsType**.</span></span> <span data-ttu-id="a70a3-158">类型定义子元素是否是必需的。</span><span class="sxs-lookup"><span data-stu-id="a70a3-158">The types define whether a child element is required.</span></span> <span data-ttu-id="a70a3-159">**ArrayOfAttachmentsType**仅响应消息中使用。</span><span class="sxs-lookup"><span data-stu-id="a70a3-159">The **ArrayOfAttachmentsType** is only used in the response message.</span></span> <span data-ttu-id="a70a3-160">务必还请注意，这些元素将发生的消息和类型的命名空间中。</span><span class="sxs-lookup"><span data-stu-id="a70a3-160">It is also important to note that these elements occur in both the messages and types namespaces.</span></span> 
  
<span data-ttu-id="a70a3-161">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a70a3-161">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a70a3-162">元素信息</span><span class="sxs-lookup"><span data-stu-id="a70a3-162">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a70a3-163">命名空间</span><span class="sxs-lookup"><span data-stu-id="a70a3-163">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a70a3-164">架构名称</span><span class="sxs-lookup"><span data-stu-id="a70a3-164">Schema Name</span></span>  <br/> |<span data-ttu-id="a70a3-165">类型架构</span><span class="sxs-lookup"><span data-stu-id="a70a3-165">Types schema</span></span>  <br/> |
|<span data-ttu-id="a70a3-166">验证文件</span><span class="sxs-lookup"><span data-stu-id="a70a3-166">Validation File</span></span>  <br/> |<span data-ttu-id="a70a3-167">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a70a3-167">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a70a3-168">可以为空</span><span class="sxs-lookup"><span data-stu-id="a70a3-168">Can be Empty</span></span>  <br/> |<span data-ttu-id="a70a3-169">False</span><span class="sxs-lookup"><span data-stu-id="a70a3-169">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a70a3-170">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a70a3-170">See also</span></span>

- [<span data-ttu-id="a70a3-171">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a70a3-171">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

