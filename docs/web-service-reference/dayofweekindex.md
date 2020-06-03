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
description: DayOfWeekIndex 元素描述相对定期模式中使用某个月中的哪一周。
ms.openlocfilehash: c9235d83a944f9c8883439dd2adf190b88977f16
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529208"
---
# <a name="dayofweekindex"></a><span data-ttu-id="43b7a-103">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="43b7a-103">DayOfWeekIndex</span></span>

<span data-ttu-id="43b7a-104">**DayOfWeekIndex**元素描述相对定期模式中使用某个月中的哪一周。</span><span class="sxs-lookup"><span data-stu-id="43b7a-104">The **DayOfWeekIndex** element describes which week in a month is used in a relative recurrence pattern.</span></span> 
  
```xml
<DayOfWeekIndex/>
```

<span data-ttu-id="43b7a-105">**DayOfWeekIndexType**</span><span class="sxs-lookup"><span data-stu-id="43b7a-105">**DayOfWeekIndexType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="43b7a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="43b7a-106">Attributes and elements</span></span>

<span data-ttu-id="43b7a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="43b7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43b7a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="43b7a-108">Attributes</span></span>

<span data-ttu-id="43b7a-109">无。</span><span class="sxs-lookup"><span data-stu-id="43b7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="43b7a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="43b7a-110">Child elements</span></span>

<span data-ttu-id="43b7a-111">无。</span><span class="sxs-lookup"><span data-stu-id="43b7a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43b7a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="43b7a-112">Parent elements</span></span>

|<span data-ttu-id="43b7a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="43b7a-113">**Element**</span></span>|<span data-ttu-id="43b7a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="43b7a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43b7a-115">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="43b7a-115">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="43b7a-116">介绍相对年定期模式。</span><span class="sxs-lookup"><span data-stu-id="43b7a-116">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="43b7a-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="43b7a-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="43b7a-118">介绍相对月定期模式。</span><span class="sxs-lookup"><span data-stu-id="43b7a-118">Describes a relative monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="43b7a-119">文本值</span><span class="sxs-lookup"><span data-stu-id="43b7a-119">Text value</span></span>

<span data-ttu-id="43b7a-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="43b7a-120">A text value is required.</span></span> <span data-ttu-id="43b7a-121">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="43b7a-121">The following are the possible values:</span></span>
  
- <span data-ttu-id="43b7a-122">First</span><span class="sxs-lookup"><span data-stu-id="43b7a-122">First</span></span>    
- <span data-ttu-id="43b7a-123">秒</span><span class="sxs-lookup"><span data-stu-id="43b7a-123">Second</span></span>    
- <span data-ttu-id="43b7a-124">第三节</span><span class="sxs-lookup"><span data-stu-id="43b7a-124">Third</span></span>    
- <span data-ttu-id="43b7a-125">四分之一</span><span class="sxs-lookup"><span data-stu-id="43b7a-125">Fourth</span></span>    
- <span data-ttu-id="43b7a-126">最后一个</span><span class="sxs-lookup"><span data-stu-id="43b7a-126">Last</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43b7a-127">备注</span><span class="sxs-lookup"><span data-stu-id="43b7a-127">Remarks</span></span>

<span data-ttu-id="43b7a-128">例如，一个月的第二个星期一可能发生在该月的第三个星期。</span><span class="sxs-lookup"><span data-stu-id="43b7a-128">For example, the second Monday of a month may occur in the third week of that month.</span></span> <span data-ttu-id="43b7a-129">如果一个月从星期五开始，则该月的第一周仅包含几天，并且不包含星期一。</span><span class="sxs-lookup"><span data-stu-id="43b7a-129">If a month starts on a Friday, the first week of the month only contains a few days and does not contain a Monday.</span></span> <span data-ttu-id="43b7a-130">因此，第一个星期一必须在第二周发生。</span><span class="sxs-lookup"><span data-stu-id="43b7a-130">Therefore, the first Monday would have to occur in the second week.</span></span>
  
<span data-ttu-id="43b7a-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="43b7a-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43b7a-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="43b7a-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43b7a-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="43b7a-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="43b7a-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="43b7a-134">Schema name</span></span>  <br/> |<span data-ttu-id="43b7a-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="43b7a-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="43b7a-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="43b7a-136">Validation file</span></span>  <br/> |<span data-ttu-id="43b7a-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="43b7a-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="43b7a-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="43b7a-138">Can be empty</span></span>  <br/> |<span data-ttu-id="43b7a-139">False</span><span class="sxs-lookup"><span data-stu-id="43b7a-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43b7a-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="43b7a-140">See also</span></span>

- [<span data-ttu-id="43b7a-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="43b7a-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

