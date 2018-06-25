---
title: SuggestionDayResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionDayResult
api_type:
- schema
ms.assetid: 916b1cbb-f2e3-471d-84b0-e33467616652
description: SuggestionDayResult 元素均表示一天包含建议的会议的时间。
ms.openlocfilehash: 7b75258a9e70f1ec6feed6a0b18beb76f356c7f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838159"
---
# <a name="suggestiondayresult"></a><span data-ttu-id="db7ca-103">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="db7ca-103">SuggestionDayResult</span></span>

<span data-ttu-id="db7ca-104">**SuggestionDayResult**元素均表示一天包含建议的会议的时间。</span><span class="sxs-lookup"><span data-stu-id="db7ca-104">The **SuggestionDayResult** element represents a single day that contains suggested meeting times.</span></span> 
  
[<span data-ttu-id="db7ca-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="db7ca-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="db7ca-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="db7ca-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="db7ca-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="db7ca-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="db7ca-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="db7ca-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
```xml
<SuggestionDayResult>
   <Date>...</Date>
   <DayQuality>...</DayQuality>
   <SuggestionArray>...</SuggestionArray>
</SuggestionDayResult>
```

 <span data-ttu-id="db7ca-109">**SuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="db7ca-109">**SuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db7ca-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="db7ca-110">Attributes and elements</span></span>

<span data-ttu-id="db7ca-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="db7ca-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db7ca-112">属性</span><span class="sxs-lookup"><span data-stu-id="db7ca-112">Attributes</span></span>

<span data-ttu-id="db7ca-113">无。</span><span class="sxs-lookup"><span data-stu-id="db7ca-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db7ca-114">子元素</span><span class="sxs-lookup"><span data-stu-id="db7ca-114">Child elements</span></span>

|<span data-ttu-id="db7ca-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="db7ca-115">**Element**</span></span>|<span data-ttu-id="db7ca-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="db7ca-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db7ca-117">Date</span><span class="sxs-lookup"><span data-stu-id="db7ca-117">Date</span></span>](date.md) <br/> |<span data-ttu-id="db7ca-118">表示包含建议的会议时间的日期。</span><span class="sxs-lookup"><span data-stu-id="db7ca-118">Represents the date that contains the suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="db7ca-119">DayQuality</span><span class="sxs-lookup"><span data-stu-id="db7ca-119">DayQuality</span></span>](dayquality.md) <br/> |<span data-ttu-id="db7ca-120">代表包含质量建议的会议时间天的质量。</span><span class="sxs-lookup"><span data-stu-id="db7ca-120">Represents the quality of the day for containing quality suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="db7ca-121">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="db7ca-121">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="db7ca-122">包含一个会议建议数组。</span><span class="sxs-lookup"><span data-stu-id="db7ca-122">Contains an array of meeting suggestions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="db7ca-123">父元素</span><span class="sxs-lookup"><span data-stu-id="db7ca-123">Parent elements</span></span>

|<span data-ttu-id="db7ca-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="db7ca-124">**Element**</span></span>|<span data-ttu-id="db7ca-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="db7ca-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db7ca-126">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="db7ca-126">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="db7ca-127">包含数组的会议建议组织的日期。</span><span class="sxs-lookup"><span data-stu-id="db7ca-127">Contains an array of meeting suggestions organized by date.</span></span>  <br/> <span data-ttu-id="db7ca-128">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="db7ca-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db7ca-129">备注</span><span class="sxs-lookup"><span data-stu-id="db7ca-129">Remarks</span></span>

<span data-ttu-id="db7ca-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="db7ca-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db7ca-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="db7ca-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db7ca-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="db7ca-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db7ca-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="db7ca-133">Schema Name</span></span>  <br/> |<span data-ttu-id="db7ca-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="db7ca-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="db7ca-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="db7ca-135">Validation File</span></span>  <br/> |<span data-ttu-id="db7ca-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="db7ca-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="db7ca-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="db7ca-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="db7ca-138">False</span><span class="sxs-lookup"><span data-stu-id="db7ca-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db7ca-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="db7ca-139">See also</span></span>



[<span data-ttu-id="db7ca-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="db7ca-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="db7ca-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="db7ca-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="db7ca-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="db7ca-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

