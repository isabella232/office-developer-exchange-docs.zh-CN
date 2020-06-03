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
description: RequestedView 元素定义客户端请求的日历信息的类型。
ms.openlocfilehash: bc4f863841fc5a7d1d23f0bd4c7c2895d2593a2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459158"
---
# <a name="requestedview"></a><span data-ttu-id="aa4bc-103">RequestedView</span><span class="sxs-lookup"><span data-stu-id="aa4bc-103">RequestedView</span></span>

<span data-ttu-id="aa4bc-104">**RequestedView**元素定义客户端请求的日历信息的类型。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-104">The **RequestedView** element defines the type of calendar information that a client requests.</span></span> 
  
[<span data-ttu-id="aa4bc-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="aa4bc-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="aa4bc-106">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="aa4bc-106">FreeBusyViewOptions</span></span>](freebusyviewoptions.md)
  
[<span data-ttu-id="aa4bc-107">RequestedView</span><span class="sxs-lookup"><span data-stu-id="aa4bc-107">RequestedView</span></span>](requestedview.md)
  
```xml
<RequestedView>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</RequestedView>
```

 <span data-ttu-id="aa4bc-108">**FreeBusyViewType**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-108">**FreeBusyViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa4bc-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa4bc-109">Attributes and elements</span></span>

<span data-ttu-id="aa4bc-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa4bc-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="aa4bc-111">Attributes</span></span>

<span data-ttu-id="aa4bc-112">无。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa4bc-113">子元素</span><span class="sxs-lookup"><span data-stu-id="aa4bc-113">Child elements</span></span>

<span data-ttu-id="aa4bc-114">无。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aa4bc-115">父元素</span><span class="sxs-lookup"><span data-stu-id="aa4bc-115">Parent elements</span></span>

|<span data-ttu-id="aa4bc-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-116">**Element**</span></span>|<span data-ttu-id="aa4bc-117">**描述**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa4bc-118">FreeBusyViewOptions</span><span class="sxs-lookup"><span data-stu-id="aa4bc-118">FreeBusyViewOptions</span></span>](freebusyviewoptions.md) <br/> |<span data-ttu-id="aa4bc-119">指定响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-119">Specifies the type of free/busy information returned in the response.</span></span>  <br/> <span data-ttu-id="aa4bc-120">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="aa4bc-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aa4bc-121">文本值</span><span class="sxs-lookup"><span data-stu-id="aa4bc-121">Text value</span></span>

<span data-ttu-id="aa4bc-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-122">A text value is required.</span></span> <span data-ttu-id="aa4bc-123">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-123">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="aa4bc-124">**值**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-124">**Value**</span></span>|<span data-ttu-id="aa4bc-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa4bc-126">无</span><span class="sxs-lookup"><span data-stu-id="aa4bc-126">None</span></span>  <br/> |<span data-ttu-id="aa4bc-127">对于请求，此值无效。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-127">This value is not valid for requests.</span></span> <span data-ttu-id="aa4bc-128">此值对响应有效。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-128">This value is valid for responses.</span></span>  <br/> |
|<span data-ttu-id="aa4bc-129">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="aa4bc-129">MergedOnly</span></span>  <br/> |<span data-ttu-id="aa4bc-130">表示聚合的忙/闲流。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-130">Represents an aggregated free/busy stream.</span></span> <span data-ttu-id="aa4bc-131">在跨林方案中，在一个林中的目标用户未配置可用性服务的情况下，请求者的可用性服务将从忙/闲公用文件夹中检索目标用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-131">In cross-forest scenarios in which the target user in one forest does not have an Availability service configured, the Availability service of the requestor retrieves the target user's free/busy information from the free/busy public folder.</span></span> <span data-ttu-id="aa4bc-132">由于公用文件夹仅将忙/闲信息存储在合并表单中，因此**MergedOnly**是唯一可用的信息。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-132">Because public folders only store free/busy information in merged form, **MergedOnly** is the only available information.</span></span>  <br/> |
|<span data-ttu-id="aa4bc-133">FreeBusy</span><span class="sxs-lookup"><span data-stu-id="aa4bc-133">FreeBusy</span></span>  <br/> |<span data-ttu-id="aa4bc-134">代表旧状态信息：闲、忙、暂定和 OOF。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-134">Represents the legacy status information: free, busy, tentative, and OOF.</span></span> <span data-ttu-id="aa4bc-135">这还包括约会的开始/结束时间。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-135">This also includes the start/end times of the appointments.</span></span> <span data-ttu-id="aa4bc-136">此视图比旧版的忙/闲视图更丰富，因为提供了单个会议开始和结束时间，而不是聚合的忙/闲流。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-136">This view is richer than the legacy free/busy view because individual meeting start and end times are provided instead of an aggregated free/busy stream.</span></span>  <br/> |
|<span data-ttu-id="aa4bc-137">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="aa4bc-137">FreeBusyMerged</span></span>  <br/> |<span data-ttu-id="aa4bc-138">表示包含合并的忙/闲信息流的**FreeBusy**中的所有属性。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-138">Represents all the properties in **FreeBusy** with a stream of merged free/busy information.</span></span>  <br/> |
|<span data-ttu-id="aa4bc-139">具体</span><span class="sxs-lookup"><span data-stu-id="aa4bc-139">Detailed</span></span>  <br/> |<span data-ttu-id="aa4bc-140">代表旧状态信息：闲、忙、暂定和 OOF;约会的开始/结束时间;以及约会的各种属性，如主题、位置和重要性。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-140">Represents the legacy status information: free, busy, tentative, and OOF; the start/end times of the appointments; and various properties of the appointment such as subject, location, and importance.</span></span> <span data-ttu-id="aa4bc-141">此请求的视图将返回请求用户有权限的最大信息量。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-141">This requested view will return the maximum amount of information for which the requesting user is privileged.</span></span> <span data-ttu-id="aa4bc-142">如果只提供了合并的忙/闲信息，就像 Microsoft Exchange Server 2003 林中的用户请求信息一样，将返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-142">If merged free/busy information only is available, as with requesting information for users in a Microsoft Exchange Server 2003 forest, **MergedOnly** will be returned.</span></span> <span data-ttu-id="aa4bc-143">否则，将返回**FreeBusy**或**详细信息**。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-143">Otherwise, **FreeBusy** or **Detailed** will be returned.</span></span>  <br/> |
|<span data-ttu-id="aa4bc-144">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="aa4bc-144">DetailedMerged</span></span>  <br/> |<span data-ttu-id="aa4bc-145">表示与合并的忙/闲信息流**详细**的所有属性。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-145">Represents all the properties in **Detailed** with a stream of merged free/busy information.</span></span> <span data-ttu-id="aa4bc-146">如果仅提供了合并的忙/闲信息，将返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-146">If merged free/busy information only is available, **MergedOnly** will be returned.</span></span> <span data-ttu-id="aa4bc-147">否则，将返回**FreeBusyMerged**或**DetailedMerged** 。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-147">Otherwise, **FreeBusyMerged** or **DetailedMerged** will be returned.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa4bc-148">备注</span><span class="sxs-lookup"><span data-stu-id="aa4bc-148">Remarks</span></span>

<span data-ttu-id="aa4bc-149">此元素设置的值随响应中的[FreeBusyViewType](freebusyviewtype.md)元素一起返回。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-149">The value set by this element is returned with the [FreeBusyViewType](freebusyviewtype.md) element in the response.</span></span> 
  
<span data-ttu-id="aa4bc-150">下表显示了为不同的视图类型和相应的 MAPI 属性返回的内容。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-150">The following table shows what is returned for the different view types and the corresponding MAPI property.</span></span> <span data-ttu-id="aa4bc-151">每个视图类型都基于以前的视图类型。</span><span class="sxs-lookup"><span data-stu-id="aa4bc-151">Each view type builds upon the former view type.</span></span>
  
|<span data-ttu-id="aa4bc-152">**忙/闲视图类型**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-152">**Free/Busy View Type**</span></span>|<span data-ttu-id="aa4bc-153">**属性**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-153">**Properties**</span></span>|<span data-ttu-id="aa4bc-154">**MAPI 日历属性**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-154">**MAPI Calendar Property**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa4bc-155">**MergedOnly**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-155">**MergedOnly**</span></span> <br/> |<span data-ttu-id="aa4bc-156">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="aa4bc-156">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-157">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-157">**FreeBusy**</span></span> <br/> |<span data-ttu-id="aa4bc-158">古典状态</span><span class="sxs-lookup"><span data-stu-id="aa4bc-158">Classical status</span></span>  <br/> |<span data-ttu-id="aa4bc-159">属性标记（0x80860003）</span><span class="sxs-lookup"><span data-stu-id="aa4bc-159">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="aa4bc-160">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-160">**FreeBusy**</span></span> <br/> |<span data-ttu-id="aa4bc-161">工作时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-161">Working hours</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-162">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-162">**FreeBusy**</span></span> <br/> |<span data-ttu-id="aa4bc-163">开始时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-163">Start time</span></span>  <br/> |<span data-ttu-id="aa4bc-164">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="aa4bc-164">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="aa4bc-165">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-165">**FreeBusy**</span></span> <br/> |<span data-ttu-id="aa4bc-166">结束时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-166">End time</span></span>  <br/> |<span data-ttu-id="aa4bc-167">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="aa4bc-167">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="aa4bc-168">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-168">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-169">古典状态</span><span class="sxs-lookup"><span data-stu-id="aa4bc-169">Classical status</span></span>  <br/> |<span data-ttu-id="aa4bc-170">属性标记（0x80860003）</span><span class="sxs-lookup"><span data-stu-id="aa4bc-170">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="aa4bc-171">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-171">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-172">工作时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-172">Working hours</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-173">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-173">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-174">开始时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-174">Start time</span></span>  <br/> |<span data-ttu-id="aa4bc-175">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="aa4bc-175">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="aa4bc-176">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-176">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-177">结束时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-177">End time</span></span>  <br/> |<span data-ttu-id="aa4bc-178">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="aa4bc-178">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="aa4bc-179">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-179">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-180">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="aa4bc-180">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-181">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-181">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-182">古典状态</span><span class="sxs-lookup"><span data-stu-id="aa4bc-182">Classical status</span></span>  <br/> |<span data-ttu-id="aa4bc-183">属性标记（0x80860003）</span><span class="sxs-lookup"><span data-stu-id="aa4bc-183">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="aa4bc-184">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-184">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-185">工作时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-185">Working hours</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-186">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-186">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-187">开始时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-187">Start time</span></span>  <br/> |<span data-ttu-id="aa4bc-188">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="aa4bc-188">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="aa4bc-189">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-189">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-190">结束时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-190">End time</span></span>  <br/> |<span data-ttu-id="aa4bc-191">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="aa4bc-191">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="aa4bc-192">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-192">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-193">Subject</span><span class="sxs-lookup"><span data-stu-id="aa4bc-193">Subject</span></span>  <br/> |<span data-ttu-id="aa4bc-194">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="aa4bc-194">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="aa4bc-195">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-195">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-196">位置</span><span class="sxs-lookup"><span data-stu-id="aa4bc-196">Location</span></span>  <br/> |<span data-ttu-id="aa4bc-197">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="aa4bc-197">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="aa4bc-198">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-198">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-199">条目 Id （除非是私有）</span><span class="sxs-lookup"><span data-stu-id="aa4bc-199">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-200">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-200">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-201">私有标志</span><span class="sxs-lookup"><span data-stu-id="aa4bc-201">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-202">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-202">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-203">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="aa4bc-203">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-204">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-204">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-205">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="aa4bc-205">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-206">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-206">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-207">IsException</span><span class="sxs-lookup"><span data-stu-id="aa4bc-207">IsException</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-208">**具体**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-208">**Detailed**</span></span> <br/> |<span data-ttu-id="aa4bc-209">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="aa4bc-209">IsReminderSet</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-210">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-210">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-211">古典状态</span><span class="sxs-lookup"><span data-stu-id="aa4bc-211">Classical status</span></span>  <br/> |<span data-ttu-id="aa4bc-212">属性标记（0x80860003）</span><span class="sxs-lookup"><span data-stu-id="aa4bc-212">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="aa4bc-213">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-213">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-214">工作时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-214">Working hours</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-215">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-215">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-216">开始时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-216">Start time</span></span>  <br/> |<span data-ttu-id="aa4bc-217">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="aa4bc-217">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="aa4bc-218">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-218">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-219">结束时间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-219">End time</span></span>  <br/> |<span data-ttu-id="aa4bc-220">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="aa4bc-220">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="aa4bc-221">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-221">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-222">Subject</span><span class="sxs-lookup"><span data-stu-id="aa4bc-222">Subject</span></span>  <br/> |<span data-ttu-id="aa4bc-223">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="aa4bc-223">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="aa4bc-224">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-224">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-225">位置</span><span class="sxs-lookup"><span data-stu-id="aa4bc-225">Location</span></span>  <br/> |<span data-ttu-id="aa4bc-226">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="aa4bc-226">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="aa4bc-227">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-227">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-228">条目 Id （除非是私有）</span><span class="sxs-lookup"><span data-stu-id="aa4bc-228">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-229">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-229">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-230">私有标志</span><span class="sxs-lookup"><span data-stu-id="aa4bc-230">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-231">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-231">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-232">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="aa4bc-232">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-233">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-233">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-234">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="aa4bc-234">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-235">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-235">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-236">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="aa4bc-236">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-237">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-237">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-238">IsException</span><span class="sxs-lookup"><span data-stu-id="aa4bc-238">IsException</span></span>  <br/> ||
|<span data-ttu-id="aa4bc-239">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="aa4bc-239">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="aa4bc-240">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="aa4bc-240">IsReminderSet</span></span>  <br/> ||
   
## <a name="element-information"></a><span data-ttu-id="aa4bc-241">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa4bc-241">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa4bc-242">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa4bc-242">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aa4bc-243">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa4bc-243">Schema Name</span></span>  <br/> |<span data-ttu-id="aa4bc-244">类型架构</span><span class="sxs-lookup"><span data-stu-id="aa4bc-244">Types schema</span></span>  <br/> |
|<span data-ttu-id="aa4bc-245">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa4bc-245">Validation File</span></span>  <br/> |<span data-ttu-id="aa4bc-246">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aa4bc-246">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aa4bc-247">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa4bc-247">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa4bc-248">False</span><span class="sxs-lookup"><span data-stu-id="aa4bc-248">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa4bc-249">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa4bc-249">See also</span></span>



[<span data-ttu-id="aa4bc-250">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="aa4bc-250">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="aa4bc-251">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="aa4bc-251">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

