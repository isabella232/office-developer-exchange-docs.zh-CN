---
title: FreeBusyViewType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyViewType
api_type:
- schema
ms.assetid: 7c7f82ba-fa52-4a3e-bec7-39d373c66fc7
description: FreeBusyViewType 元素表示的响应中返回的忙/闲信息的类型。
ms.openlocfilehash: fe965d062f72d99dff7148f4d00b12fd8c4e1366
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754443"
---
# <a name="freebusyviewtype"></a><span data-ttu-id="b479d-103">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="b479d-103">FreeBusyViewType</span></span>

<span data-ttu-id="b479d-104">**FreeBusyViewType**元素表示的响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="b479d-104">The **FreeBusyViewType** element represents the type of free/busy information returned in the response.</span></span> 
  
[<span data-ttu-id="b479d-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b479d-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="b479d-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="b479d-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="b479d-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="b479d-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="b479d-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="b479d-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="b479d-109">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="b479d-109">FreeBusyViewType</span></span>](freebusyviewtype.md)
  
```xml
<FreeBusyViewType>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</FreeBusyViewType>
```

 <span data-ttu-id="b479d-110">**FreeBusyViewType**</span><span class="sxs-lookup"><span data-stu-id="b479d-110">**FreeBusyViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b479d-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b479d-111">Attributes and elements</span></span>

<span data-ttu-id="b479d-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b479d-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b479d-113">属性</span><span class="sxs-lookup"><span data-stu-id="b479d-113">Attributes</span></span>

<span data-ttu-id="b479d-114">无。</span><span class="sxs-lookup"><span data-stu-id="b479d-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b479d-115">子元素</span><span class="sxs-lookup"><span data-stu-id="b479d-115">Child elements</span></span>

<span data-ttu-id="b479d-116">无。</span><span class="sxs-lookup"><span data-stu-id="b479d-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b479d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b479d-117">Parent elements</span></span>

|<span data-ttu-id="b479d-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="b479d-118">**Element**</span></span>|<span data-ttu-id="b479d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="b479d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b479d-120">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="b479d-120">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="b479d-121">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="b479d-121">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="b479d-122">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="b479d-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b479d-123">文本值</span><span class="sxs-lookup"><span data-stu-id="b479d-123">Text value</span></span>

<span data-ttu-id="b479d-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="b479d-124">A text value is required.</span></span> <span data-ttu-id="b479d-125">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="b479d-125">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="b479d-126">**值**</span><span class="sxs-lookup"><span data-stu-id="b479d-126">**Value**</span></span>|<span data-ttu-id="b479d-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="b479d-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b479d-128">无</span><span class="sxs-lookup"><span data-stu-id="b479d-128">None</span></span>  <br/> |<span data-ttu-id="b479d-129">此值的请求无效。</span><span class="sxs-lookup"><span data-stu-id="b479d-129">This value is not valid for requests.</span></span> <span data-ttu-id="b479d-130">此值是有效的响应。</span><span class="sxs-lookup"><span data-stu-id="b479d-130">This value is valid for responses.</span></span>  <br/> |
|<span data-ttu-id="b479d-131">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="b479d-131">MergedOnly</span></span>  <br/> |<span data-ttu-id="b479d-132">表示一个聚合的忙/闲流。</span><span class="sxs-lookup"><span data-stu-id="b479d-132">Represents an aggregated free/busy stream.</span></span> <span data-ttu-id="b479d-133">在一个林中的目标用户不具有可用性服务配置跨林方案中，可用性服务请求者的忙/闲信息的公用文件夹中检索目标用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="b479d-133">In cross-forest scenarios in which the target user in one forest does not have an Availability service configured, the Availability service of the requestor retrieves the target user's free/busy information from the free/busy public folder.</span></span> <span data-ttu-id="b479d-134">公用文件夹只将忙/闲信息存储在合并的表单中，因为**MergedOnly**是唯一可用的信息。</span><span class="sxs-lookup"><span data-stu-id="b479d-134">Because public folders only store free/busy information in merged form, **MergedOnly** is the only available information.</span></span>  <br/> |
|<span data-ttu-id="b479d-135">FreeBusy</span><span class="sxs-lookup"><span data-stu-id="b479d-135">FreeBusy</span></span>  <br/> |<span data-ttu-id="b479d-136">表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF。</span><span class="sxs-lookup"><span data-stu-id="b479d-136">Represents the legacy status information: free, busy, tentative, and OOF.</span></span> <span data-ttu-id="b479d-137">这还包括约会的开始/结束的时间。</span><span class="sxs-lookup"><span data-stu-id="b479d-137">This also includes the start/end times of the appointments.</span></span> <span data-ttu-id="b479d-138">此视图是更丰富而不是一个聚合的忙/闲流提供比的旧的忙/闲查看，因为单个会议开始和结束时间。</span><span class="sxs-lookup"><span data-stu-id="b479d-138">This view is richer than the legacy free/busy view because individual meeting start and end times are provided instead of an aggregated free/busy stream.</span></span>  <br/> |
|<span data-ttu-id="b479d-139">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="b479d-139">FreeBusyMerged</span></span>  <br/> |<span data-ttu-id="b479d-140">代表中的所有属性**FreeBusy**与合并闲/忙时间信息的数据流。</span><span class="sxs-lookup"><span data-stu-id="b479d-140">Represents all the properties in **FreeBusy** with a stream of merged free/busy availability information.</span></span>  <br/> |
|<span data-ttu-id="b479d-141">Detailed</span><span class="sxs-lookup"><span data-stu-id="b479d-141">Detailed</span></span>  <br/> |<span data-ttu-id="b479d-142">表示的旧的状态信息： 闲、 忙、 暂定、 和 OOF;约会; 的开始/结束时间和主题、 位置和重要性如约会的各种属性。</span><span class="sxs-lookup"><span data-stu-id="b479d-142">Represents the legacy status information: free, busy, tentative, and OOF; the start/end times of the appointments; and various properties of the appointment such as subject, location, and importance.</span></span> <span data-ttu-id="b479d-143">此请求的视图将返回的最大量为其特权发出请求的用户的信息。</span><span class="sxs-lookup"><span data-stu-id="b479d-143">This requested view will return the maximum amount of information for which the requesting user is privileged.</span></span> <span data-ttu-id="b479d-144">如果合并忙/闲信息仅为可用，为与用户的 Microsoft Exchange Server 2003 林请求信息**MergedOnly**将返回。</span><span class="sxs-lookup"><span data-stu-id="b479d-144">If merged free/busy information only is available, as with requesting information for users in a Microsoft Exchange Server 2003 forest, **MergedOnly** will be returned.</span></span> <span data-ttu-id="b479d-145">否则，将返回**FreeBusy**或**Detailed** 。</span><span class="sxs-lookup"><span data-stu-id="b479d-145">Otherwise, **FreeBusy** or **Detailed** will be returned.</span></span>  <br/> <span data-ttu-id="b479d-146">如果通讯组列表指定**Detailed** ，则列表的成员的忙/闲信息合并，并返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="b479d-146">If **Detailed** is specified for a distribution list, the free/busy information for the members of the list is merged, and **MergedOnly** is returned.</span></span>  <br/> |
|<span data-ttu-id="b479d-147">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="b479d-147">DetailedMerged</span></span>  <br/> |<span data-ttu-id="b479d-148">代表中的所有属性**Detailed**与合并闲/忙时间信息的数据流。</span><span class="sxs-lookup"><span data-stu-id="b479d-148">Represents all the properties in **Detailed** with a stream of merged free/busy availability information.</span></span> <span data-ttu-id="b479d-149">如果只有合并忙/闲信息可用，例如，如果该邮箱存在运行 Exchange 2003 的计算机上，将返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="b479d-149">If only merged free/busy information is available, for example if the mailbox exists on a computer running Exchange 2003, **MergedOnly** will be returned.</span></span> <span data-ttu-id="b479d-150">否则，将返回**FreeBusyMerged**或**DetailedMerged** 。</span><span class="sxs-lookup"><span data-stu-id="b479d-150">Otherwise, **FreeBusyMerged** or **DetailedMerged** will be returned.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b479d-151">注解</span><span class="sxs-lookup"><span data-stu-id="b479d-151">Remarks</span></span>

<span data-ttu-id="b479d-152">如果使用[FreeBusyView](freebusyview.md)元素，此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b479d-152">This element is required if the [FreeBusyView](freebusyview.md) element is used.</span></span> <span data-ttu-id="b479d-153">[RequestedView](requestedview.md)元素中指定返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="b479d-153">The type of free/busy information returned is designated in the [RequestedView](requestedview.md) element.</span></span> <span data-ttu-id="b479d-154">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b479d-154">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="b479d-155">下表显示不同的视图类型和相应的 MAPI 属性返回的内容。</span><span class="sxs-lookup"><span data-stu-id="b479d-155">The following table shows what is returned for the different view types and the corresponding MAPI property.</span></span> <span data-ttu-id="b479d-156">每个视图类型基于以前的视图类型。</span><span class="sxs-lookup"><span data-stu-id="b479d-156">Each view type builds upon the former view type.</span></span>
  
|<span data-ttu-id="b479d-157">**FreeBusyViewType**</span><span class="sxs-lookup"><span data-stu-id="b479d-157">**FreeBusyViewType**</span></span>|<span data-ttu-id="b479d-158">**属性**</span><span class="sxs-lookup"><span data-stu-id="b479d-158">**Properties**</span></span>|<span data-ttu-id="b479d-159">**MAPI 日历属性**</span><span class="sxs-lookup"><span data-stu-id="b479d-159">**MAPI Calendar Property**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b479d-160">**MergedOnly**</span><span class="sxs-lookup"><span data-stu-id="b479d-160">**MergedOnly**</span></span> <br/> |<span data-ttu-id="b479d-161">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="b479d-161">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="b479d-162">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="b479d-162">**FreeBusy**</span></span> <br/> |<span data-ttu-id="b479d-163">古典状态</span><span class="sxs-lookup"><span data-stu-id="b479d-163">Classical status</span></span>  <br/> |<span data-ttu-id="b479d-164">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="b479d-164">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="b479d-165">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="b479d-165">**FreeBusy**</span></span> <br/> |<span data-ttu-id="b479d-166">工作时间</span><span class="sxs-lookup"><span data-stu-id="b479d-166">Working hours</span></span>  <br/> ||
|<span data-ttu-id="b479d-167">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="b479d-167">**FreeBusy**</span></span> <br/> |<span data-ttu-id="b479d-168">开始时间</span><span class="sxs-lookup"><span data-stu-id="b479d-168">Start time</span></span>  <br/> |<span data-ttu-id="b479d-169">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="b479d-169">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="b479d-170">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="b479d-170">**FreeBusy**</span></span> <br/> |<span data-ttu-id="b479d-171">结束时间</span><span class="sxs-lookup"><span data-stu-id="b479d-171">End time</span></span>  <br/> |<span data-ttu-id="b479d-172">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="b479d-172">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="b479d-173">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-173">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="b479d-174">古典状态</span><span class="sxs-lookup"><span data-stu-id="b479d-174">Classical status</span></span>  <br/> |<span data-ttu-id="b479d-175">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="b479d-175">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="b479d-176">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-176">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="b479d-177">工作时间</span><span class="sxs-lookup"><span data-stu-id="b479d-177">Working hours</span></span>  <br/> ||
|<span data-ttu-id="b479d-178">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-178">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="b479d-179">开始时间</span><span class="sxs-lookup"><span data-stu-id="b479d-179">Start time</span></span>  <br/> |<span data-ttu-id="b479d-180">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="b479d-180">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="b479d-181">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-181">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="b479d-182">结束时间</span><span class="sxs-lookup"><span data-stu-id="b479d-182">End time</span></span>  <br/> |<span data-ttu-id="b479d-183">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="b479d-183">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="b479d-184">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-184">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="b479d-185">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="b479d-185">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="b479d-186">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-186">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-187">古典状态</span><span class="sxs-lookup"><span data-stu-id="b479d-187">Classical status</span></span>  <br/> |<span data-ttu-id="b479d-188">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="b479d-188">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="b479d-189">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-189">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-190">工作时间</span><span class="sxs-lookup"><span data-stu-id="b479d-190">Working hours</span></span>  <br/> ||
|<span data-ttu-id="b479d-191">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-191">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-192">开始时间</span><span class="sxs-lookup"><span data-stu-id="b479d-192">Start time</span></span>  <br/> |<span data-ttu-id="b479d-193">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="b479d-193">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="b479d-194">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-194">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-195">结束时间</span><span class="sxs-lookup"><span data-stu-id="b479d-195">End time</span></span>  <br/> |<span data-ttu-id="b479d-196">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="b479d-196">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="b479d-197">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-197">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-198">主题</span><span class="sxs-lookup"><span data-stu-id="b479d-198">Subject</span></span>  <br/> |<span data-ttu-id="b479d-199">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="b479d-199">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="b479d-200">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-200">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-201">位置</span><span class="sxs-lookup"><span data-stu-id="b479d-201">Location</span></span>  <br/> |<span data-ttu-id="b479d-202">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="b479d-202">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="b479d-203">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-203">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-204">条目 Id(unless private)</span><span class="sxs-lookup"><span data-stu-id="b479d-204">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="b479d-205">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-205">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-206">私有标志</span><span class="sxs-lookup"><span data-stu-id="b479d-206">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="b479d-207">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-207">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-208">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="b479d-208">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="b479d-209">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-209">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-210">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="b479d-210">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="b479d-211">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-211">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-212">IsException</span><span class="sxs-lookup"><span data-stu-id="b479d-212">IsException</span></span>  <br/> ||
|<span data-ttu-id="b479d-213">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-213">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-214">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="b479d-214">IsReminderSet</span></span>  <br/> ||
|<span data-ttu-id="b479d-215">**详细**</span><span class="sxs-lookup"><span data-stu-id="b479d-215">**Detailed**</span></span> <br/> |<span data-ttu-id="b479d-216">利用 Office 邮件 （如果请求）</span><span class="sxs-lookup"><span data-stu-id="b479d-216">Out of Office Message (if requested)</span></span>  <br/> ||
|<span data-ttu-id="b479d-217">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-217">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-218">古典状态</span><span class="sxs-lookup"><span data-stu-id="b479d-218">Classical status</span></span>  <br/> |<span data-ttu-id="b479d-219">属性标记 (0x80860003)</span><span class="sxs-lookup"><span data-stu-id="b479d-219">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="b479d-220">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-220">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-221">工作时间</span><span class="sxs-lookup"><span data-stu-id="b479d-221">Working hours</span></span>  <br/> ||
|<span data-ttu-id="b479d-222">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-222">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-223">开始时间</span><span class="sxs-lookup"><span data-stu-id="b479d-223">Start time</span></span>  <br/> |<span data-ttu-id="b479d-224">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="b479d-224">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="b479d-225">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-225">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-226">结束时间</span><span class="sxs-lookup"><span data-stu-id="b479d-226">End time</span></span>  <br/> |<span data-ttu-id="b479d-227">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="b479d-227">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="b479d-228">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-228">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-229">主题</span><span class="sxs-lookup"><span data-stu-id="b479d-229">Subject</span></span>  <br/> |<span data-ttu-id="b479d-230">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="b479d-230">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="b479d-231">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-231">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-232">位置</span><span class="sxs-lookup"><span data-stu-id="b479d-232">Location</span></span>  <br/> |<span data-ttu-id="b479d-233">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="b479d-233">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="b479d-234">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-234">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-235">条目 Id(unless private)</span><span class="sxs-lookup"><span data-stu-id="b479d-235">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="b479d-236">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-236">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-237">私有标志</span><span class="sxs-lookup"><span data-stu-id="b479d-237">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="b479d-238">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-238">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-239">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="b479d-239">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="b479d-240">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-240">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-241">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="b479d-241">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="b479d-242">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-242">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-243">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="b479d-243">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="b479d-244">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-244">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-245">IsException</span><span class="sxs-lookup"><span data-stu-id="b479d-245">IsException</span></span>  <br/> ||
|<span data-ttu-id="b479d-246">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="b479d-246">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="b479d-247">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="b479d-247">IsReminderSet</span></span>  <br/> ||
   
## <a name="element-information"></a><span data-ttu-id="b479d-248">元素信息</span><span class="sxs-lookup"><span data-stu-id="b479d-248">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b479d-249">命名空间</span><span class="sxs-lookup"><span data-stu-id="b479d-249">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b479d-250">架构名称</span><span class="sxs-lookup"><span data-stu-id="b479d-250">Schema Name</span></span>  <br/> |<span data-ttu-id="b479d-251">类型架构</span><span class="sxs-lookup"><span data-stu-id="b479d-251">Types schema</span></span>  <br/> |
|<span data-ttu-id="b479d-252">验证文件</span><span class="sxs-lookup"><span data-stu-id="b479d-252">Validation File</span></span>  <br/> |<span data-ttu-id="b479d-253">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b479d-253">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b479d-254">可以为空</span><span class="sxs-lookup"><span data-stu-id="b479d-254">Can be Empty</span></span>  <br/> |<span data-ttu-id="b479d-255">False</span><span class="sxs-lookup"><span data-stu-id="b479d-255">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b479d-256">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b479d-256">See also</span></span>



[<span data-ttu-id="b479d-257">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="b479d-257">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="b479d-258">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b479d-258">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="b479d-259">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="b479d-259">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

