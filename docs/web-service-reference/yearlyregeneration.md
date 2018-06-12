---
title: YearlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- YearlyRegeneration
api_type:
- schema
ms.assetid: 23538bca-738e-4319-944e-f459ff8a7eba
description: YearlyRegeneration 元素介绍的年、 一个任务会重新生成的频率。
ms.openlocfilehash: d034be1ff70e92fd5e96118b9fd1eb3033737f6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838585"
---
# <a name="yearlyregeneration"></a><span data-ttu-id="4dbd0-103">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="4dbd0-103">YearlyRegeneration</span></span>

<span data-ttu-id="4dbd0-104">**YearlyRegeneration**元素介绍的年、 一个任务会重新生成的频率。</span><span class="sxs-lookup"><span data-stu-id="4dbd0-104">The **YearlyRegeneration** element describes the frequency, in years, in which a task is regenerated.</span></span> 
  
```xml
<YearlyRegeneratingPatternType>
   <Interval/>
</YearlyRegeneratingPatternType>
```

<span data-ttu-id="4dbd0-105">**YearlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="4dbd0-105">**YearlyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4dbd0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4dbd0-106">Attributes and elements</span></span>

<span data-ttu-id="4dbd0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4dbd0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4dbd0-108">属性</span><span class="sxs-lookup"><span data-stu-id="4dbd0-108">Attributes</span></span>

<span data-ttu-id="4dbd0-109">无。</span><span class="sxs-lookup"><span data-stu-id="4dbd0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4dbd0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4dbd0-110">Child elements</span></span>

|<span data-ttu-id="4dbd0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4dbd0-111">**Element**</span></span>|<span data-ttu-id="4dbd0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4dbd0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4dbd0-113">Interval</span><span class="sxs-lookup"><span data-stu-id="4dbd0-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="4dbd0-114">在年中，在此期间任务完成后重新新任务中定义的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="4dbd0-114">Defines the interval, in years, during which a new task is regenerated after the completion of the task.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4dbd0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4dbd0-115">Parent elements</span></span>

|<span data-ttu-id="4dbd0-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4dbd0-116">**Element**</span></span>|<span data-ttu-id="4dbd0-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4dbd0-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4dbd0-118">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="4dbd0-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="4dbd0-119">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="4dbd0-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4dbd0-120">备注</span><span class="sxs-lookup"><span data-stu-id="4dbd0-120">Remarks</span></span>

<span data-ttu-id="4dbd0-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4dbd0-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4dbd0-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="4dbd0-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4dbd0-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="4dbd0-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4dbd0-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="4dbd0-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4dbd0-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="4dbd0-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="4dbd0-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="4dbd0-126">Validation File</span></span>  <br/> |<span data-ttu-id="4dbd0-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4dbd0-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4dbd0-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="4dbd0-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="4dbd0-129">False</span><span class="sxs-lookup"><span data-stu-id="4dbd0-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4dbd0-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4dbd0-130">See also</span></span>

- [<span data-ttu-id="4dbd0-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4dbd0-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

