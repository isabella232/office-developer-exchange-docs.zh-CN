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
description: IsPrivate 元素指示日历项目是否是私有的。
ms.openlocfilehash: c36c659414700439436cd2ca903e443164c1473b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457800"
---
# <a name="isprivate"></a><span data-ttu-id="74390-103">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="74390-103">IsPrivate</span></span>

<span data-ttu-id="74390-104">**IsPrivate**元素指示日历项目是否是私有的。</span><span class="sxs-lookup"><span data-stu-id="74390-104">The **IsPrivate** element indicates whether the calendar item is private.</span></span> 
  
[<span data-ttu-id="74390-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="74390-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="74390-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="74390-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="74390-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="74390-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="74390-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="74390-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="74390-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="74390-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="74390-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="74390-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="74390-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="74390-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="74390-112">IsPrivate</span><span class="sxs-lookup"><span data-stu-id="74390-112">IsPrivate</span></span>](isprivate.md)
  
```xml
<IsPrivate>true or false</IsPrivate>
```

 <span data-ttu-id="74390-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="74390-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="74390-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="74390-114">Attributes and elements</span></span>

<span data-ttu-id="74390-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="74390-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="74390-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="74390-116">Attributes</span></span>

<span data-ttu-id="74390-117">无。</span><span class="sxs-lookup"><span data-stu-id="74390-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="74390-118">子元素</span><span class="sxs-lookup"><span data-stu-id="74390-118">Child elements</span></span>

<span data-ttu-id="74390-119">无。</span><span class="sxs-lookup"><span data-stu-id="74390-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="74390-120">父元素</span><span class="sxs-lookup"><span data-stu-id="74390-120">Parent elements</span></span>

|<span data-ttu-id="74390-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="74390-121">**Element**</span></span>|<span data-ttu-id="74390-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="74390-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="74390-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="74390-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="74390-124">提供有关日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="74390-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="74390-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="74390-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="74390-126">文本值</span><span class="sxs-lookup"><span data-stu-id="74390-126">Text value</span></span>

<span data-ttu-id="74390-127">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="74390-127">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="74390-128">备注</span><span class="sxs-lookup"><span data-stu-id="74390-128">Remarks</span></span>

<span data-ttu-id="74390-129">如果使用此元素，则[CalendarEventDetails](calendareventdetails.md)元素中的其他元素将不包含在响应中。</span><span class="sxs-lookup"><span data-stu-id="74390-129">If this element is used, the other elements in the [CalendarEventDetails](calendareventdetails.md) element will not be included in the response.</span></span> 
  
<span data-ttu-id="74390-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="74390-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="74390-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="74390-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74390-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="74390-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="74390-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="74390-133">Schema Name</span></span>  <br/> |<span data-ttu-id="74390-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="74390-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="74390-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="74390-135">Validation File</span></span>  <br/> |<span data-ttu-id="74390-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="74390-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="74390-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="74390-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="74390-138">False</span><span class="sxs-lookup"><span data-stu-id="74390-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74390-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="74390-139">See also</span></span>



[<span data-ttu-id="74390-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="74390-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="74390-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="74390-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="74390-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="74390-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

