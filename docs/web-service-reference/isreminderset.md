---
title: IsReminderSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsReminderSet
api_type:
- schema
ms.assetid: 6aea4cb7-ca14-4949-8e7f-660b565f6556
description: IsReminderSet 元素指示是否已设置日历事件提醒。
ms.openlocfilehash: 589178072baca652bff2779e64a212fb90478247
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826100"
---
# <a name="isreminderset"></a><span data-ttu-id="87357-103">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="87357-103">IsReminderSet</span></span>

<span data-ttu-id="87357-104">**IsReminderSet**元素指示是否已设置日历事件提醒。</span><span class="sxs-lookup"><span data-stu-id="87357-104">The **IsReminderSet** element indicates whether a reminder has been set for the calendar event.</span></span> 
  
[<span data-ttu-id="87357-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="87357-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="87357-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="87357-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="87357-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="87357-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="87357-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="87357-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="87357-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="87357-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="87357-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="87357-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="87357-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="87357-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="87357-112">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="87357-112">IsReminderSet</span></span>](isreminderset.md)
  
```xml
<IsReminderSet>true or false</IsReminderSet>
```

 <span data-ttu-id="87357-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="87357-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="87357-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="87357-114">Attributes and elements</span></span>

<span data-ttu-id="87357-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="87357-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87357-116">属性</span><span class="sxs-lookup"><span data-stu-id="87357-116">Attributes</span></span>

<span data-ttu-id="87357-117">无。</span><span class="sxs-lookup"><span data-stu-id="87357-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="87357-118">子元素</span><span class="sxs-lookup"><span data-stu-id="87357-118">Child elements</span></span>

<span data-ttu-id="87357-119">无。</span><span class="sxs-lookup"><span data-stu-id="87357-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="87357-120">父元素</span><span class="sxs-lookup"><span data-stu-id="87357-120">Parent elements</span></span>

|<span data-ttu-id="87357-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="87357-121">**Element**</span></span>|<span data-ttu-id="87357-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="87357-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87357-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="87357-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="87357-124">提供有关日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="87357-124">Provides additional information about a calendar event.</span></span>  <br/> <span data-ttu-id="87357-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="87357-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="87357-126">文本值</span><span class="sxs-lookup"><span data-stu-id="87357-126">Text value</span></span>

<span data-ttu-id="87357-127">此元素响应中返回时所需的文本值。</span><span class="sxs-lookup"><span data-stu-id="87357-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="87357-128">如果[CalendarEventDetails](calendareventdetails.md)元素使用除非[IsPrivate](isprivate.md)元素设置为**true**，则需要此元素。</span><span class="sxs-lookup"><span data-stu-id="87357-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used unless the [IsPrivate](isprivate.md) element is set to **true**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="87357-129">备注</span><span class="sxs-lookup"><span data-stu-id="87357-129">Remarks</span></span>

<span data-ttu-id="87357-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="87357-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="87357-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="87357-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87357-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="87357-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="87357-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="87357-133">Schema Name</span></span>  <br/> |<span data-ttu-id="87357-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="87357-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="87357-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="87357-135">Validation File</span></span>  <br/> |<span data-ttu-id="87357-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="87357-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="87357-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="87357-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="87357-138">False</span><span class="sxs-lookup"><span data-stu-id="87357-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87357-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="87357-139">See also</span></span>



[<span data-ttu-id="87357-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="87357-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="87357-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="87357-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="87357-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="87357-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

