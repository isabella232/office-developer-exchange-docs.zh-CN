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
ms.openlocfilehash: ec982417c39569820beef82ae837eacbe316740c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466673"
---
# <a name="suggestionarray"></a><span data-ttu-id="207da-103">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="207da-103">SuggestionArray</span></span>

<span data-ttu-id="207da-104">**SuggestionArray**元素包含一个会议建议数组。</span><span class="sxs-lookup"><span data-stu-id="207da-104">The **SuggestionArray** element contains an array of meeting suggestions.</span></span> 
  
[<span data-ttu-id="207da-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="207da-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="207da-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="207da-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="207da-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="207da-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="207da-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="207da-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="207da-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="207da-109">SuggestionArray</span></span>](suggestionarray.md)
  
```xml
<SuggestionArray>
   <Suggestion>...</Suggestion>
</SuggestionArray>
```

 <span data-ttu-id="207da-110">**ArrayOfSuggestion**</span><span class="sxs-lookup"><span data-stu-id="207da-110">**ArrayOfSuggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="207da-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="207da-111">Attributes and elements</span></span>

<span data-ttu-id="207da-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="207da-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="207da-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="207da-113">Attributes</span></span>

<span data-ttu-id="207da-114">无。</span><span class="sxs-lookup"><span data-stu-id="207da-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="207da-115">子元素</span><span class="sxs-lookup"><span data-stu-id="207da-115">Child elements</span></span>

|<span data-ttu-id="207da-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="207da-116">**Element**</span></span>|<span data-ttu-id="207da-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="207da-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="207da-118">建议</span><span class="sxs-lookup"><span data-stu-id="207da-118">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="207da-119">代表单个会议建议。</span><span class="sxs-lookup"><span data-stu-id="207da-119">Represents a single meeting suggestion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="207da-120">父元素</span><span class="sxs-lookup"><span data-stu-id="207da-120">Parent elements</span></span>

|<span data-ttu-id="207da-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="207da-121">**Element**</span></span>|<span data-ttu-id="207da-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="207da-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="207da-123">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="207da-123">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="207da-124">表示包含建议会议时间的一天。</span><span class="sxs-lookup"><span data-stu-id="207da-124">Represents a single day that contains suggested meeting times.</span></span>  <br/> <span data-ttu-id="207da-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="207da-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="207da-126">说明</span><span class="sxs-lookup"><span data-stu-id="207da-126">Remarks</span></span>

<span data-ttu-id="207da-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="207da-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="207da-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="207da-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="207da-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="207da-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="207da-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="207da-130">Schema Name</span></span>  <br/> |<span data-ttu-id="207da-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="207da-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="207da-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="207da-132">Validation File</span></span>  <br/> |<span data-ttu-id="207da-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="207da-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="207da-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="207da-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="207da-135">False</span><span class="sxs-lookup"><span data-stu-id="207da-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="207da-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="207da-136">See also</span></span>



[<span data-ttu-id="207da-137">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="207da-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="207da-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="207da-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="207da-139">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="207da-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

