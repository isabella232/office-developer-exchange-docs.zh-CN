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
ms.openlocfilehash: d85fef0d67633733f6aa1943d70413ea70a528d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826642"
---
# <a name="offset"></a><span data-ttu-id="1b460-104">Offset</span><span class="sxs-lookup"><span data-stu-id="1b460-104">Offset</span></span>

<span data-ttu-id="1b460-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Offset** 元素描述与 [BaseOffset](baseoffset.md) 的时差。 **BaseOffset** 元素和 **Offset** 元素一起标识时间是标准时间还是夏令时。</span><span class="sxs-lookup"><span data-stu-id="1b460-p102">The **Offset** element describes the offset from the [BaseOffset](baseoffset.md). Together with the **BaseOffset** element, the **Offset** element identifies whether the time is standard or daylight saving time.</span></span> 
  
```xml
<Offset/>
```

 <span data-ttu-id="1b460-107">**duration**</span><span class="sxs-lookup"><span data-stu-id="1b460-107">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b460-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1b460-108">Attributes and elements</span></span>

<span data-ttu-id="1b460-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1b460-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b460-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="1b460-110">Attributes</span></span>

<span data-ttu-id="1b460-111">无。</span><span class="sxs-lookup"><span data-stu-id="1b460-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b460-112">子元素</span><span class="sxs-lookup"><span data-stu-id="1b460-112">Child elements</span></span>

<span data-ttu-id="1b460-113">无。</span><span class="sxs-lookup"><span data-stu-id="1b460-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1b460-114">父元素</span><span class="sxs-lookup"><span data-stu-id="1b460-114">Parent elements</span></span>

|<span data-ttu-id="1b460-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="1b460-115">**Element**</span></span>|<span data-ttu-id="1b460-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="1b460-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b460-117">夏时制</span><span class="sxs-lookup"><span data-stu-id="1b460-117">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="1b460-118">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="1b460-118">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="1b460-119">标准</span><span class="sxs-lookup"><span data-stu-id="1b460-119">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="1b460-120">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="1b460-120">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1b460-121">文本值</span><span class="sxs-lookup"><span data-stu-id="1b460-121">Text value</span></span>

<span data-ttu-id="1b460-122">文本值表示与协调世界时 (UTC) 的时差。</span><span class="sxs-lookup"><span data-stu-id="1b460-122">The text value represents the offset from Coordinated Universal Time (UTC).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b460-123">说明</span><span class="sxs-lookup"><span data-stu-id="1b460-123">Remarks</span></span>

<span data-ttu-id="1b460-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1b460-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b460-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="1b460-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b460-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="1b460-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1b460-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="1b460-127">Schema Name</span></span>  <br/> |<span data-ttu-id="1b460-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="1b460-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="1b460-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="1b460-129">Validation File</span></span>  <br/> |<span data-ttu-id="1b460-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1b460-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1b460-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="1b460-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="1b460-132">False</span><span class="sxs-lookup"><span data-stu-id="1b460-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b460-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1b460-133">See also</span></span>



- [<span data-ttu-id="1b460-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1b460-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

