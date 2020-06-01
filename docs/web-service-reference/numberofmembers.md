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
description: NumberOfMembers 元素表示通讯组列表中的用户、资源和会议室的数量。
ms.openlocfilehash: c91087f42d806afb0a0d3d607cc84f14a1a6c1b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462596"
---
# <a name="numberofmembers"></a><span data-ttu-id="047f9-103">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="047f9-103">NumberOfMembers</span></span>

<span data-ttu-id="047f9-104">**NumberOfMembers**元素表示通讯组列表中的用户、资源和会议室的数量。</span><span class="sxs-lookup"><span data-stu-id="047f9-104">The **NumberOfMembers** element represents the number of users, resources, and rooms in a distribution list.</span></span> 
  
[<span data-ttu-id="047f9-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="047f9-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="047f9-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="047f9-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="047f9-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="047f9-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="047f9-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="047f9-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="047f9-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="047f9-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="047f9-110">建议</span><span class="sxs-lookup"><span data-stu-id="047f9-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="047f9-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="047f9-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="047f9-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="047f9-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="047f9-113">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="047f9-113">NumberOfMembers</span></span>](numberofmembers.md)
  
```xml
<NumberOfMembers>...</NumberOfMembers>
```

 <span data-ttu-id="047f9-114">**int**</span><span class="sxs-lookup"><span data-stu-id="047f9-114">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="047f9-115">属性和元素</span><span class="sxs-lookup"><span data-stu-id="047f9-115">Attributes and elements</span></span>

<span data-ttu-id="047f9-116">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="047f9-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="047f9-117">Attributes</span><span class="sxs-lookup"><span data-stu-id="047f9-117">Attributes</span></span>

<span data-ttu-id="047f9-118">无。</span><span class="sxs-lookup"><span data-stu-id="047f9-118">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="047f9-119">子元素</span><span class="sxs-lookup"><span data-stu-id="047f9-119">Child elements</span></span>

<span data-ttu-id="047f9-120">无。</span><span class="sxs-lookup"><span data-stu-id="047f9-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="047f9-121">父元素</span><span class="sxs-lookup"><span data-stu-id="047f9-121">Parent elements</span></span>

|<span data-ttu-id="047f9-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="047f9-122">**Element**</span></span>|<span data-ttu-id="047f9-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="047f9-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="047f9-124">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="047f9-124">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="047f9-125">包含有关可用用户数、有冲突的用户数以及在通讯组列表中没有可用性信息的用户数的聚合冲突信息，以获取建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="047f9-125">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="047f9-126">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="047f9-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="047f9-127">备注</span><span class="sxs-lookup"><span data-stu-id="047f9-127">Remarks</span></span>

<span data-ttu-id="047f9-128">**NumberOfMembers**元素的最大值为100。</span><span class="sxs-lookup"><span data-stu-id="047f9-128">The maximum value of the **NumberOfMembers** element is 100.</span></span> 
  
<span data-ttu-id="047f9-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="047f9-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="047f9-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="047f9-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="047f9-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="047f9-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="047f9-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="047f9-132">Schema Name</span></span>  <br/> |<span data-ttu-id="047f9-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="047f9-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="047f9-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="047f9-134">Validation File</span></span>  <br/> |<span data-ttu-id="047f9-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="047f9-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="047f9-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="047f9-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="047f9-137">False</span><span class="sxs-lookup"><span data-stu-id="047f9-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="047f9-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="047f9-138">See also</span></span>



[<span data-ttu-id="047f9-139">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="047f9-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="047f9-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="047f9-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="047f9-141">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="047f9-141">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

