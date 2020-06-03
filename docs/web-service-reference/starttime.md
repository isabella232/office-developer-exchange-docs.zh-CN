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
description: StartTime 元素表示时间范围的开始时间。
ms.openlocfilehash: 16bee698b65dc512a709e2af9ddfe8629347fee3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458563"
---
# <a name="starttime"></a><span data-ttu-id="015b8-103">StartTime</span><span class="sxs-lookup"><span data-stu-id="015b8-103">StartTime</span></span>

<span data-ttu-id="015b8-104">**StartTime**元素表示时间范围的开始时间。</span><span class="sxs-lookup"><span data-stu-id="015b8-104">The **StartTime** element represents the start of a time span.</span></span> 
  
```xml
<StartTime/
```

<span data-ttu-id="015b8-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="015b8-105">**dateTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="015b8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="015b8-106">Attributes and elements</span></span>

<span data-ttu-id="015b8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="015b8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="015b8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="015b8-108">Attributes</span></span>

<span data-ttu-id="015b8-109">无。</span><span class="sxs-lookup"><span data-stu-id="015b8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="015b8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="015b8-110">Child elements</span></span>

<span data-ttu-id="015b8-111">无。</span><span class="sxs-lookup"><span data-stu-id="015b8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="015b8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="015b8-112">Parent elements</span></span>

|<span data-ttu-id="015b8-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="015b8-113">**Element**</span></span>|<span data-ttu-id="015b8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="015b8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="015b8-115">TimeWindow</span><span class="sxs-lookup"><span data-stu-id="015b8-115">TimeWindow</span></span>](timewindow.md) <br/> |<span data-ttu-id="015b8-116">标识查询的用户可用性信息的时间跨度。</span><span class="sxs-lookup"><span data-stu-id="015b8-116">Identifies the time span queried for the user availability information.</span></span>  <br/><br/> <span data-ttu-id="015b8-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="015b8-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[<span data-ttu-id="015b8-118">DetailedSuggestionsWindow</span><span class="sxs-lookup"><span data-stu-id="015b8-118">DetailedSuggestionsWindow</span></span>](detailedsuggestionswindow.md) <br/> |<span data-ttu-id="015b8-119">标识查询的时间跨度，以获取有关建议会议时间的详细信息。</span><span class="sxs-lookup"><span data-stu-id="015b8-119">Identifies the time span that is queried for detailed information about suggested meeting times.</span></span>  <br/><br/> <span data-ttu-id="015b8-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="015b8-120">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[<span data-ttu-id="015b8-121">持续时间（UserOofSettings）</span><span class="sxs-lookup"><span data-stu-id="015b8-121">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> | <span data-ttu-id="015b8-122">指定在[OofState](oofstate.md)元素设置为 "已**计划**" 时启用 "外出" （OOF）状态的持续时间。</span><span class="sxs-lookup"><span data-stu-id="015b8-122">Specifies the duration for which the Out of Office (OOF) status is enabled if the [OofState](oofstate.md) element is set to **Scheduled**.</span></span>  <br/><br/>  <span data-ttu-id="015b8-123">以下是此元素的可能的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="015b8-123">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[<span data-ttu-id="015b8-124">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="015b8-124">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="015b8-125">代表唯一的日历项目事件。</span><span class="sxs-lookup"><span data-stu-id="015b8-125">Represents a unique calendar item occurrence.</span></span> <span data-ttu-id="015b8-126">这用于可用性查询。</span><span class="sxs-lookup"><span data-stu-id="015b8-126">This is used for Availability inquiries.</span></span> <span data-ttu-id="015b8-127">在**CalendarEvent**元素中， **StartTime**元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="015b8-127">The **StartTime** element is required in the **CalendarEvent** element.</span></span> <span data-ttu-id="015b8-128">**CalendarEvent**元素中的**Starttime**元素对于**CalendarEvent**类型是唯一的，但它包含**持续时间**类型中的**starttime**元素包含的相同 facet 值。</span><span class="sxs-lookup"><span data-stu-id="015b8-128">The **StartTime** element in the **CalendarEvent** element is unique to the **CalendarEvent** type although it contains the same facet values that the **StartTime** elements in the **Duration** type contain.</span></span>  <br/><br/> <span data-ttu-id="015b8-129">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="015b8-129">The following is the XPath expression to this element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="015b8-130">文本值</span><span class="sxs-lookup"><span data-stu-id="015b8-130">Text value</span></span>

<span data-ttu-id="015b8-131">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="015b8-131">A text value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="015b8-132">说明</span><span class="sxs-lookup"><span data-stu-id="015b8-132">Remarks</span></span>

<span data-ttu-id="015b8-133">[EndTime](endtime.md)元素表示时间跨度的结束。</span><span class="sxs-lookup"><span data-stu-id="015b8-133">The [EndTime](endtime.md) element represents the end of the time span.</span></span> 
  
<span data-ttu-id="015b8-134">架构包含许多[StartTime](starttime.md)元素。</span><span class="sxs-lookup"><span data-stu-id="015b8-134">The schema includes many [StartTime](starttime.md) elements.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="015b8-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="015b8-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="015b8-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="015b8-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="015b8-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="015b8-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="015b8-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="015b8-138">Schema Name</span></span>  <br/> |<span data-ttu-id="015b8-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="015b8-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="015b8-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="015b8-140">Validation File</span></span>  <br/> |<span data-ttu-id="015b8-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="015b8-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="015b8-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="015b8-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="015b8-143">False</span><span class="sxs-lookup"><span data-stu-id="015b8-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="015b8-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="015b8-144">See also</span></span>

- [<span data-ttu-id="015b8-145">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="015b8-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="015b8-146">获取用户可用性</span><span class="sxs-lookup"><span data-stu-id="015b8-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

