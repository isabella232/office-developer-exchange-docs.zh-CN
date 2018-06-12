---
title: IsPrivate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsPrivate
api_type:
- schema
ms.assetid: 1712bc94-9789-4507-8521-bde1be51e331
description: IsPrivate 元素指示日历项目是否为私有。
ms.openlocfilehash: 37c0357b3eab2314ee74e1c98287b3dc05a3bf26
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826095"
---
# <a name="isprivate"></a><span data-ttu-id="eff2b-103">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="eff2b-103">IsPrivate</span></span>

<span data-ttu-id="eff2b-104">**IsPrivate**元素指示日历项目是否为私有。</span><span class="sxs-lookup"><span data-stu-id="eff2b-104">The **IsPrivate** element indicates whether the calendar item is private.</span></span> 
  
[<span data-ttu-id="eff2b-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="eff2b-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="eff2b-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="eff2b-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="eff2b-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="eff2b-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="eff2b-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="eff2b-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="eff2b-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="eff2b-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="eff2b-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="eff2b-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="eff2b-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="eff2b-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="eff2b-112">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="eff2b-112">IsPrivate</span></span>](isprivate.md)
  
```xml
<IsPrivate>true or false</IsPrivate>
```

 <span data-ttu-id="eff2b-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="eff2b-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eff2b-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eff2b-114">Attributes and elements</span></span>

<span data-ttu-id="eff2b-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eff2b-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eff2b-116">属性</span><span class="sxs-lookup"><span data-stu-id="eff2b-116">Attributes</span></span>

<span data-ttu-id="eff2b-117">无。</span><span class="sxs-lookup"><span data-stu-id="eff2b-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eff2b-118">子元素</span><span class="sxs-lookup"><span data-stu-id="eff2b-118">Child elements</span></span>

<span data-ttu-id="eff2b-119">无。</span><span class="sxs-lookup"><span data-stu-id="eff2b-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="eff2b-120">父元素</span><span class="sxs-lookup"><span data-stu-id="eff2b-120">Parent elements</span></span>

|<span data-ttu-id="eff2b-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="eff2b-121">**Element**</span></span>|<span data-ttu-id="eff2b-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="eff2b-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="eff2b-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="eff2b-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="eff2b-124">提供有关日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="eff2b-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="eff2b-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="eff2b-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="eff2b-126">文本值</span><span class="sxs-lookup"><span data-stu-id="eff2b-126">Text value</span></span>

<span data-ttu-id="eff2b-127">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="eff2b-127">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eff2b-128">备注</span><span class="sxs-lookup"><span data-stu-id="eff2b-128">Remarks</span></span>

<span data-ttu-id="eff2b-129">如果使用此元素，则将不会在响应中包含的[CalendarEventDetails](calendareventdetails.md)元素中的其他元素。</span><span class="sxs-lookup"><span data-stu-id="eff2b-129">If this element is used, the other elements in the [CalendarEventDetails](calendareventdetails.md) element will not be included in the response.</span></span> 
  
<span data-ttu-id="eff2b-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eff2b-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eff2b-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="eff2b-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eff2b-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="eff2b-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="eff2b-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="eff2b-133">Schema Name</span></span>  <br/> |<span data-ttu-id="eff2b-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="eff2b-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="eff2b-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="eff2b-135">Validation File</span></span>  <br/> |<span data-ttu-id="eff2b-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="eff2b-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="eff2b-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="eff2b-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="eff2b-138">False</span><span class="sxs-lookup"><span data-stu-id="eff2b-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eff2b-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eff2b-139">See also</span></span>



[<span data-ttu-id="eff2b-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="eff2b-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="eff2b-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="eff2b-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="eff2b-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="eff2b-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

