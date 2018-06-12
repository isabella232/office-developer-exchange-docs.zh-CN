---
title: 出现 （所在的时区转换）
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
description: 出现元素均表示所在的时区转换发生当月星期几的匹配项。
ms.openlocfilehash: bc5160480cc6881bb9d724aa61323f5717d1f2fa
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826636"
---
# <a name="occurrence-time-zone-transition"></a><span data-ttu-id="fa6ea-103">出现 （所在的时区转换）</span><span class="sxs-lookup"><span data-stu-id="fa6ea-103">Occurrence (Time Zone Transition)</span></span>

<span data-ttu-id="fa6ea-104">**出现**元素均表示所在的时区转换发生当月星期几的匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-104">The **Occurrence** element represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> 
  
```xml
<Occurrence/>
```

<span data-ttu-id="fa6ea-105">**int**</span><span class="sxs-lookup"><span data-stu-id="fa6ea-105">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fa6ea-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa6ea-106">Attributes and elements</span></span>

<span data-ttu-id="fa6ea-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa6ea-108">属性</span><span class="sxs-lookup"><span data-stu-id="fa6ea-108">Attributes</span></span>

<span data-ttu-id="fa6ea-109">无。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa6ea-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fa6ea-110">Child elements</span></span>

<span data-ttu-id="fa6ea-111">无。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fa6ea-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fa6ea-112">Parent elements</span></span>

|<span data-ttu-id="fa6ea-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa6ea-113">**Element**</span></span>|<span data-ttu-id="fa6ea-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa6ea-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa6ea-115">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="fa6ea-115">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="fa6ea-116">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-116">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fa6ea-117">文本值</span><span class="sxs-lookup"><span data-stu-id="fa6ea-117">Text value</span></span>

<span data-ttu-id="fa6ea-118">文本值是一个整数，表示发生所在的时区切换当月星期几的匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-118">The text value is an integer that represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span> <span data-ttu-id="fa6ea-119">下表列出了可能的值。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-119">The following table lists the possible values.</span></span>
  
|<span data-ttu-id="fa6ea-120">**值**</span><span class="sxs-lookup"><span data-stu-id="fa6ea-120">**Value**</span></span>|<span data-ttu-id="fa6ea-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa6ea-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fa6ea-122">1</span><span class="sxs-lookup"><span data-stu-id="fa6ea-122">1</span></span>  <br/> |<span data-ttu-id="fa6ea-123">指定的日期相应月份的从头一周的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-123">The first occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="fa6ea-124">2</span><span class="sxs-lookup"><span data-stu-id="fa6ea-124">2</span></span>  <br/> |<span data-ttu-id="fa6ea-125">指定星期几从头相应月份的第二个匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-125">The second occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="fa6ea-126">3</span><span class="sxs-lookup"><span data-stu-id="fa6ea-126">3</span></span>  <br/> |<span data-ttu-id="fa6ea-127">第三个月的开始从一周中的指定日期发生。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-127">The third occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="fa6ea-128">4</span><span class="sxs-lookup"><span data-stu-id="fa6ea-128">4</span></span>  <br/> |<span data-ttu-id="fa6ea-129">指定的日期相应月份的从头一周的第四个匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-129">The fourth occurrence of the specified day of the week from the beginning of the month.</span></span>  <br/> |
|<span data-ttu-id="fa6ea-130">-1</span><span class="sxs-lookup"><span data-stu-id="fa6ea-130">-1</span></span>  <br/> |<span data-ttu-id="fa6ea-131">指定一天从相应月份的末尾一周中的第一个匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-131">The first occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="fa6ea-132">-2</span><span class="sxs-lookup"><span data-stu-id="fa6ea-132">-2</span></span>  <br/> |<span data-ttu-id="fa6ea-133">指定一天从相应月份的末尾一周中的第二个匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-133">The second occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="fa6ea-134">-3</span><span class="sxs-lookup"><span data-stu-id="fa6ea-134">-3</span></span>  <br/> |<span data-ttu-id="fa6ea-135">指定一天从相应月份的末尾一周中的第三个匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-135">The third occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
|<span data-ttu-id="fa6ea-136">-4</span><span class="sxs-lookup"><span data-stu-id="fa6ea-136">-4</span></span>  <br/> |<span data-ttu-id="fa6ea-137">指定一天从相应月份的末尾一周中的第四个匹配项。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-137">The fourth occurrence of the specified day of the week from the end of the month.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa6ea-138">备注</span><span class="sxs-lookup"><span data-stu-id="fa6ea-138">Remarks</span></span>

<span data-ttu-id="fa6ea-139">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa6ea-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa6ea-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa6ea-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa6ea-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa6ea-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa6ea-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa6ea-142">Schema Name</span></span>  <br/> |<span data-ttu-id="fa6ea-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="fa6ea-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="fa6ea-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa6ea-144">Validation File</span></span>  <br/> |<span data-ttu-id="fa6ea-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fa6ea-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa6ea-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa6ea-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="fa6ea-147">False</span><span class="sxs-lookup"><span data-stu-id="fa6ea-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa6ea-148">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa6ea-148">See also</span></span>

- [<span data-ttu-id="fa6ea-149">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fa6ea-149">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
