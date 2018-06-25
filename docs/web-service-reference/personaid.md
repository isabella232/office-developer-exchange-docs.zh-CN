---
title: PersonaId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eec3a468-afd5-4d72-a61e-cd1964fb686c
description: PersonaId 元素指定关联的角色的角色标识符。
ms.openlocfilehash: 77668a1b32a97eef08b3316c7d4d7c8e6494c7bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826738"
---
# <a name="personaid"></a><span data-ttu-id="ded70-103">PersonaId</span><span class="sxs-lookup"><span data-stu-id="ded70-103">PersonaId</span></span>

<span data-ttu-id="ded70-104">**PersonaId**元素指定关联的角色的角色标识符。</span><span class="sxs-lookup"><span data-stu-id="ded70-104">The **PersonaId** element specifies the persona identifier for the associated persona.</span></span> 
  
```XML
<PersonaId Id="" ChangeKey=""/>
```

 <span data-ttu-id="ded70-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="ded70-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ded70-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ded70-106">Attributes and elements</span></span>

<span data-ttu-id="ded70-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ded70-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ded70-108">属性</span><span class="sxs-lookup"><span data-stu-id="ded70-108">Attributes</span></span>

|<span data-ttu-id="ded70-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="ded70-109">**Attribute**</span></span>|<span data-ttu-id="ded70-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="ded70-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ded70-111">Id</span><span class="sxs-lookup"><span data-stu-id="ded70-111">Id</span></span>  <br/> |<span data-ttu-id="ded70-112">**Id**属性的文本值是角色的标识符。</span><span class="sxs-lookup"><span data-stu-id="ded70-112">The text value of the **Id** attribute is the identifier of the persona.</span></span>  <br/> |
|<span data-ttu-id="ded70-113">更改密钥</span><span class="sxs-lookup"><span data-stu-id="ded70-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="ded70-114">**更改密钥**属性的文本值是角色的更改键。</span><span class="sxs-lookup"><span data-stu-id="ded70-114">The text value of the **ChangeKey** attribute is the change key of the persona.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ded70-115">子元素</span><span class="sxs-lookup"><span data-stu-id="ded70-115">Child elements</span></span>

<span data-ttu-id="ded70-116">无。</span><span class="sxs-lookup"><span data-stu-id="ded70-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ded70-117">父元素</span><span class="sxs-lookup"><span data-stu-id="ded70-117">Parent elements</span></span>

<span data-ttu-id="ded70-118">[GetPersona](getpersona.md) | [角色](persona.md)</span><span class="sxs-lookup"><span data-stu-id="ded70-118">[GetPersona](getpersona.md) | [Persona](persona.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ded70-119">备注</span><span class="sxs-lookup"><span data-stu-id="ded70-119">Remarks</span></span>

<span data-ttu-id="ded70-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ded70-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ded70-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ded70-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ded70-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="ded70-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ded70-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="ded70-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ded70-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="ded70-124">Schema name</span></span>  <br/> |<span data-ttu-id="ded70-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="ded70-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ded70-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="ded70-126">Validation file</span></span>  <br/> |<span data-ttu-id="ded70-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ded70-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ded70-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="ded70-128">Can be empty</span></span>  <br/> ||
   

