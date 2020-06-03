---
title: BodyContentAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f99e9590-8388-4203-ac30-1ea394f351a6
description: BodyContentAttributedValue 元素指定项目的正文内容。
ms.openlocfilehash: 3550d9307e9bd652afc217f72610379a0a5b2f68
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527395"
---
# <a name="bodycontentattributedvalue"></a><span data-ttu-id="46084-103">BodyContentAttributedValue</span><span class="sxs-lookup"><span data-stu-id="46084-103">BodyContentAttributedValue</span></span>

<span data-ttu-id="46084-104">**BodyContentAttributedValue**元素指定项目的正文内容。</span><span class="sxs-lookup"><span data-stu-id="46084-104">The **BodyContentAttributedValue** element specifies the body content of an item.</span></span> 
  
```XML
<BodyContentAttributedValue>
   <Value></Value>
   <Attributions></Attributions>
</ BodyContentAttributedValue>
```

 <span data-ttu-id="46084-105">**BodyContentAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="46084-105">**BodyContentAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46084-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="46084-106">Attributes and elements</span></span>

<span data-ttu-id="46084-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="46084-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46084-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="46084-108">Attributes</span></span>

<span data-ttu-id="46084-109">无。</span><span class="sxs-lookup"><span data-stu-id="46084-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46084-110">子元素</span><span class="sxs-lookup"><span data-stu-id="46084-110">Child elements</span></span>

|<span data-ttu-id="46084-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="46084-111">**Element**</span></span>|<span data-ttu-id="46084-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="46084-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46084-113">Value （BodyContentType）</span><span class="sxs-lookup"><span data-stu-id="46084-113">Value (BodyContentType)</span></span>](value-bodycontenttype.md) <br/> |<span data-ttu-id="46084-114">指定**BodyContentAttributedValue**元素的值。</span><span class="sxs-lookup"><span data-stu-id="46084-114">Specifies the value of a **BodyContentAttributedValue** element.</span></span>  <br/> |
|[<span data-ttu-id="46084-115">归属（ArrayOfPersonaAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="46084-115">Attributions (ArrayOfPersonaAttributionsType)</span></span>](attributions-arrayofpersonaattributionstype.md) <br/> |<span data-ttu-id="46084-116">为聚合到关联角色中的一个或多个联系人或 active directory 收件人指定归属信息的数组。</span><span class="sxs-lookup"><span data-stu-id="46084-116">Specifies an array of attribution information for one or more of the contacts or active directory recipients aggregated into the associated persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46084-117">父元素</span><span class="sxs-lookup"><span data-stu-id="46084-117">Parent elements</span></span>

|<span data-ttu-id="46084-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="46084-118">**Element**</span></span>|<span data-ttu-id="46084-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="46084-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46084-120">团体</span><span class="sxs-lookup"><span data-stu-id="46084-120">Bodies</span></span>](bodies.md) <br/> |<span data-ttu-id="46084-121">指定**BodyContentAttributedValue**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="46084-121">Specifies an array of **BodyContentAttributedValue** elements.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46084-122">备注</span><span class="sxs-lookup"><span data-stu-id="46084-122">Remarks</span></span>

<span data-ttu-id="46084-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="46084-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="46084-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="46084-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46084-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="46084-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46084-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="46084-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="46084-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="46084-127">Schema Name</span></span>  <br/> |<span data-ttu-id="46084-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="46084-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="46084-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="46084-129">Validation File</span></span>  <br/> |<span data-ttu-id="46084-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="46084-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="46084-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="46084-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="46084-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46084-132">See also</span></span>



- [<span data-ttu-id="46084-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="46084-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

