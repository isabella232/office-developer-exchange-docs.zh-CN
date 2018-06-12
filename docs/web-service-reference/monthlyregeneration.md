---
title: MonthlyRegeneration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MonthlyRegeneration
api_type:
- schema
ms.assetid: 9a52ca97-a663-41fe-b61a-61d8c53833ca
description: MonthlyRegeneration 元素描述以月为单位的任务重新生成的频率。
ms.openlocfilehash: 3de8ab5a6a2134ad5c596bf2bcb073d881c89746
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826488"
---
# <a name="monthlyregeneration"></a><span data-ttu-id="6ce1e-103">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="6ce1e-103">MonthlyRegeneration</span></span>

<span data-ttu-id="6ce1e-104">**MonthlyRegeneration**元素描述以月为单位的任务重新生成的频率。</span><span class="sxs-lookup"><span data-stu-id="6ce1e-104">The **MonthlyRegeneration** element describes the frequency, in months, of which task is regenerated.</span></span> 
  
```xml
<MonthlyRegeneration>
   <Interval/>
</MonthlyRegeneration>
```

 <span data-ttu-id="6ce1e-105">**MonthlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="6ce1e-105">**MonthlyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ce1e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6ce1e-106">Attributes and elements</span></span>

<span data-ttu-id="6ce1e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6ce1e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ce1e-108">属性</span><span class="sxs-lookup"><span data-stu-id="6ce1e-108">Attributes</span></span>

<span data-ttu-id="6ce1e-109">无。</span><span class="sxs-lookup"><span data-stu-id="6ce1e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ce1e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6ce1e-110">Child elements</span></span>

|<span data-ttu-id="6ce1e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6ce1e-111">**Element**</span></span>|<span data-ttu-id="6ce1e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6ce1e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ce1e-113">Interval</span><span class="sxs-lookup"><span data-stu-id="6ce1e-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="6ce1e-114">在两个连续的定期项目的间隔月份数中定义的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="6ce1e-114">Defines the interval, in months, between two consecutive recurring items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6ce1e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6ce1e-115">Parent elements</span></span>

|<span data-ttu-id="6ce1e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6ce1e-116">**Element**</span></span>|<span data-ttu-id="6ce1e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6ce1e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ce1e-118">定期 (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="6ce1e-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="6ce1e-119">包含定期周期性任务信息。</span><span class="sxs-lookup"><span data-stu-id="6ce1e-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ce1e-120">备注</span><span class="sxs-lookup"><span data-stu-id="6ce1e-120">Remarks</span></span>

<span data-ttu-id="6ce1e-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6ce1e-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ce1e-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="6ce1e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ce1e-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="6ce1e-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6ce1e-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="6ce1e-124">Schema name</span></span>  <br/> |<span data-ttu-id="6ce1e-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="6ce1e-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="6ce1e-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="6ce1e-126">Validation file</span></span>  <br/> |<span data-ttu-id="6ce1e-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6ce1e-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6ce1e-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="6ce1e-128">Can be empty</span></span>  <br/> |<span data-ttu-id="6ce1e-129">False</span><span class="sxs-lookup"><span data-stu-id="6ce1e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ce1e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6ce1e-130">See also</span></span>



- [<span data-ttu-id="6ce1e-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6ce1e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
