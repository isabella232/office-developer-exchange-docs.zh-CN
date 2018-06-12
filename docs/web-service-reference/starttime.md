---
title: StartTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTime
api_type:
- schema
ms.assetid: 1fac7937-7a06-4d66-9d2a-14423bcb3b37
description: StartTime 元素均表示的时间跨度。
ms.openlocfilehash: 4346797d755bb6e577e1cacb8bec656a7562bf1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827560"
---
# <a name="starttime"></a><span data-ttu-id="68f6d-103">StartTime</span><span class="sxs-lookup"><span data-stu-id="68f6d-103">StartTime</span></span>

<span data-ttu-id="68f6d-104">**StartTime**元素均表示的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="68f6d-104">The **StartTime** element represents the start of a time span.</span></span> 
  
```xml
<StartTime/
```

<span data-ttu-id="68f6d-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="68f6d-105">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="68f6d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="68f6d-106">Attributes and elements</span></span>

<span data-ttu-id="68f6d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="68f6d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="68f6d-108">属性</span><span class="sxs-lookup"><span data-stu-id="68f6d-108">Attributes</span></span>

<span data-ttu-id="68f6d-109">无。</span><span class="sxs-lookup"><span data-stu-id="68f6d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="68f6d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="68f6d-110">Child elements</span></span>

<span data-ttu-id="68f6d-111">无。</span><span class="sxs-lookup"><span data-stu-id="68f6d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="68f6d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="68f6d-112">Parent elements</span></span>

|<span data-ttu-id="68f6d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="68f6d-113">**Element**</span></span>|<span data-ttu-id="68f6d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="68f6d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="68f6d-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="68f6d-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="68f6d-116">标识查询的用户的可用性信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="68f6d-116">Identifies the time span queried for the user availability information.</span></span>  <br/><br/> <span data-ttu-id="68f6d-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="68f6d-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="68f6d-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="68f6d-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="68f6d-119">标识查询建议的会议时间有关的详细信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="68f6d-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/><br/> <span data-ttu-id="68f6d-120">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="68f6d-120">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[<span data-ttu-id="68f6d-121">持续时间 (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="68f6d-121">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="68f6d-122">指定如果[OofState](oofstate.md)元素设置为**计划**为其启用 Office 外出 (OOF) 状态的持续时间。</span><span class="sxs-lookup"><span data-stu-id="68f6d-122">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="68f6d-123">以下是此元素可能 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="68f6d-123">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="68f6d-124">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="68f6d-124">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="68f6d-125">代表独特的日历项匹配项。</span><span class="sxs-lookup"><span data-stu-id="68f6d-125">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="68f6d-126">这用于可用性的查询。</span><span class="sxs-lookup"><span data-stu-id="68f6d-126">This is used for Availability inquiries.</span></span> <span data-ttu-id="68f6d-127">**StartTime**元素需要**CalendarEvent**元素中。</span><span class="sxs-lookup"><span data-stu-id="68f6d-127">The **StartTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="68f6d-128">尽管它包含的**持续时间**类型中的**StartTime**元素包含的方面值相同， **CalendarEvent**元素中的**StartTime**元素是唯一的**CalendarEvent**类型。</span><span class="sxs-lookup"><span data-stu-id="68f6d-128">The **StartTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type although it contains the same facet values that the **StartTime** elements in the **Duration** type contain.</span></span>  <br/><br/> <span data-ttu-id="68f6d-129">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="68f6d-129">The following is the XPath expression to this element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="68f6d-130">文本值</span><span class="sxs-lookup"><span data-stu-id="68f6d-130">Text value</span></span>

<span data-ttu-id="68f6d-131">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="68f6d-131">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68f6d-132">备注</span><span class="sxs-lookup"><span data-stu-id="68f6d-132">Remarks</span></span>

<span data-ttu-id="68f6d-133">[EndTime](endtime.md)元素均表示时间范围的末尾。</span><span class="sxs-lookup"><span data-stu-id="68f6d-133">The [EndTime](endtime.md) element represents the end of the time span.</span></span> 
  
<span data-ttu-id="68f6d-134">架构包括许多[StartTime](starttime.md)元素。</span><span class="sxs-lookup"><span data-stu-id="68f6d-134">The schema includes many [StartTime](starttime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="68f6d-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="68f6d-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="68f6d-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="68f6d-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68f6d-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="68f6d-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="68f6d-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="68f6d-138">Schema Name</span></span>  <br/> |<span data-ttu-id="68f6d-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="68f6d-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="68f6d-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="68f6d-140">Validation File</span></span>  <br/> |<span data-ttu-id="68f6d-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="68f6d-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="68f6d-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="68f6d-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="68f6d-143">False</span><span class="sxs-lookup"><span data-stu-id="68f6d-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68f6d-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="68f6d-144">See also</span></span>

- [<span data-ttu-id="68f6d-145">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="68f6d-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="68f6d-146">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="68f6d-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

