---
title: WorkingPeriodArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingPeriodArray
api_type:
- schema
ms.assetid: 3a3f6393-eacc-4734-b6c9-b67023fe2830
description: WorkingPeriodArray 元素包含处理期间邮箱用户的信息。
ms.openlocfilehash: 02712f05dc3373a532d769f476341b78ad25a79c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838579"
---
# <a name="workingperiodarray"></a><span data-ttu-id="a355a-103">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="a355a-103">WorkingPeriodArray</span></span>

<span data-ttu-id="a355a-104">**WorkingPeriodArray**元素包含处理期间邮箱用户的信息。</span><span class="sxs-lookup"><span data-stu-id="a355a-104">The **WorkingPeriodArray** element contains working period information for the mailbox user.</span></span> 
  
[<span data-ttu-id="a355a-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a355a-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="a355a-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="a355a-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="a355a-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="a355a-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="a355a-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="a355a-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="a355a-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="a355a-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="a355a-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="a355a-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
```xml
<WorkingPeriodArray>
   <WorkingPeriod>...</WorkingPeriod>
</WorkingPeriodArray>
```

 <span data-ttu-id="a355a-111">**ArrayOfWorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="a355a-111">**ArrayOfWorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a355a-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a355a-112">Attributes and elements</span></span>

<span data-ttu-id="a355a-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a355a-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a355a-114">属性</span><span class="sxs-lookup"><span data-stu-id="a355a-114">Attributes</span></span>

<span data-ttu-id="a355a-115">无。</span><span class="sxs-lookup"><span data-stu-id="a355a-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a355a-116">子元素</span><span class="sxs-lookup"><span data-stu-id="a355a-116">Child elements</span></span>

|<span data-ttu-id="a355a-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="a355a-117">**Element**</span></span>|<span data-ttu-id="a355a-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="a355a-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a355a-119">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="a355a-119">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="a355a-120">包含工作周的那几天和邮箱用户的时间。</span><span class="sxs-lookup"><span data-stu-id="a355a-120">Contains the work week days and hours of the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a355a-121">父元素</span><span class="sxs-lookup"><span data-stu-id="a355a-121">Parent elements</span></span>

|<span data-ttu-id="a355a-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="a355a-122">**Element**</span></span>|<span data-ttu-id="a355a-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="a355a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a355a-124">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="a355a-124">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a355a-125">表示所在的时区设置和请求的邮箱用户的工作时间。</span><span class="sxs-lookup"><span data-stu-id="a355a-125">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="a355a-126">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a355a-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a355a-127">备注</span><span class="sxs-lookup"><span data-stu-id="a355a-127">Remarks</span></span>

<span data-ttu-id="a355a-128">如果使用[WorkingHours](workinghours-ex15websvcsotherref.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="a355a-128">This element is required if the [WorkingHours](workinghours-ex15websvcsotherref.md) element is used.</span></span> <span data-ttu-id="a355a-129">中发生的顺序排列的所有子元素。</span><span class="sxs-lookup"><span data-stu-id="a355a-129">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="a355a-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a355a-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a355a-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="a355a-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a355a-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="a355a-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a355a-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="a355a-133">Schema Name</span></span>  <br/> |<span data-ttu-id="a355a-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="a355a-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="a355a-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="a355a-135">Validation File</span></span>  <br/> |<span data-ttu-id="a355a-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a355a-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a355a-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="a355a-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="a355a-138">False</span><span class="sxs-lookup"><span data-stu-id="a355a-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a355a-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a355a-139">See also</span></span>



[<span data-ttu-id="a355a-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="a355a-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="a355a-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a355a-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="a355a-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="a355a-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)
