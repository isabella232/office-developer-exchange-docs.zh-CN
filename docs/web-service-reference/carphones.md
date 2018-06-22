---
title: CarPhones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ad096246-113c-42ea-9e63-861b546003e8
description: CarPhone 元素指定一个数组汽车电话号码和为相关联的角色其源归属的标识符。
ms.openlocfilehash: 694b3578e127a84dfd2fb844c6e81b28553b687c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753436"
---
# <a name="carphones"></a><span data-ttu-id="954ad-103">CarPhones</span><span class="sxs-lookup"><span data-stu-id="954ad-103">CarPhones</span></span>

<span data-ttu-id="954ad-104">**CarPhone**元素指定一个数组汽车电话号码和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="954ad-104">The **CarPhone** element specifies an array of car phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<CarPhones>
    <Value></Value>
    <Attributions></Attributions>
</CarPhones>
```

 <span data-ttu-id="954ad-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="954ad-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="954ad-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="954ad-106">Attributes and elements</span></span>

<span data-ttu-id="954ad-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="954ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="954ad-108">属性</span><span class="sxs-lookup"><span data-stu-id="954ad-108">Attributes</span></span>

<span data-ttu-id="954ad-109">无。</span><span class="sxs-lookup"><span data-stu-id="954ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="954ad-110">子元素</span><span class="sxs-lookup"><span data-stu-id="954ad-110">Child elements</span></span>

|<span data-ttu-id="954ad-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="954ad-111">**Element**</span></span>|<span data-ttu-id="954ad-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="954ad-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="954ad-113">值 (PersonaPhoneNumberType)</span><span class="sxs-lookup"><span data-stu-id="954ad-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="954ad-114">指定电话号码和类型信息并与归属的一组相关联。</span><span class="sxs-lookup"><span data-stu-id="954ad-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="954ad-115">归属 (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="954ad-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="954ad-116">指定其关联的**值**元素的归属的数组。</span><span class="sxs-lookup"><span data-stu-id="954ad-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="954ad-117">父元素</span><span class="sxs-lookup"><span data-stu-id="954ad-117">Parent elements</span></span>

|<span data-ttu-id="954ad-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="954ad-118">**Element**</span></span>|<span data-ttu-id="954ad-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="954ad-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="954ad-120">角色</span><span class="sxs-lookup"><span data-stu-id="954ad-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="954ad-121">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="954ad-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="954ad-122">备注</span><span class="sxs-lookup"><span data-stu-id="954ad-122">Remarks</span></span>

<span data-ttu-id="954ad-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="954ad-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="954ad-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="954ad-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="954ad-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="954ad-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="954ad-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="954ad-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="954ad-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="954ad-127">Schema Name</span></span>  <br/> |<span data-ttu-id="954ad-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="954ad-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="954ad-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="954ad-129">Validation File</span></span>  <br/> |<span data-ttu-id="954ad-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="954ad-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="954ad-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="954ad-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="954ad-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="954ad-132">See also</span></span>



- [<span data-ttu-id="954ad-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="954ad-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

