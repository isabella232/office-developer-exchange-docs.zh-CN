---
title: BaseShape (PreviewItemBaseShapeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b9e2fdd-5678-4178-9297-7f12a3ca9d64
description: BaseShape 元素指定具有返回的所有属性的默认预览或返回较少属性的精简预览。
ms.openlocfilehash: 29f008840d649f97dfb299fee8e7bf5aaa573404
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527416"
---
# <a name="baseshape-previewitembaseshapetype"></a><span data-ttu-id="98e62-103">BaseShape (PreviewItemBaseShapeType)</span><span class="sxs-lookup"><span data-stu-id="98e62-103">BaseShape (PreviewItemBaseShapeType)</span></span>

<span data-ttu-id="98e62-104">**BaseShape**元素指定具有返回的所有属性的默认预览或返回较少属性的精简预览。</span><span class="sxs-lookup"><span data-stu-id="98e62-104">The **BaseShape** element specifies either the default preview with all properties returned or a compact preview with fewer properties returned.</span></span> 
  
```XML
<BaseShape> Default | Compact</BaseShape>
```

 <span data-ttu-id="98e62-105">**PreviewItemBaseShapeType**</span><span class="sxs-lookup"><span data-stu-id="98e62-105">**PreviewItemBaseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="98e62-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="98e62-106">Attributes and elements</span></span>

<span data-ttu-id="98e62-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="98e62-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98e62-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="98e62-108">Attributes</span></span>

<span data-ttu-id="98e62-109">无。</span><span class="sxs-lookup"><span data-stu-id="98e62-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="98e62-110">子元素</span><span class="sxs-lookup"><span data-stu-id="98e62-110">Child elements</span></span>

<span data-ttu-id="98e62-111">无。</span><span class="sxs-lookup"><span data-stu-id="98e62-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="98e62-112">父元素</span><span class="sxs-lookup"><span data-stu-id="98e62-112">Parent elements</span></span>

|<span data-ttu-id="98e62-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="98e62-113">**Element**</span></span>|<span data-ttu-id="98e62-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="98e62-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="98e62-115">PreviewItemResponseShape</span><span class="sxs-lookup"><span data-stu-id="98e62-115">PreviewItemResponseShape</span></span>](previewitemresponseshape.md) <br/> |<span data-ttu-id="98e62-116">包含响应的形状。</span><span class="sxs-lookup"><span data-stu-id="98e62-116">Contains the shape of the response.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="98e62-117">文本值</span><span class="sxs-lookup"><span data-stu-id="98e62-117">Text value</span></span>

<span data-ttu-id="98e62-118">**BaseShape 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="98e62-118">**BaseShape element text values**</span></span>

|<span data-ttu-id="98e62-119">**值**</span><span class="sxs-lookup"><span data-stu-id="98e62-119">**Value**</span></span>|<span data-ttu-id="98e62-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="98e62-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="98e62-121">默认</span><span class="sxs-lookup"><span data-stu-id="98e62-121">Default</span></span>  <br/> |<span data-ttu-id="98e62-122">指示显示所有属性。</span><span class="sxs-lookup"><span data-stu-id="98e62-122">Indicates that all properties are shown.</span></span>  <br/> |
|<span data-ttu-id="98e62-123">紧凑型</span><span class="sxs-lookup"><span data-stu-id="98e62-123">Compact</span></span>  <br/> |<span data-ttu-id="98e62-124">指示仅显示选定的属性。</span><span class="sxs-lookup"><span data-stu-id="98e62-124">Indicates that only selected properties are shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98e62-125">备注</span><span class="sxs-lookup"><span data-stu-id="98e62-125">Remarks</span></span>

<span data-ttu-id="98e62-126">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="98e62-126">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="98e62-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="98e62-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98e62-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="98e62-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98e62-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="98e62-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="98e62-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="98e62-130">Schema Name</span></span>  <br/> |<span data-ttu-id="98e62-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="98e62-131">Type schema</span></span>  <br/> |
|<span data-ttu-id="98e62-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="98e62-132">Validation File</span></span>  <br/> |<span data-ttu-id="98e62-133">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="98e62-133">types.xsd</span></span>  <br/> |
|<span data-ttu-id="98e62-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="98e62-134">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="98e62-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="98e62-135">See also</span></span>



- [<span data-ttu-id="98e62-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="98e62-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

