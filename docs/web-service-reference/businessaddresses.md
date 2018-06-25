---
title: BusinessAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 828f8f62-7abf-44d4-8d58-f706d595a812
description: BusinessAddresses 元素指定的业务地址数组和为相关联的角色其源归属的标识符。
ms.openlocfilehash: bc7ad948572c24f913ae02abb9e8fc5a7b1e0b0d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753365"
---
# <a name="businessaddresses"></a><span data-ttu-id="c23f6-103">BusinessAddresses</span><span class="sxs-lookup"><span data-stu-id="c23f6-103">BusinessAddresses</span></span>

<span data-ttu-id="c23f6-104">**BusinessAddresses**元素指定的业务地址数组和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="c23f6-104">The **BusinessAddresses** element specifies an array of business addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<BusinessAddresses>
    <PostalAddressAttributedValue></PostalAddressAttributedValue>
</BusinessAddresses
```

 <span data-ttu-id="c23f6-105">**ArrayOfPostalAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="c23f6-105">**ArrayOfPostalAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c23f6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c23f6-106">Attributes and elements</span></span>

<span data-ttu-id="c23f6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c23f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c23f6-108">属性</span><span class="sxs-lookup"><span data-stu-id="c23f6-108">Attributes</span></span>

<span data-ttu-id="c23f6-109">无。</span><span class="sxs-lookup"><span data-stu-id="c23f6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c23f6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c23f6-110">Child elements</span></span>

|<span data-ttu-id="c23f6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c23f6-111">**Element**</span></span>|<span data-ttu-id="c23f6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c23f6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c23f6-113">PostalAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="c23f6-113">PostalAddressAttributedValue</span></span>](postaladdressattributedvalue.md) <br/> |<span data-ttu-id="c23f6-114">指定的邮政地址和其关联的归属声明数组的实例。</span><span class="sxs-lookup"><span data-stu-id="c23f6-114">Specifies an instance of an array of postal addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c23f6-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c23f6-115">Parent elements</span></span>

|<span data-ttu-id="c23f6-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="c23f6-116">**Element**</span></span>|<span data-ttu-id="c23f6-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c23f6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c23f6-118">角色</span><span class="sxs-lookup"><span data-stu-id="c23f6-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="c23f6-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="c23f6-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c23f6-120">备注</span><span class="sxs-lookup"><span data-stu-id="c23f6-120">Remarks</span></span>

<span data-ttu-id="c23f6-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c23f6-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c23f6-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c23f6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c23f6-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="c23f6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c23f6-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="c23f6-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c23f6-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="c23f6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="c23f6-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="c23f6-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="c23f6-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="c23f6-127">Validation File</span></span>  <br/> |<span data-ttu-id="c23f6-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="c23f6-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="c23f6-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="c23f6-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="c23f6-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c23f6-130">See also</span></span>



- [<span data-ttu-id="c23f6-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c23f6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

