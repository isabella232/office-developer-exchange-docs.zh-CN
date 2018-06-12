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
description: IndividualAttendeeConflictData 元素包含用户的或建议元素中标识的建议的会议时间时将发生时间窗口的联系人的忙/闲状态。
ms.openlocfilehash: 0bd164e08a6f3685415452b7c82a4220cf69d792
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825930"
---
# <a name="individualattendeeconflictdata"></a><span data-ttu-id="dee70-103">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="dee70-103">IndividualAttendeeConflictData</span></span>

<span data-ttu-id="dee70-104">**IndividualAttendeeConflictData**元素包含用户的或[建议](suggestion.md)元素中标识的建议的会议时间时将发生时间窗口的联系人的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="dee70-104">The **IndividualAttendeeConflictData** element contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
[<span data-ttu-id="dee70-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dee70-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="dee70-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="dee70-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="dee70-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="dee70-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="dee70-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="dee70-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="dee70-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="dee70-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="dee70-110">建议</span><span class="sxs-lookup"><span data-stu-id="dee70-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="dee70-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="dee70-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="dee70-112">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="dee70-112">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md)
  
```xml
<IndividualAttendeeConflictData>
   <BusyType>...</BusyType>
</IndividualAttendeeConflictData>
```

 <span data-ttu-id="dee70-113">**IndividualAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="dee70-113">**IndividualAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dee70-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dee70-114">Attributes and elements</span></span>

<span data-ttu-id="dee70-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dee70-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dee70-116">属性</span><span class="sxs-lookup"><span data-stu-id="dee70-116">Attributes</span></span>

<span data-ttu-id="dee70-117">无。</span><span class="sxs-lookup"><span data-stu-id="dee70-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dee70-118">子元素</span><span class="sxs-lookup"><span data-stu-id="dee70-118">Child elements</span></span>

|<span data-ttu-id="dee70-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="dee70-119">**Element**</span></span>|<span data-ttu-id="dee70-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="dee70-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dee70-121">BusyType</span><span class="sxs-lookup"><span data-stu-id="dee70-121">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="dee70-122">建议的会议的时间表示用户的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="dee70-122">Represents the free/busy status of a user for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dee70-123">父元素</span><span class="sxs-lookup"><span data-stu-id="dee70-123">Parent elements</span></span>

|<span data-ttu-id="dee70-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="dee70-124">**Element**</span></span>|<span data-ttu-id="dee70-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="dee70-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dee70-126">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="dee70-126">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="dee70-127">与会者[GetUserAvailabilityRequest](getuseravailabilityrequest.md)中标识为包含数组的冲突数据。</span><span class="sxs-lookup"><span data-stu-id="dee70-127">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="dee70-128">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="dee70-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dee70-129">备注</span><span class="sxs-lookup"><span data-stu-id="dee70-129">Remarks</span></span>

<span data-ttu-id="dee70-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dee70-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dee70-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="dee70-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dee70-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="dee70-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dee70-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="dee70-133">Schema Name</span></span>  <br/> |<span data-ttu-id="dee70-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="dee70-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="dee70-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="dee70-135">Validation File</span></span>  <br/> |<span data-ttu-id="dee70-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dee70-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dee70-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="dee70-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="dee70-138">False</span><span class="sxs-lookup"><span data-stu-id="dee70-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dee70-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dee70-139">See also</span></span>



[<span data-ttu-id="dee70-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="dee70-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="dee70-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dee70-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="dee70-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="dee70-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

