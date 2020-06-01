---
title: 在 Exchange 中处理 EWS 中与同步相关的错误
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0807b90-645a-4ea6-aee1-96828df14be0
description: 了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中与同步相关的错误。
ms.openlocfilehash: f62937ec444d64b0b358581371f1260f565215b3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455938"
---
# <a name="handling-synchronization-related-errors-in-ews-in-exchange"></a><span data-ttu-id="8f4cd-103">在 Exchange 中处理 EWS 中与同步相关的错误</span><span class="sxs-lookup"><span data-stu-id="8f4cd-103">Handling synchronization-related errors in EWS in Exchange</span></span>

<span data-ttu-id="8f4cd-104">了解如何处理通过在 Exchange 中使用 EWS 托管 API 或 EWS 开发的应用程序中与同步相关的错误。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-104">Find out how to handle synchronization-related errors in applications that you develop by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="8f4cd-105">如果您的应用程序同步项目和文件夹，则您可能需要处理与同步相关的错误。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-105">If your application synchronizes items and folders, you might have to handle synchronization-related errors.</span></span> <span data-ttu-id="8f4cd-106">您可以处理这些错误在运行时，或者开发 EWS 应用程序时。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-106">You can handle these errors at runtime, or while you are developing your EWS application.</span></span> <span data-ttu-id="8f4cd-107">其中大多数错误是由 EWS 托管 API 中的[ResponseCodeType](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx)枚举和 Exchange Web 服务（EWS）中的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)元素定义的。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-107">Most of these errors are defined by the [ResponseCodeType](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) enumeration in the EWS Managed API, and the [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) element in Exchange Web Services (EWS).</span></span> 
  
<span data-ttu-id="8f4cd-108">**表1。与同步相关的错误及其处理方法**</span><span class="sxs-lookup"><span data-stu-id="8f4cd-108">**Table 1. Sync-related errors and how to handle them**</span></span>

|<span data-ttu-id="8f4cd-109">**Error**</span><span class="sxs-lookup"><span data-stu-id="8f4cd-109">**Error**</span></span>|<span data-ttu-id="8f4cd-110">**当您尝试 .。。**</span><span class="sxs-lookup"><span data-stu-id="8f4cd-110">**Occurs when you try to…**</span></span>|<span data-ttu-id="8f4cd-111">**处理它的...**</span><span class="sxs-lookup"><span data-stu-id="8f4cd-111">**Handle it by…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8f4cd-112">ErrorInvalidSyncStateData</span><span class="sxs-lookup"><span data-stu-id="8f4cd-112">ErrorInvalidSyncStateData</span></span>  <br/> | <span data-ttu-id="8f4cd-113">使用无效的同步状态值同步项目或文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-113">Synchronize items or folders by using an invalid sync state value.</span></span>  <br/>  <span data-ttu-id="8f4cd-114">如果您的后续请求包含根文件夹，则在初始 SyncFolderHierarchy 请求中排除根文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-114">Exclude a root folder in your initial SyncFolderHierarchy request, when your subsequent request does include a root folder.</span></span>  <br/>  <span data-ttu-id="8f4cd-115">在后续请求中使用不同的根文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-115">Use different root folders in subsequent requests.</span></span>  <br/> | <span data-ttu-id="8f4cd-116">确保您要发送的同步状态值与上一次同步过程中返回的同步状态值相匹配。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-116">Ensuring that the sync state value you are sending matches the sync state value returned during a previous synchronization.</span></span>  <br/>  <span data-ttu-id="8f4cd-117">确保在尝试同步项目时不会发送文件夹层次结构的同步状态，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-117">Ensuring that you are not sending the sync state for the folder hierarchy when you attempt to sync items, and vice versa.</span></span>  <br/>  <span data-ttu-id="8f4cd-118">确保您正在为正确的根文件夹发送同步状态。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-118">Ensuring that you are sending the sync state for the correct root folder.</span></span>  <br/>  <span data-ttu-id="8f4cd-119">确保每个请求中指定了相同的根文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-119">Ensuring that the same root folder is specified in each request.</span></span>  <br/>  <span data-ttu-id="8f4cd-120">确保上一个请求未指定 null 的根文件夹，而当前请求包含根的根文件夹。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-120">Ensuring that the previous request did not specify a root folder of null, while the current request includes a root folder of root.</span></span> <span data-ttu-id="8f4cd-121">Null 和根的处理方式不相同。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-121">Null and root are not treated the same.</span></span>  <br/> |
|<span data-ttu-id="8f4cd-122">ErrorSyncFolderNotFound</span><span class="sxs-lookup"><span data-stu-id="8f4cd-122">ErrorSyncFolderNotFound</span></span>  <br/> |<span data-ttu-id="8f4cd-123">同步无法在服务器上找到的文件夹中的子文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-123">Synchronize subfolders or items in a folder that cannot be found on the server.</span></span>  <br/> |<span data-ttu-id="8f4cd-124">确保请求中指定的文件夹 ID 与以前的同步响应中从服务器返回的文件夹 ID 相匹配。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-124">Ensuring that the folder ID specified in the request matches a folder ID returned from the server in a previous sync response.</span></span>  <br/> |
|<span data-ttu-id="8f4cd-125">ErrorTimeoutExpired</span><span class="sxs-lookup"><span data-stu-id="8f4cd-125">ErrorTimeoutExpired</span></span>  <br/> |<span data-ttu-id="8f4cd-126">发送的请求过多。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-126">Send too many requests.</span></span>  <br/> |<span data-ttu-id="8f4cd-127">将批处理限制为每个批次的10个项目，以避免受到[限制](ews-throttling-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-127">Limiting your batches to 10 items per batch to avoid getting [throttled](ews-throttling-in-exchange.md).</span></span>  <br/> |
|[<span data-ttu-id="8f4cd-128">ServiceResponseException</span><span class="sxs-lookup"><span data-stu-id="8f4cd-128">ServiceResponseException</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="8f4cd-129">当服务器脱机或连接存在问题时连接到 EWS。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-129">Connect to EWS when the server is offline or there is a problem with connectivity.</span></span>  <br/> |<span data-ttu-id="8f4cd-130">请检查与服务器的连接并稍后重试请求。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-130">Checking connectivity with the server and retrying your request later.</span></span> <span data-ttu-id="8f4cd-131">这可能是暂时性的服务错误或网络错误。</span><span class="sxs-lookup"><span data-stu-id="8f4cd-131">This is likely a transient service error or network error.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f4cd-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8f4cd-132">See also</span></span>


- [<span data-ttu-id="8f4cd-133">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="8f4cd-133">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    
- [<span data-ttu-id="8f4cd-134">使用 Exchange 中的 EWS 同步文件夹</span><span class="sxs-lookup"><span data-stu-id="8f4cd-134">Synchronize folders by using EWS in Exchange</span></span>](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8f4cd-135">使用 Exchange 中的 EWS 同步项目</span><span class="sxs-lookup"><span data-stu-id="8f4cd-135">Synchronize items by using EWS in Exchange</span></span>](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="8f4cd-136">ServiceResponseException</span><span class="sxs-lookup"><span data-stu-id="8f4cd-136">ServiceResponseException</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)
    

