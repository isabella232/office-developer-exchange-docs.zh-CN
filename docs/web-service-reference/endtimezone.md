---
title: EndTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTimeZone
api_type:
- schema
ms.assetid: 6c53c337-be60-4d22-9e9e-a0c140c5e913
description: EndTimeZone 元素的结束时间的日历项目或 MeetingRequest 定义时区。
ms.openlocfilehash: 65eeedcc7c4d0e616ae54d4e2545fd310e9ad905
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754125"
---
# <a name="endtimezone"></a><span data-ttu-id="92873-103">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="92873-103">EndTimeZone</span></span>

<span data-ttu-id="92873-104">**EndTimeZone**元素的结束时间的[日历项目](calendaritem.md)或[MeetingRequest](meetingrequest.md)定义时区。</span><span class="sxs-lookup"><span data-stu-id="92873-104">The **EndTimeZone** element defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<EndTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</EndTimeZone>
```

 <span data-ttu-id="92873-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="92873-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="92873-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="92873-106">Attributes and elements</span></span>

<span data-ttu-id="92873-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="92873-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92873-108">属性</span><span class="sxs-lookup"><span data-stu-id="92873-108">Attributes</span></span>

|<span data-ttu-id="92873-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="92873-109">**Attribute**</span></span>|<span data-ttu-id="92873-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="92873-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="92873-111">Id</span><span class="sxs-lookup"><span data-stu-id="92873-111">Id</span></span>  <br/> |<span data-ttu-id="92873-112">代表所在的时区定义的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="92873-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="92873-113">名称</span><span class="sxs-lookup"><span data-stu-id="92873-113">Name</span></span>  <br/> |<span data-ttu-id="92873-114">代表所在的时区定义的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="92873-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="92873-115">子元素</span><span class="sxs-lookup"><span data-stu-id="92873-115">Child elements</span></span>

|<span data-ttu-id="92873-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="92873-116">**Element**</span></span>|<span data-ttu-id="92873-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="92873-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92873-118">时间段</span><span class="sxs-lookup"><span data-stu-id="92873-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="92873-119">表示定义的时间偏移量的时区的不同阶段的[时间段](period.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="92873-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="92873-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="92873-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="92873-121">代表指定时区转换的[TransitionsGroup](transitionsgroup.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="92873-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="92873-122">切换</span><span class="sxs-lookup"><span data-stu-id="92873-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="92873-123">代表所在的时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="92873-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="92873-124">父元素</span><span class="sxs-lookup"><span data-stu-id="92873-124">Parent elements</span></span>

|<span data-ttu-id="92873-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="92873-125">**Element**</span></span>|<span data-ttu-id="92873-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="92873-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92873-127">日历项目</span><span class="sxs-lookup"><span data-stu-id="92873-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="92873-128">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="92873-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="92873-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="92873-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="92873-130">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="92873-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92873-131">注解</span><span class="sxs-lookup"><span data-stu-id="92873-131">Remarks</span></span>

<span data-ttu-id="92873-132">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="92873-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92873-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="92873-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92873-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="92873-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="92873-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="92873-135">Schema Name</span></span>  <br/> |<span data-ttu-id="92873-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="92873-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="92873-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="92873-137">Validation File</span></span>  <br/> |<span data-ttu-id="92873-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="92873-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="92873-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="92873-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="92873-140">False</span><span class="sxs-lookup"><span data-stu-id="92873-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92873-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="92873-141">See also</span></span>



- [<span data-ttu-id="92873-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="92873-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

