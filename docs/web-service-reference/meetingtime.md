---
title: MeetingTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingTime
api_type:
- schema
ms.assetid: 6e6d2d8b-e8a2-43e6-a715-0fc7d6dd44b9
description: MeetingTime 元素均表示建议的会议时间。
ms.openlocfilehash: 1ea79be394124431aa1279ee94d5e5c6331d377b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826435"
---
# <a name="meetingtime"></a><span data-ttu-id="894d7-103">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="894d7-103">MeetingTime</span></span>

<span data-ttu-id="894d7-104">**MeetingTime**元素均表示建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="894d7-104">The **MeetingTime** element represents a suggested meeting time.</span></span> 
  
[<span data-ttu-id="894d7-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="894d7-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="894d7-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="894d7-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="894d7-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="894d7-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="894d7-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="894d7-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="894d7-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="894d7-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="894d7-110">建议</span><span class="sxs-lookup"><span data-stu-id="894d7-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="894d7-111">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="894d7-111">MeetingTime</span></span>](meetingtime.md)
  
```xml
<MeetingTime>...</MeetingTime
```

 <span data-ttu-id="894d7-112">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="894d7-112">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="894d7-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="894d7-113">Attributes and elements</span></span>

<span data-ttu-id="894d7-114">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="894d7-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="894d7-115">属性</span><span class="sxs-lookup"><span data-stu-id="894d7-115">Attributes</span></span>

<span data-ttu-id="894d7-116">无。</span><span class="sxs-lookup"><span data-stu-id="894d7-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="894d7-117">子元素</span><span class="sxs-lookup"><span data-stu-id="894d7-117">Child elements</span></span>

<span data-ttu-id="894d7-118">无。</span><span class="sxs-lookup"><span data-stu-id="894d7-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="894d7-119">父元素</span><span class="sxs-lookup"><span data-stu-id="894d7-119">Parent elements</span></span>

|<span data-ttu-id="894d7-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="894d7-120">**Element**</span></span>|<span data-ttu-id="894d7-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="894d7-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="894d7-122">建议</span><span class="sxs-lookup"><span data-stu-id="894d7-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="894d7-123">代表单个会议时间建议。</span><span class="sxs-lookup"><span data-stu-id="894d7-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="894d7-124">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="894d7-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="894d7-125">文本值</span><span class="sxs-lookup"><span data-stu-id="894d7-125">Text value</span></span>

<span data-ttu-id="894d7-126">所需的文本值，该值代表**dateTime**值。</span><span class="sxs-lookup"><span data-stu-id="894d7-126">A text value that represents a **dateTime** value is required.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="894d7-127">注解</span><span class="sxs-lookup"><span data-stu-id="894d7-127">Remarks</span></span>

<span data-ttu-id="894d7-128">[MeetingTime](meetingtime.md)元素是[建议](suggestion.md)元素的必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="894d7-128">The [MeetingTime](meetingtime.md) element is a required child element of the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="894d7-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="894d7-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="894d7-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="894d7-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="894d7-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="894d7-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="894d7-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="894d7-132">Schema Name</span></span>  <br/> |<span data-ttu-id="894d7-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="894d7-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="894d7-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="894d7-134">Validation File</span></span>  <br/> |<span data-ttu-id="894d7-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="894d7-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="894d7-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="894d7-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="894d7-137">False</span><span class="sxs-lookup"><span data-stu-id="894d7-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="894d7-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="894d7-138">See also</span></span>



[<span data-ttu-id="894d7-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="894d7-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="894d7-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="894d7-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="894d7-141">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="894d7-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

