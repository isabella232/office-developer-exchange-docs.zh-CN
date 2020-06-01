---
title: BusinessPhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ecbe4f1c-1c9e-44e0-a8f7-08c160a0fddb
description: BusinessPhoneNumbers 元素指定业务电话号码的数组以及关联角色的源归属的标识符。
ms.openlocfilehash: 8713af3ad302a2940cab247ff7188e55e8021ca0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461616"
---
# <a name="businessphonenumbers"></a><span data-ttu-id="d949d-103">BusinessPhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="d949d-103">BusinessPhoneNumbers</span></span>

<span data-ttu-id="d949d-104">**BusinessPhoneNumbers**元素指定业务电话号码的数组以及关联角色的源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="d949d-104">The **BusinessPhoneNumbers** element specifies an array of business phone numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessPhoneNumbers>
    <Value></Value>
    <Attributions></Attributions>
</BusinessPhoneNumbers>
```

 <span data-ttu-id="d949d-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="d949d-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d949d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d949d-106">Attributes and elements</span></span>

<span data-ttu-id="d949d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d949d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d949d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d949d-108">Attributes</span></span>

<span data-ttu-id="d949d-109">无。</span><span class="sxs-lookup"><span data-stu-id="d949d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d949d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d949d-110">Child elements</span></span>

|<span data-ttu-id="d949d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d949d-111">**Element**</span></span>|<span data-ttu-id="d949d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d949d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d949d-113">Value （PersonaPhoneNumberType）</span><span class="sxs-lookup"><span data-stu-id="d949d-113">Value (PersonaPhoneNumberType)</span></span>](value-personaphonenumbertype.md) <br/> |<span data-ttu-id="d949d-114">指定电话号码和类型信息，并与一组归属相关联。</span><span class="sxs-lookup"><span data-stu-id="d949d-114">Specifies a phone number and type information and is associated with a set of attributions.</span></span>  <br/> |
|[<span data-ttu-id="d949d-115">归属（ArrayOfValueAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="d949d-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="d949d-116">为其关联的**Value**元素指定归属的数组。</span><span class="sxs-lookup"><span data-stu-id="d949d-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d949d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d949d-117">Parent elements</span></span>

|<span data-ttu-id="d949d-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="d949d-118">**Element**</span></span>|<span data-ttu-id="d949d-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d949d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d949d-120">角色</span><span class="sxs-lookup"><span data-stu-id="d949d-120">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="d949d-121">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="d949d-121">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d949d-122">备注</span><span class="sxs-lookup"><span data-stu-id="d949d-122">Remarks</span></span>

<span data-ttu-id="d949d-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d949d-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d949d-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d949d-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d949d-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="d949d-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d949d-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="d949d-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d949d-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="d949d-127">Schema Name</span></span>  <br/> |<span data-ttu-id="d949d-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="d949d-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="d949d-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="d949d-129">Validation File</span></span>  <br/> |<span data-ttu-id="d949d-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="d949d-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d949d-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="d949d-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d949d-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d949d-132">See also</span></span>



- [<span data-ttu-id="d949d-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d949d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

