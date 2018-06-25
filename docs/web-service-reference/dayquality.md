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
description: DayQuality 元素均表示包含质量建议的会议时间天的质量。
ms.openlocfilehash: 156d5bc58d481c9c812793da4722272ac76adaad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753769"
---
# <a name="dayquality"></a><span data-ttu-id="5b928-103">DayQuality</span><span class="sxs-lookup"><span data-stu-id="5b928-103">DayQuality</span></span>

<span data-ttu-id="5b928-104">**DayQuality**元素均表示包含建议会议时间的质量天的质量。</span><span class="sxs-lookup"><span data-stu-id="5b928-104">The **DayQuality** element represents the quality of the day for containing quality suggested meeting times.</span></span> 
  
- [<span data-ttu-id="5b928-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5b928-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="5b928-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="5b928-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="5b928-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="5b928-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="5b928-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="5b928-108">SuggestionDayResult</span></span>](suggestiondayresult.md) 
- [<span data-ttu-id="5b928-109">DayQuality</span><span class="sxs-lookup"><span data-stu-id="5b928-109">DayQuality</span></span>](dayquality.md)
  
```xml
<DayQuality>Excellent or Good or Fair or Poor</DayQuality>
```

<span data-ttu-id="5b928-110">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="5b928-110">**SuggestionQuality**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5b928-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5b928-111">Attributes and elements</span></span>

<span data-ttu-id="5b928-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5b928-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b928-113">属性</span><span class="sxs-lookup"><span data-stu-id="5b928-113">Attributes</span></span>

<span data-ttu-id="5b928-114">无。</span><span class="sxs-lookup"><span data-stu-id="5b928-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b928-115">子元素</span><span class="sxs-lookup"><span data-stu-id="5b928-115">Child elements</span></span>

<span data-ttu-id="5b928-116">无。</span><span class="sxs-lookup"><span data-stu-id="5b928-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5b928-117">父元素</span><span class="sxs-lookup"><span data-stu-id="5b928-117">Parent elements</span></span>

|<span data-ttu-id="5b928-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="5b928-118">**Element**</span></span>|<span data-ttu-id="5b928-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="5b928-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b928-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="5b928-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="5b928-121">表示一天包含建议的会议的时间。</span><span class="sxs-lookup"><span data-stu-id="5b928-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="5b928-122">以下是此元素的 XPath 2.0 表达式：</span><span class="sxs-lookup"><span data-stu-id="5b928-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5b928-123">文本值</span><span class="sxs-lookup"><span data-stu-id="5b928-123">Text value</span></span>

<span data-ttu-id="5b928-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="5b928-124">A text value is required.</span></span> <span data-ttu-id="5b928-125">此元素的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="5b928-125">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="5b928-126">**非常好**</span><span class="sxs-lookup"><span data-stu-id="5b928-126">**Excellent**</span></span>   
- <span data-ttu-id="5b928-127">**良好**</span><span class="sxs-lookup"><span data-stu-id="5b928-127">**Good**</span></span>    
- <span data-ttu-id="5b928-128">**公平**</span><span class="sxs-lookup"><span data-stu-id="5b928-128">**Fair**</span></span>    
- <span data-ttu-id="5b928-129">**不佳**</span><span class="sxs-lookup"><span data-stu-id="5b928-129">**Poor**</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b928-130">备注</span><span class="sxs-lookup"><span data-stu-id="5b928-130">Remarks</span></span>

<span data-ttu-id="5b928-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5b928-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b928-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="5b928-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b928-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="5b928-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5b928-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="5b928-134">Schema Name</span></span>  <br/> |<span data-ttu-id="5b928-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="5b928-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="5b928-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="5b928-136">Validation File</span></span>  <br/> |<span data-ttu-id="5b928-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5b928-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5b928-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="5b928-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="5b928-139">False</span><span class="sxs-lookup"><span data-stu-id="5b928-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b928-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b928-140">See also</span></span>

- [<span data-ttu-id="5b928-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="5b928-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="5b928-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5b928-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="5b928-143">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="5b928-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

