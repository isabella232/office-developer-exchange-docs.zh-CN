---
title: 地址 (ArrayOfAddressesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 711acc90-8e5b-4658-92d2-16cd441db56e
description: 地址元素指定地址元素的数组。
ms.openlocfilehash: c1ee79611da1d19ce85202f9e3c0f68c421e98c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753129"
---
# <a name="addresses-arrayofaddressestype"></a><span data-ttu-id="ae0bb-103">地址 (ArrayOfAddressesType)</span><span class="sxs-lookup"><span data-stu-id="ae0bb-103">Addresses (ArrayOfAddressesType)</span></span>

<span data-ttu-id="ae0bb-104">**地址**元素指定**地址**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="ae0bb-104">The **Addresses** element specifies an array of **Address** elements.</span></span> 
  
```XML
<Addresses>
    <Address></Address>
</Addresses>
```

 <span data-ttu-id="ae0bb-105">**ArrayOfAddressesType**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-105">**ArrayOfAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae0bb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae0bb-106">Attributes and elements</span></span>

<span data-ttu-id="ae0bb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae0bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae0bb-108">属性</span><span class="sxs-lookup"><span data-stu-id="ae0bb-108">Attributes</span></span>

<span data-ttu-id="ae0bb-109">无。</span><span class="sxs-lookup"><span data-stu-id="ae0bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae0bb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ae0bb-110">Child elements</span></span>

|<span data-ttu-id="ae0bb-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-111">**Element**</span></span>|<span data-ttu-id="ae0bb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae0bb-113">地址 (ContactType)</span><span class="sxs-lookup"><span data-stu-id="ae0bb-113">Address (ContactType)</span></span>](address-contacttype.md) <br/> |<span data-ttu-id="ae0bb-114">指定联系人的地址。</span><span class="sxs-lookup"><span data-stu-id="ae0bb-114">Specifies the address of a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae0bb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ae0bb-115">Parent elements</span></span>

|<span data-ttu-id="ae0bb-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-116">**Element**</span></span>|<span data-ttu-id="ae0bb-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae0bb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae0bb-118">联系人 (ContactType)</span><span class="sxs-lookup"><span data-stu-id="ae0bb-118">Contact (ContactType)</span></span>](contact-contacttype.md) <br/> |<span data-ttu-id="ae0bb-119">指定统一联系人存储库中的联系人。</span><span class="sxs-lookup"><span data-stu-id="ae0bb-119">Specifies a contact in the Unified Contact Store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae0bb-120">备注</span><span class="sxs-lookup"><span data-stu-id="ae0bb-120">Remarks</span></span>

<span data-ttu-id="ae0bb-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ae0bb-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ae0bb-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ae0bb-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae0bb-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae0bb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae0bb-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae0bb-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae0bb-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae0bb-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ae0bb-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="ae0bb-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="ae0bb-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae0bb-127">Validation File</span></span>  <br/> |<span data-ttu-id="ae0bb-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae0bb-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae0bb-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae0bb-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ae0bb-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae0bb-130">See also</span></span>

- [<span data-ttu-id="ae0bb-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ae0bb-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

