---
title: StartTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTimeZone
api_type:
- schema
ms.assetid: d38c4dc1-4ecb-42a1-8d57-a451b16a2de2
description: StartTimeZone 元素定义开始时间的日历项目或 MeetingRequest 所在的时区。
ms.openlocfilehash: 6d21869c4b3be048db27dcc9f128fff868aebcb5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827559"
---
# <a name="starttimezone"></a><span data-ttu-id="1e216-103">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="1e216-103">StartTimeZone</span></span>

<span data-ttu-id="1e216-104">**StartTimeZone**元素定义开始时间的[日历项目](calendaritem.md)或[MeetingRequest](meetingrequest.md)所在的时区。</span><span class="sxs-lookup"><span data-stu-id="1e216-104">The **StartTimeZone** element defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<StartTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</StartTimeZone>
```

<span data-ttu-id="1e216-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="1e216-105">**TimeZoneDefinitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1e216-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1e216-106">Attributes and elements</span></span>

<span data-ttu-id="1e216-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1e216-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e216-108">属性</span><span class="sxs-lookup"><span data-stu-id="1e216-108">Attributes</span></span>

|<span data-ttu-id="1e216-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="1e216-109">**Attribute**</span></span>|<span data-ttu-id="1e216-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e216-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1e216-111">Id</span><span class="sxs-lookup"><span data-stu-id="1e216-111">Id</span></span>  <br/> |<span data-ttu-id="1e216-112">代表所在的时区定义的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="1e216-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="1e216-113">名称</span><span class="sxs-lookup"><span data-stu-id="1e216-113">Name</span></span>  <br/> |<span data-ttu-id="1e216-114">代表所在的时区定义的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="1e216-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1e216-115">子元素</span><span class="sxs-lookup"><span data-stu-id="1e216-115">Child elements</span></span>

|<span data-ttu-id="1e216-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e216-116">**Element**</span></span>|<span data-ttu-id="1e216-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e216-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e216-118">时间段</span><span class="sxs-lookup"><span data-stu-id="1e216-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="1e216-119">表示定义的时间偏移量的时区的不同阶段的[时间段](period.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="1e216-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="1e216-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="1e216-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="1e216-121">代表指定时区转换的[TransitionsGroup](transitionsgroup.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="1e216-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="1e216-122">切换</span><span class="sxs-lookup"><span data-stu-id="1e216-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="1e216-123">代表所在的时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="1e216-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1e216-124">父元素</span><span class="sxs-lookup"><span data-stu-id="1e216-124">Parent elements</span></span>

|<span data-ttu-id="1e216-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e216-125">**Element**</span></span>|<span data-ttu-id="1e216-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e216-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e216-127">日历项目</span><span class="sxs-lookup"><span data-stu-id="1e216-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1e216-128">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="1e216-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1e216-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1e216-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1e216-130">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="1e216-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e216-131">注解</span><span class="sxs-lookup"><span data-stu-id="1e216-131">Remarks</span></span>

<span data-ttu-id="1e216-132">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1e216-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e216-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="1e216-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e216-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="1e216-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1e216-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="1e216-135">Schema Name</span></span>  <br/> |<span data-ttu-id="1e216-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="1e216-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="1e216-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="1e216-137">Validation File</span></span>  <br/> |<span data-ttu-id="1e216-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1e216-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1e216-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="1e216-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="1e216-140">False</span><span class="sxs-lookup"><span data-stu-id="1e216-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e216-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1e216-141">See also</span></span>

- [<span data-ttu-id="1e216-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1e216-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

