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
description: FirstOccurrence 元素表示定期日历项目的第一个事件。
ms.openlocfilehash: 22ee9018df1e89a3783c4dfb56aaf065b2c8ea6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466295"
---
# <a name="firstoccurrence"></a><span data-ttu-id="caa26-103">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="caa26-103">FirstOccurrence</span></span>

<span data-ttu-id="caa26-104">**FirstOccurrence**元素表示定期日历项目的第一个事件。</span><span class="sxs-lookup"><span data-stu-id="caa26-104">The **FirstOccurrence** element represents the first occurrence of a recurring calendar item.</span></span> 
  
```xml
<FirstOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</FirstOccurrence>
```

 <span data-ttu-id="caa26-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="caa26-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="caa26-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="caa26-106">Attributes and elements</span></span>

<span data-ttu-id="caa26-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="caa26-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="caa26-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="caa26-108">Attributes</span></span>

<span data-ttu-id="caa26-109">无。</span><span class="sxs-lookup"><span data-stu-id="caa26-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="caa26-110">子元素</span><span class="sxs-lookup"><span data-stu-id="caa26-110">Child elements</span></span>

|<span data-ttu-id="caa26-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="caa26-111">**Element**</span></span>|<span data-ttu-id="caa26-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="caa26-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="caa26-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="caa26-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="caa26-114">包含定期日历项目的第一个匹配项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="caa26-114">Contains the unique identifier and change key of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="caa26-115">开始</span><span class="sxs-lookup"><span data-stu-id="caa26-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="caa26-116">表示定期日历项目的第一次出现的开始时间。</span><span class="sxs-lookup"><span data-stu-id="caa26-116">Represents the start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="caa26-117">停止</span><span class="sxs-lookup"><span data-stu-id="caa26-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="caa26-118">表示定期日历项目的第一次出现的结束时间。</span><span class="sxs-lookup"><span data-stu-id="caa26-118">Represents the end time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="caa26-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="caa26-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="caa26-120">表示定期日历项目的第一次出现的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="caa26-120">Represents the original start time of the first occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="caa26-121">父元素</span><span class="sxs-lookup"><span data-stu-id="caa26-121">Parent elements</span></span>

|<span data-ttu-id="caa26-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="caa26-122">**Element**</span></span>|<span data-ttu-id="caa26-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="caa26-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="caa26-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="caa26-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="caa26-125">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="caa26-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="caa26-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="caa26-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="caa26-127">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="caa26-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="caa26-128">备注</span><span class="sxs-lookup"><span data-stu-id="caa26-128">Remarks</span></span>

<span data-ttu-id="caa26-129">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="caa26-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="caa26-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="caa26-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="caa26-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="caa26-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="caa26-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="caa26-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="caa26-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="caa26-133">Schema name</span></span>  <br/> |<span data-ttu-id="caa26-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="caa26-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="caa26-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="caa26-135">Validation file</span></span>  <br/> |<span data-ttu-id="caa26-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="caa26-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="caa26-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="caa26-137">Can be empty</span></span>  <br/> |<span data-ttu-id="caa26-138">False</span><span class="sxs-lookup"><span data-stu-id="caa26-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="caa26-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="caa26-139">See also</span></span>



- [<span data-ttu-id="caa26-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="caa26-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="caa26-141">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="caa26-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

