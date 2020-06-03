---
title: IsRecurring （CalendarEventDetails）
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
ms.assetid: 42323940-0ccb-4a05-86e4-262bde5e41b0
description: IsRecurring 元素指示 calendar 事件是定期日历项目的实例还是单个日历项目。
ms.openlocfilehash: f9a9c8b4d2a20d42dbec7cd6fd36935eb0b941f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530251"
---
# <a name="isrecurring-calendareventdetails"></a><span data-ttu-id="f9f32-103">IsRecurring （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="f9f32-103">IsRecurring (CalendarEventDetails)</span></span>

<span data-ttu-id="f9f32-104">**IsRecurring**元素指示 calendar 事件是定期日历项目的实例还是单个日历项目。</span><span class="sxs-lookup"><span data-stu-id="f9f32-104">The **IsRecurring** element indicates whether the calendar event is an instance of a recurring calendar item or a single calendar item.</span></span> 
  
[<span data-ttu-id="f9f32-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f9f32-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="f9f32-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="f9f32-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="f9f32-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="f9f32-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="f9f32-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="f9f32-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="f9f32-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="f9f32-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="f9f32-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="f9f32-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="f9f32-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="f9f32-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="f9f32-112">IsRecurring （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="f9f32-112">IsRecurring (CalendarEventDetails)</span></span>](isrecurring-calendareventdetails.md)
  
```xml
<IsRecurring>true or false</IsRecurring>
```

 <span data-ttu-id="f9f32-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="f9f32-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9f32-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f9f32-114">Attributes and elements</span></span>

<span data-ttu-id="f9f32-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f9f32-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9f32-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="f9f32-116">Attributes</span></span>

<span data-ttu-id="f9f32-117">无。</span><span class="sxs-lookup"><span data-stu-id="f9f32-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9f32-118">子元素</span><span class="sxs-lookup"><span data-stu-id="f9f32-118">Child elements</span></span>

<span data-ttu-id="f9f32-119">无。</span><span class="sxs-lookup"><span data-stu-id="f9f32-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9f32-120">父元素</span><span class="sxs-lookup"><span data-stu-id="f9f32-120">Parent elements</span></span>

|<span data-ttu-id="f9f32-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="f9f32-121">**Element**</span></span>|<span data-ttu-id="f9f32-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="f9f32-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9f32-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="f9f32-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="f9f32-124">提供有关日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="f9f32-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="f9f32-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f9f32-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f9f32-126">文本值</span><span class="sxs-lookup"><span data-stu-id="f9f32-126">Text value</span></span>

<span data-ttu-id="f9f32-127">如果在响应中返回此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="f9f32-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="f9f32-128">如果使用[CalendarEventDetails](calendareventdetails.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="f9f32-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f9f32-129">说明</span><span class="sxs-lookup"><span data-stu-id="f9f32-129">Remarks</span></span>

<span data-ttu-id="f9f32-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f9f32-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9f32-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="f9f32-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9f32-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="f9f32-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9f32-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="f9f32-133">Schema Name</span></span>  <br/> |<span data-ttu-id="f9f32-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="f9f32-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9f32-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="f9f32-135">Validation File</span></span>  <br/> |<span data-ttu-id="f9f32-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f9f32-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9f32-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="f9f32-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="f9f32-138">False</span><span class="sxs-lookup"><span data-stu-id="f9f32-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9f32-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f9f32-139">See also</span></span>



[<span data-ttu-id="f9f32-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="f9f32-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="f9f32-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f9f32-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="f9f32-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="f9f32-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

