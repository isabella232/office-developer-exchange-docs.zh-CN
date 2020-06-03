---
title: IsRecurring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: IsRecurring 元素指示日历项目、会议请求或任务是否为定期项目的一部分。 此元素是只读的。
ms.openlocfilehash: 72c71c1955b69f1c0df855ce4bd0ed02d4c89122
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526485"
---
# <a name="isrecurring"></a><span data-ttu-id="5d748-104">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5d748-104">IsRecurring</span></span>

<span data-ttu-id="5d748-105">**IsRecurring**元素指示日历项目、会议请求或任务是否为定期项目的一部分。</span><span class="sxs-lookup"><span data-stu-id="5d748-105">The **IsRecurring** element indicates whether a calendar item, meeting request, or task is part of a recurring item.</span></span> <span data-ttu-id="5d748-106">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="5d748-106">This element is read-only.</span></span> 
  
```xml
<IsRecurring/>
```

 <span data-ttu-id="5d748-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5d748-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d748-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5d748-108">Attributes and elements</span></span>

<span data-ttu-id="5d748-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5d748-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d748-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="5d748-110">Attributes</span></span>

<span data-ttu-id="5d748-111">无。</span><span class="sxs-lookup"><span data-stu-id="5d748-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d748-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5d748-112">Child elements</span></span>

<span data-ttu-id="5d748-113">无。</span><span class="sxs-lookup"><span data-stu-id="5d748-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5d748-114">父元素</span><span class="sxs-lookup"><span data-stu-id="5d748-114">Parent elements</span></span>

|<span data-ttu-id="5d748-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d748-115">**Element**</span></span>|<span data-ttu-id="5d748-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d748-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d748-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5d748-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5d748-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="5d748-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5d748-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5d748-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5d748-120">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="5d748-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="5d748-121">任务</span><span class="sxs-lookup"><span data-stu-id="5d748-121">Task</span></span>](task.md) <br/> |<span data-ttu-id="5d748-122">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="5d748-122">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5d748-123">文本值</span><span class="sxs-lookup"><span data-stu-id="5d748-123">Text value</span></span>

<span data-ttu-id="5d748-124">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="5d748-124">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d748-125">备注</span><span class="sxs-lookup"><span data-stu-id="5d748-125">Remarks</span></span>

<span data-ttu-id="5d748-126">下表显示了如何为组织者和与会者以及会议请求和更新的不同日历项目类型设置**IsRecurring**属性。</span><span class="sxs-lookup"><span data-stu-id="5d748-126">The following table shows how the **IsRecurring** property is set for different calendar item types for organizers and attendees and for meeting requests and updates.</span></span> 
  
|<span data-ttu-id="5d748-127">**CalendarItem 类型**</span><span class="sxs-lookup"><span data-stu-id="5d748-127">**CalendarItem Type**</span></span>|<span data-ttu-id="5d748-128">**组织者 <br/> （IsRecurring）**</span><span class="sxs-lookup"><span data-stu-id="5d748-128">**Organizer  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="5d748-129">**与会者 <br/> （IsRecurring）**</span><span class="sxs-lookup"><span data-stu-id="5d748-129">**Attendee  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="5d748-130">**会议请求/更新 <br/> （IsRecurring）**</span><span class="sxs-lookup"><span data-stu-id="5d748-130">**Meeting request/update  <br/> (IsRecurring)**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5d748-131">单个事件</span><span class="sxs-lookup"><span data-stu-id="5d748-131">Single Occurrence</span></span>  <br/> |<span data-ttu-id="5d748-132">**该值**</span><span class="sxs-lookup"><span data-stu-id="5d748-132">**FALSE**</span></span> <br/> |<span data-ttu-id="5d748-133">**该值**</span><span class="sxs-lookup"><span data-stu-id="5d748-133">**FALSE**</span></span> <br/> |<span data-ttu-id="5d748-134">**该值**</span><span class="sxs-lookup"><span data-stu-id="5d748-134">**FALSE**</span></span> <br/> |
|<span data-ttu-id="5d748-135">定期母版</span><span class="sxs-lookup"><span data-stu-id="5d748-135">Recurring Master</span></span>  <br/> |<span data-ttu-id="5d748-136">**该值**</span><span class="sxs-lookup"><span data-stu-id="5d748-136">**FALSE**</span></span> <br/> |<span data-ttu-id="5d748-137">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5d748-137">**TRUE**</span></span> <br/> |<span data-ttu-id="5d748-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5d748-138">**TRUE**</span></span> <br/> |
|<span data-ttu-id="5d748-139">定期异常</span><span class="sxs-lookup"><span data-stu-id="5d748-139">Recurring Exception</span></span>  <br/> |<span data-ttu-id="5d748-140">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5d748-140">**TRUE**</span></span> <br/> |<span data-ttu-id="5d748-141">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5d748-141">**TRUE**</span></span> <br/> |<span data-ttu-id="5d748-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5d748-142">**TRUE**</span></span> <br/> |
   
<span data-ttu-id="5d748-143">为组织者的定期主日历项目设置的**IsRecurring**属性值不正确;此值应设置为**TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5d748-143">The **IsRecurring** property value that is set for recurring master calendar items for the organizer is incorrect; this value should be set to **TRUE**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5d748-144">GetUserAvailability 操作还具有[IsRecurring （CalendarEventDetails）](isrecurring-calendareventdetails.md)元素。</span><span class="sxs-lookup"><span data-stu-id="5d748-144">The GetUserAvailability operation also has an [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) element.</span></span> 
  
<span data-ttu-id="5d748-145">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5d748-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d748-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="5d748-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d748-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="5d748-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d748-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="5d748-148">Schema name</span></span>  <br/> |<span data-ttu-id="5d748-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="5d748-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="5d748-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="5d748-150">Validation file</span></span>  <br/> |<span data-ttu-id="5d748-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5d748-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d748-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="5d748-152">Can be empty</span></span>  <br/> |<span data-ttu-id="5d748-153">False</span><span class="sxs-lookup"><span data-stu-id="5d748-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d748-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d748-154">See also</span></span>



[<span data-ttu-id="5d748-155">TaskType。 IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5d748-155">TaskType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[<span data-ttu-id="5d748-156">CalendarEventDetails。 IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5d748-156">CalendarEventDetails.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[<span data-ttu-id="5d748-157">CalendarItemType。 IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5d748-157">CalendarItemType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[<span data-ttu-id="5d748-158">MeetingRequestMessageType。 IsRecurring</span><span class="sxs-lookup"><span data-stu-id="5d748-158">MeetingRequestMessageType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[<span data-ttu-id="5d748-159">CalendarItemType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="5d748-159">CalendarItemType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="5d748-160">MeetingRequestMessageType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="5d748-160">MeetingRequestMessageType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="5d748-161">TaskType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="5d748-161">TaskType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [<span data-ttu-id="5d748-162">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5d748-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

