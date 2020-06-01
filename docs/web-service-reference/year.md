---
title: 年份
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Year
api_type:
- schema
ms.assetid: 93bf2847-53fa-496c-9a1e-dc9a9ffd0b9f
description: Year 元素用于定义根据年份变化的时区。 此元素为可选。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: cc83f9b2137f151f3f8ef0ceaf603ec036989961
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465168"
---
# <a name="year"></a><span data-ttu-id="41a35-105">年份</span><span class="sxs-lookup"><span data-stu-id="41a35-105">Year</span></span>

<span data-ttu-id="41a35-106">**Year**元素用于定义根据年份变化的时区。</span><span class="sxs-lookup"><span data-stu-id="41a35-106">The **Year** element is used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="41a35-107">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="41a35-107">This element is optional.</span></span> <span data-ttu-id="41a35-108">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="41a35-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Year/>
```

<span data-ttu-id="41a35-109">**string**</span><span class="sxs-lookup"><span data-stu-id="41a35-109">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="41a35-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="41a35-110">Attributes and elements</span></span>

<span data-ttu-id="41a35-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="41a35-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41a35-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="41a35-112">Attributes</span></span>

<span data-ttu-id="41a35-113">无。</span><span class="sxs-lookup"><span data-stu-id="41a35-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41a35-114">子元素</span><span class="sxs-lookup"><span data-stu-id="41a35-114">Child elements</span></span>

<span data-ttu-id="41a35-115">无。</span><span class="sxs-lookup"><span data-stu-id="41a35-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="41a35-116">父元素</span><span class="sxs-lookup"><span data-stu-id="41a35-116">Parent elements</span></span>

|<span data-ttu-id="41a35-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="41a35-117">**Element**</span></span>|<span data-ttu-id="41a35-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="41a35-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41a35-119">StandardTime</span><span class="sxs-lookup"><span data-stu-id="41a35-119">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="41a35-120">表示相对于[偏差（utc）](bias-utc.md)元素所表示的协调世界时（utc）的时间的偏移量。</span><span class="sxs-lookup"><span data-stu-id="41a35-120">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span>  <br/> |
|[<span data-ttu-id="41a35-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="41a35-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="41a35-122">表示相对于协调世界时（UTC）的时间的偏移量，由观察到夏时制的区域中的[偏置（utc）](bias-utc.md)元素表示。</span><span class="sxs-lookup"><span data-stu-id="41a35-122">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="41a35-123">文本值</span><span class="sxs-lookup"><span data-stu-id="41a35-123">Text value</span></span>

<span data-ttu-id="41a35-124">Year 元素接受表示一年的字符串。</span><span class="sxs-lookup"><span data-stu-id="41a35-124">The Year element accepts a string that represents a year.</span></span> <span data-ttu-id="41a35-125">年格式为 YYYY。</span><span class="sxs-lookup"><span data-stu-id="41a35-125">The year format is YYYY.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41a35-126">说明</span><span class="sxs-lookup"><span data-stu-id="41a35-126">Remarks</span></span>

<span data-ttu-id="41a35-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="41a35-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41a35-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="41a35-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41a35-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="41a35-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="41a35-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="41a35-130">Schema Name</span></span>  <br/> |<span data-ttu-id="41a35-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="41a35-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="41a35-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="41a35-132">Validation File</span></span>  <br/> |<span data-ttu-id="41a35-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="41a35-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="41a35-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="41a35-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="41a35-135">False</span><span class="sxs-lookup"><span data-stu-id="41a35-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41a35-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="41a35-136">See also</span></span>

- [<span data-ttu-id="41a35-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="41a35-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

