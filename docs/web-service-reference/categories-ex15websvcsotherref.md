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
description: Categories 元素包含字符串标识的邮箱中项目所属的类别的集合。
ms.openlocfilehash: 8f112a9a736ff4f242b9dfb084b3ad7541cc493d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753441"
---
# <a name="categories"></a><span data-ttu-id="238b1-103">类别</span><span class="sxs-lookup"><span data-stu-id="238b1-103">Categories</span></span>

<span data-ttu-id="238b1-104">**Categories**元素包含字符串标识的邮箱中项目所属的类别的集合。</span><span class="sxs-lookup"><span data-stu-id="238b1-104">The **Categories** element contains a collection of strings that identify the categories to which an item in the mailbox belongs.</span></span> 
  
```XML
<Categories>
   <String/>
</Categories>
```

 <span data-ttu-id="238b1-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="238b1-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="238b1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="238b1-106">Attributes and elements</span></span>

<span data-ttu-id="238b1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="238b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="238b1-108">属性</span><span class="sxs-lookup"><span data-stu-id="238b1-108">Attributes</span></span>

<span data-ttu-id="238b1-109">无。</span><span class="sxs-lookup"><span data-stu-id="238b1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="238b1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="238b1-110">Child elements</span></span>

|<span data-ttu-id="238b1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="238b1-111">**Element**</span></span>|<span data-ttu-id="238b1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="238b1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="238b1-113">字符串</span><span class="sxs-lookup"><span data-stu-id="238b1-113">String</span></span>](string.md) <br/> |<span data-ttu-id="238b1-114">包含标识单个类别的字符串。</span><span class="sxs-lookup"><span data-stu-id="238b1-114">Contains a string that identifies a single category.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="238b1-115">父元素</span><span class="sxs-lookup"><span data-stu-id="238b1-115">Parent elements</span></span>

|<span data-ttu-id="238b1-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="238b1-116">**Element**</span></span>|<span data-ttu-id="238b1-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="238b1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="238b1-118">Item</span><span class="sxs-lookup"><span data-stu-id="238b1-118">Item</span></span>](item.md) <br/> |<span data-ttu-id="238b1-119">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="238b1-119">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="238b1-120">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="238b1-120">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="238b1-121">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="238b1-121">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="238b1-122">Message</span><span class="sxs-lookup"><span data-stu-id="238b1-122">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="238b1-123">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="238b1-123">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="238b1-124">任务</span><span class="sxs-lookup"><span data-stu-id="238b1-124">Task</span></span>](task.md) <br/> |<span data-ttu-id="238b1-125">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="238b1-125">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="238b1-126">日历项目</span><span class="sxs-lookup"><span data-stu-id="238b1-126">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="238b1-127">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="238b1-127">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="238b1-128">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="238b1-128">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="238b1-129">表示单个对话。</span><span class="sxs-lookup"><span data-stu-id="238b1-129">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="238b1-130">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="238b1-130">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="238b1-131">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="238b1-131">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="238b1-132">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="238b1-132">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="238b1-133">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="238b1-133">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="238b1-134">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="238b1-134">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="238b1-135">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="238b1-135">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="238b1-136">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="238b1-136">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="238b1-137">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="238b1-137">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="238b1-138">联系人</span><span class="sxs-lookup"><span data-stu-id="238b1-138">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="238b1-139">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="238b1-139">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="238b1-140">DistributionList</span><span class="sxs-lookup"><span data-stu-id="238b1-140">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="238b1-141">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="238b1-141">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="238b1-142">条件</span><span class="sxs-lookup"><span data-stu-id="238b1-142">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="238b1-143">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="238b1-143">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="238b1-144">异常</span><span class="sxs-lookup"><span data-stu-id="238b1-144">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="238b1-145">代表收件箱规则的所有可用规则例外条件。</span><span class="sxs-lookup"><span data-stu-id="238b1-145">Represents all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
|[<span data-ttu-id="238b1-146">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="238b1-146">ConversationAction</span></span>](conversationaction.md) <br/> |<span data-ttu-id="238b1-147">包含要应用于单个会话的单个操作。</span><span class="sxs-lookup"><span data-stu-id="238b1-147">Contains a single action to be applied to a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="238b1-148">文本值</span><span class="sxs-lookup"><span data-stu-id="238b1-148">Text value</span></span>

<span data-ttu-id="238b1-149">无。</span><span class="sxs-lookup"><span data-stu-id="238b1-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="238b1-150">备注</span><span class="sxs-lookup"><span data-stu-id="238b1-150">Remarks</span></span>

<span data-ttu-id="238b1-151">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="238b1-151">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="238b1-152">元素信息</span><span class="sxs-lookup"><span data-stu-id="238b1-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="238b1-153">命名空间</span><span class="sxs-lookup"><span data-stu-id="238b1-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="238b1-154">架构名称</span><span class="sxs-lookup"><span data-stu-id="238b1-154">Schema Name</span></span>  <br/> |<span data-ttu-id="238b1-155">类型架构</span><span class="sxs-lookup"><span data-stu-id="238b1-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="238b1-156">验证文件</span><span class="sxs-lookup"><span data-stu-id="238b1-156">Validation File</span></span>  <br/> |<span data-ttu-id="238b1-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="238b1-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="238b1-158">可以为空</span><span class="sxs-lookup"><span data-stu-id="238b1-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="238b1-159">False</span><span class="sxs-lookup"><span data-stu-id="238b1-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="238b1-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="238b1-160">See also</span></span>



- [<span data-ttu-id="238b1-161">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="238b1-161">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

