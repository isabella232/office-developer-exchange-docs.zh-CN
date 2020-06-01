---
title: TooBigGroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TooBigGroupAttendeeConflictData
api_type:
- schema
ms.assetid: 1512428d-ce22-4da9-b1c1-446b4bcd0a21
description: TooBigGroupAttendeeConflictData 元素表示作为通讯组列表解析但通讯组列表太大而无法展开的与会者。
ms.openlocfilehash: 407a4a49e5f32c81439063f47df2e131dd663a4f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468598"
---
# <a name="toobiggroupattendeeconflictdata"></a><span data-ttu-id="4d267-103">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="4d267-103">TooBigGroupAttendeeConflictData</span></span>

<span data-ttu-id="4d267-104">**TooBigGroupAttendeeConflictData**元素表示作为通讯组列表解析但通讯组列表太大而无法展开的与会者。</span><span class="sxs-lookup"><span data-stu-id="4d267-104">The **TooBigGroupAttendeeConflictData** element represents an attendee that was resolved as a distribution list but the distribution list was too large to expand.</span></span> 
  
[<span data-ttu-id="4d267-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4d267-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="4d267-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="4d267-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="4d267-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="4d267-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="4d267-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="4d267-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="4d267-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="4d267-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="4d267-110">建议</span><span class="sxs-lookup"><span data-stu-id="4d267-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="4d267-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="4d267-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="4d267-112">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="4d267-112">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md)
  
```xml
<TooBigGroupAttendeeConflictData/>
```

 <span data-ttu-id="4d267-113">**TooBigGroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="4d267-113">**TooBigGroupAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4d267-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4d267-114">Attributes and elements</span></span>

<span data-ttu-id="4d267-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4d267-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d267-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="4d267-116">Attributes</span></span>

<span data-ttu-id="4d267-117">无。</span><span class="sxs-lookup"><span data-stu-id="4d267-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4d267-118">子元素</span><span class="sxs-lookup"><span data-stu-id="4d267-118">Child elements</span></span>

<span data-ttu-id="4d267-119">无。</span><span class="sxs-lookup"><span data-stu-id="4d267-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4d267-120">父元素</span><span class="sxs-lookup"><span data-stu-id="4d267-120">Parent elements</span></span>

|<span data-ttu-id="4d267-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="4d267-121">**Element**</span></span>|<span data-ttu-id="4d267-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="4d267-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4d267-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="4d267-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="4d267-124">包含[GetUserAvailabilityRequest](getuseravailabilityrequest.md)中标识的与会者的冲突数据数组。</span><span class="sxs-lookup"><span data-stu-id="4d267-124">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="4d267-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="4d267-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d267-126">备注</span><span class="sxs-lookup"><span data-stu-id="4d267-126">Remarks</span></span>

<span data-ttu-id="4d267-127">包含超过100个成员的通讯组列表无法展开。</span><span class="sxs-lookup"><span data-stu-id="4d267-127">Distribution lists that contain more than 100 members cannot be expanded.</span></span>
  
<span data-ttu-id="4d267-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4d267-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d267-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="4d267-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d267-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="4d267-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4d267-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="4d267-131">Schema Name</span></span>  <br/> |<span data-ttu-id="4d267-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="4d267-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="4d267-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="4d267-133">Validation File</span></span>  <br/> |<span data-ttu-id="4d267-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4d267-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4d267-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="4d267-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="4d267-136">False</span><span class="sxs-lookup"><span data-stu-id="4d267-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d267-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4d267-137">See also</span></span>



[<span data-ttu-id="4d267-138">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="4d267-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="4d267-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="4d267-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="4d267-140">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="4d267-140">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

