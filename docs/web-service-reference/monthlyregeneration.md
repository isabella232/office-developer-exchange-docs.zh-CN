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
description: MonthlyRegeneration 元素描述了重新生成任务的频率（以月为单位）。
ms.openlocfilehash: c941bc2606790646d2797df27c854996901c0bc6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462736"
---
# <a name="monthlyregeneration"></a><span data-ttu-id="58664-103">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="58664-103">MonthlyRegeneration</span></span>

<span data-ttu-id="58664-104">**MonthlyRegeneration**元素描述了重新生成任务的频率（以月为单位）。</span><span class="sxs-lookup"><span data-stu-id="58664-104">The **MonthlyRegeneration** element describes the frequency, in months, of which task is regenerated.</span></span> 
  
```xml
<MonthlyRegeneration>
   <Interval/>
</MonthlyRegeneration>
```

 <span data-ttu-id="58664-105">**MonthlyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="58664-105">**MonthlyRegeneratingPatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58664-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="58664-106">Attributes and elements</span></span>

<span data-ttu-id="58664-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="58664-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58664-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="58664-108">Attributes</span></span>

<span data-ttu-id="58664-109">无。</span><span class="sxs-lookup"><span data-stu-id="58664-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="58664-110">子元素</span><span class="sxs-lookup"><span data-stu-id="58664-110">Child elements</span></span>

|<span data-ttu-id="58664-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="58664-111">**Element**</span></span>|<span data-ttu-id="58664-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="58664-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58664-113">Interval</span><span class="sxs-lookup"><span data-stu-id="58664-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="58664-114">定义两个连续定期项目之间的时间间隔（以月为单位）。</span><span class="sxs-lookup"><span data-stu-id="58664-114">Defines the interval, in months, between two consecutive recurring items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="58664-115">父元素</span><span class="sxs-lookup"><span data-stu-id="58664-115">Parent elements</span></span>

|<span data-ttu-id="58664-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="58664-116">**Element**</span></span>|<span data-ttu-id="58664-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="58664-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58664-118">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="58664-118">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="58664-119">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="58664-119">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58664-120">说明</span><span class="sxs-lookup"><span data-stu-id="58664-120">Remarks</span></span>

<span data-ttu-id="58664-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="58664-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58664-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="58664-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58664-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="58664-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58664-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="58664-124">Schema name</span></span>  <br/> |<span data-ttu-id="58664-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="58664-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="58664-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="58664-126">Validation file</span></span>  <br/> |<span data-ttu-id="58664-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="58664-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58664-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="58664-128">Can be empty</span></span>  <br/> |<span data-ttu-id="58664-129">False</span><span class="sxs-lookup"><span data-stu-id="58664-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58664-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="58664-130">See also</span></span>



- [<span data-ttu-id="58664-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="58664-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

