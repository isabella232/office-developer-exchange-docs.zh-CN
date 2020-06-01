---
title: Location （CalendarEventDetails）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Location
api_type:
- schema
ms.assetid: 883cce6e-66b8-4dbc-935c-83ef5100a953
description: Location 元素表示日历项目的位置字段。
ms.openlocfilehash: 4a590c315d2211ce9128305a514e68f1c785596c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467996"
---
# <a name="location-calendareventdetails"></a><span data-ttu-id="dd9f7-103">Location （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="dd9f7-103">Location (CalendarEventDetails)</span></span>

<span data-ttu-id="dd9f7-104">**Location**元素表示日历项目的位置字段。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-104">The **Location** element represents the location field of the calendar item.</span></span> 
  
[<span data-ttu-id="dd9f7-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dd9f7-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="dd9f7-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="dd9f7-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="dd9f7-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="dd9f7-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="dd9f7-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="dd9f7-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="dd9f7-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="dd9f7-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="dd9f7-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="dd9f7-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="dd9f7-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="dd9f7-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="dd9f7-112">Location （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="dd9f7-112">Location (CalendarEventDetails)</span></span>](location-calendareventdetails.md)
  
```xml
<Location/>
```

 <span data-ttu-id="dd9f7-113">**string**</span><span class="sxs-lookup"><span data-stu-id="dd9f7-113">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd9f7-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dd9f7-114">Attributes and elements</span></span>

<span data-ttu-id="dd9f7-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd9f7-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="dd9f7-116">Attributes</span></span>

<span data-ttu-id="dd9f7-117">无。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd9f7-118">子元素</span><span class="sxs-lookup"><span data-stu-id="dd9f7-118">Child elements</span></span>

<span data-ttu-id="dd9f7-119">无。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dd9f7-120">父元素</span><span class="sxs-lookup"><span data-stu-id="dd9f7-120">Parent elements</span></span>

|<span data-ttu-id="dd9f7-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="dd9f7-121">**Element**</span></span>|<span data-ttu-id="dd9f7-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="dd9f7-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dd9f7-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="dd9f7-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="dd9f7-124">提供日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-124">Provides additional information for a calendar event.</span></span>  <br/> <span data-ttu-id="dd9f7-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="dd9f7-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dd9f7-126">文本值</span><span class="sxs-lookup"><span data-stu-id="dd9f7-126">Text value</span></span>

<span data-ttu-id="dd9f7-127">如果在响应中返回此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="dd9f7-128">此元素可以包含空字符串。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-128">This element can contain an empty string.</span></span> <span data-ttu-id="dd9f7-129">如果使用[CalendarEventDetails](calendareventdetails.md)元素，则此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-129">This element is optional if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dd9f7-130">备注</span><span class="sxs-lookup"><span data-stu-id="dd9f7-130">Remarks</span></span>

<span data-ttu-id="dd9f7-131">此元素映射到 PR_Location MAPI 命名属性。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-131">This element maps to a PR_Location MAPI named property.</span></span>
  
<span data-ttu-id="dd9f7-132">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dd9f7-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd9f7-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="dd9f7-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd9f7-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="dd9f7-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dd9f7-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="dd9f7-135">Schema Name</span></span>  <br/> |<span data-ttu-id="dd9f7-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="dd9f7-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="dd9f7-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="dd9f7-137">Validation File</span></span>  <br/> |<span data-ttu-id="dd9f7-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dd9f7-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dd9f7-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="dd9f7-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="dd9f7-140">False</span><span class="sxs-lookup"><span data-stu-id="dd9f7-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd9f7-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dd9f7-141">See also</span></span>



[<span data-ttu-id="dd9f7-142">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="dd9f7-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="dd9f7-143">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dd9f7-143">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="dd9f7-144">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="dd9f7-144">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

