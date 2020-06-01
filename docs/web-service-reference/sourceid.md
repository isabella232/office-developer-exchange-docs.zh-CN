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
ms.openlocfilehash: a795f9fa2cc2084bee34c82b6df9567c79d430eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465756"
---
# <a name="sourceid"></a><span data-ttu-id="f692f-103">SourceId</span><span class="sxs-lookup"><span data-stu-id="f692f-103">SourceId</span></span>

<span data-ttu-id="f692f-104">**SourceId**元素指定角色中的属性化联系人的标识符。</span><span class="sxs-lookup"><span data-stu-id="f692f-104">The **SourceId** element specifies the identifier of the attributed contact in a persona.</span></span> 
  
```XML
<SourceId Id="" ChangeKey=""/>
```

 <span data-ttu-id="f692f-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="f692f-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f692f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f692f-106">Attributes and elements</span></span>

<span data-ttu-id="f692f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f692f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f692f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f692f-108">Attributes</span></span>

|<span data-ttu-id="f692f-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f692f-109">**Attribute**</span></span>|<span data-ttu-id="f692f-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f692f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f692f-111">Id</span><span class="sxs-lookup"><span data-stu-id="f692f-111">Id</span></span>  <br/> |<span data-ttu-id="f692f-112">**Id**属性的文本值是联系人的标识符。</span><span class="sxs-lookup"><span data-stu-id="f692f-112">The text value of the **Id** attribute is the identifier of the contact.</span></span>  <br/> |
|<span data-ttu-id="f692f-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="f692f-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="f692f-114">**ChangeKey**属性的文本值是联系人的更改键。</span><span class="sxs-lookup"><span data-stu-id="f692f-114">The text value of the **ChangeKey** attribute is the change key of the contact.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f692f-115">子元素</span><span class="sxs-lookup"><span data-stu-id="f692f-115">Child elements</span></span>

<span data-ttu-id="f692f-116">无。</span><span class="sxs-lookup"><span data-stu-id="f692f-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f692f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f692f-117">Parent elements</span></span>

[<span data-ttu-id="f692f-118">归属（PersonaAttributionType）</span><span class="sxs-lookup"><span data-stu-id="f692f-118">Attribution (PersonaAttributionType)</span></span>](attribution-personaattributiontype.md)
  
## <a name="remarks"></a><span data-ttu-id="f692f-119">备注</span><span class="sxs-lookup"><span data-stu-id="f692f-119">Remarks</span></span>

<span data-ttu-id="f692f-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f692f-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f692f-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f692f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f692f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="f692f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f692f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="f692f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f692f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="f692f-124">Schema name</span></span>  <br/> |<span data-ttu-id="f692f-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="f692f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f692f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="f692f-126">Validation file</span></span>  <br/> |<span data-ttu-id="f692f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f692f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f692f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="f692f-128">Can be empty</span></span>  <br/> ||
   

