---
title: IsWorkTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsWorkTime
api_type:
- schema
ms.assetid: 5243dd19-3593-4a81-bb2d-90496e04cb98
description: IsWorkTime 元素表示是否建议的会议时间期间计划的工作小时发生。
ms.openlocfilehash: c687b29df226ebb28cdf01d3a2da62590f790924
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826135"
---
# <a name="isworktime"></a><span data-ttu-id="1d0bc-103">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="1d0bc-103">IsWorkTime</span></span>

<span data-ttu-id="1d0bc-104">**IsWorkTime**元素表示是否建议的会议时间期间计划的工作小时发生。</span><span class="sxs-lookup"><span data-stu-id="1d0bc-104">The **IsWorkTime** element represents whether the suggested meeting time occurs during scheduled work hours.</span></span> 
  
[<span data-ttu-id="1d0bc-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1d0bc-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="1d0bc-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="1d0bc-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="1d0bc-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="1d0bc-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="1d0bc-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="1d0bc-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="1d0bc-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="1d0bc-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="1d0bc-110">建议</span><span class="sxs-lookup"><span data-stu-id="1d0bc-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="1d0bc-111">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="1d0bc-111">IsWorkTime</span></span>](isworktime.md)
  
```xml
<IsWorkTime>true or false</IsWorkTime>
```

 <span data-ttu-id="1d0bc-112">**boolean**</span><span class="sxs-lookup"><span data-stu-id="1d0bc-112">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d0bc-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1d0bc-113">Attributes and elements</span></span>

<span data-ttu-id="1d0bc-114">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d0bc-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d0bc-115">属性</span><span class="sxs-lookup"><span data-stu-id="1d0bc-115">Attributes</span></span>

<span data-ttu-id="1d0bc-116">无。</span><span class="sxs-lookup"><span data-stu-id="1d0bc-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d0bc-117">子元素</span><span class="sxs-lookup"><span data-stu-id="1d0bc-117">Child elements</span></span>

<span data-ttu-id="1d0bc-118">无。</span><span class="sxs-lookup"><span data-stu-id="1d0bc-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d0bc-119">父元素</span><span class="sxs-lookup"><span data-stu-id="1d0bc-119">Parent elements</span></span>

|<span data-ttu-id="1d0bc-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="1d0bc-120">**Element**</span></span>|<span data-ttu-id="1d0bc-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="1d0bc-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d0bc-122">建议</span><span class="sxs-lookup"><span data-stu-id="1d0bc-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="1d0bc-123">代表单个会议时间建议。</span><span class="sxs-lookup"><span data-stu-id="1d0bc-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="1d0bc-124">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="1d0bc-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1d0bc-125">文本值</span><span class="sxs-lookup"><span data-stu-id="1d0bc-125">Text value</span></span>

<span data-ttu-id="1d0bc-126">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="1d0bc-126">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d0bc-127">备注</span><span class="sxs-lookup"><span data-stu-id="1d0bc-127">Remarks</span></span>

<span data-ttu-id="1d0bc-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1d0bc-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d0bc-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="1d0bc-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d0bc-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="1d0bc-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d0bc-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="1d0bc-131">Schema Name</span></span>  <br/> |<span data-ttu-id="1d0bc-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="1d0bc-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d0bc-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="1d0bc-133">Validation File</span></span>  <br/> |<span data-ttu-id="1d0bc-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1d0bc-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d0bc-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="1d0bc-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d0bc-136">False</span><span class="sxs-lookup"><span data-stu-id="1d0bc-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d0bc-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1d0bc-137">See also</span></span>



[<span data-ttu-id="1d0bc-138">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="1d0bc-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1d0bc-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1d0bc-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="1d0bc-140">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="1d0bc-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

