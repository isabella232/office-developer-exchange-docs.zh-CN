---
title: 值
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Value
api_type:
- schema
ms.assetid: 9a30cadd-909e-41b1-b4e9-291643dd89c6
description: Value 元素包含扩展属性的值。
ms.openlocfilehash: 5de1528dda6d58ea772d050e709c0720e389fae6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465210"
---
# <a name="value"></a><span data-ttu-id="4347d-103">值</span><span class="sxs-lookup"><span data-stu-id="4347d-103">Value</span></span>

<span data-ttu-id="4347d-104">**Value**元素包含扩展属性的值。</span><span class="sxs-lookup"><span data-stu-id="4347d-104">The **Value** element contains the value of an extended property.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="4347d-105">**String**</span><span class="sxs-lookup"><span data-stu-id="4347d-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4347d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4347d-106">Attributes and elements</span></span>

<span data-ttu-id="4347d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4347d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4347d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4347d-108">Attributes</span></span>

<span data-ttu-id="4347d-109">无。</span><span class="sxs-lookup"><span data-stu-id="4347d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4347d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4347d-110">Child elements</span></span>

<span data-ttu-id="4347d-111">无。</span><span class="sxs-lookup"><span data-stu-id="4347d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4347d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4347d-112">Parent elements</span></span>

|<span data-ttu-id="4347d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4347d-113">**Element**</span></span>|<span data-ttu-id="4347d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="4347d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4347d-115">值</span><span class="sxs-lookup"><span data-stu-id="4347d-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="4347d-116">包含扩展属性值的集合。</span><span class="sxs-lookup"><span data-stu-id="4347d-116">Contains a collection of values for an extended property.</span></span>  <br/> |
|[<span data-ttu-id="4347d-117">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="4347d-117">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="4347d-118">标识文件夹和项的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="4347d-118">Identifies extended properties on folders and items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4347d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="4347d-119">Text value</span></span>

<span data-ttu-id="4347d-120">该文本值必须与 ExtendedFieldURI 的 Recordtype 属性所指示的类型兼容。</span><span class="sxs-lookup"><span data-stu-id="4347d-120">The text value must be compatible with the type that is indicated by the PropertyType attribute of the ExtendedFieldURI.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4347d-121">备注</span><span class="sxs-lookup"><span data-stu-id="4347d-121">Remarks</span></span>

<span data-ttu-id="4347d-122">**Value**元素可以同时出现在单值和多值扩展属性实例中。</span><span class="sxs-lookup"><span data-stu-id="4347d-122">A **Value** element can occur in both single and multivalued extended property instances.</span></span> <span data-ttu-id="4347d-123">对于单值实例，它作为[ExtendedProperty](extendedproperty.md)元素的直接子级存在。</span><span class="sxs-lookup"><span data-stu-id="4347d-123">For single-valued instances, it exists as a direct child of the [ExtendedProperty](extendedproperty.md) element.</span></span> <span data-ttu-id="4347d-124">对于多值实例，它作为**Values**集合的直接子级存在。</span><span class="sxs-lookup"><span data-stu-id="4347d-124">For multivalued instance, it exists as a direct child of the **Values** collection.</span></span> 
  
<span data-ttu-id="4347d-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4347d-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4347d-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="4347d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4347d-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="4347d-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4347d-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="4347d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="4347d-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="4347d-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="4347d-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="4347d-130">Validation File</span></span>  <br/> |<span data-ttu-id="4347d-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4347d-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4347d-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="4347d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="4347d-133">False</span><span class="sxs-lookup"><span data-stu-id="4347d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4347d-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4347d-134">See also</span></span>

- [<span data-ttu-id="4347d-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4347d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

