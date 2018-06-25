---
title: ImAddresses2
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 328f29b9-3a9c-4d9a-a85f-5ffff84e266a
description: ImAddresses2 元素指定的即时消息地址数组和为相关联的角色其源归属的标识符。
ms.openlocfilehash: f61084f22eb9d38766c45e63dfbacc0882ccaaca
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825870"
---
# <a name="imaddresses2"></a><span data-ttu-id="d7b66-103">ImAddresses2</span><span class="sxs-lookup"><span data-stu-id="d7b66-103">ImAddresses2</span></span>

<span data-ttu-id="d7b66-104">**ImAddresses2**元素指定的即时消息地址数组和为相关联的角色其源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="d7b66-104">The **ImAddresses2** element specifies an array of instant message addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<ImAddresses2>
    <StringAttributedValue/>
</ImAddresses2>
```

 <span data-ttu-id="d7b66-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="d7b66-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d7b66-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d7b66-106">Attributes and elements</span></span>

<span data-ttu-id="d7b66-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d7b66-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d7b66-108">属性</span><span class="sxs-lookup"><span data-stu-id="d7b66-108">Attributes</span></span>

<span data-ttu-id="d7b66-109">无。</span><span class="sxs-lookup"><span data-stu-id="d7b66-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d7b66-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d7b66-110">Child elements</span></span>

|<span data-ttu-id="d7b66-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d7b66-111">**Element**</span></span>|<span data-ttu-id="d7b66-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d7b66-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7b66-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="d7b66-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="d7b66-114">数组中的关联的个人元素的属性中指定的实例。</span><span class="sxs-lookup"><span data-stu-id="d7b66-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d7b66-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d7b66-115">Parent elements</span></span>

|<span data-ttu-id="d7b66-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d7b66-116">**Element**</span></span>|<span data-ttu-id="d7b66-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d7b66-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d7b66-118">角色</span><span class="sxs-lookup"><span data-stu-id="d7b66-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="d7b66-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="d7b66-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7b66-120">备注</span><span class="sxs-lookup"><span data-stu-id="d7b66-120">Remarks</span></span>

<span data-ttu-id="d7b66-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d7b66-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d7b66-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d7b66-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d7b66-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="d7b66-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7b66-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="d7b66-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d7b66-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="d7b66-125">Schema Name</span></span>  <br/> |<span data-ttu-id="d7b66-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="d7b66-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="d7b66-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="d7b66-127">Validation File</span></span>  <br/> |<span data-ttu-id="d7b66-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="d7b66-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d7b66-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="d7b66-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d7b66-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d7b66-130">See also</span></span>



- [<span data-ttu-id="d7b66-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d7b66-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

