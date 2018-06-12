---
title: ExtendedPropertyAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90f3c5c5-f612-4e1b-b1f5-f92dd8524179
description: ExtendedPropertyAttributedValue 元素指定角色扩展的的属性。
ms.openlocfilehash: 92e4ec7f192ccb36ea68d7862e66cb7b3349819a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754237"
---
# <a name="extendedpropertyattributedvalue"></a><span data-ttu-id="511ba-103">ExtendedPropertyAttributedValue</span><span class="sxs-lookup"><span data-stu-id="511ba-103">ExtendedPropertyAttributedValue</span></span>

<span data-ttu-id="511ba-104">**ExtendedPropertyAttributedValue**元素指定角色扩展的的属性。</span><span class="sxs-lookup"><span data-stu-id="511ba-104">The **ExtendedPropertyAttributedValue** element specifies extended properties for a persona.</span></span> 
  
```XML
<ExtendedPropertyAttributedValue>
    <Value/>
    <Attributions/>
</ExtendedPropertyAttributedValue>
```

 <span data-ttu-id="511ba-105">**ExtendedPropertyAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="511ba-105">**ExtendedPropertyAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="511ba-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="511ba-106">Attributes and elements</span></span>

<span data-ttu-id="511ba-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="511ba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="511ba-108">属性</span><span class="sxs-lookup"><span data-stu-id="511ba-108">Attributes</span></span>

<span data-ttu-id="511ba-109">无。</span><span class="sxs-lookup"><span data-stu-id="511ba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="511ba-110">子元素</span><span class="sxs-lookup"><span data-stu-id="511ba-110">Child elements</span></span>

|<span data-ttu-id="511ba-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="511ba-111">**Element**</span></span>|<span data-ttu-id="511ba-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="511ba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="511ba-113">值 (ExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="511ba-113">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md) <br/> |<span data-ttu-id="511ba-114">指定的角色扩展属性的数组。</span><span class="sxs-lookup"><span data-stu-id="511ba-114">Specifies an array of extended properties for a persona.</span></span>  <br/> |
|[<span data-ttu-id="511ba-115">归属 (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="511ba-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="511ba-116">指定其关联的**值**元素的归属的数组。</span><span class="sxs-lookup"><span data-stu-id="511ba-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="511ba-117">父元素</span><span class="sxs-lookup"><span data-stu-id="511ba-117">Parent elements</span></span>

|<span data-ttu-id="511ba-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="511ba-118">**Element**</span></span>|<span data-ttu-id="511ba-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="511ba-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="511ba-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span><span class="sxs-lookup"><span data-stu-id="511ba-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span></span>](extendedproperties-arrayofextendedpropertyattributedvaluetype.md) <br/> |<span data-ttu-id="511ba-121">包含用于统一联系人存储库的操作的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="511ba-121">Contains the extended properties used for Unified Contact Store operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="511ba-122">备注</span><span class="sxs-lookup"><span data-stu-id="511ba-122">Remarks</span></span>

<span data-ttu-id="511ba-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="511ba-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="511ba-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="511ba-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="511ba-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="511ba-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="511ba-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="511ba-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="511ba-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="511ba-127">Schema Name</span></span>  <br/> |<span data-ttu-id="511ba-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="511ba-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="511ba-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="511ba-129">Validation File</span></span>  <br/> |<span data-ttu-id="511ba-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="511ba-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="511ba-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="511ba-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="511ba-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="511ba-132">See also</span></span>



- [<span data-ttu-id="511ba-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="511ba-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

