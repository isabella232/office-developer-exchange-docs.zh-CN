---
title: 类型（字符串）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d5eea7a8-c40d-42a6-8e0d-67f3252496cf
description: Type 元素指定邮政地址或电话号码的类型，例如，HomeorBusiness。
ms.openlocfilehash: 83dd6576e8a365be61c4e6d2f3afc8a59aba92a6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465714"
---
# <a name="type-string"></a><span data-ttu-id="85082-103">类型（字符串）</span><span class="sxs-lookup"><span data-stu-id="85082-103">Type (string)</span></span>

<span data-ttu-id="85082-104">**Type**元素指定邮寄地址或电话号码的类型，例如 "住宅" 或 "商务"。</span><span class="sxs-lookup"><span data-stu-id="85082-104">The **Type** element specifies the type of postal address or phone number, for example, "Home" or "Business".</span></span> 
  
```XML
<Type></Type>
```

 <span data-ttu-id="85082-105">**string**</span><span class="sxs-lookup"><span data-stu-id="85082-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85082-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85082-106">Attributes and elements</span></span>

<span data-ttu-id="85082-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85082-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85082-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="85082-108">Attributes</span></span>

<span data-ttu-id="85082-109">无。</span><span class="sxs-lookup"><span data-stu-id="85082-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85082-110">子元素</span><span class="sxs-lookup"><span data-stu-id="85082-110">Child elements</span></span>

<span data-ttu-id="85082-111">无。</span><span class="sxs-lookup"><span data-stu-id="85082-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85082-112">父元素</span><span class="sxs-lookup"><span data-stu-id="85082-112">Parent elements</span></span>

<span data-ttu-id="85082-113">[电话](phone.md)  | [PhoneNumber](phonenumber.md)  | [Value （PersonaPostalAddressType）](value-personapostaladdresstype.md)  | [省略（PersonaPostalAddressType）](postaladdress-personapostaladdresstype.md)</span><span class="sxs-lookup"><span data-stu-id="85082-113">[Phone](phone.md) | [PhoneNumber](phonenumber.md) | [Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="85082-114">文本值</span><span class="sxs-lookup"><span data-stu-id="85082-114">Text value</span></span>

<span data-ttu-id="85082-115">**Type**元素的文本值是邮政地址或电话号码的类型。</span><span class="sxs-lookup"><span data-stu-id="85082-115">The text value of the **Type** element is the type of a postal address or phone number.</span></span> <span data-ttu-id="85082-116">例如，值 "Home" 或 "Business" 是**Type**元素的预期值。</span><span class="sxs-lookup"><span data-stu-id="85082-116">For example, the values "Home" or "Business" are expected values for the **Type** element.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85082-117">备注</span><span class="sxs-lookup"><span data-stu-id="85082-117">Remarks</span></span>

<span data-ttu-id="85082-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="85082-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="85082-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="85082-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85082-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="85082-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85082-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="85082-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85082-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="85082-122">Schema name</span></span>  <br/> |<span data-ttu-id="85082-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="85082-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="85082-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="85082-124">Validation file</span></span>  <br/> |<span data-ttu-id="85082-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85082-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85082-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="85082-126">Can be empty</span></span>  <br/> ||
   

