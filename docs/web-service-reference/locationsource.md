---
title: LocationSource
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc4d77d5-6200-4cf3-848a-1088fec0e0d6
description: LocationSource 元素指定关联的邮政地址，例如，联系人或电话簿原点有关的信息。
ms.openlocfilehash: 7f5cf5fcca0a72287593349fcf5090a74225d012
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826248"
---
# <a name="locationsource"></a><span data-ttu-id="d4b4a-103">LocationSource</span><span class="sxs-lookup"><span data-stu-id="d4b4a-103">LocationSource</span></span>

<span data-ttu-id="d4b4a-104">**LocationSource**元素指定关联的邮政地址，例如，联系人或电话簿原点有关的信息。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-104">The **LocationSource** element specifies information about the origin of the associated postal address, for example, a contact or a telephone book.</span></span> 
  
```XML
<LocationSource> None | LocationServices | PhonebookServices | Device | Contact | Resource </LocationSource>
```

 <span data-ttu-id="d4b4a-105">**LocationSourceType**</span><span class="sxs-lookup"><span data-stu-id="d4b4a-105">**LocationSourceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4b4a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d4b4a-106">Attributes and elements</span></span>

<span data-ttu-id="d4b4a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4b4a-108">属性</span><span class="sxs-lookup"><span data-stu-id="d4b4a-108">Attributes</span></span>

<span data-ttu-id="d4b4a-109">无。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4b4a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d4b4a-110">Child elements</span></span>

<span data-ttu-id="d4b4a-111">无。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d4b4a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d4b4a-112">Parent elements</span></span>

<span data-ttu-id="d4b4a-113">[值 (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span><span class="sxs-lookup"><span data-stu-id="d4b4a-113">[Value (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [PostalAddress (PersonaPostalAddressType)](postaladdress-personapostaladdresstype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d4b4a-114">文本值</span><span class="sxs-lookup"><span data-stu-id="d4b4a-114">Text value</span></span>

<span data-ttu-id="d4b4a-115">下表中列出的**LocationSource**元素的文本值：</span><span class="sxs-lookup"><span data-stu-id="d4b4a-115">The text values for the **LocationSource** element are listed in the following table:</span></span> 
  
<span data-ttu-id="d4b4a-116">**LocationSource 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="d4b4a-116">**LocationSource element text values**</span></span>

|<span data-ttu-id="d4b4a-117">**值**</span><span class="sxs-lookup"><span data-stu-id="d4b4a-117">**Value**</span></span>|<span data-ttu-id="d4b4a-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="d4b4a-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4b4a-119">无</span><span class="sxs-lookup"><span data-stu-id="d4b4a-119">None</span></span>  <br/> |<span data-ttu-id="d4b4a-120">没有任何位置源。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-120">There is no location source.</span></span>  <br/> |
|<span data-ttu-id="d4b4a-121">LocationServices</span><span class="sxs-lookup"><span data-stu-id="d4b4a-121">LocationServices</span></span>  <br/> |<span data-ttu-id="d4b4a-122">从位置服务已获得的信息。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-122">The information was obtained from location services.</span></span>  <br/> |
|<span data-ttu-id="d4b4a-123">PhonebookServices</span><span class="sxs-lookup"><span data-stu-id="d4b4a-123">PhonebookServices</span></span>  <br/> |<span data-ttu-id="d4b4a-124">从通讯簿服务已获得的信息。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-124">The information was obtained from phonebook services.</span></span>  <br/> |
|<span data-ttu-id="d4b4a-125">设备</span><span class="sxs-lookup"><span data-stu-id="d4b4a-125">Device</span></span>  <br/> |<span data-ttu-id="d4b4a-126">从设备已获得的信息。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-126">The information was obtained from the device.</span></span>  <br/> |
|<span data-ttu-id="d4b4a-127">联系人</span><span class="sxs-lookup"><span data-stu-id="d4b4a-127">Contact</span></span>  <br/> |<span data-ttu-id="d4b4a-128">从联系人已获得的信息。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-128">The information was obtained from a contact.</span></span>  <br/> |
|<span data-ttu-id="d4b4a-129">资源</span><span class="sxs-lookup"><span data-stu-id="d4b4a-129">Resource</span></span>  <br/> |<span data-ttu-id="d4b4a-130">从一个资源已获得的信息。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-130">The information was obtained from a resource.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4b4a-131">备注</span><span class="sxs-lookup"><span data-stu-id="d4b4a-131">Remarks</span></span>

<span data-ttu-id="d4b4a-132">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-132">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d4b4a-133">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d4b4a-133">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  

