---
title: LastOccurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LastOccurrence
api_type:
- schema
ms.assetid: c9ef0fcb-4265-4e60-9986-fff0f211d00b
description: LastOccurrence 元素表示定期日历项目的最后一个事件。
ms.openlocfilehash: 8771bbed166cfb6fdcf4d1dfe4fa0812013e2667
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459810"
---
# <a name="lastoccurrence"></a><span data-ttu-id="58a06-103">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="58a06-103">LastOccurrence</span></span>

<span data-ttu-id="58a06-104">**LastOccurrence**元素表示定期日历项目的最后一个事件。</span><span class="sxs-lookup"><span data-stu-id="58a06-104">The **LastOccurrence** element represents the last occurrence of a recurring calendar item.</span></span> 
  
```xml
<LastOccurrence>
   <ItemId/>
   <Start/>
   <End/>
   <OriginalStart/>
</LastOccurrence>
```

 <span data-ttu-id="58a06-105">**OccurrenceInfoType**</span><span class="sxs-lookup"><span data-stu-id="58a06-105">**OccurrenceInfoType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58a06-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="58a06-106">Attributes and elements</span></span>

<span data-ttu-id="58a06-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="58a06-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58a06-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="58a06-108">Attributes</span></span>

<span data-ttu-id="58a06-109">无。</span><span class="sxs-lookup"><span data-stu-id="58a06-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58a06-110">子元素</span><span class="sxs-lookup"><span data-stu-id="58a06-110">Child elements</span></span>

|<span data-ttu-id="58a06-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="58a06-111">**Element**</span></span>|<span data-ttu-id="58a06-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="58a06-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58a06-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="58a06-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="58a06-114">包含定期日历项目的最后一个事件的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="58a06-114">Contains the unique identifier and change key of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="58a06-115">开始</span><span class="sxs-lookup"><span data-stu-id="58a06-115">Start</span></span>](start.md) <br/> |<span data-ttu-id="58a06-116">表示定期日历项目的最后一个事件的开始时间。</span><span class="sxs-lookup"><span data-stu-id="58a06-116">Represents the start time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="58a06-117">停止</span><span class="sxs-lookup"><span data-stu-id="58a06-117">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="58a06-118">表示定期日历项目的最后一个事件的结束时间。</span><span class="sxs-lookup"><span data-stu-id="58a06-118">Represents the end time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="58a06-119">OriginalStart</span><span class="sxs-lookup"><span data-stu-id="58a06-119">OriginalStart</span></span>](originalstart.md) <br/> |<span data-ttu-id="58a06-120">表示定期日历项目的上一次发生的原始开始时间。</span><span class="sxs-lookup"><span data-stu-id="58a06-120">Represents the original start time of the last occurrence of a recurring calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="58a06-121">父元素</span><span class="sxs-lookup"><span data-stu-id="58a06-121">Parent elements</span></span>

|<span data-ttu-id="58a06-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="58a06-122">**Element**</span></span>|<span data-ttu-id="58a06-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="58a06-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58a06-124">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="58a06-124">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="58a06-125">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="58a06-125">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="58a06-126">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="58a06-126">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="58a06-127">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="58a06-127">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58a06-128">备注</span><span class="sxs-lookup"><span data-stu-id="58a06-128">Remarks</span></span>

<span data-ttu-id="58a06-129">如果[CalendarItemType](calendaritemtype.md)具有 RecurringMaster 值，则此元素有效。</span><span class="sxs-lookup"><span data-stu-id="58a06-129">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="58a06-130">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="58a06-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58a06-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="58a06-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58a06-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="58a06-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58a06-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="58a06-133">Schema name</span></span>  <br/> |<span data-ttu-id="58a06-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="58a06-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="58a06-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="58a06-135">Validation file</span></span>  <br/> |<span data-ttu-id="58a06-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58a06-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58a06-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="58a06-137">Can be empty</span></span>  <br/> |<span data-ttu-id="58a06-138">False</span><span class="sxs-lookup"><span data-stu-id="58a06-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58a06-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58a06-139">See also</span></span>



- [<span data-ttu-id="58a06-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="58a06-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
  
[<span data-ttu-id="58a06-141">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="58a06-141">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

