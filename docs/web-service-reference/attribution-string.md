---
title: 特性（string）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 736be0bc-12c4-410e-bd17-a89f996ac432
description: 归属元素指定用于标识角色属性的字符串。
ms.openlocfilehash: 9a3243904c02c3bdeea7e4a4e7dcb240d4ad3563
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464159"
---
# <a name="attribution-string"></a><span data-ttu-id="2268e-103">特性（string）</span><span class="sxs-lookup"><span data-stu-id="2268e-103">Attribution (string)</span></span>

<span data-ttu-id="2268e-104">**归属**元素指定用于标识角色属性的字符串。</span><span class="sxs-lookup"><span data-stu-id="2268e-104">The **Attribution** element specifies a string used to identify an attribute of a persona.</span></span> 
  
```XML
<Attribution></Attribution>
```

 <span data-ttu-id="2268e-105">**xs： string**</span><span class="sxs-lookup"><span data-stu-id="2268e-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2268e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2268e-106">Attributes and elements</span></span>

<span data-ttu-id="2268e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2268e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2268e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2268e-108">Attributes</span></span>

<span data-ttu-id="2268e-109">无。</span><span class="sxs-lookup"><span data-stu-id="2268e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2268e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2268e-110">Child elements</span></span>

<span data-ttu-id="2268e-111">无。</span><span class="sxs-lookup"><span data-stu-id="2268e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2268e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2268e-112">Parent elements</span></span>

|<span data-ttu-id="2268e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2268e-113">**Element**</span></span>|<span data-ttu-id="2268e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2268e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2268e-115">归属（ArrayOfValueAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="2268e-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="2268e-116">为其关联的**Value**元素指定归属的数组。</span><span class="sxs-lookup"><span data-stu-id="2268e-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2268e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="2268e-117">Text value</span></span>

<span data-ttu-id="2268e-118">**归属**元素的文本值是一个 string 值，它对源联系人的属性值进行属性。</span><span class="sxs-lookup"><span data-stu-id="2268e-118">The text value of the **attribution** element is a string value that attributes a property value to the source contact.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2268e-119">备注</span><span class="sxs-lookup"><span data-stu-id="2268e-119">Remarks</span></span>

<span data-ttu-id="2268e-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2268e-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2268e-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2268e-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2268e-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="2268e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2268e-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="2268e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2268e-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="2268e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="2268e-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="2268e-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="2268e-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="2268e-126">Validation File</span></span>  <br/> |<span data-ttu-id="2268e-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="2268e-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2268e-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="2268e-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2268e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2268e-129">See also</span></span>

- [<span data-ttu-id="2268e-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2268e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

