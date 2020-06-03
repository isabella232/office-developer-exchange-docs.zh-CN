---
title: WorkingPeriod
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingPeriod
api_type:
- schema
ms.assetid: 3b4e48af-9880-42b9-a0dc-dae7ac43c264
description: WorkingPeriod 元素包含邮箱用户的工作周天数和小时数。
ms.openlocfilehash: 5c217169fb193d4bb6dae4e18570873d55de6127
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459677"
---
# <a name="workingperiod"></a><span data-ttu-id="31be3-103">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="31be3-103">WorkingPeriod</span></span>

<span data-ttu-id="31be3-104">**WorkingPeriod**元素包含邮箱用户的工作周天数和小时数。</span><span class="sxs-lookup"><span data-stu-id="31be3-104">The **WorkingPeriod** element contains the work week days and hours of the mailbox user.</span></span> 
  
[<span data-ttu-id="31be3-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="31be3-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="31be3-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="31be3-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="31be3-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="31be3-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="31be3-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="31be3-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="31be3-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="31be3-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="31be3-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="31be3-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="31be3-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="31be3-111">WorkingPeriod</span></span>](workingperiod.md)
  
```xml
<WorkingPeriod>
   <DayOfWeek>...</DayOfWeek>
   <StartTimeInMinutes>...</StartTimeInMinutes>
   <EndTimeInMinutes>...</EndTimeInMinutes>
</WorkingPeriod>
```

 <span data-ttu-id="31be3-112">**WorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="31be3-112">**WorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31be3-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="31be3-113">Attributes and elements</span></span>

<span data-ttu-id="31be3-114">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="31be3-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31be3-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="31be3-115">Attributes</span></span>

<span data-ttu-id="31be3-116">无。</span><span class="sxs-lookup"><span data-stu-id="31be3-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31be3-117">子元素</span><span class="sxs-lookup"><span data-stu-id="31be3-117">Child elements</span></span>

|<span data-ttu-id="31be3-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="31be3-118">**Element**</span></span>|<span data-ttu-id="31be3-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="31be3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31be3-120">DayOfWeek （WorkingPeriod）</span><span class="sxs-lookup"><span data-stu-id="31be3-120">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md) <br/> |<span data-ttu-id="31be3-121">包含为邮箱用户计划的工作日列表。</span><span class="sxs-lookup"><span data-stu-id="31be3-121">Contains the list of working days scheduled for the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="31be3-122">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="31be3-122">StartTimeInMinutes</span></span>](starttimeinminutes.md) <br/> |<span data-ttu-id="31be3-123">表示邮箱用户的工作日的开始日期。</span><span class="sxs-lookup"><span data-stu-id="31be3-123">Represents the start of the working day for a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="31be3-124">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="31be3-124">EndTimeInMinutes</span></span>](endtimeinminutes.md) <br/> |<span data-ttu-id="31be3-125">表示邮箱用户的工作日的结束日期。</span><span class="sxs-lookup"><span data-stu-id="31be3-125">Represents the end of the working day for a mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31be3-126">父元素</span><span class="sxs-lookup"><span data-stu-id="31be3-126">Parent elements</span></span>

|<span data-ttu-id="31be3-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="31be3-127">**Element**</span></span>|<span data-ttu-id="31be3-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="31be3-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31be3-129">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="31be3-129">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="31be3-130">包含邮箱用户的工作时间段信息。</span><span class="sxs-lookup"><span data-stu-id="31be3-130">Contains working period information for the mailbox user.</span></span>  <br/> <span data-ttu-id="31be3-131">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="31be3-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31be3-132">备注</span><span class="sxs-lookup"><span data-stu-id="31be3-132">Remarks</span></span>

<span data-ttu-id="31be3-133">所有子元素都按它们出现的顺序列出。</span><span class="sxs-lookup"><span data-stu-id="31be3-133">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="31be3-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="31be3-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31be3-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="31be3-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31be3-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="31be3-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31be3-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="31be3-137">Schema Name</span></span>  <br/> |<span data-ttu-id="31be3-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="31be3-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="31be3-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="31be3-139">Validation File</span></span>  <br/> |<span data-ttu-id="31be3-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="31be3-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31be3-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="31be3-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="31be3-142">False</span><span class="sxs-lookup"><span data-stu-id="31be3-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31be3-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="31be3-143">See also</span></span>



[<span data-ttu-id="31be3-144">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="31be3-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="31be3-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="31be3-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="31be3-146">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="31be3-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

