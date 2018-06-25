---
title: SearchFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a7ee364-b7da-4197-aab2-57134537109a
description: SearchFilter 元素包含要筛选的邮箱从 GetSearchableMailboxes 请求返回的查询字符串。
ms.openlocfilehash: b71d8dd862e9338afc145545df4cd29e8bcc3dc8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827285"
---
# <a name="searchfilter"></a><span data-ttu-id="49cb0-103">SearchFilter</span><span class="sxs-lookup"><span data-stu-id="49cb0-103">SearchFilter</span></span>

<span data-ttu-id="49cb0-104">**SearchFilter**元素包含要筛选的邮箱从**GetSearchableMailboxes**请求返回的查询字符串。</span><span class="sxs-lookup"><span data-stu-id="49cb0-104">The **SearchFilter** element contains the query string to filter the mailboxes to be returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<SearchFilter></SearchFilter>
```

 <span data-ttu-id="49cb0-105">**string**</span><span class="sxs-lookup"><span data-stu-id="49cb0-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="49cb0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="49cb0-106">Attributes and elements</span></span>

<span data-ttu-id="49cb0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="49cb0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49cb0-108">属性</span><span class="sxs-lookup"><span data-stu-id="49cb0-108">Attributes</span></span>

<span data-ttu-id="49cb0-109">无。</span><span class="sxs-lookup"><span data-stu-id="49cb0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="49cb0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="49cb0-110">Child elements</span></span>

<span data-ttu-id="49cb0-111">无。</span><span class="sxs-lookup"><span data-stu-id="49cb0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="49cb0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="49cb0-112">Parent elements</span></span>

[<span data-ttu-id="49cb0-113">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="49cb0-113">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="49cb0-114">文本值</span><span class="sxs-lookup"><span data-stu-id="49cb0-114">Text value</span></span>

<span data-ttu-id="49cb0-115">**SearchFilter**元素的文本值是到筛选器发现搜索邮箱的查询字符串。</span><span class="sxs-lookup"><span data-stu-id="49cb0-115">The text value of the **SearchFilter** element is a query string to filter mailboxes for discovery search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="49cb0-116">备注</span><span class="sxs-lookup"><span data-stu-id="49cb0-116">Remarks</span></span>

<span data-ttu-id="49cb0-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="49cb0-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="49cb0-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="49cb0-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="49cb0-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="49cb0-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49cb0-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="49cb0-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="49cb0-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="49cb0-121">Schema name</span></span>  <br/> |<span data-ttu-id="49cb0-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="49cb0-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="49cb0-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="49cb0-123">Validation file</span></span>  <br/> |<span data-ttu-id="49cb0-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="49cb0-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="49cb0-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="49cb0-125">Can be empty</span></span>  <br/> ||
   

