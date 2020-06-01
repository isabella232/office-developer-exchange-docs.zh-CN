---
title: EndTime
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
description: EndTime 元素表示时间跨度的结束。
ms.openlocfilehash: 5a30b32ecfeafe582cd07dd662aacb0a960257c9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462990"
---
# <a name="endtime"></a><span data-ttu-id="fb47d-103">EndTime</span><span class="sxs-lookup"><span data-stu-id="fb47d-103">EndTime</span></span>

<span data-ttu-id="fb47d-104">**EndTime**元素表示时间跨度的结束。</span><span class="sxs-lookup"><span data-stu-id="fb47d-104">The **EndTime** element represents the end of a time span.</span></span> 
  
```xml
<EndTime>dateTime</EndTime>
```

 <span data-ttu-id="fb47d-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="fb47d-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb47d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fb47d-106">Attributes and elements</span></span>

<span data-ttu-id="fb47d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fb47d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb47d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fb47d-108">Attributes</span></span>

<span data-ttu-id="fb47d-109">无。</span><span class="sxs-lookup"><span data-stu-id="fb47d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb47d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fb47d-110">Child elements</span></span>

<span data-ttu-id="fb47d-111">无。</span><span class="sxs-lookup"><span data-stu-id="fb47d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fb47d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fb47d-112">Parent elements</span></span>

|<span data-ttu-id="fb47d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb47d-113">**Element**</span></span>|<span data-ttu-id="fb47d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb47d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb47d-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="fb47d-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="fb47d-116">标识查询的用户可用性信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="fb47d-116">Identifies the time span queried for the user availability information.</span></span><br/><br/> <span data-ttu-id="fb47d-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="fb47d-117">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="fb47d-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="fb47d-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="fb47d-119">标识查询的时间跨度，以获取有关建议会议时间的详细信息。</span><span class="sxs-lookup"><span data-stu-id="fb47d-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span><br/><br/> <span data-ttu-id="fb47d-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="fb47d-120">The following is the XPath expression to this element:</span></span><br/><br/>  <span data-ttu-id="fb47d-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span><span class="sxs-lookup"><span data-stu-id="fb47d-121">`/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.</span></span>  <br/> |
|[<span data-ttu-id="fb47d-122">持续时间（UserOofSettings）</span><span class="sxs-lookup"><span data-stu-id="fb47d-122">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="fb47d-123">指定在[OofState](oofstate.md)元素设置为 "已**计划**" 时启用 "外出" （OOF）状态的持续时间。</span><span class="sxs-lookup"><span data-stu-id="fb47d-123">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="fb47d-124">以下是此元素的可能的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="fb47d-124">The following are the possible XPath expressions to this element:</span></span><br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="fb47d-125">重复</span><span class="sxs-lookup"><span data-stu-id="fb47d-125">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="fb47d-126">代表定期日历项目的单个修改事件。</span><span class="sxs-lookup"><span data-stu-id="fb47d-126">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="fb47d-127">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="fb47d-127">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="fb47d-128">代表唯一的日历项目事件。</span><span class="sxs-lookup"><span data-stu-id="fb47d-128">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="fb47d-129">这用于可用性查询。</span><span class="sxs-lookup"><span data-stu-id="fb47d-129">This is used for Availability inquiries.</span></span> <span data-ttu-id="fb47d-130">**CalendarEvent**元素中的**EndTime**元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="fb47d-130">The **EndTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="fb47d-131">**CalendarEvent**元素中的**EndTime**元素对于**CalendarEvent**类型是唯一的。</span><span class="sxs-lookup"><span data-stu-id="fb47d-131">The **EndTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type.</span></span><br/><br/> <span data-ttu-id="fb47d-132">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="fb47d-132">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fb47d-133">文本值</span><span class="sxs-lookup"><span data-stu-id="fb47d-133">Text value</span></span>

<span data-ttu-id="fb47d-134">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="fb47d-134">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb47d-135">说明</span><span class="sxs-lookup"><span data-stu-id="fb47d-135">Remarks</span></span>

<span data-ttu-id="fb47d-136">[StartTime](starttime.md)元素表示时间范围的开始。</span><span class="sxs-lookup"><span data-stu-id="fb47d-136">The [StartTime](starttime.md) element represents the beginning of a time span.</span></span> 
  
<span data-ttu-id="fb47d-137">结束时间表示客户端的时间。</span><span class="sxs-lookup"><span data-stu-id="fb47d-137">The end time represents the client's time.</span></span>
  
<span data-ttu-id="fb47d-138">架构包含许多[EndTime](endtime.md)元素。</span><span class="sxs-lookup"><span data-stu-id="fb47d-138">The schema includes many [EndTime](endtime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fb47d-139">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fb47d-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fb47d-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="fb47d-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb47d-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="fb47d-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fb47d-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="fb47d-142">Schema Name</span></span>  <br/> |<span data-ttu-id="fb47d-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="fb47d-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="fb47d-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="fb47d-144">Validation File</span></span>  <br/> |<span data-ttu-id="fb47d-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fb47d-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fb47d-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="fb47d-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="fb47d-147">False</span><span class="sxs-lookup"><span data-stu-id="fb47d-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb47d-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb47d-148">See also</span></span>

- [<span data-ttu-id="fb47d-149">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="fb47d-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="fb47d-150">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="fb47d-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

