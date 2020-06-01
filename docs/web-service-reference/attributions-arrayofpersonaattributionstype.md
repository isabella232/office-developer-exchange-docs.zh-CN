---
title: 归属（ArrayOfPersonaAttributionsType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61d843c-bca5-4c88-9667-fd03d2a963a1
description: 归属元素为聚合到关联角色中的一个或多个联系人或 Active Directory 收件人指定归属信息的数组。
ms.openlocfilehash: a9883e06a8adbd5c9d3bc7e1edd28c62418df653
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460321"
---
# <a name="attributions-arrayofpersonaattributionstype"></a><span data-ttu-id="9765f-103">归属（ArrayOfPersonaAttributionsType）</span><span class="sxs-lookup"><span data-stu-id="9765f-103">Attributions (ArrayOfPersonaAttributionsType)</span></span>

<span data-ttu-id="9765f-104">**归属**元素为聚合到关联角色中的一个或多个联系人或 Active Directory 收件人指定归属信息的数组。</span><span class="sxs-lookup"><span data-stu-id="9765f-104">The **Attributions** element specifies an array of attribution information for one or more of the contacts or Active Directory recipients aggregated into the associated persona.</span></span> 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 <span data-ttu-id="9765f-105">**ArrayOfPersonaAttributionsType**</span><span class="sxs-lookup"><span data-stu-id="9765f-105">**ArrayOfPersonaAttributionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9765f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9765f-106">Attributes and elements</span></span>

<span data-ttu-id="9765f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9765f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9765f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9765f-108">Attributes</span></span>

<span data-ttu-id="9765f-109">无。</span><span class="sxs-lookup"><span data-stu-id="9765f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9765f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9765f-110">Child elements</span></span>

|<span data-ttu-id="9765f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9765f-111">**Element**</span></span>|<span data-ttu-id="9765f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9765f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9765f-113">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="9765f-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="9765f-114">指定**PersonaType**元素的属性数组中的实例。</span><span class="sxs-lookup"><span data-stu-id="9765f-114">Specifies an instance in an array of attributes for a **PersonaType** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9765f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9765f-115">Parent elements</span></span>

|<span data-ttu-id="9765f-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9765f-116">**Element**</span></span>|<span data-ttu-id="9765f-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9765f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9765f-118">角色</span><span class="sxs-lookup"><span data-stu-id="9765f-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="9765f-119">指定由**GetPersona**请求返回的一组角色数据。</span><span class="sxs-lookup"><span data-stu-id="9765f-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9765f-120">备注</span><span class="sxs-lookup"><span data-stu-id="9765f-120">Remarks</span></span>

<span data-ttu-id="9765f-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9765f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9765f-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9765f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9765f-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9765f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9765f-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9765f-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9765f-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9765f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="9765f-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="9765f-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="9765f-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9765f-127">Validation File</span></span>  <br/> |<span data-ttu-id="9765f-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="9765f-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9765f-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9765f-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9765f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9765f-130">See also</span></span>

- [<span data-ttu-id="9765f-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9765f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

