---
title: BusyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BusyType
api_type:
- schema
ms.assetid: 26d4fae0-8c78-4705-b5e8-d6033712c41e
description: BusyType 元素表示为日历事件设置忙/闲状态。
ms.openlocfilehash: 6484bc70c6a05084e5d2bc1738b575fbebe4c132
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753403"
---
# <a name="busytype"></a><span data-ttu-id="8d1b0-103">BusyType</span><span class="sxs-lookup"><span data-stu-id="8d1b0-103">BusyType</span></span>

<span data-ttu-id="8d1b0-104">**BusyType**元素表示为日历事件设置忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-104">The **BusyType** element represents the free/busy status set for a calendar event.</span></span> 
  
```xml
<BusyType>Free or Tentative or Busy or OOF or NoData</BusyType>
```

 <span data-ttu-id="8d1b0-105">**BusyType**</span><span class="sxs-lookup"><span data-stu-id="8d1b0-105">**BusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d1b0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8d1b0-106">Attributes and elements</span></span>

<span data-ttu-id="8d1b0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d1b0-108">属性</span><span class="sxs-lookup"><span data-stu-id="8d1b0-108">Attributes</span></span>

<span data-ttu-id="8d1b0-109">无。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d1b0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8d1b0-110">Child elements</span></span>

<span data-ttu-id="8d1b0-111">无。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d1b0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8d1b0-112">Parent elements</span></span>

|<span data-ttu-id="8d1b0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8d1b0-113">**Element**</span></span>|<span data-ttu-id="8d1b0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8d1b0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d1b0-115">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="8d1b0-115">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="8d1b0-116">包含用户或联系人的忙/闲信息建议的会议时间时将发生时间窗口的状态。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-116">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time.</span></span>  <br/> <span data-ttu-id="8d1b0-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="8d1b0-117">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/IndividualAttendeeConflictData` <br/> |
|[<span data-ttu-id="8d1b0-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="8d1b0-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="8d1b0-119">代表独特的日历项匹配项。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-119">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="8d1b0-120">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="8d1b0-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d1b0-121">文本值</span><span class="sxs-lookup"><span data-stu-id="8d1b0-121">Text value</span></span>

<span data-ttu-id="8d1b0-122">需要为此元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-122">A text value is required for this element.</span></span> <span data-ttu-id="8d1b0-123">值为 string 类型。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-123">The value is a string type.</span></span> <span data-ttu-id="8d1b0-124">[BusyType](busytype.md)元素的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="8d1b0-124">The following are the possible values for the [BusyType](busytype.md) element:</span></span> 
  
- <span data-ttu-id="8d1b0-125">免费</span><span class="sxs-lookup"><span data-stu-id="8d1b0-125">Free</span></span>
    
- <span data-ttu-id="8d1b0-126">暂定</span><span class="sxs-lookup"><span data-stu-id="8d1b0-126">Tentative</span></span>
    
- <span data-ttu-id="8d1b0-127">忙碌</span><span class="sxs-lookup"><span data-stu-id="8d1b0-127">Busy</span></span>
    
- <span data-ttu-id="8d1b0-128">OOF</span><span class="sxs-lookup"><span data-stu-id="8d1b0-128">OOF</span></span>
    
- <span data-ttu-id="8d1b0-129">NoData</span><span class="sxs-lookup"><span data-stu-id="8d1b0-129">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8d1b0-130">备注</span><span class="sxs-lookup"><span data-stu-id="8d1b0-130">Remarks</span></span>

<span data-ttu-id="8d1b0-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8d1b0-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d1b0-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="8d1b0-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d1b0-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="8d1b0-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d1b0-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="8d1b0-134">Schema Name</span></span>  <br/> |<span data-ttu-id="8d1b0-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="8d1b0-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d1b0-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="8d1b0-136">Validation File</span></span>  <br/> |<span data-ttu-id="8d1b0-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d1b0-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d1b0-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="8d1b0-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="8d1b0-139">False</span><span class="sxs-lookup"><span data-stu-id="8d1b0-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d1b0-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8d1b0-140">See also</span></span>



[<span data-ttu-id="8d1b0-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="8d1b0-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="8d1b0-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="8d1b0-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="8d1b0-143">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="8d1b0-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

