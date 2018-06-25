---
title: SourceId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fccdedc0-83ed-4bb7-a1d2-623e70d1a7bf
description: SourceId 元素指定角色中的属性化联系人的标识符。
ms.openlocfilehash: b08c28f93318a01e45a0d9cb812fef01905694ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827521"
---
# <a name="sourceid"></a><span data-ttu-id="1d107-103">SourceId</span><span class="sxs-lookup"><span data-stu-id="1d107-103">SourceId</span></span>

<span data-ttu-id="1d107-104">**SourceId**元素指定角色中的属性化联系人的标识符。</span><span class="sxs-lookup"><span data-stu-id="1d107-104">The **SourceId** element specifies the identifier of the attributed contact in a persona.</span></span> 
  
```XML
<SourceId Id="" ChangeKey=""/>
```

 <span data-ttu-id="1d107-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="1d107-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d107-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1d107-106">Attributes and elements</span></span>

<span data-ttu-id="1d107-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d107-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d107-108">属性</span><span class="sxs-lookup"><span data-stu-id="1d107-108">Attributes</span></span>

|<span data-ttu-id="1d107-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="1d107-109">**Attribute**</span></span>|<span data-ttu-id="1d107-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1d107-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d107-111">Id</span><span class="sxs-lookup"><span data-stu-id="1d107-111">Id</span></span>  <br/> |<span data-ttu-id="1d107-112">**Id**属性的文本值是联系人的标识符。</span><span class="sxs-lookup"><span data-stu-id="1d107-112">The text value of the **Id** attribute is the identifier of the contact.</span></span>  <br/> |
|<span data-ttu-id="1d107-113">更改密钥</span><span class="sxs-lookup"><span data-stu-id="1d107-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="1d107-114">**更改密钥**属性的文本值是联系人的更改键。</span><span class="sxs-lookup"><span data-stu-id="1d107-114">The text value of the **ChangeKey** attribute is the change key of the contact.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d107-115">子元素</span><span class="sxs-lookup"><span data-stu-id="1d107-115">Child elements</span></span>

<span data-ttu-id="1d107-116">无。</span><span class="sxs-lookup"><span data-stu-id="1d107-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d107-117">父元素</span><span class="sxs-lookup"><span data-stu-id="1d107-117">Parent elements</span></span>

[<span data-ttu-id="1d107-118">归属 (PersonaAttributionType)</span><span class="sxs-lookup"><span data-stu-id="1d107-118">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
  
## <a name="remarks"></a><span data-ttu-id="1d107-119">备注</span><span class="sxs-lookup"><span data-stu-id="1d107-119">Remarks</span></span>

<span data-ttu-id="1d107-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1d107-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1d107-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1d107-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d107-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="1d107-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d107-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="1d107-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d107-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="1d107-124">Schema name</span></span>  <br/> |<span data-ttu-id="1d107-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="1d107-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d107-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="1d107-126">Validation file</span></span>  <br/> |<span data-ttu-id="1d107-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1d107-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d107-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="1d107-128">Can be empty</span></span>  <br/> ||
   

