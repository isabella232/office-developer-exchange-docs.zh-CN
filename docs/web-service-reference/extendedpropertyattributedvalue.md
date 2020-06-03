---
title: ExtendedPropertyAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 90f3c5c5-f612-4e1b-b1f5-f92dd8524179
description: ExtendedPropertyAttributedValue 元素指定角色的扩展属性。
ms.openlocfilehash: 5c2ad5918d7ac666d5e26af6597b2c4c3dde6202
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460125"
---
# <a name="extendedpropertyattributedvalue"></a><span data-ttu-id="d9cb6-103">ExtendedPropertyAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d9cb6-103">ExtendedPropertyAttributedValue</span></span>

<span data-ttu-id="d9cb6-104">**ExtendedPropertyAttributedValue**元素指定角色的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="d9cb6-104">The **ExtendedPropertyAttributedValue** element specifies extended properties for a persona.</span></span> 
  
```XML
<ExtendedPropertyAttributedValue>
    <Value/>
    <Attributions/>
</ExtendedPropertyAttributedValue>
```

 <span data-ttu-id="d9cb6-105">**ExtendedPropertyAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="d9cb6-105">**ExtendedPropertyAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9cb6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d9cb6-106">Attributes and elements</span></span>

<span data-ttu-id="d9cb6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9cb6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9cb6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d9cb6-108">Attributes</span></span>

<span data-ttu-id="d9cb6-109">无。</span><span class="sxs-lookup"><span data-stu-id="d9cb6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9cb6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d9cb6-110">Child elements</span></span>

|<span data-ttu-id="d9cb6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9cb6-111">**Element**</span></span>|<span data-ttu-id="d9cb6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9cb6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9cb6-113">Value （ExtendedPropertyType）</span><span class="sxs-lookup"><span data-stu-id="d9cb6-113">Value (ExtendedPropertyType)</span></span>](value-extendedpropertytype.md) <br/> |<span data-ttu-id="d9cb6-114">指定角色的扩展属性的数组。</span><span class="sxs-lookup"><span data-stu-id="d9cb6-114">Specifies an array of extended properties for a persona.</span></span>  <br/> |
|[<span data-ttu-id="d9cb6-115">归属（ArrayOfValueAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="d9cb6-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="d9cb6-116">为其关联的**Value**元素指定归属的数组。</span><span class="sxs-lookup"><span data-stu-id="d9cb6-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9cb6-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d9cb6-117">Parent elements</span></span>

|<span data-ttu-id="d9cb6-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9cb6-118">**Element**</span></span>|<span data-ttu-id="d9cb6-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9cb6-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9cb6-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span><span class="sxs-lookup"><span data-stu-id="d9cb6-120">ExtendedProperties (ArrayOfExtendedPropertyAttributedValueType)</span></span>](extendedproperties-arrayofextendedpropertyattributedvaluetype.md) <br/> |<span data-ttu-id="d9cb6-121">包含用于统一联系人存储操作的扩展属性。</span><span class="sxs-lookup"><span data-stu-id="d9cb6-121">Contains the extended properties used for Unified Contact Store operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9cb6-122">备注</span><span class="sxs-lookup"><span data-stu-id="d9cb6-122">Remarks</span></span>

<span data-ttu-id="d9cb6-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d9cb6-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d9cb6-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d9cb6-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9cb6-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="d9cb6-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9cb6-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="d9cb6-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d9cb6-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="d9cb6-127">Schema Name</span></span>  <br/> |<span data-ttu-id="d9cb6-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="d9cb6-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="d9cb6-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="d9cb6-129">Validation File</span></span>  <br/> |<span data-ttu-id="d9cb6-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="d9cb6-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d9cb6-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="d9cb6-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d9cb6-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9cb6-132">See also</span></span>



- [<span data-ttu-id="d9cb6-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d9cb6-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

