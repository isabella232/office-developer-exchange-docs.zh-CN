---
title: RecurringDayTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDayTransition
api_type:
- schema
ms.assetid: 1ae28d14-c2b8-4084-9e76-e2e347a884ce
description: RecurringDayTransition 元素表示每年在同一天发生的时区转换。
ms.openlocfilehash: 44c2a6ec4dbaaa52a2772cb5c35a84b14dd77f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468465"
---
# <a name="recurringdaytransition"></a><span data-ttu-id="a7573-103">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="a7573-103">RecurringDayTransition</span></span>

<span data-ttu-id="a7573-104">**RecurringDayTransition**元素表示每年在同一天发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="a7573-104">The **RecurringDayTransition** element represents a time zone transition that occurs on the same day each year.</span></span> 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 <span data-ttu-id="a7573-105">**RecurringDayTransitionType**</span><span class="sxs-lookup"><span data-stu-id="a7573-105">**RecurringDayTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a7573-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a7573-106">Attributes and elements</span></span>

<span data-ttu-id="a7573-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a7573-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a7573-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a7573-108">Attributes</span></span>

<span data-ttu-id="a7573-109">无。</span><span class="sxs-lookup"><span data-stu-id="a7573-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a7573-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a7573-110">Child elements</span></span>

|<span data-ttu-id="a7573-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7573-111">**Element**</span></span>|<span data-ttu-id="a7573-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7573-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7573-113">To</span><span class="sxs-lookup"><span data-stu-id="a7573-113">To</span></span>](to.md) <br/> |<span data-ttu-id="a7573-114">指定作为时区转换目标的[时间段](period.md)或[TransitionsGroup](transitionsgroup.md) 。</span><span class="sxs-lookup"><span data-stu-id="a7573-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="a7573-115">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="a7573-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="a7573-116">表示时区转换与协调世界时（UTC）之间的持续时间偏移量。</span><span class="sxs-lookup"><span data-stu-id="a7573-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="a7573-117">Month （时区转换）</span><span class="sxs-lookup"><span data-stu-id="a7573-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="a7573-118">表示发生时区转换的月份。</span><span class="sxs-lookup"><span data-stu-id="a7573-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="a7573-119">DayOfWeek （时区）</span><span class="sxs-lookup"><span data-stu-id="a7573-119">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="a7573-120">表示发生时区转换的一周中的某一天。</span><span class="sxs-lookup"><span data-stu-id="a7573-120">Represents the day of the week on which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="a7573-121">事件（时区转换）</span><span class="sxs-lookup"><span data-stu-id="a7573-121">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="a7573-122">表示发生时区转换的月份中的一周中的某一天的匹配项。</span><span class="sxs-lookup"><span data-stu-id="a7573-122">Represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a7573-123">父元素</span><span class="sxs-lookup"><span data-stu-id="a7573-123">Parent elements</span></span>

|<span data-ttu-id="a7573-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="a7573-124">**Element**</span></span>|<span data-ttu-id="a7573-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="a7573-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a7573-126">移交</span><span class="sxs-lookup"><span data-stu-id="a7573-126">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="a7573-127">表示时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="a7573-127">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="a7573-128">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="a7573-128">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="a7573-129">表示时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="a7573-129">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7573-130">备注</span><span class="sxs-lookup"><span data-stu-id="a7573-130">Remarks</span></span>

<span data-ttu-id="a7573-131">[RecurringDayTransition](recurringdaytransition.md)元素可以表示的时区转换的一个示例是每年2月的第二个星期二发生的转换。</span><span class="sxs-lookup"><span data-stu-id="a7573-131">An example of a time zone transition that could be represented by the [RecurringDayTransition](recurringdaytransition.md) element is a transition that occurs on the second Tuesday of February each year.</span></span> 
  
<span data-ttu-id="a7573-132">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a7573-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a7573-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="a7573-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7573-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="a7573-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a7573-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="a7573-135">Schema Name</span></span>  <br/> |<span data-ttu-id="a7573-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="a7573-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="a7573-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="a7573-137">Validation File</span></span>  <br/> |<span data-ttu-id="a7573-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a7573-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a7573-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="a7573-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="a7573-140">False</span><span class="sxs-lookup"><span data-stu-id="a7573-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a7573-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a7573-141">See also</span></span>



- [<span data-ttu-id="a7573-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a7573-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

