---
title: ImAddresses3
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cab51a28-dfad-4c70-aafe-e239321b784e
description: ImAddresses3 元素指定即时消息地址的数组以及关联角色的源归属标识符。
ms.openlocfilehash: 2f02a57b1a113abe39a2852f8f8dbbd2b5b803ce
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460748"
---
# <a name="imaddresses3"></a><span data-ttu-id="f0ad6-103">ImAddresses3</span><span class="sxs-lookup"><span data-stu-id="f0ad6-103">ImAddresses3</span></span>

<span data-ttu-id="f0ad6-104">**ImAddresses3**元素指定即时消息地址的数组以及关联角色的源归属标识符。</span><span class="sxs-lookup"><span data-stu-id="f0ad6-104">The **ImAddresses3** element specifies an array of instant message addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<ImAddresses3>
    <StringAttributedValue/>
</ImAddresses3>
```

 <span data-ttu-id="f0ad6-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="f0ad6-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0ad6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f0ad6-106">Attributes and elements</span></span>

<span data-ttu-id="f0ad6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f0ad6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0ad6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f0ad6-108">Attributes</span></span>

<span data-ttu-id="f0ad6-109">无。</span><span class="sxs-lookup"><span data-stu-id="f0ad6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0ad6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f0ad6-110">Child elements</span></span>

|<span data-ttu-id="f0ad6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f0ad6-111">**Element**</span></span>|<span data-ttu-id="f0ad6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f0ad6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0ad6-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="f0ad6-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="f0ad6-114">指定与 persona 元素相关联的属性数组中的实例。</span><span class="sxs-lookup"><span data-stu-id="f0ad6-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f0ad6-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f0ad6-115">Parent elements</span></span>

|<span data-ttu-id="f0ad6-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f0ad6-116">**Element**</span></span>|<span data-ttu-id="f0ad6-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f0ad6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0ad6-118">角色</span><span class="sxs-lookup"><span data-stu-id="f0ad6-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="f0ad6-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="f0ad6-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0ad6-120">备注</span><span class="sxs-lookup"><span data-stu-id="f0ad6-120">Remarks</span></span>

<span data-ttu-id="f0ad6-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f0ad6-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f0ad6-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f0ad6-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0ad6-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f0ad6-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0ad6-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f0ad6-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f0ad6-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f0ad6-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f0ad6-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="f0ad6-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="f0ad6-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f0ad6-127">Validation File</span></span>  <br/> |<span data-ttu-id="f0ad6-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="f0ad6-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="f0ad6-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f0ad6-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="f0ad6-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f0ad6-130">See also</span></span>



- [<span data-ttu-id="f0ad6-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f0ad6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

