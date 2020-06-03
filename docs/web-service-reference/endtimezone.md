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
description: EndTimeZone 元素定义 CalendarItem 或 MeetingRequest 结束时间的时区。
ms.openlocfilehash: 83ab2ab90e2bed7658fe83ed33a72b60d5f10135
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462983"
---
# <a name="endtimezone"></a><span data-ttu-id="c1ef1-103">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="c1ef1-103">EndTimeZone</span></span>

<span data-ttu-id="c1ef1-104">**EndTimeZone**元素定义[CalendarItem](calendaritem.md)或[MeetingRequest](meetingrequest.md)结束时间的时区。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-104">The **EndTimeZone** element defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<EndTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</EndTimeZone>
```

 <span data-ttu-id="c1ef1-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="c1ef1-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1ef1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c1ef1-106">Attributes and elements</span></span>

<span data-ttu-id="c1ef1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1ef1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c1ef1-108">Attributes</span></span>

|<span data-ttu-id="c1ef1-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="c1ef1-109">**Attribute**</span></span>|<span data-ttu-id="c1ef1-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1ef1-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1ef1-111">Id</span><span class="sxs-lookup"><span data-stu-id="c1ef1-111">Id</span></span>  <br/> |<span data-ttu-id="c1ef1-112">表示时区定义的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="c1ef1-113">名称</span><span class="sxs-lookup"><span data-stu-id="c1ef1-113">Name</span></span>  <br/> |<span data-ttu-id="c1ef1-114">表示时区定义的描述性名称。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1ef1-115">子元素</span><span class="sxs-lookup"><span data-stu-id="c1ef1-115">Child elements</span></span>

|<span data-ttu-id="c1ef1-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="c1ef1-116">**Element**</span></span>|<span data-ttu-id="c1ef1-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1ef1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1ef1-118">课时</span><span class="sxs-lookup"><span data-stu-id="c1ef1-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="c1ef1-119">表示用于定义时区的不同阶段的时间偏移量的[Period](period.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="c1ef1-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="c1ef1-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="c1ef1-121">表示[TransitionsGroup](transitionsgroup.md)元素的数组，这些元素指定时区转换。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="c1ef1-122">移交</span><span class="sxs-lookup"><span data-stu-id="c1ef1-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="c1ef1-123">表示时区转换的数组。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1ef1-124">父元素</span><span class="sxs-lookup"><span data-stu-id="c1ef1-124">Parent elements</span></span>

|<span data-ttu-id="c1ef1-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="c1ef1-125">**Element**</span></span>|<span data-ttu-id="c1ef1-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1ef1-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1ef1-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="c1ef1-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c1ef1-128">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c1ef1-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c1ef1-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c1ef1-130">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1ef1-131">备注</span><span class="sxs-lookup"><span data-stu-id="c1ef1-131">Remarks</span></span>

<span data-ttu-id="c1ef1-132">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c1ef1-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1ef1-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="c1ef1-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1ef1-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="c1ef1-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1ef1-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="c1ef1-135">Schema Name</span></span>  <br/> |<span data-ttu-id="c1ef1-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="c1ef1-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1ef1-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="c1ef1-137">Validation File</span></span>  <br/> |<span data-ttu-id="c1ef1-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1ef1-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1ef1-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="c1ef1-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1ef1-140">False</span><span class="sxs-lookup"><span data-stu-id="c1ef1-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1ef1-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c1ef1-141">See also</span></span>



- [<span data-ttu-id="c1ef1-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c1ef1-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

