---
title: SearchScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4a53989e-eca6-45c4-afac-4d6ac19597d2
description: SearchScope 元素指定搜索的范围。
ms.openlocfilehash: 352292952c735e7d3893790a660096c6b6966536
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827315"
---
# <a name="searchscope"></a><span data-ttu-id="5dca8-103">SearchScope</span><span class="sxs-lookup"><span data-stu-id="5dca8-103">SearchScope</span></span>

<span data-ttu-id="5dca8-104">**SearchScope**元素指定搜索的范围。</span><span class="sxs-lookup"><span data-stu-id="5dca8-104">The **SearchScope** element specifies the scope of a search.</span></span> 
  
```XML
<SearchScope> PrimaryOnly | ArchiveOnly | All </SearchScope>
```

 <span data-ttu-id="5dca8-105">**MailboxSearchLocationType**</span><span class="sxs-lookup"><span data-stu-id="5dca8-105">**MailboxSearchLocationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5dca8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5dca8-106">Attributes and elements</span></span>

<span data-ttu-id="5dca8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5dca8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5dca8-108">属性</span><span class="sxs-lookup"><span data-stu-id="5dca8-108">Attributes</span></span>

<span data-ttu-id="5dca8-109">无。</span><span class="sxs-lookup"><span data-stu-id="5dca8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5dca8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5dca8-110">Child elements</span></span>

<span data-ttu-id="5dca8-111">无。</span><span class="sxs-lookup"><span data-stu-id="5dca8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5dca8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5dca8-112">Parent elements</span></span>

[<span data-ttu-id="5dca8-113">MailboxSearchScope</span><span class="sxs-lookup"><span data-stu-id="5dca8-113">MailboxSearchScope</span></span>](mailboxsearchscope.md)
  
## <a name="text-value"></a><span data-ttu-id="5dca8-114">文本值</span><span class="sxs-lookup"><span data-stu-id="5dca8-114">Text value</span></span>

<span data-ttu-id="5dca8-115">**SearchScope**元素的文本值指示搜索的发现搜索邮箱类型。</span><span class="sxs-lookup"><span data-stu-id="5dca8-115">The text value of the **SearchScope** element indicates the mailbox type that is searched for a discovery search.</span></span> <span data-ttu-id="5dca8-116">**PrimaryOnly**文本值表示主邮箱搜索。</span><span class="sxs-lookup"><span data-stu-id="5dca8-116">A text value of **PrimaryOnly** indicates that the primary mailbox is searched.</span></span> <span data-ttu-id="5dca8-117">**ArchiveOnly**文本值表示的搜索的存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="5dca8-117">A text value of **ArchiveOnly** indicates that the archive mailbox is searched.</span></span> <span data-ttu-id="5dca8-118">**所有**文本值都表示的两个主要和要搜索的存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="5dca8-118">A text value of **All** indicates that both the primary and archive mailboxes are searched.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5dca8-119">备注</span><span class="sxs-lookup"><span data-stu-id="5dca8-119">Remarks</span></span>

<span data-ttu-id="5dca8-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5dca8-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5dca8-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5dca8-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5dca8-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="5dca8-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5dca8-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="5dca8-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5dca8-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="5dca8-124">Schema name</span></span>  <br/> |<span data-ttu-id="5dca8-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="5dca8-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="5dca8-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="5dca8-126">Validation file</span></span>  <br/> |<span data-ttu-id="5dca8-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5dca8-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5dca8-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="5dca8-128">Can be empty</span></span>  <br/> ||
   

