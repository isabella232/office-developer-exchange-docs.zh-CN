---
title: CalendarEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEvent
api_type:
- schema
ms.assetid: 91958c01-1fcb-4ac0-8601-5e5b434c988a
description: CalendarEvent 元素均表示唯一日历项匹配项。
ms.openlocfilehash: f7fff7ba511ca12813dd4c2d694e89c97589ba31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753405"
---
# <a name="calendarevent"></a><span data-ttu-id="50b6e-103">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="50b6e-103">CalendarEvent</span></span>

<span data-ttu-id="50b6e-104">**CalendarEvent**元素均表示唯一日历项匹配项。</span><span class="sxs-lookup"><span data-stu-id="50b6e-104">The **CalendarEvent** element represents a unique calendar item occurrence.</span></span> 
  
[<span data-ttu-id="50b6e-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="50b6e-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="50b6e-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="50b6e-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="50b6e-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="50b6e-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="50b6e-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="50b6e-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="50b6e-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="50b6e-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="50b6e-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="50b6e-110">CalendarEvent</span></span>](calendarevent.md)
  
```xml
<CalendarEvent>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
   <BusyType>...</BusyType>
   <CalendarEventDetails>...</CalendarEventDetails>
</CalendarEvent>
```

 <span data-ttu-id="50b6e-111">**CalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="50b6e-111">**CalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50b6e-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="50b6e-112">Attributes and elements</span></span>

<span data-ttu-id="50b6e-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="50b6e-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50b6e-114">属性</span><span class="sxs-lookup"><span data-stu-id="50b6e-114">Attributes</span></span>

<span data-ttu-id="50b6e-115">无。</span><span class="sxs-lookup"><span data-stu-id="50b6e-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50b6e-116">子元素</span><span class="sxs-lookup"><span data-stu-id="50b6e-116">Child elements</span></span>

|<span data-ttu-id="50b6e-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="50b6e-117">**Element**</span></span>|<span data-ttu-id="50b6e-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="50b6e-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50b6e-119">StartTime</span><span class="sxs-lookup"><span data-stu-id="50b6e-119">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="50b6e-120">表示日历事件的开始。</span><span class="sxs-lookup"><span data-stu-id="50b6e-120">Represents the start of a calendar event.</span></span> <span data-ttu-id="50b6e-121">这是一个必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="50b6e-121">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="50b6e-122">结束时间</span><span class="sxs-lookup"><span data-stu-id="50b6e-122">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="50b6e-123">代表日历事件的末尾。</span><span class="sxs-lookup"><span data-stu-id="50b6e-123">Represents the end of a calendar event.</span></span> <span data-ttu-id="50b6e-124">这是一个必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="50b6e-124">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="50b6e-125">BusyType</span><span class="sxs-lookup"><span data-stu-id="50b6e-125">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="50b6e-126">表示为日历事件设置忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="50b6e-126">Represents the free/busy status set for a calendar event.</span></span> <span data-ttu-id="50b6e-127">这是一个必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="50b6e-127">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="50b6e-128">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="50b6e-128">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="50b6e-129">提供日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="50b6e-129">Provides additional information for a calendar event.</span></span> <span data-ttu-id="50b6e-130">这是一个可选子元素。</span><span class="sxs-lookup"><span data-stu-id="50b6e-130">This is an optional child element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50b6e-131">父元素</span><span class="sxs-lookup"><span data-stu-id="50b6e-131">Parent elements</span></span>

|<span data-ttu-id="50b6e-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="50b6e-132">**Element**</span></span>|<span data-ttu-id="50b6e-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="50b6e-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50b6e-134">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="50b6e-134">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="50b6e-135">包含一组唯一的日历项目事件表示所请求的用户的可用性。</span><span class="sxs-lookup"><span data-stu-id="50b6e-135">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> <span data-ttu-id="50b6e-136">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="50b6e-136">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50b6e-137">注解</span><span class="sxs-lookup"><span data-stu-id="50b6e-137">Remarks</span></span>

<span data-ttu-id="50b6e-138">客户端的时区中返回的约会和会议的时间。</span><span class="sxs-lookup"><span data-stu-id="50b6e-138">The appointment and meeting times are returned in the time zone of the client.</span></span> <span data-ttu-id="50b6e-139">中发生的顺序排列的所有子元素。</span><span class="sxs-lookup"><span data-stu-id="50b6e-139">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="50b6e-140">提供此元素的详细程度取决于所请求者授予的权限。</span><span class="sxs-lookup"><span data-stu-id="50b6e-140">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="50b6e-141">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="50b6e-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50b6e-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="50b6e-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50b6e-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="50b6e-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50b6e-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="50b6e-144">Schema Name</span></span>  <br/> |<span data-ttu-id="50b6e-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="50b6e-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="50b6e-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="50b6e-146">Validation File</span></span>  <br/> |<span data-ttu-id="50b6e-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="50b6e-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="50b6e-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="50b6e-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="50b6e-149">False</span><span class="sxs-lookup"><span data-stu-id="50b6e-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50b6e-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="50b6e-150">See also</span></span>



[<span data-ttu-id="50b6e-151">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="50b6e-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="50b6e-152">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="50b6e-152">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="50b6e-153">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="50b6e-153">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

