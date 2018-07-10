---
title: 工具和资源来解决 exchange 的 EWS 应用程序
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: 查找资源以帮助您解决您 EWS 托管 API 或 EWS 应用程序。
ms.openlocfilehash: d8d8ea736ca3b896642ad06f5987caeba8d8d059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753015"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a><span data-ttu-id="e9827-103">工具和资源来解决 exchange 的 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="e9827-103">Tools and resources for troubleshooting EWS applications for Exchange</span></span>

<span data-ttu-id="e9827-104">查找资源以帮助您解决您 EWS 托管 API 或 EWS 应用程序。</span><span class="sxs-lookup"><span data-stu-id="e9827-104">Find resources to help you troubleshoot your EWS Managed API or EWS application.</span></span>
  
<span data-ttu-id="e9827-105">按计划并不总是会事项。</span><span class="sxs-lookup"><span data-stu-id="e9827-105">Things don't always go as planned.</span></span> <span data-ttu-id="e9827-106">有时 EWS 请求失败，或提供意外的结果。</span><span class="sxs-lookup"><span data-stu-id="e9827-106">Sometimes EWS requests fail, or provide unexpected results.</span></span> <span data-ttu-id="e9827-107">可能会失败，尤其是原因不明显。</span><span class="sxs-lookup"><span data-stu-id="e9827-107">This can be frustrating, especially if the reason isn't obvious.</span></span> <span data-ttu-id="e9827-108">可望这永远不会发生，但如果是这样，本文提供了有关工具和资源可用于帮助解决您的问题的信息。</span><span class="sxs-lookup"><span data-stu-id="e9827-108">Hopefully this never happens to you, but if it does, this article provides information about tools and resources that you can use to help troubleshoot your problem.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e9827-109">本文提供故障排除的一般性建议和源的疑难解答信息。</span><span class="sxs-lookup"><span data-stu-id="e9827-109">This article provides general troubleshooting advice and sources for troubleshooting information.</span></span> <span data-ttu-id="e9827-110">遗憾的是不可能以提供详细的故障排除步骤。</span><span class="sxs-lookup"><span data-stu-id="e9827-110">Unfortunately it isn't possible to give detailed troubleshooting steps.</span></span> <span data-ttu-id="e9827-111">您的特定错误进行疑难解答的帮助，请参阅[下一步步骤](#bk_NextSteps)。</span><span class="sxs-lookup"><span data-stu-id="e9827-111">For assistance troubleshooting your specific error, see [Next steps](#bk_NextSteps).</span></span> 
  
## <a name="examine-the-soap-requests-and-responses"></a><span data-ttu-id="e9827-112">检查的 SOAP 请求和响应</span><span class="sxs-lookup"><span data-stu-id="e9827-112">Examine the SOAP requests and responses</span></span>

<span data-ttu-id="e9827-113">当操作不能正常工作时，它真正有助于将能够看到了什么事。</span><span class="sxs-lookup"><span data-stu-id="e9827-113">When things aren't working correctly, it really helps to be able to see what's going on.</span></span> <span data-ttu-id="e9827-114">查询时检查应用程序发送通过网络的请求和响应的服务器发送回调查问题 EWS 或 EWS 托管 API （英文） 是第一行。</span><span class="sxs-lookup"><span data-stu-id="e9827-114">The first line of inquiry when investigating a problem with EWS or the EWS Managed API is to examine the requests that your application is sending over the network and the responses that the server is sending back.</span></span>
  
<span data-ttu-id="e9827-115">EWS 托管 API 轻松检查 SOAP 请求和响应与其[内置的跟踪功能](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="e9827-115">The EWS Managed API makes examining SOAP requests and responses easy with its [built in tracing functionality](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md).</span></span> <span data-ttu-id="e9827-116">如果您使用 EWS，您可能或可能无法访问类似的跟踪功能，具体取决于哪些平台或您使用发送您的请求的类。</span><span class="sxs-lookup"><span data-stu-id="e9827-116">If you are using EWS, you might or might not have access to similar tracing functionality, depending on what platform or classes you use to send your requests.</span></span> <span data-ttu-id="e9827-117">但是，始终可以使用[网络监视器](http://www.microsoft.com/en-us/download/details.aspx?id=4865)或[Fiddler](http://www.telerik.com/fiddler)网络跟踪工具检查网络流量和查看请求和响应的有效负荷。</span><span class="sxs-lookup"><span data-stu-id="e9827-117">However, you can always use a network tracing tool like [Network Monitor](http://www.microsoft.com/en-us/download/details.aspx?id=4865) or [Fiddler](http://www.telerik.com/fiddler) to examine the network traffic and view the request and response payloads.</span></span> 
  
<span data-ttu-id="e9827-118">此外，您还可以[检测客户端请求](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)以增强请求和响应中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="e9827-118">Additionally, you can [instrument your client requests](instrumenting-client-requests-for-ews-and-rest-in-exchange.md) to enhance the information available in requests and responses.</span></span> 
  
<span data-ttu-id="e9827-119">请求和响应后，问自己以下： 执行表现正确？</span><span class="sxs-lookup"><span data-stu-id="e9827-119">After you have the requests and responses, ask yourself the following: Do they look correct?</span></span> <span data-ttu-id="e9827-120">是您的应用程序发送预期的值？</span><span class="sxs-lookup"><span data-stu-id="e9827-120">Are the values that your application is sending expected?</span></span> <span data-ttu-id="e9827-121">响应意义吗？</span><span class="sxs-lookup"><span data-stu-id="e9827-121">Do the responses make sense?</span></span>
  
## <a name="examine-error-codes"></a><span data-ttu-id="e9827-122">检查错误代码</span><span class="sxs-lookup"><span data-stu-id="e9827-122">Examine error codes</span></span>

<span data-ttu-id="e9827-123">有时的错误代码可以继续对于查明问题，即使它似乎有意义的第一次看到。</span><span class="sxs-lookup"><span data-stu-id="e9827-123">Sometimes the error code can go a long way toward pinpointing the problem, even if at first glance it doesn't seem to make sense.</span></span> <span data-ttu-id="e9827-124">此错误指示正在[受到控制](ews-throttling-in-exchange.md)您的客户端？</span><span class="sxs-lookup"><span data-stu-id="e9827-124">Does the error indicate that your client is being [throttled](ews-throttling-in-exchange.md)?</span></span> <span data-ttu-id="e9827-125">可能对自动发现刷新[配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)的调用是顺序？</span><span class="sxs-lookup"><span data-stu-id="e9827-125">Perhaps a call to Autodiscover to [refresh configuration information](how-to-refresh-configuration-information-by-using-autodiscover.md) is in order?</span></span> 
  
<span data-ttu-id="e9827-126">有关处理特定错误的详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="e9827-126">For more information about handling specific errors, see the following articles:</span></span>
  
- [<span data-ttu-id="e9827-127">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="e9827-127">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="e9827-128">在 Exchange 处理与通知相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="e9827-128">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="e9827-129">在 Exchange 处理同步相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="e9827-129">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="e9827-130">在 Exchange 处理删除相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="e9827-130">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a><span data-ttu-id="e9827-131">验证版本</span><span class="sxs-lookup"><span data-stu-id="e9827-131">Verify versions</span></span>

<span data-ttu-id="e9827-132">有 EWS 操作中所涉及的不同组件的数量，这些组件的版本会影响结果。</span><span class="sxs-lookup"><span data-stu-id="e9827-132">There are a number of different components involved in EWS operations, and the versions of those components can influence the results.</span></span>
  
<span data-ttu-id="e9827-133">**表 1。可能会影响 EWS 过程的版本控制组件**</span><span class="sxs-lookup"><span data-stu-id="e9827-133">**Table 1. Versioned components that can affect EWS processes**</span></span>

|<span data-ttu-id="e9827-134">**组件**</span><span class="sxs-lookup"><span data-stu-id="e9827-134">**Component**</span></span>|<span data-ttu-id="e9827-135">**EWS Managed API**</span><span class="sxs-lookup"><span data-stu-id="e9827-135">**EWS Managed API**</span></span>|<span data-ttu-id="e9827-136">**EWS**</span><span class="sxs-lookup"><span data-stu-id="e9827-136">**EWS**</span></span>|<span data-ttu-id="e9827-137">**备注**</span><span class="sxs-lookup"><span data-stu-id="e9827-137">**Notes**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e9827-138">请求的服务器版本</span><span class="sxs-lookup"><span data-stu-id="e9827-138">Requested server version</span></span>  <br/> |<span data-ttu-id="e9827-139">[ExchangeServiceBase.RequestedServerVersion](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="e9827-139">[ExchangeServiceBase.RequestedServerVersion](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="e9827-140">[RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="e9827-140">[RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="e9827-141">此值控制哪个版本的 EWS 架构用于处理 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="e9827-141">This value controls which version of the EWS schema is used to process the EWS request.</span></span> <span data-ttu-id="e9827-142">请确保，此处指定的架构版本有意义请求所发送。</span><span class="sxs-lookup"><span data-stu-id="e9827-142">Make sure that the schema version specified here makes sense for the request you are sending.</span></span> <span data-ttu-id="e9827-143">某些属性和操作不可用在早期版本的架构。</span><span class="sxs-lookup"><span data-stu-id="e9827-143">Some properties and operations are not available in earlier versions of the schema.</span></span>  <br/> |
|<span data-ttu-id="e9827-144">服务器版本</span><span class="sxs-lookup"><span data-stu-id="e9827-144">The server version</span></span>  <br/> |<span data-ttu-id="e9827-145">[ExchangeServiceBase.ServerInfo](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="e9827-145">[ExchangeServiceBase.ServerInfo](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="e9827-146">[ServerVersionInfo](http://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="e9827-146">[ServerVersionInfo](http://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="e9827-147">此值由服务器 EWS 响应中返回，并指示处理响应的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="e9827-147">This value is returned by the server in EWS responses, and indicates the version of the server that processed the response.</span></span> <span data-ttu-id="e9827-148">确保此值是您的预期。</span><span class="sxs-lookup"><span data-stu-id="e9827-148">Make sure this value is what you expect.</span></span> <span data-ttu-id="e9827-149">如果可能，请确保 Exchange 服务器正在运行的主要版本 Exchange 的最新的更新。</span><span class="sxs-lookup"><span data-stu-id="e9827-149">If possible, make sure that the Exchange server is running the most recent update for your major version of Exchange.</span></span>  <br/> |
|<span data-ttu-id="e9827-150">EWS 托管 API 版本</span><span class="sxs-lookup"><span data-stu-id="e9827-150">The EWS Managed API version</span></span>  <br/> |<span data-ttu-id="e9827-151">Microsoft.Exchange.WebServices.dll 文件的产品版本属性。</span><span class="sxs-lookup"><span data-stu-id="e9827-151">The Product version property of the Microsoft.Exchange.WebServices.dll file.</span></span>  <br/> |<span data-ttu-id="e9827-152">不适用</span><span class="sxs-lookup"><span data-stu-id="e9827-152">Not applicable</span></span>  <br/> |<span data-ttu-id="e9827-153">如果您正在使用 EWS 托管 API，请确保您使用的[最新版本](http://aka.ms/ews-managed-api-readme)。</span><span class="sxs-lookup"><span data-stu-id="e9827-153">If you're using the EWS Managed API, make sure that you are using [the most recent version](http://aka.ms/ews-managed-api-readme).</span></span>  <br/> |
   
## <a name="verify-access"></a><span data-ttu-id="e9827-154">验证访问权限</span><span class="sxs-lookup"><span data-stu-id="e9827-154">Verify access</span></span>

<span data-ttu-id="e9827-155">EWS 被启用的默认情况下，但[可以更改默认值](how-to-control-access-to-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="e9827-155">EWS is enabled by default, but [defaults can be changed](how-to-control-access-to-ews-in-exchange.md).</span></span> <span data-ttu-id="e9827-156">使用[Get-organizationconfig](http://technet.microsoft.com/zh-cn/library/bb124754.aspx) cmdlet，以确保 EWS 已启用的服务器上，并使用[Get-casmailbox](http://technet.microsoft.com/zh-cn/library/aa997571.aspx) cmdlet 以确保 EWS 已启用的用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="e9827-156">Use the [Get-OrganizationConfig](http://technet.microsoft.com/zh-cn/library/bb124754.aspx) cmdlet to make sure that EWS is enabled on the server, and the [Get-CASMailbox](http://technet.microsoft.com/zh-cn/library/aa997571.aspx) cmdlet to make sure that EWS is enabled for the user's mailbox.</span></span> <span data-ttu-id="e9827-157">此外可以检查这两个 cmdlet 响应的 EWS 允许或阻止列表中，并确保您的应用程序不阻止使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="e9827-157">Also check both cmdlet responses for an EWS allow or block list, and make sure that your application isn't blocked from using EWS.</span></span> 
  
<span data-ttu-id="e9827-158">您还应验证尚未修改 EWS 虚拟目录上的[默认身份验证设置](http://technet.microsoft.com/zh-cn/library/gg247612%28v=exchg.150%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e9827-158">You should also verify that the [default authentication settings](http://technet.microsoft.com/zh-cn/library/gg247612%28v=exchg.150%29.aspx) on the EWS virtual directory have not been modified.</span></span> 
  
## <a name="try-another-ews-client"></a><span data-ttu-id="e9827-159">尝试另一个 EWS 客户端</span><span class="sxs-lookup"><span data-stu-id="e9827-159">Try another EWS client</span></span>

<span data-ttu-id="e9827-160">有时非常有用尝试从另一个客户端相同的请求和比较结果。</span><span class="sxs-lookup"><span data-stu-id="e9827-160">Sometimes it is helpful to try the same request from another client and compare results.</span></span> <span data-ttu-id="e9827-161">如果另一个客户端获取不同的结果，什么是不同？</span><span class="sxs-lookup"><span data-stu-id="e9827-161">If another client gets different results, what is different?</span></span> <span data-ttu-id="e9827-162">找出请求成功和失败的请求之间的不同，可以帮助解释特定请求失败的原因。</span><span class="sxs-lookup"><span data-stu-id="e9827-162">Figuring out what is different between a successful request and a failed request can help explain why a particular request is failing.</span></span>
  
<span data-ttu-id="e9827-163">当然，您可以编写测试与另一个客户端，而您没有为 ！</span><span class="sxs-lookup"><span data-stu-id="e9827-163">While you can certainly write another client to test with, you don't have to!</span></span> <span data-ttu-id="e9827-164">[EWSEditor](http://ewseditor.codeplex.com/)是使用 EWS 托管 API 和 EWS 示例客户端。</span><span class="sxs-lookup"><span data-stu-id="e9827-164">[EWSEditor](http://ewseditor.codeplex.com/) is a sample client that uses the EWS Managed API and EWS.</span></span> <span data-ttu-id="e9827-165">您可以下载客户端 （包括源代码），并使用它来尝试相同应用程序中失败的请求。</span><span class="sxs-lookup"><span data-stu-id="e9827-165">You can download the client (including the source code) and use it to try the same requests that are failing in your application.</span></span> 
  
## <a name="examine-iis-logs"></a><span data-ttu-id="e9827-166">检查 IIS 日志</span><span class="sxs-lookup"><span data-stu-id="e9827-166">Examine IIS logs</span></span>

<span data-ttu-id="e9827-167">如果您有权访问 Exchange server，提供在客户端访问服务器上的 Internet 信息服务 (IIS) 日志记录功能可以提供有关失败的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e9827-167">If you have access to the Exchange server, the logging functionality provided by Internet Information Services (IIS) on the Client Access servers can provide more information about failures.</span></span> <span data-ttu-id="e9827-168">但是，请记住，IIS 日志将只能非常有用，如果您收到 HTTP 错误。</span><span class="sxs-lookup"><span data-stu-id="e9827-168">However, keep in mind that IIS logs will only be helpful if you are receiving an HTTP error.</span></span>
  
<span data-ttu-id="e9827-169">IIS 提供两种不同的日志记录方法： [IIS 日志记录](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)和[跟踪失败的请求](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)。</span><span class="sxs-lookup"><span data-stu-id="e9827-169">IIS provides two different logging methods: [IIS logging](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) and [failed requests tracing](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis).</span></span> <span data-ttu-id="e9827-170">若要使用 IIS 日志，您可以使用[Log Parser Studio](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)，其中包括内置 EWS 查询数。</span><span class="sxs-lookup"><span data-stu-id="e9827-170">To work with IIS logs, you can use [Log Parser Studio](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx), which includes a number of built-in EWS queries.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="e9827-171">后续步骤</span><span class="sxs-lookup"><span data-stu-id="e9827-171">Next steps</span></span>
<span data-ttu-id="e9827-172"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="e9827-172"></span></span>

<span data-ttu-id="e9827-173">现在，您已了解工具和资源可用于解决，您可能需要了解这些工具提供的信息的帮助。</span><span class="sxs-lookup"><span data-stu-id="e9827-173">Now that you've learned about the tools and resources that you can use to troubleshoot, you might need help understanding the information provided by those tools.</span></span> <span data-ttu-id="e9827-174">以下是一些用于获取帮助选项：</span><span class="sxs-lookup"><span data-stu-id="e9827-174">The following are some options for getting help:</span></span>
  
- <span data-ttu-id="e9827-175">[MSDN 上的 Exchange Server 开发论坛](http://social.msdn.microsoft.com/Forums/en-US/home?category=exchangeserver)— 提出 MSDN Exchange Server 开发社区的问题。</span><span class="sxs-lookup"><span data-stu-id="e9827-175">[Exchange Server Development forum on MSDN](http://social.msdn.microsoft.com/Forums/en-US/home?category=exchangeserver) — Ask a question of the MSDN Exchange Server development community.</span></span> 
    
- <span data-ttu-id="e9827-176">[StackOverflow](http://stackoverflow.com/tags/ews) — 提出 StackOverflow 社区的问题。</span><span class="sxs-lookup"><span data-stu-id="e9827-176">[StackOverflow](http://stackoverflow.com/tags/ews) — Ask a question of the StackOverflow community.</span></span> <span data-ttu-id="e9827-177">请务必标记"ews"与您的帖子。</span><span class="sxs-lookup"><span data-stu-id="e9827-177">Be sure to tag your post with "ews".</span></span> 
    
- <span data-ttu-id="e9827-178">[Microsoft 支持](http://support.microsoft.com/ph/730/en-us)— 与 Microsoft 支持专业人员联系以寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="e9827-178">[Microsoft Support](http://support.microsoft.com/ph/730/en-us) — Contact a Microsoft support professional for assistance.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e9827-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e9827-179">See also</span></span>


<span data-ttu-id="e9827-180">请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="e9827-180">See the following articles:</span></span>
  
- [<span data-ttu-id="e9827-181">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="e9827-181">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="e9827-182">跟踪请求和响应解决 EWS 托管 API 应用程序</span><span class="sxs-lookup"><span data-stu-id="e9827-182">Trace requests and responses to troubleshoot EWS Managed API applications</span></span>](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [<span data-ttu-id="e9827-183">在 Exchange 检测 EWS 和 REST 的客户端请求</span><span class="sxs-lookup"><span data-stu-id="e9827-183">Instrumenting client requests for EWS and REST in Exchange</span></span>](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [<span data-ttu-id="e9827-184">限制在 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="e9827-184">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    
- [<span data-ttu-id="e9827-185">使用自动发现刷新配置信息</span><span class="sxs-lookup"><span data-stu-id="e9827-185">Refresh configuration information by using Autodiscover</span></span>](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [<span data-ttu-id="e9827-186">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="e9827-186">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="e9827-187">在 Exchange 处理与通知相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="e9827-187">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="e9827-188">在 Exchange 处理同步相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="e9827-188">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="e9827-189">在 Exchange 处理删除相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="e9827-189">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="e9827-190">在 IIS 中配置日志记录</span><span class="sxs-lookup"><span data-stu-id="e9827-190">Configuring Logging in IIS</span></span>](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [<span data-ttu-id="e9827-191">疑难解答失败的请求在 IIS 7 中使用跟踪</span><span class="sxs-lookup"><span data-stu-id="e9827-191">Troubleshooting Failed Requests Using Tracing in IIS 7</span></span>](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [<span data-ttu-id="e9827-192">Log Parser Studio 简介：</span><span class="sxs-lookup"><span data-stu-id="e9827-192">Introducing: Log Parser Studio</span></span>](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [<span data-ttu-id="e9827-193">Exchange 虚拟目录的默认设置</span><span class="sxs-lookup"><span data-stu-id="e9827-193">Default Settings for Exchange Virtual Directories</span></span>](http://technet.microsoft.com/zh-cn/library/gg247612%28v=exchg.150%29.aspx)
    
<span data-ttu-id="e9827-194">下载以下组件：</span><span class="sxs-lookup"><span data-stu-id="e9827-194">Download the following:</span></span>
  
- [<span data-ttu-id="e9827-195">Microsoft 网络监视器 3.4</span><span class="sxs-lookup"><span data-stu-id="e9827-195">Microsoft Network Monitor 3.4</span></span>](http://www.microsoft.com/en-us/download/details.aspx?id=4865)
    
- [<span data-ttu-id="e9827-196">Fiddler</span><span class="sxs-lookup"><span data-stu-id="e9827-196">Fiddler</span></span>](http://www.telerik.com/fiddler)
    
- [<span data-ttu-id="e9827-197">EWSEditor</span><span class="sxs-lookup"><span data-stu-id="e9827-197">EWSEditor</span></span>](http://ewseditor.codeplex.com/)
    
- [<span data-ttu-id="e9827-198">Exchange Web Services 托管的 API</span><span class="sxs-lookup"><span data-stu-id="e9827-198">Exchange Web Services Managed API</span></span>](http://go.microsoft.com/fwlink/?LinkID=255472)
    

