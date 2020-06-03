---
title: ParentId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bb7aaa46-3a04-4197-aebb-8881ff10603f
description: ParentId 元素指定搜索预览中的父项的标识符。
ms.openlocfilehash: e09b5f9e463c7ecdfc595c87a84584f69cab3f2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529019"
---
# <a name="parentid"></a><span data-ttu-id="9c918-103">ParentId</span><span class="sxs-lookup"><span data-stu-id="9c918-103">ParentId</span></span>

<span data-ttu-id="9c918-104">**ParentId**元素指定搜索预览中的父项的标识符。</span><span class="sxs-lookup"><span data-stu-id="9c918-104">The **ParentId** element specifies the identifier of the parent item in a search preview.</span></span> 
  
```XML
<ParentId Id="" ChangeKey=""/>
```

<span data-ttu-id="9c918-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="9c918-105">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="9c918-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9c918-106">Attributes and elements</span></span>

<span data-ttu-id="9c918-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9c918-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c918-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9c918-108">Attributes</span></span>

|<span data-ttu-id="9c918-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="9c918-109">**Attribute**</span></span>|<span data-ttu-id="9c918-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c918-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c918-111">Id</span><span class="sxs-lookup"><span data-stu-id="9c918-111">Id</span></span>  <br/> |<span data-ttu-id="9c918-112">**Id**属性的文本值是父项的标识符。</span><span class="sxs-lookup"><span data-stu-id="9c918-112">The text value of the **Id** attribute is the identifier of the parent item.</span></span>  <br/> |
|<span data-ttu-id="9c918-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="9c918-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="9c918-114">**ChangeKey**属性的文本值是父项的更改键。</span><span class="sxs-lookup"><span data-stu-id="9c918-114">The text value of the **ChangeKey** attribute is the change key of the parent item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9c918-115">子元素</span><span class="sxs-lookup"><span data-stu-id="9c918-115">Child elements</span></span>

<span data-ttu-id="9c918-116">无。</span><span class="sxs-lookup"><span data-stu-id="9c918-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9c918-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9c918-117">Parent elements</span></span>

[<span data-ttu-id="9c918-118">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="9c918-118">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="9c918-119">备注</span><span class="sxs-lookup"><span data-stu-id="9c918-119">Remarks</span></span>

<span data-ttu-id="9c918-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9c918-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9c918-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9c918-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c918-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="9c918-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c918-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="9c918-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9c918-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="9c918-124">Schema name</span></span>  <br/> |<span data-ttu-id="9c918-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="9c918-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="9c918-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="9c918-126">Validation file</span></span>  <br/> |<span data-ttu-id="9c918-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9c918-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9c918-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="9c918-128">Can be empty</span></span>  <br/> |<span data-ttu-id="9c918-129">True</span><span class="sxs-lookup"><span data-stu-id="9c918-129">true</span></span>  <br/> |
   

