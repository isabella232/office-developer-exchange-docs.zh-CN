---
title: CalendarEventArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventArray
api_type:
- schema
ms.assetid: a00f7f56-d7f1-429d-ae02-97043718c864
description: CalendarEventArray 元素包含表示所请求的用户的可用性的一组唯一的日历项匹配项。
ms.openlocfilehash: 6badba2477a9d48c6d109740de454e2815d3c211
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463368"
---
# <a name="calendareventarray"></a><span data-ttu-id="cbd30-103">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="cbd30-103">CalendarEventArray</span></span>

<span data-ttu-id="cbd30-104">**CalendarEventArray**元素包含表示所请求的用户的可用性的一组唯一的日历项匹配项。</span><span class="sxs-lookup"><span data-stu-id="cbd30-104">The **CalendarEventArray** element contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span> 
  
[<span data-ttu-id="cbd30-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="cbd30-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="cbd30-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="cbd30-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="cbd30-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="cbd30-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="cbd30-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="cbd30-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="cbd30-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="cbd30-109">CalendarEventArray</span></span>](calendareventarray.md)
  
```xml
<CalendarEventArray>
   <CalendarEvent>...</CalendarEvent>
</CalendarEventArray>
```

 <span data-ttu-id="cbd30-110">**ArrayOfCalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="cbd30-110">**ArrayOfCalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cbd30-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cbd30-111">Attributes and elements</span></span>

<span data-ttu-id="cbd30-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cbd30-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbd30-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="cbd30-113">Attributes</span></span>

<span data-ttu-id="cbd30-114">无。</span><span class="sxs-lookup"><span data-stu-id="cbd30-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbd30-115">子元素</span><span class="sxs-lookup"><span data-stu-id="cbd30-115">Child elements</span></span>

|<span data-ttu-id="cbd30-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbd30-116">**Element**</span></span>|<span data-ttu-id="cbd30-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbd30-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbd30-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="cbd30-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="cbd30-119">代表唯一的日历项目事件。</span><span class="sxs-lookup"><span data-stu-id="cbd30-119">Represents a unique calendar item occurrence.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cbd30-120">父元素</span><span class="sxs-lookup"><span data-stu-id="cbd30-120">Parent elements</span></span>

|<span data-ttu-id="cbd30-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbd30-121">**Element**</span></span>|<span data-ttu-id="cbd30-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbd30-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbd30-123">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="cbd30-123">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="cbd30-124">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="cbd30-124">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="cbd30-125">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="cbd30-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbd30-126">备注</span><span class="sxs-lookup"><span data-stu-id="cbd30-126">Remarks</span></span>

<span data-ttu-id="cbd30-127">此元素提供的详细信息级别取决于授予请求者的权限。</span><span class="sxs-lookup"><span data-stu-id="cbd30-127">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span> <span data-ttu-id="cbd30-128">当[FreeBusyViewType](freebusyviewtype.md)元素设置为**FreeBusy**、 **FreeBusyMerged**、**详细**或**DetailedMerged**时，将包含此元素。</span><span class="sxs-lookup"><span data-stu-id="cbd30-128">This element is included when the [FreeBusyViewType](freebusyviewtype.md) element is set to **FreeBusy**, **FreeBusyMerged**, **Detailed**, or **DetailedMerged**.</span></span> <span data-ttu-id="cbd30-129">如果请求的时间窗口中不存在日历项目，则此元素不包含任何子元素。</span><span class="sxs-lookup"><span data-stu-id="cbd30-129">This element does not include any child elements if no calendar items are present in the requested time window.</span></span> 
  
<span data-ttu-id="cbd30-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cbd30-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cbd30-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="cbd30-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbd30-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="cbd30-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cbd30-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="cbd30-133">Schema Name</span></span>  <br/> |<span data-ttu-id="cbd30-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="cbd30-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="cbd30-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="cbd30-135">Validation File</span></span>  <br/> |<span data-ttu-id="cbd30-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cbd30-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cbd30-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="cbd30-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="cbd30-138">False</span><span class="sxs-lookup"><span data-stu-id="cbd30-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbd30-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cbd30-139">See also</span></span>



[<span data-ttu-id="cbd30-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="cbd30-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="cbd30-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="cbd30-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="cbd30-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="cbd30-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

