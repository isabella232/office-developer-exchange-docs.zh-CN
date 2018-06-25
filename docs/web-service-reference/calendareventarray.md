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
description: CalendarEventArray 元素包含一组唯一的日历项目事件表示所请求的用户的可用性。
ms.openlocfilehash: 2e56b7b2b94e12401ba708dfca94101064d625e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753406"
---
# <a name="calendareventarray"></a><span data-ttu-id="a01bd-103">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="a01bd-103">CalendarEventArray</span></span>

<span data-ttu-id="a01bd-104">**CalendarEventArray**元素包含一组唯一的日历项目事件表示所请求的用户的可用性。</span><span class="sxs-lookup"><span data-stu-id="a01bd-104">The **CalendarEventArray** element contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span> 
  
[<span data-ttu-id="a01bd-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a01bd-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="a01bd-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="a01bd-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="a01bd-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="a01bd-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="a01bd-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="a01bd-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="a01bd-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="a01bd-109">CalendarEventArray</span></span>](calendareventarray.md)
  
```xml
<CalendarEventArray>
   <CalendarEvent>...</CalendarEvent>
</CalendarEventArray>
```

 <span data-ttu-id="a01bd-110">**ArrayOfCalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="a01bd-110">**ArrayOfCalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a01bd-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a01bd-111">Attributes and elements</span></span>

<span data-ttu-id="a01bd-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a01bd-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a01bd-113">属性</span><span class="sxs-lookup"><span data-stu-id="a01bd-113">Attributes</span></span>

<span data-ttu-id="a01bd-114">无。</span><span class="sxs-lookup"><span data-stu-id="a01bd-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a01bd-115">子元素</span><span class="sxs-lookup"><span data-stu-id="a01bd-115">Child elements</span></span>

|<span data-ttu-id="a01bd-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a01bd-116">**Element**</span></span>|<span data-ttu-id="a01bd-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a01bd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a01bd-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="a01bd-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="a01bd-119">代表独特的日历项匹配项。</span><span class="sxs-lookup"><span data-stu-id="a01bd-119">Represents a unique calendar item occurrence.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a01bd-120">父元素</span><span class="sxs-lookup"><span data-stu-id="a01bd-120">Parent elements</span></span>

|<span data-ttu-id="a01bd-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="a01bd-121">**Element**</span></span>|<span data-ttu-id="a01bd-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="a01bd-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a01bd-123">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="a01bd-123">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="a01bd-124">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="a01bd-124">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="a01bd-125">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="a01bd-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a01bd-126">注解</span><span class="sxs-lookup"><span data-stu-id="a01bd-126">Remarks</span></span>

<span data-ttu-id="a01bd-127">提供此元素的详细程度取决于所请求者授予的权限。</span><span class="sxs-lookup"><span data-stu-id="a01bd-127">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span> <span data-ttu-id="a01bd-128">[FreeBusyViewType](freebusyviewtype.md)元素设置为**FreeBusy**、 **FreeBusyMerged**、 **Detailed**或**DetailedMerged**时包含此元素。</span><span class="sxs-lookup"><span data-stu-id="a01bd-128">This element is included when the [FreeBusyViewType](freebusyviewtype.md) element is set to **FreeBusy**, **FreeBusyMerged**, **Detailed**, or **DetailedMerged**.</span></span> <span data-ttu-id="a01bd-129">如果没有日历项目存在于请求的时间窗口中，此元素不包括任何子元素。</span><span class="sxs-lookup"><span data-stu-id="a01bd-129">This element does not include any child elements if no calendar items are present in the requested time window.</span></span> 
  
<span data-ttu-id="a01bd-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a01bd-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a01bd-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="a01bd-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a01bd-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="a01bd-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a01bd-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="a01bd-133">Schema Name</span></span>  <br/> |<span data-ttu-id="a01bd-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="a01bd-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="a01bd-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="a01bd-135">Validation File</span></span>  <br/> |<span data-ttu-id="a01bd-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a01bd-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a01bd-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="a01bd-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="a01bd-138">False</span><span class="sxs-lookup"><span data-stu-id="a01bd-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a01bd-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a01bd-139">See also</span></span>



[<span data-ttu-id="a01bd-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="a01bd-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="a01bd-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a01bd-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="a01bd-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="a01bd-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

