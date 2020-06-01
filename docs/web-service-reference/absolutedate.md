---
title: AbsoluteDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteDate
api_type:
- schema
ms.assetid: 8bc59a26-6fe1-42e9-968c-69a94a3fb0ae
description: AbsoluteDate 元素表示时间从标准或夏时制更改的日期。
ms.openlocfilehash: 1874fea02c1eeeb41522046963e1d1b2fcea645a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461728"
---
# <a name="absolutedate"></a><span data-ttu-id="70e9c-103">AbsoluteDate</span><span class="sxs-lookup"><span data-stu-id="70e9c-103">AbsoluteDate</span></span>

<span data-ttu-id="70e9c-104">**AbsoluteDate**元素表示时间从标准或夏时制更改的日期。</span><span class="sxs-lookup"><span data-stu-id="70e9c-104">The **AbsoluteDate** element represents the date when the time changes from standard or daylight saving time.</span></span> 
  
```xml
<AbsoluteDate/>
```

<span data-ttu-id="70e9c-105">**date**</span><span class="sxs-lookup"><span data-stu-id="70e9c-105">**date**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="70e9c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="70e9c-106">Attributes and elements</span></span>

<span data-ttu-id="70e9c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="70e9c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70e9c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="70e9c-108">Attributes</span></span>

<span data-ttu-id="70e9c-109">无。</span><span class="sxs-lookup"><span data-stu-id="70e9c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70e9c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="70e9c-110">Child elements</span></span>

<span data-ttu-id="70e9c-111">无。</span><span class="sxs-lookup"><span data-stu-id="70e9c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="70e9c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="70e9c-112">Parent elements</span></span>

|<span data-ttu-id="70e9c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="70e9c-113">**Element**</span></span>|<span data-ttu-id="70e9c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="70e9c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70e9c-115">标准</span><span class="sxs-lookup"><span data-stu-id="70e9c-115">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="70e9c-116">表示当时间从夏令时更改为标准时间时的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="70e9c-116">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="70e9c-117">夏时制</span><span class="sxs-lookup"><span data-stu-id="70e9c-117">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="70e9c-118">表示时间从标准时间更改为夏时制的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="70e9c-118">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="70e9c-119">文本值</span><span class="sxs-lookup"><span data-stu-id="70e9c-119">Text value</span></span>

<span data-ttu-id="70e9c-120">文本值表示在标准或夏时制发生时的变化日期。</span><span class="sxs-lookup"><span data-stu-id="70e9c-120">The text value represents the date when the shift between standard or daylight saving time occurs.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70e9c-121">说明</span><span class="sxs-lookup"><span data-stu-id="70e9c-121">Remarks</span></span>

<span data-ttu-id="70e9c-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="70e9c-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70e9c-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="70e9c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70e9c-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="70e9c-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70e9c-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="70e9c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="70e9c-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="70e9c-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="70e9c-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="70e9c-127">Validation File</span></span>  <br/> |<span data-ttu-id="70e9c-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="70e9c-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="70e9c-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="70e9c-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="70e9c-130">False</span><span class="sxs-lookup"><span data-stu-id="70e9c-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70e9c-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70e9c-131">See also</span></span>

- [<span data-ttu-id="70e9c-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="70e9c-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)




