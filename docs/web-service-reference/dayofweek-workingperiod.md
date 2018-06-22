---
title: DayOfWeek (WorkingPeriod)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 7a8a8cc1-392b-4db5-bb76-710477e31396
description: DayOfWeek 元素包含计划的邮箱用户的工作日的列表。
ms.openlocfilehash: a6a68017291ba13f45b3970307669222d583fcbb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753768"
---
# <a name="dayofweek-workingperiod"></a><span data-ttu-id="5f859-103">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="5f859-103">DayOfWeek (WorkingPeriod)</span></span>

<span data-ttu-id="5f859-104">**DayOfWeek**元素包含计划的邮箱用户的工作日的列表。</span><span class="sxs-lookup"><span data-stu-id="5f859-104">The **DayOfWeek** element contains the list of working days scheduled for the mailbox user.</span></span> 
  
- [<span data-ttu-id="5f859-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5f859-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="5f859-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="5f859-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)  
- [<span data-ttu-id="5f859-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="5f859-107">FreeBusyResponse</span></span>](freebusyresponse.md)  
- [<span data-ttu-id="5f859-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="5f859-108">FreeBusyView</span></span>](freebusyview.md)  
- [<span data-ttu-id="5f859-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="5f859-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)  
- [<span data-ttu-id="5f859-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="5f859-110">WorkingPeriodArray</span></span>](workingperiodarray.md) 
- [<span data-ttu-id="5f859-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="5f859-111">WorkingPeriod</span></span>](workingperiod.md)  
- [<span data-ttu-id="5f859-112">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="5f859-112">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
  
```xml
<DayOfWeek>Sunday Monday Tuesday Wednesday Thursday Friday Saturday</DayOfWeek>
```

<span data-ttu-id="5f859-113">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="5f859-113">**DaysOfWeek**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5f859-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5f859-114">Attributes and elements</span></span>

<span data-ttu-id="5f859-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5f859-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f859-116">属性</span><span class="sxs-lookup"><span data-stu-id="5f859-116">Attributes</span></span>

<span data-ttu-id="5f859-117">无。</span><span class="sxs-lookup"><span data-stu-id="5f859-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f859-118">子元素</span><span class="sxs-lookup"><span data-stu-id="5f859-118">Child elements</span></span>

<span data-ttu-id="5f859-119">无。</span><span class="sxs-lookup"><span data-stu-id="5f859-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f859-120">父元素</span><span class="sxs-lookup"><span data-stu-id="5f859-120">Parent elements</span></span>

|<span data-ttu-id="5f859-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f859-121">**Element**</span></span>|<span data-ttu-id="5f859-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f859-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f859-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="5f859-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="5f859-124">包含工作周的那几天和邮箱用户的时间。</span><span class="sxs-lookup"><span data-stu-id="5f859-124">Contains the work week days and hours of the mailbox user.</span></span><br/><br/><span data-ttu-id="5f859-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="5f859-125">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i[` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f859-126">文本值</span><span class="sxs-lookup"><span data-stu-id="5f859-126">Text value</span></span>

<span data-ttu-id="5f859-127">如果邮箱用户均设置为表示工作周的天，则返回的文本值。</span><span class="sxs-lookup"><span data-stu-id="5f859-127">A text value is returned if the mailbox user has days set to represent the work week.</span></span> <span data-ttu-id="5f859-128">此元素的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="5f859-128">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="5f859-129">星期日</span><span class="sxs-lookup"><span data-stu-id="5f859-129">Sunday</span></span>    
- <span data-ttu-id="5f859-130">周一</span><span class="sxs-lookup"><span data-stu-id="5f859-130">Monday</span></span>    
- <span data-ttu-id="5f859-131">周二</span><span class="sxs-lookup"><span data-stu-id="5f859-131">Tuesday</span></span>    
- <span data-ttu-id="5f859-132">周三</span><span class="sxs-lookup"><span data-stu-id="5f859-132">Wednesday</span></span>    
- <span data-ttu-id="5f859-133">周四</span><span class="sxs-lookup"><span data-stu-id="5f859-133">Thursday</span></span>    
- <span data-ttu-id="5f859-134">周五</span><span class="sxs-lookup"><span data-stu-id="5f859-134">Friday</span></span>    
- <span data-ttu-id="5f859-135">周六</span><span class="sxs-lookup"><span data-stu-id="5f859-135">Saturday</span></span> 
    
<span data-ttu-id="5f859-136">将该顺序返回的文本值。</span><span class="sxs-lookup"><span data-stu-id="5f859-136">The text values will be returned in that order.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f859-137">备注</span><span class="sxs-lookup"><span data-stu-id="5f859-137">Remarks</span></span>

<span data-ttu-id="5f859-138">请务必注意，此元素和可用性[(TimeZone) DayOfWeek](dayofweek-timezone.md)元素之间的区别是类型。</span><span class="sxs-lookup"><span data-stu-id="5f859-138">It is important to note that the difference between this element and the Availability [DayOfWeek (TimeZone)](dayofweek-timezone.md) element is the type.</span></span> 
  
<span data-ttu-id="5f859-139">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5f859-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f859-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="5f859-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f859-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="5f859-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f859-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="5f859-142">Schema Name</span></span>  <br/> |<span data-ttu-id="5f859-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="5f859-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f859-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="5f859-144">Validation File</span></span>  <br/> |<span data-ttu-id="5f859-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f859-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f859-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="5f859-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="5f859-147">False</span><span class="sxs-lookup"><span data-stu-id="5f859-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f859-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f859-148">See also</span></span>

- [<span data-ttu-id="5f859-149">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="5f859-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="5f859-150">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5f859-150">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="5f859-151">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="5f859-151">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

