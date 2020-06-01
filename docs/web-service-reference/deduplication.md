---
title: 项
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: 重复数据删除元素指示搜索结果是否应删除重复项。
ms.openlocfilehash: c39f980658aba7036cfabb3b51af5a41005f97b6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463711"
---
# <a name="deduplication"></a><span data-ttu-id="ef56a-103">项</span><span class="sxs-lookup"><span data-stu-id="ef56a-103">Deduplication</span></span>

<span data-ttu-id="ef56a-104">**重复数据删除**元素指示搜索结果是否应删除重复项。</span><span class="sxs-lookup"><span data-stu-id="ef56a-104">The **Deduplication** element indicates whether the search result should remove duplicate items.</span></span> 
  
```XML
<Deduplication> true | false </Deduplication>
```

<span data-ttu-id="ef56a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ef56a-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ef56a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ef56a-106">Attributes and elements</span></span>

<span data-ttu-id="ef56a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ef56a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef56a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ef56a-108">Attributes</span></span>

<span data-ttu-id="ef56a-109">无。</span><span class="sxs-lookup"><span data-stu-id="ef56a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef56a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ef56a-110">Child elements</span></span>

<span data-ttu-id="ef56a-111">无。</span><span class="sxs-lookup"><span data-stu-id="ef56a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef56a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ef56a-112">Parent elements</span></span>

<span data-ttu-id="ef56a-113">[SearchMailboxes](searchmailboxes.md)  | [SetHoldOnMailboxes](setholdonmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="ef56a-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ef56a-114">文本值</span><span class="sxs-lookup"><span data-stu-id="ef56a-114">Text value</span></span>

<span data-ttu-id="ef56a-115">对于重复数据删除元素，文本值为**true**表示搜索结果可能不包含重复项。</span><span class="sxs-lookup"><span data-stu-id="ef56a-115">A text value of **true** for the Deduplication element indicates that search results may not contain duplicate items.</span></span> <span data-ttu-id="ef56a-116">**如果值为 false** ，则表示搜索结果可能包含重复项。</span><span class="sxs-lookup"><span data-stu-id="ef56a-116">A value of **false** indicates that search results may contain duplicate items.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ef56a-117">备注</span><span class="sxs-lookup"><span data-stu-id="ef56a-117">Remarks</span></span>

<span data-ttu-id="ef56a-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ef56a-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ef56a-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ef56a-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef56a-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="ef56a-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef56a-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="ef56a-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ef56a-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="ef56a-122">Schema name</span></span>  <br/> |<span data-ttu-id="ef56a-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="ef56a-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="ef56a-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="ef56a-124">Validation file</span></span>  <br/> |<span data-ttu-id="ef56a-125">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="ef56a-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ef56a-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="ef56a-126">Can be empty</span></span>  <br/> |<span data-ttu-id="ef56a-127">false</span><span class="sxs-lookup"><span data-stu-id="ef56a-127">false</span></span>  <br/> |
   

