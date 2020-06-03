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
description: DailyRegeneration 元素描述任务重新生成的频率（以天为单位）。
ms.openlocfilehash: 518e4666031131f4a5fc80cc72c28a2110b468c5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462162"
---
# <a name="dailyregeneration"></a><span data-ttu-id="23523-103">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="23523-103">DailyRegeneration</span></span>

<span data-ttu-id="23523-104">**DailyRegeneration**元素描述任务重新生成的频率（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="23523-104">The **DailyRegeneration** element describes the frequency, in days, in which a task is regenerated.</span></span> 
  
```xml
<DailyRegeneration>
   <Interval/>
</DailyRegeneration>
```

<span data-ttu-id="23523-105">**DailyRegeneratingPatternType**</span><span class="sxs-lookup"><span data-stu-id="23523-105">**DailyRegeneratingPatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="23523-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="23523-106">Attributes and elements</span></span>

<span data-ttu-id="23523-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="23523-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23523-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="23523-108">Attributes</span></span>

<span data-ttu-id="23523-109">无。</span><span class="sxs-lookup"><span data-stu-id="23523-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23523-110">子元素</span><span class="sxs-lookup"><span data-stu-id="23523-110">Child elements</span></span>

|<span data-ttu-id="23523-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="23523-111">**Element**</span></span>|<span data-ttu-id="23523-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="23523-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23523-113">Interval</span><span class="sxs-lookup"><span data-stu-id="23523-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="23523-114">定义两个连续定期项目之间的间隔（以天为单位）。</span><span class="sxs-lookup"><span data-stu-id="23523-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="23523-115">该值必须介于1到999之间。</span><span class="sxs-lookup"><span data-stu-id="23523-115">The value must be in the range of 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23523-116">父元素</span><span class="sxs-lookup"><span data-stu-id="23523-116">Parent elements</span></span>

|<span data-ttu-id="23523-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="23523-117">**Element**</span></span>|<span data-ttu-id="23523-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="23523-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23523-119">重复周期（TaskRecurrenceType）</span><span class="sxs-lookup"><span data-stu-id="23523-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="23523-120">包含定期任务的定期信息。</span><span class="sxs-lookup"><span data-stu-id="23523-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23523-121">说明</span><span class="sxs-lookup"><span data-stu-id="23523-121">Remarks</span></span>

<span data-ttu-id="23523-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="23523-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23523-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="23523-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23523-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="23523-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23523-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="23523-125">Schema name</span></span>  <br/> |<span data-ttu-id="23523-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="23523-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="23523-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="23523-127">Validation file</span></span>  <br/> |<span data-ttu-id="23523-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="23523-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="23523-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="23523-129">Can be empty</span></span>  <br/> |<span data-ttu-id="23523-130">False</span><span class="sxs-lookup"><span data-stu-id="23523-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23523-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="23523-131">See also</span></span>

- [<span data-ttu-id="23523-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="23523-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

