---
title: NumberOfMembersWithConflict
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembersWithConflict
api_type:
- schema
ms.assetid: e61154f7-d262-43ec-b2bf-1ba6804b28dc
description: NumberOfMembersWithConflict 元素表示拥有建议的会议时间冲突的通讯组列表成员数。 此元素表示具有忙碌、 OOF，或暂定状态的成员。
ms.openlocfilehash: 227783b4bed32686e8e098f88498fe8ebb25e3cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826634"
---
# <a name="numberofmemberswithconflict"></a><span data-ttu-id="b6985-104">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="b6985-104">NumberOfMembersWithConflict</span></span>

<span data-ttu-id="b6985-105">**NumberOfMembersWithConflict**元素表示拥有建议的会议时间冲突的通讯组列表成员数。</span><span class="sxs-lookup"><span data-stu-id="b6985-105">The **NumberOfMembersWithConflict** element represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="b6985-106">此元素表示具有**忙碌**、 **OOF**，或**暂定**状态的成员。</span><span class="sxs-lookup"><span data-stu-id="b6985-106">This element represents members who have a status of **Busy**, **OOF**, or **Tentative**.</span></span>
  
[<span data-ttu-id="b6985-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b6985-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="b6985-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="b6985-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="b6985-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="b6985-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="b6985-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="b6985-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="b6985-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="b6985-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="b6985-112">建议</span><span class="sxs-lookup"><span data-stu-id="b6985-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="b6985-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="b6985-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="b6985-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="b6985-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="b6985-115">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="b6985-115">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md)
  
```xml
<NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
```

 <span data-ttu-id="b6985-116">**int**</span><span class="sxs-lookup"><span data-stu-id="b6985-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b6985-117">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b6985-117">Attributes and elements</span></span>

<span data-ttu-id="b6985-118">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b6985-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b6985-119">属性</span><span class="sxs-lookup"><span data-stu-id="b6985-119">Attributes</span></span>

<span data-ttu-id="b6985-120">无。</span><span class="sxs-lookup"><span data-stu-id="b6985-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b6985-121">子元素</span><span class="sxs-lookup"><span data-stu-id="b6985-121">Child elements</span></span>

<span data-ttu-id="b6985-122">无。</span><span class="sxs-lookup"><span data-stu-id="b6985-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b6985-123">父元素</span><span class="sxs-lookup"><span data-stu-id="b6985-123">Parent elements</span></span>

|<span data-ttu-id="b6985-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="b6985-124">**Element**</span></span>|<span data-ttu-id="b6985-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="b6985-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b6985-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="b6985-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="b6985-127">包含有关可用的用户数、 用户拥有冲突，数和不具有可用性信息通讯组列表中建议的会议时间的用户数的聚合冲突信息。</span><span class="sxs-lookup"><span data-stu-id="b6985-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="b6985-128">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="b6985-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6985-129">备注</span><span class="sxs-lookup"><span data-stu-id="b6985-129">Remarks</span></span>

<span data-ttu-id="b6985-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b6985-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b6985-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="b6985-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6985-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="b6985-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b6985-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="b6985-133">Schema Name</span></span>  <br/> |<span data-ttu-id="b6985-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="b6985-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="b6985-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="b6985-135">Validation File</span></span>  <br/> |<span data-ttu-id="b6985-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b6985-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b6985-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="b6985-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="b6985-138">False</span><span class="sxs-lookup"><span data-stu-id="b6985-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6985-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b6985-139">See also</span></span>



[<span data-ttu-id="b6985-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="b6985-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="b6985-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b6985-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="b6985-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="b6985-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

