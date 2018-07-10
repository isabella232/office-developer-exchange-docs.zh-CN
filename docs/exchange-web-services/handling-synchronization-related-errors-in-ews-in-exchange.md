---
title: 在 Exchange 处理同步相关 EWS 中的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: 了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中同步相关的错误。
ms.openlocfilehash: 6de27d585e467d900941f34b2210877d17205502
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752720"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a><span data-ttu-id="fa1a6-103">在 Exchange 处理同步相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="fa1a6-103">Handling synchronization-related errors in EWS in Exchange</span></span>

<span data-ttu-id="fa1a6-104">了解如何处理您通过使用 EWS 的 EWS 托管 API 在 Exchange 开发的应用程序中同步相关的错误。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-104">Find out how to handle synchronization-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="fa1a6-105">如果您的应用程序同步项目和文件夹，您可能需要处理与同步相关的错误。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-105">If your application synchronizes items and folders, you might have to handle synchronization-related errors.</span></span> <span data-ttu-id="fa1a6-106">您可以处理这些错误在运行时，或者开发 EWS 应用程序时。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-106">You can handle these errors at runtime, or while you are developing your EWS application.</span></span> <span data-ttu-id="fa1a6-107">大部分这些错误的[ResponseCodeType](http://msdn.microsoft.com/zh-cn/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx)枚举中 EWS 托管 API 和[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)元素中 Exchange Web Services (EWS) 来定义。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-107">Most of these errors are defined by the [ResponseCodeType](http://msdn.microsoft.com/zh-cn/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) enumeration in the EWS Managed API, and the [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) element in Exchange Web Services (EWS).</span></span> 
  
<span data-ttu-id="fa1a6-108">**表 1。同步相关错误和如何处理它们**</span><span class="sxs-lookup"><span data-stu-id="fa1a6-108">**Table 1. Sync-related errors and how to handle them**</span></span>

|<span data-ttu-id="fa1a6-109">**Error**</span><span class="sxs-lookup"><span data-stu-id="fa1a6-109">**Error**</span></span>|<span data-ttu-id="fa1a6-110">**您尝试对时发生...**</span><span class="sxs-lookup"><span data-stu-id="fa1a6-110">**Occurs when you try to…**</span></span>|<span data-ttu-id="fa1a6-111">**处理它的...**</span><span class="sxs-lookup"><span data-stu-id="fa1a6-111">**Handle it by…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa1a6-112">ErrorInvalidSyncStateData</span><span class="sxs-lookup"><span data-stu-id="fa1a6-112">ErrorInvalidSyncStateData</span></span>  <br/> | <span data-ttu-id="fa1a6-113">通过使用无效的同步状态值同步项目或文件夹。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-113">Synchronize items or folders by using an invalid sync state value.</span></span>  <br/>  <span data-ttu-id="fa1a6-114">当您后续请求执行包含根文件夹排除在初始 SyncFolderHierarchy 请求中，根文件夹。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-114">Exclude a root folder in your initial SyncFolderHierarchy request, when your subsequent request does include a root folder.</span></span>  <br/>  <span data-ttu-id="fa1a6-115">使用在后续请求中的不同的根文件夹。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-115">Use different root folders in subsequent requests.</span></span>  <br/> | <span data-ttu-id="fa1a6-116">确保您要发送的匹配项的同步状态值同步状态返回的值以前同步过程中。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-116">Ensuring that the sync state value you are sending matches the sync state value returned during a previous synchronization.</span></span>  <br/>  <span data-ttu-id="fa1a6-117">确保您正在不发送的同步状态的文件夹层次结构当您尝试同步项时，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-117">Ensuring that you are not sending the sync state for the folder hierarchy when you attempt to sync items, and vice versa.</span></span>  <br/>  <span data-ttu-id="fa1a6-118">确保您正在发送正确的根文件夹的同步状态。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-118">Ensuring that you are sending the sync state for the correct root folder.</span></span>  <br/>  <span data-ttu-id="fa1a6-119">确保每个请求中，指定相同的根文件夹。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-119">Ensuring that the same root folder is specified in each request.</span></span>  <br/>  <span data-ttu-id="fa1a6-120">确保在上一个请求没有当前请求中包括根根文件夹时指定 null、 根文件夹。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-120">Ensuring that the previous request did not specify a root folder of null, while the current request includes a root folder of root.</span></span> <span data-ttu-id="fa1a6-121">Null 和根不是视为相同。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-121">Null and root are not treated the same.</span></span>  <br/> |
|<span data-ttu-id="fa1a6-122">ErrorSyncFolderNotFound</span><span class="sxs-lookup"><span data-stu-id="fa1a6-122">ErrorSyncFolderNotFound</span></span>  <br/> |<span data-ttu-id="fa1a6-123">同步子文件夹或找不到的服务器的文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-123">Synchronize subfolders or items in a folder that cannot be found on the server.</span></span>  <br/> |<span data-ttu-id="fa1a6-124">确保文件夹请求中指定的 ID 匹配从以前的同步响应中的服务器返回文件夹 ID。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-124">Ensuring that the folder ID specified in the request matches a folder ID returned from the server in a previous sync response.</span></span>  <br/> |
|<span data-ttu-id="fa1a6-125">ErrorTimeoutExpired</span><span class="sxs-lookup"><span data-stu-id="fa1a6-125">ErrorTimeoutExpired</span></span>  <br/> |<span data-ttu-id="fa1a6-126">发送太多的请求。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-126">Send too many requests.</span></span>  <br/> |<span data-ttu-id="fa1a6-127">限制为 10 个项目，每批次以避免获取[会限制](ews-throttling-in-exchange.md)您批次。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-127">Limiting your batches to 10 items per batch to avoid getting [throttled](ews-throttling-in-exchange.md).</span></span>  <br/> |
|[<span data-ttu-id="fa1a6-128">ServiceResponseException</span><span class="sxs-lookup"><span data-stu-id="fa1a6-128">ServiceResponseException</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="fa1a6-129">连接到 EWS 服务器处于脱机状态或没有连接问题。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-129">Connect to EWS when the server is offline or there is a problem with connectivity.</span></span>  <br/> |<span data-ttu-id="fa1a6-130">检查服务器连接和更高版本重试您的请求。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-130">Checking connectivity with the server and retrying your request later.</span></span> <span data-ttu-id="fa1a6-131">这可能是临时服务错误或网络错误。</span><span class="sxs-lookup"><span data-stu-id="fa1a6-131">This is likely a transient service error or network error.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa1a6-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa1a6-132">See also</span></span>


- [<span data-ttu-id="fa1a6-133">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="fa1a6-133">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    
- [<span data-ttu-id="fa1a6-134">使用 EWS 在 Exchange 同步文件夹</span><span class="sxs-lookup"><span data-stu-id="fa1a6-134">Synchronize folders by using EWS in Exchange</span></span>](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="fa1a6-135">使用 EWS 在 Exchange 同步的项目</span><span class="sxs-lookup"><span data-stu-id="fa1a6-135">Synchronize items by using EWS in Exchange</span></span>](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="fa1a6-136">ServiceResponseException</span><span class="sxs-lookup"><span data-stu-id="fa1a6-136">ServiceResponseException</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

