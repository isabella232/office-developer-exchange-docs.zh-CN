---
title: UnknownAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownAttendeeConflictData
api_type:
- schema
ms.assetid: 70e41268-c231-4587-9d23-e46927fe5272
description: UnknownAttendeeConflictData 元素表示不能解析的与会者或不是用户、通讯组列表或联系人的与会者。
ms.openlocfilehash: b4362e0117e3939c21342a1ab8079d95512aec79
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459866"
---
# <a name="unknownattendeeconflictdata"></a><span data-ttu-id="0141c-103">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="0141c-103">UnknownAttendeeConflictData</span></span>

<span data-ttu-id="0141c-104">**UnknownAttendeeConflictData**元素表示不能解析的与会者或不是用户、通讯组列表或联系人的与会者。</span><span class="sxs-lookup"><span data-stu-id="0141c-104">The **UnknownAttendeeConflictData** element represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span> 
  
[<span data-ttu-id="0141c-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="0141c-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="0141c-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="0141c-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="0141c-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="0141c-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="0141c-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="0141c-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="0141c-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="0141c-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="0141c-110">建议</span><span class="sxs-lookup"><span data-stu-id="0141c-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="0141c-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="0141c-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="0141c-112">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="0141c-112">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md)
  
```xml
<UnknownAttendeeConflictData/>
```

 <span data-ttu-id="0141c-113">**UnknownAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="0141c-113">**UnknownAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0141c-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0141c-114">Attributes and elements</span></span>

<span data-ttu-id="0141c-115">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0141c-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0141c-116">Attributes</span><span class="sxs-lookup"><span data-stu-id="0141c-116">Attributes</span></span>

<span data-ttu-id="0141c-117">无。</span><span class="sxs-lookup"><span data-stu-id="0141c-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0141c-118">子元素</span><span class="sxs-lookup"><span data-stu-id="0141c-118">Child elements</span></span>

<span data-ttu-id="0141c-119">无。</span><span class="sxs-lookup"><span data-stu-id="0141c-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0141c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="0141c-120">Parent elements</span></span>

|<span data-ttu-id="0141c-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="0141c-121">**Element**</span></span>|<span data-ttu-id="0141c-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="0141c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0141c-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="0141c-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="0141c-124">包含在[GetUserAvailability 操作](getuseravailability-operation.md)中标识的被查询的与会者的冲突数据数组。</span><span class="sxs-lookup"><span data-stu-id="0141c-124">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="0141c-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="0141c-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0141c-126">备注</span><span class="sxs-lookup"><span data-stu-id="0141c-126">Remarks</span></span>

<span data-ttu-id="0141c-127">如果某个与会者无法针对 Active Directory 目录服务对象进行解析，则该与会者是未知的。</span><span class="sxs-lookup"><span data-stu-id="0141c-127">An attendee is unknown if it cannot be resolved against an Active Directory directory service object.</span></span> <span data-ttu-id="0141c-128">如果与会者无法确定为用户、组或联系人，则无法解析该与会者。</span><span class="sxs-lookup"><span data-stu-id="0141c-128">An attendee is unresolved if it cannot be determined to be a user, group, or contact.</span></span> <span data-ttu-id="0141c-129">例如，如果某个与会者是已启用邮件的公用文件夹，则不会对其进行解析。</span><span class="sxs-lookup"><span data-stu-id="0141c-129">For example, an attendee will not be resolved if it is a mail-enabled public folder.</span></span>
  
<span data-ttu-id="0141c-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0141c-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0141c-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="0141c-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0141c-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="0141c-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0141c-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="0141c-133">Schema Name</span></span>  <br/> |<span data-ttu-id="0141c-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="0141c-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="0141c-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="0141c-135">Validation File</span></span>  <br/> |<span data-ttu-id="0141c-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0141c-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0141c-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="0141c-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="0141c-138">False</span><span class="sxs-lookup"><span data-stu-id="0141c-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0141c-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0141c-139">See also</span></span>



[<span data-ttu-id="0141c-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="0141c-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="0141c-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="0141c-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="0141c-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="0141c-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

