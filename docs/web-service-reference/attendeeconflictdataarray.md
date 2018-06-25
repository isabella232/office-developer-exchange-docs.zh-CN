---
title: AttendeeConflictDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeConflictDataArray
api_type:
- schema
ms.assetid: 1d758547-28c5-4649-8334-427480c282d6
description: AttendeeConflictDataArray 元素包含标识 GetUserAvailability 操作中的查询与会者冲突数据的数组。
ms.openlocfilehash: 169312b8a3d37c014ba58fbfe094d786b134fc90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753285"
---
# <a name="attendeeconflictdataarray"></a><span data-ttu-id="86051-103">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="86051-103">AttendeeConflictDataArray</span></span>

<span data-ttu-id="86051-104">**AttendeeConflictDataArray**元素包含标识[GetUserAvailability 操作](getuseravailability-operation.md)中的查询与会者冲突数据的数组。</span><span class="sxs-lookup"><span data-stu-id="86051-104">The **AttendeeConflictDataArray** element contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>
  
- [<span data-ttu-id="86051-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="86051-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="86051-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="86051-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
- [<span data-ttu-id="86051-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="86051-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
- [<span data-ttu-id="86051-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="86051-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
- [<span data-ttu-id="86051-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="86051-109">SuggestionArray</span></span>](suggestionarray.md)
  
- [<span data-ttu-id="86051-110">建议</span><span class="sxs-lookup"><span data-stu-id="86051-110">Suggestion</span></span>](suggestion.md)
  
- [<span data-ttu-id="86051-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="86051-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 <span data-ttu-id="86051-112">**ArrayOfAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="86051-112">**ArrayOfAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="86051-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="86051-113">Attributes and elements</span></span>

<span data-ttu-id="86051-114">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="86051-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86051-115">属性</span><span class="sxs-lookup"><span data-stu-id="86051-115">Attributes</span></span>

<span data-ttu-id="86051-116">无。</span><span class="sxs-lookup"><span data-stu-id="86051-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86051-117">子元素</span><span class="sxs-lookup"><span data-stu-id="86051-117">Child elements</span></span>

|<span data-ttu-id="86051-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="86051-118">**Element**</span></span>|<span data-ttu-id="86051-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="86051-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86051-120">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="86051-120">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md) <br/> |<span data-ttu-id="86051-121">表示无法解决 attendee 或与会者不是用户、 通讯组列表或联系人。</span><span class="sxs-lookup"><span data-stu-id="86051-121">Represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span>  <br/> |
|[<span data-ttu-id="86051-122">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="86051-122">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="86051-123">包含用户或联系人的忙/闲状态为建议同时发生时间窗口会议[建议](suggestion.md)元素中标识的时间。</span><span class="sxs-lookup"><span data-stu-id="86051-123">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span>  <br/> |
|[<span data-ttu-id="86051-124">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="86051-124">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md) <br/> |<span data-ttu-id="86051-125">代表解析为太大，展开通讯组列表成为与会者。</span><span class="sxs-lookup"><span data-stu-id="86051-125">Represents an attendee that resolved as a distribution list that was too large to expand.</span></span>  <br/> |
|[<span data-ttu-id="86051-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="86051-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="86051-127">包含有关可用的用户数、 用户拥有冲突，数和不具有可用性信息通讯组列表中建议的会议时间的用户数的聚合冲突信息。</span><span class="sxs-lookup"><span data-stu-id="86051-127">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86051-128">父元素</span><span class="sxs-lookup"><span data-stu-id="86051-128">Parent elements</span></span>

|<span data-ttu-id="86051-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="86051-129">**Element**</span></span>|<span data-ttu-id="86051-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="86051-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86051-131">建议</span><span class="sxs-lookup"><span data-stu-id="86051-131">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="86051-132">代表单个会议时间建议。</span><span class="sxs-lookup"><span data-stu-id="86051-132">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="86051-133">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="86051-133">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86051-134">注解</span><span class="sxs-lookup"><span data-stu-id="86051-134">Remarks</span></span>

<span data-ttu-id="86051-135">每个元素的位置以**AttendeeConflictDataArray**对应于查询与会者[MailboxDataArray](mailboxdataarray.md)元素中的位置。</span><span class="sxs-lookup"><span data-stu-id="86051-135">The position of each element in the **AttendeeConflictDataArray** corresponds to the position of the queried attendees in the [MailboxDataArray](mailboxdataarray.md) element.</span></span> <span data-ttu-id="86051-136">每个查询的与会者必须对应于一个**AttendeeConflictDataArray**子元素。</span><span class="sxs-lookup"><span data-stu-id="86051-136">Each queried attendee must correspond to one of the **AttendeeConflictDataArray** child elements.</span></span> <span data-ttu-id="86051-137">与[建议](suggestion.md)元素中标识的建议的会议时间，这些元素表示单个冲突。</span><span class="sxs-lookup"><span data-stu-id="86051-137">These elements represent a single conflict with the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="86051-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="86051-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86051-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="86051-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86051-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="86051-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="86051-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="86051-141">Schema Name</span></span>  <br/> |<span data-ttu-id="86051-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="86051-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="86051-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="86051-143">Validation File</span></span>  <br/> |<span data-ttu-id="86051-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="86051-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="86051-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="86051-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="86051-146">False</span><span class="sxs-lookup"><span data-stu-id="86051-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86051-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="86051-147">See also</span></span>

- [<span data-ttu-id="86051-148">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="86051-148">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="86051-149">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="86051-149">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="86051-150">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="86051-150">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

