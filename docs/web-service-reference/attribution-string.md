---
title: 归属 （字符串）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 736be0bc-12c4-410e-bd17-a89f996ac432
description: 属性元素指定用来标识角色属性的字符串。
ms.openlocfilehash: 227379db8a77fb8cba7b4337e74d985bc5af65d2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753289"
---
# <a name="attribution-string"></a><span data-ttu-id="218cb-103">归属 （字符串）</span><span class="sxs-lookup"><span data-stu-id="218cb-103">Attribution (string)</span></span>

<span data-ttu-id="218cb-104">**属性**元素指定用来标识角色属性的字符串。</span><span class="sxs-lookup"><span data-stu-id="218cb-104">The **Attribution** element specifies a string used to identify an attribute of a persona.</span></span> 
  
```XML
<Attribution></Attribution>
```

 <span data-ttu-id="218cb-105">**将**</span><span class="sxs-lookup"><span data-stu-id="218cb-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="218cb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="218cb-106">Attributes and elements</span></span>

<span data-ttu-id="218cb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="218cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="218cb-108">属性</span><span class="sxs-lookup"><span data-stu-id="218cb-108">Attributes</span></span>

<span data-ttu-id="218cb-109">无。</span><span class="sxs-lookup"><span data-stu-id="218cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="218cb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="218cb-110">Child elements</span></span>

<span data-ttu-id="218cb-111">无。</span><span class="sxs-lookup"><span data-stu-id="218cb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="218cb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="218cb-112">Parent elements</span></span>

|<span data-ttu-id="218cb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="218cb-113">**Element**</span></span>|<span data-ttu-id="218cb-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="218cb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="218cb-115">归属 (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="218cb-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="218cb-116">指定其关联的**值**元素的归属的数组。</span><span class="sxs-lookup"><span data-stu-id="218cb-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="218cb-117">文本值</span><span class="sxs-lookup"><span data-stu-id="218cb-117">Text value</span></span>

<span data-ttu-id="218cb-118">**属性**元素的文本值是一个 string 值，对源联系人属性的属性值。</span><span class="sxs-lookup"><span data-stu-id="218cb-118">The text value of the **attribution** element is a string value that attributes a property value to the source contact.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="218cb-119">备注</span><span class="sxs-lookup"><span data-stu-id="218cb-119">Remarks</span></span>

<span data-ttu-id="218cb-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="218cb-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="218cb-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="218cb-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="218cb-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="218cb-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="218cb-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="218cb-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="218cb-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="218cb-124">Schema Name</span></span>  <br/> |<span data-ttu-id="218cb-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="218cb-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="218cb-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="218cb-126">Validation File</span></span>  <br/> |<span data-ttu-id="218cb-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="218cb-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="218cb-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="218cb-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="218cb-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="218cb-129">See also</span></span>

- [<span data-ttu-id="218cb-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="218cb-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

