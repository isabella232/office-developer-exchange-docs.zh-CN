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
description: 建议元素表示单个会议建议。
ms.openlocfilehash: 25821abd5463ddba86a487709c8d2f8d928a94cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530378"
---
# <a name="suggestion"></a><span data-ttu-id="afebf-103">建议</span><span class="sxs-lookup"><span data-stu-id="afebf-103">Suggestion</span></span>

<span data-ttu-id="afebf-104">**建议**元素表示单个会议建议。</span><span class="sxs-lookup"><span data-stu-id="afebf-104">The **Suggestion** element represents a single meeting suggestion.</span></span> 
  
[<span data-ttu-id="afebf-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="afebf-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="afebf-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="afebf-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="afebf-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="afebf-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="afebf-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="afebf-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="afebf-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="afebf-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="afebf-110">建议</span><span class="sxs-lookup"><span data-stu-id="afebf-110">Suggestion</span></span>](suggestion.md)
  
```xml
<Suggestion>
   <MeetingTime>...</MeetingTime>
   <IsWorkTime>...</IsWorkTime>
   <SuggestionQuality>...</SuggestionQuality>
   <AttendeeConflictDataArray>...</AttendeeConflictDataArray>
</Suggestion>
```

 <span data-ttu-id="afebf-111">**建议**</span><span class="sxs-lookup"><span data-stu-id="afebf-111">**Suggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="afebf-112">属性和元素</span><span class="sxs-lookup"><span data-stu-id="afebf-112">Attributes and elements</span></span>

<span data-ttu-id="afebf-113">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="afebf-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="afebf-114">Attributes</span><span class="sxs-lookup"><span data-stu-id="afebf-114">Attributes</span></span>

<span data-ttu-id="afebf-115">无。</span><span class="sxs-lookup"><span data-stu-id="afebf-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="afebf-116">子元素</span><span class="sxs-lookup"><span data-stu-id="afebf-116">Child elements</span></span>

|<span data-ttu-id="afebf-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="afebf-117">**Element**</span></span>|<span data-ttu-id="afebf-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="afebf-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afebf-119">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="afebf-119">MeetingTime</span></span>](meetingtime.md) <br/> |<span data-ttu-id="afebf-120">表示建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="afebf-120">Represents a suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="afebf-121">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="afebf-121">IsWorkTime</span></span>](isworktime.md) <br/> |<span data-ttu-id="afebf-122">表示建议的会议时间是否在安排的工作时间内发生。</span><span class="sxs-lookup"><span data-stu-id="afebf-122">Represents whether the suggested meeting time occurs during scheduled work hours.</span></span>  <br/> |
|[<span data-ttu-id="afebf-123">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="afebf-123">SuggestionQuality</span></span>](suggestionquality.md) <br/> |<span data-ttu-id="afebf-124">表示建议会议时间的质量。</span><span class="sxs-lookup"><span data-stu-id="afebf-124">Represents the quality of the suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="afebf-125">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="afebf-125">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="afebf-126">包含描述用户和资源之间的冲突以及建议的会议时间的信息数组。</span><span class="sxs-lookup"><span data-stu-id="afebf-126">Contains an array of information that describes conflicts between users and resources and the suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="afebf-127">父元素</span><span class="sxs-lookup"><span data-stu-id="afebf-127">Parent elements</span></span>

|<span data-ttu-id="afebf-128">**元素**</span><span class="sxs-lookup"><span data-stu-id="afebf-128">**Element**</span></span>|<span data-ttu-id="afebf-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="afebf-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="afebf-130">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="afebf-130">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="afebf-131">包含建议会议时间的数组。</span><span class="sxs-lookup"><span data-stu-id="afebf-131">Contains an array of suggested meeting times.</span></span>  <br/> <span data-ttu-id="afebf-132">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="afebf-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afebf-133">说明</span><span class="sxs-lookup"><span data-stu-id="afebf-133">Remarks</span></span>

<span data-ttu-id="afebf-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="afebf-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="afebf-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="afebf-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="afebf-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="afebf-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="afebf-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="afebf-137">Schema Name</span></span>  <br/> |<span data-ttu-id="afebf-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="afebf-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="afebf-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="afebf-139">Validation File</span></span>  <br/> |<span data-ttu-id="afebf-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="afebf-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="afebf-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="afebf-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="afebf-142">False</span><span class="sxs-lookup"><span data-stu-id="afebf-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="afebf-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="afebf-143">See also</span></span>



[<span data-ttu-id="afebf-144">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="afebf-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="afebf-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="afebf-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="afebf-146">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="afebf-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

