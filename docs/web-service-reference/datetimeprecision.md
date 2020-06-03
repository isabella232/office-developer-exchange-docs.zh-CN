---
title: DateTimePrecision
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 822dc5a6-2d57-474b-8a7d-da150898e5b6
description: DateTimePrecision 元素指定返回的日期/时间值的精度。
ms.openlocfilehash: 9d245dfb0123daae42ba9b9b4e98aff872b67d80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529222"
---
# <a name="datetimeprecision"></a><span data-ttu-id="f11e1-103">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="f11e1-103">DateTimePrecision</span></span>

<span data-ttu-id="f11e1-104">**DateTimePrecision**元素指定返回的日期/时间值的精度。</span><span class="sxs-lookup"><span data-stu-id="f11e1-104">The **DateTimePrecision** element specifies the precision for returned date/time values.</span></span> 
  
```XML
<DateTimePrecision />
```

<span data-ttu-id="f11e1-105">**DateTimePrecisionType**</span><span class="sxs-lookup"><span data-stu-id="f11e1-105">**DateTimePrecisionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f11e1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f11e1-106">Attributes and elements</span></span>

<span data-ttu-id="f11e1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f11e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f11e1-108">属性</span><span class="sxs-lookup"><span data-stu-id="f11e1-108">Attributes</span></span>

<span data-ttu-id="f11e1-109">无</span><span class="sxs-lookup"><span data-stu-id="f11e1-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f11e1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f11e1-110">Child elements</span></span>

<span data-ttu-id="f11e1-111">无。</span><span class="sxs-lookup"><span data-stu-id="f11e1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f11e1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f11e1-112">Parent elements</span></span>

<span data-ttu-id="f11e1-113">**DateTimePrecision**元素位于 SOAP 标头中。</span><span class="sxs-lookup"><span data-stu-id="f11e1-113">The **DateTimePrecision** element is located in the SOAP header.</span></span> 
  
## <a name="text-value"></a><span data-ttu-id="f11e1-114">文本值</span><span class="sxs-lookup"><span data-stu-id="f11e1-114">Text value</span></span>

<span data-ttu-id="f11e1-115">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="f11e1-115">A text value is required.</span></span> <span data-ttu-id="f11e1-116">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="f11e1-116">The following are the possible values:</span></span>
  
- <span data-ttu-id="f11e1-117">秒</span><span class="sxs-lookup"><span data-stu-id="f11e1-117">Seconds</span></span>
    
- <span data-ttu-id="f11e1-118">毫秒</span><span class="sxs-lookup"><span data-stu-id="f11e1-118">Milliseconds</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f11e1-119">备注</span><span class="sxs-lookup"><span data-stu-id="f11e1-119">Remarks</span></span>

<span data-ttu-id="f11e1-120">使用**DateTimePrecision**元素设置为 "秒" 的 SOAP 标头时，日期/时间值将返回到最接近的秒数（00:00:00）。</span><span class="sxs-lookup"><span data-stu-id="f11e1-120">When a SOAP header with the **DateTimePrecision** element set to "Seconds" is used, date/time values are returned to the nearest seconds (00:00:00).</span></span> <span data-ttu-id="f11e1-121">使用 "毫秒" 时，日期/时间值将返回到最接近的毫秒（00：00：00.0000）。</span><span class="sxs-lookup"><span data-stu-id="f11e1-121">When "Milliseconds" is used, date/time values are returned to the nearest millisecond (00:00:00.0000).</span></span> 
  
<span data-ttu-id="f11e1-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f11e1-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="f11e1-123">Exchange Server 2010 Service Pack 2 (SP2) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f11e1-123">This element was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f11e1-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="f11e1-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f11e1-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="f11e1-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f11e1-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="f11e1-126">Schema Name</span></span>  <br/> |<span data-ttu-id="f11e1-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="f11e1-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="f11e1-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="f11e1-128">Validation File</span></span>  <br/> |<span data-ttu-id="f11e1-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f11e1-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f11e1-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="f11e1-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="f11e1-131">False</span><span class="sxs-lookup"><span data-stu-id="f11e1-131">False</span></span>  <br/> |
   

