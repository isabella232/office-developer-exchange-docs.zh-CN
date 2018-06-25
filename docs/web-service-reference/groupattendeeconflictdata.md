---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: GroupAttendeeConflictData 元素包含聚合冲突信息均可用、 存在冲突，用户数量和分布中没有可用性信息的用户数列出的用户数量建议的会议时间。
ms.openlocfilehash: 382b4d866c95de98bd444cd6226d71813889d4f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825757"
---
# <a name="groupattendeeconflictdata"></a><span data-ttu-id="43c84-103">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="43c84-103">GroupAttendeeConflictData</span></span>

<span data-ttu-id="43c84-104">**GroupAttendeeConflictData**元素包含聚合冲突有关可用的用户数、 用户拥有冲突，数和通讯组列表中没有可用性信息的用户数在建议的会议的时间。</span><span class="sxs-lookup"><span data-stu-id="43c84-104">The **GroupAttendeeConflictData** element contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span> 
  
- [<span data-ttu-id="43c84-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="43c84-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="43c84-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="43c84-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
- [<span data-ttu-id="43c84-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="43c84-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
- [<span data-ttu-id="43c84-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="43c84-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
- [<span data-ttu-id="43c84-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="43c84-109">SuggestionArray</span></span>](suggestionarray.md)
- [<span data-ttu-id="43c84-110">建议</span><span class="sxs-lookup"><span data-stu-id="43c84-110">Suggestion</span></span>](suggestion.md)
- [<span data-ttu-id="43c84-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="43c84-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
- [<span data-ttu-id="43c84-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="43c84-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

<span data-ttu-id="43c84-113">**GroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="43c84-113">**GroupAttendeeConflictData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="43c84-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="43c84-114">Attributes and elements</span></span>

<span data-ttu-id="43c84-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43c84-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43c84-116">属性</span><span class="sxs-lookup"><span data-stu-id="43c84-116">Attributes</span></span>

<span data-ttu-id="43c84-117">无。</span><span class="sxs-lookup"><span data-stu-id="43c84-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43c84-118">子元素</span><span class="sxs-lookup"><span data-stu-id="43c84-118">Child elements</span></span>

|<span data-ttu-id="43c84-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="43c84-119">**Element**</span></span>|<span data-ttu-id="43c84-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="43c84-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43c84-121">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="43c84-121">NumberOfMembers</span></span>](numberofmembers.md) <br/> |<span data-ttu-id="43c84-122">代表用户、 资源和通讯组列表中的聊天室的数量。</span><span class="sxs-lookup"><span data-stu-id="43c84-122">Represents the number of users, resources, and rooms in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="43c84-123">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="43c84-123">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md) <br/> |<span data-ttu-id="43c84-124">代表建议的会议的时间可用的通讯组列表成员的数量。</span><span class="sxs-lookup"><span data-stu-id="43c84-124">Represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="43c84-125">此元素表示为其状态是**免费**的成员。</span><span class="sxs-lookup"><span data-stu-id="43c84-125">This element represents members for whom the status is **Free**.</span></span>  <br/> |
|[<span data-ttu-id="43c84-126">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="43c84-126">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md) <br/> |<span data-ttu-id="43c84-127">代表拥有建议的会议时间冲突的通讯组列表成员的数量。</span><span class="sxs-lookup"><span data-stu-id="43c84-127">Represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="43c84-128">此元素表示具有**忙碌**、 **OOF**，或**暂定**状态的成员。</span><span class="sxs-lookup"><span data-stu-id="43c84-128">This element represents members who have a **Busy**, **OOF**, or **Tentative** status.</span></span>  <br/> |
|[<span data-ttu-id="43c84-129">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="43c84-129">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md) <br/> |<span data-ttu-id="43c84-130">表示没有已发布忙/闲数据到建议的会议的时间比较组成员的数目。</span><span class="sxs-lookup"><span data-stu-id="43c84-130">Represents the number of group members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="43c84-131">此元素表示太大通讯组列表的成员或拥有**无数据**状态的成员。</span><span class="sxs-lookup"><span data-stu-id="43c84-131">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="43c84-132">父元素</span><span class="sxs-lookup"><span data-stu-id="43c84-132">Parent elements</span></span>

|<span data-ttu-id="43c84-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="43c84-133">**Element**</span></span>|<span data-ttu-id="43c84-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="43c84-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43c84-135">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="43c84-135">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="43c84-136">包含标识[GetUserAvailability 操作](getuseravailability-operation.md)中的查询与会者冲突数据的数组。</span><span class="sxs-lookup"><span data-stu-id="43c84-136">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="43c84-137">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="43c84-137">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43c84-138">注解</span><span class="sxs-lookup"><span data-stu-id="43c84-138">Remarks</span></span>

<span data-ttu-id="43c84-139">[GetUserAvailabilityRequest](getuseravailabilityrequest.md)中的与会者解析为通讯组列表时，可以在响应中存在的**GroupAttendeeConflictData**元素。</span><span class="sxs-lookup"><span data-stu-id="43c84-139">The **GroupAttendeeConflictData** element is present in the response when an attendee in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) is resolved to a distribution list.</span></span> <span data-ttu-id="43c84-140">**GroupAttendeeConflictData**元素标识三种状态的通讯组列表的成员： 可用、 冲突，或没有数据。</span><span class="sxs-lookup"><span data-stu-id="43c84-140">The **GroupAttendeeConflictData** element identifies three states for members of a distribution list: available, conflicted, or no data.</span></span> <span data-ttu-id="43c84-141">通讯组列表扩展将支持多达 100 个成员。</span><span class="sxs-lookup"><span data-stu-id="43c84-141">Distribution list expansion will support up to 100 members.</span></span> <span data-ttu-id="43c84-142">因此， [NumberOfMembers](numberofmembers.md)元素可以包含 100 个成员的最大值。</span><span class="sxs-lookup"><span data-stu-id="43c84-142">Therefore, the [NumberOfMembers](numberofmembers.md) element can contain a maximum of 100 members.</span></span> <span data-ttu-id="43c84-143">通讯组列表扩展是递归。</span><span class="sxs-lookup"><span data-stu-id="43c84-143">Distribution list expansion is recursive.</span></span> <span data-ttu-id="43c84-144">如果通讯组列表中包含子通讯组列表扩展到超过 100 个成员的总父成员资格，子通讯组列表不会被展开，并将计数为一个条目的[NumberOfMembersWithNoData](numberofmemberswithnodata.md)元素计数。</span><span class="sxs-lookup"><span data-stu-id="43c84-144">If a distribution list contains a child distribution list that expands the total parent membership to over 100 members, the child distribution list will not be expanded and will count as a single entry of the [NumberOfMembersWithNoData](numberofmemberswithnodata.md) element count.</span></span> <span data-ttu-id="43c84-145">如果可以展开子通讯组列表，并且总父成员资格不会展开到超过 100 个成员，扩展其成员资格和成员计数添加到**GroupAttendeeConflictData**元素的子元素。</span><span class="sxs-lookup"><span data-stu-id="43c84-145">If a child distribution list can be expanded and the total parent membership does not expand to over 100 members, its membership is expanded and the member counts are added to the child elements of the **GroupAttendeeConflictData** element.</span></span> 
  
<span data-ttu-id="43c84-146">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="43c84-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43c84-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="43c84-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43c84-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="43c84-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43c84-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="43c84-149">Schema Name</span></span>  <br/> |<span data-ttu-id="43c84-150">类型架构</span><span class="sxs-lookup"><span data-stu-id="43c84-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="43c84-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="43c84-151">Validation File</span></span>  <br/> |<span data-ttu-id="43c84-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="43c84-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43c84-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="43c84-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="43c84-154">False</span><span class="sxs-lookup"><span data-stu-id="43c84-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43c84-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43c84-155">See also</span></span>

- [<span data-ttu-id="43c84-156">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="43c84-156">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="43c84-157">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="43c84-157">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="43c84-158">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="43c84-158">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

