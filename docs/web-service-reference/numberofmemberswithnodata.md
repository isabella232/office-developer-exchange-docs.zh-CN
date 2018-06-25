---
title: NumberOfMembersWithNoData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembersWithNoData
api_type:
- schema
ms.assetid: 7ca9c57c-9519-442c-a9f4-dca2b0309716
description: NumberOfMembersWithNoData 元素表示没有已发布忙/闲数据到建议的会议的时间比较通讯组列表成员数。 此元素表示太大通讯组列表的成员或拥有无数据状态的成员。
ms.openlocfilehash: f73978df47bd8240dd5dabfbbf74523525e3270f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826637"
---
# <a name="numberofmemberswithnodata"></a><span data-ttu-id="fd63f-104">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="fd63f-104">NumberOfMembersWithNoData</span></span>

<span data-ttu-id="fd63f-105">**NumberOfMembersWithNoData**元素表示没有已发布忙/闲数据到建议的会议的时间比较通讯组列表成员数。</span><span class="sxs-lookup"><span data-stu-id="fd63f-105">The **NumberOfMembersWithNoData** element represents the number of distribution list members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="fd63f-106">此元素表示太大通讯组列表的成员或拥有**无数据**状态的成员。</span><span class="sxs-lookup"><span data-stu-id="fd63f-106">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span> 
  
[<span data-ttu-id="fd63f-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fd63f-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="fd63f-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="fd63f-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="fd63f-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="fd63f-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="fd63f-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="fd63f-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="fd63f-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="fd63f-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="fd63f-112">建议</span><span class="sxs-lookup"><span data-stu-id="fd63f-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="fd63f-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="fd63f-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="fd63f-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="fd63f-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="fd63f-115">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="fd63f-115">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md)
  
```xml
<NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
```

 <span data-ttu-id="fd63f-116">**int**</span><span class="sxs-lookup"><span data-stu-id="fd63f-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd63f-117">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fd63f-117">Attributes and elements</span></span>

<span data-ttu-id="fd63f-118">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fd63f-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd63f-119">属性</span><span class="sxs-lookup"><span data-stu-id="fd63f-119">Attributes</span></span>

<span data-ttu-id="fd63f-120">无。</span><span class="sxs-lookup"><span data-stu-id="fd63f-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd63f-121">子元素</span><span class="sxs-lookup"><span data-stu-id="fd63f-121">Child elements</span></span>

<span data-ttu-id="fd63f-122">无。</span><span class="sxs-lookup"><span data-stu-id="fd63f-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fd63f-123">父元素</span><span class="sxs-lookup"><span data-stu-id="fd63f-123">Parent elements</span></span>

|<span data-ttu-id="fd63f-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="fd63f-124">**Element**</span></span>|<span data-ttu-id="fd63f-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="fd63f-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd63f-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="fd63f-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="fd63f-127">包含有关可用的用户数、 用户拥有冲突，数和不具有可用性信息通讯组列表中建议的会议时间的用户数的聚合冲突信息。</span><span class="sxs-lookup"><span data-stu-id="fd63f-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="fd63f-128">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="fd63f-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd63f-129">注解</span><span class="sxs-lookup"><span data-stu-id="fd63f-129">Remarks</span></span>

<span data-ttu-id="fd63f-130">组中没有邮箱中的联系人是通讯组列表成员中没有日历数据的示例。</span><span class="sxs-lookup"><span data-stu-id="fd63f-130">A contact in a group who does not have a mailbox is an example of a distribution list member who does not have calendar data.</span></span> <span data-ttu-id="fd63f-131">联系人可能还必须**无数据**状态，原因如下：</span><span class="sxs-lookup"><span data-stu-id="fd63f-131">A contact may also have **No Data** status for the following reasons:</span></span> 
  
- <span data-ttu-id="fd63f-132">没有足够的权限。</span><span class="sxs-lookup"><span data-stu-id="fd63f-132">Permissions are insufficient.</span></span>
    
- <span data-ttu-id="fd63f-133">太大，无法展开通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="fd63f-133">The distribution list is too large to expand.</span></span>
    
- <span data-ttu-id="fd63f-134">Active Directory 目录服务不可用。</span><span class="sxs-lookup"><span data-stu-id="fd63f-134">The Active Directory directory service is unavailable.</span></span>
    
<span data-ttu-id="fd63f-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fd63f-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd63f-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="fd63f-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd63f-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="fd63f-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fd63f-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="fd63f-138">Schema Name</span></span>  <br/> |<span data-ttu-id="fd63f-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="fd63f-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="fd63f-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="fd63f-140">Validation File</span></span>  <br/> |<span data-ttu-id="fd63f-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fd63f-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fd63f-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="fd63f-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd63f-143">False</span><span class="sxs-lookup"><span data-stu-id="fd63f-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd63f-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fd63f-144">See also</span></span>



[<span data-ttu-id="fd63f-145">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="fd63f-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="fd63f-146">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fd63f-146">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="fd63f-147">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="fd63f-147">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

