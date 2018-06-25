---
title: DayOfWeekIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeekIndex
api_type:
- schema
ms.assetid: 82420338-a1f7-4887-b338-b2d93b2c2bf1
description: DayOfWeekIndex 元素描述一个月中的一周的相对定期模式中使用。
ms.openlocfilehash: 4987685d0c3cefdfad4f5be1368776a5b859bf94
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753767"
---
# <a name="dayofweekindex"></a><span data-ttu-id="19a88-103">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="19a88-103">DayOfWeekIndex</span></span>

<span data-ttu-id="19a88-104">**DayOfWeekIndex**元素描述一个月中的一周的相对定期模式中使用。</span><span class="sxs-lookup"><span data-stu-id="19a88-104">The **DayOfWeekIndex** element describes which week in a month is used in a relative recurrence pattern.</span></span> 
  
```xml
<DayOfWeekIndex/>
```

<span data-ttu-id="19a88-105">**DayOfWeekIndexType**</span><span class="sxs-lookup"><span data-stu-id="19a88-105">**DayOfWeekIndexType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="19a88-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="19a88-106">Attributes and elements</span></span>

<span data-ttu-id="19a88-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="19a88-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19a88-108">属性</span><span class="sxs-lookup"><span data-stu-id="19a88-108">Attributes</span></span>

<span data-ttu-id="19a88-109">无。</span><span class="sxs-lookup"><span data-stu-id="19a88-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19a88-110">子元素</span><span class="sxs-lookup"><span data-stu-id="19a88-110">Child elements</span></span>

<span data-ttu-id="19a88-111">无。</span><span class="sxs-lookup"><span data-stu-id="19a88-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19a88-112">父元素</span><span class="sxs-lookup"><span data-stu-id="19a88-112">Parent elements</span></span>

|<span data-ttu-id="19a88-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="19a88-113">**Element**</span></span>|<span data-ttu-id="19a88-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="19a88-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19a88-115">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="19a88-115">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="19a88-116">介绍相对的每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="19a88-116">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="19a88-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="19a88-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="19a88-118">介绍相对的每月定期模式。</span><span class="sxs-lookup"><span data-stu-id="19a88-118">Describes a relative monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19a88-119">文本值</span><span class="sxs-lookup"><span data-stu-id="19a88-119">Text value</span></span>

<span data-ttu-id="19a88-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="19a88-120">A text value is required.</span></span> <span data-ttu-id="19a88-121">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="19a88-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="19a88-122">第一节</span><span class="sxs-lookup"><span data-stu-id="19a88-122">First</span></span>    
- <span data-ttu-id="19a88-123">第二节</span><span class="sxs-lookup"><span data-stu-id="19a88-123">Second</span></span>    
- <span data-ttu-id="19a88-124">第三节</span><span class="sxs-lookup"><span data-stu-id="19a88-124">Third</span></span>    
- <span data-ttu-id="19a88-125">第四</span><span class="sxs-lookup"><span data-stu-id="19a88-125">Fourth</span></span>    
- <span data-ttu-id="19a88-126">最后一个</span><span class="sxs-lookup"><span data-stu-id="19a88-126">Last</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19a88-127">注解</span><span class="sxs-lookup"><span data-stu-id="19a88-127">Remarks</span></span>

<span data-ttu-id="19a88-128">例如，某个月份的第二个星期一可能会出现在月的第三个星期。</span><span class="sxs-lookup"><span data-stu-id="19a88-128">For example, the second Monday of a month may occur in the third week of that month.</span></span> <span data-ttu-id="19a88-129">如果一个月开始在某个星期五，相应月份的第一周将仅包含几天，并且不包含星期一。</span><span class="sxs-lookup"><span data-stu-id="19a88-129">If a month starts on a Friday, the first week of the month only contains a few days and does not contain a Monday.</span></span> <span data-ttu-id="19a88-130">因此的第一个星期一者必须发生在第二个星期。</span><span class="sxs-lookup"><span data-stu-id="19a88-130">Therefore, the first Monday would have to occur in the second week.</span></span>
  
<span data-ttu-id="19a88-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="19a88-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19a88-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="19a88-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19a88-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="19a88-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19a88-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="19a88-134">Schema name</span></span>  <br/> |<span data-ttu-id="19a88-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="19a88-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="19a88-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="19a88-136">Validation file</span></span>  <br/> |<span data-ttu-id="19a88-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19a88-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="19a88-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="19a88-138">Can be empty</span></span>  <br/> |<span data-ttu-id="19a88-139">False</span><span class="sxs-lookup"><span data-stu-id="19a88-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19a88-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="19a88-140">See also</span></span>

- [<span data-ttu-id="19a88-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="19a88-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

