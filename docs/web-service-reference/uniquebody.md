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
description: UniqueBody 元素均表示一个 HTML 片段或代表此对话的唯一正文的纯文本。
ms.openlocfilehash: 49d3607926e0b985074d79cde76cad084f537f01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838325"
---
# <a name="uniquebody"></a><span data-ttu-id="ff086-103">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="ff086-103">UniqueBody</span></span>

<span data-ttu-id="ff086-104">**UniqueBody**元素均表示一个 HTML 片段或代表此对话的唯一正文的纯文本。</span><span class="sxs-lookup"><span data-stu-id="ff086-104">The **UniqueBody** element represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span> 
  
```XML
<UniqueBody BodyType=""/>
```

 <span data-ttu-id="ff086-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="ff086-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff086-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ff086-106">Attributes and elements</span></span>

<span data-ttu-id="ff086-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ff086-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff086-108">属性</span><span class="sxs-lookup"><span data-stu-id="ff086-108">Attributes</span></span>

|<span data-ttu-id="ff086-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="ff086-109">**Attribute**</span></span>|<span data-ttu-id="ff086-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff086-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff086-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="ff086-111">**BodyType**</span></span> <br/> |<span data-ttu-id="ff086-112">介绍如何将项目正文存储在项。</span><span class="sxs-lookup"><span data-stu-id="ff086-112">Describes how the item body is stored in the item.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="ff086-113">BodyType 属性</span><span class="sxs-lookup"><span data-stu-id="ff086-113">BodyType Attribute</span></span>

|<span data-ttu-id="ff086-114">**值**</span><span class="sxs-lookup"><span data-stu-id="ff086-114">**Value**</span></span>|<span data-ttu-id="ff086-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff086-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ff086-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="ff086-116">**HTML**</span></span> <br/> |<span data-ttu-id="ff086-117">将所有正文都转换为 HTML。</span><span class="sxs-lookup"><span data-stu-id="ff086-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="ff086-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="ff086-118">**Text**</span></span> <br/> |<span data-ttu-id="ff086-119">将所有正文都转换为纯文本。</span><span class="sxs-lookup"><span data-stu-id="ff086-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ff086-120">子元素</span><span class="sxs-lookup"><span data-stu-id="ff086-120">Child elements</span></span>

<span data-ttu-id="ff086-121">无。</span><span class="sxs-lookup"><span data-stu-id="ff086-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ff086-122">父元素</span><span class="sxs-lookup"><span data-stu-id="ff086-122">Parent elements</span></span>

|<span data-ttu-id="ff086-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="ff086-123">**Element**</span></span>|<span data-ttu-id="ff086-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff086-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff086-125">日历项目</span><span class="sxs-lookup"><span data-stu-id="ff086-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="ff086-126">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="ff086-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="ff086-127">联系人</span><span class="sxs-lookup"><span data-stu-id="ff086-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="ff086-128">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="ff086-128">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="ff086-129">DistributionList</span><span class="sxs-lookup"><span data-stu-id="ff086-129">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="ff086-130">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="ff086-130">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ff086-131">项目</span><span class="sxs-lookup"><span data-stu-id="ff086-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="ff086-132">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="ff086-132">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff086-133">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="ff086-133">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="ff086-134">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="ff086-134">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff086-135">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="ff086-135">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="ff086-136">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="ff086-136">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff086-137">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="ff086-137">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="ff086-138">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="ff086-138">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff086-139">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="ff086-139">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="ff086-140">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="ff086-140">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff086-141">Message</span><span class="sxs-lookup"><span data-stu-id="ff086-141">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ff086-142">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="ff086-142">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="ff086-143">PostItem</span><span class="sxs-lookup"><span data-stu-id="ff086-143">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="ff086-144">代表一个 Exchange 存储中的公告项目。</span><span class="sxs-lookup"><span data-stu-id="ff086-144">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff086-145">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="ff086-145">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="ff086-146">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="ff086-146">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="ff086-147">任务</span><span class="sxs-lookup"><span data-stu-id="ff086-147">Task</span></span>](task.md) <br/> |<span data-ttu-id="ff086-148">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="ff086-148">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ff086-149">文本值</span><span class="sxs-lookup"><span data-stu-id="ff086-149">Text value</span></span>

<span data-ttu-id="ff086-150">无。</span><span class="sxs-lookup"><span data-stu-id="ff086-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ff086-151">备注</span><span class="sxs-lookup"><span data-stu-id="ff086-151">Remarks</span></span>

<span data-ttu-id="ff086-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ff086-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff086-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="ff086-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff086-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="ff086-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ff086-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="ff086-155">Schema Name</span></span>  <br/> |<span data-ttu-id="ff086-156">类型架构</span><span class="sxs-lookup"><span data-stu-id="ff086-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="ff086-157">验证文件</span><span class="sxs-lookup"><span data-stu-id="ff086-157">Validation File</span></span>  <br/> |<span data-ttu-id="ff086-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ff086-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ff086-159">可以为空</span><span class="sxs-lookup"><span data-stu-id="ff086-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff086-160">False</span><span class="sxs-lookup"><span data-stu-id="ff086-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff086-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ff086-161">See also</span></span>



- [<span data-ttu-id="ff086-162">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ff086-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

