---
title: 主题
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subject
api_type:
- schema
ms.assetid: c140d6c2-deb1-4f67-a908-9397197c4ae7
description: Subject 元素表示 Exchange 存储项的 subject 属性。 主题限制为255个字符。
ms.openlocfilehash: c4d7c21ab70c21ceb63e53d008d25aebf8e22270
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458969"
---
# <a name="subject"></a><span data-ttu-id="2f419-104">Subject</span><span class="sxs-lookup"><span data-stu-id="2f419-104">Subject</span></span>

<span data-ttu-id="2f419-105">**Subject**元素表示 Exchange 存储项的 subject 属性。</span><span class="sxs-lookup"><span data-stu-id="2f419-105">The **Subject** element represents the subject property of Exchange store items.</span></span> <span data-ttu-id="2f419-106">主题限制为255个字符。</span><span class="sxs-lookup"><span data-stu-id="2f419-106">The subject is limited to 255 characters.</span></span> 
  
```XML
<Subject/>
```

 <span data-ttu-id="2f419-107">**string**</span><span class="sxs-lookup"><span data-stu-id="2f419-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f419-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f419-108">Attributes and elements</span></span>

<span data-ttu-id="2f419-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f419-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f419-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="2f419-110">Attributes</span></span>

<span data-ttu-id="2f419-111">无。</span><span class="sxs-lookup"><span data-stu-id="2f419-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f419-112">子元素</span><span class="sxs-lookup"><span data-stu-id="2f419-112">Child elements</span></span>

<span data-ttu-id="2f419-113">无。</span><span class="sxs-lookup"><span data-stu-id="2f419-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f419-114">父元素</span><span class="sxs-lookup"><span data-stu-id="2f419-114">Parent elements</span></span>

|<span data-ttu-id="2f419-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f419-115">**Element**</span></span>|<span data-ttu-id="2f419-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f419-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f419-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="2f419-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="2f419-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="2f419-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="2f419-119">CancelCalendarItem</span><span class="sxs-lookup"><span data-stu-id="2f419-119">CancelCalendarItem</span></span>](cancelcalendaritem.md) <br/> |<span data-ttu-id="2f419-120">代表 "取消日历项目" 响应对象。</span><span class="sxs-lookup"><span data-stu-id="2f419-120">Represents a cancel calendar item response object.</span></span>  <br/> |
|[<span data-ttu-id="2f419-121">Contact</span><span class="sxs-lookup"><span data-stu-id="2f419-121">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="2f419-122">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="2f419-122">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="2f419-123">DistributionList</span><span class="sxs-lookup"><span data-stu-id="2f419-123">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="2f419-124">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="2f419-124">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="2f419-125">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="2f419-125">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="2f419-126">指定要查找的邮件类型的条件。</span><span class="sxs-lookup"><span data-stu-id="2f419-126">Specifies criteria for the types of messages to find.</span></span>  <br/> |
|[<span data-ttu-id="2f419-127">ForwardItem</span><span class="sxs-lookup"><span data-stu-id="2f419-127">ForwardItem</span></span>](forwarditem.md) <br/> |<span data-ttu-id="2f419-128">代表 "转发项目" 智能响应对象。</span><span class="sxs-lookup"><span data-stu-id="2f419-128">Represents a forward item smart response object.</span></span>  <br/> |
|[<span data-ttu-id="2f419-129">项目</span><span class="sxs-lookup"><span data-stu-id="2f419-129">Item</span></span>](item.md) <br/> |<span data-ttu-id="2f419-130">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="2f419-130">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2f419-131">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="2f419-131">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="2f419-132">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="2f419-132">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2f419-133">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="2f419-133">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="2f419-134">表示 Exchange 存储中的会议邮件。</span><span class="sxs-lookup"><span data-stu-id="2f419-134">Represents a meeting message in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2f419-135">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="2f419-135">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="2f419-136">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="2f419-136">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2f419-137">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="2f419-137">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="2f419-138">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="2f419-138">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2f419-139">Message</span><span class="sxs-lookup"><span data-stu-id="2f419-139">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2f419-140">表示 Exchange 存储中的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="2f419-140">Represents an e-mail in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="2f419-141">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="2f419-141">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="2f419-142">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="2f419-142">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="2f419-143">MessageTrackingSearchResult</span><span class="sxs-lookup"><span data-stu-id="2f419-143">MessageTrackingSearchResult</span></span>](messagetrackingsearchresult.md) <br/> |<span data-ttu-id="2f419-144">包含[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素的单个邮件结果。</span><span class="sxs-lookup"><span data-stu-id="2f419-144">Contains a single message result for a [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) element.</span></span>  <br/> |
|[<span data-ttu-id="2f419-145">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="2f419-145">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="2f419-146">表示一个删除项响应对象。</span><span class="sxs-lookup"><span data-stu-id="2f419-146">Represents a remove item response object.</span></span>  <br/> |
|[<span data-ttu-id="2f419-147">ReplyAllToItem</span><span class="sxs-lookup"><span data-stu-id="2f419-147">ReplyAllToItem</span></span>](replyalltoitem.md) <br/> |<span data-ttu-id="2f419-148">代表 "全部答复" 智能响应对象。</span><span class="sxs-lookup"><span data-stu-id="2f419-148">Represents a reply-to-all smart response object.</span></span>  <br/> |
|[<span data-ttu-id="2f419-149">ReplyToItem</span><span class="sxs-lookup"><span data-stu-id="2f419-149">ReplyToItem</span></span>](replytoitem.md) <br/> |<span data-ttu-id="2f419-150">代表 "答复项目" 智能响应对象。</span><span class="sxs-lookup"><span data-stu-id="2f419-150">Represents a reply-to-item smart response object.</span></span>  <br/> |
|[<span data-ttu-id="2f419-151">任务</span><span class="sxs-lookup"><span data-stu-id="2f419-151">Task</span></span>](task.md) <br/> |<span data-ttu-id="2f419-152">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="2f419-152">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f419-153">文本值</span><span class="sxs-lookup"><span data-stu-id="2f419-153">Text value</span></span>

<span data-ttu-id="2f419-154">包含 Exchange 项目的主题的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="2f419-154">A text value that contains the subject of an Exchange item is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f419-155">说明</span><span class="sxs-lookup"><span data-stu-id="2f419-155">Remarks</span></span>

<span data-ttu-id="2f419-156">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2f419-156">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f419-157">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f419-157">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f419-158">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f419-158">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f419-159">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f419-159">Schema Name</span></span>  <br/> |<span data-ttu-id="2f419-160">类型架构</span><span class="sxs-lookup"><span data-stu-id="2f419-160">Types schema</span></span>  <br/> |
|<span data-ttu-id="2f419-161">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f419-161">Validation File</span></span>  <br/> |<span data-ttu-id="2f419-162">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2f419-162">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f419-163">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f419-163">Can be Empty</span></span>  <br/> |<span data-ttu-id="2f419-164">False</span><span class="sxs-lookup"><span data-stu-id="2f419-164">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f419-165">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f419-165">See also</span></span>



[<span data-ttu-id="2f419-166">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="2f419-166">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="2f419-167">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2f419-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

