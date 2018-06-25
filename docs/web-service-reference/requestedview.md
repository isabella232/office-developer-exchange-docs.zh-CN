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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827145"
---
# <a name="requestedview"></a><span data-ttu-id="2e07c-103">RequestedView</span><span class="sxs-lookup"><span data-stu-id="2e07c-103">RequestedView</span></span>

<span data-ttu-id="2e07c-104">**RequestedView**元素定义的客户端请求的日历信息的类型。</span><span class="sxs-lookup"><span data-stu-id="2e07c-104">The **RequestedView** element defines the type of calendar information that a client requests.</span></span> 
  
[<span data-ttu-id="2e07c-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="2e07c-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="2e07c-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="2e07c-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="2e07c-107">RequestedView</span><span class="sxs-lookup"><span data-stu-id="2e07c-107">RequestedView</span></span>](requestedview.md)
  
```xml
<RequestedView>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</RequestedView>
```

 <span data-ttu-id="2e07c-108">**FreeBusyViewType**</span><span class="sxs-lookup"><span data-stu-id="2e07c-108">**FreeBusyViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e07c-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2e07c-109">Attributes and elements</span></span>

<span data-ttu-id="2e07c-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2e07c-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e07c-111">属性</span><span class="sxs-lookup"><span data-stu-id="2e07c-111">Attributes</span></span>

<span data-ttu-id="2e07c-112">无。</span><span class="sxs-lookup"><span data-stu-id="2e07c-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e07c-113">子元素</span><span class="sxs-lookup"><span data-stu-id="2e07c-113">Child elements</span></span>

<span data-ttu-id="2e07c-114">无。</span><span class="sxs-lookup"><span data-stu-id="2e07c-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2e07c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2e07c-115">Parent elements</span></span>

|<span data-ttu-id="2e07c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e07c-116">**Element**</span></span>|<span data-ttu-id="2e07c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e07c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e07c-118">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="2e07c-118">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="2e07c-119">指定响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="2e07c-119">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="2e07c-120">以下是此元素的 XPath:</span><span class="sxs-lookup"><span data-stu-id="2e07c-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2e07c-121">文本值</span><span class="sxs-lookup"><span data-stu-id="2e07c-121">Text value</span></span>

<span data-ttu-id="2e07c-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="2e07c-122">A text value is required.</span></span> <span data-ttu-id="2e07c-123">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="2e07c-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="2e07c-124">**值**</span><span class="sxs-lookup"><span data-stu-id="2e07c-124">**Value**</span></span>|<span data-ttu-id="2e07c-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e07c-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e07c-126">无</span><span class="sxs-lookup"><span data-stu-id="2e07c-126">None</span></span>  <br/> |<span data-ttu-id="2e07c-127">此值的请求无效。</span><span class="sxs-lookup"><span data-stu-id="2e07c-127">This value is not valid for requests.</span></span> <span data-ttu-id="2e07c-128">此值是有效的响应。</span><span class="sxs-lookup"><span data-stu-id="2e07c-128">This value is valid for responses.</span></span>  <br/> |
|<span data-ttu-id="2e07c-129">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="2e07c-129">MergedOnly</span></span>  <br/> |<span data-ttu-id="2e07c-130">表示一个聚合的忙/闲流。</span><span class="sxs-lookup"><span data-stu-id="2e07c-130">Represents an aggregated free/busy stream.</span></span> <span data-ttu-id="2e07c-131">在一个林中的目标用户不具有可用性服务配置跨林方案中，可用性服务请求者的忙/闲信息的公用文件夹中检索目标用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="2e07c-131">In cross-forest scenarios in which the target user in one forest does not have an Availability service configured, the Availability service of the requestor retrieves the target user's free/busy information from the free/busy public folder.</span></span> <span data-ttu-id="2e07c-132">公用文件夹只将忙/闲信息存储在合并的表单中，因为**MergedOnly**是唯一可用的信息。</span><span class="sxs-lookup"><span data-stu-id="2e07c-132">Because public folders only store free/busy information in merged form, **MergedOnly** is the only available information.</span></span>  <br/> |
|<span data-ttu-id="2e07c-133">FreeBusy</span><span class="sxs-lookup"><span data-stu-id="2e07c-133">FreeBusy</span></span>  <br/> |<span data-ttu-id="2e07c-134">表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF。</span><span class="sxs-lookup"><span data-stu-id="2e07c-134">Represents the legacy status information: free, busy, tentative, and OOF.</span></span> <span data-ttu-id="2e07c-135">这还包括约会的开始/结束的时间。</span><span class="sxs-lookup"><span data-stu-id="2e07c-135">This also includes the start/end times of the appointments.</span></span> <span data-ttu-id="2e07c-136">此视图是更丰富而不是一个聚合的忙/闲流提供比的旧的忙/闲查看，因为单个会议开始和结束时间。</span><span class="sxs-lookup"><span data-stu-id="2e07c-136">This view is richer than the legacy free/busy view because individual meeting start and end times are provided instead of an aggregated free/busy stream.</span></span>  <br/> |
|<span data-ttu-id="2e07c-137">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="2e07c-137">FreeBusyMerged</span></span>  <br/> |<span data-ttu-id="2e07c-138">代表中的所有属性**FreeBusy**与合并忙/闲信息的数据流。</span><span class="sxs-lookup"><span data-stu-id="2e07c-138">Represents all the properties in **FreeBusy** with a stream of merged free/busy information.</span></span>  <br/> |
|<span data-ttu-id="2e07c-139">Detailed</span><span class="sxs-lookup"><span data-stu-id="2e07c-139">Detailed</span></span>  <br/> |<span data-ttu-id="2e07c-140">表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF;约会; 的开始/结束时间和主题、 位置和重要性如约会的各种属性。</span><span class="sxs-lookup"><span data-stu-id="2e07c-140">Represents the legacy status information: free, busy, tentative, and OOF; the start/end times of the appointments; and various properties of the appointment such as subject, location, and importance.</span></span> <span data-ttu-id="2e07c-141">此请求的视图将返回的最大量为其特权发出请求的用户的信息。</span><span class="sxs-lookup"><span data-stu-id="2e07c-141">This requested view will return the maximum amount of information for which the requesting user is privileged.</span></span> <span data-ttu-id="2e07c-142">如果合并忙/闲信息仅为可用，为与用户的 Microsoft Exchange Server 2003 林请求信息**MergedOnly**将返回。</span><span class="sxs-lookup"><span data-stu-id="2e07c-142">If merged free/busy information only is available, as with requesting information for users in a Microsoft Exchange Server 2003 forest, **MergedOnly** will be returned.</span></span> <span data-ttu-id="2e07c-143">否则，将返回**FreeBusy**或**Detailed** 。</span><span class="sxs-lookup"><span data-stu-id="2e07c-143">Otherwise, **FreeBusy** or **Detailed** will be returned.</span></span>  <br/> |
|<span data-ttu-id="2e07c-144">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="2e07c-144">DetailedMerged</span></span>  <br/> |<span data-ttu-id="2e07c-145">代表中的所有属性**Detailed**与合并忙/闲信息的数据流。</span><span class="sxs-lookup"><span data-stu-id="2e07c-145">Represents all the properties in **Detailed** with a stream of merged free/busy information.</span></span> <span data-ttu-id="2e07c-146">如果合并忙/闲信息仅为可用，则将返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="2e07c-146">If merged free/busy information only is available, **MergedOnly** will be returned.</span></span> <span data-ttu-id="2e07c-147">否则，将返回**FreeBusyMerged**或**DetailedMerged** 。</span><span class="sxs-lookup"><span data-stu-id="2e07c-147">Otherwise, **FreeBusyMerged** or **DetailedMerged** will be returned.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e07c-148">注解</span><span class="sxs-lookup"><span data-stu-id="2e07c-148">Remarks</span></span>

<span data-ttu-id="2e07c-149">此元素的设置的值与[FreeBusyViewType](freebusyviewtype.md)元素在响应中返回。</span><span class="sxs-lookup"><span data-stu-id="2e07c-149">The value set by this element is returned with the [FreeBusyViewType](freebusyviewtype.md) element in the response.</span></span> 
  
<span data-ttu-id="2e07c-150">下表显示不同的视图类型和相应的 MAPI 属性返回的内容。</span><span class="sxs-lookup"><span data-stu-id="2e07c-150">The following table shows what is returned for the different view types and the corresponding MAPI property.</span></span> <span data-ttu-id="2e07c-151">每个视图类型基于以前的视图类型。</span><span class="sxs-lookup"><span data-stu-id="2e07c-151">Each view type builds upon the former view type.</span></span>
  
|<span data-ttu-id="2e07c-152">**忙/闲视图类型**</span><span class="sxs-lookup"><span data-stu-id="2e07c-152">**Free/Busy View Type**</span></span>|<span data-ttu-id="2e07c-153">**属性**</span><span class="sxs-lookup"><span data-stu-id="2e07c-153">**Properties**</span></span>|<span data-ttu-id="2e07c-154">**MAPI 日历属性**</span><span class="sxs-lookup"><span data-stu-id="2e07c-154">**MAPI Calendar Property**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2e07c-155">**MergedOnly**</span><span class="sxs-lookup"><span data-stu-id="2e07c-155">**MergedOnly**</span></span> <br/> |<span data-ttu-id="2e07c-156">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="2e07c-156">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="2e07c-157">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="2e07c-157">**FreeBusy**</span></span> <br/> |<span data-ttu-id="2e07c-158">古典状态</span><span class="sxs-lookup"><span data-stu-id="2e07c-158">Classical status</span></span>  <br/> |<span data-ttu-id="2e07c-159">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="2e07c-159">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="2e07c-160">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="2e07c-160">**FreeBusy**</span></span> <br/> |<span data-ttu-id="2e07c-161">工作时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-161">Working hours</span></span>  <br/> ||
|<span data-ttu-id="2e07c-162">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="2e07c-162">**FreeBusy**</span></span> <br/> |<span data-ttu-id="2e07c-163">开始时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-163">Start time</span></span>  <br/> |<span data-ttu-id="2e07c-164">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="2e07c-164">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="2e07c-165">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="2e07c-165">**FreeBusy**</span></span> <br/> |<span data-ttu-id="2e07c-166">结束时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-166">End time</span></span>  <br/> |<span data-ttu-id="2e07c-167">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="2e07c-167">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="2e07c-168">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-168">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="2e07c-169">古典状态</span><span class="sxs-lookup"><span data-stu-id="2e07c-169">Classical status</span></span>  <br/> |<span data-ttu-id="2e07c-170">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="2e07c-170">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="2e07c-171">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-171">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="2e07c-172">工作时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-172">Working hours</span></span>  <br/> ||
|<span data-ttu-id="2e07c-173">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-173">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="2e07c-174">开始时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-174">Start time</span></span>  <br/> |<span data-ttu-id="2e07c-175">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="2e07c-175">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="2e07c-176">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-176">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="2e07c-177">结束时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-177">End time</span></span>  <br/> |<span data-ttu-id="2e07c-178">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="2e07c-178">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="2e07c-179">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-179">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="2e07c-180">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="2e07c-180">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="2e07c-181">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-181">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-182">古典状态</span><span class="sxs-lookup"><span data-stu-id="2e07c-182">Classical status</span></span>  <br/> |<span data-ttu-id="2e07c-183">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="2e07c-183">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="2e07c-184">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-184">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-185">工作时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-185">Working hours</span></span>  <br/> ||
|<span data-ttu-id="2e07c-186">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-186">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-187">开始时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-187">Start time</span></span>  <br/> |<span data-ttu-id="2e07c-188">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="2e07c-188">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="2e07c-189">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-189">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-190">结束时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-190">End time</span></span>  <br/> |<span data-ttu-id="2e07c-191">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="2e07c-191">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="2e07c-192">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-192">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-193">主题</span><span class="sxs-lookup"><span data-stu-id="2e07c-193">Subject</span></span>  <br/> |<span data-ttu-id="2e07c-194">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="2e07c-194">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="2e07c-195">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-195">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-196">位置</span><span class="sxs-lookup"><span data-stu-id="2e07c-196">Location</span></span>  <br/> |<span data-ttu-id="2e07c-197">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="2e07c-197">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="2e07c-198">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-198">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-199">条目 Id(unless private)</span><span class="sxs-lookup"><span data-stu-id="2e07c-199">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="2e07c-200">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-200">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-201">私有标志</span><span class="sxs-lookup"><span data-stu-id="2e07c-201">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="2e07c-202">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-202">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-203">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="2e07c-203">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="2e07c-204">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-204">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-205">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="2e07c-205">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="2e07c-206">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-206">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-207">IsException</span><span class="sxs-lookup"><span data-stu-id="2e07c-207">IsException</span></span>  <br/> ||
|<span data-ttu-id="2e07c-208">**详细**</span><span class="sxs-lookup"><span data-stu-id="2e07c-208">**Detailed**</span></span> <br/> |<span data-ttu-id="2e07c-209">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="2e07c-209">IsReminderSet</span></span>  <br/> ||
|<span data-ttu-id="2e07c-210">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-210">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-211">古典状态</span><span class="sxs-lookup"><span data-stu-id="2e07c-211">Classical status</span></span>  <br/> |<span data-ttu-id="2e07c-212">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="2e07c-212">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="2e07c-213">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-213">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-214">工作时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-214">Working hours</span></span>  <br/> ||
|<span data-ttu-id="2e07c-215">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-215">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-216">开始时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-216">Start time</span></span>  <br/> |<span data-ttu-id="2e07c-217">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="2e07c-217">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="2e07c-218">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-218">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-219">结束时间</span><span class="sxs-lookup"><span data-stu-id="2e07c-219">End time</span></span>  <br/> |<span data-ttu-id="2e07c-220">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="2e07c-220">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="2e07c-221">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-221">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-222">主题</span><span class="sxs-lookup"><span data-stu-id="2e07c-222">Subject</span></span>  <br/> |<span data-ttu-id="2e07c-223">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="2e07c-223">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="2e07c-224">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-224">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-225">位置</span><span class="sxs-lookup"><span data-stu-id="2e07c-225">Location</span></span>  <br/> |<span data-ttu-id="2e07c-226">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="2e07c-226">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="2e07c-227">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-227">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-228">条目 Id(unless private)</span><span class="sxs-lookup"><span data-stu-id="2e07c-228">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="2e07c-229">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-229">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-230">私有标志</span><span class="sxs-lookup"><span data-stu-id="2e07c-230">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="2e07c-231">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-231">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-232">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="2e07c-232">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="2e07c-233">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-233">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-234">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="2e07c-234">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="2e07c-235">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-235">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-236">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="2e07c-236">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="2e07c-237">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-237">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-238">IsException</span><span class="sxs-lookup"><span data-stu-id="2e07c-238">IsException</span></span>  <br/> ||
|<span data-ttu-id="2e07c-239">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="2e07c-239">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="2e07c-240">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="2e07c-240">IsReminderSet</span></span>  <br/> ||
   
## <a name="element-information"></a><span data-ttu-id="2e07c-241">元素信息</span><span class="sxs-lookup"><span data-stu-id="2e07c-241">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e07c-242">命名空间</span><span class="sxs-lookup"><span data-stu-id="2e07c-242">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e07c-243">架构名称</span><span class="sxs-lookup"><span data-stu-id="2e07c-243">Schema Name</span></span>  <br/> |<span data-ttu-id="2e07c-244">类型架构</span><span class="sxs-lookup"><span data-stu-id="2e07c-244">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e07c-245">验证文件</span><span class="sxs-lookup"><span data-stu-id="2e07c-245">Validation File</span></span>  <br/> |<span data-ttu-id="2e07c-246">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2e07c-246">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e07c-247">可以为空</span><span class="sxs-lookup"><span data-stu-id="2e07c-247">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e07c-248">False</span><span class="sxs-lookup"><span data-stu-id="2e07c-248">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e07c-249">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2e07c-249">See also</span></span>



[<span data-ttu-id="2e07c-250">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="2e07c-250">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="2e07c-251">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="2e07c-251">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

