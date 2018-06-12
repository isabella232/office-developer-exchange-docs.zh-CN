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
description: UnknownAttendeeConflictData 元素均表示无法解析与会者或与会者不是用户、 通讯组列表或联系人。
ms.openlocfilehash: 2363e243a833f580b4b5701b7d39d9ba9420f35a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838336"
---
# <a name="unknownattendeeconflictdata"></a><span data-ttu-id="f744f-103">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="f744f-103">UnknownAttendeeConflictData</span></span>

<span data-ttu-id="f744f-104">**UnknownAttendeeConflictData**元素均表示无法解析与会者或与会者不是用户、 通讯组列表或联系人。</span><span class="sxs-lookup"><span data-stu-id="f744f-104">The **UnknownAttendeeConflictData** element represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span> 
  
[<span data-ttu-id="f744f-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f744f-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="f744f-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="f744f-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="f744f-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="f744f-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="f744f-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="f744f-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="f744f-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="f744f-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="f744f-110">建议</span><span class="sxs-lookup"><span data-stu-id="f744f-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="f744f-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="f744f-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="f744f-112">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="f744f-112">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md)
  
```xml
<UnknownAttendeeConflictData/>
```

 <span data-ttu-id="f744f-113">**UnknownAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="f744f-113">**UnknownAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f744f-114">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f744f-114">Attributes and elements</span></span>

<span data-ttu-id="f744f-115">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f744f-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f744f-116">属性</span><span class="sxs-lookup"><span data-stu-id="f744f-116">Attributes</span></span>

<span data-ttu-id="f744f-117">无。</span><span class="sxs-lookup"><span data-stu-id="f744f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f744f-118">子元素</span><span class="sxs-lookup"><span data-stu-id="f744f-118">Child elements</span></span>

<span data-ttu-id="f744f-119">无。</span><span class="sxs-lookup"><span data-stu-id="f744f-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f744f-120">父元素</span><span class="sxs-lookup"><span data-stu-id="f744f-120">Parent elements</span></span>

|<span data-ttu-id="f744f-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="f744f-121">**Element**</span></span>|<span data-ttu-id="f744f-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="f744f-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f744f-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="f744f-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="f744f-124">包含标识[GetUserAvailability 操作](getuseravailability-operation.md)中的查询与会者冲突数据的数组。</span><span class="sxs-lookup"><span data-stu-id="f744f-124">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="f744f-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="f744f-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f744f-126">备注</span><span class="sxs-lookup"><span data-stu-id="f744f-126">Remarks</span></span>

<span data-ttu-id="f744f-127">Attendee 是未知的如果它无法解析对 Active Directory 目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="f744f-127">An attendee is unknown if it cannot be resolved against an Active Directory directory service object.</span></span> <span data-ttu-id="f744f-128">如果无法确定为用户、 组或联系人与会者无法解析。</span><span class="sxs-lookup"><span data-stu-id="f744f-128">An attendee is unresolved if it cannot be determined to be a user, group, or contact.</span></span> <span data-ttu-id="f744f-129">例如，与会者不会解析是否已启用邮件的公用文件夹。</span><span class="sxs-lookup"><span data-stu-id="f744f-129">For example, an attendee will not be resolved if it is a mail-enabled public folder.</span></span>
  
<span data-ttu-id="f744f-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f744f-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f744f-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="f744f-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f744f-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="f744f-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f744f-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="f744f-133">Schema Name</span></span>  <br/> |<span data-ttu-id="f744f-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="f744f-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="f744f-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="f744f-135">Validation File</span></span>  <br/> |<span data-ttu-id="f744f-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f744f-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f744f-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="f744f-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="f744f-138">False</span><span class="sxs-lookup"><span data-stu-id="f744f-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f744f-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f744f-139">See also</span></span>



[<span data-ttu-id="f744f-140">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="f744f-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="f744f-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f744f-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="f744f-142">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="f744f-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

