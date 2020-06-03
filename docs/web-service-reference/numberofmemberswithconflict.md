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
description: NumberOfMembersWithConflict 元素表示与建议的会议时间有冲突的通讯组列表成员的数量。 此元素表示状态为 "忙碌"、"OOF" 或 "暂定" 的成员。
ms.openlocfilehash: 3ed81fc8adece140e8a94b08a9c2d94c2d9787c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529033"
---
# <a name="numberofmemberswithconflict"></a><span data-ttu-id="52b64-104">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="52b64-104">NumberOfMembersWithConflict</span></span>

<span data-ttu-id="52b64-105">**NumberOfMembersWithConflict**元素表示与建议的会议时间有冲突的通讯组列表成员的数量。</span><span class="sxs-lookup"><span data-stu-id="52b64-105">The **NumberOfMembersWithConflict** element represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="52b64-106">此元素表示状态为 "**忙碌**"、" **OOF**" 或 "**暂定**" 的成员。</span><span class="sxs-lookup"><span data-stu-id="52b64-106">This element represents members who have a status of **Busy**, **OOF**, or **Tentative**.</span></span>
  
[<span data-ttu-id="52b64-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="52b64-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="52b64-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="52b64-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="52b64-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="52b64-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="52b64-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="52b64-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="52b64-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="52b64-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="52b64-112">建议</span><span class="sxs-lookup"><span data-stu-id="52b64-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="52b64-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="52b64-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="52b64-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="52b64-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="52b64-115">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="52b64-115">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md)
  
```xml
<NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
```

 <span data-ttu-id="52b64-116">**int**</span><span class="sxs-lookup"><span data-stu-id="52b64-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52b64-117">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52b64-117">Attributes and elements</span></span>

<span data-ttu-id="52b64-118">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52b64-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52b64-119">Attributes</span><span class="sxs-lookup"><span data-stu-id="52b64-119">Attributes</span></span>

<span data-ttu-id="52b64-120">无。</span><span class="sxs-lookup"><span data-stu-id="52b64-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52b64-121">子元素</span><span class="sxs-lookup"><span data-stu-id="52b64-121">Child elements</span></span>

<span data-ttu-id="52b64-122">无。</span><span class="sxs-lookup"><span data-stu-id="52b64-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="52b64-123">父元素</span><span class="sxs-lookup"><span data-stu-id="52b64-123">Parent elements</span></span>

|<span data-ttu-id="52b64-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="52b64-124">**Element**</span></span>|<span data-ttu-id="52b64-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="52b64-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52b64-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="52b64-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="52b64-127">包含有关可用用户数的聚合冲突信息、有冲突的用户数以及在通讯组列表中没有可用性信息的用户数量建议的会议时间。</span><span class="sxs-lookup"><span data-stu-id="52b64-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="52b64-128">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="52b64-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52b64-129">说明</span><span class="sxs-lookup"><span data-stu-id="52b64-129">Remarks</span></span>

<span data-ttu-id="52b64-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52b64-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52b64-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="52b64-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52b64-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="52b64-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52b64-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="52b64-133">Schema Name</span></span>  <br/> |<span data-ttu-id="52b64-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="52b64-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="52b64-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="52b64-135">Validation File</span></span>  <br/> |<span data-ttu-id="52b64-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="52b64-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52b64-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="52b64-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="52b64-138">False</span><span class="sxs-lookup"><span data-stu-id="52b64-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52b64-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52b64-139">See also</span></span>



[<span data-ttu-id="52b64-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="52b64-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="52b64-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="52b64-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="52b64-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="52b64-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

