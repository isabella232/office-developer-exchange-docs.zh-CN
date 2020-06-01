---
title: PersonaId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eec3a468-afd5-4d72-a61e-cd1964fb686c
description: PersonaId 元素指定关联角色的角色标识符。
ms.openlocfilehash: 3d7315097a14fb1eed5f378422cba80414601675
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457240"
---
# <a name="personaid"></a><span data-ttu-id="b681b-103">PersonaId</span><span class="sxs-lookup"><span data-stu-id="b681b-103">PersonaId</span></span>

<span data-ttu-id="b681b-104">**PersonaId**元素指定关联角色的角色标识符。</span><span class="sxs-lookup"><span data-stu-id="b681b-104">The **PersonaId** element specifies the persona identifier for the associated persona.</span></span> 
  
```XML
<PersonaId Id="" ChangeKey=""/>
```

 <span data-ttu-id="b681b-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="b681b-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b681b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b681b-106">Attributes and elements</span></span>

<span data-ttu-id="b681b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b681b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b681b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b681b-108">Attributes</span></span>

|<span data-ttu-id="b681b-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="b681b-109">**Attribute**</span></span>|<span data-ttu-id="b681b-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="b681b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b681b-111">Id</span><span class="sxs-lookup"><span data-stu-id="b681b-111">Id</span></span>  <br/> |<span data-ttu-id="b681b-112">**Id**属性的文本值是角色的标识符。</span><span class="sxs-lookup"><span data-stu-id="b681b-112">The text value of the **Id** attribute is the identifier of the persona.</span></span>  <br/> |
|<span data-ttu-id="b681b-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="b681b-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="b681b-114">**ChangeKey**属性的文本值是角色的更改键。</span><span class="sxs-lookup"><span data-stu-id="b681b-114">The text value of the **ChangeKey** attribute is the change key of the persona.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b681b-115">子元素</span><span class="sxs-lookup"><span data-stu-id="b681b-115">Child elements</span></span>

<span data-ttu-id="b681b-116">无。</span><span class="sxs-lookup"><span data-stu-id="b681b-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b681b-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b681b-117">Parent elements</span></span>

<span data-ttu-id="b681b-118">[GetPersona](getpersona.md)  | [Persona](persona.md)</span><span class="sxs-lookup"><span data-stu-id="b681b-118">[GetPersona](getpersona.md) | [Persona](persona.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b681b-119">备注</span><span class="sxs-lookup"><span data-stu-id="b681b-119">Remarks</span></span>

<span data-ttu-id="b681b-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b681b-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b681b-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b681b-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b681b-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b681b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b681b-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b681b-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b681b-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b681b-124">Schema name</span></span>  <br/> |<span data-ttu-id="b681b-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="b681b-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b681b-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b681b-126">Validation file</span></span>  <br/> |<span data-ttu-id="b681b-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b681b-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b681b-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b681b-128">Can be empty</span></span>  <br/> ||
   

