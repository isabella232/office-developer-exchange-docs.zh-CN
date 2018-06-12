---
title: ResultType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 488ee828-343f-4382-a5e8-eed1005f5dbc
description: ResultType 元素包含要执行的搜索的类型。 搜索的类型可以仅限统计信息或仅预览。
ms.openlocfilehash: 750f53ae05a7ad9f5aefc9396911a23ef32cdfc2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827211"
---
# <a name="resulttype"></a><span data-ttu-id="dec6f-104">ResultType</span><span class="sxs-lookup"><span data-stu-id="dec6f-104">ResultType</span></span>

<span data-ttu-id="dec6f-105">**ResultType**元素包含要执行的搜索的类型。</span><span class="sxs-lookup"><span data-stu-id="dec6f-105">The **ResultType** element contains the type of search to perform.</span></span> <span data-ttu-id="dec6f-106">搜索的类型可以仅限统计信息或仅预览。</span><span class="sxs-lookup"><span data-stu-id="dec6f-106">The type of search can be statistics only or preview only.</span></span> 
  
```XML
<ResultType>StatisticsOnly | PreviewOnly</ResultType>
```

 <span data-ttu-id="dec6f-107">**SearchResultType**</span><span class="sxs-lookup"><span data-stu-id="dec6f-107">**SearchResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dec6f-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dec6f-108">Attributes and elements</span></span>

<span data-ttu-id="dec6f-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dec6f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dec6f-110">属性</span><span class="sxs-lookup"><span data-stu-id="dec6f-110">Attributes</span></span>

<span data-ttu-id="dec6f-111">无。</span><span class="sxs-lookup"><span data-stu-id="dec6f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dec6f-112">子元素</span><span class="sxs-lookup"><span data-stu-id="dec6f-112">Child elements</span></span>

<span data-ttu-id="dec6f-113">无。</span><span class="sxs-lookup"><span data-stu-id="dec6f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dec6f-114">父元素</span><span class="sxs-lookup"><span data-stu-id="dec6f-114">Parent elements</span></span>

<span data-ttu-id="dec6f-115">[SearchMailboxesResult](searchmailboxesresult.md) | [SearchMailboxes](searchmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="dec6f-115">[SearchMailboxesResult](searchmailboxesresult.md) | [SearchMailboxes](searchmailboxes.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="dec6f-116">文本值</span><span class="sxs-lookup"><span data-stu-id="dec6f-116">Text value</span></span>

<span data-ttu-id="dec6f-117">**ResultType**元素的文本值是结果的发现搜索在搜索返回的类型。</span><span class="sxs-lookup"><span data-stu-id="dec6f-117">The text value of the **ResultType** element is the type of result that is returned for a discovery search.</span></span> <span data-ttu-id="dec6f-118">**StatisticsOnly**文本值将返回的搜索统计信息。</span><span class="sxs-lookup"><span data-stu-id="dec6f-118">A text value of **StatisticsOnly** will return the search statistics.</span></span> <span data-ttu-id="dec6f-119">**PreviewOnly**文本值将返回项预览信息。</span><span class="sxs-lookup"><span data-stu-id="dec6f-119">A text value of **PreviewOnly** will return item preview information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dec6f-120">备注</span><span class="sxs-lookup"><span data-stu-id="dec6f-120">Remarks</span></span>

<span data-ttu-id="dec6f-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="dec6f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dec6f-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dec6f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dec6f-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="dec6f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dec6f-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="dec6f-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dec6f-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="dec6f-125">Schema name</span></span>  <br/> |<span data-ttu-id="dec6f-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="dec6f-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dec6f-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="dec6f-127">Validation file</span></span>  <br/> |<span data-ttu-id="dec6f-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dec6f-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dec6f-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="dec6f-129">Can be empty</span></span>  <br/> |<span data-ttu-id="dec6f-130">false</span><span class="sxs-lookup"><span data-stu-id="dec6f-130">false</span></span>  <br/> |
   

