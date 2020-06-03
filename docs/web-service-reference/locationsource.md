---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: LocationSource 元素指定有关关联邮政地址的来源的信息，例如，联系人或电话簿。
ms.openlocfilehash: ceba52c43d1c798bb8f5492b779c7c45d7d00b0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467100"
---
# <a name="locationsource"></a><span data-ttu-id="dc129-103">LocationSource</span><span class="sxs-lookup"><span data-stu-id="dc129-103">LocationSource</span></span>

<span data-ttu-id="dc129-104">**LocationSource**元素指定有关关联邮政地址的来源的信息，例如，联系人或电话簿。</span><span class="sxs-lookup"><span data-stu-id="dc129-104">The **LocationSource** element specifies information about the origin of the associated postal address, for example, a contact or a telephone book.</span></span> 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 <span data-ttu-id="dc129-105">**LocationSourceType**</span><span class="sxs-lookup"><span data-stu-id="dc129-105">**LocationSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc129-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc129-106">Attributes and elements</span></span>

<span data-ttu-id="dc129-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc129-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc129-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dc129-108">Attributes</span></span>

<span data-ttu-id="dc129-109">无。</span><span class="sxs-lookup"><span data-stu-id="dc129-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc129-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dc129-110">Child elements</span></span>

<span data-ttu-id="dc129-111">无。</span><span class="sxs-lookup"><span data-stu-id="dc129-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc129-112">父元素</span><span class="sxs-lookup"><span data-stu-id="dc129-112">Parent elements</span></span>

<span data-ttu-id="dc129-113">[Value （PersonaPostalAddressType）](value-personapostaladdresstype.md)  | [省略（PersonaPostalAddressType）](postaladdress-personapostaladdresstype.md)</span><span class="sxs-lookup"><span data-stu-id="dc129-113">[Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="dc129-114">文本值</span><span class="sxs-lookup"><span data-stu-id="dc129-114">Text value</span></span>

<span data-ttu-id="dc129-115">下表列出了**LocationSource**元素的文本值：</span><span class="sxs-lookup"><span data-stu-id="dc129-115">The text values for the **LocationSource** element are listed in the following table:</span></span> 
  
<span data-ttu-id="dc129-116">**LocationSource 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="dc129-116">**LocationSource element text values**</span></span>

|<span data-ttu-id="dc129-117">**值**</span><span class="sxs-lookup"><span data-stu-id="dc129-117">**Value**</span></span>|<span data-ttu-id="dc129-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc129-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc129-119">无</span><span class="sxs-lookup"><span data-stu-id="dc129-119">None</span></span>  <br/> |<span data-ttu-id="dc129-120">没有位置源。</span><span class="sxs-lookup"><span data-stu-id="dc129-120">There is no location source.</span></span>  <br/> |
|<span data-ttu-id="dc129-121">LocationServices</span><span class="sxs-lookup"><span data-stu-id="dc129-121">LocationServices</span></span>  <br/> |<span data-ttu-id="dc129-122">信息是从位置服务获取的。</span><span class="sxs-lookup"><span data-stu-id="dc129-122">The information was obtained from location services.</span></span>  <br/> |
|<span data-ttu-id="dc129-123">PhonebookServices</span><span class="sxs-lookup"><span data-stu-id="dc129-123">PhonebookServices</span></span>  <br/> |<span data-ttu-id="dc129-124">此信息是通过电话簿服务获取的。</span><span class="sxs-lookup"><span data-stu-id="dc129-124">The information was obtained from phonebook services.</span></span>  <br/> |
|<span data-ttu-id="dc129-125">设备</span><span class="sxs-lookup"><span data-stu-id="dc129-125">Device</span></span>  <br/> |<span data-ttu-id="dc129-126">信息是从设备获取的。</span><span class="sxs-lookup"><span data-stu-id="dc129-126">The information was obtained from the device.</span></span>  <br/> |
|<span data-ttu-id="dc129-127">Contact</span><span class="sxs-lookup"><span data-stu-id="dc129-127">Contact</span></span>  <br/> |<span data-ttu-id="dc129-128">信息是从联系人获取的。</span><span class="sxs-lookup"><span data-stu-id="dc129-128">The information was obtained from a contact.</span></span>  <br/> |
|<span data-ttu-id="dc129-129">Resource</span><span class="sxs-lookup"><span data-stu-id="dc129-129">Resource</span></span>  <br/> |<span data-ttu-id="dc129-130">信息是从资源获取的。</span><span class="sxs-lookup"><span data-stu-id="dc129-130">The information was obtained from a resource.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc129-131">备注</span><span class="sxs-lookup"><span data-stu-id="dc129-131">Remarks</span></span>

<span data-ttu-id="dc129-132">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="dc129-132">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc129-133">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc129-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

