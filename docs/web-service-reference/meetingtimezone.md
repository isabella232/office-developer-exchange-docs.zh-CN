---
title: MeetingTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingTimeZone
api_type:
- schema
ms.assetid: 413b47d9-8126-462c-9a4f-4e771a5e8889
description: MeetingTimeZone 元素均表示承载会议的位置所在的时区。
ms.openlocfilehash: ce014ac6d8841e451927a94049cb4e8860886fdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826440"
---
# <a name="meetingtimezone"></a><span data-ttu-id="11621-103">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="11621-103">MeetingTimeZone</span></span>

<span data-ttu-id="11621-104">**MeetingTimeZone**元素均表示承载会议的位置所在的时区。</span><span class="sxs-lookup"><span data-stu-id="11621-104">The **MeetingTimeZone** element represents the time zone of the location where the meeting is hosted.</span></span> 
  
```xml
<MeetingTimeZone>
   <BaseOffset/>
   <Standard/>
   <Daylight/>
</MeetingTimeZone>
```

 <span data-ttu-id="11621-105">**TimeZoneType**</span><span class="sxs-lookup"><span data-stu-id="11621-105">**TimeZoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11621-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="11621-106">Attributes and elements</span></span>

<span data-ttu-id="11621-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="11621-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11621-108">属性</span><span class="sxs-lookup"><span data-stu-id="11621-108">Attributes</span></span>

|<span data-ttu-id="11621-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="11621-109">**Attribute**</span></span>|<span data-ttu-id="11621-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="11621-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11621-111">**TimeZoneName**</span><span class="sxs-lookup"><span data-stu-id="11621-111">**TimeZoneName**</span></span> <br/> |<span data-ttu-id="11621-112">介绍时区的名称。</span><span class="sxs-lookup"><span data-stu-id="11621-112">Describes the name of the time zone.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="11621-113">子元素</span><span class="sxs-lookup"><span data-stu-id="11621-113">Child elements</span></span>

|<span data-ttu-id="11621-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="11621-114">**Element**</span></span>|<span data-ttu-id="11621-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="11621-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11621-116">BaseOffset</span><span class="sxs-lookup"><span data-stu-id="11621-116">BaseOffset</span></span>](baseoffset.md) <br/> |<span data-ttu-id="11621-117">代表为当前时区偏移 UTC 小时。</span><span class="sxs-lookup"><span data-stu-id="11621-117">Represents the hourly offset from UTC for the current time zone.</span></span>  <br/> |
|[<span data-ttu-id="11621-118">标准</span><span class="sxs-lookup"><span data-stu-id="11621-118">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="11621-119">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="11621-119">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="11621-120">夏时制</span><span class="sxs-lookup"><span data-stu-id="11621-120">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="11621-121">表示的日期和时间更改时从标准时间到夏时制的时间。</span><span class="sxs-lookup"><span data-stu-id="11621-121">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="11621-122">父元素</span><span class="sxs-lookup"><span data-stu-id="11621-122">Parent elements</span></span>

|<span data-ttu-id="11621-123">**元素**</span><span class="sxs-lookup"><span data-stu-id="11621-123">**Element**</span></span>|<span data-ttu-id="11621-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="11621-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11621-125">日历项目</span><span class="sxs-lookup"><span data-stu-id="11621-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="11621-126">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="11621-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="11621-127">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="11621-127">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="11621-128">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="11621-128">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11621-129">备注</span><span class="sxs-lookup"><span data-stu-id="11621-129">Remarks</span></span>

<span data-ttu-id="11621-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="11621-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11621-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="11621-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11621-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="11621-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11621-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="11621-133">Schema Name</span></span>  <br/> |<span data-ttu-id="11621-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="11621-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="11621-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="11621-135">Validation File</span></span>  <br/> |<span data-ttu-id="11621-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="11621-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11621-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="11621-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="11621-138">False</span><span class="sxs-lookup"><span data-stu-id="11621-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11621-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="11621-139">See also</span></span>



- [<span data-ttu-id="11621-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="11621-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

