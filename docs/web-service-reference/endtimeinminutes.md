---
title: EndTimeInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTimeInMinutes
api_type:
- schema
ms.assetid: ef05bdda-7a66-44db-bb73-a2ce8316c257
description: EndTimeInMinutes 元素表示邮箱用户的工作日的结束日期。
ms.openlocfilehash: cb564f9de944848734749a30c813a94d6b5c4187
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459649"
---
# <a name="endtimeinminutes"></a><span data-ttu-id="ccac1-103">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="ccac1-103">EndTimeInMinutes</span></span>

<span data-ttu-id="ccac1-104">**EndTimeInMinutes**元素表示邮箱用户的工作日的结束日期。</span><span class="sxs-lookup"><span data-stu-id="ccac1-104">The **EndTimeInMinutes** element represents the end of the working day for a mailbox user.</span></span> 
  
[<span data-ttu-id="ccac1-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ccac1-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ccac1-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="ccac1-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="ccac1-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ccac1-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="ccac1-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ccac1-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="ccac1-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="ccac1-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="ccac1-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="ccac1-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="ccac1-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="ccac1-111">WorkingPeriod</span></span>](workingperiod.md)
  
[<span data-ttu-id="ccac1-112">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="ccac1-112">EndTimeInMinutes</span></span>](endtimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

 <span data-ttu-id="ccac1-113">**int**</span><span class="sxs-lookup"><span data-stu-id="ccac1-113">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccac1-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ccac1-114">Attributes and elements</span></span>

<span data-ttu-id="ccac1-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ccac1-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccac1-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="ccac1-116">Attributes</span></span>

<span data-ttu-id="ccac1-117">无。</span><span class="sxs-lookup"><span data-stu-id="ccac1-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccac1-118">子元素</span><span class="sxs-lookup"><span data-stu-id="ccac1-118">Child elements</span></span>

<span data-ttu-id="ccac1-119">无。</span><span class="sxs-lookup"><span data-stu-id="ccac1-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ccac1-120">父元素</span><span class="sxs-lookup"><span data-stu-id="ccac1-120">Parent elements</span></span>

|<span data-ttu-id="ccac1-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="ccac1-121">**Element**</span></span>|<span data-ttu-id="ccac1-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="ccac1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccac1-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="ccac1-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="ccac1-124">包含邮箱用户的工作周天数和小时数。</span><span class="sxs-lookup"><span data-stu-id="ccac1-124">Contains the work week days and hours of the mailbox user.</span></span>  <br/> <span data-ttu-id="ccac1-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="ccac1-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ccac1-126">文本值</span><span class="sxs-lookup"><span data-stu-id="ccac1-126">Text value</span></span>

<span data-ttu-id="ccac1-127">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="ccac1-127">A text value is required.</span></span> <span data-ttu-id="ccac1-128">该文本值表示自一天开始以来经过的分钟数的结束日期。</span><span class="sxs-lookup"><span data-stu-id="ccac1-128">The text value represents the end of the working day by how many minutes have elapsed since the day began.</span></span> <span data-ttu-id="ccac1-129">例如，结束时间为下午6点。</span><span class="sxs-lookup"><span data-stu-id="ccac1-129">For example, an end time of 6 P.M.</span></span> <span data-ttu-id="ccac1-130">由1080分钟表示。</span><span class="sxs-lookup"><span data-stu-id="ccac1-130">is represented by 1080 minutes.</span></span>
  
<span data-ttu-id="ccac1-131">此元素的可能值的范围是0到1440。</span><span class="sxs-lookup"><span data-stu-id="ccac1-131">The range of possible values for this element is 0 to 1440.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ccac1-132">说明</span><span class="sxs-lookup"><span data-stu-id="ccac1-132">Remarks</span></span>

<span data-ttu-id="ccac1-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ccac1-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccac1-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="ccac1-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccac1-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="ccac1-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ccac1-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="ccac1-136">Schema Name</span></span>  <br/> |<span data-ttu-id="ccac1-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="ccac1-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="ccac1-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="ccac1-138">Validation File</span></span>  <br/> |<span data-ttu-id="ccac1-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ccac1-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ccac1-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="ccac1-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccac1-141">False</span><span class="sxs-lookup"><span data-stu-id="ccac1-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccac1-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ccac1-142">See also</span></span>



[<span data-ttu-id="ccac1-143">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ccac1-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ccac1-144">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ccac1-144">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ccac1-145">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="ccac1-145">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

