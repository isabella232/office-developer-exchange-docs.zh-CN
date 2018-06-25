---
title: 消除
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a38acc3d-29a8-4466-81a4-73cb30fe5e80
description: 消除元素指示搜索结果是否应移除重复项。
ms.openlocfilehash: 3f06bb1dccd0677b7fd43c4ad82eda54a0c3f812
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753775"
---
# <a name="deduplication"></a><span data-ttu-id="4f06c-103">消除</span><span class="sxs-lookup"><span data-stu-id="4f06c-103">Deduplication</span></span>

<span data-ttu-id="4f06c-104">**消除**元素指示搜索结果是否应移除重复项。</span><span class="sxs-lookup"><span data-stu-id="4f06c-104">The **Deduplication** element indicates whether the search result should remove duplicate items.</span></span> 
  
```XML
<Deduplication> true | false </Deduplication>
```

<span data-ttu-id="4f06c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4f06c-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="4f06c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4f06c-106">Attributes and elements</span></span>

<span data-ttu-id="4f06c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4f06c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f06c-108">属性</span><span class="sxs-lookup"><span data-stu-id="4f06c-108">Attributes</span></span>

<span data-ttu-id="4f06c-109">无。</span><span class="sxs-lookup"><span data-stu-id="4f06c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f06c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4f06c-110">Child elements</span></span>

<span data-ttu-id="4f06c-111">无。</span><span class="sxs-lookup"><span data-stu-id="4f06c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4f06c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4f06c-112">Parent elements</span></span>

<span data-ttu-id="4f06c-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="4f06c-113">[SearchMailboxes](searchmailboxes.md) | [SetHoldOnMailboxes](setholdonmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4f06c-114">文本值</span><span class="sxs-lookup"><span data-stu-id="4f06c-114">Text value</span></span>

<span data-ttu-id="4f06c-115">文本值为**true**的消除元素指示搜索结果可能不包含重复的项目。</span><span class="sxs-lookup"><span data-stu-id="4f06c-115">A text value of **true** for the Deduplication element indicates that search results may not contain duplicate items.</span></span> <span data-ttu-id="4f06c-116">如果值为**false**指示搜索结果可能包含重复的项目。</span><span class="sxs-lookup"><span data-stu-id="4f06c-116">A value of **false** indicates that search results may contain duplicate items.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4f06c-117">备注</span><span class="sxs-lookup"><span data-stu-id="4f06c-117">Remarks</span></span>

<span data-ttu-id="4f06c-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4f06c-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4f06c-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4f06c-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f06c-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="4f06c-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f06c-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="4f06c-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4f06c-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="4f06c-122">Schema name</span></span>  <br/> |<span data-ttu-id="4f06c-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="4f06c-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="4f06c-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="4f06c-124">Validation file</span></span>  <br/> |<span data-ttu-id="4f06c-125">types.xsd</span><span class="sxs-lookup"><span data-stu-id="4f06c-125">types.xsd</span></span>  <br/> |
|<span data-ttu-id="4f06c-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="4f06c-126">Can be empty</span></span>  <br/> |<span data-ttu-id="4f06c-127">false</span><span class="sxs-lookup"><span data-stu-id="4f06c-127">false</span></span>  <br/> |
   

