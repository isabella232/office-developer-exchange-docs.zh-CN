---
title: 地址（ArrayOfAddressEntitiesType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c1f3fd3-1b78-46ee-8dd4-b2aff51e767e
description: Addresses 元素指定 AddressEntity 元素的数组。
ms.openlocfilehash: 48cf8c0fda6a8ef894ef8d3a4c154f7255b218bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463627"
---
# <a name="addresses-arrayofaddressentitiestype"></a><span data-ttu-id="be399-103">地址（ArrayOfAddressEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="be399-103">Addresses (ArrayOfAddressEntitiesType)</span></span>

<span data-ttu-id="be399-104">**Addresses**元素指定**AddressEntity**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="be399-104">The **Addresses** element specifies an array of **AddressEntity** elements.</span></span> 
  
```XML
<Addresses>
   <AddressEntity/>
</Addresses>
```

 <span data-ttu-id="be399-105">**ArrayOfAddressEntitiesType**</span><span class="sxs-lookup"><span data-stu-id="be399-105">**ArrayOfAddressEntitiesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="be399-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="be399-106">Attributes and elements</span></span>

<span data-ttu-id="be399-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be399-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be399-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="be399-108">Attributes</span></span>

<span data-ttu-id="be399-109">无。</span><span class="sxs-lookup"><span data-stu-id="be399-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be399-110">子元素</span><span class="sxs-lookup"><span data-stu-id="be399-110">Child elements</span></span>

|<span data-ttu-id="be399-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="be399-111">**Element**</span></span>|<span data-ttu-id="be399-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="be399-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be399-113">AddressEntity</span><span class="sxs-lookup"><span data-stu-id="be399-113">AddressEntity</span></span>](addressentity.md) <br/> |<span data-ttu-id="be399-114">指定单个地址实体。</span><span class="sxs-lookup"><span data-stu-id="be399-114">Specifies a single address entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="be399-115">父元素</span><span class="sxs-lookup"><span data-stu-id="be399-115">Parent elements</span></span>

|<span data-ttu-id="be399-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="be399-116">**Element**</span></span>|<span data-ttu-id="be399-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="be399-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be399-118">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="be399-118">EntityExtractionResult</span></span>](entityextractionresult.md) <br/> |<span data-ttu-id="be399-119">指定项的**EntityExtractionResult**属性。</span><span class="sxs-lookup"><span data-stu-id="be399-119">Specifies the **EntityExtractionResult** property of an item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be399-120">备注</span><span class="sxs-lookup"><span data-stu-id="be399-120">Remarks</span></span>

<span data-ttu-id="be399-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="be399-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="be399-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="be399-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be399-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="be399-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be399-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="be399-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be399-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="be399-125">Schema Name</span></span>  <br/> |<span data-ttu-id="be399-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="be399-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="be399-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="be399-127">Validation File</span></span>  <br/> |<span data-ttu-id="be399-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="be399-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="be399-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="be399-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="be399-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="be399-130">See also</span></span>

- [<span data-ttu-id="be399-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="be399-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

