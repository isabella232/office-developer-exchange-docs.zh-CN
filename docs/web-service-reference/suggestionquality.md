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
description: SuggestionQuality 元素表示建议的会议时间的质量。
ms.openlocfilehash: 3f8c15ccabd03687dc386a0328020cbc0bc802c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457975"
---
# <a name="suggestionquality"></a><span data-ttu-id="ccaa5-103">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="ccaa5-103">SuggestionQuality</span></span>

<span data-ttu-id="ccaa5-104">**SuggestionQuality**元素表示建议的会议时间的质量。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-104">The **SuggestionQuality** element represents the quality of the suggested meeting time.</span></span> 
  
[<span data-ttu-id="ccaa5-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ccaa5-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ccaa5-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="ccaa5-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="ccaa5-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="ccaa5-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="ccaa5-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="ccaa5-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="ccaa5-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="ccaa5-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="ccaa5-110">建议</span><span class="sxs-lookup"><span data-stu-id="ccaa5-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="ccaa5-111">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="ccaa5-111">SuggestionQuality</span></span>](suggestionquality.md)
  
```xml
<SuggestionQuality>Excellent or Good or Fair or Poor</SuggestionQuality>
```

 <span data-ttu-id="ccaa5-112">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="ccaa5-112">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccaa5-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ccaa5-113">Attributes and elements</span></span>

<span data-ttu-id="ccaa5-114">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccaa5-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="ccaa5-115">Attributes</span></span>

<span data-ttu-id="ccaa5-116">无。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ccaa5-117">子元素</span><span class="sxs-lookup"><span data-stu-id="ccaa5-117">Child elements</span></span>

<span data-ttu-id="ccaa5-118">无。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ccaa5-119">父元素</span><span class="sxs-lookup"><span data-stu-id="ccaa5-119">Parent elements</span></span>

|<span data-ttu-id="ccaa5-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="ccaa5-120">**Element**</span></span>|<span data-ttu-id="ccaa5-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="ccaa5-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccaa5-122">建议</span><span class="sxs-lookup"><span data-stu-id="ccaa5-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="ccaa5-123">表示单个会议时间建议。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="ccaa5-124">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="ccaa5-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ccaa5-125">文本值</span><span class="sxs-lookup"><span data-stu-id="ccaa5-125">Text value</span></span>

<span data-ttu-id="ccaa5-126">一个代表**SuggestionQuality**值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-126">A text value that represents a **SuggestionQuality** value is required.</span></span> <span data-ttu-id="ccaa5-127">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="ccaa5-127">The following are the possible values:</span></span> 
  
- <span data-ttu-id="ccaa5-128">**理想**的100% 的用户和资源可用于建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-128">**Excellent** 100 percent of users and resources are available for the suggested meeting time.</span></span> 
    
- <span data-ttu-id="ccaa5-129">**正常**可用的用户和资源的最小百分比等于或大于[GoodThreshold](goodthreshold.md)元素的值加上50。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-129">**Good** The minimum percentage of users and resources available is equal to or greater than the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> 
    
- <span data-ttu-id="ccaa5-130">**公平**可用于建议会议时间的用户和资源的最大百分比等于[GoodThreshold](goodthreshold.md)元素值加上50。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-130">**Fair** The maximum percentage of users and resources available for a suggested meeting time is equal to the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> <span data-ttu-id="ccaa5-131">**合理**质量会议时间的最小值为50%。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-131">The minimum value for a **Fair** quality meeting time is 50 percent.</span></span> 
    
- <span data-ttu-id="ccaa5-132">**较差**少于50% 的用户和资源可用于建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-132">**Poor** Less than 50 percent of the users and resources are available for the suggested meeting time.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ccaa5-133">备注</span><span class="sxs-lookup"><span data-stu-id="ccaa5-133">Remarks</span></span>

<span data-ttu-id="ccaa5-134">**SuggestionQuality**类型也是[DayQuality](dayquality.md)和[MinimumSuggestionQuality](minimumsuggestionquality.md)元素的类型。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-134">The **SuggestionQuality** type is also the type for the [DayQuality](dayquality.md) and the [MinimumSuggestionQuality](minimumsuggestionquality.md) elements.</span></span> 
  
<span data-ttu-id="ccaa5-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ccaa5-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccaa5-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="ccaa5-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccaa5-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="ccaa5-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ccaa5-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="ccaa5-138">Schema Name</span></span>  <br/> |<span data-ttu-id="ccaa5-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="ccaa5-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="ccaa5-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="ccaa5-140">Validation File</span></span>  <br/> |<span data-ttu-id="ccaa5-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ccaa5-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ccaa5-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="ccaa5-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccaa5-143">False</span><span class="sxs-lookup"><span data-stu-id="ccaa5-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccaa5-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ccaa5-144">See also</span></span>



[<span data-ttu-id="ccaa5-145">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ccaa5-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ccaa5-146">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ccaa5-146">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ccaa5-147">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="ccaa5-147">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

