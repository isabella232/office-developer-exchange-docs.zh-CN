---
title: IsQuickContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9542d6-ef72-4743-828a-bb671e783836
description: IsQuickContact 元素指定一个布尔值，该值指示基础联系人是否快速联系人。
ms.openlocfilehash: 979dbd3c0358eacd443eed79b258f7dd6bb9bc7d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826092"
---
# <a name="isquickcontact"></a><span data-ttu-id="36308-103">IsQuickContact</span><span class="sxs-lookup"><span data-stu-id="36308-103">IsQuickContact</span></span>

<span data-ttu-id="36308-104">**IsQuickContact**元素指定一个布尔值，该值指示基础联系人是否快速联系人。</span><span class="sxs-lookup"><span data-stu-id="36308-104">The **IsQuickContact** element specifies a Boolean value that indicates whether the underlying contact is a quick contact.</span></span> 
  
```XML
<IsQuickContact>true | false</IsQuickContact>
```

 <span data-ttu-id="36308-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="36308-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36308-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="36308-106">Attributes and elements</span></span>

<span data-ttu-id="36308-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="36308-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36308-108">属性</span><span class="sxs-lookup"><span data-stu-id="36308-108">Attributes</span></span>

<span data-ttu-id="36308-109">无。</span><span class="sxs-lookup"><span data-stu-id="36308-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36308-110">子元素</span><span class="sxs-lookup"><span data-stu-id="36308-110">Child elements</span></span>

<span data-ttu-id="36308-111">无。</span><span class="sxs-lookup"><span data-stu-id="36308-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="36308-112">父元素</span><span class="sxs-lookup"><span data-stu-id="36308-112">Parent elements</span></span>

|<span data-ttu-id="36308-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="36308-113">**Element**</span></span>|<span data-ttu-id="36308-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="36308-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36308-115">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="36308-115">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="36308-116">**个人**元素的属性数组中指定的实例。</span><span class="sxs-lookup"><span data-stu-id="36308-116">Specifies an instance in an array of attributes for a **Persona** element.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36308-117">文本值</span><span class="sxs-lookup"><span data-stu-id="36308-117">Text value</span></span>

<span data-ttu-id="36308-118">文本值为**true**的**IsQuickContact**元素指示联系人快速联系人。</span><span class="sxs-lookup"><span data-stu-id="36308-118">A text value of **true** for the **IsQuickContact** element indicates that the contact is a quick contact.</span></span> <span data-ttu-id="36308-119">如果值为**false**指示该联系人不快速联系人。</span><span class="sxs-lookup"><span data-stu-id="36308-119">A value of **false** indicates that the contact is not a quick contact.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="36308-120">备注</span><span class="sxs-lookup"><span data-stu-id="36308-120">Remarks</span></span>

<span data-ttu-id="36308-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="36308-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="36308-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="36308-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36308-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="36308-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36308-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="36308-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="36308-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="36308-125">Schema Name</span></span>  <br/> |<span data-ttu-id="36308-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="36308-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="36308-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="36308-127">Validation File</span></span>  <br/> |<span data-ttu-id="36308-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="36308-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="36308-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="36308-129">Can Be Empty</span></span>  <br/> |<span data-ttu-id="36308-130">false</span><span class="sxs-lookup"><span data-stu-id="36308-130">false</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36308-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36308-131">See also</span></span>



- [<span data-ttu-id="36308-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="36308-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

