---
title: HomeFaxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 459ddb1c-8cff-4125-b6fa-dc93c183dee8
description: HomeFaxes 元素指定 home fax 号码的数组以及关联角色的源归属的标识符。
ms.openlocfilehash: d49eb9e12547e4011e4ba403cb898c0fe6e9bf02
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460846"
---
# <a name="homefaxes"></a><span data-ttu-id="23d46-103">HomeFaxes</span><span class="sxs-lookup"><span data-stu-id="23d46-103">HomeFaxes</span></span>

<span data-ttu-id="23d46-104">**HomeFaxes**元素指定 home fax 号码的数组以及关联角色的源归属的标识符。</span><span class="sxs-lookup"><span data-stu-id="23d46-104">The **HomeFaxes** element specifies an array of home fax numbers and the identifiers of their source attributions for the associated persona.</span></span> 
  
```XML
<HomeFaxes>
    <PhoneNumberAttributedValue/>
</HomeFaxes>
```

 <span data-ttu-id="23d46-105">**ArrayOfPhoneNumberAttributedValuesType**</span><span class="sxs-lookup"><span data-stu-id="23d46-105">**ArrayOfPhoneNumberAttributedValuesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23d46-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="23d46-106">Attributes and elements</span></span>

<span data-ttu-id="23d46-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="23d46-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23d46-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="23d46-108">Attributes</span></span>

<span data-ttu-id="23d46-109">无。</span><span class="sxs-lookup"><span data-stu-id="23d46-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23d46-110">子元素</span><span class="sxs-lookup"><span data-stu-id="23d46-110">Child elements</span></span>

|<span data-ttu-id="23d46-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="23d46-111">**Element**</span></span>|<span data-ttu-id="23d46-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="23d46-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23d46-113">PhoneNumberAttributedValue</span><span class="sxs-lookup"><span data-stu-id="23d46-113">PhoneNumberAttributedValue</span></span>](phonenumberattributedvalue.md) <br/> |<span data-ttu-id="23d46-114">包含角色的单个属性电话号码。</span><span class="sxs-lookup"><span data-stu-id="23d46-114">Contains a single attributed phone number for a persona.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23d46-115">父元素</span><span class="sxs-lookup"><span data-stu-id="23d46-115">Parent elements</span></span>

|<span data-ttu-id="23d46-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="23d46-116">**Element**</span></span>|<span data-ttu-id="23d46-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="23d46-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23d46-118">角色</span><span class="sxs-lookup"><span data-stu-id="23d46-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="23d46-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="23d46-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23d46-120">备注</span><span class="sxs-lookup"><span data-stu-id="23d46-120">Remarks</span></span>

<span data-ttu-id="23d46-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="23d46-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="23d46-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="23d46-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23d46-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="23d46-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23d46-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="23d46-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23d46-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="23d46-125">Schema Name</span></span>  <br/> |<span data-ttu-id="23d46-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="23d46-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="23d46-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="23d46-127">Validation File</span></span>  <br/> |<span data-ttu-id="23d46-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="23d46-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="23d46-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="23d46-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="23d46-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="23d46-130">See also</span></span>



- [<span data-ttu-id="23d46-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="23d46-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

