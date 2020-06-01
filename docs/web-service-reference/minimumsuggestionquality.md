---
title: MinimumSuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MinimumSuggestionQuality
api_type:
- schema
ms.assetid: 3725cbd4-9bc1-4f7d-8929-b2c68cb46114
description: MinimumSuggestionQuality 元素定义要在响应中返回的会议建议的质量。
ms.openlocfilehash: c85cbf65a63ac0b09408c14e01889f97a05b27b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467478"
---
# <a name="minimumsuggestionquality"></a><span data-ttu-id="bd179-103">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="bd179-103">MinimumSuggestionQuality</span></span>

<span data-ttu-id="bd179-104">**MinimumSuggestionQuality**元素定义要在响应中返回的会议建议的质量。</span><span class="sxs-lookup"><span data-stu-id="bd179-104">The **MinimumSuggestionQuality** element defines the quality of meeting suggestions to be returned in the response.</span></span> 
  
[<span data-ttu-id="bd179-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="bd179-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="bd179-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="bd179-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="bd179-107">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="bd179-107">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md)
  
```xml
<MinimumSuggestionQuality>...</MinimumSuggestionQuality>
```

 <span data-ttu-id="bd179-108">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="bd179-108">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd179-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bd179-109">Attributes and elements</span></span>

<span data-ttu-id="bd179-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bd179-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd179-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="bd179-111">Attributes</span></span>

<span data-ttu-id="bd179-112">无。</span><span class="sxs-lookup"><span data-stu-id="bd179-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd179-113">子元素</span><span class="sxs-lookup"><span data-stu-id="bd179-113">Child elements</span></span>

<span data-ttu-id="bd179-114">无。</span><span class="sxs-lookup"><span data-stu-id="bd179-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bd179-115">父元素</span><span class="sxs-lookup"><span data-stu-id="bd179-115">Parent elements</span></span>

|<span data-ttu-id="bd179-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="bd179-116">**Element**</span></span>|<span data-ttu-id="bd179-117">**描述**</span><span class="sxs-lookup"><span data-stu-id="bd179-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd179-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="bd179-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="bd179-119">包含用于获取会议建议信息的选项。</span><span class="sxs-lookup"><span data-stu-id="bd179-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="bd179-120">以下是此元素的 XPath：</span><span class="sxs-lookup"><span data-stu-id="bd179-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bd179-121">文本值</span><span class="sxs-lookup"><span data-stu-id="bd179-121">Text value</span></span>

<span data-ttu-id="bd179-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="bd179-122">A text value is required.</span></span> <span data-ttu-id="bd179-123">下表列出了此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="bd179-123">The following table lists the possible values for this element:</span></span>
  
|<span data-ttu-id="bd179-124">**值**</span><span class="sxs-lookup"><span data-stu-id="bd179-124">**Value**</span></span>|<span data-ttu-id="bd179-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="bd179-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd179-126">**极好**</span><span class="sxs-lookup"><span data-stu-id="bd179-126">**Excellent**</span></span> <br/> |<span data-ttu-id="bd179-127">0% 的与会者有与建议会议时间的冲突。</span><span class="sxs-lookup"><span data-stu-id="bd179-127">0% of the attendees have a conflict with the suggested meeting time.</span></span>  <br/> |
|<span data-ttu-id="bd179-128">**Good**</span><span class="sxs-lookup"><span data-stu-id="bd179-128">**Good**</span></span> <br/> |<span data-ttu-id="bd179-129">被视为 "正常" 的百分比通过使用[GoodThreshold](goodthreshold.md)元素进行设置。</span><span class="sxs-lookup"><span data-stu-id="bd179-129">The percentage that is considered good is set by using the [GoodThreshold](goodthreshold.md) element.</span></span>  <br/> |
|<span data-ttu-id="bd179-130">**大量**</span><span class="sxs-lookup"><span data-stu-id="bd179-130">**Fair**</span></span> <br/> |<span data-ttu-id="bd179-131">被视为公平的百分比是通过使用[GoodThreshold](goodthreshold.md)元素设置的。</span><span class="sxs-lookup"><span data-stu-id="bd179-131">The percentage that is considered fair is set by using the [GoodThreshold](goodthreshold.md) element.</span></span>  <br/> |
|<span data-ttu-id="bd179-132">**较差**</span><span class="sxs-lookup"><span data-stu-id="bd179-132">**Poor**</span></span> <br/> |<span data-ttu-id="bd179-133">50% 或更多与会者与建议的会议时间有冲突。</span><span class="sxs-lookup"><span data-stu-id="bd179-133">50% or more of the attendees have a conflict with the suggested meeting time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd179-134">备注</span><span class="sxs-lookup"><span data-stu-id="bd179-134">Remarks</span></span>

<span data-ttu-id="bd179-135">如果使用[SuggestionsViewOptions](suggestionsviewoptions.md)元素，则此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="bd179-135">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bd179-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bd179-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="bd179-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="bd179-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd179-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="bd179-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bd179-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="bd179-139">Schema Name</span></span>  <br/> |<span data-ttu-id="bd179-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="bd179-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="bd179-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="bd179-141">Validation File</span></span>  <br/> |<span data-ttu-id="bd179-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bd179-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bd179-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="bd179-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="bd179-144">False</span><span class="sxs-lookup"><span data-stu-id="bd179-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd179-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bd179-145">See also</span></span>



[<span data-ttu-id="bd179-146">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="bd179-146">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="bd179-147">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="bd179-147">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

