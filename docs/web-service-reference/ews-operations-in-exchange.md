---
title: Exchange 中的 EWS 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- Exchange
api_type:
- schema
ms.assetid: cf6fd871-9a65-4f34-8557-c8c71dd7ce09
description: 查找有关 Exchange 中可用的 EWS 操作的信息。
localization_priority: Priority
ms.openlocfilehash: 143903d9198a7e31e876adcbbb336df34ecf01fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526121"
---
# <a name="ews-operations-in-exchange"></a><span data-ttu-id="9e44f-103">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-103">EWS operations in Exchange</span></span>

<span data-ttu-id="9e44f-104">查找有关 Exchange 中可用的 EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-104">Find information about the EWS operations that are available in Exchange.</span></span>
  
<span data-ttu-id="9e44f-105">Exchange Web 服务（EWS）提供了许多可让您访问 Exchange 存储中的信息的操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-105">Exchange Web Services (EWS) provides many operations that enable you to access information from the Exchange store.</span></span> <span data-ttu-id="9e44f-106">本节中的文章提供有关 EWS 操作的请求、响应和错误响应消息的整体结构的信息，以及每个操作的 XML 示例。</span><span class="sxs-lookup"><span data-stu-id="9e44f-106">The articles in this section provide information about the overall structure of the requests, responses, and error response messages for EWS operations, as well as XML examples for each operation.</span></span> <span data-ttu-id="9e44f-107">它们提供在客户端和服务器之间发送的邮件结构的概述。</span><span class="sxs-lookup"><span data-stu-id="9e44f-107">They provide an overview of the message structures that are sent between the client and the server.</span></span> <span data-ttu-id="9e44f-108">您可以使用此信息来调试邮件结构，并查找有关在 EWS 请求中可以执行的操作的信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-108">You can use this information to debug message structures and to find information about what you can do in an EWS request.</span></span> <span data-ttu-id="9e44f-109">有关 XML 结构表示的内容的详细信息，请参阅- [EWS xml 元素在 Exchange 中](ews-xml-elements-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="9e44f-109">For more information about what the XML structure represents, see - [EWS XML elements in Exchange](ews-xml-elements-in-exchange.md).</span></span>
  
<span data-ttu-id="9e44f-110">所有 EWS 功能都与架构的一个版本相关联。</span><span class="sxs-lookup"><span data-stu-id="9e44f-110">All EWS functionality is associated with a version of the schema.</span></span> <span data-ttu-id="9e44f-111">Exchange Server 或 Exchange Online 的新版本中引入了新的 EWS 架构版本。</span><span class="sxs-lookup"><span data-stu-id="9e44f-111">New EWS schema versions are introduced in new releases of Exchange Server or Exchange Online.</span></span> <span data-ttu-id="9e44f-112">[RequestServerVersion](requestserverversion.md)元素包含一个**version**属性，该属性将服务器版本映射到架构版本。</span><span class="sxs-lookup"><span data-stu-id="9e44f-112">The [RequestServerVersion](requestserverversion.md) element contains a **Version** attribute that maps the server version to the schema version.</span></span> <span data-ttu-id="9e44f-113">本文提供有关每个操作的引入时间的信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-113">This article provides information about when each operation was introduced.</span></span> <span data-ttu-id="9e44f-114">操作中的特定功能可能需要更高版本的服务。</span><span class="sxs-lookup"><span data-stu-id="9e44f-114">Specific functionality within an operation might require a later version of the service.</span></span> <span data-ttu-id="9e44f-115">已对版本化架构进行了实现，以便针对较旧版本的 EWS 设计的客户端将在新版本的 EWS 中运行。</span><span class="sxs-lookup"><span data-stu-id="9e44f-115">The versioned schemas are implemented so that clients that are designed against an older version of EWS will work with a newer version of EWS.</span></span> 
  
<span data-ttu-id="9e44f-116">这些操作可面向为您的邮箱服务的 EWS 终结点。</span><span class="sxs-lookup"><span data-stu-id="9e44f-116">These operations can target the EWS endpoint that services your mailbox.</span></span> <span data-ttu-id="9e44f-117">您可以使用结构中类似于 http:///EWS/的 URL 浏览到 EWS 终结点 <clientaccessserver> ，其中 <clientaccessserver> 是为您的邮箱服务的 Exchange 客户端访问服务器。</span><span class="sxs-lookup"><span data-stu-id="9e44f-117">You can browse to the EWS endpoint by using a URL that is similar in structure to http://<clientaccessserver>.com/ews/exchange.asmx, where <clientaccessserver> is the Exchange Client Access server that services your mailbox.</span></span> <span data-ttu-id="9e44f-118">您可以使用自动发现获取服务于您的邮箱的客户端访问服务器的 URL。</span><span class="sxs-lookup"><span data-stu-id="9e44f-118">You can use Autodiscover to get the URL to the Client Access server that services your mailbox.</span></span> <span data-ttu-id="9e44f-119">有关自动发现的详细信息，请参阅[Exchange 的自动发现](../exchange-web-services/autodiscover-for-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="9e44f-119">For more information about Autodiscover, see [Autodiscover for Exchange](../exchange-web-services/autodiscover-for-exchange.md).</span></span>
  
## <a name="ediscovery-operations"></a><span data-ttu-id="9e44f-120">电子数据展示操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-120">eDiscovery operations</span></span>
<span data-ttu-id="9e44f-121"><a name="bk_eDiscovery"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-121"><a name="bk_eDiscovery"> </a></span></span>

<span data-ttu-id="9e44f-122">电子数据展示操作提供了用于法律保留的搜索操作，并可识别在发现搜索结果中无法编制索引和返回的邮箱数据。</span><span class="sxs-lookup"><span data-stu-id="9e44f-122">The eDiscovery operations provide search operations for legal holds and identify mailbox data that cannot be indexed and returned in discovery search results.</span></span>
  
<span data-ttu-id="9e44f-123">下表列出了电子数据展示操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-123">The following table lists the eDiscovery operations.</span></span>
  
|<span data-ttu-id="9e44f-124">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-124">**Operation name**</span></span>|<span data-ttu-id="9e44f-125">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-125">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-126">GetDiscoverySearchConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-126">GetDiscoverySearchConfiguration operation</span></span>](getdiscoverysearchconfiguration-operation.md) <br/> |<span data-ttu-id="9e44f-127">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-127">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-128">GetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-128">GetHoldOnMailboxes operation</span></span>](getholdonmailboxes-operation.md) <br/> |<span data-ttu-id="9e44f-129">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-129">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-130">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-130">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md) <br/> |<span data-ttu-id="9e44f-131">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-131">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-132">GetNonIndexableItemStatistics 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-132">GetNonIndexableItemStatistics operation</span></span>](getnonindexableitemstatistics-operation.md) <br/> |<span data-ttu-id="9e44f-133">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-133">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-134">GetSearchableMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-134">GetSearchableMailboxes operation</span></span>](getsearchablemailboxes-operation.md) <br/> |<span data-ttu-id="9e44f-135">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-135">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-136">SearchMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-136">SearchMailboxes operation</span></span>](searchmailboxes-operation.md) <br/> |<span data-ttu-id="9e44f-137">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-137">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-138">SetHoldOnMailboxes 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-138">SetHoldOnMailboxes operation</span></span>](setholdonmailboxes-operation.md) <br/> |<span data-ttu-id="9e44f-139">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-139">Exchange 2013</span></span>  <br/> |
   
## <a name="exchange-mailbox-data-operations"></a><span data-ttu-id="9e44f-140">Exchange 邮箱数据操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-140">Exchange mailbox data operations</span></span>
<span data-ttu-id="9e44f-141"><a name="bk_Exchange_mailbox_data"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-141"><a name="bk_Exchange_mailbox_data"> </a></span></span>

<span data-ttu-id="9e44f-142">Exchange 邮箱数据操作使客户端能够处理和组织项目、文件夹和附件，以及不明确的名称解析和通讯组列表扩展。</span><span class="sxs-lookup"><span data-stu-id="9e44f-142">The Exchange mailbox data operations enable clients to handle and organize items, folders, and attachments, as well as ambiguous name resolution and distribution list expansion.</span></span> <span data-ttu-id="9e44f-143">Exchange 邮箱数据操作包括项目、文件夹、附件和实用工具操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-143">Exchange mailbox data operations include item, folder, attachment, and utilities operations.</span></span>
  
<span data-ttu-id="9e44f-144">下表列出了 Exchange 邮箱数据操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-144">The following table lists the Exchange mailbox data operations.</span></span>
  
|<span data-ttu-id="9e44f-145">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-145">**Operation name**</span></span>|<span data-ttu-id="9e44f-146">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-146">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-147">ArchiveItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-147">ArchiveItem operation</span></span>](archiveitem-operation.md) <br/> |<span data-ttu-id="9e44f-148">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-148">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-149">CreateItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-149">CreateItem operation</span></span>](createitem-operation.md) <br/> |<span data-ttu-id="9e44f-150">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-150">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-151">CopyItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-151">CopyItem operation</span></span>](copyitem-operation.md) <br/> |<span data-ttu-id="9e44f-152">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-152">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-153">DeleteItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-153">DeleteItem operation</span></span>](deleteitem-operation.md) <br/> |<span data-ttu-id="9e44f-154">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-154">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-155">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-155">FindItem operation</span></span>](finditem-operation.md) <br/> |<span data-ttu-id="9e44f-156">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-156">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-157">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-157">GetItem operation</span></span>](getitem-operation.md) <br/> |<span data-ttu-id="9e44f-158">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-158">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-159">MarkAllItemsAsRead 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-159">MarkAllItemsAsRead operation</span></span>](markallitemsasread-operation.md) <br/> |<span data-ttu-id="9e44f-160">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-160">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-161">MoveItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-161">MoveItem operation</span></span>](moveitem-operation.md) <br/> |<span data-ttu-id="9e44f-162">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-162">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-163">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-163">SendItem operation</span></span>](senditem-operation.md) <br/> |<span data-ttu-id="9e44f-164">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-164">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-165">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-165">UpdateItem operation</span></span>](updateitem-operation.md) <br/> |<span data-ttu-id="9e44f-166">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-166">Exchange 2007</span></span>  <br/> |
   
<span data-ttu-id="9e44f-167">下表列出了 Exchange 邮箱数据文件夹操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-167">The following table lists the Exchange mailbox data folder operations.</span></span>
  
|<span data-ttu-id="9e44f-168">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-168">**Operation name**</span></span>|<span data-ttu-id="9e44f-169">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-169">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-170">CreateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-170">CreateFolder operation</span></span>](createfolder-operation.md) <br/> |<span data-ttu-id="9e44f-171">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-171">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-172">CreateFolderPath 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-172">CreateFolderPath operation</span></span>](createfolderpath-operation.md) <br/> |<span data-ttu-id="9e44f-173">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-173">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-174">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-174">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md) <br/> |<span data-ttu-id="9e44f-175">Exchange 2007。</span><span class="sxs-lookup"><span data-stu-id="9e44f-175">Exchange 2007.</span></span> <span data-ttu-id="9e44f-176">此功能已在从 Exchange 2010 开始的 Exchange 版本中 deemphasized。</span><span class="sxs-lookup"><span data-stu-id="9e44f-176">This functionality has been deemphasized in versions of Exchange starting with Exchange 2010.</span></span> <span data-ttu-id="9e44f-177">有关如何迁移到使用保留标记和邮件记录管理策略的详细信息，请参阅[从托管文件夹迁移](https://technet.microsoft.com/library/dd298032%28v=exchg.141%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9e44f-177">For more information about how to migrate to using retention tags and policies for messaging records management, see [Migrate from Managed Folders](https://technet.microsoft.com/library/dd298032%28v=exchg.141%29.aspx).</span></span>  <br/> |
|[<span data-ttu-id="9e44f-178">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-178">CopyFolder operation</span></span>](copyfolder-operation.md) <br/> |<span data-ttu-id="9e44f-179">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-179">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-180">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-180">DeleteFolder operation</span></span>](deletefolder-operation.md) <br/> |<span data-ttu-id="9e44f-181">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-181">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-182">EmptyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-182">EmptyFolder operation</span></span>](emptyfolder-operation.md) <br/> |<span data-ttu-id="9e44f-183">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-183">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-184">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-184">FindFolder operation</span></span>](findfolder-operation.md) <br/> |<span data-ttu-id="9e44f-185">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-185">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-186">GetFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-186">GetFolder operation</span></span>](getfolder-operation.md) <br/> |<span data-ttu-id="9e44f-187">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-187">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-188">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-188">MoveFolder operation</span></span>](movefolder-operation.md) <br/> |<span data-ttu-id="9e44f-189">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-189">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-190">UpdateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-190">UpdateFolder operation</span></span>](updatefolder-operation.md) <br/> |<span data-ttu-id="9e44f-191">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-191">Exchange 2007</span></span>  <br/> |
   
<span data-ttu-id="9e44f-192">下表列出了 Exchange 邮箱数据附件操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-192">The following table lists the Exchange mailbox data attachment operations.</span></span>
  
|<span data-ttu-id="9e44f-193">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-193">**Operation name**</span></span>|<span data-ttu-id="9e44f-194">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-194">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-195">CreateAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-195">CreateAttachment operation</span></span>](createattachment-operation.md) <br/> |<span data-ttu-id="9e44f-196">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-196">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-197">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-197">GetAttachment operation</span></span>](getattachment-operation.md) <br/> |<span data-ttu-id="9e44f-198">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-198">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-199">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-199">DeleteAttachment operation</span></span>](deleteattachment-operation.md) <br/> |<span data-ttu-id="9e44f-200">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-200">Exchange 2007</span></span>  <br/> |
   
<span data-ttu-id="9e44f-201">下表列出了 Exchange 邮箱提醒操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-201">The following table lists the Exchange mailbox reminder operations.</span></span>
  
|<span data-ttu-id="9e44f-202">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-202">**Operation name**</span></span>|<span data-ttu-id="9e44f-203">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-203">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-204">GetReminders 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-204">GetReminders operation</span></span>](getreminders-operation.md) <br/> |<span data-ttu-id="9e44f-205">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-205">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-206">PerformReminderAction 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-206">PerformReminderAction operation</span></span>](performreminderaction-operation.md) <br/> |<span data-ttu-id="9e44f-207">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-207">Exchange 2013</span></span>  <br/> |
   
<span data-ttu-id="9e44f-208">下表列出了 Exchange 邮箱数据对话操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-208">The following table lists the Exchange mailbox data conversation operations.</span></span>
  
|<span data-ttu-id="9e44f-209">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-209">**Operation name**</span></span>|<span data-ttu-id="9e44f-210">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-210">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-211">ApplyConversationAction 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-211">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md) <br/> |<span data-ttu-id="9e44f-212">Exchange 2010 Service Pack 1 （SP1）</span><span class="sxs-lookup"><span data-stu-id="9e44f-212">Exchange 2010 Service Pack 1 (SP1)</span></span>  <br/> |
|[<span data-ttu-id="9e44f-213">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-213">FindConversation operation</span></span>](findconversation-operation.md) <br/> |<span data-ttu-id="9e44f-214">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-214">Exchange 2010 SP1</span></span>  <br/> |
|[<span data-ttu-id="9e44f-215">GetConversationItems 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-215">GetConversationItems operation</span></span>](getconversationitems-operation.md) <br/> |<span data-ttu-id="9e44f-216">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-216">Exchange 2013</span></span>  <br/> |
   
<span data-ttu-id="9e44f-217">下表列出了 Exchange 邮箱数据实用程序操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-217">The following table lists the Exchange mailbox data utilities operations.</span></span>
  
|<span data-ttu-id="9e44f-218">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-218">**Operation name**</span></span>|<span data-ttu-id="9e44f-219">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-219">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-220">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-220">ConvertId operation</span></span>](convertid-operation.md) <br/> |<span data-ttu-id="9e44f-221">Exchange 2007 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="9e44f-221">Exchange 2007 Service Pack 1</span></span>  <br/> |
|[<span data-ttu-id="9e44f-222">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-222">ExpandDL operation</span></span>](expanddl-operation.md) <br/> |<span data-ttu-id="9e44f-223">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-223">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-224">GetUserPhoto 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-224">GetUserPhoto operation</span></span>](getuserphoto-operation.md) <br/> |<span data-ttu-id="9e44f-225">Exchange 2013。</span><span class="sxs-lookup"><span data-stu-id="9e44f-225">Exchange 2013.</span></span> <span data-ttu-id="9e44f-226">此操作同时具有 REST 和 SOAP 实现。</span><span class="sxs-lookup"><span data-stu-id="9e44f-226">This operation has both a REST and a SOAP implementation.</span></span>  <br/> |
|[<span data-ttu-id="9e44f-227">MarkAsJunk 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-227">MarkAsJunk operation</span></span>](markasjunk-operation.md) <br/> |<span data-ttu-id="9e44f-228">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-228">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-229">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-229">ResolveNames operation</span></span>](resolvenames-operation.md) <br/> |<span data-ttu-id="9e44f-230">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-230">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-231">GetPasswordExpirationDate 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-231">GetPasswordExpirationDate operation</span></span>](getpasswordexpirationdate-operation.md) <br/> |<span data-ttu-id="9e44f-232">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-232">Exchange 2010 SP1</span></span>  <br/> |
   
## <a name="availability-operations"></a><span data-ttu-id="9e44f-233">可用性操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-233">Availability operations</span></span>
<span data-ttu-id="9e44f-234"><a name="bk_Availability"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-234"><a name="bk_Availability"> </a></span></span>

<span data-ttu-id="9e44f-235">可用性操作通过提供更安全、最新且丰富的忙/闲信息来改进日历和忙/闲共享体验。</span><span class="sxs-lookup"><span data-stu-id="9e44f-235">The availability operations improve the calendar and free/busy sharing experience by providing more secure, up-to-date, and rich free/busy information.</span></span> <span data-ttu-id="9e44f-236">闲/忙数据是安排会议的关键因素。</span><span class="sxs-lookup"><span data-stu-id="9e44f-236">Free/busy data is a critical component of scheduling meetings.</span></span> <span data-ttu-id="9e44f-237">可用性操作为有效的日程安排提供了可靠的基础。</span><span class="sxs-lookup"><span data-stu-id="9e44f-237">The availability operations provide a reliable foundation for effective scheduling.</span></span> 
  
<span data-ttu-id="9e44f-238">下表列出了可用性操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-238">The following table lists the availability operations.</span></span>
  
|<span data-ttu-id="9e44f-239">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-239">**Operation name**</span></span>|<span data-ttu-id="9e44f-240">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-240">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-241">GetUserAvailability 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-241">GetUserAvailability operation</span></span>](getuseravailability-operation.md) <br/> |<span data-ttu-id="9e44f-242">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-242">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-243">GetRoomLists 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-243">GetRoomLists operation</span></span>](getroomlists-operation.md) <br/> |<span data-ttu-id="9e44f-244">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-244">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-245">GetRooms 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-245">GetRooms operation</span></span>](getrooms-operation.md) <br/> |<span data-ttu-id="9e44f-246">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-246">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-247">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-247">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md) <br/> |<span data-ttu-id="9e44f-248">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-248">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-249">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-249">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md) <br/> |<span data-ttu-id="9e44f-250">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-250">Exchange 2007</span></span>  <br/> |
   
## <a name="bulk-transfer-operations"></a><span data-ttu-id="9e44f-251">批量转移操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-251">Bulk transfer operations</span></span>
<span data-ttu-id="9e44f-252"><a name="bk_bulk_transfer"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-252"><a name="bk_bulk_transfer"> </a></span></span>

<span data-ttu-id="9e44f-253">批量传输操作使客户端能够将邮件流入或传出邮箱。</span><span class="sxs-lookup"><span data-stu-id="9e44f-253">The bulk transfer operations enable clients to stream items into and out of a mailbox.</span></span> 
  
<span data-ttu-id="9e44f-254">下表列出批量转移操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-254">The following table lists the bulk transfer operations.</span></span>
  
|<span data-ttu-id="9e44f-255">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-255">**Operation name**</span></span>|<span data-ttu-id="9e44f-256">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-256">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-257">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-257">UploadItems operation</span></span>](uploaditems-operation.md) <br/> |<span data-ttu-id="9e44f-258">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-258">Exchange 2010 SP1</span></span>  <br/> |
|[<span data-ttu-id="9e44f-259">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-259">ExportItems operation</span></span>](exportitems-operation.md) <br/> |<span data-ttu-id="9e44f-260">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-260">Exchange 2010 SP1</span></span>  <br/> |
   
## <a name="delegate-management-operations"></a><span data-ttu-id="9e44f-261">委派管理操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-261">Delegate management operations</span></span>
<span data-ttu-id="9e44f-262"><a name="bk_delegate_management"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-262"><a name="bk_delegate_management"> </a></span></span>

<span data-ttu-id="9e44f-263">代理管理操作使客户端能够在其邮箱中添加、获取、更新和删除委派。</span><span class="sxs-lookup"><span data-stu-id="9e44f-263">The delegate management operations enable clients to add, get, update, and remove delegates from their mailboxes.</span></span> 
  
<span data-ttu-id="9e44f-264">下表列出了代理管理操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-264">The following table lists the delegate management operations.</span></span>
  
|<span data-ttu-id="9e44f-265">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-265">**Operation name**</span></span>|<span data-ttu-id="9e44f-266">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-266">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-267">AddDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-267">AddDelegate operation</span></span>](adddelegate-operation.md) <br/> |<span data-ttu-id="9e44f-268">Exchange 2007 Service Pack 1 （SP1）</span><span class="sxs-lookup"><span data-stu-id="9e44f-268">Exchange 2007 Service Pack 1 (SP1)</span></span>  <br/> |
|[<span data-ttu-id="9e44f-269">GetDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-269">GetDelegate operation</span></span>](getdelegate-operation.md) <br/> |<span data-ttu-id="9e44f-270">Exchange 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-270">Exchange 2007 SP1</span></span>  <br/> |
|[<span data-ttu-id="9e44f-271">UpdateDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-271">UpdateDelegate operation</span></span>](updatedelegate-operation.md) <br/> |<span data-ttu-id="9e44f-272">Exchange 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-272">Exchange 2007 SP1</span></span>  <br/> |
|[<span data-ttu-id="9e44f-273">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-273">RemoveDelegate operation</span></span>](removedelegate-operation.md) <br/> |<span data-ttu-id="9e44f-274">Exchange 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-274">Exchange 2007 SP1</span></span>  <br/> |
   
## <a name="inbox-rules-operations"></a><span data-ttu-id="9e44f-275">收件箱规则操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-275">Inbox rules operations</span></span>
<span data-ttu-id="9e44f-276"><a name="bk_inbox_rules"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-276"><a name="bk_inbox_rules"> </a></span></span>

<span data-ttu-id="9e44f-277">"收件箱规则" 操作使客户端可以获取收件箱规则并更新服务器上的邮件。</span><span class="sxs-lookup"><span data-stu-id="9e44f-277">The Inbox rules operations enable clients to get Inbox rules and update them for messages on the server.</span></span> <span data-ttu-id="9e44f-278">收件箱规则是条件和关联操作的集合，使客户端能够在邮件传递到文件夹时自动对邮件进行组织、分类和操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-278">Inbox rules are sets of conditions and associated actions that enable clients to automatically organize, categorize, and act on messages as the messages are delivered to a folder.</span></span> 
  
<span data-ttu-id="9e44f-279">下表列出了收件箱规则操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-279">The following table lists the Inbox rules operations.</span></span>
  
|<span data-ttu-id="9e44f-280">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-280">**Operation name**</span></span>|<span data-ttu-id="9e44f-281">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-281">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-282">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-282">GetInboxRules operation</span></span>](getinboxrules-operation.md) <br/> |<span data-ttu-id="9e44f-283">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-283">Exchange 2010 SP1</span></span>  <br/> |
|[<span data-ttu-id="9e44f-284">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-284">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md) <br/> |<span data-ttu-id="9e44f-285">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-285">Exchange 2010 SP1</span></span>  <br/> |
   
## <a name="mail-app-management-operations"></a><span data-ttu-id="9e44f-286">邮件应用程序管理操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-286">Mail app management operations</span></span>
<span data-ttu-id="9e44f-287"><a name="bk_mail_apps"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-287"><a name="bk_mail_apps"> </a></span></span>

<span data-ttu-id="9e44f-288">邮件应用程序管理操作使您能够管理 Outlook 的邮件应用程序。</span><span class="sxs-lookup"><span data-stu-id="9e44f-288">The mail app management operations enable you to manage mail apps for Outlook.</span></span> <span data-ttu-id="9e44f-289">您可以使用这些操作来安装、卸载、禁用和获取适用于 Outlook Web App 和 Outlook 2013 的邮件应用程序的相关信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-289">You can use these operations to install, uninstall, disable, and get information about mail apps that are available for Outlook Web App and Outlook 2013.</span></span>
  
<span data-ttu-id="9e44f-290">下表列出了邮件应用程序管理操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-290">The following table lists the mail app management operations.</span></span>
  
|<span data-ttu-id="9e44f-291">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-291">**Operation name**</span></span>|<span data-ttu-id="9e44f-292">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-292">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-293">DisableApp 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-293">DisableApp operation</span></span>](disableapp-operation.md) <br/> |<span data-ttu-id="9e44f-294">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-294">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-295">Getappmanifests 已操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-295">GetAppManifests operation</span></span>](getappmanifests-operation.md) <br/> |<span data-ttu-id="9e44f-296">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-296">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-297">GetAppMarketplaceUrl 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-297">GetAppMarketplaceUrl operation</span></span>](getappmarketplaceurl-operation.md) <br/> |<span data-ttu-id="9e44f-298">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-298">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-299">GetClientAccessToken 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-299">GetClientAccessToken operation</span></span>](getclientaccesstoken-operation.md) <br/> |<span data-ttu-id="9e44f-300">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-300">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-301">InstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-301">InstallApp operation</span></span>](installapp-operation.md) <br/> |<span data-ttu-id="9e44f-302">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-302">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-303">UninstallApp 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-303">UninstallApp operation</span></span>](uninstallapp-operation.md) <br/> |<span data-ttu-id="9e44f-304">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-304">Exchange 2013</span></span>  <br/> |
   
## <a name="mail-tips-operation"></a><span data-ttu-id="9e44f-305">邮件提示操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-305">Mail tips operation</span></span>
<span data-ttu-id="9e44f-306"><a name="bk_mail_tips"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-306"><a name="bk_mail_tips"> </a></span></span>

<span data-ttu-id="9e44f-307">通过邮件提示操作，客户端可以在作者撰写邮件时向服务器请求有关收件人邮箱的信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-307">The mail tips operation enables clients to request information from the server about recipient mailboxes when an author is composing a message.</span></span> <span data-ttu-id="9e44f-308">下表列出了邮件提示操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-308">The following table lists the mail tips operation.</span></span>
  
|<span data-ttu-id="9e44f-309">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-309">**Operation name**</span></span>|<span data-ttu-id="9e44f-310">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-310">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-311">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-311">GetMailTips operation</span></span>](getmailtips-operation.md) <br/> |<span data-ttu-id="9e44f-312">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-312">Exchange 2010</span></span>  <br/> |
   
## <a name="message-tracking-operations"></a><span data-ttu-id="9e44f-313">邮件跟踪操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-313">Message tracking operations</span></span>
<span data-ttu-id="9e44f-314"><a name="bk_message_tracking"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-314"><a name="bk_message_tracking"> </a></span></span>

<span data-ttu-id="9e44f-315">邮件跟踪操作使客户端能够查找符合指定条件的邮件，并在邮件跟踪报告中获取有关每封邮件的详细跟踪信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-315">The message tracking operations enable clients to find messages that meet specified criteria and to get detailed tracking information about each message in a message tracking report.</span></span> 
  
<span data-ttu-id="9e44f-316">下表列出了邮件跟踪操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-316">The following table lists the message tracking operations.</span></span>
  
|<span data-ttu-id="9e44f-317">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-317">**Operation name**</span></span>|<span data-ttu-id="9e44f-318">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-318">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-319">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-319">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md) <br/> |<span data-ttu-id="9e44f-320">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-320">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-321">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-321">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md) <br/> |<span data-ttu-id="9e44f-322">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-322">Exchange 2010</span></span>  <br/> |
   
## <a name="notification-operations"></a><span data-ttu-id="9e44f-323">通知操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-323">Notification operations</span></span>
<span data-ttu-id="9e44f-324"><a name="bk_notification"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-324"><a name="bk_notification"> </a></span></span>

<span data-ttu-id="9e44f-325">通知操作会将与项目和文件夹相关联的事件的客户端应用程序通知到指定的邮箱。</span><span class="sxs-lookup"><span data-stu-id="9e44f-325">The notification operations notify the client application of events that are associated with items and folders a specified mailbox.</span></span> <span data-ttu-id="9e44f-326">订阅模型可以是基于推送、基于请求的，也可以是基于流的。</span><span class="sxs-lookup"><span data-stu-id="9e44f-326">The subscription model can be push-based, pull-based, or streaming-based.</span></span> 
  
<span data-ttu-id="9e44f-327">下表列出了通知操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-327">The following table lists the notification operations.</span></span>
  
|<span data-ttu-id="9e44f-328">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-328">**Operation name**</span></span>|<span data-ttu-id="9e44f-329">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-329">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-330">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-330">GetEvents operation</span></span>](getevents-operation.md) <br/> |<span data-ttu-id="9e44f-331">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-331">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-332">GetStreamingEvents 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-332">GetStreamingEvents operation</span></span>](getstreamingevents-operation.md) <br/> |<span data-ttu-id="9e44f-333">Exchange 2010 SP1</span><span class="sxs-lookup"><span data-stu-id="9e44f-333">Exchange 2010 SP1</span></span>  <br/> |
|[<span data-ttu-id="9e44f-334">订阅操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-334">Subscribe operation</span></span>](subscribe-operation.md) <br/> |<span data-ttu-id="9e44f-335">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-335">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-336">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-336">Unsubscribe operation</span></span>](unsubscribe-operation.md) <br/> |<span data-ttu-id="9e44f-337">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-337">Exchange 2007</span></span>  <br/> |
   
## <a name="persona-operations"></a><span data-ttu-id="9e44f-338">角色操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-338">Persona operations</span></span>
<span data-ttu-id="9e44f-339"><a name="bk_personas"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-339"><a name="bk_personas"> </a></span></span>

<span data-ttu-id="9e44f-340">角色操作提供了一个接口，用于查找和获取有关链接的联系人的信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-340">The persona operations provide an interface to find and get information about a linked contact.</span></span> <span data-ttu-id="9e44f-341">下表列出了角色操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-341">The following table lists the persona operations.</span></span>
  
|<span data-ttu-id="9e44f-342">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-342">**Operation name**</span></span>|<span data-ttu-id="9e44f-343">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-343">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-344">FindPeople 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-344">FindPeople operation</span></span>](findpeople-operation.md) <br/> |<span data-ttu-id="9e44f-345">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-345">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-346">GetPersona 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-346">GetPersona operation</span></span>](getpersona-operation.md) <br/> |<span data-ttu-id="9e44f-347">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-347">Exchange 2013</span></span>  <br/> |
   
## <a name="retention-policy-operation"></a><span data-ttu-id="9e44f-348">保留策略操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-348">Retention policy operation</span></span>
<span data-ttu-id="9e44f-349"><a name="bk_retention_policy"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-349"><a name="bk_retention_policy"> </a></span></span>

<span data-ttu-id="9e44f-350">保留策略操作提供了链接到用户的保留策略的所有保留标记的列表。</span><span class="sxs-lookup"><span data-stu-id="9e44f-350">The retention policy operation provides a list of all the retention tags that are linked to a user's retention policy.</span></span> 
  
<span data-ttu-id="9e44f-351">下表列出了保留策略操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-351">The following table lists the retention policy operation.</span></span>
  
|<span data-ttu-id="9e44f-352">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-352">**Operation name**</span></span>|<span data-ttu-id="9e44f-353">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-353">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-354">GetUserRetentionPolicyTags 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-354">GetUserRetentionPolicyTags operation</span></span>](getuserretentionpolicytags-operation.md) <br/> |<span data-ttu-id="9e44f-355">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-355">Exchange 2013</span></span>  <br/> |
   
## <a name="service-configuration-operation"></a><span data-ttu-id="9e44f-356">服务配置操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-356">Service configuration operation</span></span>
<span data-ttu-id="9e44f-357"><a name="bk_service_config"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-357"><a name="bk_service_config"> </a></span></span>

<span data-ttu-id="9e44f-358">服务配置操作使客户端能够获取统一消息、保护规则、策略提示和邮件提示服务的配置信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-358">The service configuration operation enables clients to get configuration information for the Unified Messaging, Protection Rules, Policy Tips, and Mail Tips services.</span></span> 
  
<span data-ttu-id="9e44f-359">下表列出了服务配置操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-359">The following table lists the service configuration operation.</span></span>
  
|<span data-ttu-id="9e44f-360">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-360">**Operation name**</span></span>|<span data-ttu-id="9e44f-361">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-361">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-362">GetServiceConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-362">GetServiceConfiguration operation</span></span>](getserviceconfiguration-operation.md) <br/> |<span data-ttu-id="9e44f-363">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-363">Exchange 2010</span></span>  <br/> |
   
## <a name="sharing-operations"></a><span data-ttu-id="9e44f-364">共享操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-364">Sharing operations</span></span>
<span data-ttu-id="9e44f-365"><a name="bk_sharing"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-365"><a name="bk_sharing"> </a></span></span>

<span data-ttu-id="9e44f-366">共享操作使客户端可以共享日历数据和联系人数据。</span><span class="sxs-lookup"><span data-stu-id="9e44f-366">The sharing operations enable clients to share calendar data and contacts data.</span></span> 
  
<span data-ttu-id="9e44f-367">下表列出了共享操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-367">The following table lists the sharing operations.</span></span>
  
|<span data-ttu-id="9e44f-368">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-368">**Operation name**</span></span>|<span data-ttu-id="9e44f-369">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-369">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-370">CreateItem （AcceptSharingInvitation）</span><span class="sxs-lookup"><span data-stu-id="9e44f-370">CreateItem (AcceptSharingInvitation)</span></span>](createitem-acceptsharinginvitation.md) <br/> |<span data-ttu-id="9e44f-371">Exchange 2010。</span><span class="sxs-lookup"><span data-stu-id="9e44f-371">Exchange 2010.</span></span> <span data-ttu-id="9e44f-372">尽管**CreateItem**操作适用于所有的 EWS 版本，但**AcceptSharingInvitation**响应对象仅适用于从 Exchange 2010 开始的 EXCHANGE 版本中的 EWS。</span><span class="sxs-lookup"><span data-stu-id="9e44f-372">Although the **CreateItem** operation is applicable to all versions of EWS, the **AcceptSharingInvitation** response object is only applicable to EWS in versions of Exchange starting with Exchange 2010.</span></span>  <br/> |
|[<span data-ttu-id="9e44f-373">GetSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-373">GetSharingFolder operation</span></span>](getsharingfolder-operation.md) <br/> |<span data-ttu-id="9e44f-374">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-374">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-375">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-375">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md) <br/> |<span data-ttu-id="9e44f-376">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-376">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-377">RefreshSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-377">RefreshSharingFolder operation</span></span>](refreshsharingfolder-operation.md) <br/> |<span data-ttu-id="9e44f-378">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-378">Exchange 2010</span></span>  <br/> |
   
## <a name="synchronization-operations"></a><span data-ttu-id="9e44f-379">同步操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-379">Synchronization operations</span></span>
<span data-ttu-id="9e44f-380"><a name="bk_synchronization"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-380"><a name="bk_synchronization"> </a></span></span>

<span data-ttu-id="9e44f-381">同步操作提供用户文件夹和项目的单向同步缓存副本。</span><span class="sxs-lookup"><span data-stu-id="9e44f-381">The synchronization operations provide a one-way synchronized cached copy of a user's folders and items.</span></span> 
  
<span data-ttu-id="9e44f-382">下表列出了同步操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-382">The following table lists the synchronization operations.</span></span>
  
|<span data-ttu-id="9e44f-383">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-383">**Operation name**</span></span>|<span data-ttu-id="9e44f-384">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-384">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-385">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-385">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md) <br/> |<span data-ttu-id="9e44f-386">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-386">Exchange 2007</span></span>  <br/> |
|[<span data-ttu-id="9e44f-387">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-387">SyncFolderItems operation</span></span>](syncfolderitems-operation.md) <br/> |<span data-ttu-id="9e44f-388">Exchange 2007</span><span class="sxs-lookup"><span data-stu-id="9e44f-388">Exchange 2007</span></span>  <br/> |
   
## <a name="time-zone-operation"></a><span data-ttu-id="9e44f-389">时区操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-389">Time zone operation</span></span>
<span data-ttu-id="9e44f-390"><a name="bk_timezone"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-390"><a name="bk_timezone"> </a></span></span>

<span data-ttu-id="9e44f-391">时区操作使客户端可以获取服务器支持的时区定义的列表。</span><span class="sxs-lookup"><span data-stu-id="9e44f-391">The time zone operation enables clients to get a list of time zone definitions that are supported by the server.</span></span> 
  
<span data-ttu-id="9e44f-392">下表列出了时区操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-392">The following table lists the time zone operation.</span></span>
  
|<span data-ttu-id="9e44f-393">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-393">**Operation name**</span></span>|<span data-ttu-id="9e44f-394">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-394">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-395">GetServerTimeZones 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-395">GetServerTimeZones operation</span></span>](getservertimezones-operation.md) <br/> |<span data-ttu-id="9e44f-396">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-396">Exchange 2010</span></span>  <br/> |
   
## <a name="unified-messaging-operations"></a><span data-ttu-id="9e44f-397">统一消息操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-397">Unified Messaging operations</span></span>
<span data-ttu-id="9e44f-398"><a name="bk_um"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-398"><a name="bk_um"> </a></span></span>

<span data-ttu-id="9e44f-399">统一消息操作使客户端能够读取有关统一消息属性的信息，并通过电话播放语音邮件消息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-399">The Unified Messaging operations enable clients to read information about Unified Messaging properties and to play voice mail messages over the phone.</span></span> 
  
<span data-ttu-id="9e44f-400">下表列出了统一消息操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-400">The following table lists the Unified Messaging operations.</span></span>
  
|<span data-ttu-id="9e44f-401">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-401">**Operation name**</span></span>|<span data-ttu-id="9e44f-402">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-402">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-403">DisconnectPhoneCall 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-403">DisconnectPhoneCall operation</span></span>](disconnectphonecall-operation.md) <br/> |<span data-ttu-id="9e44f-404">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-404">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-405">GetPhoneCallInformation 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-405">GetPhoneCallInformation operation</span></span>](getphonecallinformation-operation.md) <br/> |<span data-ttu-id="9e44f-406">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-406">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-407">PlayOnPhone 操作（EWS）</span><span class="sxs-lookup"><span data-stu-id="9e44f-407">PlayOnPhone operation (EWS)</span></span>](playonphone-operation-ews.md) <br/> |<span data-ttu-id="9e44f-408">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-408">Exchange 2010</span></span>  <br/> |
   
<span data-ttu-id="9e44f-409">使用[GetServiceConfiguration 操作](getserviceconfiguration-operation.md)可获取邮箱的统一消息配置信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-409">Use the [GetServiceConfiguration operation](getserviceconfiguration-operation.md) to get the Unified Messaging configuration information for a mailbox.</span></span> <span data-ttu-id="9e44f-410">对面向 Exchange 2007 的统一消息应用程序使用统一消息 web 服务。</span><span class="sxs-lookup"><span data-stu-id="9e44f-410">Use the Unified Messaging web service for Unified Messaging applications that target Exchange 2007.</span></span> <span data-ttu-id="9e44f-411">有关详细信息，请参阅[Exchange 统一消息 web 服务参考](unified-messaging-web-service-reference-for-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="9e44f-411">For more information, see [Unified Messaging web service reference for Exchange](unified-messaging-web-service-reference-for-exchange.md).</span></span>
  
## <a name="unified-contact-store-operations"></a><span data-ttu-id="9e44f-412">统一联系人存储操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-412">Unified Contact Store operations</span></span>
<span data-ttu-id="9e44f-413"><a name="bk_ucs"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-413"><a name="bk_ucs"> </a></span></span>

<span data-ttu-id="9e44f-414">统一联系人存储跨 Office 产品提供一致的联系人体验，并充当第三方应用程序的集成点以使用同一联系人存储。</span><span class="sxs-lookup"><span data-stu-id="9e44f-414">The Unified Contact Store provides a consistent contact experience across Office products and acts as an integration point for third-party applications to use the same contact store.</span></span> <span data-ttu-id="9e44f-415">它使用户和应用程序能够存储、管理和访问联系人信息，并使其在 Lync、Exchange 2013、Outlook、Outlook Web App 和任何其他实现对统一联系人存储的访问权限的应用程序之间全局可用。</span><span class="sxs-lookup"><span data-stu-id="9e44f-415">It enables users and applications to store, manage, and access contact information and make it available globally among Lync, Exchange 2013, Outlook, Outlook Web App, and any other application that implements access to the Unified Contact Store.</span></span> <span data-ttu-id="9e44f-416">Exchange 是统一联系人存储区体验的内容存储区。</span><span class="sxs-lookup"><span data-stu-id="9e44f-416">Exchange is the content store for the Unified Contact Store experience.</span></span>
  
<span data-ttu-id="9e44f-417">下表列出了统一的联系人存储操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-417">The following table lists the Unified Contact Store operations.</span></span>
  
|<span data-ttu-id="9e44f-418">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-418">**Operation name**</span></span>|<span data-ttu-id="9e44f-419">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-419">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-420">AddNewImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-420">AddNewImContactToGroup operation</span></span>](addnewimcontacttogroup-operation.md) <br/> |<span data-ttu-id="9e44f-421">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-421">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-422">AddImContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-422">AddImContactToGroup operation</span></span>](addimcontacttogroup-operation.md) <br/> |<span data-ttu-id="9e44f-423">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-423">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-424">AddImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-424">AddImGroup operation</span></span>](addimgroup-operation.md) <br/> |<span data-ttu-id="9e44f-425">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-425">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-426">AddNewTelUriContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-426">AddNewTelUriContactToGroup operation</span></span>](addnewteluricontacttogroup-operation.md) <br/> |<span data-ttu-id="9e44f-427">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-427">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-428">AddDistributionGroupToImList 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-428">AddDistributionGroupToImList operation</span></span>](adddistributiongrouptoimlist-operation.md) <br/> |<span data-ttu-id="9e44f-429">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-429">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-430">GetImItemList 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-430">GetImItemList operation</span></span>](getimitemlist-operation.md) <br/> |<span data-ttu-id="9e44f-431">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-431">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-432">GetImItems 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-432">GetImItems operation</span></span>](getimitems-operation.md) <br/> |<span data-ttu-id="9e44f-433">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-433">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-434">RemoveContactFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-434">RemoveContactFromImList operation</span></span>](removecontactfromimlist-operation.md) <br/> |<span data-ttu-id="9e44f-435">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-435">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-436">RemoveImContactFromGroup 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-436">RemoveImContactFromGroup operation</span></span>](removeimcontactfromgroup-operation.md) <br/> |<span data-ttu-id="9e44f-437">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-437">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-438">RemoveDistributionGroupFromImList 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-438">RemoveDistributionGroupFromImList operation</span></span>](removedistributiongroupfromimlist-operation.md) <br/> |<span data-ttu-id="9e44f-439">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-439">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-440">RemoveImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-440">RemoveImGroup operation</span></span>](removeimgroup-operation.md) <br/> |<span data-ttu-id="9e44f-441">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-441">Exchange 2013</span></span>  <br/> |
|[<span data-ttu-id="9e44f-442">SetImGroup 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-442">SetImGroup operation</span></span>](setimgroup-operation.md) <br/> |<span data-ttu-id="9e44f-443">Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="9e44f-443">Exchange 2013</span></span>  <br/> |
   
## <a name="user-configuration-operations"></a><span data-ttu-id="9e44f-444">用户配置操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-444">User configuration operations</span></span>
<span data-ttu-id="9e44f-445"><a name="bk_user_config"> </a></span><span class="sxs-lookup"><span data-stu-id="9e44f-445"><a name="bk_user_config"> </a></span></span>

<span data-ttu-id="9e44f-446">用户配置操作使客户端能够创建、删除、获取和更新用户配置信息。</span><span class="sxs-lookup"><span data-stu-id="9e44f-446">The user configuration operations enable clients to create, delete, get, and update user configuration information.</span></span> 
  
<span data-ttu-id="9e44f-447">下表列出了用户配置操作。</span><span class="sxs-lookup"><span data-stu-id="9e44f-447">The following table lists the user configuration operations.</span></span>
  
|<span data-ttu-id="9e44f-448">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="9e44f-448">**Operation name**</span></span>|<span data-ttu-id="9e44f-449">**引入版本**</span><span class="sxs-lookup"><span data-stu-id="9e44f-449">**Introduced in**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e44f-450">CreateUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-450">CreateUserConfiguration operation</span></span>](createuserconfiguration-operation.md) <br/> |<span data-ttu-id="9e44f-451">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-451">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-452">DeleteUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-452">DeleteUserConfiguration operation</span></span>](deleteuserconfiguration-operation.md) <br/> |<span data-ttu-id="9e44f-453">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-453">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-454">GetUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-454">GetUserConfiguration operation</span></span>](getuserconfiguration-operation.md) <br/> |<span data-ttu-id="9e44f-455">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-455">Exchange 2010</span></span>  <br/> |
|[<span data-ttu-id="9e44f-456">UpdateUserConfiguration 操作</span><span class="sxs-lookup"><span data-stu-id="9e44f-456">UpdateUserConfiguration operation</span></span>](updateuserconfiguration-operation.md) <br/> |<span data-ttu-id="9e44f-457">Exchange 2010</span><span class="sxs-lookup"><span data-stu-id="9e44f-457">Exchange 2010</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e44f-458">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9e44f-458">See also</span></span>

- [<span data-ttu-id="9e44f-459">在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务</span><span class="sxs-lookup"><span data-stu-id="9e44f-459">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [<span data-ttu-id="9e44f-460">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="9e44f-460">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
- [<span data-ttu-id="9e44f-461">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="9e44f-461">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
    

