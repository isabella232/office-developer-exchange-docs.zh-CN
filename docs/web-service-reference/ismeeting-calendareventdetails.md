---
title: IsMeeting (CalendarEventDetails)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsMeeting
api_type:
- schema
ms.assetid: dd6900e4-e4a3-471a-909d-7240ebec501b
description: IsMeeting 元素指示日历事件是否为会议或约会。
ms.openlocfilehash: b75dfba203177d6451f3847bf8d1f68014612e1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465994"
---
# <a name="ismeeting-calendareventdetails"></a><span data-ttu-id="ee437-103">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="ee437-103">IsMeeting (CalendarEventDetails)</span></span>

<span data-ttu-id="ee437-104">**IsMeeting**元素指示日历事件是否为会议或约会。</span><span class="sxs-lookup"><span data-stu-id="ee437-104">The **IsMeeting** element indicates whether the calendar event is a meeting or an appointment.</span></span> 
  
[<span data-ttu-id="ee437-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ee437-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ee437-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="ee437-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="ee437-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ee437-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="ee437-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ee437-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="ee437-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="ee437-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="ee437-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="ee437-110">CalendarEvent</span></span>](calendarevent.md)
  
[<span data-ttu-id="ee437-111">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="ee437-111">CalendarEventDetails</span></span>](calendareventdetails.md)
  
[<span data-ttu-id="ee437-112">IsMeeting (CalendarEventDetails)</span><span class="sxs-lookup"><span data-stu-id="ee437-112">IsMeeting (CalendarEventDetails)</span></span>](ismeeting-calendareventdetails.md)
  
```xml
<IsMeeting>true or false</IsMeeting>
```

 <span data-ttu-id="ee437-113">**boolean**</span><span class="sxs-lookup"><span data-stu-id="ee437-113">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ee437-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ee437-114">Attributes and elements</span></span>

<span data-ttu-id="ee437-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ee437-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee437-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="ee437-116">Attributes</span></span>

<span data-ttu-id="ee437-117">无。</span><span class="sxs-lookup"><span data-stu-id="ee437-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee437-118">子元素</span><span class="sxs-lookup"><span data-stu-id="ee437-118">Child elements</span></span>

<span data-ttu-id="ee437-119">无。</span><span class="sxs-lookup"><span data-stu-id="ee437-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ee437-120">父元素</span><span class="sxs-lookup"><span data-stu-id="ee437-120">Parent elements</span></span>

|<span data-ttu-id="ee437-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="ee437-121">**Element**</span></span>|<span data-ttu-id="ee437-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="ee437-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee437-123">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="ee437-123">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="ee437-124">提供日历事件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="ee437-124">Provides additional information for a calendar event.</span></span>  <br/> <span data-ttu-id="ee437-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="ee437-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]/CalendarEventDetails` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ee437-126">文本值</span><span class="sxs-lookup"><span data-stu-id="ee437-126">Text value</span></span>

<span data-ttu-id="ee437-127">如果在响应中返回此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="ee437-127">A text value is required if this element is returned in the response.</span></span> <span data-ttu-id="ee437-128">如果使用[CalendarEventDetails](calendareventdetails.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="ee437-128">This element is required if the [CalendarEventDetails](calendareventdetails.md) element is used.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ee437-129">备注</span><span class="sxs-lookup"><span data-stu-id="ee437-129">Remarks</span></span>

<span data-ttu-id="ee437-130">会议和约会的区别在于会议是包含与会者的日历项目;约会是不包含与会者的日历项目。</span><span class="sxs-lookup"><span data-stu-id="ee437-130">The difference between a meeting and an appointment is that a meeting is a calendar item that includes attendees; an appointment is a calendar item that does not include attendees.</span></span>
  
<span data-ttu-id="ee437-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ee437-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee437-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="ee437-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee437-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="ee437-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ee437-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="ee437-134">Schema Name</span></span>  <br/> |<span data-ttu-id="ee437-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="ee437-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="ee437-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="ee437-136">Validation File</span></span>  <br/> |<span data-ttu-id="ee437-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ee437-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ee437-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="ee437-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="ee437-139">False</span><span class="sxs-lookup"><span data-stu-id="ee437-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee437-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ee437-140">See also</span></span>



[<span data-ttu-id="ee437-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ee437-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ee437-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ee437-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ee437-143">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="ee437-143">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

