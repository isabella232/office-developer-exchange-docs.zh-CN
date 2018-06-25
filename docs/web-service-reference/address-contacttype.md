---
title: 地址 (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c39f37bf-5cf5-47a7-8a2a-337b5e68f94f
description: 在 Address 元素指定联系人的地址。
ms.openlocfilehash: 75fee4bd793497b1758bb848c7aa7dcc4d1a4e8e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753123"
---
# <a name="address-contacttype"></a><span data-ttu-id="b7792-103">地址 (ContactType)</span><span class="sxs-lookup"><span data-stu-id="b7792-103">Address (ContactType)</span></span>

<span data-ttu-id="b7792-104">**在 Address**元素指定联系人的地址。</span><span class="sxs-lookup"><span data-stu-id="b7792-104">The **Address** element specifies the address of a contact.</span></span> 
  
```XML
<Address></Address>
```

 <span data-ttu-id="b7792-105">**将**</span><span class="sxs-lookup"><span data-stu-id="b7792-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7792-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7792-106">Attributes and elements</span></span>

<span data-ttu-id="b7792-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7792-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7792-108">属性</span><span class="sxs-lookup"><span data-stu-id="b7792-108">Attributes</span></span>

<span data-ttu-id="b7792-109">无。</span><span class="sxs-lookup"><span data-stu-id="b7792-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7792-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b7792-110">Child elements</span></span>

<span data-ttu-id="b7792-111">无。</span><span class="sxs-lookup"><span data-stu-id="b7792-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7792-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b7792-112">Parent elements</span></span>

|<span data-ttu-id="b7792-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7792-113">**Element**</span></span>|<span data-ttu-id="b7792-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7792-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7792-115">地址 (ArrayOfAddressesType)</span><span class="sxs-lookup"><span data-stu-id="b7792-115">Addresses (ArrayOfAddressesType)</span></span>](addresses-arrayofaddressestype.md) <br/> |<span data-ttu-id="b7792-116">指定**地址**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="b7792-116">Specifies an array of **Address** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b7792-117">文本值</span><span class="sxs-lookup"><span data-stu-id="b7792-117">Text value</span></span>

<span data-ttu-id="b7792-118">**在 Address**元素的文本值是联系人的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="b7792-118">The text value of the **Address** element is the contact's postal address.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b7792-119">备注</span><span class="sxs-lookup"><span data-stu-id="b7792-119">Remarks</span></span>

<span data-ttu-id="b7792-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b7792-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b7792-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7792-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7792-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7792-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7792-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7792-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b7792-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7792-124">Schema Name</span></span>  <br/> |<span data-ttu-id="b7792-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="b7792-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="b7792-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7792-126">Validation File</span></span>  <br/> |<span data-ttu-id="b7792-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="b7792-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b7792-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7792-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b7792-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7792-129">See also</span></span>

- [<span data-ttu-id="b7792-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7792-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

