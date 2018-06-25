---
title: ReminderDueBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReminderDueBy
api_type:
- schema
ms.assetid: e28a0485-86af-4a4e-a2ba-3ad2d4ebff6f
description: ReminderDueBy 元素均表示的日期和时间事件发生。 这使用 ReminderMinutesBeforeStart 元素以确定其何时在显示提醒。
ms.openlocfilehash: cff8142958108635dd9dfaec425af135dee2f2eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827061"
---
# <a name="reminderdueby"></a><span data-ttu-id="b9833-104">ReminderDueBy</span><span class="sxs-lookup"><span data-stu-id="b9833-104">ReminderDueBy</span></span>

<span data-ttu-id="b9833-105">**ReminderDueBy**元素均表示的日期和时间事件发生。</span><span class="sxs-lookup"><span data-stu-id="b9833-105">The **ReminderDueBy** element represents the date and time when the event occurs.</span></span> <span data-ttu-id="b9833-106">这使用[ReminderMinutesBeforeStart](reminderminutesbeforestart.md)元素以确定其何时在显示提醒。</span><span class="sxs-lookup"><span data-stu-id="b9833-106">This is used by the [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) element to determine when the reminder is displayed.</span></span> 
  
```xml
<ReminderDueBy/>
```

 <span data-ttu-id="b9833-107">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="b9833-107">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b9833-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b9833-108">Attributes and elements</span></span>

<span data-ttu-id="b9833-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b9833-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b9833-110">属性</span><span class="sxs-lookup"><span data-stu-id="b9833-110">Attributes</span></span>

<span data-ttu-id="b9833-111">无。</span><span class="sxs-lookup"><span data-stu-id="b9833-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b9833-112">子元素</span><span class="sxs-lookup"><span data-stu-id="b9833-112">Child elements</span></span>

<span data-ttu-id="b9833-113">无。</span><span class="sxs-lookup"><span data-stu-id="b9833-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b9833-114">父元素</span><span class="sxs-lookup"><span data-stu-id="b9833-114">Parent elements</span></span>

|<span data-ttu-id="b9833-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="b9833-115">**Element**</span></span>|<span data-ttu-id="b9833-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="b9833-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b9833-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="b9833-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="b9833-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="b9833-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b9833-119">联系人</span><span class="sxs-lookup"><span data-stu-id="b9833-119">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="b9833-120">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="b9833-120">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="b9833-121">DistributionList</span><span class="sxs-lookup"><span data-stu-id="b9833-121">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="b9833-122">表示通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="b9833-122">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="b9833-123">项目</span><span class="sxs-lookup"><span data-stu-id="b9833-123">Item</span></span>](item.md) <br/> |<span data-ttu-id="b9833-124">表示 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="b9833-124">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b9833-125">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="b9833-125">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="b9833-126">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="b9833-126">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b9833-127">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="b9833-127">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="b9833-128">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="b9833-128">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b9833-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="b9833-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="b9833-130">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="b9833-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b9833-131">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="b9833-131">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="b9833-132">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="b9833-132">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b9833-133">Message</span><span class="sxs-lookup"><span data-stu-id="b9833-133">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="b9833-134">表示 Exchange 电子邮件。</span><span class="sxs-lookup"><span data-stu-id="b9833-134">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="b9833-135">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="b9833-135">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="b9833-136">从 Exchange 存储中删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="b9833-136">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="b9833-137">任务</span><span class="sxs-lookup"><span data-stu-id="b9833-137">Task</span></span>](task.md) <br/> |<span data-ttu-id="b9833-138">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="b9833-138">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b9833-139">文本值</span><span class="sxs-lookup"><span data-stu-id="b9833-139">Text value</span></span>

<span data-ttu-id="b9833-140">文本值表示的日期和提醒到期的时间。</span><span class="sxs-lookup"><span data-stu-id="b9833-140">The text value represents the date and time when a reminder is due.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b9833-141">备注</span><span class="sxs-lookup"><span data-stu-id="b9833-141">Remarks</span></span>

<span data-ttu-id="b9833-142">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b9833-142">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b9833-143">元素信息</span><span class="sxs-lookup"><span data-stu-id="b9833-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b9833-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="b9833-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b9833-145">架构名称</span><span class="sxs-lookup"><span data-stu-id="b9833-145">Schema Name</span></span>  <br/> |<span data-ttu-id="b9833-146">类型架构</span><span class="sxs-lookup"><span data-stu-id="b9833-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="b9833-147">验证文件</span><span class="sxs-lookup"><span data-stu-id="b9833-147">Validation File</span></span>  <br/> |<span data-ttu-id="b9833-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b9833-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b9833-149">可以为空</span><span class="sxs-lookup"><span data-stu-id="b9833-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="b9833-150">False</span><span class="sxs-lookup"><span data-stu-id="b9833-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9833-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b9833-151">See also</span></span>



- [<span data-ttu-id="b9833-152">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b9833-152">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

