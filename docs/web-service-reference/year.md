---
title: 年
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
description: Year 元素用于定义更改这取决于一年的时区。 此元素是可选的。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 95d75f9c6166fc26e86534346fb07292a7fb3dcd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838589"
---
# <a name="year"></a><span data-ttu-id="0419c-105">年</span><span class="sxs-lookup"><span data-stu-id="0419c-105">Year</span></span>

<span data-ttu-id="0419c-106">**Year**元素用于定义更改这取决于一年的时区。</span><span class="sxs-lookup"><span data-stu-id="0419c-106">The **Year** element is used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="0419c-107">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="0419c-107">This element is optional.</span></span> <span data-ttu-id="0419c-108">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0419c-108">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Year/>
```

<span data-ttu-id="0419c-109">**string**</span><span class="sxs-lookup"><span data-stu-id="0419c-109">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0419c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0419c-110">Attributes and elements</span></span>

<span data-ttu-id="0419c-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0419c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0419c-112">属性</span><span class="sxs-lookup"><span data-stu-id="0419c-112">Attributes</span></span>

<span data-ttu-id="0419c-113">无。</span><span class="sxs-lookup"><span data-stu-id="0419c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0419c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="0419c-114">Child elements</span></span>

<span data-ttu-id="0419c-115">无。</span><span class="sxs-lookup"><span data-stu-id="0419c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0419c-116">父元素</span><span class="sxs-lookup"><span data-stu-id="0419c-116">Parent elements</span></span>

|<span data-ttu-id="0419c-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="0419c-117">**Element**</span></span>|<span data-ttu-id="0419c-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="0419c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0419c-119">StandardTime</span><span class="sxs-lookup"><span data-stu-id="0419c-119">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="0419c-120">表示的时间相对于协调世界时 (UTC) 表示[斜线 (UTC)](bias-utc.md)元素的偏移量。</span><span class="sxs-lookup"><span data-stu-id="0419c-120">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span>  <br/> |
|[<span data-ttu-id="0419c-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="0419c-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="0419c-122">表示从时间相对于协调世界时 (UTC) 表示的夏时制观察到的位置的区域中的[斜线 (UTC)](bias-utc.md)元素的偏移量。</span><span class="sxs-lookup"><span data-stu-id="0419c-122">Represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0419c-123">文本值</span><span class="sxs-lookup"><span data-stu-id="0419c-123">Text value</span></span>

<span data-ttu-id="0419c-124">Year 元素接受一个字符串，表示一年。</span><span class="sxs-lookup"><span data-stu-id="0419c-124">The Year element accepts a string that represents a year.</span></span> <span data-ttu-id="0419c-125">YYYY 年份格式。</span><span class="sxs-lookup"><span data-stu-id="0419c-125">The year format is YYYY.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0419c-126">备注</span><span class="sxs-lookup"><span data-stu-id="0419c-126">Remarks</span></span>

<span data-ttu-id="0419c-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0419c-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0419c-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="0419c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0419c-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="0419c-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0419c-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="0419c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="0419c-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="0419c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="0419c-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="0419c-132">Validation File</span></span>  <br/> |<span data-ttu-id="0419c-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0419c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0419c-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="0419c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="0419c-135">False</span><span class="sxs-lookup"><span data-stu-id="0419c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0419c-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0419c-136">See also</span></span>

- [<span data-ttu-id="0419c-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0419c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

