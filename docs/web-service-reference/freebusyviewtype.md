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
description: FreeBusyViewType 元素表示响应中返回的忙/闲信息的类型。
ms.openlocfilehash: 3556ad236693ac9aa018b8aa3af7843765da6aa4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459565"
---
# <a name="freebusyviewtype"></a><span data-ttu-id="41ae2-103">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="41ae2-103">FreeBusyViewType</span></span>

<span data-ttu-id="41ae2-104">**FreeBusyViewType**元素表示响应中返回的忙/闲信息的类型。</span><span class="sxs-lookup"><span data-stu-id="41ae2-104">The **FreeBusyViewType** element represents the type of free/busy information returned in the response.</span></span> 
  
[<span data-ttu-id="41ae2-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="41ae2-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="41ae2-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="41ae2-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="41ae2-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="41ae2-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="41ae2-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="41ae2-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="41ae2-109">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="41ae2-109">FreeBusyViewType</span></span>](freebusyviewtype.md)
  
```xml
<FreeBusyViewType>None or MergedOnly or FreeBusy or FreeBusyMerged or Detailed or DetailedMerged</FreeBusyViewType>
```

 <span data-ttu-id="41ae2-110">**FreeBusyViewType**</span><span class="sxs-lookup"><span data-stu-id="41ae2-110">**FreeBusyViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41ae2-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41ae2-111">Attributes and elements</span></span>

<span data-ttu-id="41ae2-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41ae2-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41ae2-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="41ae2-113">Attributes</span></span>

<span data-ttu-id="41ae2-114">无。</span><span class="sxs-lookup"><span data-stu-id="41ae2-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41ae2-115">子元素</span><span class="sxs-lookup"><span data-stu-id="41ae2-115">Child elements</span></span>

<span data-ttu-id="41ae2-116">无。</span><span class="sxs-lookup"><span data-stu-id="41ae2-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41ae2-117">父元素</span><span class="sxs-lookup"><span data-stu-id="41ae2-117">Parent elements</span></span>

|<span data-ttu-id="41ae2-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="41ae2-118">**Element**</span></span>|<span data-ttu-id="41ae2-119">**描述**</span><span class="sxs-lookup"><span data-stu-id="41ae2-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41ae2-120">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="41ae2-120">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="41ae2-121">包含特定用户的可用性信息。</span><span class="sxs-lookup"><span data-stu-id="41ae2-121">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="41ae2-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="41ae2-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41ae2-123">文本值</span><span class="sxs-lookup"><span data-stu-id="41ae2-123">Text value</span></span>

<span data-ttu-id="41ae2-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="41ae2-124">A text value is required.</span></span> <span data-ttu-id="41ae2-125">下表列出了此元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="41ae2-125">The following table lists the possible values for this element.</span></span>
  
|<span data-ttu-id="41ae2-126">**值**</span><span class="sxs-lookup"><span data-stu-id="41ae2-126">**Value**</span></span>|<span data-ttu-id="41ae2-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="41ae2-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="41ae2-128">无</span><span class="sxs-lookup"><span data-stu-id="41ae2-128">None</span></span>  <br/> |<span data-ttu-id="41ae2-129">对于请求，此值无效。</span><span class="sxs-lookup"><span data-stu-id="41ae2-129">This value is not valid for requests.</span></span> <span data-ttu-id="41ae2-130">此值对响应有效。</span><span class="sxs-lookup"><span data-stu-id="41ae2-130">This value is valid for responses.</span></span>  <br/> |
|<span data-ttu-id="41ae2-131">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="41ae2-131">MergedOnly</span></span>  <br/> |<span data-ttu-id="41ae2-132">表示聚合的忙/闲流。</span><span class="sxs-lookup"><span data-stu-id="41ae2-132">Represents an aggregated free/busy stream.</span></span> <span data-ttu-id="41ae2-133">在跨林方案中，在一个林中的目标用户未配置可用性服务的情况下，请求者的可用性服务将从忙/闲公用文件夹中检索目标用户的忙/闲信息。</span><span class="sxs-lookup"><span data-stu-id="41ae2-133">In cross-forest scenarios in which the target user in one forest does not have an Availability service configured, the Availability service of the requestor retrieves the target user's free/busy information from the free/busy public folder.</span></span> <span data-ttu-id="41ae2-134">由于公用文件夹仅将忙/闲信息存储在合并表单中，因此**MergedOnly**是唯一可用的信息。</span><span class="sxs-lookup"><span data-stu-id="41ae2-134">Because public folders only store free/busy information in merged form, **MergedOnly** is the only available information.</span></span>  <br/> |
|<span data-ttu-id="41ae2-135">FreeBusy</span><span class="sxs-lookup"><span data-stu-id="41ae2-135">FreeBusy</span></span>  <br/> |<span data-ttu-id="41ae2-136">代表旧状态信息：闲、忙、暂定和 OOF。</span><span class="sxs-lookup"><span data-stu-id="41ae2-136">Represents the legacy status information: free, busy, tentative, and OOF.</span></span> <span data-ttu-id="41ae2-137">这还包括约会的开始/结束时间。</span><span class="sxs-lookup"><span data-stu-id="41ae2-137">This also includes the start/end times of the appointments.</span></span> <span data-ttu-id="41ae2-138">此视图比旧版的忙/闲视图更丰富，因为提供了单个会议开始和结束时间，而不是聚合的忙/闲流。</span><span class="sxs-lookup"><span data-stu-id="41ae2-138">This view is richer than the legacy free/busy view because individual meeting start and end times are provided instead of an aggregated free/busy stream.</span></span>  <br/> |
|<span data-ttu-id="41ae2-139">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="41ae2-139">FreeBusyMerged</span></span>  <br/> |<span data-ttu-id="41ae2-140">表示包含合并的忙/闲可用性信息流的**FreeBusy**中的所有属性。</span><span class="sxs-lookup"><span data-stu-id="41ae2-140">Represents all the properties in **FreeBusy** with a stream of merged free/busy availability information.</span></span>  <br/> |
|<span data-ttu-id="41ae2-141">具体</span><span class="sxs-lookup"><span data-stu-id="41ae2-141">Detailed</span></span>  <br/> |<span data-ttu-id="41ae2-142">代表旧状态信息：闲、忙、暂定和 OOF;约会的开始/结束时间;以及约会的各种属性，如主题、位置和重要性。</span><span class="sxs-lookup"><span data-stu-id="41ae2-142">Represents the legacy status information: free, busy, tentative, and OOF; the start/end times of the appointments; and various properties of the appointment such as subject, location, and importance.</span></span> <span data-ttu-id="41ae2-143">此请求的视图将返回请求用户有权限的最大信息量。</span><span class="sxs-lookup"><span data-stu-id="41ae2-143">This requested view will return the maximum amount of information for which the requesting user is privileged.</span></span> <span data-ttu-id="41ae2-144">如果只提供了合并的忙/闲信息，就像 Microsoft Exchange Server 2003 林中的用户请求信息一样，将返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="41ae2-144">If merged free/busy information only is available, as with requesting information for users in a Microsoft Exchange Server 2003 forest, **MergedOnly** will be returned.</span></span> <span data-ttu-id="41ae2-145">否则，将返回**FreeBusy**或**详细信息**。</span><span class="sxs-lookup"><span data-stu-id="41ae2-145">Otherwise, **FreeBusy** or **Detailed** will be returned.</span></span>  <br/> <span data-ttu-id="41ae2-146">如果为通讯组列表指定了**详细**信息，则会合并列表成员的忙/闲信息，并返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="41ae2-146">If **Detailed** is specified for a distribution list, the free/busy information for the members of the list is merged, and **MergedOnly** is returned.</span></span>  <br/> |
|<span data-ttu-id="41ae2-147">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="41ae2-147">DetailedMerged</span></span>  <br/> |<span data-ttu-id="41ae2-148">表示与合并的忙/闲可用性信息流**有关的所有**属性。</span><span class="sxs-lookup"><span data-stu-id="41ae2-148">Represents all the properties in **Detailed** with a stream of merged free/busy availability information.</span></span> <span data-ttu-id="41ae2-149">如果仅有合并的忙/闲信息，例如，如果该邮箱存在于运行 Exchange 2003 的计算机上，则将返回**MergedOnly** 。</span><span class="sxs-lookup"><span data-stu-id="41ae2-149">If only merged free/busy information is available, for example if the mailbox exists on a computer running Exchange 2003, **MergedOnly** will be returned.</span></span> <span data-ttu-id="41ae2-150">否则，将返回**FreeBusyMerged**或**DetailedMerged** 。</span><span class="sxs-lookup"><span data-stu-id="41ae2-150">Otherwise, **FreeBusyMerged** or **DetailedMerged** will be returned.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41ae2-151">备注</span><span class="sxs-lookup"><span data-stu-id="41ae2-151">Remarks</span></span>

<span data-ttu-id="41ae2-152">如果使用[FreeBusyView](freebusyview.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="41ae2-152">This element is required if the [FreeBusyView](freebusyview.md) element is used.</span></span> <span data-ttu-id="41ae2-153">返回的忙/闲信息的类型在[RequestedView](requestedview.md)元素中指定。</span><span class="sxs-lookup"><span data-stu-id="41ae2-153">The type of free/busy information returned is designated in the [RequestedView](requestedview.md) element.</span></span> <span data-ttu-id="41ae2-154">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="41ae2-154">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="41ae2-155">下表显示了为不同的视图类型和相应的 MAPI 属性返回的内容。</span><span class="sxs-lookup"><span data-stu-id="41ae2-155">The following table shows what is returned for the different view types and the corresponding MAPI property.</span></span> <span data-ttu-id="41ae2-156">每个视图类型都基于以前的视图类型。</span><span class="sxs-lookup"><span data-stu-id="41ae2-156">Each view type builds upon the former view type.</span></span>
  
|<span data-ttu-id="41ae2-157">**FreeBusyViewType**</span><span class="sxs-lookup"><span data-stu-id="41ae2-157">**FreeBusyViewType**</span></span>|<span data-ttu-id="41ae2-158">**属性**</span><span class="sxs-lookup"><span data-stu-id="41ae2-158">**Properties**</span></span>|<span data-ttu-id="41ae2-159">**MAPI 日历属性**</span><span class="sxs-lookup"><span data-stu-id="41ae2-159">**MAPI Calendar Property**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41ae2-160">**MergedOnly**</span><span class="sxs-lookup"><span data-stu-id="41ae2-160">**MergedOnly**</span></span> <br/> |<span data-ttu-id="41ae2-161">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="41ae2-161">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="41ae2-162">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="41ae2-162">**FreeBusy**</span></span> <br/> |<span data-ttu-id="41ae2-163">古典状态</span><span class="sxs-lookup"><span data-stu-id="41ae2-163">Classical status</span></span>  <br/> |<span data-ttu-id="41ae2-164">属性标记（0x80860003）</span><span class="sxs-lookup"><span data-stu-id="41ae2-164">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="41ae2-165">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="41ae2-165">**FreeBusy**</span></span> <br/> |<span data-ttu-id="41ae2-166">工作时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-166">Working hours</span></span>  <br/> ||
|<span data-ttu-id="41ae2-167">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="41ae2-167">**FreeBusy**</span></span> <br/> |<span data-ttu-id="41ae2-168">开始时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-168">Start time</span></span>  <br/> |<span data-ttu-id="41ae2-169">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="41ae2-169">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="41ae2-170">**FreeBusy**</span><span class="sxs-lookup"><span data-stu-id="41ae2-170">**FreeBusy**</span></span> <br/> |<span data-ttu-id="41ae2-171">结束时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-171">End time</span></span>  <br/> |<span data-ttu-id="41ae2-172">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="41ae2-172">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="41ae2-173">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-173">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="41ae2-174">古典状态</span><span class="sxs-lookup"><span data-stu-id="41ae2-174">Classical status</span></span>  <br/> |<span data-ttu-id="41ae2-175">属性标记（0x80860003）</span><span class="sxs-lookup"><span data-stu-id="41ae2-175">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="41ae2-176">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-176">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="41ae2-177">工作时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-177">Working hours</span></span>  <br/> ||
|<span data-ttu-id="41ae2-178">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-178">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="41ae2-179">开始时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-179">Start time</span></span>  <br/> |<span data-ttu-id="41ae2-180">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="41ae2-180">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="41ae2-181">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-181">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="41ae2-182">结束时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-182">End time</span></span>  <br/> |<span data-ttu-id="41ae2-183">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="41ae2-183">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="41ae2-184">**FreeBusyMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-184">**FreeBusyMerged**</span></span> <br/> |<span data-ttu-id="41ae2-185">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="41ae2-185">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="41ae2-186">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-186">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-187">古典状态</span><span class="sxs-lookup"><span data-stu-id="41ae2-187">Classical status</span></span>  <br/> |<span data-ttu-id="41ae2-188">属性标记（0x80860003）</span><span class="sxs-lookup"><span data-stu-id="41ae2-188">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="41ae2-189">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-189">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-190">工作时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-190">Working hours</span></span>  <br/> ||
|<span data-ttu-id="41ae2-191">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-191">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-192">开始时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-192">Start time</span></span>  <br/> |<span data-ttu-id="41ae2-193">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="41ae2-193">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="41ae2-194">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-194">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-195">结束时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-195">End time</span></span>  <br/> |<span data-ttu-id="41ae2-196">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="41ae2-196">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="41ae2-197">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-197">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-198">Subject</span><span class="sxs-lookup"><span data-stu-id="41ae2-198">Subject</span></span>  <br/> |<span data-ttu-id="41ae2-199">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="41ae2-199">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="41ae2-200">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-200">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-201">位置</span><span class="sxs-lookup"><span data-stu-id="41ae2-201">Location</span></span>  <br/> |<span data-ttu-id="41ae2-202">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="41ae2-202">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="41ae2-203">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-203">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-204">条目 Id （除非是私有）</span><span class="sxs-lookup"><span data-stu-id="41ae2-204">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="41ae2-205">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-205">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-206">私有标志</span><span class="sxs-lookup"><span data-stu-id="41ae2-206">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="41ae2-207">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-207">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-208">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="41ae2-208">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="41ae2-209">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-209">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-210">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="41ae2-210">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="41ae2-211">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-211">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-212">IsException</span><span class="sxs-lookup"><span data-stu-id="41ae2-212">IsException</span></span>  <br/> ||
|<span data-ttu-id="41ae2-213">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-213">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-214">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="41ae2-214">IsReminderSet</span></span>  <br/> ||
|<span data-ttu-id="41ae2-215">**具体**</span><span class="sxs-lookup"><span data-stu-id="41ae2-215">**Detailed**</span></span> <br/> |<span data-ttu-id="41ae2-216">外出邮件（如果需要）</span><span class="sxs-lookup"><span data-stu-id="41ae2-216">Out of Office Message (if requested)</span></span>  <br/> ||
|<span data-ttu-id="41ae2-217">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-217">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-218">古典状态</span><span class="sxs-lookup"><span data-stu-id="41ae2-218">Classical status</span></span>  <br/> |<span data-ttu-id="41ae2-219">属性标记（0x80860003）</span><span class="sxs-lookup"><span data-stu-id="41ae2-219">PropTag (0x80860003)</span></span>  <br/> |
|<span data-ttu-id="41ae2-220">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-220">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-221">工作时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-221">Working hours</span></span>  <br/> ||
|<span data-ttu-id="41ae2-222">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-222">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-223">开始时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-223">Start time</span></span>  <br/> |<span data-ttu-id="41ae2-224">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="41ae2-224">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="41ae2-225">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-225">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-226">结束时间</span><span class="sxs-lookup"><span data-stu-id="41ae2-226">End time</span></span>  <br/> |<span data-ttu-id="41ae2-227">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="41ae2-227">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="41ae2-228">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-228">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-229">Subject</span><span class="sxs-lookup"><span data-stu-id="41ae2-229">Subject</span></span>  <br/> |<span data-ttu-id="41ae2-230">PR_SUBJECT</span><span class="sxs-lookup"><span data-stu-id="41ae2-230">PR_SUBJECT</span></span>  <br/> |
|<span data-ttu-id="41ae2-231">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-231">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-232">位置</span><span class="sxs-lookup"><span data-stu-id="41ae2-232">Location</span></span>  <br/> |<span data-ttu-id="41ae2-233">PR_LOCATION</span><span class="sxs-lookup"><span data-stu-id="41ae2-233">PR_LOCATION</span></span>  <br/> |
|<span data-ttu-id="41ae2-234">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-234">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-235">条目 Id （除非是私有）</span><span class="sxs-lookup"><span data-stu-id="41ae2-235">Entry-Id(unless private)</span></span>  <br/> ||
|<span data-ttu-id="41ae2-236">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-236">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-237">私有标志</span><span class="sxs-lookup"><span data-stu-id="41ae2-237">Private Flag</span></span>  <br/> ||
|<span data-ttu-id="41ae2-238">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-238">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-239">MergedFreeBusyStream</span><span class="sxs-lookup"><span data-stu-id="41ae2-239">MergedFreeBusyStream</span></span>  <br/> ||
|<span data-ttu-id="41ae2-240">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-240">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-241">IsMeeting</span><span class="sxs-lookup"><span data-stu-id="41ae2-241">IsMeeting</span></span>  <br/> ||
|<span data-ttu-id="41ae2-242">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-242">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-243">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="41ae2-243">IsRecurring</span></span>  <br/> ||
|<span data-ttu-id="41ae2-244">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-244">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-245">IsException</span><span class="sxs-lookup"><span data-stu-id="41ae2-245">IsException</span></span>  <br/> ||
|<span data-ttu-id="41ae2-246">**DetailedMerged**</span><span class="sxs-lookup"><span data-stu-id="41ae2-246">**DetailedMerged**</span></span> <br/> |<span data-ttu-id="41ae2-247">IsReminderSet</span><span class="sxs-lookup"><span data-stu-id="41ae2-247">IsReminderSet</span></span>  <br/> ||
   
## <a name="element-information"></a><span data-ttu-id="41ae2-248">元素信息</span><span class="sxs-lookup"><span data-stu-id="41ae2-248">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41ae2-249">命名空间</span><span class="sxs-lookup"><span data-stu-id="41ae2-249">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="41ae2-250">架构名称</span><span class="sxs-lookup"><span data-stu-id="41ae2-250">Schema Name</span></span>  <br/> |<span data-ttu-id="41ae2-251">类型架构</span><span class="sxs-lookup"><span data-stu-id="41ae2-251">Types schema</span></span>  <br/> |
|<span data-ttu-id="41ae2-252">验证文件</span><span class="sxs-lookup"><span data-stu-id="41ae2-252">Validation File</span></span>  <br/> |<span data-ttu-id="41ae2-253">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="41ae2-253">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="41ae2-254">可以为空</span><span class="sxs-lookup"><span data-stu-id="41ae2-254">Can be Empty</span></span>  <br/> |<span data-ttu-id="41ae2-255">False</span><span class="sxs-lookup"><span data-stu-id="41ae2-255">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41ae2-256">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41ae2-256">See also</span></span>



[<span data-ttu-id="41ae2-257">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="41ae2-257">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="41ae2-258">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="41ae2-258">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="41ae2-259">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="41ae2-259">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

