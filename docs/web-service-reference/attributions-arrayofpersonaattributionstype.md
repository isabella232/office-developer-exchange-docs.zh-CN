---
title: 归属 (ArrayOfPersonaAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f61d843c-bca5-4c88-9667-fd03d2a963a1
description: 归属元素指定一个或多个联系人或聚合到相关联的角色的 Active Directory 收件人的归属信息的数组。
ms.openlocfilehash: 52fecb4e4381d5e9dbbaf7134fa18068ba15f6ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753290"
---
# <a name="attributions-arrayofpersonaattributionstype"></a><span data-ttu-id="2ac6c-103">归属 (ArrayOfPersonaAttributionsType)</span><span class="sxs-lookup"><span data-stu-id="2ac6c-103">Attributions (ArrayOfPersonaAttributionsType)</span></span>

<span data-ttu-id="2ac6c-104">**归属**元素指定一个或多个联系人或聚合到相关联的角色的 Active Directory 收件人的归属信息的数组。</span><span class="sxs-lookup"><span data-stu-id="2ac6c-104">The **Attributions** element specifies an array of attribution information for one or more of the contacts or Active Directory recipients aggregated into the associated persona.</span></span> 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attributions>
```

 <span data-ttu-id="2ac6c-105">**ArrayOfPersonaAttributionsType**</span><span class="sxs-lookup"><span data-stu-id="2ac6c-105">**ArrayOfPersonaAttributionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2ac6c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2ac6c-106">Attributes and elements</span></span>

<span data-ttu-id="2ac6c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2ac6c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2ac6c-108">属性</span><span class="sxs-lookup"><span data-stu-id="2ac6c-108">Attributes</span></span>

<span data-ttu-id="2ac6c-109">无。</span><span class="sxs-lookup"><span data-stu-id="2ac6c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2ac6c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2ac6c-110">Child elements</span></span>

|<span data-ttu-id="2ac6c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2ac6c-111">**Element**</span></span>|<span data-ttu-id="2ac6c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ac6c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ac6c-113">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="2ac6c-113">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md) <br/> |<span data-ttu-id="2ac6c-114">数组**PersonaType**元素的属性中指定的实例。</span><span class="sxs-lookup"><span data-stu-id="2ac6c-114">Specifies an instance in an array of attributes for a **PersonaType** element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2ac6c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2ac6c-115">Parent elements</span></span>

|<span data-ttu-id="2ac6c-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2ac6c-116">**Element**</span></span>|<span data-ttu-id="2ac6c-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2ac6c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ac6c-118">角色</span><span class="sxs-lookup"><span data-stu-id="2ac6c-118">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="2ac6c-119">指定一组个人**GetPersona**请求返回的数据。</span><span class="sxs-lookup"><span data-stu-id="2ac6c-119">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ac6c-120">备注</span><span class="sxs-lookup"><span data-stu-id="2ac6c-120">Remarks</span></span>

<span data-ttu-id="2ac6c-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2ac6c-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2ac6c-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2ac6c-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2ac6c-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="2ac6c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ac6c-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="2ac6c-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2ac6c-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="2ac6c-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2ac6c-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="2ac6c-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2ac6c-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="2ac6c-127">Validation File</span></span>  <br/> |<span data-ttu-id="2ac6c-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="2ac6c-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2ac6c-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="2ac6c-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2ac6c-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2ac6c-130">See also</span></span>

- [<span data-ttu-id="2ac6c-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2ac6c-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

