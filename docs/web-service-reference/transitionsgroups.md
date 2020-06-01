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
description: TransitionsGroups 元素表示时区转换组的数组。
ms.openlocfilehash: 35244e122ee31045359afd0833459bbb94fd0aa1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467408"
---
# <a name="transitionsgroups"></a><span data-ttu-id="e9fd9-103">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="e9fd9-103">TransitionsGroups</span></span>

<span data-ttu-id="e9fd9-104">**TransitionsGroups**元素表示时区转换组的数组。</span><span class="sxs-lookup"><span data-stu-id="e9fd9-104">The **TransitionsGroups** element represents an array of time zone transition groups.</span></span> 
  
```XML
<TransitionsGroups>
   <TransitionsGroup/>
</TransitionsGroups>
```

 <span data-ttu-id="e9fd9-105">**ArrayOfTransitionsGroupsType**</span><span class="sxs-lookup"><span data-stu-id="e9fd9-105">**ArrayOfTransitionsGroupsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e9fd9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e9fd9-106">Attributes and elements</span></span>

<span data-ttu-id="e9fd9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e9fd9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9fd9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e9fd9-108">Attributes</span></span>

<span data-ttu-id="e9fd9-109">无。</span><span class="sxs-lookup"><span data-stu-id="e9fd9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9fd9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e9fd9-110">Child elements</span></span>

|<span data-ttu-id="e9fd9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e9fd9-111">**Element**</span></span>|<span data-ttu-id="e9fd9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e9fd9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9fd9-113">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="e9fd9-113">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="e9fd9-114">表示时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="e9fd9-114">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e9fd9-115">父元素</span><span class="sxs-lookup"><span data-stu-id="e9fd9-115">Parent elements</span></span>

|<span data-ttu-id="e9fd9-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e9fd9-116">**Element**</span></span>|<span data-ttu-id="e9fd9-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e9fd9-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e9fd9-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="e9fd9-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="e9fd9-119">定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)的开始时间的时区。</span><span class="sxs-lookup"><span data-stu-id="e9fd9-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="e9fd9-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="e9fd9-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="e9fd9-121">定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)的结束时间的时区。</span><span class="sxs-lookup"><span data-stu-id="e9fd9-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="e9fd9-122">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="e9fd9-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="e9fd9-123">定义时区。</span><span class="sxs-lookup"><span data-stu-id="e9fd9-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9fd9-124">说明</span><span class="sxs-lookup"><span data-stu-id="e9fd9-124">Remarks</span></span>

<span data-ttu-id="e9fd9-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e9fd9-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9fd9-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="e9fd9-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9fd9-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="e9fd9-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e9fd9-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="e9fd9-128">Schema Name</span></span>  <br/> |<span data-ttu-id="e9fd9-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="e9fd9-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="e9fd9-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="e9fd9-130">Validation File</span></span>  <br/> |<span data-ttu-id="e9fd9-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e9fd9-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e9fd9-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="e9fd9-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="e9fd9-133">False</span><span class="sxs-lookup"><span data-stu-id="e9fd9-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9fd9-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e9fd9-134">See also</span></span>



- [<span data-ttu-id="e9fd9-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e9fd9-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

