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
description: EndTimeInMinutes 元素均表示邮箱用户的工作日的末尾。
ms.openlocfilehash: 2885d810512eb0e575aa25b4f38d28332a10b8f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754140"
---
# <a name="endtimeinminutes"></a><span data-ttu-id="ec43f-103">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="ec43f-103">EndTimeInMinutes</span></span>

<span data-ttu-id="ec43f-104">**EndTimeInMinutes**元素均表示邮箱用户的工作日的末尾。</span><span class="sxs-lookup"><span data-stu-id="ec43f-104">The **EndTimeInMinutes** element represents the end of the working day for a mailbox user.</span></span> 
  
[<span data-ttu-id="ec43f-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ec43f-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ec43f-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="ec43f-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="ec43f-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="ec43f-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="ec43f-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="ec43f-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="ec43f-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="ec43f-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="ec43f-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="ec43f-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="ec43f-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="ec43f-111">WorkingPeriod</span></span>](workingperiod.md)
  
[<span data-ttu-id="ec43f-112">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="ec43f-112">EndTimeInMinutes</span></span>](endtimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

 <span data-ttu-id="ec43f-113">**int**</span><span class="sxs-lookup"><span data-stu-id="ec43f-113">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec43f-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ec43f-114">Attributes and elements</span></span>

<span data-ttu-id="ec43f-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ec43f-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec43f-116">属性</span><span class="sxs-lookup"><span data-stu-id="ec43f-116">Attributes</span></span>

<span data-ttu-id="ec43f-117">无。</span><span class="sxs-lookup"><span data-stu-id="ec43f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec43f-118">子元素</span><span class="sxs-lookup"><span data-stu-id="ec43f-118">Child elements</span></span>

<span data-ttu-id="ec43f-119">无。</span><span class="sxs-lookup"><span data-stu-id="ec43f-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ec43f-120">父元素</span><span class="sxs-lookup"><span data-stu-id="ec43f-120">Parent elements</span></span>

|<span data-ttu-id="ec43f-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="ec43f-121">**Element**</span></span>|<span data-ttu-id="ec43f-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec43f-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec43f-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="ec43f-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="ec43f-124">包含工作周的那几天和邮箱用户的时间。</span><span class="sxs-lookup"><span data-stu-id="ec43f-124">Contains the work week days and hours of the mailbox user.</span></span>  <br/> <span data-ttu-id="ec43f-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ec43f-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec43f-126">文本值</span><span class="sxs-lookup"><span data-stu-id="ec43f-126">Text value</span></span>

<span data-ttu-id="ec43f-127">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="ec43f-127">A text value is required.</span></span> <span data-ttu-id="ec43f-128">文本值的某一天开始以来经过多少分钟代表工作日的末尾。</span><span class="sxs-lookup"><span data-stu-id="ec43f-128">The text value represents the end of the working day by how many minutes have elapsed since the day began.</span></span> <span data-ttu-id="ec43f-129">例如，下午 6 结束时间</span><span class="sxs-lookup"><span data-stu-id="ec43f-129">For example, an end time of 6 P.M.</span></span> <span data-ttu-id="ec43f-130">表示由 1080 分钟。</span><span class="sxs-lookup"><span data-stu-id="ec43f-130">is represented by 1080 minutes.</span></span>
  
<span data-ttu-id="ec43f-131">此元素的可能值的范围是 0 到 1440年。</span><span class="sxs-lookup"><span data-stu-id="ec43f-131">The range of possible values for this element is 0 to 1440.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ec43f-132">备注</span><span class="sxs-lookup"><span data-stu-id="ec43f-132">Remarks</span></span>

<span data-ttu-id="ec43f-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ec43f-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec43f-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="ec43f-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec43f-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="ec43f-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ec43f-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="ec43f-136">Schema Name</span></span>  <br/> |<span data-ttu-id="ec43f-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="ec43f-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="ec43f-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="ec43f-138">Validation File</span></span>  <br/> |<span data-ttu-id="ec43f-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ec43f-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ec43f-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="ec43f-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec43f-141">False</span><span class="sxs-lookup"><span data-stu-id="ec43f-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec43f-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ec43f-142">See also</span></span>



[<span data-ttu-id="ec43f-143">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ec43f-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ec43f-144">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ec43f-144">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ec43f-145">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="ec43f-145">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

