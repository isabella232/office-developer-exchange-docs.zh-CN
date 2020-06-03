---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: IsHidden 元素包含一个布尔值，该值指示是否应将基础联系人隐藏或显示为角色的一部分。
ms.openlocfilehash: a22628e9ab4a46de04fe395f2d6c1b70083a5c77
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464236"
---
# <a name="ishidden"></a><span data-ttu-id="3d90e-103">IsHidden</span><span class="sxs-lookup"><span data-stu-id="3d90e-103">IsHidden</span></span>

<span data-ttu-id="3d90e-104">**IsHidden**元素包含一个布尔值，该值指示是否应将基础联系人隐藏或显示为角色的一部分。</span><span class="sxs-lookup"><span data-stu-id="3d90e-104">The **IsHidden** element contains a Boolean value that indicates whether the underlying contact should be hidden or displayed as part of the persona.</span></span> 
  
```XML
<IsHidden>true | false</IsHidden>
```

 <span data-ttu-id="3d90e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="3d90e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3d90e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3d90e-106">Attributes and elements</span></span>

<span data-ttu-id="3d90e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3d90e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3d90e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3d90e-108">Attributes</span></span>

<span data-ttu-id="3d90e-109">无。</span><span class="sxs-lookup"><span data-stu-id="3d90e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3d90e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3d90e-110">Child elements</span></span>

<span data-ttu-id="3d90e-111">无。</span><span class="sxs-lookup"><span data-stu-id="3d90e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3d90e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3d90e-112">Parent elements</span></span>

|<span data-ttu-id="3d90e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3d90e-113">**Element**</span></span>|<span data-ttu-id="3d90e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3d90e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3d90e-115">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="3d90e-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="3d90e-116">指定一个**Persona**元素的属性数组中的一个实例。</span><span class="sxs-lookup"><span data-stu-id="3d90e-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3d90e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="3d90e-117">Text value</span></span>

<span data-ttu-id="3d90e-118">如果**IsHidden**元素的文本值为**true** ，则表示基础联系人应隐藏或显示为角色的一部分。</span><span class="sxs-lookup"><span data-stu-id="3d90e-118">A text value of **true** for the **IsHidden** element indicates that the underlying contact should be hidden or displayed as part of the persona.</span></span> <span data-ttu-id="3d90e-119">**如果值为 false** ，则表示不应将基础联系人隐藏或显示为角色的一部分。</span><span class="sxs-lookup"><span data-stu-id="3d90e-119">A value of **false** indicates that the underlying contact should not be hidden or displayed as part of the persona.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3d90e-120">备注</span><span class="sxs-lookup"><span data-stu-id="3d90e-120">Remarks</span></span>

<span data-ttu-id="3d90e-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3d90e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3d90e-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3d90e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d90e-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="3d90e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d90e-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="3d90e-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3d90e-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="3d90e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="3d90e-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="3d90e-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="3d90e-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="3d90e-127">Validation File</span></span>  <br/> |<span data-ttu-id="3d90e-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="3d90e-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3d90e-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="3d90e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3d90e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3d90e-130">See also</span></span>



- [<span data-ttu-id="3d90e-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3d90e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

