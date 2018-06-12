---
title: SuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionQuality
api_type:
- schema
ms.assetid: 734f1a58-adda-4830-973e-e84bf7b870d5
description: SuggestionQuality 元素均表示建议的会议时间的质量。
ms.openlocfilehash: e67e0149226b36c22cdd00acd78f6582f826dd3e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838160"
---
# <a name="suggestionquality"></a><span data-ttu-id="a64e0-103">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="a64e0-103">SuggestionQuality</span></span>

<span data-ttu-id="a64e0-104">**SuggestionQuality**元素均表示建议的会议时间的质量。</span><span class="sxs-lookup"><span data-stu-id="a64e0-104">The **SuggestionQuality** element represents the quality of the suggested meeting time.</span></span> 
  
[<span data-ttu-id="a64e0-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a64e0-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="a64e0-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="a64e0-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="a64e0-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="a64e0-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="a64e0-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="a64e0-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="a64e0-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="a64e0-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="a64e0-110">建议</span><span class="sxs-lookup"><span data-stu-id="a64e0-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="a64e0-111">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="a64e0-111">SuggestionQuality</span></span>](suggestionquality.md)
  
```xml
<SuggestionQuality>Excellent or Good or Fair or Poor</SuggestionQuality>
```

 <span data-ttu-id="a64e0-112">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="a64e0-112">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a64e0-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a64e0-113">Attributes and elements</span></span>

<span data-ttu-id="a64e0-114">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a64e0-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a64e0-115">属性</span><span class="sxs-lookup"><span data-stu-id="a64e0-115">Attributes</span></span>

<span data-ttu-id="a64e0-116">无。</span><span class="sxs-lookup"><span data-stu-id="a64e0-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a64e0-117">子元素</span><span class="sxs-lookup"><span data-stu-id="a64e0-117">Child elements</span></span>

<span data-ttu-id="a64e0-118">无。</span><span class="sxs-lookup"><span data-stu-id="a64e0-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a64e0-119">父元素</span><span class="sxs-lookup"><span data-stu-id="a64e0-119">Parent elements</span></span>

|<span data-ttu-id="a64e0-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="a64e0-120">**Element**</span></span>|<span data-ttu-id="a64e0-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="a64e0-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a64e0-122">建议</span><span class="sxs-lookup"><span data-stu-id="a64e0-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="a64e0-123">代表单个会议时间建议。</span><span class="sxs-lookup"><span data-stu-id="a64e0-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="a64e0-124">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a64e0-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a64e0-125">文本值</span><span class="sxs-lookup"><span data-stu-id="a64e0-125">Text value</span></span>

<span data-ttu-id="a64e0-126">所需的文本值，该值代表**SuggestionQuality**值。</span><span class="sxs-lookup"><span data-stu-id="a64e0-126">A text value that represents a **SuggestionQuality** value is required.</span></span> <span data-ttu-id="a64e0-127">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="a64e0-127">The following are the possible values:</span></span> 
  
- <span data-ttu-id="a64e0-128">**极好**100%的用户和资源的建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="a64e0-128">**Excellent** 100 percent of users and resources are available for the suggested meeting time.</span></span> 
    
- <span data-ttu-id="a64e0-129">**良好**用户和资源可用的最小百分比是等于或大于[GoodThreshold](goodthreshold.md)元素的值以及 50。</span><span class="sxs-lookup"><span data-stu-id="a64e0-129">**Good** The minimum percentage of users and resources available is equal to or greater than the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> 
    
- <span data-ttu-id="a64e0-130">**公平**用户和资源可用于建议的会议时间的最大百分比等于[GoodThreshold](goodthreshold.md)元素的值以及 50。</span><span class="sxs-lookup"><span data-stu-id="a64e0-130">**Fair** The maximum percentage of users and resources available for a suggested meeting time is equal to the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> <span data-ttu-id="a64e0-131">**公平**的质量的会议时间的最小值为 50%。</span><span class="sxs-lookup"><span data-stu-id="a64e0-131">The minimum value for a **Fair** quality meeting time is 50 percent.</span></span> 
    
- <span data-ttu-id="a64e0-132">**不佳**小于 50%的用户和资源的建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="a64e0-132">**Poor** Less than 50 percent of the users and resources are available for the suggested meeting time.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a64e0-133">备注</span><span class="sxs-lookup"><span data-stu-id="a64e0-133">Remarks</span></span>

<span data-ttu-id="a64e0-134">**SuggestionQuality**类型也是[DayQuality](dayquality.md)和[MinimumSuggestionQuality](minimumsuggestionquality.md)元素的类型。</span><span class="sxs-lookup"><span data-stu-id="a64e0-134">The **SuggestionQuality** type is also the type for the [DayQuality](dayquality.md) and the [MinimumSuggestionQuality](minimumsuggestionquality.md) elements.</span></span> 
  
<span data-ttu-id="a64e0-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a64e0-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a64e0-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="a64e0-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a64e0-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="a64e0-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a64e0-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="a64e0-138">Schema Name</span></span>  <br/> |<span data-ttu-id="a64e0-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="a64e0-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="a64e0-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="a64e0-140">Validation File</span></span>  <br/> |<span data-ttu-id="a64e0-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a64e0-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a64e0-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="a64e0-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="a64e0-143">False</span><span class="sxs-lookup"><span data-stu-id="a64e0-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a64e0-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a64e0-144">See also</span></span>



[<span data-ttu-id="a64e0-145">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="a64e0-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="a64e0-146">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a64e0-146">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="a64e0-147">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="a64e0-147">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

