---
title: AltitudeAccuracy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aadc1f90-e9ab-4411-b51f-2d43e5e22f2a
description: AltitudeAccuracy 元素指定邮政地址的海拔属性的精度。
ms.openlocfilehash: 3025982baae130421e5d48aa76ea8dc073f7a656
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464747"
---
# <a name="altitudeaccuracy"></a><span data-ttu-id="d0f12-103">AltitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="d0f12-103">AltitudeAccuracy</span></span>

<span data-ttu-id="d0f12-104">**AltitudeAccuracy**元素指定邮政地址的海拔属性的精度。</span><span class="sxs-lookup"><span data-stu-id="d0f12-104">The **AltitudeAccuracy** element specifies the accuracy of the altitude property for a postal address.</span></span> 
  
```XML
<AltitudeAccuracy></AltitudeAccuracy>
```

 <span data-ttu-id="d0f12-105">**xs： double**</span><span class="sxs-lookup"><span data-stu-id="d0f12-105">**xs:double**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0f12-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d0f12-106">Attributes and elements</span></span>

<span data-ttu-id="d0f12-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d0f12-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0f12-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d0f12-108">Attributes</span></span>

<span data-ttu-id="d0f12-109">无。</span><span class="sxs-lookup"><span data-stu-id="d0f12-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0f12-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d0f12-110">Child elements</span></span>

<span data-ttu-id="d0f12-111">无。</span><span class="sxs-lookup"><span data-stu-id="d0f12-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0f12-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d0f12-112">Parent elements</span></span>

|<span data-ttu-id="d0f12-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d0f12-113">**Element**</span></span>|<span data-ttu-id="d0f12-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d0f12-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0f12-115">省略（PersonaPostalAddressType）</span><span class="sxs-lookup"><span data-stu-id="d0f12-115">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="d0f12-116">指定位置的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="d0f12-116">Specifies the postal address of the location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d0f12-117">文本值</span><span class="sxs-lookup"><span data-stu-id="d0f12-117">Text value</span></span>

<span data-ttu-id="d0f12-118">**AltitudeAccuracy**元素的文本值是通信地址的海拔高度属性的准确性估计值。</span><span class="sxs-lookup"><span data-stu-id="d0f12-118">The text value of the **AltitudeAccuracy** element is the accuracy estimate for the altitude property of a postal address.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0f12-119">备注</span><span class="sxs-lookup"><span data-stu-id="d0f12-119">Remarks</span></span>

<span data-ttu-id="d0f12-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d0f12-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d0f12-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d0f12-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0f12-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="d0f12-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0f12-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="d0f12-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0f12-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="d0f12-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d0f12-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="d0f12-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="d0f12-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="d0f12-126">Validation File</span></span>  <br/> |<span data-ttu-id="d0f12-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="d0f12-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0f12-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="d0f12-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d0f12-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0f12-129">See also</span></span>

- [<span data-ttu-id="d0f12-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d0f12-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

