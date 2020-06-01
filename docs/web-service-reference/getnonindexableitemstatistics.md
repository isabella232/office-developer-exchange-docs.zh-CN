---
title: GetNonIndexableItemStatistics
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dd16d1fb-d82d-42e5-b64a-bc6c19c48fa8
description: GetNonIndexableItemStatistics 元素指定检索 nonindexable 项统计信息的请求。
ms.openlocfilehash: 4b605379f20f5558566f1cfbad9ef1aa33b6fce6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44452788"
---
# <a name="getnonindexableitemstatistics"></a><span data-ttu-id="6f4fb-103">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="6f4fb-103">GetNonIndexableItemStatistics</span></span>

<span data-ttu-id="6f4fb-104">**GetNonIndexableItemStatistics**元素指定检索 nonindexable 项统计信息的请求。</span><span class="sxs-lookup"><span data-stu-id="6f4fb-104">The **GetNonIndexableItemStatistics** element specifies a request to retrieve nonindexable item statistics.</span></span> 
  
```XML
<GetNonIndexableItemStatistics>
    <Mailboxes/>
</GetNonIndexableItemStatistics>
```

 <span data-ttu-id="6f4fb-105">**GetNonIndexableItemStatisticsType**</span><span class="sxs-lookup"><span data-stu-id="6f4fb-105">**GetNonIndexableItemStatisticsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f4fb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f4fb-106">Attributes and elements</span></span>

<span data-ttu-id="6f4fb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f4fb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f4fb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f4fb-108">Attributes</span></span>

<span data-ttu-id="6f4fb-109">无。</span><span class="sxs-lookup"><span data-stu-id="6f4fb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f4fb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6f4fb-110">Child elements</span></span>

|<span data-ttu-id="6f4fb-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f4fb-111">**Element**</span></span>|<span data-ttu-id="6f4fb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f4fb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f4fb-113">邮箱（NonEmptyArrayOfLegacyDNsType）</span><span class="sxs-lookup"><span data-stu-id="6f4fb-113">Mailboxes (NonEmptyArrayOfLegacyDNsType)</span></span>](mailboxes-nonemptyarrayoflegacydnstype.md) <br/> |<span data-ttu-id="6f4fb-114">指定**邮箱**元素的数组。</span><span class="sxs-lookup"><span data-stu-id="6f4fb-114">Specifies an array of **Mailbox** elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f4fb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6f4fb-115">Parent elements</span></span>

<span data-ttu-id="6f4fb-116">无。</span><span class="sxs-lookup"><span data-stu-id="6f4fb-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f4fb-117">说明</span><span class="sxs-lookup"><span data-stu-id="6f4fb-117">Remarks</span></span>

<span data-ttu-id="6f4fb-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f4fb-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6f4fb-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f4fb-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f4fb-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f4fb-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f4fb-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f4fb-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6f4fb-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f4fb-122">Schema Name</span></span>  <br/> |<span data-ttu-id="6f4fb-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="6f4fb-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="6f4fb-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f4fb-124">Validation File</span></span>  <br/> |<span data-ttu-id="6f4fb-125">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="6f4fb-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6f4fb-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f4fb-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6f4fb-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f4fb-127">See also</span></span>



- [<span data-ttu-id="6f4fb-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f4fb-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

