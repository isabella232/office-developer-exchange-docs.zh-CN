---
title: AltitudeAccuracy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aadc1f90-e9ab-4411-b51f-2d43e5e22f2a
description: AltitudeAccuracy 元素指定邮政地址的海拔属性的准确性。
ms.openlocfilehash: 09ec86e4913327feb47067f5e5de7a60efc47bc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753139"
---
# <a name="altitudeaccuracy"></a><span data-ttu-id="567df-103">AltitudeAccuracy</span><span class="sxs-lookup"><span data-stu-id="567df-103">AltitudeAccuracy</span></span>

<span data-ttu-id="567df-104">**AltitudeAccuracy**元素指定邮政地址的海拔属性的准确性。</span><span class="sxs-lookup"><span data-stu-id="567df-104">The **AltitudeAccuracy** element specifies the accuracy of the altitude property for a postal address.</span></span> 
  
```XML
<AltitudeAccuracy></AltitudeAccuracy>
```

 <span data-ttu-id="567df-105">**xs:double**</span><span class="sxs-lookup"><span data-stu-id="567df-105">**xs:double**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="567df-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="567df-106">Attributes and elements</span></span>

<span data-ttu-id="567df-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="567df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="567df-108">属性</span><span class="sxs-lookup"><span data-stu-id="567df-108">Attributes</span></span>

<span data-ttu-id="567df-109">无。</span><span class="sxs-lookup"><span data-stu-id="567df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="567df-110">子元素</span><span class="sxs-lookup"><span data-stu-id="567df-110">Child elements</span></span>

<span data-ttu-id="567df-111">无。</span><span class="sxs-lookup"><span data-stu-id="567df-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="567df-112">父元素</span><span class="sxs-lookup"><span data-stu-id="567df-112">Parent elements</span></span>

|<span data-ttu-id="567df-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="567df-113">**Element**</span></span>|<span data-ttu-id="567df-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="567df-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="567df-115">PostalAddress (PersonaPostalAddressType)</span><span class="sxs-lookup"><span data-stu-id="567df-115">PostalAddress (PersonaPostalAddressType)</span></span>](postaladdress-personapostaladdresstype.md) <br/> |<span data-ttu-id="567df-116">指定位置的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="567df-116">Specifies the postal address of the location.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="567df-117">文本值</span><span class="sxs-lookup"><span data-stu-id="567df-117">Text value</span></span>

<span data-ttu-id="567df-118">**AltitudeAccuracy**元素的文本值是邮寄地址的海拔属性的准确性估计值。</span><span class="sxs-lookup"><span data-stu-id="567df-118">The text value of the **AltitudeAccuracy** element is the accuracy estimate for the altitude property of a postal address.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="567df-119">备注</span><span class="sxs-lookup"><span data-stu-id="567df-119">Remarks</span></span>

<span data-ttu-id="567df-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="567df-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="567df-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="567df-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="567df-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="567df-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="567df-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="567df-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="567df-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="567df-124">Schema Name</span></span>  <br/> |<span data-ttu-id="567df-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="567df-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="567df-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="567df-126">Validation File</span></span>  <br/> |<span data-ttu-id="567df-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="567df-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="567df-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="567df-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="567df-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="567df-129">See also</span></span>

- [<span data-ttu-id="567df-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="567df-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

