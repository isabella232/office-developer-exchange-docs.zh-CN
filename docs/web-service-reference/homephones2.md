---
title: HomePhones2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba9bb159-362d-48e0-889d-823cb46ecebf
description: HomePhones2 元素指定的 HomePhone2 值的数组和为相关联的角色其源归属的标识符。
ms.openlocfilehash: 205f2f71421a0dfc7d0057412529bcefdb6636d5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825842"
---
# <a name="homephones2"></a><span data-ttu-id="5f51d-103">HomePhones2</span><span class="sxs-lookup"><span data-stu-id="5f51d-103">HomePhones2</span></span>

<span data-ttu-id="5f51d-104">**HomePhones2**元素指定的**HomePhone2**值的数组和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="5f51d-104">The **HomePhones2** element specifies an array of **HomePhone2** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomePhones2>
    <PhoneNumberAttributedValue/>
</HomePhones2>
```

 <span data-ttu-id="5f51d-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="5f51d-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f51d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5f51d-106">Attributes and elements</span></span>

<span data-ttu-id="5f51d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5f51d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f51d-108">属性</span><span class="sxs-lookup"><span data-stu-id="5f51d-108">Attributes</span></span>

<span data-ttu-id="5f51d-109">无。</span><span class="sxs-lookup"><span data-stu-id="5f51d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f51d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5f51d-110">Child elements</span></span>

|<span data-ttu-id="5f51d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f51d-111">**Element**</span></span>|<span data-ttu-id="5f51d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f51d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f51d-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="5f51d-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="5f51d-114">包含单个属性化的电话号码的角色。</span><span class="sxs-lookup"><span data-stu-id="5f51d-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5f51d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="5f51d-115">Parent elements</span></span>

|<span data-ttu-id="5f51d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f51d-116">**Element**</span></span>|<span data-ttu-id="5f51d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f51d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f51d-118">角色</span><span class="sxs-lookup"><span data-stu-id="5f51d-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="5f51d-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="5f51d-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f51d-120">备注</span><span class="sxs-lookup"><span data-stu-id="5f51d-120">Remarks</span></span>

<span data-ttu-id="5f51d-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5f51d-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5f51d-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5f51d-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f51d-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="5f51d-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f51d-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="5f51d-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f51d-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="5f51d-125">Schema Name</span></span>  <br/> |<span data-ttu-id="5f51d-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="5f51d-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="5f51d-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="5f51d-127">Validation File</span></span>  <br/> |<span data-ttu-id="5f51d-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f51d-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f51d-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="5f51d-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="5f51d-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f51d-130">See also</span></span>



- [<span data-ttu-id="5f51d-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5f51d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

