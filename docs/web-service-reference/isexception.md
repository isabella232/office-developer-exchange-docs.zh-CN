---
title: IsException
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsException
api_type:
- schema
ms.assetid: e7bd8ae2-2643-411e-ae08-358bac445800
description: IsException 元素指示是否从主控形状更改定期日历项目的实例。
ms.openlocfilehash: bb884110fd3642bebbc03504aef369f9e0412714
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826009"
---
# <a name="isexception"></a><span data-ttu-id="10d30-103">IsException</span><span class="sxs-lookup"><span data-stu-id="10d30-103">IsException</span></span>

<span data-ttu-id="10d30-104">**IsException**元素指示是否从主控形状更改定期日历项目的实例。</span><span class="sxs-lookup"><span data-stu-id="10d30-104">The **IsException** element indicates whether an instance of a recurring calendar item is changed from the master.</span></span> 
  
[<span data-ttu-id="10d30-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="10d30-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="10d30-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="10d30-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="10d30-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="10d30-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="10d30-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="10d30-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="10d30-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="10d30-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="10d30-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="10d30-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="10d30-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="10d30-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="10d30-112">IsException</span><span class="sxs-lookup"><span data-stu-id="10d30-112">IsException</span></span>](isexception.md)
  
```xml
<IsException/>
```

 <span data-ttu-id="10d30-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="10d30-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10d30-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="10d30-114">Attributes and elements</span></span>

<span data-ttu-id="10d30-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="10d30-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10d30-116">属性</span><span class="sxs-lookup"><span data-stu-id="10d30-116">Attributes</span></span>

<span data-ttu-id="10d30-117">无。</span><span class="sxs-lookup"><span data-stu-id="10d30-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10d30-118">子元素</span><span class="sxs-lookup"><span data-stu-id="10d30-118">Child elements</span></span>

<span data-ttu-id="10d30-119">无。</span><span class="sxs-lookup"><span data-stu-id="10d30-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="10d30-120">父元素</span><span class="sxs-lookup"><span data-stu-id="10d30-120">Parent elements</span></span>

|<span data-ttu-id="10d30-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="10d30-121">**Element**</span></span>|<span data-ttu-id="10d30-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="10d30-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10d30-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="10d30-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="10d30-124">提供有关日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="10d30-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="10d30-125">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="10d30-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="10d30-126">文本值</span><span class="sxs-lookup"><span data-stu-id="10d30-126">Text value</span></span>

<span data-ttu-id="10d30-127">此元素响应中返回时所需的文本值。</span><span class="sxs-lookup"><span data-stu-id="10d30-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="10d30-128">如果使用[CalendarEventDetails](calendareventdetails.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="10d30-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10d30-129">备注</span><span class="sxs-lookup"><span data-stu-id="10d30-129">Remarks</span></span>

<span data-ttu-id="10d30-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="10d30-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10d30-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="10d30-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10d30-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="10d30-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="10d30-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="10d30-133">Schema Name</span></span>  <br/> |<span data-ttu-id="10d30-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="10d30-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="10d30-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="10d30-135">Validation File</span></span>  <br/> |<span data-ttu-id="10d30-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="10d30-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="10d30-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="10d30-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="10d30-138">False</span><span class="sxs-lookup"><span data-stu-id="10d30-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10d30-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="10d30-139">See also</span></span>



[<span data-ttu-id="10d30-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="10d30-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="10d30-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="10d30-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="10d30-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="10d30-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

