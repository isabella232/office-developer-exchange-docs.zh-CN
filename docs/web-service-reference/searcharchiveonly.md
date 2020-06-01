---
title: SearchArchiveOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cce5344c-b622-44d4-bc14-a0de346c9335
description: SearchArchiveOnly 元素指示是否仅搜索存档邮箱中没有可建立索引的项目。
ms.openlocfilehash: 9014044ed06c697cc43dd62103d7a1a907bda5a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460496"
---
# <a name="searcharchiveonly"></a><span data-ttu-id="baa32-103">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="baa32-103">SearchArchiveOnly</span></span>

<span data-ttu-id="baa32-104">**SearchArchiveOnly**元素指示是否仅搜索存档邮箱中没有可建立索引的项目。</span><span class="sxs-lookup"><span data-stu-id="baa32-104">The **SearchArchiveOnly** element indicates whether only the archive mailbox is searched for non-indexable items.</span></span> 
  
```xml
<SearchArchiveOnly>true | false</SearchArchiveOnly>
```

 <span data-ttu-id="baa32-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="baa32-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="baa32-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="baa32-106">Attributes and elements</span></span>

<span data-ttu-id="baa32-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="baa32-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="baa32-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="baa32-108">Attributes</span></span>

<span data-ttu-id="baa32-109">无。</span><span class="sxs-lookup"><span data-stu-id="baa32-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="baa32-110">子元素</span><span class="sxs-lookup"><span data-stu-id="baa32-110">Child elements</span></span>

<span data-ttu-id="baa32-111">无。</span><span class="sxs-lookup"><span data-stu-id="baa32-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="baa32-112">父元素</span><span class="sxs-lookup"><span data-stu-id="baa32-112">Parent elements</span></span>

<span data-ttu-id="baa32-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span><span class="sxs-lookup"><span data-stu-id="baa32-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="baa32-114">文本值</span><span class="sxs-lookup"><span data-stu-id="baa32-114">Text value</span></span>

<span data-ttu-id="baa32-115">如果**SearchArchiveOnly**元素的文本值为**true** ，则表示仅对存档邮箱执行非索引项目搜索。</span><span class="sxs-lookup"><span data-stu-id="baa32-115">A text value of **true** for the **SearchArchiveOnly** element indicates that non-indexable item search is only performed on the archive mailbox.</span></span> <span data-ttu-id="baa32-116">如果文本值为**false** ，则表示对主邮箱和存档邮箱执行搜索。</span><span class="sxs-lookup"><span data-stu-id="baa32-116">A text value of **false** indicates that the search is performed against the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="baa32-117">备注</span><span class="sxs-lookup"><span data-stu-id="baa32-117">Remarks</span></span>

<span data-ttu-id="baa32-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="baa32-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="baa32-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="baa32-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="baa32-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="baa32-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="baa32-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="baa32-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="baa32-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="baa32-122">Schema name</span></span>  <br/> |<span data-ttu-id="baa32-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="baa32-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="baa32-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="baa32-124">Validation file</span></span>  <br/> |<span data-ttu-id="baa32-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="baa32-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="baa32-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="baa32-126">Can be empty</span></span>  <br/> ||
   

