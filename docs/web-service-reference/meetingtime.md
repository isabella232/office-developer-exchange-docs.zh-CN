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
description: MeetingTime 元素表示建议的会议时间。
ms.openlocfilehash: 3a7031e70eb8b22adc8030c1cec09d33399332ee
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530448"
---
# <a name="meetingtime"></a><span data-ttu-id="f820e-103">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="f820e-103">MeetingTime</span></span>

<span data-ttu-id="f820e-104">**MeetingTime**元素表示建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="f820e-104">The **MeetingTime** element represents a suggested meeting time.</span></span> 
  
[<span data-ttu-id="f820e-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f820e-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="f820e-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="f820e-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="f820e-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="f820e-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="f820e-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="f820e-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="f820e-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="f820e-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="f820e-110">建议</span><span class="sxs-lookup"><span data-stu-id="f820e-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="f820e-111">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="f820e-111">MeetingTime</span></span>](meetingtime.md)
  
```xml
<MeetingTime>...</MeetingTime
```

 <span data-ttu-id="f820e-112">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="f820e-112">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f820e-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f820e-113">Attributes and elements</span></span>

<span data-ttu-id="f820e-114">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f820e-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f820e-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="f820e-115">Attributes</span></span>

<span data-ttu-id="f820e-116">无。</span><span class="sxs-lookup"><span data-stu-id="f820e-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f820e-117">子元素</span><span class="sxs-lookup"><span data-stu-id="f820e-117">Child elements</span></span>

<span data-ttu-id="f820e-118">无。</span><span class="sxs-lookup"><span data-stu-id="f820e-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f820e-119">父元素</span><span class="sxs-lookup"><span data-stu-id="f820e-119">Parent elements</span></span>

|<span data-ttu-id="f820e-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="f820e-120">**Element**</span></span>|<span data-ttu-id="f820e-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="f820e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f820e-122">建议</span><span class="sxs-lookup"><span data-stu-id="f820e-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="f820e-123">表示单个会议时间建议。</span><span class="sxs-lookup"><span data-stu-id="f820e-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="f820e-124">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="f820e-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f820e-125">文本值</span><span class="sxs-lookup"><span data-stu-id="f820e-125">Text value</span></span>

<span data-ttu-id="f820e-126">需要一个代表**dateTime**值的文本值。</span><span class="sxs-lookup"><span data-stu-id="f820e-126">A text value that represents a **dateTime** value is required.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f820e-127">备注</span><span class="sxs-lookup"><span data-stu-id="f820e-127">Remarks</span></span>

<span data-ttu-id="f820e-128">[MeetingTime](meetingtime.md)元素是[建议](suggestion.md)元素的必需子元素。</span><span class="sxs-lookup"><span data-stu-id="f820e-128">The [MeetingTime](meetingtime.md) element is a required child element of the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="f820e-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f820e-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f820e-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="f820e-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f820e-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="f820e-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f820e-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="f820e-132">Schema Name</span></span>  <br/> |<span data-ttu-id="f820e-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="f820e-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="f820e-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="f820e-134">Validation File</span></span>  <br/> |<span data-ttu-id="f820e-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f820e-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f820e-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="f820e-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="f820e-137">False</span><span class="sxs-lookup"><span data-stu-id="f820e-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f820e-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f820e-138">See also</span></span>



[<span data-ttu-id="f820e-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="f820e-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="f820e-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f820e-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="f820e-141">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="f820e-141">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

