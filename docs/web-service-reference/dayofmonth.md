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
description: DayOfMonth 元素描述定期项目出现在一个月中的哪一天。
ms.openlocfilehash: dc333a46283d5e8eba3a79f62f8c22c22f56e190
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44442827"
---
# <a name="dayofmonth"></a><span data-ttu-id="4c1a4-103">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="4c1a4-103">DayOfMonth</span></span>

<span data-ttu-id="4c1a4-104">**DayOfMonth**元素描述定期项目出现在一个月中的哪一天。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-104">The **DayOfMonth** element describes the day in a month that a recurring item occurs.</span></span> 
  
```xml
<DayOfMonth/>
```

<span data-ttu-id="4c1a4-105">**int**</span><span class="sxs-lookup"><span data-stu-id="4c1a4-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4c1a4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4c1a4-106">Attributes and elements</span></span>

<span data-ttu-id="4c1a4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c1a4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4c1a4-108">Attributes</span></span>

<span data-ttu-id="4c1a4-109">无。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c1a4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4c1a4-110">Child elements</span></span>

<span data-ttu-id="4c1a4-111">无。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4c1a4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4c1a4-112">Parent elements</span></span>

|<span data-ttu-id="4c1a4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4c1a4-113">**Element**</span></span>|<span data-ttu-id="4c1a4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4c1a4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c1a4-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4c1a4-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="4c1a4-116">代表每年定期模式。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="4c1a4-117">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4c1a4-117">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="4c1a4-118">表示每月重复模式。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-118">Represents a monthly recurrence pattern.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4c1a4-119">文本值</span><span class="sxs-lookup"><span data-stu-id="4c1a4-119">Text value</span></span>

<span data-ttu-id="4c1a4-120">一个代表1到31范围内的整数的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-120">A text value that represents an integer in the range of 1 to 31 is required.</span></span> <span data-ttu-id="4c1a4-121">如果特定月份的值大于该月中的天数，则假定为该月的最后一天。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-121">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c1a4-122">说明</span><span class="sxs-lookup"><span data-stu-id="4c1a4-122">Remarks</span></span>

<span data-ttu-id="4c1a4-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4c1a4-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c1a4-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="4c1a4-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c1a4-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="4c1a4-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4c1a4-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="4c1a4-126">Schema name</span></span>  <br/> |<span data-ttu-id="4c1a4-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="4c1a4-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="4c1a4-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="4c1a4-128">Validation file</span></span>  <br/> |<span data-ttu-id="4c1a4-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4c1a4-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4c1a4-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="4c1a4-130">Can be empty</span></span>  <br/> |<span data-ttu-id="4c1a4-131">False</span><span class="sxs-lookup"><span data-stu-id="4c1a4-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c1a4-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4c1a4-132">See also</span></span>

- [<span data-ttu-id="4c1a4-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4c1a4-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

