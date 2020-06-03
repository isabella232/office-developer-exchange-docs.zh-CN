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
description: BusyType 元素表示为日历事件设置的忙/闲状态。
ms.openlocfilehash: 7c2d18c21156a8603d3caeeb796a56c5d8afcba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459081"
---
# <a name="busytype"></a><span data-ttu-id="623d2-103">BusyType</span><span class="sxs-lookup"><span data-stu-id="623d2-103">BusyType</span></span>

<span data-ttu-id="623d2-104">**BusyType**元素表示为日历事件设置的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="623d2-104">The **BusyType** element represents the free/busy status set for a calendar event.</span></span> 
  
```xml
<BusyType>Free or Tentative or Busy or OOF or NoData</BusyType>
```

 <span data-ttu-id="623d2-105">**BusyType**</span><span class="sxs-lookup"><span data-stu-id="623d2-105">**BusyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="623d2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="623d2-106">Attributes and elements</span></span>

<span data-ttu-id="623d2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="623d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="623d2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="623d2-108">Attributes</span></span>

<span data-ttu-id="623d2-109">无。</span><span class="sxs-lookup"><span data-stu-id="623d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="623d2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="623d2-110">Child elements</span></span>

<span data-ttu-id="623d2-111">无。</span><span class="sxs-lookup"><span data-stu-id="623d2-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="623d2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="623d2-112">Parent elements</span></span>

|<span data-ttu-id="623d2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="623d2-113">**Element**</span></span>|<span data-ttu-id="623d2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="623d2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="623d2-115">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="623d2-115">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="623d2-116">包含与建议的会议时间同时发生的时间窗口的用户或联系人的忙/闲状态。</span><span class="sxs-lookup"><span data-stu-id="623d2-116">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time.</span></span>  <br/> <span data-ttu-id="623d2-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="623d2-117">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/IndividualAttendeeConflictData` <br/> |
|[<span data-ttu-id="623d2-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="623d2-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="623d2-119">代表唯一的日历项目事件。</span><span class="sxs-lookup"><span data-stu-id="623d2-119">Represents a unique calendar item occurrence.</span></span>  <br/> <span data-ttu-id="623d2-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="623d2-120">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="623d2-121">文本值</span><span class="sxs-lookup"><span data-stu-id="623d2-121">Text value</span></span>

<span data-ttu-id="623d2-122">此元素需要一个文本值。</span><span class="sxs-lookup"><span data-stu-id="623d2-122">A text value is required for this element.</span></span> <span data-ttu-id="623d2-123">值为字符串类型。</span><span class="sxs-lookup"><span data-stu-id="623d2-123">The value is a string type.</span></span> <span data-ttu-id="623d2-124">以下是[BusyType](busytype.md)元素的可能值：</span><span class="sxs-lookup"><span data-stu-id="623d2-124">The following are the possible values for the [BusyType](busytype.md) element:</span></span> 
  
- <span data-ttu-id="623d2-125">空闲</span><span class="sxs-lookup"><span data-stu-id="623d2-125">Free</span></span>
    
- <span data-ttu-id="623d2-126">暂</span><span class="sxs-lookup"><span data-stu-id="623d2-126">Tentative</span></span>
    
- <span data-ttu-id="623d2-127">忙碌</span><span class="sxs-lookup"><span data-stu-id="623d2-127">Busy</span></span>
    
- <span data-ttu-id="623d2-128">OOF</span><span class="sxs-lookup"><span data-stu-id="623d2-128">OOF</span></span>
    
- <span data-ttu-id="623d2-129">NoData</span><span class="sxs-lookup"><span data-stu-id="623d2-129">NoData</span></span>
    
## <a name="remarks"></a><span data-ttu-id="623d2-130">说明</span><span class="sxs-lookup"><span data-stu-id="623d2-130">Remarks</span></span>

<span data-ttu-id="623d2-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="623d2-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="623d2-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="623d2-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="623d2-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="623d2-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="623d2-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="623d2-134">Schema Name</span></span>  <br/> |<span data-ttu-id="623d2-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="623d2-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="623d2-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="623d2-136">Validation File</span></span>  <br/> |<span data-ttu-id="623d2-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="623d2-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="623d2-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="623d2-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="623d2-139">False</span><span class="sxs-lookup"><span data-stu-id="623d2-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="623d2-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="623d2-140">See also</span></span>



[<span data-ttu-id="623d2-141">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="623d2-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="623d2-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="623d2-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="623d2-143">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="623d2-143">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

