---
title: DailyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRegeneration
api_type:
- schema
ms.assetid: cafb57e4-c518-45e0-b565-2babd0dab1df
description: DailyRegeneration 元素描述以天为单位，任务会重新生成的频率。
ms.openlocfilehash: 356f7fd2672b2ad87d17e597c52e9f12273ce3c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753730"
---
# <a name="dailyregeneration"></a><span data-ttu-id="980a6-103">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="980a6-103">DailyRegeneration</span></span>

<span data-ttu-id="980a6-104">**DailyRegeneration**元素描述以天为单位，任务会重新生成的频率。</span><span class="sxs-lookup"><span data-stu-id="980a6-104">The **DailyRegeneration** element describes the frequency, in days, in which a task is regenerated.</span></span> 
  
```xml
<DailyRegeneration>
   <Interval/>
</DailyRegeneration>
```

<span data-ttu-id="980a6-105">**DailyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="980a6-105">**DailyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="980a6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="980a6-106">Attributes and elements</span></span>

<span data-ttu-id="980a6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="980a6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="980a6-108">属性</span><span class="sxs-lookup"><span data-stu-id="980a6-108">Attributes</span></span>

<span data-ttu-id="980a6-109">无。</span><span class="sxs-lookup"><span data-stu-id="980a6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="980a6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="980a6-110">Child elements</span></span>

|<span data-ttu-id="980a6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="980a6-111">**Element**</span></span>|<span data-ttu-id="980a6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="980a6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="980a6-113">Interval</span><span class="sxs-lookup"><span data-stu-id="980a6-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="980a6-114">以天为单位，两个连续的定期项目间中定义的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="980a6-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="980a6-115">值必须是介于 1 到 999 之间。</span><span class="sxs-lookup"><span data-stu-id="980a6-115">The value must be in the range of 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="980a6-116">父元素</span><span class="sxs-lookup"><span data-stu-id="980a6-116">Parent elements</span></span>

|<span data-ttu-id="980a6-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="980a6-117">**Element**</span></span>|<span data-ttu-id="980a6-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="980a6-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="980a6-119">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="980a6-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="980a6-120">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="980a6-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="980a6-121">备注</span><span class="sxs-lookup"><span data-stu-id="980a6-121">Remarks</span></span>

<span data-ttu-id="980a6-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="980a6-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="980a6-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="980a6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="980a6-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="980a6-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="980a6-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="980a6-125">Schema name</span></span>  <br/> |<span data-ttu-id="980a6-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="980a6-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="980a6-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="980a6-127">Validation file</span></span>  <br/> |<span data-ttu-id="980a6-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="980a6-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="980a6-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="980a6-129">Can be empty</span></span>  <br/> |<span data-ttu-id="980a6-130">False</span><span class="sxs-lookup"><span data-stu-id="980a6-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="980a6-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="980a6-131">See also</span></span>

- [<span data-ttu-id="980a6-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="980a6-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

