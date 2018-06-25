---
title: 正文
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a71a75f0-0b77-4cb9-8f9d-319de72fc1fd
description: 正文元素指定 BodyContentAttributedValue 元素的数组。
ms.openlocfilehash: 3316d25a567a791301c0e703a912ef28da42fa74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753348"
---
# <a name="bodies"></a><span data-ttu-id="e8376-103">正文</span><span class="sxs-lookup"><span data-stu-id="e8376-103">Bodies</span></span>

<span data-ttu-id="e8376-104">**正文**元素指定**BodyContentAttributedValue**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="e8376-104">The **Bodies** element specifies an array of **BodyContentAttributedValue** elements.</span></span> 
  
```XML
<Bodies>
    <BodyContentAttributedValue></BodyContentAttributedValue>
<Bodies>
```

 <span data-ttu-id="e8376-105">**ArrayOfBodyContentAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="e8376-105">**ArrayOfBodyContentAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8376-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e8376-106">Attributes and elements</span></span>

<span data-ttu-id="e8376-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e8376-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8376-108">属性</span><span class="sxs-lookup"><span data-stu-id="e8376-108">Attributes</span></span>

<span data-ttu-id="e8376-109">无。</span><span class="sxs-lookup"><span data-stu-id="e8376-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8376-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e8376-110">Child elements</span></span>

|<span data-ttu-id="e8376-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e8376-111">**Element**</span></span>|<span data-ttu-id="e8376-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e8376-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8376-113">BodyContentAttributedValue</span><span class="sxs-lookup"><span data-stu-id="e8376-113">BodyContentAttributedValue</span></span>](bodycontentattributedvalue.md) <br/> |<span data-ttu-id="e8376-114">指定项目的正文内容。</span><span class="sxs-lookup"><span data-stu-id="e8376-114">Specifies the body content of an item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8376-115">父元素</span><span class="sxs-lookup"><span data-stu-id="e8376-115">Parent elements</span></span>

|<span data-ttu-id="e8376-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e8376-116">**Element**</span></span>|<span data-ttu-id="e8376-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e8376-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8376-118">角色</span><span class="sxs-lookup"><span data-stu-id="e8376-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="e8376-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="e8376-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8376-120">备注</span><span class="sxs-lookup"><span data-stu-id="e8376-120">Remarks</span></span>

<span data-ttu-id="e8376-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e8376-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e8376-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e8376-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8376-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="e8376-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8376-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="e8376-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e8376-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="e8376-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e8376-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="e8376-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="e8376-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="e8376-127">Validation File</span></span>  <br/> |<span data-ttu-id="e8376-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="e8376-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e8376-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="e8376-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e8376-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8376-130">See also</span></span>



- [<span data-ttu-id="e8376-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e8376-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

