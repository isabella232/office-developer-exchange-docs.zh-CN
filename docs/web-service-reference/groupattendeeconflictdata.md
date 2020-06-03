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
description: GroupAttendeeConflictData 元素包含有关可用用户数的聚合冲突信息、有冲突的用户数以及在通讯组列表中没有可用性信息的用户数，以获取建议的会议时间。
ms.openlocfilehash: c75a4e6f8fdff7fb2514f448350fee9f1acb9775
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462927"
---
# <a name="groupattendeeconflictdata"></a><span data-ttu-id="64771-103">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="64771-103">GroupAttendeeConflictData</span></span>

<span data-ttu-id="64771-104">**GroupAttendeeConflictData**元素包含有关可用用户数的聚合冲突信息、有冲突的用户数以及在通讯组列表中没有可用性信息的用户数，以获取建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="64771-104">The **GroupAttendeeConflictData** element contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span> 
  
- [<span data-ttu-id="64771-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="64771-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="64771-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="64771-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
- [<span data-ttu-id="64771-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="64771-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
- [<span data-ttu-id="64771-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="64771-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
- [<span data-ttu-id="64771-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="64771-109">SuggestionArray</span></span>](suggestionarray.md)
- [<span data-ttu-id="64771-110">建议</span><span class="sxs-lookup"><span data-stu-id="64771-110">Suggestion</span></span>](suggestion.md)
- [<span data-ttu-id="64771-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="64771-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
- [<span data-ttu-id="64771-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="64771-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

<span data-ttu-id="64771-113">**GroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="64771-113">**GroupAttendeeConflictData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="64771-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="64771-114">Attributes and elements</span></span>

<span data-ttu-id="64771-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="64771-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64771-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="64771-116">Attributes</span></span>

<span data-ttu-id="64771-117">无。</span><span class="sxs-lookup"><span data-stu-id="64771-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64771-118">子元素</span><span class="sxs-lookup"><span data-stu-id="64771-118">Child elements</span></span>

|<span data-ttu-id="64771-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="64771-119">**Element**</span></span>|<span data-ttu-id="64771-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="64771-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64771-121">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="64771-121">NumberOfMembers</span></span>](numberofmembers.md) <br/> |<span data-ttu-id="64771-122">表示通讯组列表中的用户、资源和会议室的数量。</span><span class="sxs-lookup"><span data-stu-id="64771-122">Represents the number of users, resources, and rooms in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="64771-123">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="64771-123">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md) <br/> |<span data-ttu-id="64771-124">表示可用于建议会议时间的通讯组列表成员的数量。</span><span class="sxs-lookup"><span data-stu-id="64771-124">Represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="64771-125">此元素表示其状态为 "**空闲**" 的成员。</span><span class="sxs-lookup"><span data-stu-id="64771-125">This element represents members for whom the status is **Free**.</span></span>  <br/> |
|[<span data-ttu-id="64771-126">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="64771-126">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md) <br/> |<span data-ttu-id="64771-127">表示与建议的会议时间有冲突的通讯组列表成员的数量。</span><span class="sxs-lookup"><span data-stu-id="64771-127">Represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="64771-128">此元素表示具有 "**忙碌**"、" **OOF**" 或 "**暂定**" 状态的成员。</span><span class="sxs-lookup"><span data-stu-id="64771-128">This element represents members who have a **Busy**, **OOF**, or **Tentative** status.</span></span>  <br/> |
|[<span data-ttu-id="64771-129">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="64771-129">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md) <br/> |<span data-ttu-id="64771-130">表示没有发布的忙/闲数据以与建议的会议时间进行比较的组成员的数量。</span><span class="sxs-lookup"><span data-stu-id="64771-130">Represents the number of group members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="64771-131">此元素表示通讯组列表的成员过大或没有**数据**状态的成员。</span><span class="sxs-lookup"><span data-stu-id="64771-131">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="64771-132">父元素</span><span class="sxs-lookup"><span data-stu-id="64771-132">Parent elements</span></span>

|<span data-ttu-id="64771-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="64771-133">**Element**</span></span>|<span data-ttu-id="64771-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="64771-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64771-135">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="64771-135">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="64771-136">包含在[GetUserAvailability 操作](getuseravailability-operation.md)中标识的被查询的与会者的冲突数据数组。</span><span class="sxs-lookup"><span data-stu-id="64771-136">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="64771-137">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="64771-137">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64771-138">备注</span><span class="sxs-lookup"><span data-stu-id="64771-138">Remarks</span></span>

<span data-ttu-id="64771-139">将[GetUserAvailabilityRequest](getuseravailabilityrequest.md)中的与会者解析为通讯组列表时，响应中存在**GroupAttendeeConflictData**元素。</span><span class="sxs-lookup"><span data-stu-id="64771-139">The **GroupAttendeeConflictData** element is present in the response when an attendee in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) is resolved to a distribution list.</span></span> <span data-ttu-id="64771-140">**GroupAttendeeConflictData**元素标识通讯组列表成员的三种状态：可用、冲突或无数据。</span><span class="sxs-lookup"><span data-stu-id="64771-140">The **GroupAttendeeConflictData** element identifies three states for members of a distribution list: available, conflicted, or no data.</span></span> <span data-ttu-id="64771-141">通讯组列表扩展将最长支持100个成员。</span><span class="sxs-lookup"><span data-stu-id="64771-141">Distribution list expansion will support up to 100 members.</span></span> <span data-ttu-id="64771-142">因此， [NumberOfMembers](numberofmembers.md)元素最多可包含100个成员。</span><span class="sxs-lookup"><span data-stu-id="64771-142">Therefore, the [NumberOfMembers](numberofmembers.md) element can contain a maximum of 100 members.</span></span> <span data-ttu-id="64771-143">通讯组列表展开是递归的。</span><span class="sxs-lookup"><span data-stu-id="64771-143">Distribution list expansion is recursive.</span></span> <span data-ttu-id="64771-144">如果通讯组列表包含将总父成员资格扩展到超过100个成员的子通讯组列表，则子通讯组列表将不会展开，并将作为[NumberOfMembersWithNoData](numberofmemberswithnodata.md)元素计数的单个条目进行计数。</span><span class="sxs-lookup"><span data-stu-id="64771-144">If a distribution list contains a child distribution list that expands the total parent membership to over 100 members, the child distribution list will not be expanded and will count as a single entry of the [NumberOfMembersWithNoData](numberofmemberswithnodata.md) element count.</span></span> <span data-ttu-id="64771-145">如果可以扩展子通讯组列表，并且总父成员资格不会扩展到超过100个成员，则将展开其成员资格，并将成员计数添加到**GroupAttendeeConflictData**元素的子元素中。</span><span class="sxs-lookup"><span data-stu-id="64771-145">If a child distribution list can be expanded and the total parent membership does not expand to over 100 members, its membership is expanded and the member counts are added to the child elements of the **GroupAttendeeConflictData** element.</span></span> 
  
<span data-ttu-id="64771-146">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="64771-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64771-147">元素信息</span><span class="sxs-lookup"><span data-stu-id="64771-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64771-148">命名空间</span><span class="sxs-lookup"><span data-stu-id="64771-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="64771-149">架构名称</span><span class="sxs-lookup"><span data-stu-id="64771-149">Schema Name</span></span>  <br/> |<span data-ttu-id="64771-150">类型架构</span><span class="sxs-lookup"><span data-stu-id="64771-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="64771-151">验证文件</span><span class="sxs-lookup"><span data-stu-id="64771-151">Validation File</span></span>  <br/> |<span data-ttu-id="64771-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="64771-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="64771-153">可以为空</span><span class="sxs-lookup"><span data-stu-id="64771-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="64771-154">False</span><span class="sxs-lookup"><span data-stu-id="64771-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64771-155">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64771-155">See also</span></span>

- [<span data-ttu-id="64771-156">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="64771-156">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="64771-157">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="64771-157">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="64771-158">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="64771-158">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

