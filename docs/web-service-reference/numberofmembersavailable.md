---
title: NumberOfMembersAvailable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembersAvailable
api_type:
- schema
ms.assetid: e367a278-1622-4b65-955f-2d4b2fc6e4d7
description: NumberOfMembersAvailable 元素表示建议的会议的时间可用的通讯组列表成员的数。 此元素表示为其状态是免费的成员。
ms.openlocfilehash: 8669f61fbd640c160ad54739c5a15407b3dd470a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826641"
---
# <a name="numberofmembersavailable"></a><span data-ttu-id="80e8e-104">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="80e8e-104">NumberOfMembersAvailable</span></span>

<span data-ttu-id="80e8e-105">**NumberOfMembersAvailable**元素表示建议的会议的时间可用的通讯组列表成员的数。</span><span class="sxs-lookup"><span data-stu-id="80e8e-105">The **NumberOfMembersAvailable** element represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="80e8e-106">此元素表示为其状态是**免费**的成员。</span><span class="sxs-lookup"><span data-stu-id="80e8e-106">This element represents members for whom the status is **Free**.</span></span>
  
[<span data-ttu-id="80e8e-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="80e8e-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="80e8e-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="80e8e-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="80e8e-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="80e8e-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="80e8e-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="80e8e-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="80e8e-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="80e8e-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="80e8e-112">建议</span><span class="sxs-lookup"><span data-stu-id="80e8e-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="80e8e-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="80e8e-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="80e8e-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="80e8e-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="80e8e-115">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="80e8e-115">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md)
  
```xml
<NumberOfMembersAvailable>...</NumberOfMembersAvailable>
```

 <span data-ttu-id="80e8e-116">**int**</span><span class="sxs-lookup"><span data-stu-id="80e8e-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80e8e-117">属性和元素</span><span class="sxs-lookup"><span data-stu-id="80e8e-117">Attributes and elements</span></span>

<span data-ttu-id="80e8e-118">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="80e8e-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80e8e-119">属性</span><span class="sxs-lookup"><span data-stu-id="80e8e-119">Attributes</span></span>

<span data-ttu-id="80e8e-120">无。</span><span class="sxs-lookup"><span data-stu-id="80e8e-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80e8e-121">子元素</span><span class="sxs-lookup"><span data-stu-id="80e8e-121">Child elements</span></span>

<span data-ttu-id="80e8e-122">无。</span><span class="sxs-lookup"><span data-stu-id="80e8e-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80e8e-123">父元素</span><span class="sxs-lookup"><span data-stu-id="80e8e-123">Parent elements</span></span>

|<span data-ttu-id="80e8e-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="80e8e-124">**Element**</span></span>|<span data-ttu-id="80e8e-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="80e8e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="80e8e-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="80e8e-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="80e8e-127">包含有关可用的用户数、 用户拥有冲突，数和不具有可用性信息通讯组列表中建议的会议时间的用户数的聚合冲突信息。</span><span class="sxs-lookup"><span data-stu-id="80e8e-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="80e8e-128">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="80e8e-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80e8e-129">备注</span><span class="sxs-lookup"><span data-stu-id="80e8e-129">Remarks</span></span>

<span data-ttu-id="80e8e-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="80e8e-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80e8e-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="80e8e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80e8e-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="80e8e-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="80e8e-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="80e8e-133">Schema Name</span></span>  <br/> |<span data-ttu-id="80e8e-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="80e8e-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="80e8e-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="80e8e-135">Validation File</span></span>  <br/> |<span data-ttu-id="80e8e-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="80e8e-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="80e8e-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="80e8e-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="80e8e-138">False</span><span class="sxs-lookup"><span data-stu-id="80e8e-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80e8e-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80e8e-139">See also</span></span>



[<span data-ttu-id="80e8e-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="80e8e-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="80e8e-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="80e8e-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="80e8e-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="80e8e-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

