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
description: WorkingPeriodArray 元素包含邮箱用户的工作时间段信息。
ms.openlocfilehash: a9ca55866a574c5208d8561fca6daf417867fef6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465196"
---
# <a name="workingperiodarray"></a><span data-ttu-id="2b237-103">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="2b237-103">WorkingPeriodArray</span></span>

<span data-ttu-id="2b237-104">**WorkingPeriodArray**元素包含邮箱用户的工作时间段信息。</span><span class="sxs-lookup"><span data-stu-id="2b237-104">The **WorkingPeriodArray** element contains working period information for the mailbox user.</span></span> 
  
[<span data-ttu-id="2b237-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2b237-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="2b237-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="2b237-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="2b237-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="2b237-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="2b237-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="2b237-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="2b237-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="2b237-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="2b237-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="2b237-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
```xml
<WorkingPeriodArray>
   <WorkingPeriod>...</WorkingPeriod>
</WorkingPeriodArray>
```

 <span data-ttu-id="2b237-111">**ArrayOfWorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="2b237-111">**ArrayOfWorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b237-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2b237-112">Attributes and elements</span></span>

<span data-ttu-id="2b237-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2b237-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b237-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="2b237-114">Attributes</span></span>

<span data-ttu-id="2b237-115">无。</span><span class="sxs-lookup"><span data-stu-id="2b237-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b237-116">子元素</span><span class="sxs-lookup"><span data-stu-id="2b237-116">Child elements</span></span>

|<span data-ttu-id="2b237-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="2b237-117">**Element**</span></span>|<span data-ttu-id="2b237-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="2b237-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b237-119">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="2b237-119">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="2b237-120">包含邮箱用户的工作周天数和小时数。</span><span class="sxs-lookup"><span data-stu-id="2b237-120">Contains the work week days and hours of the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2b237-121">父元素</span><span class="sxs-lookup"><span data-stu-id="2b237-121">Parent elements</span></span>

|<span data-ttu-id="2b237-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="2b237-122">**Element**</span></span>|<span data-ttu-id="2b237-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="2b237-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2b237-124">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="2b237-124">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="2b237-125">表示所请求的邮箱用户的时区设置和工作时间。</span><span class="sxs-lookup"><span data-stu-id="2b237-125">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="2b237-126">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="2b237-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b237-127">备注</span><span class="sxs-lookup"><span data-stu-id="2b237-127">Remarks</span></span>

<span data-ttu-id="2b237-128">如果使用[WorkingHours](workinghours-ex15websvcsotherref.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="2b237-128">This element is required if the [WorkingHours](workinghours-ex15websvcsotherref.md) element is used.</span></span> <span data-ttu-id="2b237-129">所有子元素都按它们出现的顺序列出。</span><span class="sxs-lookup"><span data-stu-id="2b237-129">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="2b237-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2b237-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b237-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="2b237-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b237-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="2b237-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2b237-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="2b237-133">Schema Name</span></span>  <br/> |<span data-ttu-id="2b237-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="2b237-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="2b237-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="2b237-135">Validation File</span></span>  <br/> |<span data-ttu-id="2b237-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2b237-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2b237-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="2b237-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="2b237-138">False</span><span class="sxs-lookup"><span data-stu-id="2b237-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2b237-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2b237-139">See also</span></span>



[<span data-ttu-id="2b237-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="2b237-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="2b237-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="2b237-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="2b237-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="2b237-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

