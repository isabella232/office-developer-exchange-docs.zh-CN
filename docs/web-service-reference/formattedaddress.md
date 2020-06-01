---
title: FormattedAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643f8663-1fab-4625-a7e9-5724e352972b
description: FormattedAddress 元素指定关联的邮政地址的格式化显示值。
ms.openlocfilehash: 9150a3bb5bc81f7afecdafbf0cc33fafff597578
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461938"
---
# <a name="formattedaddress"></a><span data-ttu-id="1aa3c-103">FormattedAddress</span><span class="sxs-lookup"><span data-stu-id="1aa3c-103">FormattedAddress</span></span>

<span data-ttu-id="1aa3c-104">**FormattedAddress**元素指定关联的邮政地址的格式化显示值。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-104">The **FormattedAddress** element specifies the formatted display value of the associated postal address.</span></span> 
  
```XML
<FormattedAddress></FormattedAddress>
```

 <span data-ttu-id="1aa3c-105">**string**</span><span class="sxs-lookup"><span data-stu-id="1aa3c-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1aa3c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1aa3c-106">Attributes and elements</span></span>

<span data-ttu-id="1aa3c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1aa3c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1aa3c-108">Attributes</span></span>

<span data-ttu-id="1aa3c-109">无。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1aa3c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1aa3c-110">Child elements</span></span>

<span data-ttu-id="1aa3c-111">无。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1aa3c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1aa3c-112">Parent elements</span></span>

|<span data-ttu-id="1aa3c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1aa3c-113">**Element**</span></span>|<span data-ttu-id="1aa3c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1aa3c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1aa3c-115">Value （PersonaPostalAddressType）</span><span class="sxs-lookup"><span data-stu-id="1aa3c-115">Value (PersonaPostalAddressType)</span></span>](value-personapostaladdresstype.md) <br/> |<span data-ttu-id="1aa3c-116">指定与邮政地址相关联的信息。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-116">Specifies information associated with a postal address.</span></span>  <br/> |
|[<span data-ttu-id="1aa3c-117">省略（PersonaPostalAddressType）</span><span class="sxs-lookup"><span data-stu-id="1aa3c-117">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="1aa3c-118">指定位置的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-118">Specifies the postal address of the location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1aa3c-119">文本值</span><span class="sxs-lookup"><span data-stu-id="1aa3c-119">Text value</span></span>

<span data-ttu-id="1aa3c-120">**FormattedAddress**元素的文本值是一个 string 值，用于指定已设置格式的地址。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-120">The text value of the **FormattedAddress** element is a string value that specifies the formatted address.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1aa3c-121">备注</span><span class="sxs-lookup"><span data-stu-id="1aa3c-121">Remarks</span></span>

<span data-ttu-id="1aa3c-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1aa3c-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1aa3c-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1aa3c-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="1aa3c-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1aa3c-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="1aa3c-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1aa3c-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="1aa3c-126">Schema Name</span></span>  <br/> |<span data-ttu-id="1aa3c-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="1aa3c-127">Type schema</span></span>  <br/> |
|<span data-ttu-id="1aa3c-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="1aa3c-128">Validation File</span></span>  <br/> |<span data-ttu-id="1aa3c-129">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="1aa3c-129">types.xsd</span></span>  <br/> |
|<span data-ttu-id="1aa3c-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="1aa3c-130">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1aa3c-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1aa3c-131">See also</span></span>



- [<span data-ttu-id="1aa3c-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1aa3c-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

