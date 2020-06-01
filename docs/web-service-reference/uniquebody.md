---
title: UniqueBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueBody
api_type:
- schema
ms.assetid: 06bc95d7-121c-433b-bd27-c2b0eb8c011f
description: UniqueBody 元素表示一个 HTML 片段或纯文本，表示此对话的唯一正文。
ms.openlocfilehash: 0a8d52c7d4eb8bda9fd41c4c25e448523185df93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461917"
---
# <a name="uniquebody"></a><span data-ttu-id="87e8d-103">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="87e8d-103">UniqueBody</span></span>

<span data-ttu-id="87e8d-104">**UniqueBody**元素表示一个 HTML 片段或纯文本，表示此对话的唯一正文。</span><span class="sxs-lookup"><span data-stu-id="87e8d-104">The **UniqueBody** element represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span> 
  
```XML
<UniqueBody BodyType=""/>
```

 <span data-ttu-id="87e8d-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="87e8d-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="87e8d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="87e8d-106">Attributes and elements</span></span>

<span data-ttu-id="87e8d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="87e8d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87e8d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="87e8d-108">Attributes</span></span>

|<span data-ttu-id="87e8d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="87e8d-109">**Attribute**</span></span>|<span data-ttu-id="87e8d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="87e8d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87e8d-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="87e8d-111">**BodyType**</span></span> <br/> |<span data-ttu-id="87e8d-112">介绍项正文在项中的存储方式。</span><span class="sxs-lookup"><span data-stu-id="87e8d-112">Describes how the item body is stored in the item.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="87e8d-113">Office.mailboxenums.bodytype 属性</span><span class="sxs-lookup"><span data-stu-id="87e8d-113">BodyType Attribute</span></span>

|<span data-ttu-id="87e8d-114">**值**</span><span class="sxs-lookup"><span data-stu-id="87e8d-114">**Value**</span></span>|<span data-ttu-id="87e8d-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="87e8d-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87e8d-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="87e8d-116">**HTML**</span></span> <br/> |<span data-ttu-id="87e8d-117">将所有正文转换为 HTML。</span><span class="sxs-lookup"><span data-stu-id="87e8d-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="87e8d-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="87e8d-118">**Text**</span></span> <br/> |<span data-ttu-id="87e8d-119">将所有正文转换为纯文本。</span><span class="sxs-lookup"><span data-stu-id="87e8d-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="87e8d-120">子元素</span><span class="sxs-lookup"><span data-stu-id="87e8d-120">Child elements</span></span>

<span data-ttu-id="87e8d-121">无。</span><span class="sxs-lookup"><span data-stu-id="87e8d-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="87e8d-122">父元素</span><span class="sxs-lookup"><span data-stu-id="87e8d-122">Parent elements</span></span>

|<span data-ttu-id="87e8d-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="87e8d-123">**Element**</span></span>|<span data-ttu-id="87e8d-124">**描述**</span><span class="sxs-lookup"><span data-stu-id="87e8d-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87e8d-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="87e8d-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="87e8d-126">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="87e8d-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-127">Contact</span><span class="sxs-lookup"><span data-stu-id="87e8d-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="87e8d-128">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="87e8d-128">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-129">DistributionList</span><span class="sxs-lookup"><span data-stu-id="87e8d-129">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="87e8d-130">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="87e8d-130">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-131">项目</span><span class="sxs-lookup"><span data-stu-id="87e8d-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="87e8d-132">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="87e8d-132">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-133">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="87e8d-133">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="87e8d-134">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="87e8d-134">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-135">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="87e8d-135">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="87e8d-136">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="87e8d-136">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-137">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="87e8d-137">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="87e8d-138">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="87e8d-138">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-139">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="87e8d-139">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="87e8d-140">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="87e8d-140">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-141">Message</span><span class="sxs-lookup"><span data-stu-id="87e8d-141">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="87e8d-142">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="87e8d-142">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-143">PostItem</span><span class="sxs-lookup"><span data-stu-id="87e8d-143">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="87e8d-144">表示 Exchange 存储中的公告项。</span><span class="sxs-lookup"><span data-stu-id="87e8d-144">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-145">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="87e8d-145">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="87e8d-146">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="87e8d-146">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="87e8d-147">任务</span><span class="sxs-lookup"><span data-stu-id="87e8d-147">Task</span></span>](task.md) <br/> |<span data-ttu-id="87e8d-148">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="87e8d-148">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="87e8d-149">文本值</span><span class="sxs-lookup"><span data-stu-id="87e8d-149">Text value</span></span>

<span data-ttu-id="87e8d-150">无。</span><span class="sxs-lookup"><span data-stu-id="87e8d-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87e8d-151">说明</span><span class="sxs-lookup"><span data-stu-id="87e8d-151">Remarks</span></span>

<span data-ttu-id="87e8d-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="87e8d-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87e8d-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="87e8d-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87e8d-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="87e8d-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="87e8d-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="87e8d-155">Schema Name</span></span>  <br/> |<span data-ttu-id="87e8d-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="87e8d-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="87e8d-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="87e8d-157">Validation File</span></span>  <br/> |<span data-ttu-id="87e8d-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="87e8d-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="87e8d-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="87e8d-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="87e8d-160">False</span><span class="sxs-lookup"><span data-stu-id="87e8d-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87e8d-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="87e8d-161">See also</span></span>



- [<span data-ttu-id="87e8d-162">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="87e8d-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

