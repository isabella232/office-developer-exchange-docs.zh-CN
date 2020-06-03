---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: EmailAddressAttributedValue 元素指定电子邮件地址数组的实例及其关联的归属。
ms.openlocfilehash: 09fdd5921cef3d70a6da4b6d4d38f08834c5d482
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530689"
---
# <a name="emailaddressattributedvalue"></a><span data-ttu-id="d50f2-103">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d50f2-103">EmailAddressAttributedValue</span></span>

<span data-ttu-id="d50f2-104">**EmailAddressAttributedValue**元素指定电子邮件地址数组的实例及其关联的归属。</span><span class="sxs-lookup"><span data-stu-id="d50f2-104">The **EmailAddressAttributedValue** element specifies an instance of an array of email addresses and their associated attributions.</span></span> 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 <span data-ttu-id="d50f2-105">**EmailAddressAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="d50f2-105">**EmailAddressAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d50f2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d50f2-106">Attributes and elements</span></span>

<span data-ttu-id="d50f2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d50f2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d50f2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d50f2-108">Attributes</span></span>

<span data-ttu-id="d50f2-109">无。</span><span class="sxs-lookup"><span data-stu-id="d50f2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d50f2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d50f2-110">Child elements</span></span>

|<span data-ttu-id="d50f2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d50f2-111">**Element**</span></span>|<span data-ttu-id="d50f2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d50f2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d50f2-113">Value （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="d50f2-113">Value (EmailAddressType)</span></span>](value-emailaddresstype.md) <br/> |<span data-ttu-id="d50f2-114">指定与归属数组相关联的**EmailAddress**的值。</span><span class="sxs-lookup"><span data-stu-id="d50f2-114">Specifies the value of an **EmailAddress** associated with an attributions array.</span></span>  <br/> |
|[<span data-ttu-id="d50f2-115">归属（ArrayOfValueAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="d50f2-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="d50f2-116">为其关联的**Value**元素指定归属的数组。</span><span class="sxs-lookup"><span data-stu-id="d50f2-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d50f2-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d50f2-117">Parent elements</span></span>

|<span data-ttu-id="d50f2-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="d50f2-118">**Element**</span></span>|<span data-ttu-id="d50f2-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d50f2-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d50f2-120">Emails1</span><span class="sxs-lookup"><span data-stu-id="d50f2-120">Emails1</span></span>](emails1.md) <br/> |<span data-ttu-id="d50f2-121">为关联角色的电子邮件值和其源归属的标识符指定一个数组。</span><span class="sxs-lookup"><span data-stu-id="d50f2-121">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="d50f2-122">Emails2</span><span class="sxs-lookup"><span data-stu-id="d50f2-122">Emails2</span></span>](emails2.md) <br/> |<span data-ttu-id="d50f2-123">为关联角色的电子邮件值和其源归属的标识符指定一个数组。</span><span class="sxs-lookup"><span data-stu-id="d50f2-123">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="d50f2-124">Emails3</span><span class="sxs-lookup"><span data-stu-id="d50f2-124">Emails3</span></span>](emails3.md) <br/> |<span data-ttu-id="d50f2-125">为关联角色的电子邮件值和其源归属的标识符指定一个数组。</span><span class="sxs-lookup"><span data-stu-id="d50f2-125">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d50f2-126">备注</span><span class="sxs-lookup"><span data-stu-id="d50f2-126">Remarks</span></span>

<span data-ttu-id="d50f2-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d50f2-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d50f2-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d50f2-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d50f2-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="d50f2-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d50f2-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="d50f2-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d50f2-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="d50f2-131">Schema Name</span></span>  <br/> |<span data-ttu-id="d50f2-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="d50f2-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="d50f2-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="d50f2-133">Validation File</span></span>  <br/> |<span data-ttu-id="d50f2-134">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="d50f2-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d50f2-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="d50f2-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d50f2-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d50f2-136">See also</span></span>



- [<span data-ttu-id="d50f2-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d50f2-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

