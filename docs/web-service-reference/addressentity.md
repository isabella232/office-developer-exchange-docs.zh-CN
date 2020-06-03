---
title: AddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ead22eab-f1e7-48b4-a165-db0e49fe86a8
description: AddressEntity 元素指定单个地址实体。
ms.openlocfilehash: c597557fe02a9c0ff7ed3c9862e1662cfbae596a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466904"
---
# <a name="addressentity"></a><span data-ttu-id="fba2f-103">AddressEntity</span><span class="sxs-lookup"><span data-stu-id="fba2f-103">AddressEntity</span></span>

<span data-ttu-id="fba2f-104">**AddressEntity**元素指定单个地址实体。</span><span class="sxs-lookup"><span data-stu-id="fba2f-104">The **AddressEntity** element specifies a single address entity.</span></span> 
  
```XML
<AddressEntity>
    <Address></Address>
    <Position></Position>
</AddressEntity>
```

 <span data-ttu-id="fba2f-105">**AddressEntityType**</span><span class="sxs-lookup"><span data-stu-id="fba2f-105">**AddressEntityType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fba2f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fba2f-106">Attributes and elements</span></span>

<span data-ttu-id="fba2f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fba2f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fba2f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fba2f-108">Attributes</span></span>

<span data-ttu-id="fba2f-109">无。</span><span class="sxs-lookup"><span data-stu-id="fba2f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fba2f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fba2f-110">Child elements</span></span>

|<span data-ttu-id="fba2f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fba2f-111">**Element**</span></span>|<span data-ttu-id="fba2f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fba2f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fba2f-113">Address （string）</span><span class="sxs-lookup"><span data-stu-id="fba2f-113">Address (string)</span></span>](address-string.md) <br/> |<span data-ttu-id="fba2f-114">指定地址。</span><span class="sxs-lookup"><span data-stu-id="fba2f-114">Specifies an address.</span></span>  <br/> |
|[<span data-ttu-id="fba2f-115">Position</span><span class="sxs-lookup"><span data-stu-id="fba2f-115">Position</span></span>](position.md) <br/> |<span data-ttu-id="fba2f-116">指定电子邮件中的位置。</span><span class="sxs-lookup"><span data-stu-id="fba2f-116">Specifies the position in an email message.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fba2f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="fba2f-117">Parent elements</span></span>

|<span data-ttu-id="fba2f-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="fba2f-118">**Element**</span></span>|<span data-ttu-id="fba2f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="fba2f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fba2f-120">地址（ArrayOfAddressEntitiesType）</span><span class="sxs-lookup"><span data-stu-id="fba2f-120">Addresses (ArrayOfAddressEntitiesType)</span></span>](addresses-arrayofaddressentitiestype.md) <br/> |<span data-ttu-id="fba2f-121">指定**AddressEntity**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="fba2f-121">Specifies an array of **AddressEntity** elements.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fba2f-122">文本值</span><span class="sxs-lookup"><span data-stu-id="fba2f-122">Text value</span></span>

<span data-ttu-id="fba2f-123">无。</span><span class="sxs-lookup"><span data-stu-id="fba2f-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fba2f-124">说明</span><span class="sxs-lookup"><span data-stu-id="fba2f-124">Remarks</span></span>

<span data-ttu-id="fba2f-125">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fba2f-125">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fba2f-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fba2f-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fba2f-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="fba2f-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fba2f-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="fba2f-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fba2f-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="fba2f-129">Schema Name</span></span>  <br/> |<span data-ttu-id="fba2f-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="fba2f-130">Type schema</span></span>  <br/> |
|<span data-ttu-id="fba2f-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="fba2f-131">Validation File</span></span>  <br/> |<span data-ttu-id="fba2f-132">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="fba2f-132">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fba2f-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="fba2f-133">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fba2f-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fba2f-134">See also</span></span>

- [<span data-ttu-id="fba2f-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fba2f-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

