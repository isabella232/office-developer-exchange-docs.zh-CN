---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: SortBy 元素包含用于对搜索结果进行排序的项属性。
ms.openlocfilehash: cf2b1e633bc66e526028078833afade363e4c5e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468395"
---
# <a name="sortby"></a><span data-ttu-id="37a6d-103">SortBy</span><span class="sxs-lookup"><span data-stu-id="37a6d-103">SortBy</span></span>

<span data-ttu-id="37a6d-104">**SortBy**元素包含用于对搜索结果进行排序的项属性。</span><span class="sxs-lookup"><span data-stu-id="37a6d-104">The **SortBy** element contains an item property used for sorting the search result.</span></span> 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 <span data-ttu-id="37a6d-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="37a6d-105">**FieldOrderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="37a6d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="37a6d-106">Attributes and elements</span></span>

<span data-ttu-id="37a6d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="37a6d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="37a6d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="37a6d-108">Attributes</span></span>

|<span data-ttu-id="37a6d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="37a6d-109">**Attribute**</span></span>|<span data-ttu-id="37a6d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="37a6d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37a6d-111">Order</span><span class="sxs-lookup"><span data-stu-id="37a6d-111">Order</span></span>  <br/> |<span data-ttu-id="37a6d-112">**Order**属性的文本值为排序顺序。</span><span class="sxs-lookup"><span data-stu-id="37a6d-112">The text value of the **Order** attribute is the sort order.</span></span> <span data-ttu-id="37a6d-113">文本值为**升序**表示结果按升序排列。</span><span class="sxs-lookup"><span data-stu-id="37a6d-113">A text value of **Ascending** indicates that the results are in ascending order.</span></span> <span data-ttu-id="37a6d-114">"**降序**" 文本表示结果按降序排列。</span><span class="sxs-lookup"><span data-stu-id="37a6d-114">A text value of **Descending** indicates that the results are in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="37a6d-115">子元素</span><span class="sxs-lookup"><span data-stu-id="37a6d-115">Child elements</span></span>

<span data-ttu-id="37a6d-116">[FieldURI](fielduri.md)  | [IndexedFieldURI](indexedfielduri.md)</span><span class="sxs-lookup"><span data-stu-id="37a6d-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="37a6d-117">父元素</span><span class="sxs-lookup"><span data-stu-id="37a6d-117">Parent elements</span></span>

[<span data-ttu-id="37a6d-118">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="37a6d-118">SearchMailboxes</span></span>](searchmailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="37a6d-119">备注</span><span class="sxs-lookup"><span data-stu-id="37a6d-119">Remarks</span></span>

<span data-ttu-id="37a6d-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="37a6d-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="37a6d-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="37a6d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="37a6d-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="37a6d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="37a6d-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="37a6d-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="37a6d-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="37a6d-124">Schema name</span></span>  <br/> |<span data-ttu-id="37a6d-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="37a6d-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="37a6d-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="37a6d-126">Validation file</span></span>  <br/> |<span data-ttu-id="37a6d-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="37a6d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="37a6d-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="37a6d-128">Can be empty</span></span>  <br/> ||
   

