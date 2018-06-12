---
title: RequestedView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RequestedView
api_type:
- schema
ms.assetid: e2b4cf8c-5d43-4cd8-b86d-cc27a5d2f095
description: RequestedView 元素定义的客户端请求的日历信息的类型。
ms.openlocfilehash: 7710227720264432c325f95da894cbbbd4748dc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827145"
---
# <a name="requestedview"></a><span data-ttu-id="0735e-103">RequestedView</span><span class="sxs-lookup"><span data-stu-id="0735e-103">RequestedView</span></span>

<span data-ttu-id="0735e-104">**RequestedView**元素定义的客户端请求的日历信息的类型。</span><span class="sxs-lookup"><span data-stu-id="0735e-104">The **RequestedView** element defines the type of calendar information that a client requests.</span></span> 
  
[<span data-ttu-id="0735e-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="0735e-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="0735e-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="0735e-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="0735e-107">RequestedView</span><span class="sxs-lookup"><span data-stu-id="0735e-107">RequestedView</span></span>](requestedview.md)
  
```xml
<RequestedView>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</RequestedView>
```

 <span data-ttu-id="0735e-108">**FreeBusyViewType**</span><span class="sxs-lookup"><span data-stu-id="0735e-108">**FreeBusyViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0735e-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0735e-109">Attributes and elements</span></span>

<span data-ttu-id="0735e-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0735e-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0735e-111">属性</span><span class="sxs-lookup"><span data-stu-id="0735e-111">Attributes</span></span>

<span data-ttu-id="0735e-112">无。</span><span class="sxs-lookup"><span data-stu-id="0735e-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0735e-113">子元素</span><span class="sxs-lookup"><span data-stu-id="0735e-113">Child elements</span></span>

<span data-ttu-id="0735e-114">无。</span><span class="sxs-lookup"><span data-stu-id="0735e-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0735e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="0735e-115">Parent elements</span></span>

|<span data-ttu-id="0735e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="0735e-116">**Element**</span></span>|<span data-ttu-id="0735e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="0735e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0735e-118">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="0735e-118">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="0735e-119">指定响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="0735e-119">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="0735e-120">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="0735e-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0735e-121">文本值</span><span class="sxs-lookup"><span data-stu-id="0735e-121">Text value</span></span>

<span data-ttu-id="0735e-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="0735e-122">A text value is required.</span></span> <span data-ttu-id="0735e-123">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="0735e-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="0735e-124">**值**</span><span class="sxs-lookup"><span data-stu-id="0735e-124">**Value**</span></span>|<span data-ttu-id="0735e-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="0735e-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0735e-126">无</span><span class="sxs-lookup"><span data-stu-id="0735e-126">None</span></span>  <br/> |<span data-ttu-id="0735e-127">此值的请求无效。</span><span class="sxs-lookup"><span data-stu-id="0735e-127">This value is not valid for requests.</span></span> <span data-ttu-id="0735e-128">此值是有效的响应。</span><span class="sxs-lookup"><span data-stu-id="0735e-128">This value is valid for responses.</span></span>  <br/> |
|<span data-ttu-id="0735e-129">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="0735e-129">MergedOnly</span></span>  <br/> |<span data-ttu-id="0735e-130">表示一个聚合的忙/闲流。</span><span class="sxs-lookup"><span data-stu-id="0735e-130">Represents an aggregated free/busy stream.</span></span> <span data-ttu-id="0735e-131">在一个林中的目标用户不具有可用性服务配置跨林方案中，可用性服务请求者的忙/闲信息的公用文件夹中检索目标用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="0735e-131">In cross-forest scenarios in which the target user in one forest does not have an Availability service configured, the Availability service of the requestor retrieves the target user's free/busy information from the free/busy public folder.</span></span> <span data-ttu-id="0735e-132">公用文件夹只将忙/闲信息存储在合并的表单中，因为**MergedOnly**是唯一可用的信息。</span><span class="sxs-lookup"><span data-stu-id="0735e-132">Because public folders only store free/busy information in merged form, **MergedOnly** is the only available information.</span></span>  <br/> |
|<span data-ttu-id="0735e-133">FreeBusy</span><span class="sxs-lookup"><span data-stu-id="0735e-133">FreeBusy</span></span>  <br/> |<span data-ttu-id="0735e-134">表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF。</span><span class="sxs-lookup"><span data-stu-id="0735e-134">Represents the legacy status information: free, busy, tentative, and OOF.</span></span> <span data-ttu-id="0735e-135">这还包括约会的开始/结束的时间。</span><span class="sxs-lookup"><span data-stu-id="0735e-135">This also includes the start/end times of the appointments.</span></span> <span data-ttu-id="0735e-136">此视图是更丰富而不是一个聚合的忙/闲流提供比的旧的忙/闲查看，因为单个会议开始和结束时间。</span><span class="sxs-lookup"><span data-stu-id="0735e-136">This view is richer than the legacy free/busy view because individual meeting start and end times are provided instead of an aggregated free/busy stream.</span></span>  <br/> |
|<span data-ttu-id="0735e-137">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="0735e-137">FreeBusyMerged</span></span>  <br/> |<span data-ttu-id="0735e-138">代表中的所有属性**FreeBusy**与合并忙/闲信息的数据流。</span><span class="sxs-lookup"><span data-stu-id="0735e-138">Represents all the properties in **FreeBusy** with a stream of merged free/busy information.</span></span>  <br/> |
|<span data-ttu-id="0735e-139">Detailed</span><span class="sxs-lookup"><span data-stu-id="0735e-139">Detailed</span></span>  <br/> |<span data-ttu-id="0735e-140">表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF;约会; 的开始/结束时间和主题、 位置和重要性如约会的各种属性。</span><span class="sxs-lookup"><span data-stu-id="0735e-140">Represents the legacy status information: free, busy, tentative, and OOF; the start/end times of the appointments; and various properties of the appointment such as subject, location, and importance.</span></span> <span data-ttu-id="0735e-141">此请求的视图将返回的最大量为其特权发出请求的用户的信息。</span><span class="sxs-lookup"><span data-stu-id="0735e-141">This requested view will return the maximum amount of information for which the requesting user is privileged.</span></span> <span data-ttu-id="0735e-142">如果合并忙/闲信息仅为可用，为与用户的 Microsoft Exchange Server 2003 林请求信息**MergedOnly**将返回。</span><span class="sxs-lookup"><span data-stu-id="0735e-142">If merged free/busy information only is available, as with requesting information for users in a Microsoft Exchange Server 2003 forest, **MergedOnly** will be returned.</span></span> <span data-ttu-id="0735e-143">否则，将返回**FreeBusy**或**Detailed** 。</span><span class="sxs-lookup"><span data-stu-id="0735e-143">Otherwise, **FreeBusy** or **Detailed** will be returned.</span></span>  <br/> |
|<span data-ttu-id="0735e-144">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="0735e-144">DetailedMerged</span></span>  <br/> |<span data-ttu-id="0735e-145">代表中的所有属性**Detailed**与合并忙/闲信息的数据流。</span><span class="sxs-lookup"><span data-stu-id="0735e-145">Represents all the properties in **Detailed** with a stream of merged free/busy information.</span></span> <span data-ttu-id="0735e-146">如果合并忙/闲信息仅为可用，则将返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="0735e-146">If merged free/busy information only is available, **MergedOnly** will be returned.</span></span> <span data-ttu-id="0735e-147">否则，将返回**FreeBusyMerged**或**DetailedMerged** 。</span><span class="sxs-lookup"><span data-stu-id="0735e-147">Otherwise, **FreeBusyMerged** or **DetailedMerged** will be returned.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0735e-148">备注</span><span class="sxs-lookup"><span data-stu-id="0735e-148">Remarks</span></span>

<span data-ttu-id="0735e-149">此元素的设置的值与[FreeBusyViewType](freebusyviewtype.md)元素在响应中返回。</span><span class="sxs-lookup"><span data-stu-id="0735e-149">The value set by this element is returned with the [FreeBusyViewType](freebusyviewtype.md) element in the response.</span></span> 
  
<span data-ttu-id="0735e-150">下表显示不同的视图类型和相应的 MAPI 属性返回的内容。</span><span class="sxs-lookup"><span data-stu-id="0735e-150">The following table shows what is returned for the different view types and the corresponding MAPI property.</span></span> <span data-ttu-id="0735e-151">每个视图类型基于以前的视图类型。</span><span class="sxs-lookup"><span data-stu-id="0735e-151">Each view type builds upon the former view type.</span></span>
  
|<span data-ttu-id="0735e-152">**忙/闲视图类型**</span><span class="sxs-lookup"><span data-stu-id="0735e-152">**Free/Busy View Type**</span></span>|<span data-ttu-id="0735e-153">**属性**</span><span class="sxs-lookup"><span data-stu-id="0735e-153">**Properties**</span></span>|<span data-ttu-id="0735e-154">**MAPI 日历属性**</span><span class="sxs-lookup"><span data-stu-id="0735e-154">**MAPI Calendar Property**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0735e-155">**MergedOnly**</span><span class="sxs-lookup"><span data-stu-id="0735e-155">**MergedOnly**</span></span> <br/> |<span data-ttu-id="0735e-156">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="0735e-156">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="0735e-157">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="0735e-157">**FreeBusy**</span></span> <br/> |<span data-ttu-id="0735e-158">古典状态</span><span class="sxs-lookup"><span data-stu-id="0735e-158">Classical status</span></span>  <br/> |<span data-ttu-id="0735e-159">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="0735e-159">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="0735e-160">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="0735e-160">**FreeBusy**</span></span> <br/> |<span data-ttu-id="0735e-161">工作时间</span><span class="sxs-lookup"><span data-stu-id="0735e-161">Working hours</span></span>  <br/> ||
|<span data-ttu-id="0735e-162">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="0735e-162">**FreeBusy**</span></span> <br/> |<span data-ttu-id="0735e-163">开始时间</span><span class="sxs-lookup"><span data-stu-id="0735e-163">Start time</span></span>  <br/> |<span data-ttu-id="0735e-164">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="0735e-164">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="0735e-165">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="0735e-165">**FreeBusy**</span></span> <br/> |<span data-ttu-id="0735e-166">结束时间</span><span class="sxs-lookup"><span data-stu-id="0735e-166">End time</span></span>  <br/> |<span data-ttu-id="0735e-167">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="0735e-167">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="0735e-168">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-168">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="0735e-169">古典状态</span><span class="sxs-lookup"><span data-stu-id="0735e-169">Classical status</span></span>  <br/> |<span data-ttu-id="0735e-170">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="0735e-170">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="0735e-171">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-171">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="0735e-172">工作时间</span><span class="sxs-lookup"><span data-stu-id="0735e-172">Working hours</span></span>  <br/> ||
|<span data-ttu-id="0735e-173">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-173">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="0735e-174">开始时间</span><span class="sxs-lookup"><span data-stu-id="0735e-174">Start time</span></span>  <br/> |<span data-ttu-id="0735e-175">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="0735e-175">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="0735e-176">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-176">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="0735e-177">结束时间</span><span class="sxs-lookup"><span data-stu-id="0735e-177">End time</span></span>  <br/> |<span data-ttu-id="0735e-178">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="0735e-178">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="0735e-179">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-179">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="0735e-180">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="0735e-180">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="0735e-181">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-181">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-182">古典状态</span><span class="sxs-lookup"><span data-stu-id="0735e-182">Classical status</span></span>  <br/> |<span data-ttu-id="0735e-183">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="0735e-183">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="0735e-184">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-184">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-185">工作时间</span><span class="sxs-lookup"><span data-stu-id="0735e-185">Working hours</span></span>  <br/> ||
|<span data-ttu-id="0735e-186">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-186">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-187">开始时间</span><span class="sxs-lookup"><span data-stu-id="0735e-187">Start time</span></span>  <br/> |<span data-ttu-id="0735e-188">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="0735e-188">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="0735e-189">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-189">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-190">结束时间</span><span class="sxs-lookup"><span data-stu-id="0735e-190">End time</span></span>  <br/> |<span data-ttu-id="0735e-191">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="0735e-191">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="0735e-192">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-192">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-193">主题</span><span class="sxs-lookup"><span data-stu-id="0735e-193">Subject</span></span>  <br/> |<span data-ttu-id="0735e-194">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="0735e-194">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="0735e-195">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-195">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-196">位置</span><span class="sxs-lookup"><span data-stu-id="0735e-196">Location</span></span>  <br/> |<span data-ttu-id="0735e-197">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="0735e-197">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="0735e-198">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-198">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-199">条目 Id(unless private)</span><span class="sxs-lookup"><span data-stu-id="0735e-199">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="0735e-200">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-200">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-201">私有标志</span><span class="sxs-lookup"><span data-stu-id="0735e-201">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="0735e-202">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-202">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-203">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="0735e-203">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="0735e-204">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-204">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-205">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="0735e-205">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="0735e-206">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-206">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-207">IsException</span><span class="sxs-lookup"><span data-stu-id="0735e-207">IsException</span></span>  <br/> ||
|<span data-ttu-id="0735e-208">**详细**</span><span class="sxs-lookup"><span data-stu-id="0735e-208">**Detailed**</span></span> <br/> |<span data-ttu-id="0735e-209">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="0735e-209">IsReminderSet</span></span>  <br/> ||
|<span data-ttu-id="0735e-210">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-210">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-211">古典状态</span><span class="sxs-lookup"><span data-stu-id="0735e-211">Classical status</span></span>  <br/> |<span data-ttu-id="0735e-212">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="0735e-212">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="0735e-213">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-213">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-214">工作时间</span><span class="sxs-lookup"><span data-stu-id="0735e-214">Working hours</span></span>  <br/> ||
|<span data-ttu-id="0735e-215">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-215">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-216">开始时间</span><span class="sxs-lookup"><span data-stu-id="0735e-216">Start time</span></span>  <br/> |<span data-ttu-id="0735e-217">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="0735e-217">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="0735e-218">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-218">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-219">结束时间</span><span class="sxs-lookup"><span data-stu-id="0735e-219">End time</span></span>  <br/> |<span data-ttu-id="0735e-220">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="0735e-220">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="0735e-221">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-221">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-222">主题</span><span class="sxs-lookup"><span data-stu-id="0735e-222">Subject</span></span>  <br/> |<span data-ttu-id="0735e-223">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="0735e-223">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="0735e-224">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-224">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-225">位置</span><span class="sxs-lookup"><span data-stu-id="0735e-225">Location</span></span>  <br/> |<span data-ttu-id="0735e-226">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="0735e-226">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="0735e-227">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-227">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-228">条目 Id(unless private)</span><span class="sxs-lookup"><span data-stu-id="0735e-228">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="0735e-229">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-229">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-230">私有标志</span><span class="sxs-lookup"><span data-stu-id="0735e-230">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="0735e-231">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-231">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-232">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="0735e-232">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="0735e-233">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-233">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-234">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="0735e-234">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="0735e-235">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-235">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-236">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="0735e-236">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="0735e-237">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-237">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-238">IsException</span><span class="sxs-lookup"><span data-stu-id="0735e-238">IsException</span></span>  <br/> ||
|<span data-ttu-id="0735e-239">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="0735e-239">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="0735e-240">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="0735e-240">IsReminderSet</span></span>  <br/> ||
   
## <a name="element-information"></a><span data-ttu-id="0735e-241">元素信息</span><span class="sxs-lookup"><span data-stu-id="0735e-241">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0735e-242">命名空间</span><span class="sxs-lookup"><span data-stu-id="0735e-242">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0735e-243">架构名称</span><span class="sxs-lookup"><span data-stu-id="0735e-243">Schema Name</span></span>  <br/> |<span data-ttu-id="0735e-244">类型架构</span><span class="sxs-lookup"><span data-stu-id="0735e-244">Types schema</span></span>  <br/> |
|<span data-ttu-id="0735e-245">验证文件</span><span class="sxs-lookup"><span data-stu-id="0735e-245">Validation File</span></span>  <br/> |<span data-ttu-id="0735e-246">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0735e-246">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0735e-247">可以为空</span><span class="sxs-lookup"><span data-stu-id="0735e-247">Can be Empty</span></span>  <br/> |<span data-ttu-id="0735e-248">False</span><span class="sxs-lookup"><span data-stu-id="0735e-248">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0735e-249">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0735e-249">See also</span></span>



[<span data-ttu-id="0735e-250">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="0735e-250">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="0735e-251">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="0735e-251">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

