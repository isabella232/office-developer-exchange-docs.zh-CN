---
title: FirstOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FirstOccurrence
api_type:
- schema
ms.assetid: d6748860-ce0d-4d2e-b7e4-9ed834f1e45a
description: FirstOccurrence 元素均表示定期日历项目的第一个匹配项。
ms.openlocfilehash: e5244e74bdd5a4b8e22c6e63811db53b46fa353a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754374"
---
# <a name="firstoccurrence"></a><span data-ttu-id="d5d66-103">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="d5d66-103">FirstOccurrence</span></span>

<span data-ttu-id="d5d66-104">**FirstOccurrence**元素均表示定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="d5d66-104">The **FirstOccurrence** element represents the first occurrence of a recurring calendar item.</span></span> 
  
```xml
<FirstOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</FirstOccurrence>
```

 <span data-ttu-id="d5d66-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="d5d66-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5d66-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d5d66-106">Attributes and elements</span></span>

<span data-ttu-id="d5d66-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d5d66-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5d66-108">属性</span><span class="sxs-lookup"><span data-stu-id="d5d66-108">Attributes</span></span>

<span data-ttu-id="d5d66-109">无。</span><span class="sxs-lookup"><span data-stu-id="d5d66-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5d66-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d5d66-110">Child elements</span></span>

|<span data-ttu-id="d5d66-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d5d66-111">**Element**</span></span>|<span data-ttu-id="d5d66-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d5d66-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5d66-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="d5d66-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d5d66-114">包含定期日历项目的第一个匹配项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="d5d66-114">Contains the unique identifier and change key of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d5d66-115">Start</span><span class="sxs-lookup"><span data-stu-id="d5d66-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="d5d66-116">代表定期日历项目的第一个匹配项的开始时间。</span><span class="sxs-lookup"><span data-stu-id="d5d66-116">Represents the start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d5d66-117">结束</span><span class="sxs-lookup"><span data-stu-id="d5d66-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d5d66-118">代表定期日历项目的第一个出现的结束时间。</span><span class="sxs-lookup"><span data-stu-id="d5d66-118">Represents the end time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d5d66-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="d5d66-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="d5d66-120">代表定期日历项目的第一个匹配项的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="d5d66-120">Represents the original start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5d66-121">父元素</span><span class="sxs-lookup"><span data-stu-id="d5d66-121">Parent elements</span></span>

|<span data-ttu-id="d5d66-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="d5d66-122">**Element**</span></span>|<span data-ttu-id="d5d66-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="d5d66-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5d66-124">日历项目</span><span class="sxs-lookup"><span data-stu-id="d5d66-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d5d66-125">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="d5d66-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d5d66-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d5d66-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d5d66-127">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="d5d66-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d5d66-128">备注</span><span class="sxs-lookup"><span data-stu-id="d5d66-128">Remarks</span></span>

<span data-ttu-id="d5d66-129">此元素是如果[CalendarItemType](calendaritemtype.md) RecurringMaster 值有效。</span><span class="sxs-lookup"><span data-stu-id="d5d66-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="d5d66-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d5d66-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5d66-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="d5d66-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5d66-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="d5d66-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d5d66-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="d5d66-133">Schema name</span></span>  <br/> |<span data-ttu-id="d5d66-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="d5d66-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="d5d66-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="d5d66-135">Validation file</span></span>  <br/> |<span data-ttu-id="d5d66-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d5d66-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d5d66-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="d5d66-137">Can be empty</span></span>  <br/> |<span data-ttu-id="d5d66-138">False</span><span class="sxs-lookup"><span data-stu-id="d5d66-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5d66-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5d66-139">See also</span></span>



- [<span data-ttu-id="d5d66-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d5d66-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="d5d66-141">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="d5d66-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

