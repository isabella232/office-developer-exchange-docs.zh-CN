---
title: SearchArchiveOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cce5344c-b622-44d4-bc14-a0de346c9335
description: SearchArchiveOnly 元素指示是否将仅存档邮箱搜索的非可索引的项目。
ms.openlocfilehash: ac9d3262784d8052486c631ef3e99e650d4757c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827293"
---
# <a name="searcharchiveonly"></a><span data-ttu-id="2d000-103">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="2d000-103">SearchArchiveOnly</span></span>

<span data-ttu-id="2d000-104">**SearchArchiveOnly**元素指示是否将仅存档邮箱搜索的非可索引的项目。</span><span class="sxs-lookup"><span data-stu-id="2d000-104">The **SearchArchiveOnly** element indicates whether only the archive mailbox is searched for non-indexable items.</span></span> 
  
```xml
<SearchArchiveOnly>true | false</SearchArchiveOnly>
```

 <span data-ttu-id="2d000-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2d000-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d000-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d000-106">Attributes and elements</span></span>

<span data-ttu-id="2d000-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d000-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d000-108">属性</span><span class="sxs-lookup"><span data-stu-id="2d000-108">Attributes</span></span>

<span data-ttu-id="2d000-109">无。</span><span class="sxs-lookup"><span data-stu-id="2d000-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d000-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2d000-110">Child elements</span></span>

<span data-ttu-id="2d000-111">无。</span><span class="sxs-lookup"><span data-stu-id="2d000-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d000-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2d000-112">Parent elements</span></span>

<span data-ttu-id="2d000-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span><span class="sxs-lookup"><span data-stu-id="2d000-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="2d000-114">文本值</span><span class="sxs-lookup"><span data-stu-id="2d000-114">Text value</span></span>

<span data-ttu-id="2d000-115">文本值为**true**的**SearchArchiveOnly**元素指示非可索引项搜索仅执行对存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="2d000-115">A text value of **true** for the **SearchArchiveOnly** element indicates that non-indexable item search is only performed on the archive mailbox.</span></span> <span data-ttu-id="2d000-116">文本值为**false**指示搜索针对的主邮箱和存档邮箱执行。</span><span class="sxs-lookup"><span data-stu-id="2d000-116">A text value of **false** indicates that the search is performed against the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d000-117">备注</span><span class="sxs-lookup"><span data-stu-id="2d000-117">Remarks</span></span>

<span data-ttu-id="2d000-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2d000-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2d000-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d000-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d000-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d000-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d000-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d000-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d000-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d000-122">Schema name</span></span>  <br/> |<span data-ttu-id="2d000-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="2d000-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d000-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d000-124">Validation file</span></span>  <br/> |<span data-ttu-id="2d000-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2d000-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d000-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d000-126">Can be empty</span></span>  <br/> ||
   

