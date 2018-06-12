---
title: InternetMessageHeaders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InternetMessageHeaders
api_type:
- schema
ms.assetid: 4dcf8671-96df-4a2d-9836-7e8e3a67e0db
description: InternetMessageHeaders 元素包含一些邮箱中的项目中包含 Internet 邮件头的集合。 若要获取的 Internet 邮件头的整个集合，请使用 PR_TRANSPORT_MESSAGE_HEADERS 属性。 有关 EWS 和 Internet 邮件头、 seeGetting Internet 邮件 headersin EWS、 MIME 和缺少的 Internet 邮件头的详细信息。
ms.openlocfilehash: 2da529a8a3532cebb2791b285b7673c962a2a656
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825954"
---
# <a name="internetmessageheaders"></a><span data-ttu-id="908a9-105">InternetMessageHeaders</span><span class="sxs-lookup"><span data-stu-id="908a9-105">InternetMessageHeaders</span></span>

<span data-ttu-id="908a9-106">**InternetMessageHeaders**元素包含一些邮箱中的项目中包含 Internet 邮件头的集合。</span><span class="sxs-lookup"><span data-stu-id="908a9-106">The **InternetMessageHeaders** element contains a collection of some of the Internet message headers that are contained in an item in a mailbox.</span></span> <span data-ttu-id="908a9-107">若要获取的 Internet 邮件头的整个集合，请使用**PR_TRANSPORT_MESSAGE_HEADERS**属性。</span><span class="sxs-lookup"><span data-stu-id="908a9-107">To get the entire collection of Internet message headers, use the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> <span data-ttu-id="908a9-108">有关 EWS 和 Internet 邮件头的详细信息，请参阅[EWS、 MIME 和缺少的 Internet 邮件头](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)中的"获取 Internet 邮件头"。</span><span class="sxs-lookup"><span data-stu-id="908a9-108">For more information about EWS and Internet message headers, see "Getting Internet message headers" in [EWS, MIME, and the missing Internet message headers](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx).</span></span>
  
```XML
<InternetMessageHeaders>
   <InternetMessageHeader/>
</InternetMessageHeaders>
```

 <span data-ttu-id="908a9-109">**NonEmptyArrayOfInternetHeadersType**</span><span class="sxs-lookup"><span data-stu-id="908a9-109">**NonEmptyArrayOfInternetHeadersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="908a9-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="908a9-110">Attributes and elements</span></span>

<span data-ttu-id="908a9-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="908a9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="908a9-112">属性</span><span class="sxs-lookup"><span data-stu-id="908a9-112">Attributes</span></span>

<span data-ttu-id="908a9-113">无。</span><span class="sxs-lookup"><span data-stu-id="908a9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="908a9-114">子元素</span><span class="sxs-lookup"><span data-stu-id="908a9-114">Child elements</span></span>

|<span data-ttu-id="908a9-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="908a9-115">**Element**</span></span>|<span data-ttu-id="908a9-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="908a9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="908a9-117">InternetMessageHeader</span><span class="sxs-lookup"><span data-stu-id="908a9-117">InternetMessageHeader</span></span>](internetmessageheader.md) <br/> |<span data-ttu-id="908a9-118">表示给定标题的标头集合中的 Internet 邮件标题。</span><span class="sxs-lookup"><span data-stu-id="908a9-118">Represents the Internet message header for a given header within the headers collection.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="908a9-119">父元素</span><span class="sxs-lookup"><span data-stu-id="908a9-119">Parent elements</span></span>

|<span data-ttu-id="908a9-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="908a9-120">**Element**</span></span>|<span data-ttu-id="908a9-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="908a9-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="908a9-122">AcceptItem</span><span class="sxs-lookup"><span data-stu-id="908a9-122">AcceptItem</span></span>](acceptitem.md) <br/> |<span data-ttu-id="908a9-123">表示接受答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="908a9-123">Represents an Accept reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="908a9-124">日历项目</span><span class="sxs-lookup"><span data-stu-id="908a9-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="908a9-125">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="908a9-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="908a9-126">联系人</span><span class="sxs-lookup"><span data-stu-id="908a9-126">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="908a9-127">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="908a9-127">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="908a9-128">DeclineItem</span><span class="sxs-lookup"><span data-stu-id="908a9-128">DeclineItem</span></span>](declineitem.md) <br/> |<span data-ttu-id="908a9-129">表示谢绝答复会议要求。</span><span class="sxs-lookup"><span data-stu-id="908a9-129">Represents a Decline reply to a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="908a9-130">DistributionList</span><span class="sxs-lookup"><span data-stu-id="908a9-130">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="908a9-131">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="908a9-131">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="908a9-132">项目</span><span class="sxs-lookup"><span data-stu-id="908a9-132">Item</span></span>](item.md) <br/> |<span data-ttu-id="908a9-133">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="908a9-133">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="908a9-134">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="908a9-134">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="908a9-135">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="908a9-135">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="908a9-136">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="908a9-136">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="908a9-137">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="908a9-137">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="908a9-138">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="908a9-138">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="908a9-139">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="908a9-139">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="908a9-140">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="908a9-140">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="908a9-141">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="908a9-141">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="908a9-142">Message</span><span class="sxs-lookup"><span data-stu-id="908a9-142">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="908a9-143">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="908a9-143">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="908a9-144">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="908a9-144">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="908a9-145">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="908a9-145">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="908a9-146">任务</span><span class="sxs-lookup"><span data-stu-id="908a9-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="908a9-147">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="908a9-147">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="908a9-148">TentativelyAcceptItem</span><span class="sxs-lookup"><span data-stu-id="908a9-148">TentativelyAcceptItem</span></span>](tentativelyacceptitem.md) <br/> |<span data-ttu-id="908a9-149">表示暂时接受的会议请求答复。</span><span class="sxs-lookup"><span data-stu-id="908a9-149">Represents a tentatively accepted reply to a meeting request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="908a9-150">备注</span><span class="sxs-lookup"><span data-stu-id="908a9-150">Remarks</span></span>

<span data-ttu-id="908a9-151">下面是 EWS 托管 API 扩展属性**PR_TRANSPORT_MESSAGE_HEADERS**属性的定义。</span><span class="sxs-lookup"><span data-stu-id="908a9-151">The following is the EWS Managed API extended property definition for the **PR_TRANSPORT_MESSAGE_HEADERS** property.</span></span> 
  
```cs
ExtendedPropertyDefinition transportMsgHdr = new ExtendedPropertyDefinition(0x007D, MapiPropertyType.String);
```

<span data-ttu-id="908a9-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="908a9-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="908a9-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="908a9-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="908a9-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="908a9-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="908a9-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="908a9-155">Schema Name</span></span>  <br/> |<span data-ttu-id="908a9-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="908a9-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="908a9-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="908a9-157">Validation File</span></span>  <br/> |<span data-ttu-id="908a9-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="908a9-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="908a9-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="908a9-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="908a9-160">False</span><span class="sxs-lookup"><span data-stu-id="908a9-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="908a9-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="908a9-161">See also</span></span>



- [<span data-ttu-id="908a9-162">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="908a9-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="908a9-163">EWS、 MIME 和缺少的 Internet 邮件头</span><span class="sxs-lookup"><span data-stu-id="908a9-163">EWS, MIME, and the missing Internet message headers</span></span>](http://msdn.microsoft.com/en-us/library/exchange/hh545614%28v=exchg.140%29.aspx)

