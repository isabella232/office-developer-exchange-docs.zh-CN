---
title: 过滤
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a7ee364-b7da-4197-aab2-57134537109a
description: 过滤元素包含用于筛选要从 GetSearchableMailboxes 请求中返回的邮箱的查询字符串。
ms.openlocfilehash: 5bc7389ecc54dd6d1c97debdb97e6fce42517ef4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467429"
---
# <a name="searchfilter"></a><span data-ttu-id="ad356-103">过滤</span><span class="sxs-lookup"><span data-stu-id="ad356-103">SearchFilter</span></span>

<span data-ttu-id="ad356-104">**过滤**元素包含用于筛选要从**GetSearchableMailboxes**请求中返回的邮箱的查询字符串。</span><span class="sxs-lookup"><span data-stu-id="ad356-104">The **SearchFilter** element contains the query string to filter the mailboxes to be returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<SearchFilter></SearchFilter>
```

 <span data-ttu-id="ad356-105">**string**</span><span class="sxs-lookup"><span data-stu-id="ad356-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ad356-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ad356-106">Attributes and elements</span></span>

<span data-ttu-id="ad356-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ad356-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad356-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ad356-108">Attributes</span></span>

<span data-ttu-id="ad356-109">无。</span><span class="sxs-lookup"><span data-stu-id="ad356-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ad356-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ad356-110">Child elements</span></span>

<span data-ttu-id="ad356-111">无。</span><span class="sxs-lookup"><span data-stu-id="ad356-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ad356-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ad356-112">Parent elements</span></span>

[<span data-ttu-id="ad356-113">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="ad356-113">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="ad356-114">文本值</span><span class="sxs-lookup"><span data-stu-id="ad356-114">Text value</span></span>

<span data-ttu-id="ad356-115">**过滤**元素的文本值是用于筛选要发现搜索的邮箱的查询字符串。</span><span class="sxs-lookup"><span data-stu-id="ad356-115">The text value of the **SearchFilter** element is a query string to filter mailboxes for discovery search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ad356-116">备注</span><span class="sxs-lookup"><span data-stu-id="ad356-116">Remarks</span></span>

<span data-ttu-id="ad356-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ad356-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ad356-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ad356-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad356-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="ad356-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad356-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="ad356-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ad356-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="ad356-121">Schema name</span></span>  <br/> |<span data-ttu-id="ad356-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="ad356-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ad356-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="ad356-123">Validation file</span></span>  <br/> |<span data-ttu-id="ad356-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ad356-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ad356-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="ad356-125">Can be empty</span></span>  <br/> ||
   

