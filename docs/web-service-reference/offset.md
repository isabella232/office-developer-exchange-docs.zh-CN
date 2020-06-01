---
title: Offset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Offset
api_type:
- schema
ms.assetid: dcbb9d85-d90c-4363-b4c9-d081ad03f407
description: Offset 元素描述与 BaseOffset 的时差。BaseOffset 元素和 Offset 元素一起标识时间是标准时间还是夏令时。
ms.openlocfilehash: 74ad87026c2cb89f3b0c35218c91f81380029963
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459754"
---
# <a name="offset"></a><span data-ttu-id="e3bb6-104">Offset</span><span class="sxs-lookup"><span data-stu-id="e3bb6-104">Offset</span></span>

<span data-ttu-id="e3bb6-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Offset** 元素描述与 [BaseOffset](baseoffset.md) 的时差。 **BaseOffset** 元素和 **Offset** 元素一起标识时间是标准时间还是夏令时。</span><span class="sxs-lookup"><span data-stu-id="e3bb6-p102">The **Offset** element describes the offset from the [BaseOffset](baseoffset.md). Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard or daylight saving time.</span></span> 
  
```xml
<Offset/>
```

 <span data-ttu-id="e3bb6-107">**duration**</span><span class="sxs-lookup"><span data-stu-id="e3bb6-107">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3bb6-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3bb6-108">Attributes and elements</span></span>

<span data-ttu-id="e3bb6-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3bb6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3bb6-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="e3bb6-110">Attributes</span></span>

<span data-ttu-id="e3bb6-111">无。</span><span class="sxs-lookup"><span data-stu-id="e3bb6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3bb6-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e3bb6-112">Child elements</span></span>

<span data-ttu-id="e3bb6-113">无。</span><span class="sxs-lookup"><span data-stu-id="e3bb6-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e3bb6-114">父元素</span><span class="sxs-lookup"><span data-stu-id="e3bb6-114">Parent elements</span></span>

|<span data-ttu-id="e3bb6-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3bb6-115">**Element**</span></span>|<span data-ttu-id="e3bb6-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3bb6-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3bb6-117">夏时制</span><span class="sxs-lookup"><span data-stu-id="e3bb6-117">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="e3bb6-118">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e3bb6-118">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="e3bb6-119">标准</span><span class="sxs-lookup"><span data-stu-id="e3bb6-119">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="e3bb6-120">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e3bb6-120">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e3bb6-121">文本值</span><span class="sxs-lookup"><span data-stu-id="e3bb6-121">Text value</span></span>

<span data-ttu-id="e3bb6-122">文本值表示与协调世界时 (UTC) 的时差。</span><span class="sxs-lookup"><span data-stu-id="e3bb6-122">The text value represents the offset from Coordinated Universal Time (UTC).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3bb6-123">说明</span><span class="sxs-lookup"><span data-stu-id="e3bb6-123">Remarks</span></span>

<span data-ttu-id="e3bb6-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e3bb6-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3bb6-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3bb6-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3bb6-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3bb6-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e3bb6-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3bb6-127">Schema Name</span></span>  <br/> |<span data-ttu-id="e3bb6-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="e3bb6-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="e3bb6-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3bb6-129">Validation File</span></span>  <br/> |<span data-ttu-id="e3bb6-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e3bb6-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e3bb6-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3bb6-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3bb6-132">False</span><span class="sxs-lookup"><span data-stu-id="e3bb6-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3bb6-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3bb6-133">See also</span></span>



- [<span data-ttu-id="e3bb6-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e3bb6-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

