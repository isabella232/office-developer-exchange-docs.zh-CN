---
title: IndexedOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 951ee079-417f-45a2-b47f-633e8cd6b520
description: IndexedOffset元素指示分页的FindConversation响应的索引偏移量。
ms.openlocfilehash: 1332e6e133f20b83bbf5eb713ffb8e0592045d67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825911"
---
# <a name="indexedoffset"></a><span data-ttu-id="4c773-103">IndexedOffset</span><span class="sxs-lookup"><span data-stu-id="4c773-103">IndexedOffset</span></span>

<span data-ttu-id="4c773-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **IndexedOffset**元素指示分页的 **FindConversation**响应的索引偏移量。</span><span class="sxs-lookup"><span data-stu-id="4c773-104">The **IndexedOffset** element indicates the index offset for a paged **FindConversation** response.</span></span> 
  
```XML
<IndexedOffset></IndexedOffset>
```

 <span data-ttu-id="4c773-105">**int**</span><span class="sxs-lookup"><span data-stu-id="4c773-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c773-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4c773-106">Attributes and elements</span></span>

<span data-ttu-id="4c773-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4c773-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c773-108">属性</span><span class="sxs-lookup"><span data-stu-id="4c773-108">Attributes</span></span>

<span data-ttu-id="4c773-109">无。</span><span class="sxs-lookup"><span data-stu-id="4c773-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c773-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4c773-110">Child elements</span></span>

<span data-ttu-id="4c773-111">无。</span><span class="sxs-lookup"><span data-stu-id="4c773-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4c773-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4c773-112">Parent elements</span></span>

[<span data-ttu-id="4c773-113">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="4c773-113">FindConversationResponse</span></span>](findconversationresponse.md)
  
## <a name="text-value"></a><span data-ttu-id="4c773-114">文本值</span><span class="sxs-lookup"><span data-stu-id="4c773-114">Text value</span></span>

<span data-ttu-id="4c773-115">**IndexedOffset**元素的文本值是 **FindConversation**响应页面索引偏移量。</span><span class="sxs-lookup"><span data-stu-id="4c773-115">The text value of the **IndexedOffset** element is the page index offset for **FindConversation** responses.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4c773-116">备注</span><span class="sxs-lookup"><span data-stu-id="4c773-116">Remarks</span></span>

<span data-ttu-id="4c773-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="4c773-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4c773-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4c773-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c773-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="4c773-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c773-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="4c773-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4c773-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="4c773-121">Schema name</span></span>  <br/> |<span data-ttu-id="4c773-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="4c773-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4c773-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="4c773-123">Validation file</span></span>  <br/> |<span data-ttu-id="4c773-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4c773-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4c773-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="4c773-125">Can be empty</span></span>  <br/> ||
   

