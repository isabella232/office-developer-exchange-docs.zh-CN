---
title: 事件（时区转换）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Occurrence
api_type:
- schema
ms.assetid: 5c1142b1-c51f-42e1-bbb2-57e00cad0fdb
description: 具体值元素表示发生时区转换的月份中的一周中的某一天的匹配项。
ms.openlocfilehash: 846f6b22f43bcda07b9408d768d0845a5acfe668
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467975"
---
# <a name="occurrence-time-zone-transition"></a><span data-ttu-id="cbbcd-103">事件（时区转换）</span><span class="sxs-lookup"><span data-stu-id="cbbcd-103">Occurrence (Time Zone Transition)</span></span>

<span data-ttu-id="cbbcd-104">**具体**值元素表示发生时区转换的月份中的一周中的某一天的匹配项。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-104">The **Occurrence** element represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> 
  
```xml
<Occurrence/>
```

<span data-ttu-id="cbbcd-105">**int**</span><span class="sxs-lookup"><span data-stu-id="cbbcd-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="cbbcd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cbbcd-106">Attributes and elements</span></span>

<span data-ttu-id="cbbcd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbbcd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cbbcd-108">Attributes</span></span>

<span data-ttu-id="cbbcd-109">无。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbbcd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cbbcd-110">Child elements</span></span>

<span data-ttu-id="cbbcd-111">无。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cbbcd-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cbbcd-112">Parent elements</span></span>

|<span data-ttu-id="cbbcd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbbcd-113">**Element**</span></span>|<span data-ttu-id="cbbcd-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="cbbcd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbbcd-115">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="cbbcd-115">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="cbbcd-116">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-116">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cbbcd-117">文本值</span><span class="sxs-lookup"><span data-stu-id="cbbcd-117">Text value</span></span>

<span data-ttu-id="cbbcd-118">Text 值是一个整数，表示发生时区转换的月份中的某一天的匹配项。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-118">The text value is an integer that represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> <span data-ttu-id="cbbcd-119">下表列出了可能的值。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="cbbcd-120">**值**</span><span class="sxs-lookup"><span data-stu-id="cbbcd-120">**Value**</span></span>|<span data-ttu-id="cbbcd-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbbcd-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cbbcd-122">1</span><span class="sxs-lookup"><span data-stu-id="cbbcd-122">1</span></span>  <br/> |<span data-ttu-id="cbbcd-123">指定的一周中第一天的第一次发生，从月初算起。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-123">The first occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="cbbcd-124">双面</span><span class="sxs-lookup"><span data-stu-id="cbbcd-124">2</span></span>  <br/> |<span data-ttu-id="cbbcd-125">第二次在一周中的某一天中指定的一天。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-125">The second occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="cbbcd-126">第三章</span><span class="sxs-lookup"><span data-stu-id="cbbcd-126">3</span></span>  <br/> |<span data-ttu-id="cbbcd-127">一周中指定日期的第三个匹配项。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-127">The third occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="cbbcd-128">4 </span><span class="sxs-lookup"><span data-stu-id="cbbcd-128">4</span></span>  <br/> |<span data-ttu-id="cbbcd-129">从一月开始算起的指定星期几的第四个事件。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-129">The fourth occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="cbbcd-130">-1</span><span class="sxs-lookup"><span data-stu-id="cbbcd-130">-1</span></span>  <br/> |<span data-ttu-id="cbbcd-131">一周中指定的一天的第一个匹配项，从月初结束。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-131">The first occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="cbbcd-132">-2</span><span class="sxs-lookup"><span data-stu-id="cbbcd-132">-2</span></span>  <br/> |<span data-ttu-id="cbbcd-133">第二次出现在一周中的某一天，从月末结束。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-133">The second occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="cbbcd-134">-3</span><span class="sxs-lookup"><span data-stu-id="cbbcd-134">-3</span></span>  <br/> |<span data-ttu-id="cbbcd-135">一周中指定的某一天的第三个事件（月份结束）。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-135">The third occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="cbbcd-136">-4</span><span class="sxs-lookup"><span data-stu-id="cbbcd-136">-4</span></span>  <br/> |<span data-ttu-id="cbbcd-137">一周中指定日期的第四个事件（月份结束）。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-137">The fourth occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbbcd-138">备注</span><span class="sxs-lookup"><span data-stu-id="cbbcd-138">Remarks</span></span>

<span data-ttu-id="cbbcd-139">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cbbcd-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cbbcd-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="cbbcd-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbbcd-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="cbbcd-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cbbcd-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="cbbcd-142">Schema Name</span></span>  <br/> |<span data-ttu-id="cbbcd-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="cbbcd-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="cbbcd-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="cbbcd-144">Validation File</span></span>  <br/> |<span data-ttu-id="cbbcd-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cbbcd-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cbbcd-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="cbbcd-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="cbbcd-147">False</span><span class="sxs-lookup"><span data-stu-id="cbbcd-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbbcd-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cbbcd-148">See also</span></span>

- [<span data-ttu-id="cbbcd-149">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cbbcd-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

