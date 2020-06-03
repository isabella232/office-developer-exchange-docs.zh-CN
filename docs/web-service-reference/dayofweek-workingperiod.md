---
title: DayOfWeek （WorkingPeriod）
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
description: DayOfWeek 元素包含为邮箱用户计划的工作日的列表。
ms.openlocfilehash: 06d4a7d5541b3b71fcbf9be9beb7512d06853283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457443"
---
# <a name="dayofweek-workingperiod"></a><span data-ttu-id="05c7c-103">DayOfWeek （WorkingPeriod）</span><span class="sxs-lookup"><span data-stu-id="05c7c-103">DayOfWeek (WorkingPeriod)</span></span>

<span data-ttu-id="05c7c-104">**DayOfWeek**元素包含为邮箱用户计划的工作日的列表。</span><span class="sxs-lookup"><span data-stu-id="05c7c-104">The **DayOfWeek** element contains the list of working days scheduled for the mailbox user.</span></span> 
  
- [<span data-ttu-id="05c7c-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="05c7c-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="05c7c-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="05c7c-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)  
- [<span data-ttu-id="05c7c-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="05c7c-107">FreeBusyResponse</span></span>](freebusyresponse.md)  
- [<span data-ttu-id="05c7c-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="05c7c-108">FreeBusyView</span></span>](freebusyview.md)  
- [<span data-ttu-id="05c7c-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="05c7c-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)  
- [<span data-ttu-id="05c7c-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="05c7c-110">WorkingPeriodArray</span></span>](workingperiodarray.md) 
- [<span data-ttu-id="05c7c-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="05c7c-111">WorkingPeriod</span></span>](workingperiod.md)  
- [<span data-ttu-id="05c7c-112">DayOfWeek （WorkingPeriod）</span><span class="sxs-lookup"><span data-stu-id="05c7c-112">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
  
```xml
<DayOfWeek>Sunday Monday Tuesday Wednesday Thursday Friday Saturday</DayOfWeek>
```

<span data-ttu-id="05c7c-113">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="05c7c-113">**DaysOfWeek**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="05c7c-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="05c7c-114">Attributes and elements</span></span>

<span data-ttu-id="05c7c-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="05c7c-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05c7c-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="05c7c-116">Attributes</span></span>

<span data-ttu-id="05c7c-117">无。</span><span class="sxs-lookup"><span data-stu-id="05c7c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05c7c-118">子元素</span><span class="sxs-lookup"><span data-stu-id="05c7c-118">Child elements</span></span>

<span data-ttu-id="05c7c-119">无。</span><span class="sxs-lookup"><span data-stu-id="05c7c-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="05c7c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="05c7c-120">Parent elements</span></span>

|<span data-ttu-id="05c7c-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="05c7c-121">**Element**</span></span>|<span data-ttu-id="05c7c-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="05c7c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05c7c-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="05c7c-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="05c7c-124">包含邮箱用户的工作周天数和小时数。</span><span class="sxs-lookup"><span data-stu-id="05c7c-124">Contains the work week days and hours of the mailbox user.</span></span><br/><br/><span data-ttu-id="05c7c-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="05c7c-125">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i[` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="05c7c-126">文本值</span><span class="sxs-lookup"><span data-stu-id="05c7c-126">Text value</span></span>

<span data-ttu-id="05c7c-127">如果邮箱用户的天数设置为表示工作周，则返回一个文本值。</span><span class="sxs-lookup"><span data-stu-id="05c7c-127">A text value is returned if the mailbox user has days set to represent the work week.</span></span> <span data-ttu-id="05c7c-128">以下是此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="05c7c-128">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="05c7c-129">星期日</span><span class="sxs-lookup"><span data-stu-id="05c7c-129">Sunday</span></span>    
- <span data-ttu-id="05c7c-130">星期一</span><span class="sxs-lookup"><span data-stu-id="05c7c-130">Monday</span></span>    
- <span data-ttu-id="05c7c-131">星期二</span><span class="sxs-lookup"><span data-stu-id="05c7c-131">Tuesday</span></span>    
- <span data-ttu-id="05c7c-132">星期三</span><span class="sxs-lookup"><span data-stu-id="05c7c-132">Wednesday</span></span>    
- <span data-ttu-id="05c7c-133">星期四</span><span class="sxs-lookup"><span data-stu-id="05c7c-133">Thursday</span></span>    
- <span data-ttu-id="05c7c-134">星期五</span><span class="sxs-lookup"><span data-stu-id="05c7c-134">Friday</span></span>    
- <span data-ttu-id="05c7c-135">星期六</span><span class="sxs-lookup"><span data-stu-id="05c7c-135">Saturday</span></span> 
    
<span data-ttu-id="05c7c-136">文本值将按该顺序返回。</span><span class="sxs-lookup"><span data-stu-id="05c7c-136">The text values will be returned in that order.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05c7c-137">备注</span><span class="sxs-lookup"><span data-stu-id="05c7c-137">Remarks</span></span>

<span data-ttu-id="05c7c-138">请务必注意，此元素与可用性[DayOfWeek （时区）](dayofweek-timezone.md)元素之间的差异在于类型。</span><span class="sxs-lookup"><span data-stu-id="05c7c-138">It is important to note that the difference between this element and the Availability [DayOfWeek (TimeZone)](dayofweek-timezone.md) element is the type.</span></span> 
  
<span data-ttu-id="05c7c-139">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="05c7c-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05c7c-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="05c7c-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05c7c-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="05c7c-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05c7c-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="05c7c-142">Schema Name</span></span>  <br/> |<span data-ttu-id="05c7c-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="05c7c-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="05c7c-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="05c7c-144">Validation File</span></span>  <br/> |<span data-ttu-id="05c7c-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05c7c-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05c7c-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="05c7c-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="05c7c-147">False</span><span class="sxs-lookup"><span data-stu-id="05c7c-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05c7c-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="05c7c-148">See also</span></span>

- [<span data-ttu-id="05c7c-149">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="05c7c-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="05c7c-150">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="05c7c-150">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="05c7c-151">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="05c7c-151">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

