---
title: Exchange 中的 EWS 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exchange
api_type:
- schema
ms.assetid: cf6fd871-9a65-4f34-8557-c8c71dd7ce09
description: 查找有关可在 Exchange 中的 EWS 操作的信息。
ms.openlocfilehash: c56c3be746138cec251836fcb61ee3738d168869
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754192"
---
# <a name="ews-operations-in-exchange"></a><span data-ttu-id="8c9c9-103">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-103">EWS operations in Exchange</span></span>

<span data-ttu-id="8c9c9-104">查找有关可在 Exchange 中的 EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-104">Find information about the EWS operations that are available in Exchange.</span></span>
  
<span data-ttu-id="8c9c9-105">Exchange Web Services (EWS) 提供了使您能够从 Exchange 存储中访问信息的多个操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-105">Exchange Web Services (EWS) provides many operations that enable you to access information from the Exchange store.</span></span> <span data-ttu-id="8c9c9-106">本节中的文章提供有关请求、 响应和错误响应消息 EWS 操作，以及对于每个操作的 XML 示例的总体结构的信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-106">The articles in this section provide information about the overall structure of the requests, responses, and error response messages for EWS operations, as well as XML examples for each operation.</span></span> <span data-ttu-id="8c9c9-107">它们提供客户端和服务器之间发送的消息结构的概述。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-107">They provide an overview of the message structures that are sent between the client and the server.</span></span> <span data-ttu-id="8c9c9-108">调试消息结构并查找 EWS 请求中可以实现的功能的信息，您可以使用此信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-108">You can use this information to debug message structures and to find information about what you can do in an EWS request.</span></span> <span data-ttu-id="8c9c9-109">有关详细信息哪些 XML 结构表示，请参阅- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-109">For more information about what the XML structure represents, see - [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md).</span></span>
  
<span data-ttu-id="8c9c9-110">EWS 的所有功能都相关联的架构的版本。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-110">All EWS functionality is associated with a version of the schema.</span></span> <span data-ttu-id="8c9c9-111">在 Exchange 服务器或 Exchange Online 的新版本中引入新 EWS 架构版本。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-111">New EWS schema versions are introduced in new releases of Exchange Server or Exchange Online.</span></span> <span data-ttu-id="8c9c9-112">[RequestServerVersion](requestserverversion.md)元素包含**版本**属性映射到的架构版本的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-112">The [RequestServerVersion](requestserverversion.md) element contains a **Version** attribute that maps the server version to the schema version.</span></span> <span data-ttu-id="8c9c9-113">本文提供有关每个操作引入时信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-113">This article provides information about when each operation was introduced.</span></span> <span data-ttu-id="8c9c9-114">操作中的特定功能可能需要更高版本的服务。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-114">Specific functionality within an operation might require a later version of the service.</span></span> <span data-ttu-id="8c9c9-115">以便旨在针对 EWS 旧版本的客户端将使用新版本的 EWS 实现版本控制的架构。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-115">The versioned schemas are implemented so that clients that are designed against an older version of EWS will work with a newer version of EWS.</span></span> 
  
<span data-ttu-id="8c9c9-116">这些操作可以目标 services 您的邮箱的 EWS 终结点。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-116">These operations can target the EWS endpoint that services your mailbox.</span></span> <span data-ttu-id="8c9c9-117">您可以通过使用在结构类似于 http:// URL 浏览到 EWS 终结点<clientaccessserver>.com/ews/exchange.asmx，其中<clientaccessserver>是 services 您的邮箱的 Exchange 客户端访问服务器。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-117">You can browse to the EWS endpoint by using a URL that is similar in structure to http://<clientaccessserver>.com/ews/exchange.asmx, where <clientaccessserver> is the Exchange Client Access server that services your mailbox.</span></span> <span data-ttu-id="8c9c9-118">您可以使用自动发现服务邮箱的客户端访问服务器获取 URL。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-118">You can use Autodiscover to get the URL to the Client Access server that services your mailbox.</span></span> <span data-ttu-id="8c9c9-119">有关自动发现的详细信息，请参阅[exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-119">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
## <a name="ediscovery-operations"></a><span data-ttu-id="8c9c9-120">电子数据展示操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-120">eDiscovery operations</span></span>
<span data-ttu-id="8c9c9-121"><a name="bk_eDiscovery"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-121"></span></span>

<span data-ttu-id="8c9c9-122">电子数据展示操作提供的法律保留项搜索操作，并确定无法编制索引和发现搜索结果中返回的邮箱数据。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-122">The eDiscovery operations provide search operations for legal holds and identify mailbox data that cannot be indexed and returned in discovery search results.</span></span>
  
<span data-ttu-id="8c9c9-123">下表列出的电子数据展示操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-123">The following table lists the eDiscovery operations.</span></span>
  
|<span data-ttu-id="8c9c9-124">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-124">**Operation name**</span></span>|<span data-ttu-id="8c9c9-125">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-125">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-126">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-126">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md) <br/> |<span data-ttu-id="8c9c9-127">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-127">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-128">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-128">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md) <br/> |<span data-ttu-id="8c9c9-129">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-129">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-130">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-130">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md) <br/> |<span data-ttu-id="8c9c9-131">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-131">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-132">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-132">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md) <br/> |<span data-ttu-id="8c9c9-133">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-133">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-134">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-134">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md) <br/> |<span data-ttu-id="8c9c9-135">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-135">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-136">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-136">SearchMailboxes operation</span></span>](searchmailboxes-operation.md) <br/> |<span data-ttu-id="8c9c9-137">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-137">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-138">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-138">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md) <br/> |<span data-ttu-id="8c9c9-139">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-139">Exchange 2013</span></span>  <br/> |
   
## <a name="exchange-mailbox-data-operations"></a><span data-ttu-id="8c9c9-140">Exchange 邮箱数据操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-140">Exchange mailbox data operations</span></span>
<span data-ttu-id="8c9c9-141"><a name="bk_Exchange_mailbox_data"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-141"></span></span>

<span data-ttu-id="8c9c9-142">Exchange 邮箱数据操作使客户端处理和组织项目、 文件夹和附件，以及模糊名称解析和通讯组列表扩展。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-142">The Exchange mailbox data operations enable clients to handle and organize items, folders, and attachments, as well as ambiguous name resolution and distribution list expansion.</span></span> <span data-ttu-id="8c9c9-143">Exchange 邮箱数据操作包括项目、 文件夹、 附件和实用程序操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-143">Exchange mailbox data operations include item, folder, attachment, and utilities operations.</span></span>
  
<span data-ttu-id="8c9c9-144">下表列出了 Exchange 邮箱数据操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-144">The following table lists the Exchange mailbox data operations.</span></span>
  
|<span data-ttu-id="8c9c9-145">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-145">**Operation name**</span></span>|<span data-ttu-id="8c9c9-146">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-146">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-147">ArchiveItem 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-147">ArchiveItem operation</span></span>](archiveitem-operation.md) <br/> |<span data-ttu-id="8c9c9-148">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-148">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-149">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-149">CreateItem operation</span></span>](createitem-operation.md) <br/> |<span data-ttu-id="8c9c9-150">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-150">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-151">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-151">CopyItem operation</span></span>](copyitem-operation.md) <br/> |<span data-ttu-id="8c9c9-152">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-152">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-153">删除项操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-153">DeleteItem operation</span></span>](deleteitem-operation.md) <br/> |<span data-ttu-id="8c9c9-154">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-154">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-155">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-155">FindItem operation</span></span>](finditem-operation.md) <br/> |<span data-ttu-id="8c9c9-156">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-156">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-157">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-157">GetItem operation</span></span>](getitem-operation.md) <br/> |<span data-ttu-id="8c9c9-158">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-158">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-159">MarkAllItemsAsRead 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-159">MarkAllItemsAsRead operation</span></span>](markallitemsasread-operation.md) <br/> |<span data-ttu-id="8c9c9-160">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-160">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-161">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-161">MoveItem operation</span></span>](moveitem-operation.md) <br/> |<span data-ttu-id="8c9c9-162">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-162">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-163">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-163">SendItem operation</span></span>](senditem-operation.md) <br/> |<span data-ttu-id="8c9c9-164">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-164">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-165">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-165">UpdateItem operation</span></span>](updateitem-operation.md) <br/> |<span data-ttu-id="8c9c9-166">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-166">Exchange 2007</span></span>  <br/> |
   
<span data-ttu-id="8c9c9-167">下表列出了 Exchange 邮箱数据文件夹操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-167">The following table lists the Exchange mailbox data folder operations.</span></span>
  
|<span data-ttu-id="8c9c9-168">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-168">**Operation name**</span></span>|<span data-ttu-id="8c9c9-169">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-169">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-170">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8c9c9-170">CreateFolder operation</span></span>](createfolder-operation.md) <br/> |<span data-ttu-id="8c9c9-171">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-171">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-172">CreateFolderPath 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-172">CreateFolderPath operation</span></span>](createfolderpath-operation.md) <br/> |<span data-ttu-id="8c9c9-173">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-173">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-174">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-174">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md) <br/> |<span data-ttu-id="8c9c9-175">Exchange 2007。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-175">Exchange 2007.</span></span> <span data-ttu-id="8c9c9-176">此功能具有已 deemphasized 中启动与 Exchange 2010 的 Exchange 版本。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-176">This functionality has been deemphasized in versions of Exchange starting with Exchange 2010.</span></span> <span data-ttu-id="8c9c9-177">有关如何迁移到用于保留标记和策略邮件记录管理的详细信息，请参阅[从托管文件夹迁移](http://technet.microsoft.com/en-us/library/dd298032%28v=exchg.141%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-177">For more information about how to migrate to using retention tags and policies for messaging records management, see [Migrate from Managed Folders](http://technet.microsoft.com/en-us/library/dd298032%28v=exchg.141%29.aspx).</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-178">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-178">CopyFolder operation</span></span>](copyfolder-operation.md) <br/> |<span data-ttu-id="8c9c9-179">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-179">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-180">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-180">DeleteFolder operation</span></span>](deletefolder-operation.md) <br/> |<span data-ttu-id="8c9c9-181">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-181">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-182">EmptyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-182">EmptyFolder operation</span></span>](emptyfolder-operation.md) <br/> |<span data-ttu-id="8c9c9-183">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-183">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-184">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8c9c9-184">FindFolder operation</span></span>](findfolder-operation.md) <br/> |<span data-ttu-id="8c9c9-185">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-185">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-186">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8c9c9-186">GetFolder operation</span></span>](getfolder-operation.md) <br/> |<span data-ttu-id="8c9c9-187">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-187">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-188">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-188">MoveFolder operation</span></span>](movefolder-operation.md) <br/> |<span data-ttu-id="8c9c9-189">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-189">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-190">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8c9c9-190">UpdateFolder operation</span></span>](updatefolder-operation.md) <br/> |<span data-ttu-id="8c9c9-191">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-191">Exchange 2007</span></span>  <br/> |
   
<span data-ttu-id="8c9c9-192">下表列出了 Exchange 邮箱数据附件操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-192">The following table lists the Exchange mailbox data attachment operations.</span></span>
  
|<span data-ttu-id="8c9c9-193">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-193">**Operation name**</span></span>|<span data-ttu-id="8c9c9-194">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-194">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-195">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-195">CreateAttachment operation</span></span>](createattachment-operation.md) <br/> |<span data-ttu-id="8c9c9-196">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-196">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-197">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-197">GetAttachment operation</span></span>](getattachment-operation.md) <br/> |<span data-ttu-id="8c9c9-198">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-198">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-199">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-199">DeleteAttachment operation</span></span>](deleteattachment-operation.md) <br/> |<span data-ttu-id="8c9c9-200">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-200">Exchange 2007</span></span>  <br/> |
   
<span data-ttu-id="8c9c9-201">下表列出了 Exchange 邮箱提醒操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-201">The following table lists the Exchange mailbox reminder operations.</span></span>
  
|<span data-ttu-id="8c9c9-202">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-202">**Operation name**</span></span>|<span data-ttu-id="8c9c9-203">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-203">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-204">GetReminders 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-204">GetReminders operation</span></span>](getreminders-operation.md) <br/> |<span data-ttu-id="8c9c9-205">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-205">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-206">PerformReminderAction 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-206">PerformReminderAction operation</span></span>](performreminderaction-operation.md) <br/> |<span data-ttu-id="8c9c9-207">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-207">Exchange 2013</span></span>  <br/> |
   
<span data-ttu-id="8c9c9-208">下表列出了 Exchange 邮箱数据对话操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-208">The following table lists the Exchange mailbox data conversation operations.</span></span>
  
|<span data-ttu-id="8c9c9-209">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-209">**Operation name**</span></span>|<span data-ttu-id="8c9c9-210">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-210">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-211">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-211">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md) <br/> |<span data-ttu-id="8c9c9-212">Exchange 2010 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="8c9c9-212">Exchange 2010 Service Pack 1 (SP1)</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-213">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="8c9c9-213">FindConversation operation</span></span>](findconversation-operation.md) <br/> |<span data-ttu-id="8c9c9-214">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-214">Exchange 2010 SP1</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-215">GetConversationItems 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-215">GetConversationItems operation</span></span>](getconversationitems-operation.md) <br/> |<span data-ttu-id="8c9c9-216">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-216">Exchange 2013</span></span>  <br/> |
   
<span data-ttu-id="8c9c9-217">下表列出了 Exchange 邮箱数据实用程序操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-217">The following table lists the Exchange mailbox data utilities operations.</span></span>
  
|<span data-ttu-id="8c9c9-218">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-218">**Operation name**</span></span>|<span data-ttu-id="8c9c9-219">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-219">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-220">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-220">ConvertId operation</span></span>](convertid-operation.md) <br/> |<span data-ttu-id="8c9c9-221">Exchange 2007 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-221">Exchange 2007 Service Pack 1</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-222">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-222">ExpandDL operation</span></span>](expanddl-operation.md) <br/> |<span data-ttu-id="8c9c9-223">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-223">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-224">GetUserPhoto 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-224">GetUserPhoto operation</span></span>](getuserphoto-operation.md) <br/> |<span data-ttu-id="8c9c9-225">Exchange 2013。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-225">Exchange 2013.</span></span> <span data-ttu-id="8c9c9-226">此操作具有 REST 和 SOAP 实现。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-226">This operation has both a REST and a SOAP implementation.</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-227">MarkAsJunk 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-227">MarkAsJunk operation</span></span>](markasjunk-operation.md) <br/> |<span data-ttu-id="8c9c9-228">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-228">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-229">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-229">ResolveNames operation</span></span>](resolvenames-operation.md) <br/> |<span data-ttu-id="8c9c9-230">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-230">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-231">GetPasswordExpirationDate 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-231">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md) <br/> |<span data-ttu-id="8c9c9-232">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-232">Exchange 2010 SP1</span></span>  <br/> |
   
## <a name="availability-operations"></a><span data-ttu-id="8c9c9-233">可用性操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-233">Availability operations</span></span>
<span data-ttu-id="8c9c9-234"><a name="bk_Availability"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-234"></span></span>

<span data-ttu-id="8c9c9-235">可用性操作改进的日历和忙/闲共享提供了更多安全、 最新的且丰富忙/闲信息的体验。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-235">The availability operations improve the calendar and free/busy sharing experience by providing more secure, up-to-date, and rich free/busy information.</span></span> <span data-ttu-id="8c9c9-236">忙/闲数据是安排会议的关键组成部分。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-236">Free/busy data is a critical component of scheduling meetings.</span></span> <span data-ttu-id="8c9c9-237">可用性操作提供有效安排的可靠基础。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-237">The availability operations provide a reliable foundation for effective scheduling.</span></span> 
  
<span data-ttu-id="8c9c9-238">下表列出了可用性操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-238">The following table lists the availability operations.</span></span>
  
|<span data-ttu-id="8c9c9-239">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-239">**Operation name**</span></span>|<span data-ttu-id="8c9c9-240">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-240">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-241">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-241">GetUserAvailability operation</span></span>](getuseravailability-operation.md) <br/> |<span data-ttu-id="8c9c9-242">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-242">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-243">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-243">GetRoomLists operation</span></span>](getroomlists-operation.md) <br/> |<span data-ttu-id="8c9c9-244">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-244">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-245">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-245">GetRooms operation</span></span>](getrooms-operation.md) <br/> |<span data-ttu-id="8c9c9-246">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-246">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-247">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-247">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md) <br/> |<span data-ttu-id="8c9c9-248">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-248">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-249">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-249">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md) <br/> |<span data-ttu-id="8c9c9-250">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-250">Exchange 2007</span></span>  <br/> |
   
## <a name="bulk-transfer-operations"></a><span data-ttu-id="8c9c9-251">批量传输操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-251">Bulk transfer operations</span></span>
<span data-ttu-id="8c9c9-252"><a name="bk_bulk_transfer"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-252"></span></span>

<span data-ttu-id="8c9c9-253">批量传输操作使流项目的客户端和注销邮箱。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-253">The bulk transfer operations enable clients to stream items into and out of a mailbox.</span></span> 
  
<span data-ttu-id="8c9c9-254">下表列出了批量传输操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-254">The following table lists the bulk transfer operations.</span></span>
  
|<span data-ttu-id="8c9c9-255">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-255">**Operation name**</span></span>|<span data-ttu-id="8c9c9-256">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-256">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-257">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-257">UploadItems operation</span></span>](uploaditems-operation.md) <br/> |<span data-ttu-id="8c9c9-258">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-258">Exchange 2010 SP1</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-259">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-259">ExportItems operation</span></span>](exportitems-operation.md) <br/> |<span data-ttu-id="8c9c9-260">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-260">Exchange 2010 SP1</span></span>  <br/> |
   
## <a name="delegate-management-operations"></a><span data-ttu-id="8c9c9-261">委派管理操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-261">Delegate management operations</span></span>
<span data-ttu-id="8c9c9-262"><a name="bk_delegate_management"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-262"></span></span>

<span data-ttu-id="8c9c9-263">委托管理操作使客户端可以添加、 获取、 更新和删除其邮箱的代理人。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-263">The delegate management operations enable clients to add, get, update, and remove delegates from their mailboxes.</span></span> 
  
<span data-ttu-id="8c9c9-264">下表列出了委托管理操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-264">The following table lists the delegate management operations.</span></span>
  
|<span data-ttu-id="8c9c9-265">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-265">**Operation name**</span></span>|<span data-ttu-id="8c9c9-266">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-266">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-267">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-267">AddDelegate operation</span></span>](adddelegate-operation.md) <br/> |<span data-ttu-id="8c9c9-268">Exchange 2007 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="8c9c9-268">Exchange 2007 Service Pack 1 (SP1)</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-269">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-269">GetDelegate operation</span></span>](getdelegate-operation.md) <br/> |<span data-ttu-id="8c9c9-270">Exchange 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-270">Exchange 2007 SP1</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-271">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-271">UpdateDelegate operation</span></span>](updatedelegate-operation.md) <br/> |<span data-ttu-id="8c9c9-272">Exchange 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-272">Exchange 2007 SP1</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-273">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-273">RemoveDelegate operation</span></span>](removedelegate-operation.md) <br/> |<span data-ttu-id="8c9c9-274">Exchange 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-274">Exchange 2007 SP1</span></span>  <br/> |
   
## <a name="inbox-rules-operations"></a><span data-ttu-id="8c9c9-275">收件箱规则操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-275">Inbox rules operations</span></span>
<span data-ttu-id="8c9c9-276"><a name="bk_inbox_rules"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-276"></span></span>

<span data-ttu-id="8c9c9-277">收件箱规则操作使客户端获取收件箱规则和更新这些服务器上的邮件。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-277">The Inbox rules operations enable clients to get Inbox rules and update them for messages on the server.</span></span> <span data-ttu-id="8c9c9-278">收件箱规则是条件和启用自动组织、 分类和消息传递到文件夹用作邮件客户端中的关联的操作的集合。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-278">Inbox rules are sets of conditions and associated actions that enable clients to automatically organize, categorize, and act on messages as the messages are delivered to a folder.</span></span> 
  
<span data-ttu-id="8c9c9-279">下表列出的收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-279">The following table lists the Inbox rules operations.</span></span>
  
|<span data-ttu-id="8c9c9-280">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-280">**Operation name**</span></span>|<span data-ttu-id="8c9c9-281">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-281">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-282">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-282">GetInboxRules operation</span></span>](getinboxrules-operation.md) <br/> |<span data-ttu-id="8c9c9-283">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-283">Exchange 2010 SP1</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-284">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-284">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md) <br/> |<span data-ttu-id="8c9c9-285">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-285">Exchange 2010 SP1</span></span>  <br/> |
   
## <a name="mail-app-management-operations"></a><span data-ttu-id="8c9c9-286">邮件应用程序管理操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-286">Mail app management operations</span></span>
<span data-ttu-id="8c9c9-287"><a name="bk_mail_apps"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-287"></span></span>

<span data-ttu-id="8c9c9-288">邮件应用程序管理操作使您能够管理 outlook 邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-288">The mail app management operations enable you to manage mail apps for Outlook.</span></span> <span data-ttu-id="8c9c9-289">您可以使用这些操作来安装、 卸载、 禁用，并获取有关可用于 Outlook Web App 和 Outlook 2013 的邮件应用程序的信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-289">You can use these operations to install, uninstall, disable, and get information about mail apps that are available for Outlook Web App and Outlook 2013.</span></span>
  
<span data-ttu-id="8c9c9-290">下表列出了邮件应用程序管理操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-290">The following table lists the mail app management operations.</span></span>
  
|<span data-ttu-id="8c9c9-291">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-291">**Operation name**</span></span>|<span data-ttu-id="8c9c9-292">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-292">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-293">DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-293">DisableApp operation</span></span>](disableapp-operation.md) <br/> |<span data-ttu-id="8c9c9-294">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-294">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-295">GetAppManifests 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-295">GetAppManifests operation</span></span>](getappmanifests-operation.md) <br/> |<span data-ttu-id="8c9c9-296">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-296">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-297">GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-297">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md) <br/> |<span data-ttu-id="8c9c9-298">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-298">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-299">GetClientAccessToken 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-299">GetClientAccessToken operation</span></span>](getclientaccesstoken-operation.md) <br/> |<span data-ttu-id="8c9c9-300">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-300">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-301">InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-301">InstallApp operation</span></span>](installapp-operation.md) <br/> |<span data-ttu-id="8c9c9-302">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-302">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-303">UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-303">UninstallApp operation</span></span>](uninstallapp-operation.md) <br/> |<span data-ttu-id="8c9c9-304">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-304">Exchange 2013</span></span>  <br/> |
   
## <a name="mail-tips-operation"></a><span data-ttu-id="8c9c9-305">邮件提示操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-305">Mail tips operation</span></span>
<span data-ttu-id="8c9c9-306"><a name="bk_mail_tips"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-306"></span></span>

<span data-ttu-id="8c9c9-307">邮件提示操作作者撰写邮件时允许从有关收件人的邮箱服务器请求信息的客户端。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-307">The mail tips operation enables clients to request information from the server about recipient mailboxes when an author is composing a message.</span></span> <span data-ttu-id="8c9c9-308">下表列出了邮件提示操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-308">The following table lists the mail tips operation.</span></span>
  
|<span data-ttu-id="8c9c9-309">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-309">**Operation name**</span></span>|<span data-ttu-id="8c9c9-310">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-310">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-311">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-311">GetMailTips operation</span></span>](getmailtips-operation.md) <br/> |<span data-ttu-id="8c9c9-312">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-312">Exchange 2010</span></span>  <br/> |
   
## <a name="message-tracking-operations"></a><span data-ttu-id="8c9c9-313">邮件跟踪操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-313">Message tracking operations</span></span>
<span data-ttu-id="8c9c9-314"><a name="bk_message_tracking"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-314"></span></span>

<span data-ttu-id="8c9c9-315">邮件跟踪操作使客户端来查找满足指定的条件的邮件并获取邮件跟踪报告中的每封邮件的详细的跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-315">The message tracking operations enable clients to find messages that meet specified criteria and to get detailed tracking information about each message in a message tracking report.</span></span> 
  
<span data-ttu-id="8c9c9-316">下表列出的邮件跟踪操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-316">The following table lists the message tracking operations.</span></span>
  
|<span data-ttu-id="8c9c9-317">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-317">**Operation name**</span></span>|<span data-ttu-id="8c9c9-318">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-318">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-319">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-319">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md) <br/> |<span data-ttu-id="8c9c9-320">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-320">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-321">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-321">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md) <br/> |<span data-ttu-id="8c9c9-322">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-322">Exchange 2010</span></span>  <br/> |
   
## <a name="notification-operations"></a><span data-ttu-id="8c9c9-323">通知操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-323">Notification operations</span></span>
<span data-ttu-id="8c9c9-324"><a name="bk_notification"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-324"></span></span>

<span data-ttu-id="8c9c9-325">通知操作通知的项目和文件夹与相关联的事件的客户端应用程序指定的邮箱。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-325">The notification operations notify the client application of events that are associated with items and folders a specified mailbox.</span></span> <span data-ttu-id="8c9c9-326">订阅模型可以基于推送的、 基于拉或基于流式处理的。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-326">The subscription model can be push-based, pull-based, or streaming-based.</span></span> 
  
<span data-ttu-id="8c9c9-327">下表列出了通知操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-327">The following table lists the notification operations.</span></span>
  
|<span data-ttu-id="8c9c9-328">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-328">**Operation name**</span></span>|<span data-ttu-id="8c9c9-329">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-329">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-330">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-330">GetEvents operation</span></span>](getevents-operation.md) <br/> |<span data-ttu-id="8c9c9-331">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-331">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-332">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-332">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md) <br/> |<span data-ttu-id="8c9c9-333">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="8c9c9-333">Exchange 2010 SP1</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-334">订阅操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-334">Subscribe operation</span></span>](subscribe-operation.md) <br/> |<span data-ttu-id="8c9c9-335">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-335">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-336">取消操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-336">Unsubscribe operation</span></span>](unsubscribe-operation.md) <br/> |<span data-ttu-id="8c9c9-337">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-337">Exchange 2007</span></span>  <br/> |
   
## <a name="persona-operations"></a><span data-ttu-id="8c9c9-338">个人操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-338">Persona operations</span></span>
<span data-ttu-id="8c9c9-339"><a name="bk_personas"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-339"></span></span>

<span data-ttu-id="8c9c9-340">个人操作提供查找和获取有关链接的联系人信息的接口。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-340">The persona operations provide an interface to find and get information about a linked contact.</span></span> <span data-ttu-id="8c9c9-341">下表列出了个人操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-341">The following table lists the persona operations.</span></span>
  
|<span data-ttu-id="8c9c9-342">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-342">**Operation name**</span></span>|<span data-ttu-id="8c9c9-343">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-343">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-344">FindPeople 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-344">FindPeople operation</span></span>](findpeople-operation.md) <br/> |<span data-ttu-id="8c9c9-345">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-345">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-346">GetPersona 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-346">GetPersona operation</span></span>](getpersona-operation.md) <br/> |<span data-ttu-id="8c9c9-347">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-347">Exchange 2013</span></span>  <br/> |
   
## <a name="retention-policy-operation"></a><span data-ttu-id="8c9c9-348">保留策略操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-348">Retention policy operation</span></span>
<span data-ttu-id="8c9c9-349"><a name="bk_retention_policy"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-349"></span></span>

<span data-ttu-id="8c9c9-350">保留策略操作提供的所有保留标记链接到用户的保留策略的列表。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-350">The retention policy operation provides a list of all the retention tags that are linked to a user's retention policy.</span></span> 
  
<span data-ttu-id="8c9c9-351">下表列出了保留策略操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-351">The following table lists the retention policy operation.</span></span>
  
|<span data-ttu-id="8c9c9-352">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-352">**Operation name**</span></span>|<span data-ttu-id="8c9c9-353">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-353">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-354">GetUserRetentionPolicyTags 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-354">GetUserRetentionPolicyTags operation</span></span>](getuserretentionpolicytags-operation.md) <br/> |<span data-ttu-id="8c9c9-355">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-355">Exchange 2013</span></span>  <br/> |
   
## <a name="service-configuration-operation"></a><span data-ttu-id="8c9c9-356">服务配置操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-356">Service configuration operation</span></span>
<span data-ttu-id="8c9c9-357"><a name="bk_service_config"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-357"></span></span>

<span data-ttu-id="8c9c9-358">服务配置操作使客户端若要获取的统一消息、 保护规则、 策略提示和邮件提示服务的配置信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-358">The service configuration operation enables clients to get configuration information for the Unified Messaging, Protection Rules, Policy Tips, and Mail Tips services.</span></span> 
  
<span data-ttu-id="8c9c9-359">下表列出的服务配置操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-359">The following table lists the service configuration operation.</span></span>
  
|<span data-ttu-id="8c9c9-360">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-360">**Operation name**</span></span>|<span data-ttu-id="8c9c9-361">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-361">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-362">GetServiceConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-362">GetServiceConfiguration operation</span></span>](getserviceconfiguration-operation.md) <br/> |<span data-ttu-id="8c9c9-363">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-363">Exchange 2010</span></span>  <br/> |
   
## <a name="sharing-operations"></a><span data-ttu-id="8c9c9-364">共享操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-364">Sharing operations</span></span>
<span data-ttu-id="8c9c9-365"><a name="bk_sharing"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-365"></span></span>

<span data-ttu-id="8c9c9-366">共享操作使客户端共享日历数据和联系人数据。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-366">The sharing operations enable clients to share calendar data and contacts data.</span></span> 
  
<span data-ttu-id="8c9c9-367">下表列出的共享的操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-367">The following table lists the sharing operations.</span></span>
  
|<span data-ttu-id="8c9c9-368">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-368">**Operation name**</span></span>|<span data-ttu-id="8c9c9-369">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-369">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-370">CreateItem (AcceptSharingInvitation)</span><span class="sxs-lookup"><span data-stu-id="8c9c9-370">CreateItem (AcceptSharingInvitation)</span></span>](createitem-acceptsharinginvitation.md) <br/> |<span data-ttu-id="8c9c9-371">Exchange 2010。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-371">Exchange 2010.</span></span> <span data-ttu-id="8c9c9-372">适用于所有版本的 EWS **CreateItem** operation，尽管**AcceptSharingInvitation** response 对象才适用于 EWS 中启动与 Exchange 2010 的 Exchange 版本。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-372">Although the **CreateItem** operation is applicable to all versions of EWS, the **AcceptSharingInvitation** response object is only applicable to EWS in versions of Exchange starting with Exchange 2010.</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-373">GetSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-373">GetSharingFolder operation</span></span>](getsharingfolder-operation.md) <br/> |<span data-ttu-id="8c9c9-374">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-374">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-375">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-375">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md) <br/> |<span data-ttu-id="8c9c9-376">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-376">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-377">RefreshSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-377">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md) <br/> |<span data-ttu-id="8c9c9-378">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-378">Exchange 2010</span></span>  <br/> |
   
## <a name="synchronization-operations"></a><span data-ttu-id="8c9c9-379">同步操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-379">Synchronization operations</span></span>
<span data-ttu-id="8c9c9-380"><a name="bk_synchronization"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-380"></span></span>

<span data-ttu-id="8c9c9-381">同步操作提供用户的文件夹和项目的单向同步缓存的副本。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-381">The synchronization operations provide a one-way synchronized cached copy of a user's folders and items.</span></span> 
  
<span data-ttu-id="8c9c9-382">下表列出的同步操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-382">The following table lists the synchronization operations.</span></span>
  
|<span data-ttu-id="8c9c9-383">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-383">**Operation name**</span></span>|<span data-ttu-id="8c9c9-384">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-384">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-385">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-385">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md) <br/> |<span data-ttu-id="8c9c9-386">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-386">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-387">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-387">SyncFolderItems operation</span></span>](syncfolderitems-operation.md) <br/> |<span data-ttu-id="8c9c9-388">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="8c9c9-388">Exchange 2007</span></span>  <br/> |
   
## <a name="time-zone-operation"></a><span data-ttu-id="8c9c9-389">所在的时区操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-389">Time zone operation</span></span>
<span data-ttu-id="8c9c9-390"><a name="bk_timezone"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-390"></span></span>

<span data-ttu-id="8c9c9-391">所在的时区操作使客户端以获取服务器支持的时区定义的列表。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-391">The time zone operation enables clients to get a list of time zone definitions that are supported by the server.</span></span> 
  
<span data-ttu-id="8c9c9-392">下表列出了所在的时区操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-392">The following table lists the time zone operation.</span></span>
  
|<span data-ttu-id="8c9c9-393">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-393">**Operation name**</span></span>|<span data-ttu-id="8c9c9-394">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-394">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-395">GetServerTimeZones 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-395">GetServerTimeZones operation</span></span>](getservertimezones-operation.md) <br/> |<span data-ttu-id="8c9c9-396">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-396">Exchange 2010</span></span>  <br/> |
   
## <a name="unified-messaging-operations"></a><span data-ttu-id="8c9c9-397">统一的消息操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-397">Unified Messaging operations</span></span>
<span data-ttu-id="8c9c9-398"><a name="bk_um"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-398"></span></span>

<span data-ttu-id="8c9c9-399">统一消息操作使客户端读取有关统一消息属性的信息以及通过电话播放语音邮件。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-399">The Unified Messaging operations enable clients to read information about Unified Messaging properties and to play voice mail messages over the phone.</span></span> 
  
<span data-ttu-id="8c9c9-400">下表列出了统一消息操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-400">The following table lists the Unified Messaging operations.</span></span>
  
|<span data-ttu-id="8c9c9-401">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-401">**Operation name**</span></span>|<span data-ttu-id="8c9c9-402">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-402">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-403">DisconnectPhoneCall 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-403">DisconnectPhoneCall operation</span></span>](disconnectphonecall-operation.md) <br/> |<span data-ttu-id="8c9c9-404">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-404">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-405">GetPhoneCallInformation 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-405">GetPhoneCallInformation operation</span></span>](getphonecallinformation-operation.md) <br/> |<span data-ttu-id="8c9c9-406">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-406">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-407">PlayOnPhone 操作 (EWS)</span><span class="sxs-lookup"><span data-stu-id="8c9c9-407">PlayOnPhone operation (EWS)</span></span>](playonphone-operation-ews.md) <br/> |<span data-ttu-id="8c9c9-408">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-408">Exchange 2010</span></span>  <br/> |
   
<span data-ttu-id="8c9c9-409">使用[GetServiceConfiguration 操作](getserviceconfiguration-operation.md)获取邮箱的统一消息配置信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-409">Use the [GetServiceConfiguration operation](getserviceconfiguration-operation.md) to get the Unified Messaging configuration information for a mailbox.</span></span> <span data-ttu-id="8c9c9-410">使用面向 Exchange 2007 的统一消息的应用程序的统一消息 web 服务。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-410">Use the Unified Messaging web service for Unified Messaging applications that target Exchange 2007.</span></span> <span data-ttu-id="8c9c9-411">有关详细信息，请参阅[exchange 统一消息 web 服务的引用](unified-messaging-web-service-reference-for-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-411">For more information, see [Unified Messaging web service reference for Exchange](unified-messaging-web-service-reference-for-exchange.md).</span></span>
  
## <a name="unified-contact-store-operations"></a><span data-ttu-id="8c9c9-412">统一的联系人存储库操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-412">Unified Contact Store operations</span></span>
<span data-ttu-id="8c9c9-413"><a name="bk_ucs"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-413"></span></span>

<span data-ttu-id="8c9c9-414">统一联系人存储库跨 Office 产品提供一致的联系人体验，并用作第三方应用程序可以使用相同的联系人存储库的集成点。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-414">The Unified Contact Store provides a consistent contact experience across Office products and acts as an integration point for third-party applications to use the same contact store.</span></span> <span data-ttu-id="8c9c9-415">使用户和应用程序存储、 管理和访问联系人信息并使其可全局之间 Lync、 Exchange 2013、 Outlook、 Outlook Web App 和实现对统一联系人存储库的访问的任何其他应用程序。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-415">It enables users and applications to store, manage, and access contact information and make it available globally among Lync, Exchange 2013, Outlook, Outlook Web App, and any other application that implements access to the Unified Contact Store.</span></span> <span data-ttu-id="8c9c9-416">Exchange 的统一联系人存储库体验的内容存储。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-416">Exchange is the content store for the Unified Contact Store experience.</span></span>
  
<span data-ttu-id="8c9c9-417">下表列出了统一联系人存储库操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-417">The following table lists the Unified Contact Store operations.</span></span>
  
|<span data-ttu-id="8c9c9-418">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-418">**Operation name**</span></span>|<span data-ttu-id="8c9c9-419">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-419">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-420">AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-420">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md) <br/> |<span data-ttu-id="8c9c9-421">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-421">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-422">AddImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-422">AddImContactToGroup operation</span></span>](addimcontacttogroup-operation.md) <br/> |<span data-ttu-id="8c9c9-423">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-423">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-424">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-424">AddImGroup operation</span></span>](addimgroup-operation.md) <br/> |<span data-ttu-id="8c9c9-425">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-425">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-426">AddNewTelUriContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-426">AddNewTelUriContactToGroup operation</span></span>](addnewteluricontacttogroup-operation.md) <br/> |<span data-ttu-id="8c9c9-427">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-427">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-428">AddDistributionGroupToImList 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-428">AddDistributionGroupToImList operation</span></span>](adddistributiongrouptoimlist-operation.md) <br/> |<span data-ttu-id="8c9c9-429">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-429">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-430">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-430">GetImItemList operation</span></span>](getimitemlist-operation.md) <br/> |<span data-ttu-id="8c9c9-431">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-431">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-432">GetImItems 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-432">GetImItems operation</span></span>](getimitems-operation.md) <br/> |<span data-ttu-id="8c9c9-433">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-433">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-434">RemoveContactFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-434">RemoveContactFromImList operation</span></span>](removecontactfromimlist-operation.md) <br/> |<span data-ttu-id="8c9c9-435">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-435">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-436">RemoveImContactFromGroup 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-436">RemoveImContactFromGroup operation</span></span>](removeimcontactfromgroup-operation.md) <br/> |<span data-ttu-id="8c9c9-437">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-437">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-438">RemoveDistributionGroupFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-438">RemoveDistributionGroupFromImList operation</span></span>](removedistributiongroupfromimlist-operation.md) <br/> |<span data-ttu-id="8c9c9-439">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-439">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-440">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-440">RemoveImGroup operation</span></span>](removeimgroup-operation.md) <br/> |<span data-ttu-id="8c9c9-441">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-441">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-442">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-442">SetImGroup operation</span></span>](setimgroup-operation.md) <br/> |<span data-ttu-id="8c9c9-443">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="8c9c9-443">Exchange 2013</span></span>  <br/> |
   
## <a name="user-configuration-operations"></a><span data-ttu-id="8c9c9-444">用户配置操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-444">User configuration operations</span></span>
<span data-ttu-id="8c9c9-445"><a name="bk_user_config"> </a></span><span class="sxs-lookup"><span data-stu-id="8c9c9-445"></span></span>

<span data-ttu-id="8c9c9-446">用户配置操作使客户端可以创建、 删除和获取，并更新用户配置信息。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-446">The user configuration operations enable clients to create, delete, get, and update user configuration information.</span></span> 
  
<span data-ttu-id="8c9c9-447">下表列出了用户配置操作。</span><span class="sxs-lookup"><span data-stu-id="8c9c9-447">The following table lists the user configuration operations.</span></span>
  
|<span data-ttu-id="8c9c9-448">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-448">**Operation name**</span></span>|<span data-ttu-id="8c9c9-449">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="8c9c9-449">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c9c9-450">CreateUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-450">CreateUserConfiguration operation</span></span>](createuserconfiguration-operation.md) <br/> |<span data-ttu-id="8c9c9-451">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-451">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-452">DeleteUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-452">DeleteUserConfiguration operation</span></span>](deleteuserconfiguration-operation.md) <br/> |<span data-ttu-id="8c9c9-453">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-453">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-454">GetUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-454">GetUserConfiguration operation</span></span>](getuserconfiguration-operation.md) <br/> |<span data-ttu-id="8c9c9-455">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-455">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="8c9c9-456">UpdateUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="8c9c9-456">UpdateUserConfiguration operation</span></span>](updateuserconfiguration-operation.md) <br/> |<span data-ttu-id="8c9c9-457">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="8c9c9-457">Exchange 2010</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c9c9-458">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8c9c9-458">See also</span></span>

- [<span data-ttu-id="8c9c9-459">在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务</span><span class="sxs-lookup"><span data-stu-id="8c9c9-459">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [<span data-ttu-id="8c9c9-460">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="8c9c9-460">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
- [<span data-ttu-id="8c9c9-461">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="8c9c9-461">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
    

