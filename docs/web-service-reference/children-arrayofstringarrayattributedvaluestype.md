---
title: 子级（ArrayOfStringArrayAttributedValuesType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d37b3fd5-63f1-4003-a6ec-54adfce23d52
description: Child 元素为关联的角色指定其源归属的子名称和标识符的数组。
ms.openlocfilehash: f4217f8a444bfdb6d86ff7b912294cfad9cbdcdc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460230"
---
# <a name="children-arrayofstringarrayattributedvaluestype"></a><span data-ttu-id="c83f3-103">子级（ArrayOfStringArrayAttributedValuesType）</span><span class="sxs-lookup"><span data-stu-id="c83f3-103">Children (ArrayOfStringArrayAttributedValuesType)</span></span>

<span data-ttu-id="c83f3-104">Child**元素为**关联的角色指定其源归属的子名称和标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="c83f3-104">The **Children** element specifies an array of child names and identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Children>
    <StringAttributedValue></StringAttributedValue>
</Children>
```

 <span data-ttu-id="c83f3-105">**ArrayOfStringArrayAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="c83f3-105">**ArrayOfStringArrayAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c83f3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c83f3-106">Attributes and elements</span></span>

<span data-ttu-id="c83f3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c83f3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c83f3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c83f3-108">Attributes</span></span>

<span data-ttu-id="c83f3-109">无。</span><span class="sxs-lookup"><span data-stu-id="c83f3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c83f3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c83f3-110">Child elements</span></span>

|<span data-ttu-id="c83f3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c83f3-111">**Element**</span></span>|<span data-ttu-id="c83f3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c83f3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c83f3-113">StringArrayAttributedValue</span><span class="sxs-lookup"><span data-stu-id="c83f3-113">StringArrayAttributedValue</span></span>](stringarrayattributedvalue.md) <br/> |<span data-ttu-id="c83f3-114">指定一个 persona 元素的字符串数据数组的实例。</span><span class="sxs-lookup"><span data-stu-id="c83f3-114">Specifies an instance of an array of string data for a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c83f3-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c83f3-115">Parent elements</span></span>

|<span data-ttu-id="c83f3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="c83f3-116">**Element**</span></span>|<span data-ttu-id="c83f3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c83f3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c83f3-118">角色</span><span class="sxs-lookup"><span data-stu-id="c83f3-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="c83f3-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="c83f3-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c83f3-120">备注</span><span class="sxs-lookup"><span data-stu-id="c83f3-120">Remarks</span></span>

<span data-ttu-id="c83f3-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c83f3-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c83f3-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c83f3-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c83f3-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="c83f3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c83f3-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="c83f3-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c83f3-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="c83f3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c83f3-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="c83f3-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="c83f3-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="c83f3-127">Validation File</span></span>  <br/> |<span data-ttu-id="c83f3-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="c83f3-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c83f3-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="c83f3-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c83f3-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c83f3-130">See also</span></span>



- [<span data-ttu-id="c83f3-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c83f3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

