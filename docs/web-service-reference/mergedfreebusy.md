---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: MergedFreeBusy 元素包含合并的忙/闲数据流。
ms.openlocfilehash: 542b9fae0c36b0236bd806e8a9117753968e812c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826449"
---
# <a name="mergedfreebusy"></a><span data-ttu-id="22b94-103">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="22b94-103">MergedFreeBusy</span></span>

<span data-ttu-id="22b94-104">**MergedFreeBusy**元素包含合并的忙/闲数据流。</span><span class="sxs-lookup"><span data-stu-id="22b94-104">The **MergedFreeBusy** element contains the merged free/busy stream of data.</span></span> 
  
[<span data-ttu-id="22b94-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="22b94-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="22b94-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="22b94-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="22b94-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="22b94-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="22b94-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="22b94-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="22b94-109">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="22b94-109">MergedFreeBusy</span></span>](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 <span data-ttu-id="22b94-110">**string**</span><span class="sxs-lookup"><span data-stu-id="22b94-110">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22b94-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22b94-111">Attributes and elements</span></span>

<span data-ttu-id="22b94-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22b94-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22b94-113">属性</span><span class="sxs-lookup"><span data-stu-id="22b94-113">Attributes</span></span>

<span data-ttu-id="22b94-114">无。</span><span class="sxs-lookup"><span data-stu-id="22b94-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22b94-115">子元素</span><span class="sxs-lookup"><span data-stu-id="22b94-115">Child elements</span></span>

<span data-ttu-id="22b94-116">无。</span><span class="sxs-lookup"><span data-stu-id="22b94-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22b94-117">父元素</span><span class="sxs-lookup"><span data-stu-id="22b94-117">Parent elements</span></span>

|<span data-ttu-id="22b94-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="22b94-118">**Element**</span></span>|<span data-ttu-id="22b94-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="22b94-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22b94-120">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="22b94-120">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="22b94-121">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="22b94-121">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="22b94-122">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="22b94-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="22b94-123">文本值</span><span class="sxs-lookup"><span data-stu-id="22b94-123">Text value</span></span>

<span data-ttu-id="22b94-124">如果[FreeBusyViewType](freebusyviewtype.md)元素的值可以是下列选项之一，由服务器提供的文本值：</span><span class="sxs-lookup"><span data-stu-id="22b94-124">A text value is provided by the server if the value for the [FreeBusyViewType](freebusyviewtype.md) element is one of the following:</span></span> 
  
- <span data-ttu-id="22b94-125">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="22b94-125">DetailedMerged</span></span>
    
- <span data-ttu-id="22b94-126">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="22b94-126">FreeBusyMerged</span></span>
    
- <span data-ttu-id="22b94-127">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="22b94-127">MergedOnly</span></span>
    
<span data-ttu-id="22b94-128">忙/闲信息的数据流的文本值。</span><span class="sxs-lookup"><span data-stu-id="22b94-128">The text value is a stream of free/busy information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="22b94-129">注解</span><span class="sxs-lookup"><span data-stu-id="22b94-129">Remarks</span></span>

<span data-ttu-id="22b94-130">由的[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)和[TimeWindow](timewindow.md)元素定义此元素提供的数据流。</span><span class="sxs-lookup"><span data-stu-id="22b94-130">The stream of data provided by this element is defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) and [TimeWindow](timewindow.md) elements.</span></span> <span data-ttu-id="22b94-131">[TimeWindow](timewindow.md)元素定义查询可用性的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="22b94-131">The [TimeWindow](timewindow.md) element defines the time span queried for availability.</span></span> <span data-ttu-id="22b94-132">[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义如何从[TimeWindow](timewindow.md)元素所需时间分为**MergedFreeBusy**元素中返回的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="22b94-132">The [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element defines how the time from the [TimeWindow](timewindow.md) element is broken into intervals returned in the **MergedFreeBusy** element.</span></span> <span data-ttu-id="22b94-133">**MergedFreeBusy**流中的每个数字代表[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义一个单个时间间隔。</span><span class="sxs-lookup"><span data-stu-id="22b94-133">Each number in the **MergedFreeBusy** stream represents a single interval defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element.</span></span> <span data-ttu-id="22b94-134">下表列出各个间隔的可能值。</span><span class="sxs-lookup"><span data-stu-id="22b94-134">The following table lists the possible values for an individual interval.</span></span> 
  
|<span data-ttu-id="22b94-135">**数字**</span><span class="sxs-lookup"><span data-stu-id="22b94-135">**Digit**</span></span>|<span data-ttu-id="22b94-136">**可用性**</span><span class="sxs-lookup"><span data-stu-id="22b94-136">**Availability**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22b94-137">0</span><span class="sxs-lookup"><span data-stu-id="22b94-137">0</span></span>  <br/> |<span data-ttu-id="22b94-138">免费</span><span class="sxs-lookup"><span data-stu-id="22b94-138">Free</span></span>  <br/> |
|<span data-ttu-id="22b94-139">1</span><span class="sxs-lookup"><span data-stu-id="22b94-139">1</span></span>  <br/> |<span data-ttu-id="22b94-140">暂定</span><span class="sxs-lookup"><span data-stu-id="22b94-140">Tentative</span></span>  <br/> |
|<span data-ttu-id="22b94-141">2</span><span class="sxs-lookup"><span data-stu-id="22b94-141">2</span></span>  <br/> |<span data-ttu-id="22b94-142">忙碌</span><span class="sxs-lookup"><span data-stu-id="22b94-142">Busy</span></span>  <br/> |
|<span data-ttu-id="22b94-143">3</span><span class="sxs-lookup"><span data-stu-id="22b94-143">3</span></span>  <br/> |<span data-ttu-id="22b94-144">不在办公室 (OOF)</span><span class="sxs-lookup"><span data-stu-id="22b94-144">Out of Office (OOF)</span></span>  <br/> |
|<span data-ttu-id="22b94-145">4</span><span class="sxs-lookup"><span data-stu-id="22b94-145">4</span></span>  <br/> |<span data-ttu-id="22b94-146">没有数据</span><span class="sxs-lookup"><span data-stu-id="22b94-146">No data</span></span>  <br/> |
   
<span data-ttu-id="22b94-147">例如，忙/闲数据的请求包含代表四小时[TimeWindow](timewindow.md)元素和[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素值，该值代表 60 分钟。</span><span class="sxs-lookup"><span data-stu-id="22b94-147">For example, a request for free/busy data includes a [TimeWindow](timewindow.md) element that represents four hours and a [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element that represents 60 minutes.</span></span> <span data-ttu-id="22b94-148">如果请求的用户的日历 OOF 前 60 分钟，以下 90 分钟，忙和计划外的最终 90 分钟在时间窗口中， **MergedFreeBusy**流将 3220。</span><span class="sxs-lookup"><span data-stu-id="22b94-148">If the requested user's calendar is OOF for the first 60 minutes, busy for the following 90 minutes, and unscheduled for the final 90 minutes in the time window, the **MergedFreeBusy** stream will be 3220.</span></span> <span data-ttu-id="22b94-149">如果间隔包含多个可用性分类，最大数字用于分类的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="22b94-149">If an interval contains more than one availability classification, the highest number is used to classify that interval.</span></span> 
  
<span data-ttu-id="22b94-150">提供此元素的详细程度取决于所请求者授予的权限。</span><span class="sxs-lookup"><span data-stu-id="22b94-150">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="22b94-151">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22b94-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22b94-152">元素信息</span><span class="sxs-lookup"><span data-stu-id="22b94-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22b94-153">命名空间</span><span class="sxs-lookup"><span data-stu-id="22b94-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22b94-154">架构名称</span><span class="sxs-lookup"><span data-stu-id="22b94-154">Schema Name</span></span>  <br/> |<span data-ttu-id="22b94-155">类型架构</span><span class="sxs-lookup"><span data-stu-id="22b94-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="22b94-156">验证文件</span><span class="sxs-lookup"><span data-stu-id="22b94-156">Validation File</span></span>  <br/> |<span data-ttu-id="22b94-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="22b94-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22b94-158">可以为空</span><span class="sxs-lookup"><span data-stu-id="22b94-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="22b94-159">False</span><span class="sxs-lookup"><span data-stu-id="22b94-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22b94-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22b94-160">See also</span></span>



[<span data-ttu-id="22b94-161">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="22b94-161">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="22b94-162">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="22b94-162">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="22b94-163">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="22b94-163">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

