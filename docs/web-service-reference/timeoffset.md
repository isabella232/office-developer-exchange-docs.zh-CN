---
title: TimeOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeOffset
api_type:
- schema
ms.assetid: b70bf498-cc3a-4fa6-8236-514acb973b33
description: TimeOffset元素代表的时间偏移时区转换为协调世界时 (UTC)。
ms.openlocfilehash: 46b1b2c8eec9bae871b4dafe43036e9d725075ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838213"
---
# <a name="timeoffset"></a><span data-ttu-id="24598-103">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="24598-103">TimeOffset</span></span>

<span data-ttu-id="24598-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **TimeOffset**元素代表的时间偏移时区转换为协调世界时 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="24598-104">The **TimeOffset** element represents the time offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span> 
  
```XML
<TimeOffset/>
```

 <span data-ttu-id="24598-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="24598-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="24598-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="24598-106">Attributes and elements</span></span>

<span data-ttu-id="24598-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="24598-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="24598-108">属性</span><span class="sxs-lookup"><span data-stu-id="24598-108">Attributes</span></span>

<span data-ttu-id="24598-109">无。</span><span class="sxs-lookup"><span data-stu-id="24598-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="24598-110">子元素</span><span class="sxs-lookup"><span data-stu-id="24598-110">Child elements</span></span>

<span data-ttu-id="24598-111">无。</span><span class="sxs-lookup"><span data-stu-id="24598-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="24598-112">父元素</span><span class="sxs-lookup"><span data-stu-id="24598-112">Parent elements</span></span>

|<span data-ttu-id="24598-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="24598-113">**Element**</span></span>|<span data-ttu-id="24598-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="24598-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="24598-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="24598-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="24598-116">表示每年的特定日期发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="24598-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="24598-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="24598-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="24598-118">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="24598-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="24598-119">文本值</span><span class="sxs-lookup"><span data-stu-id="24598-119">Text value</span></span>

<span data-ttu-id="24598-120">**TimeOffset**元素的文本值是指定从 UTC 时间偏移量的时区转换的持续时间。</span><span class="sxs-lookup"><span data-stu-id="24598-120">The text value of the **TimeOffset** element is a duration that specifies the time offset from UTC for the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="24598-121">备注</span><span class="sxs-lookup"><span data-stu-id="24598-121">Remarks</span></span>

<span data-ttu-id="24598-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="24598-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="24598-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="24598-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="24598-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="24598-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="24598-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="24598-125">Schema Name</span></span>  <br/> |<span data-ttu-id="24598-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="24598-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="24598-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="24598-127">Validation File</span></span>  <br/> |<span data-ttu-id="24598-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="24598-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="24598-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="24598-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="24598-130">False</span><span class="sxs-lookup"><span data-stu-id="24598-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24598-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="24598-131">See also</span></span>



- [<span data-ttu-id="24598-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="24598-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

