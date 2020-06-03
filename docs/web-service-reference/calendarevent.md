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
description: CalendarEvent 元素表示唯一的日历项目事件。
ms.openlocfilehash: 8bf37c907ed726e33dd2b1eff9add5d6235704da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459074"
---
# <a name="calendarevent"></a><span data-ttu-id="d4ea5-103">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="d4ea5-103">CalendarEvent</span></span>

<span data-ttu-id="d4ea5-104">**CalendarEvent**元素表示唯一的日历项目事件。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-104">The **CalendarEvent** element represents a unique calendar item occurrence.</span></span> 
  
[<span data-ttu-id="d4ea5-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d4ea5-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="d4ea5-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="d4ea5-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="d4ea5-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="d4ea5-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="d4ea5-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="d4ea5-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="d4ea5-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="d4ea5-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="d4ea5-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="d4ea5-110">CalendarEvent</span></span>](calendarevent.md)
  
```xml
<CalendarEvent>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
   <BusyType>...</BusyType>
   <CalendarEventDetails>...</CalendarEventDetails>
</CalendarEvent>
```

 <span data-ttu-id="d4ea5-111">**CalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="d4ea5-111">**CalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4ea5-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d4ea5-112">Attributes and elements</span></span>

<span data-ttu-id="d4ea5-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4ea5-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="d4ea5-114">Attributes</span></span>

<span data-ttu-id="d4ea5-115">无。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4ea5-116">子元素</span><span class="sxs-lookup"><span data-stu-id="d4ea5-116">Child elements</span></span>

|<span data-ttu-id="d4ea5-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="d4ea5-117">**Element**</span></span>|<span data-ttu-id="d4ea5-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d4ea5-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4ea5-119">StartTime</span><span class="sxs-lookup"><span data-stu-id="d4ea5-119">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="d4ea5-120">表示日历事件的开始。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-120">Represents the start of a calendar event.</span></span> <span data-ttu-id="d4ea5-121">这是必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-121">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="d4ea5-122">EndTime</span><span class="sxs-lookup"><span data-stu-id="d4ea5-122">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="d4ea5-123">表示日历事件的结束。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-123">Represents the end of a calendar event.</span></span> <span data-ttu-id="d4ea5-124">这是必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-124">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="d4ea5-125">BusyType</span><span class="sxs-lookup"><span data-stu-id="d4ea5-125">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="d4ea5-126">代表日历事件的忙/闲状态设置。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-126">Represents the free/busy status set for a calendar event.</span></span> <span data-ttu-id="d4ea5-127">这是必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-127">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="d4ea5-128">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="d4ea5-128">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="d4ea5-129">提供日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-129">Provides additional information for a calendar event.</span></span> <span data-ttu-id="d4ea5-130">这是一个可选的子元素。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-130">This is an optional child element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d4ea5-131">父元素</span><span class="sxs-lookup"><span data-stu-id="d4ea5-131">Parent elements</span></span>

|<span data-ttu-id="d4ea5-132">**元素**</span><span class="sxs-lookup"><span data-stu-id="d4ea5-132">**Element**</span></span>|<span data-ttu-id="d4ea5-133">**说明**</span><span class="sxs-lookup"><span data-stu-id="d4ea5-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4ea5-134">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="d4ea5-134">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="d4ea5-135">包含一组代表所请求用户的可用性的唯一的日历项目匹配项。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-135">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> <span data-ttu-id="d4ea5-136">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="d4ea5-136">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4ea5-137">备注</span><span class="sxs-lookup"><span data-stu-id="d4ea5-137">Remarks</span></span>

<span data-ttu-id="d4ea5-138">约会和会议时间按客户端的时区返回。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-138">The appointment and meeting times are returned in the time zone of the client.</span></span> <span data-ttu-id="d4ea5-139">所有子元素都按它们出现的顺序列出。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-139">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="d4ea5-140">此元素提供的详细信息级别取决于授予请求者的权限。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-140">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="d4ea5-141">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d4ea5-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4ea5-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="d4ea5-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4ea5-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="d4ea5-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4ea5-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="d4ea5-144">Schema Name</span></span>  <br/> |<span data-ttu-id="d4ea5-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="d4ea5-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4ea5-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="d4ea5-146">Validation File</span></span>  <br/> |<span data-ttu-id="d4ea5-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d4ea5-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4ea5-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="d4ea5-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="d4ea5-149">False</span><span class="sxs-lookup"><span data-stu-id="d4ea5-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4ea5-150">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d4ea5-150">See also</span></span>



[<span data-ttu-id="d4ea5-151">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="d4ea5-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="d4ea5-152">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d4ea5-152">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="d4ea5-153">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="d4ea5-153">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

