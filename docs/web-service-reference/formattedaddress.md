---
title: FormattedAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643f8663-1fab-4625-a7e9-5724e352972b
description: FormattedAddress 元素指定关联的邮政地址的格式的显示值。
ms.openlocfilehash: 14c970fcbe20567546e99e637c9c78c6003d9c0f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754407"
---
# <a name="formattedaddress"></a><span data-ttu-id="2ca58-103">FormattedAddress</span><span class="sxs-lookup"><span data-stu-id="2ca58-103">FormattedAddress</span></span>

<span data-ttu-id="2ca58-104">**FormattedAddress**元素指定关联的邮政地址的格式的显示值。</span><span class="sxs-lookup"><span data-stu-id="2ca58-104">The **FormattedAddress** element specifies the formatted display value of the associated postal address.</span></span> 
  
```XML
<FormattedAddress></FormattedAddress>
```

 <span data-ttu-id="2ca58-105">**string**</span><span class="sxs-lookup"><span data-stu-id="2ca58-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ca58-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2ca58-106">Attributes and elements</span></span>

<span data-ttu-id="2ca58-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2ca58-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ca58-108">属性</span><span class="sxs-lookup"><span data-stu-id="2ca58-108">Attributes</span></span>

<span data-ttu-id="2ca58-109">无。</span><span class="sxs-lookup"><span data-stu-id="2ca58-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ca58-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2ca58-110">Child elements</span></span>

<span data-ttu-id="2ca58-111">无。</span><span class="sxs-lookup"><span data-stu-id="2ca58-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2ca58-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2ca58-112">Parent elements</span></span>

|<span data-ttu-id="2ca58-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2ca58-113">**Element**</span></span>|<span data-ttu-id="2ca58-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ca58-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ca58-115">值 (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="2ca58-115">Value (PersonaPostalAddressType)</span></span>](value-personapostaladdresstype.md) <br/> |<span data-ttu-id="2ca58-116">指定与邮寄地址关联的信息。</span><span class="sxs-lookup"><span data-stu-id="2ca58-116">Specifies information associated with a postal address.</span></span>  <br/> |
|[<span data-ttu-id="2ca58-117">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="2ca58-117">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="2ca58-118">指定位置的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="2ca58-118">Specifies the postal address of the location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2ca58-119">文本值</span><span class="sxs-lookup"><span data-stu-id="2ca58-119">Text value</span></span>

<span data-ttu-id="2ca58-120">**FormattedAddress**元素的文本值是一个 string 值，指定格式化的地址。</span><span class="sxs-lookup"><span data-stu-id="2ca58-120">The text value of the **FormattedAddress** element is a string value that specifies the formatted address.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2ca58-121">备注</span><span class="sxs-lookup"><span data-stu-id="2ca58-121">Remarks</span></span>

<span data-ttu-id="2ca58-122">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2ca58-122">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2ca58-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2ca58-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ca58-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="2ca58-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ca58-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="2ca58-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2ca58-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="2ca58-126">Schema Name</span></span>  <br/> |<span data-ttu-id="2ca58-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="2ca58-127">Type schema</span></span>  <br/> |
|<span data-ttu-id="2ca58-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="2ca58-128">Validation File</span></span>  <br/> |<span data-ttu-id="2ca58-129">types.xsd</span><span class="sxs-lookup"><span data-stu-id="2ca58-129">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2ca58-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="2ca58-130">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2ca58-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2ca58-131">See also</span></span>



- [<span data-ttu-id="2ca58-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2ca58-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

