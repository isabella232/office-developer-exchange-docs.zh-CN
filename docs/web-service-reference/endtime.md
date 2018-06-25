---
title: 结束时间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: EndTime 元素均表示时间范围的末尾。
ms.openlocfilehash: 7d3d186618a7bcc05ad82532e13e03d2e67a0e40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754138"
---
# <a name="endtime"></a><span data-ttu-id="062ba-103">结束时间</span><span class="sxs-lookup"><span data-stu-id="062ba-103">EndTime</span></span>

<span data-ttu-id="062ba-104">**EndTime**元素均表示时间范围的末尾。</span><span class="sxs-lookup"><span data-stu-id="062ba-104">The **EndTime** element represents the end of a time span.</span></span> 
  
```xml
<EndTime>dateTime</EndTime>
```

 <span data-ttu-id="062ba-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="062ba-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="062ba-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="062ba-106">Attributes and elements</span></span>

<span data-ttu-id="062ba-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="062ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="062ba-108">属性</span><span class="sxs-lookup"><span data-stu-id="062ba-108">Attributes</span></span>

<span data-ttu-id="062ba-109">无。</span><span class="sxs-lookup"><span data-stu-id="062ba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="062ba-110">子元素</span><span class="sxs-lookup"><span data-stu-id="062ba-110">Child elements</span></span>

<span data-ttu-id="062ba-111">无。</span><span class="sxs-lookup"><span data-stu-id="062ba-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="062ba-112">父元素</span><span class="sxs-lookup"><span data-stu-id="062ba-112">Parent elements</span></span>

|<span data-ttu-id="062ba-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="062ba-113">**Element**</span></span>|<span data-ttu-id="062ba-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="062ba-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="062ba-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="062ba-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="062ba-116">标识查询的用户的可用性信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="062ba-116">Identifies the time span queried for the user availability information.</span></span><br/><br/> <span data-ttu-id="062ba-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="062ba-117">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="062ba-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="062ba-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="062ba-119">标识查询建议的会议时间有关的详细信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="062ba-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span><br/><br/> <span data-ttu-id="062ba-120">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="062ba-120">The following is the XPath expression to this element:</span></span><br/><br/>  <span data-ttu-id="062ba-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span><span class="sxs-lookup"><span data-stu-id="062ba-121"></span></span>  <br/> |
|[<span data-ttu-id="062ba-122">持续时间 (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="062ba-122">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="062ba-123">指定如果[OofState](oofstate.md)元素设置为**计划**为其启用 Office 外出 (OOF) 状态的持续时间。</span><span class="sxs-lookup"><span data-stu-id="062ba-123">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="062ba-124">以下是此元素可能 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="062ba-124">The following are the possible XPath expressions to this element:</span></span><br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="062ba-125">匹配项</span><span class="sxs-lookup"><span data-stu-id="062ba-125">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="062ba-126">代表定期日历项目的一个已修改匹配项。</span><span class="sxs-lookup"><span data-stu-id="062ba-126">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="062ba-127">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="062ba-127">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="062ba-128">代表独特的日历项匹配项。</span><span class="sxs-lookup"><span data-stu-id="062ba-128">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="062ba-129">这用于可用性的查询。</span><span class="sxs-lookup"><span data-stu-id="062ba-129">This is used for Availability inquiries.</span></span> <span data-ttu-id="062ba-130">**EndTime**元素需要**CalendarEvent**元素中。</span><span class="sxs-lookup"><span data-stu-id="062ba-130">The **EndTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="062ba-131">**CalendarEvent**元素中的**EndTime**元素是唯一的**CalendarEvent**类型。</span><span class="sxs-lookup"><span data-stu-id="062ba-131">The **EndTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type.</span></span><br/><br/> <span data-ttu-id="062ba-132">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="062ba-132">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="062ba-133">文本值</span><span class="sxs-lookup"><span data-stu-id="062ba-133">Text value</span></span>

<span data-ttu-id="062ba-134">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="062ba-134">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="062ba-135">备注</span><span class="sxs-lookup"><span data-stu-id="062ba-135">Remarks</span></span>

<span data-ttu-id="062ba-136">[StartTime](starttime.md)元素均表示时间跨度的开头。</span><span class="sxs-lookup"><span data-stu-id="062ba-136">The [StartTime](starttime.md) element represents the beginning of a time span.</span></span> 
  
<span data-ttu-id="062ba-137">结束时间表示客户端的时间。</span><span class="sxs-lookup"><span data-stu-id="062ba-137">The end time represents the client's time.</span></span>
  
<span data-ttu-id="062ba-138">架构包括许多[EndTime](endtime.md)元素。</span><span class="sxs-lookup"><span data-stu-id="062ba-138">The schema includes many [EndTime](endtime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="062ba-139">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="062ba-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="062ba-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="062ba-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="062ba-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="062ba-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="062ba-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="062ba-142">Schema Name</span></span>  <br/> |<span data-ttu-id="062ba-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="062ba-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="062ba-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="062ba-144">Validation File</span></span>  <br/> |<span data-ttu-id="062ba-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="062ba-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="062ba-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="062ba-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="062ba-147">False</span><span class="sxs-lookup"><span data-stu-id="062ba-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="062ba-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="062ba-148">See also</span></span>

- [<span data-ttu-id="062ba-149">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="062ba-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="062ba-150">Getting User Availability</span><span class="sxs-lookup"><span data-stu-id="062ba-150">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

