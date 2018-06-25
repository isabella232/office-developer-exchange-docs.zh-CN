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
description: IsRecurring 元素指示日历项目、 会议请求或任务是否是定期项目的一部分。 此元素是只读的。
ms.openlocfilehash: dfb0c28fe225792c7128409a8cf010627c624fe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826104"
---
# <a name="isrecurring"></a><span data-ttu-id="af806-104">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="af806-104">IsRecurring</span></span>

<span data-ttu-id="af806-105">**IsRecurring**元素指示日历项目、 会议请求或任务是否是定期项目的一部分。</span><span class="sxs-lookup"><span data-stu-id="af806-105">The **IsRecurring** element indicates whether a calendar item, meeting request, or task is part of a recurring item.</span></span> <span data-ttu-id="af806-106">此元素是只读的。</span><span class="sxs-lookup"><span data-stu-id="af806-106">This element is read-only.</span></span> 
  
```xml
<IsRecurring/>
```

 <span data-ttu-id="af806-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="af806-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af806-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="af806-108">Attributes and elements</span></span>

<span data-ttu-id="af806-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="af806-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af806-110">属性</span><span class="sxs-lookup"><span data-stu-id="af806-110">Attributes</span></span>

<span data-ttu-id="af806-111">无。</span><span class="sxs-lookup"><span data-stu-id="af806-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af806-112">子元素</span><span class="sxs-lookup"><span data-stu-id="af806-112">Child elements</span></span>

<span data-ttu-id="af806-113">无。</span><span class="sxs-lookup"><span data-stu-id="af806-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="af806-114">父元素</span><span class="sxs-lookup"><span data-stu-id="af806-114">Parent elements</span></span>

|<span data-ttu-id="af806-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="af806-115">**Element**</span></span>|<span data-ttu-id="af806-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="af806-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af806-117">日历项目</span><span class="sxs-lookup"><span data-stu-id="af806-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="af806-118">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="af806-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="af806-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="af806-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="af806-120">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="af806-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="af806-121">任务</span><span class="sxs-lookup"><span data-stu-id="af806-121">Task</span></span>](task.md) <br/> |<span data-ttu-id="af806-122">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="af806-122">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="af806-123">文本值</span><span class="sxs-lookup"><span data-stu-id="af806-123">Text value</span></span>

<span data-ttu-id="af806-124">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="af806-124">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af806-125">注解</span><span class="sxs-lookup"><span data-stu-id="af806-125">Remarks</span></span>

<span data-ttu-id="af806-126">下表显示了如何将**IsRecurring**属性设置为不同的日历项目类型为组织者和与会者和会议请求和更新。</span><span class="sxs-lookup"><span data-stu-id="af806-126">The following table shows how the **IsRecurring** property is set for different calendar item types for organizers and attendees and for meeting requests and updates.</span></span> 
  
|<span data-ttu-id="af806-127">**日历项目类型**</span><span class="sxs-lookup"><span data-stu-id="af806-127">**CalendarItem Type**</span></span>|<span data-ttu-id="af806-128">**组织者<br/>(IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="af806-128">**Organizer  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="af806-129">**与会者<br/>(IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="af806-129">**Attendee  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="af806-130">**会议请求/更新<br/>(IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="af806-130">**Meeting request/update  <br/> (IsRecurring)**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="af806-131">一次</span><span class="sxs-lookup"><span data-stu-id="af806-131">Single Occurrence</span></span>  <br/> |<span data-ttu-id="af806-132">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="af806-132">**FALSE**</span></span> <br/> |<span data-ttu-id="af806-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="af806-133">**FALSE**</span></span> <br/> |<span data-ttu-id="af806-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="af806-134">**FALSE**</span></span> <br/> |
|<span data-ttu-id="af806-135">定期主</span><span class="sxs-lookup"><span data-stu-id="af806-135">Recurring Master</span></span>  <br/> |<span data-ttu-id="af806-136">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="af806-136">**FALSE**</span></span> <br/> |<span data-ttu-id="af806-137">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="af806-137">**TRUE**</span></span> <br/> |<span data-ttu-id="af806-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="af806-138">**TRUE**</span></span> <br/> |
|<span data-ttu-id="af806-139">定期例外</span><span class="sxs-lookup"><span data-stu-id="af806-139">Recurring Exception</span></span>  <br/> |<span data-ttu-id="af806-140">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="af806-140">**TRUE**</span></span> <br/> |<span data-ttu-id="af806-141">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="af806-141">**TRUE**</span></span> <br/> |<span data-ttu-id="af806-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="af806-142">**TRUE**</span></span> <br/> |
   
<span data-ttu-id="af806-143">**IsRecurring**属性值为组织者的定期母版日历项目设置不正确。此值应设置为**TRUE**。</span><span class="sxs-lookup"><span data-stu-id="af806-143">The **IsRecurring** property value that is set for recurring master calendar items for the organizer is incorrect; this value should be set to **TRUE**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="af806-144">GetUserAvailability 操作还具有[IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md)元素。</span><span class="sxs-lookup"><span data-stu-id="af806-144">The GetUserAvailability operation also has an [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) element.</span></span> 
  
<span data-ttu-id="af806-145">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="af806-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af806-146">元素信息</span><span class="sxs-lookup"><span data-stu-id="af806-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af806-147">命名空间</span><span class="sxs-lookup"><span data-stu-id="af806-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af806-148">架构名称</span><span class="sxs-lookup"><span data-stu-id="af806-148">Schema name</span></span>  <br/> |<span data-ttu-id="af806-149">类型架构</span><span class="sxs-lookup"><span data-stu-id="af806-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="af806-150">验证文件</span><span class="sxs-lookup"><span data-stu-id="af806-150">Validation file</span></span>  <br/> |<span data-ttu-id="af806-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af806-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af806-152">可以为空</span><span class="sxs-lookup"><span data-stu-id="af806-152">Can be empty</span></span>  <br/> |<span data-ttu-id="af806-153">False</span><span class="sxs-lookup"><span data-stu-id="af806-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af806-154">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af806-154">See also</span></span>



[<span data-ttu-id="af806-155">TaskType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="af806-155">TaskType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[<span data-ttu-id="af806-156">CalendarEventDetails.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="af806-156">CalendarEventDetails.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[<span data-ttu-id="af806-157">CalendarItemType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="af806-157">CalendarItemType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[<span data-ttu-id="af806-158">MeetingRequestMessageType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="af806-158">MeetingRequestMessageType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[<span data-ttu-id="af806-159">CalendarItemType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="af806-159">CalendarItemType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="af806-160">MeetingRequestMessageType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="af806-160">MeetingRequestMessageType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="af806-161">TaskType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="af806-161">TaskType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [<span data-ttu-id="af806-162">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="af806-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

