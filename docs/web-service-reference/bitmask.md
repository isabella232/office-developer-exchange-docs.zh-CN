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
ms.openlocfilehash: f05be466d05b13f8f362afb5fc0552653a532475
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458808"
---
# <a name="bitmask"></a><span data-ttu-id="95265-103">Bitmask</span><span class="sxs-lookup"><span data-stu-id="95265-103">Bitmask</span></span>

<span data-ttu-id="95265-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Bitmask** 元素表示要在 [不包括](excludes.md) 限制操作中使用的十六进制或十进制掩码。</span><span class="sxs-lookup"><span data-stu-id="95265-104">The **Bitmask** element represents a hexadecimal or decimal mask to be used during an [Excludes](excludes.md) restriction operation.</span></span> 
  
```xml
<Bitmask Value="" />
```

<span data-ttu-id="95265-105">**ExcludesValueType**</span><span class="sxs-lookup"><span data-stu-id="95265-105">**ExcludesValueType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="95265-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95265-106">Attributes and elements</span></span>

<span data-ttu-id="95265-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95265-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95265-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="95265-108">Attributes</span></span>

|<span data-ttu-id="95265-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="95265-109">**Attribute**</span></span>|<span data-ttu-id="95265-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="95265-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95265-111">**值**</span><span class="sxs-lookup"><span data-stu-id="95265-111">**Value**</span></span> | <span data-ttu-id="95265-112">表示十进制或十六进制位掩码。</span><span class="sxs-lookup"><span data-stu-id="95265-112">Represents a decimal or hexadecimal bitmask.</span></span> <span data-ttu-id="95265-113">由以下正则表达式表示值：</span><span class="sxs-lookup"><span data-stu-id="95265-113">The value is represented by the following regular expression:</span></span><br/><span data-ttu-id="95265-114">`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.</span><span class="sxs-lookup"><span data-stu-id="95265-114">`((0x|0X)[0-9A-Fa-f]*)|([0-9]*)`.</span></span><br/><br/><span data-ttu-id="95265-115">以下是此属性的十六进制值的示例：</span><span class="sxs-lookup"><span data-stu-id="95265-115">The following are examples of hexadecimal values for this attribute:</span></span><br/><span data-ttu-id="95265-116">- 0x12AF</span><span class="sxs-lookup"><span data-stu-id="95265-116">- 0x12AF</span></span><br/><span data-ttu-id="95265-117">- 0X334AE</span><span class="sxs-lookup"><span data-stu-id="95265-117">- 0X334AE</span></span><br/><br/><span data-ttu-id="95265-118">以下是此属性的十进制值的示例：</span><span class="sxs-lookup"><span data-stu-id="95265-118">The following are examples of decimal values for this attribute:</span></span><br/><span data-ttu-id="95265-119">- 10</span><span class="sxs-lookup"><span data-stu-id="95265-119">- 10</span></span><br/><span data-ttu-id="95265-120">- 255</span><span class="sxs-lookup"><span data-stu-id="95265-120">- 255</span></span><br/><span data-ttu-id="95265-121">- 4562</span><span class="sxs-lookup"><span data-stu-id="95265-121">- 4562</span></span> |
   
### <a name="child-elements"></a><span data-ttu-id="95265-122">子元素</span><span class="sxs-lookup"><span data-stu-id="95265-122">Child elements</span></span>

<span data-ttu-id="95265-123">无。</span><span class="sxs-lookup"><span data-stu-id="95265-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95265-124">父元素</span><span class="sxs-lookup"><span data-stu-id="95265-124">Parent elements</span></span>

|<span data-ttu-id="95265-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="95265-125">**Element**</span></span>|<span data-ttu-id="95265-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="95265-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95265-127">不包括</span><span class="sxs-lookup"><span data-stu-id="95265-127">Excludes</span></span>](excludes.md) <br/> |<span data-ttu-id="95265-128">执行这些属性的位掩码。</span><span class="sxs-lookup"><span data-stu-id="95265-128">Performs a bitwise mask of the properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95265-129">说明</span><span class="sxs-lookup"><span data-stu-id="95265-129">Remarks</span></span>

<span data-ttu-id="95265-p102">十六进制值必须有 0x 或 0X 的前缀。如果不存在此前缀，则假定该值为十进制数。</span><span class="sxs-lookup"><span data-stu-id="95265-p102">Hexadecimal values must have a prefix of either 0x or 0X. If this prefix does not exist, the value is assumed to be a decimal number.</span></span>
  
<span data-ttu-id="95265-132">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="95265-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95265-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="95265-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95265-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="95265-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95265-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="95265-135">Schema name</span></span>  <br/> |<span data-ttu-id="95265-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="95265-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="95265-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="95265-137">Validation file</span></span>  <br/> |<span data-ttu-id="95265-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="95265-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="95265-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="95265-139">Can be empty</span></span>  <br/> |<span data-ttu-id="95265-140">False</span><span class="sxs-lookup"><span data-stu-id="95265-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95265-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95265-141">See also</span></span>

- [<span data-ttu-id="95265-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="95265-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

