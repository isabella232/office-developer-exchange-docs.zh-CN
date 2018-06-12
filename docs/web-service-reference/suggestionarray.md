---
title: SuggestionArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionArray
api_type:
- schema
ms.assetid: c1c26008-7b14-4563-8db5-bceb0f475b1b
description: SuggestionArray 元素包含一个会议建议数组。
ms.openlocfilehash: d595ae77de293a1975e15102f3f2c3395e6da633
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838158"
---
# <a name="suggestionarray"></a><span data-ttu-id="e800b-103">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="e800b-103">SuggestionArray</span></span>

<span data-ttu-id="e800b-104">**SuggestionArray**元素包含一个会议建议数组。</span><span class="sxs-lookup"><span data-stu-id="e800b-104">The **SuggestionArray** element contains an array of meeting suggestions.</span></span> 
  
[<span data-ttu-id="e800b-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e800b-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="e800b-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="e800b-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="e800b-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="e800b-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="e800b-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="e800b-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="e800b-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="e800b-109">SuggestionArray</span></span>](suggestionarray.md)
  
```xml
<SuggestionArray>
   <Suggestion>...</Suggestion>
</SuggestionArray>
```

 <span data-ttu-id="e800b-110">**ArrayOfSuggestion**</span><span class="sxs-lookup"><span data-stu-id="e800b-110">**ArrayOfSuggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e800b-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e800b-111">Attributes and elements</span></span>

<span data-ttu-id="e800b-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e800b-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e800b-113">属性</span><span class="sxs-lookup"><span data-stu-id="e800b-113">Attributes</span></span>

<span data-ttu-id="e800b-114">无。</span><span class="sxs-lookup"><span data-stu-id="e800b-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e800b-115">子元素</span><span class="sxs-lookup"><span data-stu-id="e800b-115">Child elements</span></span>

|<span data-ttu-id="e800b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e800b-116">**Element**</span></span>|<span data-ttu-id="e800b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e800b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e800b-118">建议</span><span class="sxs-lookup"><span data-stu-id="e800b-118">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="e800b-119">代表单个会议建议。</span><span class="sxs-lookup"><span data-stu-id="e800b-119">Represents a single meeting suggestion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e800b-120">父元素</span><span class="sxs-lookup"><span data-stu-id="e800b-120">Parent elements</span></span>

|<span data-ttu-id="e800b-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="e800b-121">**Element**</span></span>|<span data-ttu-id="e800b-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="e800b-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e800b-123">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="e800b-123">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="e800b-124">表示一天包含建议的会议的时间。</span><span class="sxs-lookup"><span data-stu-id="e800b-124">Represents a single day that contains suggested meeting times.</span></span>  <br/> <span data-ttu-id="e800b-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="e800b-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e800b-126">备注</span><span class="sxs-lookup"><span data-stu-id="e800b-126">Remarks</span></span>

<span data-ttu-id="e800b-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e800b-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e800b-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="e800b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e800b-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="e800b-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e800b-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="e800b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="e800b-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="e800b-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="e800b-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="e800b-132">Validation File</span></span>  <br/> |<span data-ttu-id="e800b-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e800b-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e800b-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="e800b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="e800b-135">False</span><span class="sxs-lookup"><span data-stu-id="e800b-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e800b-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e800b-136">See also</span></span>



[<span data-ttu-id="e800b-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="e800b-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="e800b-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e800b-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="e800b-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="e800b-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

