---
title: 在交换中 EWS eDiscovery
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3128419f-dd5f-46d2-bb0d-0940738d0bb6
description: 了解 Exchange 中 EWS 的电子数据展示。
ms.openlocfilehash: 48e3fdb3a2f21f7dcfcb7eed21b586e099b249a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456092"
---
# <a name="ediscovery-in-ews-in-exchange"></a><span data-ttu-id="0355e-103">在交换中 EWS eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0355e-103">eDiscovery in EWS in Exchange</span></span>

<span data-ttu-id="0355e-104">了解 Exchange 中 EWS 的电子数据展示。</span><span class="sxs-lookup"><span data-stu-id="0355e-104">Learn about eDiscovery in EWS in Exchange.</span></span>
  
<span data-ttu-id="0355e-105">电子数据展示是一种联合查询 web 服务，它使外部应用程序能够执行 Exchange 数据的查询。</span><span class="sxs-lookup"><span data-stu-id="0355e-105">eDiscovery is a federated query web service that enables external applications to perform queries of Exchange data.</span></span>
  
<span data-ttu-id="0355e-106">发现包括几个阶段，包括标识和保留关键数据、在法庭中剔除和查看数据以及生成数据。</span><span class="sxs-lookup"><span data-stu-id="0355e-106">Discovery consists of several phases, including identifying and preserving key data, culling down and reviewing the data, and producing data in court.</span></span> <span data-ttu-id="0355e-107">电子数据展示查询通过跨 Exchange 和 SharePoint 提供单个发现工作流来促进发现过程。</span><span class="sxs-lookup"><span data-stu-id="0355e-107">eDiscovery queries facilitate the discovery process by providing a single discovery workflow across Exchange and SharePoint.</span></span>
  
## <a name="ediscovery-operations"></a><span data-ttu-id="0355e-108">电子数据展示操作</span><span class="sxs-lookup"><span data-stu-id="0355e-108">eDiscovery operations</span></span>

<span data-ttu-id="0355e-109">通过 Exchange Online 中引入的操作、Exchange Online （作为 Office 365 的一部分）和从 Exchange 2013 开始的 Exchange 版本提供了由 EWS 公开的电子数据展示功能。</span><span class="sxs-lookup"><span data-stu-id="0355e-109">The eDiscovery functionality that is exposed by EWS is available via operations introduced in Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013.</span></span> 
  
<span data-ttu-id="0355e-110">**表1。电子数据展示的新操作**</span><span class="sxs-lookup"><span data-stu-id="0355e-110">**Table 1. New operations for eDiscovery**</span></span>

|<span data-ttu-id="0355e-111">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="0355e-111">**Operation name**</span></span>|<span data-ttu-id="0355e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0355e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0355e-113">GetDiscoverySearchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0355e-113">GetDiscoverySearchConfiguration</span></span>](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) <br/> |<span data-ttu-id="0355e-114">获取就地保留的配置信息、已保存的发现搜索以及为发现搜索启用的邮箱。</span><span class="sxs-lookup"><span data-stu-id="0355e-114">Gets configuration information for in-place holds, saved discovery searches, and the mailboxes that are enabled for discovery search.</span></span>  <br/> |
|[<span data-ttu-id="0355e-115">GetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="0355e-115">GetHoldOnMailboxes</span></span>](https://msdn.microsoft.com/library/9157f329-80b4-4cd0-a158-378064966ae6%28Office.15%29.aspx) <br/> |<span data-ttu-id="0355e-116">获取基于查询的保留的状态，它是通过使用[SetHoldOnMailboxes 操作](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx)设置的。</span><span class="sxs-lookup"><span data-stu-id="0355e-116">Gets the status of a query-based hold, which is set by using the [SetHoldOnMailboxes operation](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx).</span></span>  <br/> |
|[<span data-ttu-id="0355e-117">GetNonIndexableItemDetails</span><span class="sxs-lookup"><span data-stu-id="0355e-117">GetNonIndexableItemDetails</span></span>](https://msdn.microsoft.com/library/9279c3ad-f7c8-4bbc-b0a7-2c78416cb39a%28Office.15%29.aspx) <br/> |<span data-ttu-id="0355e-118">检索有关无法编制索引的项目的详细信息。</span><span class="sxs-lookup"><span data-stu-id="0355e-118">Retrieves details about items that cannot be indexed.</span></span> <span data-ttu-id="0355e-119">这包括但不限于项目标识符、错误代码、错误说明、对项目编制索引时，以及有关文件的其他信息。</span><span class="sxs-lookup"><span data-stu-id="0355e-119">This includes, but is not limited to, the item identifier, an error code, an error description, when an attempt was made to index the item, and additional information about the file.</span></span>  <br/> |
|[<span data-ttu-id="0355e-120">GetNonIndexableItemStatistics</span><span class="sxs-lookup"><span data-stu-id="0355e-120">GetNonIndexableItemStatistics</span></span>](https://msdn.microsoft.com/library/ed077877-9d98-4434-b8b6-a4a905e7f7a6%28Office.15%29.aspx) <br/> |<span data-ttu-id="0355e-121">检索邮箱中无法编制索引的项目数。</span><span class="sxs-lookup"><span data-stu-id="0355e-121">Retrieves the count of items that cannot be indexed in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="0355e-122">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="0355e-122">GetSearchableMailboxes</span></span>](https://msdn.microsoft.com/library/47f8ff57-4835-4d2d-9136-44afb31a4cbe%28Office.15%29.aspx) <br/> |<span data-ttu-id="0355e-123">获取客户端有权搜索或执行电子数据展示的邮箱的列表。</span><span class="sxs-lookup"><span data-stu-id="0355e-123">Gets a list of mailboxes that the client has permission to search or perform eDiscovery on.</span></span>  <br/> |
|[<span data-ttu-id="0355e-124">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="0355e-124">SearchMailboxes</span></span>](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |<span data-ttu-id="0355e-125">搜索与查询关键字匹配的特定邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="0355e-125">Searches for items in specific mailboxes that match query keywords.</span></span>  <br/> |
|[<span data-ttu-id="0355e-126">SetHoldOnMailboxes</span><span class="sxs-lookup"><span data-stu-id="0355e-126">SetHoldOnMailboxes</span></span>](https://msdn.microsoft.com/library/9015a0d8-3495-461b-aa79-797d23169585%28Office.15%29.aspx) <br/> |<span data-ttu-id="0355e-127">设置项目的基于查询的保留。</span><span class="sxs-lookup"><span data-stu-id="0355e-127">Sets a query-based hold on items.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0355e-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0355e-128">See also</span></span>

- [<span data-ttu-id="0355e-129">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="0355e-129">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="0355e-130">开始使用 Exchange 中的 Web 服务</span><span class="sxs-lookup"><span data-stu-id="0355e-130">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="0355e-131">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="0355e-131">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

