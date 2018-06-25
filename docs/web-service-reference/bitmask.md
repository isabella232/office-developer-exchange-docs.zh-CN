---
title: Bitmask
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bitmask
api_type:
- schema
ms.assetid: fc7eeac2-555f-4cbc-8b48-26d9ed67748a
description: Bitmask 元素表示要在 不包括 限制操作中使用的十六进制或十进制掩码。
ms.openlocfilehash: 86c8c61f22d8d620a9139280b2a43ed7fec4727d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753343"
---
# <a name="bitmask"></a><span data-ttu-id="dc04f-103">Bitmask</span><span class="sxs-lookup"><span data-stu-id="dc04f-103">Bitmask</span></span>

<span data-ttu-id="dc04f-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Bitmask** 元素表示要在 [不包括](excludes.md) 限制操作中使用的十六进制或十进制掩码。</span><span class="sxs-lookup"><span data-stu-id="dc04f-104">The **Bitmask** element represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> 
  
```xml
<Bitmask Value="" />
```

<span data-ttu-id="dc04f-105">**ExcludesValueType**</span><span class="sxs-lookup"><span data-stu-id="dc04f-105">**ExcludesValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="dc04f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc04f-106">Attributes and elements</span></span>

<span data-ttu-id="dc04f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc04f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc04f-108">属性</span><span class="sxs-lookup"><span data-stu-id="dc04f-108">Attributes</span></span>

|<span data-ttu-id="dc04f-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="dc04f-109">**Attribute**</span></span>|<span data-ttu-id="dc04f-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc04f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc04f-111">**Value**</span><span class="sxs-lookup"><span data-stu-id="dc04f-111">**Value**</span></span> | <span data-ttu-id="dc04f-112">表示十进制或十六进制位掩码。</span><span class="sxs-lookup"><span data-stu-id="dc04f-112">Represents a decimal or hexadecimal bitmask.</span></span> <span data-ttu-id="dc04f-113">下面的正则表达式被表示的值：</span><span class="sxs-lookup"><span data-stu-id="dc04f-113">The value is represented by the following regular expression:</span></span><br/><span data-ttu-id="dc04f-114">((0x</span><span class="sxs-lookup"><span data-stu-id="dc04f-114">\`((0x</span></span>|<span data-ttu-id="dc04f-115">0X)[0-9A-Fa-f]\*)</span><span class="sxs-lookup"><span data-stu-id="dc04f-115">0X)[0-9A-Fa-f]\*)</span></span>|<span data-ttu-id="dc04f-116">([0-9] \*)。</span><span class="sxs-lookup"><span data-stu-id="dc04f-116">([0-9]\*)\`.</span></span><br/><br/><span data-ttu-id="dc04f-117">下面是此属性的十六进制值的示例：</span><span class="sxs-lookup"><span data-stu-id="dc04f-117">The following are examples of hexadecimal values for this attribute:</span></span><br/><span data-ttu-id="dc04f-118">-0x12AF</span><span class="sxs-lookup"><span data-stu-id="dc04f-118">- 0x12AF</span></span><br/><span data-ttu-id="dc04f-119">-0X334AE</span><span class="sxs-lookup"><span data-stu-id="dc04f-119">- 0X334AE</span></span><br/><br/><span data-ttu-id="dc04f-120">下面是此属性的十进制值的示例：</span><span class="sxs-lookup"><span data-stu-id="dc04f-120">The following are examples of decimal values for this attribute:</span></span><br/><span data-ttu-id="dc04f-121">-10</span><span class="sxs-lookup"><span data-stu-id="dc04f-121">- 10</span></span><br/><span data-ttu-id="dc04f-122">-255</span><span class="sxs-lookup"><span data-stu-id="dc04f-122">- 255</span></span><br/><span data-ttu-id="dc04f-123">-4562</span><span class="sxs-lookup"><span data-stu-id="dc04f-123">- 4562</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="dc04f-124">子元素</span><span class="sxs-lookup"><span data-stu-id="dc04f-124">Child elements</span></span>

<span data-ttu-id="dc04f-125">无。</span><span class="sxs-lookup"><span data-stu-id="dc04f-125">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc04f-126">父元素</span><span class="sxs-lookup"><span data-stu-id="dc04f-126">Parent elements</span></span>

|<span data-ttu-id="dc04f-127">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc04f-127">**Element**</span></span>|<span data-ttu-id="dc04f-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc04f-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc04f-129">不包括</span><span class="sxs-lookup"><span data-stu-id="dc04f-129">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="dc04f-130">执行这些属性的位掩码。</span><span class="sxs-lookup"><span data-stu-id="dc04f-130">Performs a bitwise mask of the properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc04f-131">备注</span><span class="sxs-lookup"><span data-stu-id="dc04f-131">Remarks</span></span>

<span data-ttu-id="dc04f-p102">十六进制值必须有 0x 或 0X 的前缀。如果不存在此前缀，则假定该值为十进制数。</span><span class="sxs-lookup"><span data-stu-id="dc04f-p102">Hexadecimal values must have a prefix of either 0x or 0X. If this prefix does not exist, the value is assumed to be a decimal number.</span></span>
  
<span data-ttu-id="dc04f-134">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc04f-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc04f-135">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc04f-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc04f-136">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc04f-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dc04f-137">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc04f-137">Schema name</span></span>  <br/> |<span data-ttu-id="dc04f-138">类型架构</span><span class="sxs-lookup"><span data-stu-id="dc04f-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="dc04f-139">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc04f-139">Validation file</span></span>  <br/> |<span data-ttu-id="dc04f-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dc04f-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dc04f-141">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc04f-141">Can be empty</span></span>  <br/> |<span data-ttu-id="dc04f-142">False</span><span class="sxs-lookup"><span data-stu-id="dc04f-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dc04f-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc04f-143">See also</span></span>

- [<span data-ttu-id="dc04f-144">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dc04f-144">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

