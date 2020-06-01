---
title: ImAddresses (ArrayOfStringAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b95d0a8b-15a6-4711-b014-55698dbd679c
description: ImAddresses 元素指定即时消息地址的数组以及关联角色的源归属标识符。
ms.openlocfilehash: 6714af5d88e50047f48da2f10dbb33d2e2feb724
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460440"
---
# <a name="imaddresses-arrayofstringattributedvaluestype"></a><span data-ttu-id="de7e7-103">ImAddresses (ArrayOfStringAttributedValuesType)</span><span class="sxs-lookup"><span data-stu-id="de7e7-103">ImAddresses (ArrayOfStringAttributedValuesType)</span></span>

<span data-ttu-id="de7e7-104">**ImAddresses**元素指定即时消息地址的数组以及关联角色的源归属标识符。</span><span class="sxs-lookup"><span data-stu-id="de7e7-104">The **ImAddresses** element specifies an array of instant message addresses and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<ImAddresses>
    <StringAttributedValue/>
</ImAddresses>
```

 <span data-ttu-id="de7e7-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="de7e7-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de7e7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="de7e7-106">Attributes and elements</span></span>

<span data-ttu-id="de7e7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="de7e7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de7e7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="de7e7-108">Attributes</span></span>

<span data-ttu-id="de7e7-109">无。</span><span class="sxs-lookup"><span data-stu-id="de7e7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de7e7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="de7e7-110">Child elements</span></span>

|<span data-ttu-id="de7e7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="de7e7-111">**Element**</span></span>|<span data-ttu-id="de7e7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="de7e7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de7e7-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="de7e7-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="de7e7-114">指定与 persona 元素相关联的属性数组中的实例。</span><span class="sxs-lookup"><span data-stu-id="de7e7-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de7e7-115">父元素</span><span class="sxs-lookup"><span data-stu-id="de7e7-115">Parent elements</span></span>

|<span data-ttu-id="de7e7-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="de7e7-116">**Element**</span></span>|<span data-ttu-id="de7e7-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="de7e7-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de7e7-118">角色</span><span class="sxs-lookup"><span data-stu-id="de7e7-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="de7e7-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="de7e7-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de7e7-120">备注</span><span class="sxs-lookup"><span data-stu-id="de7e7-120">Remarks</span></span>

<span data-ttu-id="de7e7-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="de7e7-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="de7e7-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="de7e7-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de7e7-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="de7e7-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de7e7-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="de7e7-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de7e7-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="de7e7-125">Schema Name</span></span>  <br/> |<span data-ttu-id="de7e7-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="de7e7-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="de7e7-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="de7e7-127">Validation File</span></span>  <br/> |<span data-ttu-id="de7e7-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="de7e7-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="de7e7-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="de7e7-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="de7e7-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="de7e7-130">See also</span></span>



- [<span data-ttu-id="de7e7-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="de7e7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

