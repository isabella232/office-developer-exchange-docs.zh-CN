---
title: StartTimeInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTimeInMinutes
api_type:
- schema
ms.assetid: 0fb60a78-6e79-4601-8e2f-5bd245c46d69
description: StartTimeInMinutes 元素均表示邮箱用户的工作日的开始。
ms.openlocfilehash: f3f1d26731d0406ff8a0fd45fc0243a9feabf886
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827558"
---
# <a name="starttimeinminutes"></a><span data-ttu-id="88fa9-103">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="88fa9-103">StartTimeInMinutes</span></span>

<span data-ttu-id="88fa9-104">**StartTimeInMinutes**元素均表示邮箱用户的工作日的开始。</span><span class="sxs-lookup"><span data-stu-id="88fa9-104">The **StartTimeInMinutes** element represents the start of the working day for a mailbox user.</span></span> 
  
- [<span data-ttu-id="88fa9-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="88fa9-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="88fa9-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="88fa9-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
- [<span data-ttu-id="88fa9-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="88fa9-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
- [<span data-ttu-id="88fa9-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="88fa9-108">FreeBusyView</span></span>](freebusyview.md)
  
- [<span data-ttu-id="88fa9-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="88fa9-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
- [<span data-ttu-id="88fa9-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="88fa9-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
- [<span data-ttu-id="88fa9-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="88fa9-111">WorkingPeriod</span></span>](workingperiod.md)
  
- [<span data-ttu-id="88fa9-112">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="88fa9-112">StartTimeInMinutes</span></span>](starttimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

<span data-ttu-id="88fa9-113">**int**</span><span class="sxs-lookup"><span data-stu-id="88fa9-113">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="88fa9-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="88fa9-114">Attributes and elements</span></span>

<span data-ttu-id="88fa9-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="88fa9-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="88fa9-116">属性</span><span class="sxs-lookup"><span data-stu-id="88fa9-116">Attributes</span></span>

<span data-ttu-id="88fa9-117">无。</span><span class="sxs-lookup"><span data-stu-id="88fa9-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="88fa9-118">子元素</span><span class="sxs-lookup"><span data-stu-id="88fa9-118">Child elements</span></span>

<span data-ttu-id="88fa9-119">无。</span><span class="sxs-lookup"><span data-stu-id="88fa9-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="88fa9-120">父元素</span><span class="sxs-lookup"><span data-stu-id="88fa9-120">Parent elements</span></span>

|<span data-ttu-id="88fa9-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="88fa9-121">**Element**</span></span>|<span data-ttu-id="88fa9-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="88fa9-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="88fa9-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="88fa9-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="88fa9-124">包含工作周的那几天和邮箱用户的时间。</span><span class="sxs-lookup"><span data-stu-id="88fa9-124">Contains the work week days and hours of the mailbox user.</span></span>  <br/> <span data-ttu-id="88fa9-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="88fa9-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="88fa9-126">文本值</span><span class="sxs-lookup"><span data-stu-id="88fa9-126">Text value</span></span>

<span data-ttu-id="88fa9-127">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="88fa9-127">A text value is required.</span></span> <span data-ttu-id="88fa9-128">文本值的某一天开始以来经过多少分钟表示工作日的开始。</span><span class="sxs-lookup"><span data-stu-id="88fa9-128">The text value represents the start of the working day by how many minutes have elapsed since the day began.</span></span> <span data-ttu-id="88fa9-129">例如，上午 8 点开始时间</span><span class="sxs-lookup"><span data-stu-id="88fa9-129">For example, a start time of 8 A.M.</span></span> <span data-ttu-id="88fa9-130">表示由 480 分钟。</span><span class="sxs-lookup"><span data-stu-id="88fa9-130">is represented by 480 minutes.</span></span>
  
<span data-ttu-id="88fa9-131">此元素的可能值的范围是 0 到 1440年。</span><span class="sxs-lookup"><span data-stu-id="88fa9-131">The range of possible values for this element is 0 to 1440.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88fa9-132">备注</span><span class="sxs-lookup"><span data-stu-id="88fa9-132">Remarks</span></span>

<span data-ttu-id="88fa9-133">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="88fa9-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="88fa9-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="88fa9-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88fa9-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="88fa9-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="88fa9-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="88fa9-136">Schema Name</span></span>  <br/> |<span data-ttu-id="88fa9-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="88fa9-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="88fa9-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="88fa9-138">Validation File</span></span>  <br/> |<span data-ttu-id="88fa9-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="88fa9-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="88fa9-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="88fa9-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="88fa9-141">False</span><span class="sxs-lookup"><span data-stu-id="88fa9-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88fa9-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="88fa9-142">See also</span></span>

- [<span data-ttu-id="88fa9-143">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="88fa9-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="88fa9-144">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="88fa9-144">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="88fa9-145">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="88fa9-145">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

