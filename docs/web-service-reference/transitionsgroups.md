---
title: TransitionsGroups
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TransitionsGroups
api_type:
- schema
ms.assetid: ad0849f8-5158-4a23-9c36-a49f5be1d1e1
description: TransitionsGroups 元素均表示所在的时区转换组的数组。
ms.openlocfilehash: 546dd3c96187bf9f1ebf574b37b689e26e3af997
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838288"
---
# <a name="transitionsgroups"></a><span data-ttu-id="4834b-103">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="4834b-103">TransitionsGroups</span></span>

<span data-ttu-id="4834b-104">**TransitionsGroups**元素均表示所在的时区转换组的数组。</span><span class="sxs-lookup"><span data-stu-id="4834b-104">The **TransitionsGroups** element represents an array of time zone transition groups.</span></span> 
  
```XML
<TransitionsGroups>
   <TransitionsGroup/>
</TransitionsGroups>
```

 <span data-ttu-id="4834b-105">**ArrayOfTransitionsGroupsType**</span><span class="sxs-lookup"><span data-stu-id="4834b-105">**ArrayOfTransitionsGroupsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4834b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4834b-106">Attributes and elements</span></span>

<span data-ttu-id="4834b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4834b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4834b-108">属性</span><span class="sxs-lookup"><span data-stu-id="4834b-108">Attributes</span></span>

<span data-ttu-id="4834b-109">无。</span><span class="sxs-lookup"><span data-stu-id="4834b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4834b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4834b-110">Child elements</span></span>

|<span data-ttu-id="4834b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4834b-111">**Element**</span></span>|<span data-ttu-id="4834b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4834b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4834b-113">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="4834b-113">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="4834b-114">代表所在的时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="4834b-114">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4834b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4834b-115">Parent elements</span></span>

|<span data-ttu-id="4834b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4834b-116">**Element**</span></span>|<span data-ttu-id="4834b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4834b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4834b-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="4834b-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="4834b-119">定义开始时间的[日历项目](calendaritem.md)或[MeetingRequest](meetingrequest.md)所在的时区。</span><span class="sxs-lookup"><span data-stu-id="4834b-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="4834b-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="4834b-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="4834b-121">定义的结束时间的[日历项目](calendaritem.md)或[MeetingRequest](meetingrequest.md)所在的时区。</span><span class="sxs-lookup"><span data-stu-id="4834b-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="4834b-122">时区定义</span><span class="sxs-lookup"><span data-stu-id="4834b-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="4834b-123">定义时区。</span><span class="sxs-lookup"><span data-stu-id="4834b-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4834b-124">备注</span><span class="sxs-lookup"><span data-stu-id="4834b-124">Remarks</span></span>

<span data-ttu-id="4834b-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4834b-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4834b-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="4834b-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4834b-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="4834b-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4834b-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="4834b-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4834b-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="4834b-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="4834b-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="4834b-130">Validation File</span></span>  <br/> |<span data-ttu-id="4834b-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4834b-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4834b-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="4834b-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4834b-133">False</span><span class="sxs-lookup"><span data-stu-id="4834b-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4834b-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4834b-134">See also</span></span>



- [<span data-ttu-id="4834b-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4834b-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

