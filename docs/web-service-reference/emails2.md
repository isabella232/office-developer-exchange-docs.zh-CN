---
title: Emails2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6ad95936-f61b-431a-9d86-df160b5d4b2d
description: Emails2 元素包含 EmailAddressAttributedValue 值的数组以及其源归属的标识符，用于关联的角色。
ms.openlocfilehash: b9445dfdc556ade1ad96d6e56c35ec1e56627e8c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463410"
---
# <a name="emails2"></a><span data-ttu-id="12004-103">Emails2</span><span class="sxs-lookup"><span data-stu-id="12004-103">Emails2</span></span>

<span data-ttu-id="12004-104">**Emails2**元素包含**EmailAddressAttributedValue**值的数组以及其源归属的标识符，用于关联的角色。</span><span class="sxs-lookup"><span data-stu-id="12004-104">The **Emails2** element contains an array of **EmailAddressAttributedValue** values and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<Emails2>
    <EmailAddressAttributedValue></EmailAddressAttributedValue>
</Emails2>
```

 <span data-ttu-id="12004-105">**ArrayOfEmailAddressAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="12004-105">**ArrayOfEmailAddressAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="12004-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="12004-106">Attributes and elements</span></span>

<span data-ttu-id="12004-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="12004-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12004-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="12004-108">Attributes</span></span>

<span data-ttu-id="12004-109">无。</span><span class="sxs-lookup"><span data-stu-id="12004-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="12004-110">子元素</span><span class="sxs-lookup"><span data-stu-id="12004-110">Child elements</span></span>

|<span data-ttu-id="12004-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="12004-111">**Element**</span></span>|<span data-ttu-id="12004-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="12004-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12004-113">EmailAddressAttributedValue</span><span class="sxs-lookup"><span data-stu-id="12004-113">EmailAddressAttributedValue</span></span>](emailaddressattributedvalue.md) <br/> |<span data-ttu-id="12004-114">指定电子邮件地址数组的实例及其关联的归属。</span><span class="sxs-lookup"><span data-stu-id="12004-114">Specifies an instance of an array of email addresses and their associated attributions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12004-115">父元素</span><span class="sxs-lookup"><span data-stu-id="12004-115">Parent elements</span></span>

|<span data-ttu-id="12004-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="12004-116">**Element**</span></span>|<span data-ttu-id="12004-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="12004-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12004-118">角色</span><span class="sxs-lookup"><span data-stu-id="12004-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="12004-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="12004-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12004-120">备注</span><span class="sxs-lookup"><span data-stu-id="12004-120">Remarks</span></span>

<span data-ttu-id="12004-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="12004-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="12004-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="12004-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12004-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="12004-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12004-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="12004-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="12004-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="12004-125">Schema Name</span></span>  <br/> |<span data-ttu-id="12004-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="12004-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="12004-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="12004-127">Validation File</span></span>  <br/> |<span data-ttu-id="12004-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="12004-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="12004-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="12004-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="12004-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="12004-130">See also</span></span>



- [<span data-ttu-id="12004-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="12004-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

