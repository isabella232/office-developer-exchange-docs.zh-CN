---
title: Subject （CalendarEventDetails）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subject
api_type:
- schema
ms.assetid: 05e955b5-8e90-4043-b06b-6ce523eaed9b
description: Subject 元素表示日历项目的主题。
ms.openlocfilehash: 268e5fa4bb8d02d83154267fc8e475c6d2b7c31c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463053"
---
# <a name="subject-calendareventdetails"></a><span data-ttu-id="5cdce-103">Subject （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="5cdce-103">Subject (CalendarEventDetails)</span></span>

<span data-ttu-id="5cdce-104">**Subject**元素表示日历项目的主题。</span><span class="sxs-lookup"><span data-stu-id="5cdce-104">The **Subject** element represents the subject of a calendar item.</span></span> 
  
[<span data-ttu-id="5cdce-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5cdce-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="5cdce-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="5cdce-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="5cdce-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="5cdce-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="5cdce-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="5cdce-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="5cdce-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="5cdce-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="5cdce-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="5cdce-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="5cdce-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="5cdce-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="5cdce-112">Subject （CalendarEventDetails）</span><span class="sxs-lookup"><span data-stu-id="5cdce-112">Subject (CalendarEventDetails)</span></span>](subject-calendareventdetails.md)
  
```xml
<Subject/>
```

 <span data-ttu-id="5cdce-113">**string**</span><span class="sxs-lookup"><span data-stu-id="5cdce-113">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5cdce-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5cdce-114">Attributes and elements</span></span>

<span data-ttu-id="5cdce-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5cdce-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5cdce-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="5cdce-116">Attributes</span></span>

<span data-ttu-id="5cdce-117">无。</span><span class="sxs-lookup"><span data-stu-id="5cdce-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5cdce-118">子元素</span><span class="sxs-lookup"><span data-stu-id="5cdce-118">Child elements</span></span>

<span data-ttu-id="5cdce-119">无。</span><span class="sxs-lookup"><span data-stu-id="5cdce-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5cdce-120">父元素</span><span class="sxs-lookup"><span data-stu-id="5cdce-120">Parent elements</span></span>

|<span data-ttu-id="5cdce-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="5cdce-121">**Element**</span></span>|<span data-ttu-id="5cdce-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="5cdce-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cdce-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="5cdce-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="5cdce-124">提供日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="5cdce-124">Provides additional information for a calendar event.</span></span>  <br/> <span data-ttu-id="5cdce-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="5cdce-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5cdce-126">文本值</span><span class="sxs-lookup"><span data-stu-id="5cdce-126">Text value</span></span>

<span data-ttu-id="5cdce-127">如果在响应中返回此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="5cdce-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="5cdce-128">如果[IsPrivate](isprivate.md)元素的值等于**true**，则不会返回此元素。</span><span class="sxs-lookup"><span data-stu-id="5cdce-128">This element will not be returned if the [IsPrivate](isprivate.md) element value is equal to **true**.</span></span> <span data-ttu-id="5cdce-129">此元素可以包含空字符串。</span><span class="sxs-lookup"><span data-stu-id="5cdce-129">This element can contain an empty string.</span></span> <span data-ttu-id="5cdce-130">如果使用[CalendarEventDetails](calendareventdetails.md)元素，则此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="5cdce-130">This element is optional if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5cdce-131">说明</span><span class="sxs-lookup"><span data-stu-id="5cdce-131">Remarks</span></span>

<span data-ttu-id="5cdce-132">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5cdce-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cdce-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="5cdce-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cdce-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="5cdce-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5cdce-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="5cdce-135">Schema Name</span></span>  <br/> |<span data-ttu-id="5cdce-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="5cdce-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="5cdce-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="5cdce-137">Validation File</span></span>  <br/> |<span data-ttu-id="5cdce-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5cdce-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5cdce-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="5cdce-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="5cdce-140">False</span><span class="sxs-lookup"><span data-stu-id="5cdce-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5cdce-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5cdce-141">See also</span></span>



[<span data-ttu-id="5cdce-142">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="5cdce-142">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="5cdce-143">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5cdce-143">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="5cdce-144">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="5cdce-144">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

