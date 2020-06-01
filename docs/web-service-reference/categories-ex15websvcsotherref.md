---
title: 类别
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Categories
api_type:
- schema
ms.assetid: d84d4927-b524-4e62-bf3d-1f12fec8c21a
description: "\"类别\" 元素包含一个字符串集合，这些字符串标识邮箱中的项目所属的类别。"
ms.openlocfilehash: 0d9f7068aa81306a10436ed0ca0d45f6d3b2c3a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462211"
---
# <a name="categories"></a><span data-ttu-id="05f7a-103">类别</span><span class="sxs-lookup"><span data-stu-id="05f7a-103">Categories</span></span>

<span data-ttu-id="05f7a-104">"**类别**" 元素包含一个字符串集合，这些字符串标识邮箱中的项目所属的类别。</span><span class="sxs-lookup"><span data-stu-id="05f7a-104">The **Categories** element contains a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span> 
  
```XML
<Categories>
   <String/>
</Categories>
```

 <span data-ttu-id="05f7a-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="05f7a-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05f7a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="05f7a-106">Attributes and elements</span></span>

<span data-ttu-id="05f7a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="05f7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05f7a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="05f7a-108">Attributes</span></span>

<span data-ttu-id="05f7a-109">无。</span><span class="sxs-lookup"><span data-stu-id="05f7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05f7a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="05f7a-110">Child elements</span></span>

|<span data-ttu-id="05f7a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="05f7a-111">**Element**</span></span>|<span data-ttu-id="05f7a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="05f7a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05f7a-113">字符串</span><span class="sxs-lookup"><span data-stu-id="05f7a-113">String</span></span>](string.md) <br/> |<span data-ttu-id="05f7a-114">包含用于标识单个类别的字符串。</span><span class="sxs-lookup"><span data-stu-id="05f7a-114">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05f7a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="05f7a-115">Parent elements</span></span>

|<span data-ttu-id="05f7a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="05f7a-116">**Element**</span></span>|<span data-ttu-id="05f7a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="05f7a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05f7a-118">项目</span><span class="sxs-lookup"><span data-stu-id="05f7a-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="05f7a-119">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="05f7a-119">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-120">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="05f7a-120">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="05f7a-121">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="05f7a-121">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-122">Message</span><span class="sxs-lookup"><span data-stu-id="05f7a-122">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="05f7a-123">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="05f7a-123">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-124">任务</span><span class="sxs-lookup"><span data-stu-id="05f7a-124">Task</span></span>](task.md) <br/> |<span data-ttu-id="05f7a-125">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="05f7a-125">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-126">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="05f7a-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="05f7a-127">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="05f7a-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-128">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="05f7a-128">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="05f7a-129">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="05f7a-129">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-130">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="05f7a-130">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="05f7a-131">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="05f7a-131">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-132">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="05f7a-132">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="05f7a-133">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="05f7a-133">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-134">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="05f7a-134">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="05f7a-135">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="05f7a-135">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="05f7a-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="05f7a-137">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="05f7a-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-138">Contact</span><span class="sxs-lookup"><span data-stu-id="05f7a-138">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="05f7a-139">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="05f7a-139">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-140">DistributionList</span><span class="sxs-lookup"><span data-stu-id="05f7a-140">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="05f7a-141">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="05f7a-141">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-142">条件</span><span class="sxs-lookup"><span data-stu-id="05f7a-142">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="05f7a-143">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="05f7a-143">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-144">异常</span><span class="sxs-lookup"><span data-stu-id="05f7a-144">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="05f7a-145">代表收件箱规则的所有可用的规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="05f7a-145">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="05f7a-146">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="05f7a-146">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="05f7a-147">包含要应用于单个对话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="05f7a-147">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="05f7a-148">文本值</span><span class="sxs-lookup"><span data-stu-id="05f7a-148">Text value</span></span>

<span data-ttu-id="05f7a-149">无。</span><span class="sxs-lookup"><span data-stu-id="05f7a-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05f7a-150">说明</span><span class="sxs-lookup"><span data-stu-id="05f7a-150">Remarks</span></span>

<span data-ttu-id="05f7a-151">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="05f7a-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05f7a-152">元素信息</span><span class="sxs-lookup"><span data-stu-id="05f7a-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05f7a-153">命名空间</span><span class="sxs-lookup"><span data-stu-id="05f7a-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05f7a-154">架构名称</span><span class="sxs-lookup"><span data-stu-id="05f7a-154">Schema Name</span></span>  <br/> |<span data-ttu-id="05f7a-155">类型架构</span><span class="sxs-lookup"><span data-stu-id="05f7a-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="05f7a-156">验证文件</span><span class="sxs-lookup"><span data-stu-id="05f7a-156">Validation File</span></span>  <br/> |<span data-ttu-id="05f7a-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05f7a-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05f7a-158">可以为空</span><span class="sxs-lookup"><span data-stu-id="05f7a-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="05f7a-159">False</span><span class="sxs-lookup"><span data-stu-id="05f7a-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05f7a-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05f7a-160">See also</span></span>



- [<span data-ttu-id="05f7a-161">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="05f7a-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

