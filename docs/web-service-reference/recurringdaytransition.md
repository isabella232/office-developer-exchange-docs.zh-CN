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
description: RecurringDayTransition 元素均表示发生在同一天每年时区转换。
ms.openlocfilehash: 913345188547ce9903809fdc1cbbbe3e20ae7f36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827012"
---
# <a name="recurringdaytransition"></a><span data-ttu-id="af4ca-103">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="af4ca-103">RecurringDayTransition</span></span>

<span data-ttu-id="af4ca-104">**RecurringDayTransition**元素均表示发生在同一天每年时区转换。</span><span class="sxs-lookup"><span data-stu-id="af4ca-104">The **RecurringDayTransition** element represents a time zone transition that occurs on the same day each year.</span></span> 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 <span data-ttu-id="af4ca-105">**RecurringDayTransitionType**</span><span class="sxs-lookup"><span data-stu-id="af4ca-105">**RecurringDayTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="af4ca-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="af4ca-106">Attributes and elements</span></span>

<span data-ttu-id="af4ca-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="af4ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af4ca-108">属性</span><span class="sxs-lookup"><span data-stu-id="af4ca-108">Attributes</span></span>

<span data-ttu-id="af4ca-109">无。</span><span class="sxs-lookup"><span data-stu-id="af4ca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="af4ca-110">子元素</span><span class="sxs-lookup"><span data-stu-id="af4ca-110">Child elements</span></span>

|<span data-ttu-id="af4ca-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="af4ca-111">**Element**</span></span>|<span data-ttu-id="af4ca-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="af4ca-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af4ca-113">To</span><span class="sxs-lookup"><span data-stu-id="af4ca-113">To</span></span>](to.md) <br/> |<span data-ttu-id="af4ca-114">指定[时段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标。</span><span class="sxs-lookup"><span data-stu-id="af4ca-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="af4ca-115">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="af4ca-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="af4ca-116">代表所在的时区转换的持续时间偏移量与协调世界时 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="af4ca-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="af4ca-117">每月 （所在的时区转换）</span><span class="sxs-lookup"><span data-stu-id="af4ca-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="af4ca-118">代表所在的时区转换发生的月份。</span><span class="sxs-lookup"><span data-stu-id="af4ca-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="af4ca-119">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="af4ca-119">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="af4ca-120">表示在所在的时区转换发生一周中的某一天。</span><span class="sxs-lookup"><span data-stu-id="af4ca-120">Represents the day of the week on which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="af4ca-121">出现 （所在的时区转换）</span><span class="sxs-lookup"><span data-stu-id="af4ca-121">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="af4ca-122">代表星期几所在的时区转换发生月中的匹配项。</span><span class="sxs-lookup"><span data-stu-id="af4ca-122">Represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="af4ca-123">父元素</span><span class="sxs-lookup"><span data-stu-id="af4ca-123">Parent elements</span></span>

|<span data-ttu-id="af4ca-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="af4ca-124">**Element**</span></span>|<span data-ttu-id="af4ca-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="af4ca-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="af4ca-126">切换</span><span class="sxs-lookup"><span data-stu-id="af4ca-126">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="af4ca-127">表示所在的时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="af4ca-127">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="af4ca-128">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="af4ca-128">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="af4ca-129">表示所在的时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="af4ca-129">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af4ca-130">注解</span><span class="sxs-lookup"><span data-stu-id="af4ca-130">Remarks</span></span>

<span data-ttu-id="af4ca-131">无法由[RecurringDayTransition](recurringdaytransition.md)元素所在的时区转换的一个示例是发生年 2 月的第二个星期二每年的转换。</span><span class="sxs-lookup"><span data-stu-id="af4ca-131">An example of a time zone transition that could be represented by the [RecurringDayTransition](recurringdaytransition.md) element is a transition that occurs on the second Tuesday of February each year.</span></span> 
  
<span data-ttu-id="af4ca-132">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="af4ca-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="af4ca-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="af4ca-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af4ca-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="af4ca-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="af4ca-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="af4ca-135">Schema Name</span></span>  <br/> |<span data-ttu-id="af4ca-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="af4ca-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="af4ca-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="af4ca-137">Validation File</span></span>  <br/> |<span data-ttu-id="af4ca-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="af4ca-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="af4ca-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="af4ca-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="af4ca-140">False</span><span class="sxs-lookup"><span data-stu-id="af4ca-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af4ca-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="af4ca-141">See also</span></span>



- [<span data-ttu-id="af4ca-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="af4ca-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

