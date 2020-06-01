---
title: DayQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayQuality
api_type:
- schema
ms.assetid: cd0eb239-6e7f-4a5a-b245-659f170550b7
description: DayQuality 元素表示用于包含质量建议会议时间的日的质量。
ms.openlocfilehash: 41cc8313dccb1a5172fefc167e6ed90a21109ec5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455112"
---
# <a name="dayquality"></a><span data-ttu-id="358d3-103">DayQuality</span><span class="sxs-lookup"><span data-stu-id="358d3-103">DayQuality</span></span>

<span data-ttu-id="358d3-104">**DayQuality**元素表示用于包含质量建议会议时间的日的质量。</span><span class="sxs-lookup"><span data-stu-id="358d3-104">The **DayQuality** element represents the quality of the day for containing quality suggested meeting times.</span></span> 
  
- [<span data-ttu-id="358d3-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="358d3-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="358d3-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="358d3-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="358d3-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="358d3-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="358d3-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="358d3-108">SuggestionDayResult</span></span>](suggestiondayresult.md) 
- [<span data-ttu-id="358d3-109">DayQuality</span><span class="sxs-lookup"><span data-stu-id="358d3-109">DayQuality</span></span>](dayquality.md)
  
```xml
<DayQuality>Excellent or Good or Fair or Poor</DayQuality>
```

<span data-ttu-id="358d3-110">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="358d3-110">**SuggestionQuality**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="358d3-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="358d3-111">Attributes and elements</span></span>

<span data-ttu-id="358d3-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="358d3-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="358d3-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="358d3-113">Attributes</span></span>

<span data-ttu-id="358d3-114">无。</span><span class="sxs-lookup"><span data-stu-id="358d3-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="358d3-115">子元素</span><span class="sxs-lookup"><span data-stu-id="358d3-115">Child elements</span></span>

<span data-ttu-id="358d3-116">无。</span><span class="sxs-lookup"><span data-stu-id="358d3-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="358d3-117">父元素</span><span class="sxs-lookup"><span data-stu-id="358d3-117">Parent elements</span></span>

|<span data-ttu-id="358d3-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="358d3-118">**Element**</span></span>|<span data-ttu-id="358d3-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="358d3-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="358d3-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="358d3-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="358d3-121">表示包含建议会议时间的一天。</span><span class="sxs-lookup"><span data-stu-id="358d3-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="358d3-122">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="358d3-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="358d3-123">文本值</span><span class="sxs-lookup"><span data-stu-id="358d3-123">Text value</span></span>

<span data-ttu-id="358d3-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="358d3-124">A text value is required.</span></span> <span data-ttu-id="358d3-125">以下是此元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="358d3-125">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="358d3-126">**极好**</span><span class="sxs-lookup"><span data-stu-id="358d3-126">**Excellent**</span></span>   
- <span data-ttu-id="358d3-127">**Good**</span><span class="sxs-lookup"><span data-stu-id="358d3-127">**Good**</span></span>    
- <span data-ttu-id="358d3-128">**大量**</span><span class="sxs-lookup"><span data-stu-id="358d3-128">**Fair**</span></span>    
- <span data-ttu-id="358d3-129">**较差**</span><span class="sxs-lookup"><span data-stu-id="358d3-129">**Poor**</span></span>
    
## <a name="remarks"></a><span data-ttu-id="358d3-130">说明</span><span class="sxs-lookup"><span data-stu-id="358d3-130">Remarks</span></span>

<span data-ttu-id="358d3-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="358d3-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="358d3-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="358d3-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="358d3-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="358d3-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="358d3-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="358d3-134">Schema Name</span></span>  <br/> |<span data-ttu-id="358d3-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="358d3-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="358d3-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="358d3-136">Validation File</span></span>  <br/> |<span data-ttu-id="358d3-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="358d3-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="358d3-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="358d3-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="358d3-139">False</span><span class="sxs-lookup"><span data-stu-id="358d3-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="358d3-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="358d3-140">See also</span></span>

- [<span data-ttu-id="358d3-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="358d3-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="358d3-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="358d3-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="358d3-143">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="358d3-143">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

