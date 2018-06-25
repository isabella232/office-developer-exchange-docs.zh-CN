---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: RecurringDateTransition 元素均表示发生在特定日期每年时区转换。
ms.openlocfilehash: 7cd8f3452a744e0c9a98fd3698dffb9ed8721a6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827014"
---
# <a name="recurringdatetransition"></a><span data-ttu-id="22347-103">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="22347-103">RecurringDateTransition</span></span>

<span data-ttu-id="22347-104">**RecurringDateTransition**元素均表示发生在特定日期每年时区转换。</span><span class="sxs-lookup"><span data-stu-id="22347-104">The **RecurringDateTransition** element represents a time zone transition that occurs on a specific date each year.</span></span> 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 <span data-ttu-id="22347-105">**RecurringDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="22347-105">**RecurringDateTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22347-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22347-106">Attributes and elements</span></span>

<span data-ttu-id="22347-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22347-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22347-108">属性</span><span class="sxs-lookup"><span data-stu-id="22347-108">Attributes</span></span>

<span data-ttu-id="22347-109">无。</span><span class="sxs-lookup"><span data-stu-id="22347-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22347-110">子元素</span><span class="sxs-lookup"><span data-stu-id="22347-110">Child elements</span></span>

|<span data-ttu-id="22347-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="22347-111">**Element**</span></span>|<span data-ttu-id="22347-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="22347-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22347-113">To</span><span class="sxs-lookup"><span data-stu-id="22347-113">To</span></span>](to.md) <br/> |<span data-ttu-id="22347-114">指定[时段](period.md)或[TransitionsGroup](transitionsgroup.md)所在的时区转换的目标。</span><span class="sxs-lookup"><span data-stu-id="22347-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="22347-115">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="22347-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="22347-116">代表所在的时区转换的持续时间偏移量与协调世界时 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="22347-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="22347-117">每月 （所在的时区转换）</span><span class="sxs-lookup"><span data-stu-id="22347-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="22347-118">代表所在的时区转换发生的月份。</span><span class="sxs-lookup"><span data-stu-id="22347-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="22347-119">日。</span><span class="sxs-lookup"><span data-stu-id="22347-119">Day</span></span>](day.md) <br/> |<span data-ttu-id="22347-120">表示在所在的时区转换发生相应月份的某一天。</span><span class="sxs-lookup"><span data-stu-id="22347-120">Represents the day of the month on which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="22347-121">父元素</span><span class="sxs-lookup"><span data-stu-id="22347-121">Parent elements</span></span>

|<span data-ttu-id="22347-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="22347-122">**Element**</span></span>|<span data-ttu-id="22347-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="22347-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22347-124">切换</span><span class="sxs-lookup"><span data-stu-id="22347-124">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="22347-125">表示所在的时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="22347-125">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="22347-126">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="22347-126">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="22347-127">表示所在的时区转换的集合。</span><span class="sxs-lookup"><span data-stu-id="22347-127">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22347-128">注解</span><span class="sxs-lookup"><span data-stu-id="22347-128">Remarks</span></span>

<span data-ttu-id="22347-129">无法由[RecurringDateTransition](recurringdatetransition.md)元素所在的时区转换的一个示例是发生月 15 日每年的转换。</span><span class="sxs-lookup"><span data-stu-id="22347-129">An example of a time zone transition that could be represented by the [RecurringDateTransition](recurringdatetransition.md) element is a transition that occurs on March 15 each year.</span></span> 
  
<span data-ttu-id="22347-130">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22347-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22347-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="22347-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22347-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="22347-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22347-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="22347-133">Schema Name</span></span>  <br/> |<span data-ttu-id="22347-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="22347-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="22347-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="22347-135">Validation File</span></span>  <br/> |<span data-ttu-id="22347-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="22347-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22347-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="22347-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="22347-138">False</span><span class="sxs-lookup"><span data-stu-id="22347-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22347-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22347-139">See also</span></span>



- [<span data-ttu-id="22347-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="22347-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

