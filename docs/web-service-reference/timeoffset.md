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
ms.openlocfilehash: 8cfd43477f0548227204da9ebc6d7e9307786845
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460286"
---
# <a name="timeoffset"></a><span data-ttu-id="9a145-103">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="9a145-103">TimeOffset</span></span>

<span data-ttu-id="9a145-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **TimeOffset**元素代表的时间偏移时区转换为协调世界时 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="9a145-104">The **TimeOffset** element represents the time offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span> 
  
```XML
<TimeOffset/>
```

 <span data-ttu-id="9a145-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="9a145-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9a145-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9a145-106">Attributes and elements</span></span>

<span data-ttu-id="9a145-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9a145-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a145-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9a145-108">Attributes</span></span>

<span data-ttu-id="9a145-109">无。</span><span class="sxs-lookup"><span data-stu-id="9a145-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9a145-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9a145-110">Child elements</span></span>

<span data-ttu-id="9a145-111">无。</span><span class="sxs-lookup"><span data-stu-id="9a145-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9a145-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9a145-112">Parent elements</span></span>

|<span data-ttu-id="9a145-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9a145-113">**Element**</span></span>|<span data-ttu-id="9a145-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9a145-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9a145-115">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="9a145-115">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="9a145-116">表示每年的特定日期发生的时区转换。</span><span class="sxs-lookup"><span data-stu-id="9a145-116">Represents a time zone transition that occurs on a specific date each year.</span></span>  <br/> |
|[<span data-ttu-id="9a145-117">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="9a145-117">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="9a145-118">表示时区转换发生在每年的同一天。</span><span class="sxs-lookup"><span data-stu-id="9a145-118">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9a145-119">文本值</span><span class="sxs-lookup"><span data-stu-id="9a145-119">Text value</span></span>

<span data-ttu-id="9a145-120">**TimeOffset**元素的文本值是指定从 UTC 时间偏移量的时区转换的持续时间。</span><span class="sxs-lookup"><span data-stu-id="9a145-120">The text value of the **TimeOffset** element is a duration that specifies the time offset from UTC for the time zone transition.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9a145-121">说明</span><span class="sxs-lookup"><span data-stu-id="9a145-121">Remarks</span></span>

<span data-ttu-id="9a145-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9a145-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9a145-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9a145-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a145-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9a145-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9a145-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9a145-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9a145-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="9a145-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="9a145-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9a145-127">Validation File</span></span>  <br/> |<span data-ttu-id="9a145-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9a145-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9a145-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9a145-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="9a145-130">False</span><span class="sxs-lookup"><span data-stu-id="9a145-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a145-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9a145-131">See also</span></span>



- [<span data-ttu-id="9a145-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9a145-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

