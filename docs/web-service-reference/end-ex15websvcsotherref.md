---
title: End
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- End
api_type:
- schema
ms.assetid: 72329821-32ff-495d-b6e5-fdc011003c2e
description: 结束元素表示持续时间的末尾。
ms.openlocfilehash: 90eea4fc545fae083e5675225665e517b502ba6f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754110"
---
# <a name="end"></a><span data-ttu-id="44f8b-103">End</span><span class="sxs-lookup"><span data-stu-id="44f8b-103">End</span></span>

<span data-ttu-id="44f8b-104">**结束**元素表示持续时间的末尾。</span><span class="sxs-lookup"><span data-stu-id="44f8b-104">The **End** element represents the end of a duration.</span></span> 
  
```xml
<End/>
```

 <span data-ttu-id="44f8b-105">**DateTime**</span><span class="sxs-lookup"><span data-stu-id="44f8b-105">**DateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44f8b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="44f8b-106">Attributes and elements</span></span>

<span data-ttu-id="44f8b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="44f8b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44f8b-108">属性</span><span class="sxs-lookup"><span data-stu-id="44f8b-108">Attributes</span></span>

<span data-ttu-id="44f8b-109">无。</span><span class="sxs-lookup"><span data-stu-id="44f8b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44f8b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="44f8b-110">Child elements</span></span>

<span data-ttu-id="44f8b-111">无。</span><span class="sxs-lookup"><span data-stu-id="44f8b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="44f8b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="44f8b-112">Parent elements</span></span>

|<span data-ttu-id="44f8b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="44f8b-113">**Element**</span></span>|<span data-ttu-id="44f8b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="44f8b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44f8b-115">日历项目</span><span class="sxs-lookup"><span data-stu-id="44f8b-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="44f8b-116">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="44f8b-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44f8b-117">FirstOccurrence</span><span class="sxs-lookup"><span data-stu-id="44f8b-117">FirstOccurrence</span></span>](firstoccurrence.md) <br/> |<span data-ttu-id="44f8b-118">代表定期日历项目的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="44f8b-118">Represents the first occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44f8b-119">LastOccurrence</span><span class="sxs-lookup"><span data-stu-id="44f8b-119">LastOccurrence</span></span>](lastoccurrence.md) <br/> |<span data-ttu-id="44f8b-120">代表定期日历项目的最后一个实例。</span><span class="sxs-lookup"><span data-stu-id="44f8b-120">Represents the last occurrence of a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="44f8b-121">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="44f8b-121">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="44f8b-122">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="44f8b-122">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="44f8b-123">匹配项</span><span class="sxs-lookup"><span data-stu-id="44f8b-123">Occurrence</span></span>](occurrence.md) <br/> |<span data-ttu-id="44f8b-124">代表定期日历项目的一个已修改匹配项。</span><span class="sxs-lookup"><span data-stu-id="44f8b-124">Represents a single modified occurrence of a recurring calendar item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="44f8b-125">文本值</span><span class="sxs-lookup"><span data-stu-id="44f8b-125">Text value</span></span>

<span data-ttu-id="44f8b-126">文本值表示的末尾持续时间。</span><span class="sxs-lookup"><span data-stu-id="44f8b-126">The text value represents the end of a duration.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44f8b-127">注解</span><span class="sxs-lookup"><span data-stu-id="44f8b-127">Remarks</span></span>

<span data-ttu-id="44f8b-128">UpdateItem 操作可以设置 Exchange 存储项目的[开始](start.md)和**结束**时间。</span><span class="sxs-lookup"><span data-stu-id="44f8b-128">The UpdateItem operation can set the [Start](start.md) and **End** time of an Exchange store item.</span></span> <span data-ttu-id="44f8b-129">在 UpdateItem 请求中，您可以不还设置的**结束**时间设置[开始](start.md)时间。</span><span class="sxs-lookup"><span data-stu-id="44f8b-129">In an UpdateItem request, you can set the [Start](start.md) time without also setting the **End** time.</span></span> <span data-ttu-id="44f8b-130">如果[开始](start.md)时间晚于的**结束**时间，这会导致错误。</span><span class="sxs-lookup"><span data-stu-id="44f8b-130">This can cause an error if the [Start](start.md) time is later than the **End** time.</span></span> <span data-ttu-id="44f8b-131">注意客户端应用程序必须执行的**结束**时间的[开始](start.md)时间才能保留持续时间的更改时调整。</span><span class="sxs-lookup"><span data-stu-id="44f8b-131">Be aware that client applications must perform adjustments to the **End** time when that [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
 <span data-ttu-id="44f8b-132">**注释**如果没有等于每周定期模式的第一个匹配项的日期的定期主项目的[开始](start.md)和**结束**日期，所在的时区偏移的信息将丢失。</span><span class="sxs-lookup"><span data-stu-id="44f8b-132">**Note** The time zone offset information is lost if the [Start](start.md) and **End** dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="44f8b-133">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="44f8b-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44f8b-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="44f8b-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44f8b-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="44f8b-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="44f8b-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="44f8b-136">Schema Name</span></span>  <br/> |<span data-ttu-id="44f8b-137">类型架构</span><span class="sxs-lookup"><span data-stu-id="44f8b-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="44f8b-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="44f8b-138">Validation File</span></span>  <br/> |<span data-ttu-id="44f8b-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="44f8b-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="44f8b-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="44f8b-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="44f8b-141">False</span><span class="sxs-lookup"><span data-stu-id="44f8b-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44f8b-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="44f8b-142">See also</span></span>



[<span data-ttu-id="44f8b-143">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="44f8b-143">WeeklyRecurrence</span></span>](weeklyrecurrence.md)
  
 <span data-ttu-id="44f8b-144">**End**</span><span class="sxs-lookup"><span data-stu-id="44f8b-144">**End**</span></span>


- [<span data-ttu-id="44f8b-145">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="44f8b-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

