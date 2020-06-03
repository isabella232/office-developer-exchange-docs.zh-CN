---
title: IsPartiallyIndexed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 542e7b90-eafe-4711-a9d7-71bbc30d9646
description: IsPartiallyIndexed 元素指示是否对项目进行部分索引。
ms.openlocfilehash: 4bf0c3e5dd7b75a90ac087958fbceda334306af1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466484"
---
# <a name="ispartiallyindexed"></a><span data-ttu-id="22f66-103">IsPartiallyIndexed</span><span class="sxs-lookup"><span data-stu-id="22f66-103">IsPartiallyIndexed</span></span>

<span data-ttu-id="22f66-104">**IsPartiallyIndexed**元素指示是否对项目进行部分索引。</span><span class="sxs-lookup"><span data-stu-id="22f66-104">The **IsPartiallyIndexed** element indicates whether the item is partially indexed.</span></span> 
  
```XML
<IsPartiallyIndexed>true | false</IsPartiallyIndexed>
```

 <span data-ttu-id="22f66-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="22f66-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22f66-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22f66-106">Attributes and elements</span></span>

<span data-ttu-id="22f66-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22f66-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22f66-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="22f66-108">Attributes</span></span>

<span data-ttu-id="22f66-109">无。</span><span class="sxs-lookup"><span data-stu-id="22f66-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22f66-110">子元素</span><span class="sxs-lookup"><span data-stu-id="22f66-110">Child elements</span></span>

<span data-ttu-id="22f66-111">无。</span><span class="sxs-lookup"><span data-stu-id="22f66-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22f66-112">父元素</span><span class="sxs-lookup"><span data-stu-id="22f66-112">Parent elements</span></span>

[<span data-ttu-id="22f66-113">NonIndexableItemDetail</span><span class="sxs-lookup"><span data-stu-id="22f66-113">NonIndexableItemDetail</span></span>](nonindexableitemdetail.md)
  
## <a name="text-value"></a><span data-ttu-id="22f66-114">文本值</span><span class="sxs-lookup"><span data-stu-id="22f66-114">Text value</span></span>

<span data-ttu-id="22f66-115">如果**IsPartiallyIndexed**元素的文本值为**true** ，则表示该邮箱项目已部分编制索引。</span><span class="sxs-lookup"><span data-stu-id="22f66-115">A text value of **true** for the **IsPartiallyIndexed** element indicates that the mailbox item is partially indexed.</span></span> <span data-ttu-id="22f66-116">如果值为**false** ，则表示未对邮箱项目进行部分索引。</span><span class="sxs-lookup"><span data-stu-id="22f66-116">A value of **false** indicates that the mailbox item is not partially indexed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="22f66-117">备注</span><span class="sxs-lookup"><span data-stu-id="22f66-117">Remarks</span></span>

<span data-ttu-id="22f66-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="22f66-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="22f66-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22f66-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22f66-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="22f66-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22f66-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="22f66-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22f66-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="22f66-122">Schema name</span></span>  <br/> |<span data-ttu-id="22f66-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="22f66-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="22f66-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="22f66-124">Validation file</span></span>  <br/> |<span data-ttu-id="22f66-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="22f66-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22f66-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="22f66-126">Can be empty</span></span>  <br/> |<span data-ttu-id="22f66-127">false</span><span class="sxs-lookup"><span data-stu-id="22f66-127">false</span></span>  <br/> |
   

