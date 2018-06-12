---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: SortBy 元素包含用于排序搜索结果的项目属性。
ms.openlocfilehash: 357958e393ba9331d23ee48661f21e2afe00cf01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827518"
---
# <a name="sortby"></a><span data-ttu-id="5dc7a-103">SortBy</span><span class="sxs-lookup"><span data-stu-id="5dc7a-103">SortBy</span></span>

<span data-ttu-id="5dc7a-104">**SortBy**元素包含用于排序搜索结果的项目属性。</span><span class="sxs-lookup"><span data-stu-id="5dc7a-104">The **SortBy** element contains an item property used for sorting the search result.</span></span> 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 <span data-ttu-id="5dc7a-105">**FieldOrderType**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-105">**FieldOrderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5dc7a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5dc7a-106">Attributes and elements</span></span>

<span data-ttu-id="5dc7a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5dc7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5dc7a-108">属性</span><span class="sxs-lookup"><span data-stu-id="5dc7a-108">Attributes</span></span>

|<span data-ttu-id="5dc7a-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-109">**Attribute**</span></span>|<span data-ttu-id="5dc7a-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="5dc7a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5dc7a-111">Order</span><span class="sxs-lookup"><span data-stu-id="5dc7a-111">Order</span></span>  <br/> |<span data-ttu-id="5dc7a-112">**Order**属性的文本值的排序次序。</span><span class="sxs-lookup"><span data-stu-id="5dc7a-112">The text value of the **Order** attribute is the sort order.</span></span> <span data-ttu-id="5dc7a-113">文本值为**升序**表示结果以升序排序。</span><span class="sxs-lookup"><span data-stu-id="5dc7a-113">A text value of **Ascending** indicates that the results are in ascending order.</span></span> <span data-ttu-id="5dc7a-114">文本值为**Descending**表示结果按降序顺序。</span><span class="sxs-lookup"><span data-stu-id="5dc7a-114">A text value of **Descending** indicates that the results are in descending order.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5dc7a-115">子元素</span><span class="sxs-lookup"><span data-stu-id="5dc7a-115">Child elements</span></span>

<span data-ttu-id="5dc7a-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span><span class="sxs-lookup"><span data-stu-id="5dc7a-116">[FieldURI](fielduri.md) | [IndexedFieldURI](indexedfielduri.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5dc7a-117">父元素</span><span class="sxs-lookup"><span data-stu-id="5dc7a-117">Parent elements</span></span>

[<span data-ttu-id="5dc7a-118">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="5dc7a-118">SearchMailboxes</span></span>](searchmailboxes.md)
  
## <a name="remarks"></a><span data-ttu-id="5dc7a-119">备注</span><span class="sxs-lookup"><span data-stu-id="5dc7a-119">Remarks</span></span>

<span data-ttu-id="5dc7a-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5dc7a-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5dc7a-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5dc7a-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5dc7a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="5dc7a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dc7a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="5dc7a-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5dc7a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="5dc7a-124">Schema name</span></span>  <br/> |<span data-ttu-id="5dc7a-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="5dc7a-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5dc7a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="5dc7a-126">Validation file</span></span>  <br/> |<span data-ttu-id="5dc7a-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5dc7a-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5dc7a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="5dc7a-128">Can be empty</span></span>  <br/> ||
   

