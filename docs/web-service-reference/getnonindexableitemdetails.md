---
title: GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: GetNonIndexableItemDetails 元素指定要检索 nonindexable 项目详细信息的请求。
ms.openlocfilehash: 0aeda85973aa78eff240a017db58ffb57fc0de06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754618"
---
# <a name="getnonindexableitemdetails"></a><span data-ttu-id="3a1f4-103">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="3a1f4-103">GetNonIndexableItemDetails</span></span>

<span data-ttu-id="3a1f4-104">**GetNonIndexableItemDetails**元素指定要检索 nonindexable 项目详细信息的请求。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-104">The **GetNonIndexableItemDetails** element specifies a request to retrieve nonindexable item details.</span></span> 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 <span data-ttu-id="3a1f4-105">**GetNonIndexableItemDetailsType**</span><span class="sxs-lookup"><span data-stu-id="3a1f4-105">**GetNonIndexableItemDetailsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3a1f4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3a1f4-106">Attributes and elements</span></span>

<span data-ttu-id="3a1f4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3a1f4-108">属性</span><span class="sxs-lookup"><span data-stu-id="3a1f4-108">Attributes</span></span>

<span data-ttu-id="3a1f4-109">无。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3a1f4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3a1f4-110">Child elements</span></span>

|<span data-ttu-id="3a1f4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3a1f4-111">**Element**</span></span>|<span data-ttu-id="3a1f4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3a1f4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3a1f4-113">邮箱 (NonEmptyArrayOfLegacyDNsType)</span><span class="sxs-lookup"><span data-stu-id="3a1f4-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="3a1f4-114">指定**邮箱**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
|[<span data-ttu-id="3a1f4-115">PageSize</span><span class="sxs-lookup"><span data-stu-id="3a1f4-115">PageSize</span></span>](pagesize.md) <br/> |<span data-ttu-id="3a1f4-116">包含在单个页面的搜索结果中要返回的项数。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-116">Contains the number of items to be returned in a single page for a search result.</span></span>  <br/> |
|[<span data-ttu-id="3a1f4-117">PageItemReference</span><span class="sxs-lookup"><span data-stu-id="3a1f4-117">PageItemReference</span></span>](pageitemreference.md) <br/> |<span data-ttu-id="3a1f4-118">指定页面项目的引用。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-118">Specifies the reference for a page item.</span></span>  <br/> |
|[<span data-ttu-id="3a1f4-119">PageDirection</span><span class="sxs-lookup"><span data-stu-id="3a1f4-119">PageDirection</span></span>](pagedirection.md) <br/> |<span data-ttu-id="3a1f4-120">包含在搜索结果的分页的方向。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-120">Contains the direction for pagination in the search result.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3a1f4-121">父元素</span><span class="sxs-lookup"><span data-stu-id="3a1f4-121">Parent elements</span></span>

<span data-ttu-id="3a1f4-122">无。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a1f4-123">备注</span><span class="sxs-lookup"><span data-stu-id="3a1f4-123">Remarks</span></span>

<span data-ttu-id="3a1f4-124">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3a1f4-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3a1f4-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3a1f4-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="3a1f4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a1f4-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="3a1f4-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3a1f4-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="3a1f4-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3a1f4-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="3a1f4-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="3a1f4-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="3a1f4-130">Validation File</span></span>  <br/> |<span data-ttu-id="3a1f4-131">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3a1f4-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3a1f4-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="3a1f4-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="3a1f4-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a1f4-133">See also</span></span>



- [<span data-ttu-id="3a1f4-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3a1f4-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

