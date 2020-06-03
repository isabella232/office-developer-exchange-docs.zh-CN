---
title: BusinessAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 828f8f62-7abf-44d4-8d58-f706d595a812
description: BusinessAddresses 元素指定业务地址的数组以及关联角色的源归属的标识符。
ms.openlocfilehash: d314d0de679f8eabc51dc9ee3b2e9a57cd0b8da1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465924"
---
# <a name="businessaddresses"></a><span data-ttu-id="2d729-103">BusinessAddresses</span><span class="sxs-lookup"><span data-stu-id="2d729-103">BusinessAddresses</span></span>

<span data-ttu-id="2d729-104">**BusinessAddresses**元素指定业务地址的数组以及关联角色的源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="2d729-104">The **BusinessAddresses** element specifies an array of business addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessAddresses>
    <PostalAddressAttributedValue></PostalAddressAttributedValue>
</BusinessAddresses
```

 <span data-ttu-id="2d729-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="2d729-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d729-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d729-106">Attributes and elements</span></span>

<span data-ttu-id="2d729-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d729-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d729-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2d729-108">Attributes</span></span>

<span data-ttu-id="2d729-109">无。</span><span class="sxs-lookup"><span data-stu-id="2d729-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d729-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2d729-110">Child elements</span></span>

|<span data-ttu-id="2d729-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d729-111">**Element**</span></span>|<span data-ttu-id="2d729-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d729-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d729-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="2d729-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="2d729-114">指定邮政地址数组的实例及其关联的归属。</span><span class="sxs-lookup"><span data-stu-id="2d729-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2d729-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2d729-115">Parent elements</span></span>

|<span data-ttu-id="2d729-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2d729-116">**Element**</span></span>|<span data-ttu-id="2d729-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2d729-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2d729-118">角色</span><span class="sxs-lookup"><span data-stu-id="2d729-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="2d729-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="2d729-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d729-120">备注</span><span class="sxs-lookup"><span data-stu-id="2d729-120">Remarks</span></span>

<span data-ttu-id="2d729-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2d729-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2d729-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d729-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d729-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d729-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d729-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d729-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2d729-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d729-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2d729-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="2d729-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2d729-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d729-127">Validation File</span></span>  <br/> |<span data-ttu-id="2d729-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="2d729-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2d729-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d729-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2d729-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d729-130">See also</span></span>



- [<span data-ttu-id="2d729-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2d729-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

