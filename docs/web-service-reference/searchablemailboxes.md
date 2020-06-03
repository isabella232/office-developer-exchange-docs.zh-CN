---
title: SearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eb0a7897-c642-4c93-a238-be03128af54e
description: SearchableMailboxes 元素包含从 GetSearchableMailboxes 请求返回的邮箱的数组。
ms.openlocfilehash: 5de15e1c2ae4a587052f836b189651450a1e7482
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467443"
---
# <a name="searchablemailboxes"></a><span data-ttu-id="ec4c3-103">SearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="ec4c3-103">SearchableMailboxes</span></span>

<span data-ttu-id="ec4c3-104">**SearchableMailboxes**元素包含从**GetSearchableMailboxes**请求返回的邮箱的数组。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-104">The **SearchableMailboxes** element contains an array of the mailboxes returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<SearchableMailboxes>
   <SearchableMailbox/>
</SearchableMailboxes>
```

 <span data-ttu-id="ec4c3-105">**ArrayOfSearchableMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="ec4c3-105">**ArrayOfSearchableMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec4c3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ec4c3-106">Attributes and elements</span></span>

<span data-ttu-id="ec4c3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec4c3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ec4c3-108">Attributes</span></span>

<span data-ttu-id="ec4c3-109">无。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec4c3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ec4c3-110">Child elements</span></span>

[<span data-ttu-id="ec4c3-111">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="ec4c3-111">SearchableMailbox</span></span>](searchablemailbox.md)
  
### <a name="parent-elements"></a><span data-ttu-id="ec4c3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ec4c3-112">Parent elements</span></span>

[<span data-ttu-id="ec4c3-113">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="ec4c3-113">GetSearchableMailboxesResponse</span></span>](getsearchablemailboxesresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="ec4c3-114">备注</span><span class="sxs-lookup"><span data-stu-id="ec4c3-114">Remarks</span></span>

<span data-ttu-id="ec4c3-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ec4c3-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ec4c3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec4c3-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="ec4c3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec4c3-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="ec4c3-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ec4c3-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="ec4c3-119">Schema name</span></span>  <br/> |<span data-ttu-id="ec4c3-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="ec4c3-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ec4c3-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="ec4c3-121">Validation file</span></span>  <br/> |<span data-ttu-id="ec4c3-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ec4c3-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ec4c3-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="ec4c3-123">Can be empty</span></span>  <br/> ||
   

