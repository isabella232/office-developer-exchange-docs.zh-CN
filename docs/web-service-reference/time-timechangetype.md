---
title: Time （TimeChangeType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: be12e41e-6871-4f6b-b2d4-3dfa404f9ea1
description: Time 元素描述在标准时间和夏时制时间之间的时间更改时间。
ms.openlocfilehash: c25d0bc3394fdfab42a29eab8b370bc4263618ed
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465735"
---
# <a name="time-timechangetype"></a><span data-ttu-id="5c1b7-103">Time （TimeChangeType）</span><span class="sxs-lookup"><span data-stu-id="5c1b7-103">Time (TimeChangeType)</span></span>

<span data-ttu-id="5c1b7-104">**Time**元素描述在标准时间和夏时制时间之间的时间更改时间。</span><span class="sxs-lookup"><span data-stu-id="5c1b7-104">The **Time** element describes the time when the time changes between standard time and daylight saving time.</span></span> 
  
```xml
<Time/>
```

 <span data-ttu-id="5c1b7-105">**Time**</span><span class="sxs-lookup"><span data-stu-id="5c1b7-105">**Time**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c1b7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5c1b7-106">Attributes and elements</span></span>

<span data-ttu-id="5c1b7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5c1b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c1b7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5c1b7-108">Attributes</span></span>

<span data-ttu-id="5c1b7-109">无。</span><span class="sxs-lookup"><span data-stu-id="5c1b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c1b7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5c1b7-110">Child elements</span></span>

<span data-ttu-id="5c1b7-111">无。</span><span class="sxs-lookup"><span data-stu-id="5c1b7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c1b7-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5c1b7-112">Parent elements</span></span>

|<span data-ttu-id="5c1b7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5c1b7-113">**Element**</span></span>|<span data-ttu-id="5c1b7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c1b7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c1b7-115">夏时制</span><span class="sxs-lookup"><span data-stu-id="5c1b7-115">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="5c1b7-116">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="5c1b7-116">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="5c1b7-117">标准</span><span class="sxs-lookup"><span data-stu-id="5c1b7-117">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="5c1b7-118">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="5c1b7-118">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c1b7-119">文本值</span><span class="sxs-lookup"><span data-stu-id="5c1b7-119">Text value</span></span>

<span data-ttu-id="5c1b7-120">Text 值表示在标准时间和夏时制时间之间的时间更改时间。</span><span class="sxs-lookup"><span data-stu-id="5c1b7-120">The text value represents the time when the time changes between standard time and daylight saving time.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c1b7-121">说明</span><span class="sxs-lookup"><span data-stu-id="5c1b7-121">Remarks</span></span>

<span data-ttu-id="5c1b7-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5c1b7-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c1b7-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="5c1b7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c1b7-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="5c1b7-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c1b7-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="5c1b7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5c1b7-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="5c1b7-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c1b7-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="5c1b7-127">Validation File</span></span>  <br/> |<span data-ttu-id="5c1b7-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5c1b7-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c1b7-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="5c1b7-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c1b7-130">False</span><span class="sxs-lookup"><span data-stu-id="5c1b7-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c1b7-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c1b7-131">See also</span></span>



- [<span data-ttu-id="5c1b7-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5c1b7-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

