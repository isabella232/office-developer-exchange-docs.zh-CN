---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: EmailAddressAttributedValue 元素指定实例及其关联的归属和数组的电子邮件地址。
ms.openlocfilehash: 3bcbb5c0a2bc9a2dc24516b5fc62e6e3363a360b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754059"
---
# <a name="emailaddressattributedvalue"></a><span data-ttu-id="826f9-103">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="826f9-103">EmailAddressAttributedValue</span></span>

<span data-ttu-id="826f9-104">**EmailAddressAttributedValue**元素指定实例及其关联的归属和数组的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="826f9-104">The **EmailAddressAttributedValue** element specifies an instance of an array of email addresses and their associated attributions.</span></span> 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 <span data-ttu-id="826f9-105">**EmailAddressAttributedValueType**</span><span class="sxs-lookup"><span data-stu-id="826f9-105">**EmailAddressAttributedValueType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="826f9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="826f9-106">Attributes and elements</span></span>

<span data-ttu-id="826f9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="826f9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="826f9-108">属性</span><span class="sxs-lookup"><span data-stu-id="826f9-108">Attributes</span></span>

<span data-ttu-id="826f9-109">无。</span><span class="sxs-lookup"><span data-stu-id="826f9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="826f9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="826f9-110">Child elements</span></span>

|<span data-ttu-id="826f9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="826f9-111">**Element**</span></span>|<span data-ttu-id="826f9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="826f9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="826f9-113">值 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="826f9-113">Value (EmailAddressType)</span></span>](value-emailaddresstype.md) <br/> |<span data-ttu-id="826f9-114">指定与归属数组关联的**电子邮件地址**的值。</span><span class="sxs-lookup"><span data-stu-id="826f9-114">Specifies the value of an **EmailAddress** associated with an attributions array.</span></span>  <br/> |
|[<span data-ttu-id="826f9-115">归属 (ArrayOfValueAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="826f9-115">Attributions (ArrayOfValueAttributionsType)</span></span>](attributions-arrayofvalueattributionstype.md) <br/> |<span data-ttu-id="826f9-116">指定其关联的**值**元素的归属的数组。</span><span class="sxs-lookup"><span data-stu-id="826f9-116">Specifies an array of attributions for its associated **Value** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="826f9-117">父元素</span><span class="sxs-lookup"><span data-stu-id="826f9-117">Parent elements</span></span>

|<span data-ttu-id="826f9-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="826f9-118">**Element**</span></span>|<span data-ttu-id="826f9-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="826f9-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="826f9-120">Emails1</span><span class="sxs-lookup"><span data-stu-id="826f9-120">Emails1</span></span>](emails1.md) <br/> |<span data-ttu-id="826f9-121">指定的电子邮件值的数组和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="826f9-121">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="826f9-122">Emails2</span><span class="sxs-lookup"><span data-stu-id="826f9-122">Emails2</span></span>](emails2.md) <br/> |<span data-ttu-id="826f9-123">指定的电子邮件值的数组和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="826f9-123">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
|[<span data-ttu-id="826f9-124">Emails3</span><span class="sxs-lookup"><span data-stu-id="826f9-124">Emails3</span></span>](emails3.md) <br/> |<span data-ttu-id="826f9-125">指定的电子邮件值的数组和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="826f9-125">Specifies an array of email values and the identifiers of their source attributions for the associated persona.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="826f9-126">备注</span><span class="sxs-lookup"><span data-stu-id="826f9-126">Remarks</span></span>

<span data-ttu-id="826f9-127">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="826f9-127">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="826f9-128">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="826f9-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="826f9-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="826f9-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="826f9-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="826f9-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="826f9-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="826f9-131">Schema Name</span></span>  <br/> |<span data-ttu-id="826f9-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="826f9-132">Type schema</span></span>  <br/> |
|<span data-ttu-id="826f9-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="826f9-133">Validation File</span></span>  <br/> |<span data-ttu-id="826f9-134">types.xsd</span><span class="sxs-lookup"><span data-stu-id="826f9-134">types.xsd</span></span>  <br/> |
|<span data-ttu-id="826f9-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="826f9-135">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="826f9-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="826f9-136">See also</span></span>



- [<span data-ttu-id="826f9-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="826f9-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

