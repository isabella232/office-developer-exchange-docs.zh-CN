---
title: 地址（ContactType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c39f37bf-5cf5-47a7-8a2a-337b5e68f94f
description: Address 元素指定联系人的地址。
ms.openlocfilehash: ffb13c8fed28dc1baee5002dc11f7acd7d4c3db5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464908"
---
# <a name="address-contacttype"></a><span data-ttu-id="2f4d7-103">地址（ContactType）</span><span class="sxs-lookup"><span data-stu-id="2f4d7-103">Address (ContactType)</span></span>

<span data-ttu-id="2f4d7-104">**Address**元素指定联系人的地址。</span><span class="sxs-lookup"><span data-stu-id="2f4d7-104">The **Address** element specifies the address of a contact.</span></span> 
  
```XML
<Address></Address>
```

 <span data-ttu-id="2f4d7-105">**xs： string**</span><span class="sxs-lookup"><span data-stu-id="2f4d7-105">**xs:string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f4d7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2f4d7-106">Attributes and elements</span></span>

<span data-ttu-id="2f4d7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2f4d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f4d7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2f4d7-108">Attributes</span></span>

<span data-ttu-id="2f4d7-109">无。</span><span class="sxs-lookup"><span data-stu-id="2f4d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f4d7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2f4d7-110">Child elements</span></span>

<span data-ttu-id="2f4d7-111">无。</span><span class="sxs-lookup"><span data-stu-id="2f4d7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f4d7-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2f4d7-112">Parent elements</span></span>

|<span data-ttu-id="2f4d7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2f4d7-113">**Element**</span></span>|<span data-ttu-id="2f4d7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f4d7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f4d7-115">地址（ArrayOfAddressesType）</span><span class="sxs-lookup"><span data-stu-id="2f4d7-115">Addresses (ArrayOfAddressesType)</span></span>](addresses-arrayofaddressestype.md) <br/> |<span data-ttu-id="2f4d7-116">指定**Address**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="2f4d7-116">Specifies an array of **Address** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2f4d7-117">文本值</span><span class="sxs-lookup"><span data-stu-id="2f4d7-117">Text value</span></span>

<span data-ttu-id="2f4d7-118">**Address**元素的文本值是联系人的邮政地址。</span><span class="sxs-lookup"><span data-stu-id="2f4d7-118">The text value of the **Address** element is the contact's postal address.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2f4d7-119">备注</span><span class="sxs-lookup"><span data-stu-id="2f4d7-119">Remarks</span></span>

<span data-ttu-id="2f4d7-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2f4d7-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2f4d7-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2f4d7-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f4d7-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="2f4d7-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f4d7-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="2f4d7-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2f4d7-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="2f4d7-124">Schema Name</span></span>  <br/> |<span data-ttu-id="2f4d7-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="2f4d7-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="2f4d7-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="2f4d7-126">Validation File</span></span>  <br/> |<span data-ttu-id="2f4d7-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="2f4d7-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2f4d7-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="2f4d7-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2f4d7-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f4d7-129">See also</span></span>

- [<span data-ttu-id="2f4d7-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2f4d7-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

