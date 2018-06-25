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
ms.openlocfilehash: ddc76320b1c482e3518a98fb63fc2296143d163c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826698"
---
# <a name="parentid"></a><span data-ttu-id="8b793-103">ParentId</span><span class="sxs-lookup"><span data-stu-id="8b793-103">ParentId</span></span>

<span data-ttu-id="8b793-104">**ParentId**元素指定搜索预览中的父项的标识符。</span><span class="sxs-lookup"><span data-stu-id="8b793-104">The **ParentId** element specifies the identifier of the parent item in a search preview.</span></span> 
  
```XML
<ParentId Id="" ChangeKey=""/>
```

<span data-ttu-id="8b793-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="8b793-105">**ItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8b793-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8b793-106">Attributes and elements</span></span>

<span data-ttu-id="8b793-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8b793-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b793-108">属性</span><span class="sxs-lookup"><span data-stu-id="8b793-108">Attributes</span></span>

|<span data-ttu-id="8b793-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="8b793-109">**Attribute**</span></span>|<span data-ttu-id="8b793-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="8b793-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8b793-111">Id</span><span class="sxs-lookup"><span data-stu-id="8b793-111">Id</span></span>  <br/> |<span data-ttu-id="8b793-112">**Id**属性的文本值是父项的标识符。</span><span class="sxs-lookup"><span data-stu-id="8b793-112">The text value of the **Id** attribute is the identifier of the parent item.</span></span>  <br/> |
|<span data-ttu-id="8b793-113">更改密钥</span><span class="sxs-lookup"><span data-stu-id="8b793-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="8b793-114">**更改密钥**属性的文本值是父项的更改键。</span><span class="sxs-lookup"><span data-stu-id="8b793-114">The text value of the **ChangeKey** attribute is the change key of the parent item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8b793-115">子元素</span><span class="sxs-lookup"><span data-stu-id="8b793-115">Child elements</span></span>

<span data-ttu-id="8b793-116">无。</span><span class="sxs-lookup"><span data-stu-id="8b793-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8b793-117">父元素</span><span class="sxs-lookup"><span data-stu-id="8b793-117">Parent elements</span></span>

[<span data-ttu-id="8b793-118">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="8b793-118">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="8b793-119">备注</span><span class="sxs-lookup"><span data-stu-id="8b793-119">Remarks</span></span>

<span data-ttu-id="8b793-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8b793-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8b793-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8b793-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8b793-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="8b793-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b793-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="8b793-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8b793-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="8b793-124">Schema name</span></span>  <br/> |<span data-ttu-id="8b793-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="8b793-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="8b793-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="8b793-126">Validation file</span></span>  <br/> |<span data-ttu-id="8b793-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8b793-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8b793-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="8b793-128">Can be empty</span></span>  <br/> |<span data-ttu-id="8b793-129">True</span><span class="sxs-lookup"><span data-stu-id="8b793-129">true</span></span>  <br/> |
   

