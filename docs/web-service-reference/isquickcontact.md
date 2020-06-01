---
title: IsQuickContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9542d6-ef72-4743-828a-bb671e783836
description: IsQuickContact 元素指定一个布尔值，该值指示基础联系人是否为 "快速联系人"。
ms.openlocfilehash: a8944be111a8dcbe914601ffc4e31794422d58aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44441574"
---
# <a name="isquickcontact"></a><span data-ttu-id="7a2bb-103">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="7a2bb-103">IsQuickContact</span></span>

<span data-ttu-id="7a2bb-104">**IsQuickContact**元素指定一个布尔值，该值指示基础联系人是否为 "快速联系人"。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-104">The **IsQuickContact** element specifies a Boolean value that indicates whether the underlying contact is a quick contact.</span></span> 
  
```XML
<IsQuickContact>true | false</IsQuickContact>
```

 <span data-ttu-id="7a2bb-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="7a2bb-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7a2bb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7a2bb-106">Attributes and elements</span></span>

<span data-ttu-id="7a2bb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7a2bb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7a2bb-108">Attributes</span></span>

<span data-ttu-id="7a2bb-109">无。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7a2bb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7a2bb-110">Child elements</span></span>

<span data-ttu-id="7a2bb-111">无。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7a2bb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7a2bb-112">Parent elements</span></span>

|<span data-ttu-id="7a2bb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7a2bb-113">**Element**</span></span>|<span data-ttu-id="7a2bb-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7a2bb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a2bb-115">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="7a2bb-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="7a2bb-116">指定一个**Persona**元素的属性数组中的一个实例。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7a2bb-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7a2bb-117">Text value</span></span>

<span data-ttu-id="7a2bb-118">如果**IsQuickContact**元素的文本值为**true** ，则表示该联系人是一个快速联系人。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-118">A text value of **true** for the **IsQuickContact** element indicates that the contact is a quick contact.</span></span> <span data-ttu-id="7a2bb-119">**如果值为 false** ，则表示联系人不是快速联系人。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-119">A value of **false** indicates that the contact is not a quick contact.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7a2bb-120">备注</span><span class="sxs-lookup"><span data-stu-id="7a2bb-120">Remarks</span></span>

<span data-ttu-id="7a2bb-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7a2bb-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7a2bb-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7a2bb-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="7a2bb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7a2bb-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="7a2bb-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7a2bb-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="7a2bb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7a2bb-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="7a2bb-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="7a2bb-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="7a2bb-127">Validation File</span></span>  <br/> |<span data-ttu-id="7a2bb-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="7a2bb-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="7a2bb-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="7a2bb-129">Can Be Empty</span></span>  <br/> |<span data-ttu-id="7a2bb-130">false</span><span class="sxs-lookup"><span data-stu-id="7a2bb-130">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a2bb-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7a2bb-131">See also</span></span>



- [<span data-ttu-id="7a2bb-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7a2bb-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

