---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: IsHidden 元素包含一个布尔值，指示是否应隐藏或显示该角色的一部分基础的联系人。
ms.openlocfilehash: ee20bf0af287e3cddaedb5bc6d3c63ef9a7a7006
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826032"
---
# <a name="ishidden"></a><span data-ttu-id="95232-103">IsHidden</span><span class="sxs-lookup"><span data-stu-id="95232-103">IsHidden</span></span>

<span data-ttu-id="95232-104">**IsHidden**元素包含一个布尔值，指示是否应隐藏或显示该角色的一部分基础的联系人。</span><span class="sxs-lookup"><span data-stu-id="95232-104">The **IsHidden** element contains a Boolean value that indicates whether the underlying contact should be hidden or displayed as part of the persona.</span></span> 
  
```XML
<IsHidden>true | false</IsHidden>
```

 <span data-ttu-id="95232-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="95232-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95232-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95232-106">Attributes and elements</span></span>

<span data-ttu-id="95232-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95232-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95232-108">属性</span><span class="sxs-lookup"><span data-stu-id="95232-108">Attributes</span></span>

<span data-ttu-id="95232-109">无。</span><span class="sxs-lookup"><span data-stu-id="95232-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95232-110">子元素</span><span class="sxs-lookup"><span data-stu-id="95232-110">Child elements</span></span>

<span data-ttu-id="95232-111">无。</span><span class="sxs-lookup"><span data-stu-id="95232-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="95232-112">父元素</span><span class="sxs-lookup"><span data-stu-id="95232-112">Parent elements</span></span>

|<span data-ttu-id="95232-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="95232-113">**Element**</span></span>|<span data-ttu-id="95232-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="95232-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95232-115">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="95232-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="95232-116">**个人**元素的属性数组中指定的实例。</span><span class="sxs-lookup"><span data-stu-id="95232-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="95232-117">文本值</span><span class="sxs-lookup"><span data-stu-id="95232-117">Text value</span></span>

<span data-ttu-id="95232-118">文本值为**true**的**IsHidden**元素指示应隐藏或显示该角色的一部分基础的联系人。</span><span class="sxs-lookup"><span data-stu-id="95232-118">A text value of **true** for the **IsHidden** element indicates that the underlying contact should be hidden or displayed as part of the persona.</span></span> <span data-ttu-id="95232-119">如果值为**false**指示的基础的联系人不应隐藏或显示该角色的一部分。</span><span class="sxs-lookup"><span data-stu-id="95232-119">A value of **false** indicates that the underlying contact should not be hidden or displayed as part of the persona.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="95232-120">备注</span><span class="sxs-lookup"><span data-stu-id="95232-120">Remarks</span></span>

<span data-ttu-id="95232-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="95232-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="95232-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="95232-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95232-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="95232-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95232-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="95232-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="95232-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="95232-125">Schema Name</span></span>  <br/> |<span data-ttu-id="95232-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="95232-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="95232-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="95232-127">Validation File</span></span>  <br/> |<span data-ttu-id="95232-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="95232-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="95232-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="95232-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="95232-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95232-130">See also</span></span>



- [<span data-ttu-id="95232-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="95232-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

