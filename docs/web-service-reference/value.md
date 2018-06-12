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
ms.openlocfilehash: 4b8674d267b78f0384f9457e794e88ace8234826
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838520"
---
# <a name="value"></a><span data-ttu-id="8fcae-103">值</span><span class="sxs-lookup"><span data-stu-id="8fcae-103">Value</span></span>

<span data-ttu-id="8fcae-104">**Value**元素包含扩展属性的值。</span><span class="sxs-lookup"><span data-stu-id="8fcae-104">The **Value** element contains the value of an extended property.</span></span> 
  
```xml
<Value/>
```

<span data-ttu-id="8fcae-105">**字符串**</span><span class="sxs-lookup"><span data-stu-id="8fcae-105">**String**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8fcae-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8fcae-106">Attributes and elements</span></span>

<span data-ttu-id="8fcae-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8fcae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8fcae-108">属性</span><span class="sxs-lookup"><span data-stu-id="8fcae-108">Attributes</span></span>

<span data-ttu-id="8fcae-109">无。</span><span class="sxs-lookup"><span data-stu-id="8fcae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8fcae-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8fcae-110">Child elements</span></span>

<span data-ttu-id="8fcae-111">无。</span><span class="sxs-lookup"><span data-stu-id="8fcae-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8fcae-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8fcae-112">Parent elements</span></span>

|<span data-ttu-id="8fcae-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8fcae-113">**Element**</span></span>|<span data-ttu-id="8fcae-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8fcae-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fcae-115">Values</span><span class="sxs-lookup"><span data-stu-id="8fcae-115">Values</span></span>](values.md) <br/> |<span data-ttu-id="8fcae-116">包含扩展属性的值的集合。</span><span class="sxs-lookup"><span data-stu-id="8fcae-116">Contains a collection of values for an extended property.</span></span>  <br/> |
|[<span data-ttu-id="8fcae-117">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="8fcae-117">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="8fcae-118">标识文件夹和项扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="8fcae-118">Identifies extended properties on folders and items.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8fcae-119">文本值</span><span class="sxs-lookup"><span data-stu-id="8fcae-119">Text value</span></span>

<span data-ttu-id="8fcae-120">文本值必须是兼容与由 ExtendedFieldURI 的 PropertyType 属性的类型。</span><span class="sxs-lookup"><span data-stu-id="8fcae-120">The text value must be compatible with the type that is indicated by the PropertyType attribute of the ExtendedFieldURI.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8fcae-121">备注</span><span class="sxs-lookup"><span data-stu-id="8fcae-121">Remarks</span></span>

<span data-ttu-id="8fcae-122">**Value**元素可以出现在两个扩展的单角色和多值属性实例。</span><span class="sxs-lookup"><span data-stu-id="8fcae-122">A **Value** element can occur in both single and multivalued extended property instances.</span></span> <span data-ttu-id="8fcae-123">对于单值实例，但仍然[ExtendedProperty](extendedproperty.md)元素的直接子级。</span><span class="sxs-lookup"><span data-stu-id="8fcae-123">For single-valued instances, it exists as a direct child of the [ExtendedProperty](extendedproperty.md) element.</span></span> <span data-ttu-id="8fcae-124">对于多值实例，但仍然的直接子级的**Values**集合。</span><span class="sxs-lookup"><span data-stu-id="8fcae-124">For multivalued instance, it exists as a direct child of the **Values** collection.</span></span> 
  
<span data-ttu-id="8fcae-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8fcae-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8fcae-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="8fcae-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8fcae-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="8fcae-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8fcae-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="8fcae-128">Schema Name</span></span>  <br/> |<span data-ttu-id="8fcae-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="8fcae-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="8fcae-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="8fcae-130">Validation File</span></span>  <br/> |<span data-ttu-id="8fcae-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8fcae-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8fcae-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="8fcae-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="8fcae-133">False</span><span class="sxs-lookup"><span data-stu-id="8fcae-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fcae-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8fcae-134">See also</span></span>

- [<span data-ttu-id="8fcae-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8fcae-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

