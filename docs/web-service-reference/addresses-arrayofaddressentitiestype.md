---
title: 地址 (ArrayOfAddressEntitiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c1f3fd3-1b78-46ee-8dd4-b2aff51e767e
description: 地址元素指定 AddressEntity 元素的数组。
ms.openlocfilehash: b6fbcc54a016e698bccbe075fd340c0c784f121a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753124"
---
# <a name="addresses-arrayofaddressentitiestype"></a><span data-ttu-id="15cea-103">地址 (ArrayOfAddressEntitiesType)</span><span class="sxs-lookup"><span data-stu-id="15cea-103">Addresses (ArrayOfAddressEntitiesType)</span></span>

<span data-ttu-id="15cea-104">**地址**元素指定**AddressEntity**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="15cea-104">The **Addresses** element specifies an array of **AddressEntity** elements.</span></span> 
  
```XML
<Addresses>
   <AddressEntity/>
</Addresses>
```

 <span data-ttu-id="15cea-105">**ArrayOfAddressEntitiesType**</span><span class="sxs-lookup"><span data-stu-id="15cea-105">**ArrayOfAddressEntitiesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15cea-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="15cea-106">Attributes and elements</span></span>

<span data-ttu-id="15cea-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15cea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15cea-108">属性</span><span class="sxs-lookup"><span data-stu-id="15cea-108">Attributes</span></span>

<span data-ttu-id="15cea-109">无。</span><span class="sxs-lookup"><span data-stu-id="15cea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15cea-110">子元素</span><span class="sxs-lookup"><span data-stu-id="15cea-110">Child elements</span></span>

|<span data-ttu-id="15cea-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="15cea-111">**Element**</span></span>|<span data-ttu-id="15cea-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="15cea-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15cea-113">AddressEntity</span><span class="sxs-lookup"><span data-stu-id="15cea-113">AddressEntity</span></span>](addressentity.md) <br/> |<span data-ttu-id="15cea-114">指定单个地址实体。</span><span class="sxs-lookup"><span data-stu-id="15cea-114">Specifies a single address entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="15cea-115">父元素</span><span class="sxs-lookup"><span data-stu-id="15cea-115">Parent elements</span></span>

|<span data-ttu-id="15cea-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="15cea-116">**Element**</span></span>|<span data-ttu-id="15cea-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="15cea-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="15cea-118">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="15cea-118">EntityExtractionResult</span></span>](entityextractionresult.md) <br/> |<span data-ttu-id="15cea-119">指定项目的**EntityExtractionResult**属性。</span><span class="sxs-lookup"><span data-stu-id="15cea-119">Specifies the **EntityExtractionResult** property of an item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15cea-120">备注</span><span class="sxs-lookup"><span data-stu-id="15cea-120">Remarks</span></span>

<span data-ttu-id="15cea-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="15cea-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="15cea-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="15cea-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15cea-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="15cea-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15cea-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="15cea-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="15cea-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="15cea-125">Schema Name</span></span>  <br/> |<span data-ttu-id="15cea-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="15cea-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="15cea-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="15cea-127">Validation File</span></span>  <br/> |<span data-ttu-id="15cea-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="15cea-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="15cea-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="15cea-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="15cea-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15cea-130">See also</span></span>

- [<span data-ttu-id="15cea-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="15cea-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

