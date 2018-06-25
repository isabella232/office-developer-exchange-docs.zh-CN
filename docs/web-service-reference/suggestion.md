---
title: 建议
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Suggestion
api_type:
- schema
ms.assetid: 040a5c8f-b62f-4d1d-9d2c-dc3c5e01481f
description: 建议元素均表示一个会议建议。
ms.openlocfilehash: 24e2db1e0eabe35f7c971b0f1dbcbd333358f171
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838157"
---
# <a name="suggestion"></a><span data-ttu-id="7a2a4-103">建议</span><span class="sxs-lookup"><span data-stu-id="7a2a4-103">Suggestion</span></span>

<span data-ttu-id="7a2a4-104">**建议**元素均表示一个会议建议。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-104">The **Suggestion** element represents a single meeting suggestion.</span></span> 
  
[<span data-ttu-id="7a2a4-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7a2a4-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="7a2a4-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="7a2a4-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="7a2a4-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="7a2a4-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="7a2a4-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="7a2a4-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="7a2a4-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="7a2a4-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="7a2a4-110">建议</span><span class="sxs-lookup"><span data-stu-id="7a2a4-110">Suggestion</span></span>](suggestion.md)
  
```xml
<Suggestion>
   <MeetingTime>...</MeetingTime>
   <IsWorkTime>...</IsWorkTime>
   <SuggestionQuality>...</SuggestionQuality>
   <AttendeeConflictDataArray>...</AttendeeConflictDataArray>
</Suggestion>
```

 <span data-ttu-id="7a2a4-111">**建议**</span><span class="sxs-lookup"><span data-stu-id="7a2a4-111">**Suggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a2a4-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a2a4-112">Attributes and elements</span></span>

<span data-ttu-id="7a2a4-113">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a2a4-114">属性</span><span class="sxs-lookup"><span data-stu-id="7a2a4-114">Attributes</span></span>

<span data-ttu-id="7a2a4-115">无。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a2a4-116">子元素</span><span class="sxs-lookup"><span data-stu-id="7a2a4-116">Child elements</span></span>

|<span data-ttu-id="7a2a4-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a2a4-117">**Element**</span></span>|<span data-ttu-id="7a2a4-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a2a4-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a2a4-119">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="7a2a4-119">MeetingTime</span></span>](meetingtime.md) <br/> |<span data-ttu-id="7a2a4-120">代表建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-120">Represents a suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="7a2a4-121">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="7a2a4-121">IsWorkTime</span></span>](isworktime.md) <br/> |<span data-ttu-id="7a2a4-122">表示是否建议的会议时间期间计划的工作小时发生。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-122">Represents whether the suggested meeting time occurs during scheduled work hours.</span></span>  <br/> |
|[<span data-ttu-id="7a2a4-123">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="7a2a4-123">SuggestionQuality</span></span>](suggestionquality.md) <br/> |<span data-ttu-id="7a2a4-124">表示质量的建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-124">Represents the quality of the suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="7a2a4-125">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="7a2a4-125">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="7a2a4-126">包含描述用户和资源和建议的会议时间之间的冲突的信息的数组。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-126">Contains an array of information that describes conflicts between users and resources and the suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7a2a4-127">父元素</span><span class="sxs-lookup"><span data-stu-id="7a2a4-127">Parent elements</span></span>

|<span data-ttu-id="7a2a4-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a2a4-128">**Element**</span></span>|<span data-ttu-id="7a2a4-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a2a4-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a2a4-130">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="7a2a4-130">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="7a2a4-131">包含建议的会议时间的数组。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-131">Contains an array of suggested meeting times.</span></span>  <br/> <span data-ttu-id="7a2a4-132">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="7a2a4-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a2a4-133">备注</span><span class="sxs-lookup"><span data-stu-id="7a2a4-133">Remarks</span></span>

<span data-ttu-id="7a2a4-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7a2a4-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a2a4-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="7a2a4-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a2a4-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="7a2a4-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a2a4-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="7a2a4-137">Schema Name</span></span>  <br/> |<span data-ttu-id="7a2a4-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="7a2a4-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="7a2a4-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="7a2a4-139">Validation File</span></span>  <br/> |<span data-ttu-id="7a2a4-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7a2a4-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a2a4-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="7a2a4-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="7a2a4-142">False</span><span class="sxs-lookup"><span data-stu-id="7a2a4-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a2a4-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a2a4-143">See also</span></span>



[<span data-ttu-id="7a2a4-144">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="7a2a4-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="7a2a4-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="7a2a4-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="7a2a4-146">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="7a2a4-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

