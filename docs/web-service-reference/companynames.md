---
title: CompanyNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 615fa52d-86ff-4630-b188-5fdb9391eee2
description: CompanyNames 元素包含公司名称的数组以及关联角色的源归属的标识符。
ms.openlocfilehash: 25daa43873fe00837004217e3f814a7201638450
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463256"
---
# <a name="companynames"></a><span data-ttu-id="23d2b-103">CompanyNames</span><span class="sxs-lookup"><span data-stu-id="23d2b-103">CompanyNames</span></span>

<span data-ttu-id="23d2b-104">**CompanyNames**元素包含公司名称的数组以及关联角色的源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="23d2b-104">The **CompanyNames** element contains an array of company names and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<CompanyNames>
    <StringAttributedValue></StringAttributedValue>
</CompanyNames>
```

 <span data-ttu-id="23d2b-105">**ArrayOfStringAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="23d2b-105">**ArrayOfStringAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23d2b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="23d2b-106">Attributes and elements</span></span>

<span data-ttu-id="23d2b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="23d2b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23d2b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="23d2b-108">Attributes</span></span>

<span data-ttu-id="23d2b-109">无。</span><span class="sxs-lookup"><span data-stu-id="23d2b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23d2b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="23d2b-110">Child elements</span></span>

|<span data-ttu-id="23d2b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="23d2b-111">**Element**</span></span>|<span data-ttu-id="23d2b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="23d2b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23d2b-113">StringAttributedValue</span><span class="sxs-lookup"><span data-stu-id="23d2b-113">StringAttributedValue</span></span>](stringattributedvalue.md) <br/> |<span data-ttu-id="23d2b-114">指定与 persona 元素相关联的属性数组中的实例。</span><span class="sxs-lookup"><span data-stu-id="23d2b-114">Specifies an instance in an array of attributes associated with a persona element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23d2b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="23d2b-115">Parent elements</span></span>

|<span data-ttu-id="23d2b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="23d2b-116">**Element**</span></span>|<span data-ttu-id="23d2b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="23d2b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23d2b-118">角色</span><span class="sxs-lookup"><span data-stu-id="23d2b-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="23d2b-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="23d2b-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23d2b-120">备注</span><span class="sxs-lookup"><span data-stu-id="23d2b-120">Remarks</span></span>

<span data-ttu-id="23d2b-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="23d2b-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="23d2b-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="23d2b-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23d2b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="23d2b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23d2b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="23d2b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23d2b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="23d2b-125">Schema Name</span></span>  <br/> |<span data-ttu-id="23d2b-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="23d2b-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="23d2b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="23d2b-127">Validation File</span></span>  <br/> |<span data-ttu-id="23d2b-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="23d2b-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="23d2b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="23d2b-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="23d2b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="23d2b-130">See also</span></span>



- [<span data-ttu-id="23d2b-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="23d2b-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

