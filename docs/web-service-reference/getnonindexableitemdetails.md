---
title: GetNonIndexableItemDetails
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce3994c1-3bb4-4571-b026-34a6c5705410
description: GetNonIndexableItemDetails 元素指定检索 nonindexable 项详细信息的请求。
ms.openlocfilehash: 1c04b4cd7a86183210be869973c9779188fa0adf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458598"
---
# <a name="getnonindexableitemdetails"></a><span data-ttu-id="dc56b-103">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="dc56b-103">GetNonIndexableItemDetails</span></span>

<span data-ttu-id="dc56b-104">**GetNonIndexableItemDetails**元素指定检索 nonindexable 项详细信息的请求。</span><span class="sxs-lookup"><span data-stu-id="dc56b-104">The **GetNonIndexableItemDetails** element specifies a request to retrieve nonindexable item details.</span></span> 
  
```XML
<GetNonIndexableItemDetails>
    <Mailboxes/>
    <PageSize/>
    <PageItemReference/>
    <PageDirection/>
</GetNonIndexableItemDetails>
```

 <span data-ttu-id="dc56b-105">**GetNonIndexableItemDetailsType**</span><span class="sxs-lookup"><span data-stu-id="dc56b-105">**GetNonIndexableItemDetailsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc56b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc56b-106">Attributes and elements</span></span>

<span data-ttu-id="dc56b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc56b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc56b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dc56b-108">Attributes</span></span>

<span data-ttu-id="dc56b-109">无。</span><span class="sxs-lookup"><span data-stu-id="dc56b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc56b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dc56b-110">Child elements</span></span>

|<span data-ttu-id="dc56b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="dc56b-111">**Element**</span></span>|<span data-ttu-id="dc56b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="dc56b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dc56b-113">邮箱（NonEmptyArrayOfLegacyDNsType）</span><span class="sxs-lookup"><span data-stu-id="dc56b-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="dc56b-114">指定**邮箱**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="dc56b-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
|[<span data-ttu-id="dc56b-115">PageSize</span><span class="sxs-lookup"><span data-stu-id="dc56b-115">PageSize</span></span>](pagesize.md) <br/> |<span data-ttu-id="dc56b-116">包含要在单个页面中返回的搜索结果的项目数。</span><span class="sxs-lookup"><span data-stu-id="dc56b-116">Contains the number of items to be returned in a single page for a search result.</span></span>  <br/> |
|[<span data-ttu-id="dc56b-117">PageItemReference</span><span class="sxs-lookup"><span data-stu-id="dc56b-117">PageItemReference</span></span>](pageitemreference.md) <br/> |<span data-ttu-id="dc56b-118">指定对页面项的引用。</span><span class="sxs-lookup"><span data-stu-id="dc56b-118">Specifies the reference for a page item.</span></span>  <br/> |
|[<span data-ttu-id="dc56b-119">PageDirection</span><span class="sxs-lookup"><span data-stu-id="dc56b-119">PageDirection</span></span>](pagedirection.md) <br/> |<span data-ttu-id="dc56b-120">包含在搜索结果中进行分页的方向。</span><span class="sxs-lookup"><span data-stu-id="dc56b-120">Contains the direction for pagination in the search result.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="dc56b-121">父元素</span><span class="sxs-lookup"><span data-stu-id="dc56b-121">Parent elements</span></span>

<span data-ttu-id="dc56b-122">无。</span><span class="sxs-lookup"><span data-stu-id="dc56b-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc56b-123">说明</span><span class="sxs-lookup"><span data-stu-id="dc56b-123">Remarks</span></span>

<span data-ttu-id="dc56b-124">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="dc56b-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc56b-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc56b-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc56b-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc56b-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc56b-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc56b-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dc56b-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc56b-128">Schema Name</span></span>  <br/> |<span data-ttu-id="dc56b-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="dc56b-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="dc56b-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc56b-130">Validation File</span></span>  <br/> |<span data-ttu-id="dc56b-131">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="dc56b-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dc56b-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc56b-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="dc56b-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc56b-133">See also</span></span>



- [<span data-ttu-id="dc56b-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="dc56b-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

