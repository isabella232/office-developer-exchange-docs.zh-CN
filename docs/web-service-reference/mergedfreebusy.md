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
ms.openlocfilehash: a1483449534f0d886e3c97a23d28c5d78f865042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468724"
---
# <a name="mergedfreebusy"></a><span data-ttu-id="9bcc5-103">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="9bcc5-103">MergedFreeBusy</span></span>

<span data-ttu-id="9bcc5-104">**MergedFreeBusy**元素包含合并的忙/闲数据流。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-104">The **MergedFreeBusy** element contains the merged free/busy stream of data.</span></span> 
  
[<span data-ttu-id="9bcc5-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9bcc5-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="9bcc5-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="9bcc5-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="9bcc5-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="9bcc5-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="9bcc5-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="9bcc5-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="9bcc5-109">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="9bcc5-109">MergedFreeBusy</span></span>](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 <span data-ttu-id="9bcc5-110">**string**</span><span class="sxs-lookup"><span data-stu-id="9bcc5-110">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bcc5-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9bcc5-111">Attributes and elements</span></span>

<span data-ttu-id="9bcc5-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bcc5-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="9bcc5-113">Attributes</span></span>

<span data-ttu-id="9bcc5-114">无。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9bcc5-115">子元素</span><span class="sxs-lookup"><span data-stu-id="9bcc5-115">Child elements</span></span>

<span data-ttu-id="9bcc5-116">无。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9bcc5-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9bcc5-117">Parent elements</span></span>

|<span data-ttu-id="9bcc5-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="9bcc5-118">**Element**</span></span>|<span data-ttu-id="9bcc5-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="9bcc5-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bcc5-120">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="9bcc5-120">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="9bcc5-121">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-121">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="9bcc5-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="9bcc5-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9bcc5-123">文本值</span><span class="sxs-lookup"><span data-stu-id="9bcc5-123">Text value</span></span>

<span data-ttu-id="9bcc5-124">如果[FreeBusyViewType](freebusyviewtype.md)元素的值是下列值之一，则由服务器提供一个文本值：</span><span class="sxs-lookup"><span data-stu-id="9bcc5-124">A text value is provided by the server if the value for the [FreeBusyViewType](freebusyviewtype.md) element is one of the following:</span></span> 
  
- <span data-ttu-id="9bcc5-125">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="9bcc5-125">DetailedMerged</span></span>
    
- <span data-ttu-id="9bcc5-126">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="9bcc5-126">FreeBusyMerged</span></span>
    
- <span data-ttu-id="9bcc5-127">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="9bcc5-127">MergedOnly</span></span>
    
<span data-ttu-id="9bcc5-128">该文本值是一种忙/闲信息流。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-128">The text value is a stream of free/busy information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9bcc5-129">备注</span><span class="sxs-lookup"><span data-stu-id="9bcc5-129">Remarks</span></span>

<span data-ttu-id="9bcc5-130">此元素提供的数据流由[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)和[TimeWindow](timewindow.md)元素定义。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-130">The stream of data provided by this element is defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) and [TimeWindow](timewindow.md) elements.</span></span> <span data-ttu-id="9bcc5-131">[TimeWindow](timewindow.md)元素定义查询可用性的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-131">The [TimeWindow](timewindow.md) element defines the time span queried for availability.</span></span> <span data-ttu-id="9bcc5-132">[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义如何将[TimeWindow](timewindow.md)元素中的时间分成**MergedFreeBusy**元素中返回的间隔。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-132">The [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element defines how the time from the [TimeWindow](timewindow.md) element is broken into intervals returned in the **MergedFreeBusy** element.</span></span> <span data-ttu-id="9bcc5-133">**MergedFreeBusy**流中的每个数字表示一个由[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素定义的间隔。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-133">Each number in the **MergedFreeBusy** stream represents a single interval defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element.</span></span> <span data-ttu-id="9bcc5-134">下表列出了单个间隔的可能值。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-134">The following table lists the possible values for an individual interval.</span></span> 
  
|<span data-ttu-id="9bcc5-135">**数字**</span><span class="sxs-lookup"><span data-stu-id="9bcc5-135">**Digit**</span></span>|<span data-ttu-id="9bcc5-136">**可用性**</span><span class="sxs-lookup"><span data-stu-id="9bcc5-136">**Availability**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9bcc5-137">0</span><span class="sxs-lookup"><span data-stu-id="9bcc5-137">0</span></span>  <br/> |<span data-ttu-id="9bcc5-138">空闲</span><span class="sxs-lookup"><span data-stu-id="9bcc5-138">Free</span></span>  <br/> |
|<span data-ttu-id="9bcc5-139">1 </span><span class="sxs-lookup"><span data-stu-id="9bcc5-139">1</span></span>  <br/> |<span data-ttu-id="9bcc5-140">暂</span><span class="sxs-lookup"><span data-stu-id="9bcc5-140">Tentative</span></span>  <br/> |
|<span data-ttu-id="9bcc5-141">双面</span><span class="sxs-lookup"><span data-stu-id="9bcc5-141">2</span></span>  <br/> |<span data-ttu-id="9bcc5-142">忙碌</span><span class="sxs-lookup"><span data-stu-id="9bcc5-142">Busy</span></span>  <br/> |
|<span data-ttu-id="9bcc5-143">第三章</span><span class="sxs-lookup"><span data-stu-id="9bcc5-143">3</span></span>  <br/> |<span data-ttu-id="9bcc5-144">外出 (OOF)</span><span class="sxs-lookup"><span data-stu-id="9bcc5-144">Out of Office (OOF)</span></span>  <br/> |
|<span data-ttu-id="9bcc5-145">4 </span><span class="sxs-lookup"><span data-stu-id="9bcc5-145">4</span></span>  <br/> |<span data-ttu-id="9bcc5-146">无数据</span><span class="sxs-lookup"><span data-stu-id="9bcc5-146">No data</span></span>  <br/> |
   
<span data-ttu-id="9bcc5-147">例如，忙/闲数据的请求包含一个[TimeWindow](timewindow.md)元素，该元素表示四个小时，一个[MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md)元素表示60分钟。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-147">For example, a request for free/busy data includes a [TimeWindow](timewindow.md) element that represents four hours and a [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element that represents 60 minutes.</span></span> <span data-ttu-id="9bcc5-148">如果请求的用户的日历为前60分钟的 OOF，在时间窗口中等待以下90分钟，并对最后的90分钟进行了非计划，则**MergedFreeBusy**流将为3220。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-148">If the requested user's calendar is OOF for the first 60 minutes, busy for the following 90 minutes, and unscheduled for the final 90 minutes in the time window, the **MergedFreeBusy** stream will be 3220.</span></span> <span data-ttu-id="9bcc5-149">如果某个间隔包含多个可用性分类，则将使用最大数量对该间隔进行分类。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-149">If an interval contains more than one availability classification, the highest number is used to classify that interval.</span></span> 
  
<span data-ttu-id="9bcc5-150">此元素提供的详细信息级别取决于授予请求者的权限。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-150">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="9bcc5-151">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9bcc5-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9bcc5-152">元素信息</span><span class="sxs-lookup"><span data-stu-id="9bcc5-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bcc5-153">命名空间</span><span class="sxs-lookup"><span data-stu-id="9bcc5-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9bcc5-154">架构名称</span><span class="sxs-lookup"><span data-stu-id="9bcc5-154">Schema Name</span></span>  <br/> |<span data-ttu-id="9bcc5-155">类型架构</span><span class="sxs-lookup"><span data-stu-id="9bcc5-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="9bcc5-156">验证文件</span><span class="sxs-lookup"><span data-stu-id="9bcc5-156">Validation File</span></span>  <br/> |<span data-ttu-id="9bcc5-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9bcc5-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9bcc5-158">可以为空</span><span class="sxs-lookup"><span data-stu-id="9bcc5-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="9bcc5-159">False</span><span class="sxs-lookup"><span data-stu-id="9bcc5-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bcc5-160">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9bcc5-160">See also</span></span>



[<span data-ttu-id="9bcc5-161">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="9bcc5-161">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="9bcc5-162">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="9bcc5-162">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="9bcc5-163">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="9bcc5-163">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

