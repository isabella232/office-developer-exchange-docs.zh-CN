---
title: 地址（ArrayOfAddressesType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 711acc90-8e5b-4658-92d2-16cd441db56e
description: Addresses 元素指定 Address 元素的数组。
ms.openlocfilehash: 8b3a62e22cb7fc983fba78517fe4636797d06f5b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463620"
---
# <a name="addresses-arrayofaddressestype"></a><span data-ttu-id="fa838-103">地址（ArrayOfAddressesType）</span><span class="sxs-lookup"><span data-stu-id="fa838-103">Addresses (ArrayOfAddressesType)</span></span>

<span data-ttu-id="fa838-104">**Addresses**元素指定**Address**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="fa838-104">The **Addresses** element specifies an array of **Address** elements.</span></span> 
  
```XML
<Addresses>
    <Address></Address>
</Addresses>
```

 <span data-ttu-id="fa838-105">**ArrayOfAddressesType**</span><span class="sxs-lookup"><span data-stu-id="fa838-105">**ArrayOfAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa838-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa838-106">Attributes and elements</span></span>

<span data-ttu-id="fa838-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa838-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa838-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fa838-108">Attributes</span></span>

<span data-ttu-id="fa838-109">无。</span><span class="sxs-lookup"><span data-stu-id="fa838-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa838-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fa838-110">Child elements</span></span>

|<span data-ttu-id="fa838-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa838-111">**Element**</span></span>|<span data-ttu-id="fa838-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa838-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa838-113">地址（ContactType）</span><span class="sxs-lookup"><span data-stu-id="fa838-113">Address (ContactType)</span></span>](address-contacttype.md) <br/> |<span data-ttu-id="fa838-114">指定联系人的地址。</span><span class="sxs-lookup"><span data-stu-id="fa838-114">Specifies the address of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa838-115">父元素</span><span class="sxs-lookup"><span data-stu-id="fa838-115">Parent elements</span></span>

|<span data-ttu-id="fa838-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa838-116">**Element**</span></span>|<span data-ttu-id="fa838-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa838-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa838-118">Contact （ContactType）</span><span class="sxs-lookup"><span data-stu-id="fa838-118">Contact (ContactType)</span></span>](contact-contacttype.md) <br/> |<span data-ttu-id="fa838-119">指定统一联系人存储库中的联系人。</span><span class="sxs-lookup"><span data-stu-id="fa838-119">Specifies a contact in the Unified Contact Store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa838-120">备注</span><span class="sxs-lookup"><span data-stu-id="fa838-120">Remarks</span></span>

<span data-ttu-id="fa838-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fa838-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa838-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa838-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa838-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa838-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa838-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa838-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa838-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa838-125">Schema Name</span></span>  <br/> |<span data-ttu-id="fa838-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="fa838-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="fa838-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa838-127">Validation File</span></span>  <br/> |<span data-ttu-id="fa838-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="fa838-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa838-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa838-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fa838-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa838-130">See also</span></span>

- [<span data-ttu-id="fa838-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fa838-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

