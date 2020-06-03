---
title: IndividualAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndividualAttendeeConflictData
api_type:
- schema
ms.assetid: d45d3c34-abe1-40da-afd3-23bc5c3ef474
description: IndividualAttendeeConflictData 元素包含用户或联系人的忙/闲状态，该时间窗口与建议元素中标识的建议会议时间同时发生。
ms.openlocfilehash: 55210230259b78e5ed9c4f0744aae003cf2e7ae5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459312"
---
# <a name="individualattendeeconflictdata"></a><span data-ttu-id="ada3c-103">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="ada3c-103">IndividualAttendeeConflictData</span></span>

<span data-ttu-id="ada3c-104">**IndividualAttendeeConflictData**元素包含用户或联系人的忙/闲状态，该时间窗口与[建议元素中标识的建议会议](suggestion.md)时间同时发生。</span><span class="sxs-lookup"><span data-stu-id="ada3c-104">The **IndividualAttendeeConflictData** element contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
[<span data-ttu-id="ada3c-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ada3c-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="ada3c-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="ada3c-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="ada3c-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="ada3c-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="ada3c-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="ada3c-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="ada3c-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="ada3c-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="ada3c-110">建议</span><span class="sxs-lookup"><span data-stu-id="ada3c-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="ada3c-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="ada3c-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="ada3c-112">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="ada3c-112">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md)
  
```xml
<IndividualAttendeeConflictData>
   <BusyType>...</BusyType>
</IndividualAttendeeConflictData>
```

 <span data-ttu-id="ada3c-113">**IndividualAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="ada3c-113">**IndividualAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ada3c-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ada3c-114">Attributes and elements</span></span>

<span data-ttu-id="ada3c-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ada3c-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ada3c-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="ada3c-116">Attributes</span></span>

<span data-ttu-id="ada3c-117">无。</span><span class="sxs-lookup"><span data-stu-id="ada3c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ada3c-118">子元素</span><span class="sxs-lookup"><span data-stu-id="ada3c-118">Child elements</span></span>

|<span data-ttu-id="ada3c-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="ada3c-119">**Element**</span></span>|<span data-ttu-id="ada3c-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="ada3c-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ada3c-121">BusyType</span><span class="sxs-lookup"><span data-stu-id="ada3c-121">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="ada3c-122">表示建议会议时间的用户的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="ada3c-122">Represents the free/busy status of a user for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ada3c-123">父元素</span><span class="sxs-lookup"><span data-stu-id="ada3c-123">Parent elements</span></span>

|<span data-ttu-id="ada3c-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="ada3c-124">**Element**</span></span>|<span data-ttu-id="ada3c-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="ada3c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ada3c-126">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="ada3c-126">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="ada3c-127">包含[GetUserAvailabilityRequest](getuseravailabilityrequest.md)中标识的与会者的冲突数据数组。</span><span class="sxs-lookup"><span data-stu-id="ada3c-127">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="ada3c-128">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="ada3c-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ada3c-129">说明</span><span class="sxs-lookup"><span data-stu-id="ada3c-129">Remarks</span></span>

<span data-ttu-id="ada3c-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ada3c-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ada3c-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="ada3c-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ada3c-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="ada3c-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ada3c-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="ada3c-133">Schema Name</span></span>  <br/> |<span data-ttu-id="ada3c-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="ada3c-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="ada3c-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="ada3c-135">Validation File</span></span>  <br/> |<span data-ttu-id="ada3c-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ada3c-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ada3c-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="ada3c-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="ada3c-138">False</span><span class="sxs-lookup"><span data-stu-id="ada3c-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ada3c-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ada3c-139">See also</span></span>



[<span data-ttu-id="ada3c-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="ada3c-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="ada3c-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="ada3c-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="ada3c-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="ada3c-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

