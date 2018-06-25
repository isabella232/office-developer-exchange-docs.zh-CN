---
title: NumberOfMembers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembers
api_type:
- schema
ms.assetid: 845fb877-de49-4e26-8885-6f026edd9ee9
description: NumberOfMembers 元素表示用户、 资源和通讯组列表中的聊天室的数量。
ms.openlocfilehash: 9777660b1a54bfb5afb6e569ba1009a1654bdef3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826635"
---
# <a name="numberofmembers"></a><span data-ttu-id="3368d-103">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="3368d-103">NumberOfMembers</span></span>

<span data-ttu-id="3368d-104">**NumberOfMembers**元素表示用户、 资源和通讯组列表中的聊天室的数量。</span><span class="sxs-lookup"><span data-stu-id="3368d-104">The **NumberOfMembers** element represents the number of users, resources, and rooms in a distribution list.</span></span> 
  
[<span data-ttu-id="3368d-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3368d-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="3368d-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="3368d-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="3368d-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="3368d-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="3368d-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="3368d-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="3368d-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="3368d-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="3368d-110">建议</span><span class="sxs-lookup"><span data-stu-id="3368d-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="3368d-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="3368d-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="3368d-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="3368d-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="3368d-113">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="3368d-113">NumberOfMembers</span></span>](numberofmembers.md)
  
```xml
<NumberOfMembers>...</NumberOfMembers>
```

 <span data-ttu-id="3368d-114">**int**</span><span class="sxs-lookup"><span data-stu-id="3368d-114">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3368d-115">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3368d-115">Attributes and elements</span></span>

<span data-ttu-id="3368d-116">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3368d-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3368d-117">属性</span><span class="sxs-lookup"><span data-stu-id="3368d-117">Attributes</span></span>

<span data-ttu-id="3368d-118">无。</span><span class="sxs-lookup"><span data-stu-id="3368d-118">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3368d-119">子元素</span><span class="sxs-lookup"><span data-stu-id="3368d-119">Child elements</span></span>

<span data-ttu-id="3368d-120">无。</span><span class="sxs-lookup"><span data-stu-id="3368d-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3368d-121">父元素</span><span class="sxs-lookup"><span data-stu-id="3368d-121">Parent elements</span></span>

|<span data-ttu-id="3368d-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="3368d-122">**Element**</span></span>|<span data-ttu-id="3368d-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="3368d-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3368d-124">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="3368d-124">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="3368d-125">包含有关可用的用户数、 用户拥有冲突，数和不具有可用性信息通讯组列表中建议的会议时间的用户数的聚合冲突信息。</span><span class="sxs-lookup"><span data-stu-id="3368d-125">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="3368d-126">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="3368d-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3368d-127">注解</span><span class="sxs-lookup"><span data-stu-id="3368d-127">Remarks</span></span>

<span data-ttu-id="3368d-128">**NumberOfMembers**元素的最大值为 100。</span><span class="sxs-lookup"><span data-stu-id="3368d-128">The maximum value of the **NumberOfMembers** element is 100.</span></span> 
  
<span data-ttu-id="3368d-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3368d-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3368d-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="3368d-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3368d-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="3368d-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3368d-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="3368d-132">Schema Name</span></span>  <br/> |<span data-ttu-id="3368d-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="3368d-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="3368d-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="3368d-134">Validation File</span></span>  <br/> |<span data-ttu-id="3368d-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3368d-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3368d-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="3368d-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="3368d-137">False</span><span class="sxs-lookup"><span data-stu-id="3368d-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3368d-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3368d-138">See also</span></span>



[<span data-ttu-id="3368d-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="3368d-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="3368d-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3368d-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="3368d-141">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="3368d-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

