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
description: AttendeeConflictDataArray 元素包含在 GetUserAvailability 操作中标识的被查询的与会者的冲突数据数组。
ms.openlocfilehash: 770e8c00ca248ec3562180dc9d3626fd5b58f4d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455798"
---
# <a name="attendeeconflictdataarray"></a><span data-ttu-id="62a78-103">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="62a78-103">AttendeeConflictDataArray</span></span>

<span data-ttu-id="62a78-104">**AttendeeConflictDataArray**元素包含在[GetUserAvailability 操作](getuseravailability-operation.md)中标识的被查询的与会者的冲突数据数组。</span><span class="sxs-lookup"><span data-stu-id="62a78-104">The **AttendeeConflictDataArray** element contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>
  
- [<span data-ttu-id="62a78-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="62a78-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="62a78-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="62a78-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
- [<span data-ttu-id="62a78-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="62a78-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
- [<span data-ttu-id="62a78-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="62a78-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
- [<span data-ttu-id="62a78-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="62a78-109">SuggestionArray</span></span>](suggestionarray.md)
  
- [<span data-ttu-id="62a78-110">建议</span><span class="sxs-lookup"><span data-stu-id="62a78-110">Suggestion</span></span>](suggestion.md)
  
- [<span data-ttu-id="62a78-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="62a78-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 <span data-ttu-id="62a78-112">**ArrayOfAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="62a78-112">**ArrayOfAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="62a78-113">属性和元素</span><span class="sxs-lookup"><span data-stu-id="62a78-113">Attributes and elements</span></span>

<span data-ttu-id="62a78-114">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="62a78-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62a78-115">Attributes</span><span class="sxs-lookup"><span data-stu-id="62a78-115">Attributes</span></span>

<span data-ttu-id="62a78-116">无。</span><span class="sxs-lookup"><span data-stu-id="62a78-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="62a78-117">子元素</span><span class="sxs-lookup"><span data-stu-id="62a78-117">Child elements</span></span>

|<span data-ttu-id="62a78-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="62a78-118">**Element**</span></span>|<span data-ttu-id="62a78-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="62a78-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62a78-120">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="62a78-120">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md) <br/> |<span data-ttu-id="62a78-121">代表不能解析的与会者或不是用户、通讯组列表或联系人的与会者。</span><span class="sxs-lookup"><span data-stu-id="62a78-121">Represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span>  <br/> |
|[<span data-ttu-id="62a78-122">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="62a78-122">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="62a78-123">包含与[建议](suggestion.md)元素中标识的建议会议时间同时发生的时间窗口的用户或联系人的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="62a78-123">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span>  <br/> |
|[<span data-ttu-id="62a78-124">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="62a78-124">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md) <br/> |<span data-ttu-id="62a78-125">表示解析为过大而无法展开的通讯组列表的与会者。</span><span class="sxs-lookup"><span data-stu-id="62a78-125">Represents an attendee that resolved as a distribution list that was too large to expand.</span></span>  <br/> |
|[<span data-ttu-id="62a78-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="62a78-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="62a78-127">包含有关可用用户数、有冲突的用户数以及在通讯组列表中没有可用性信息的用户数的聚合冲突信息，以获取建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="62a78-127">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="62a78-128">父元素</span><span class="sxs-lookup"><span data-stu-id="62a78-128">Parent elements</span></span>

|<span data-ttu-id="62a78-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="62a78-129">**Element**</span></span>|<span data-ttu-id="62a78-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="62a78-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="62a78-131">建议</span><span class="sxs-lookup"><span data-stu-id="62a78-131">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="62a78-132">表示单个会议时间建议。</span><span class="sxs-lookup"><span data-stu-id="62a78-132">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="62a78-133">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="62a78-133">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62a78-134">备注</span><span class="sxs-lookup"><span data-stu-id="62a78-134">Remarks</span></span>

<span data-ttu-id="62a78-135">**AttendeeConflictDataArray**中的每个元素的位置对应于[MailboxDataArray](mailboxdataarray.md)元素中被查询的与会者的位置。</span><span class="sxs-lookup"><span data-stu-id="62a78-135">The position of each element in the **AttendeeConflictDataArray** corresponds to the position of the queried attendees in the [MailboxDataArray](mailboxdataarray.md) element.</span></span> <span data-ttu-id="62a78-136">每个被查询的与会者都必须与**AttendeeConflictDataArray**子元素之一相对应。</span><span class="sxs-lookup"><span data-stu-id="62a78-136">Each queried attendee must correspond to one of the **AttendeeConflictDataArray** child elements.</span></span> <span data-ttu-id="62a78-137">这些元素表示与[建议元素中所标识](suggestion.md)的建议会议时间的单个冲突。</span><span class="sxs-lookup"><span data-stu-id="62a78-137">These elements represent a single conflict with the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="62a78-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="62a78-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62a78-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="62a78-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62a78-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="62a78-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="62a78-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="62a78-141">Schema Name</span></span>  <br/> |<span data-ttu-id="62a78-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="62a78-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="62a78-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="62a78-143">Validation File</span></span>  <br/> |<span data-ttu-id="62a78-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="62a78-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="62a78-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="62a78-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="62a78-146">False</span><span class="sxs-lookup"><span data-stu-id="62a78-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62a78-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="62a78-147">See also</span></span>

- [<span data-ttu-id="62a78-148">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="62a78-148">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="62a78-149">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="62a78-149">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="62a78-150">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="62a78-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

