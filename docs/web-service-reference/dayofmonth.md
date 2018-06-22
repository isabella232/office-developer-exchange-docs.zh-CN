---
title: DayOfMonth
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfMonth
api_type:
- schema
ms.assetid: 09b7504e-08d8-42f9-88cc-a2a37a2e2b8b
description: DayOfMonth 元素描述定期项目出现一个月中的一天。
ms.openlocfilehash: 0d0d95849a2562e06b88872b2857cc5e6ca67af3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753758"
---
# <a name="dayofmonth"></a><span data-ttu-id="c5907-103">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="c5907-103">DayOfMonth</span></span>

<span data-ttu-id="c5907-104">**DayOfMonth**元素描述定期项目出现一个月中的一天。</span><span class="sxs-lookup"><span data-stu-id="c5907-104">The **DayOfMonth** element describes the day in a month that a recurring item occurs.</span></span> 
  
```xml
<DayOfMonth/>
```

<span data-ttu-id="c5907-105">**int**</span><span class="sxs-lookup"><span data-stu-id="c5907-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c5907-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c5907-106">Attributes and elements</span></span>

<span data-ttu-id="c5907-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c5907-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5907-108">属性</span><span class="sxs-lookup"><span data-stu-id="c5907-108">Attributes</span></span>

<span data-ttu-id="c5907-109">无。</span><span class="sxs-lookup"><span data-stu-id="c5907-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5907-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c5907-110">Child elements</span></span>

<span data-ttu-id="c5907-111">无。</span><span class="sxs-lookup"><span data-stu-id="c5907-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c5907-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c5907-112">Parent elements</span></span>

|<span data-ttu-id="c5907-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c5907-113">**Element**</span></span>|<span data-ttu-id="c5907-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c5907-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5907-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="c5907-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="c5907-116">代表每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="c5907-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="c5907-117">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="c5907-117">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="c5907-118">表示每月重复模式。</span><span class="sxs-lookup"><span data-stu-id="c5907-118">Represents a monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c5907-119">文本值</span><span class="sxs-lookup"><span data-stu-id="c5907-119">Text value</span></span>

<span data-ttu-id="c5907-120">表示一个整数，范围为 1 到 31 文本值为 required。</span><span class="sxs-lookup"><span data-stu-id="c5907-120">A text value that represents an integer in the range of 1 to 31 is required.</span></span> <span data-ttu-id="c5907-121">如果特定月此值大于当月的天数，则假定月份的最后一天。</span><span class="sxs-lookup"><span data-stu-id="c5907-121">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5907-122">备注</span><span class="sxs-lookup"><span data-stu-id="c5907-122">Remarks</span></span>

<span data-ttu-id="c5907-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c5907-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5907-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c5907-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5907-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c5907-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c5907-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c5907-126">Schema name</span></span>  <br/> |<span data-ttu-id="c5907-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="c5907-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c5907-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c5907-128">Validation file</span></span>  <br/> |<span data-ttu-id="c5907-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c5907-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c5907-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c5907-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c5907-131">False</span><span class="sxs-lookup"><span data-stu-id="c5907-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5907-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c5907-132">See also</span></span>

- [<span data-ttu-id="c5907-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c5907-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

