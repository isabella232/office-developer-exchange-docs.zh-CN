---
title: 工具和资源来解决 exchange 的 EWS 应用程序
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: 查找可帮助您对 EWS 托管 API 或 EWS 应用程序进行故障排除的资源。
localization_priority: Priority
ms.openlocfilehash: 7c7cbe8c93edec5ad99df079c6eb96286c1ba063
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463739"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a><span data-ttu-id="95ed3-103">工具和资源来解决 exchange 的 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="95ed3-103">Tools and resources for troubleshooting EWS applications for Exchange</span></span>

<span data-ttu-id="95ed3-104">查找可帮助您对 EWS 托管 API 或 EWS 应用程序进行故障排除的资源。</span><span class="sxs-lookup"><span data-stu-id="95ed3-104">Find resources to help you troubleshoot your EWS Managed API or EWS application.</span></span>
  
<span data-ttu-id="95ed3-105">有些事情并不总是按计划进行。</span><span class="sxs-lookup"><span data-stu-id="95ed3-105">Things don't always go as planned.</span></span> <span data-ttu-id="95ed3-106">有时 EWS 请求失败，或提供意外的结果。</span><span class="sxs-lookup"><span data-stu-id="95ed3-106">Sometimes EWS requests fail, or provide unexpected results.</span></span> <span data-ttu-id="95ed3-107">这可能会令人沮丧，尤其是当原因不明显时。</span><span class="sxs-lookup"><span data-stu-id="95ed3-107">This can be frustrating, especially if the reason isn't obvious.</span></span> <span data-ttu-id="95ed3-108">但愿这永远不会发生，但如果是这样，本文将提供有关工具和资源的信息，您可以使用这些工具和资源来帮助您解决问题。</span><span class="sxs-lookup"><span data-stu-id="95ed3-108">Hopefully this never happens to you, but if it does, this article provides information about tools and resources that you can use to help troubleshoot your problem.</span></span>
  
> [!NOTE]
> <span data-ttu-id="95ed3-109">本文提供了有关疑难解答信息的一般故障排除建议和源。</span><span class="sxs-lookup"><span data-stu-id="95ed3-109">This article provides general troubleshooting advice and sources for troubleshooting information.</span></span> <span data-ttu-id="95ed3-110">遗憾的是，不能提供详细的故障排除步骤。</span><span class="sxs-lookup"><span data-stu-id="95ed3-110">Unfortunately it isn't possible to give detailed troubleshooting steps.</span></span> <span data-ttu-id="95ed3-111">有关解决特定错误的帮助，请参阅[后续步骤](#bk_NextSteps)。</span><span class="sxs-lookup"><span data-stu-id="95ed3-111">For assistance troubleshooting your specific error, see [Next steps](#bk_NextSteps).</span></span> 
  
## <a name="examine-the-soap-requests-and-responses"></a><span data-ttu-id="95ed3-112">检查 SOAP 请求和响应</span><span class="sxs-lookup"><span data-stu-id="95ed3-112">Examine the SOAP requests and responses</span></span>

<span data-ttu-id="95ed3-113">当事情不能正常运行时，它确实有助于查看发生的情况。</span><span class="sxs-lookup"><span data-stu-id="95ed3-113">When things aren't working correctly, it really helps to be able to see what's going on.</span></span> <span data-ttu-id="95ed3-114">在调查 EWS 或 EWS 托管 API 的问题时，第一行查询是检查您的应用程序通过网络发送的请求以及服务器发送回的响应。</span><span class="sxs-lookup"><span data-stu-id="95ed3-114">The first line of inquiry when investigating a problem with EWS or the EWS Managed API is to examine the requests that your application is sending over the network and the responses that the server is sending back.</span></span>
  
<span data-ttu-id="95ed3-115">EWS 托管 API 使 SOAP 请求和响应易于通过其[内置跟踪功能](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)进行检查。</span><span class="sxs-lookup"><span data-stu-id="95ed3-115">The EWS Managed API makes examining SOAP requests and responses easy with its [built in tracing functionality](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md).</span></span> <span data-ttu-id="95ed3-116">如果使用 EWS，则可能会也可能无法访问类似的跟踪功能，具体取决于用于发送请求的平台或类。</span><span class="sxs-lookup"><span data-stu-id="95ed3-116">If you are using EWS, you might or might not have access to similar tracing functionality, depending on what platform or classes you use to send your requests.</span></span> <span data-ttu-id="95ed3-117">但是，您始终可以使用网络跟踪工具（如[网络监视器](https://www.microsoft.com/download/details.aspx?id=4865)或[Fiddler](http://www.telerik.com/fiddler) ）来检查网络流量并查看请求和响应负载。</span><span class="sxs-lookup"><span data-stu-id="95ed3-117">However, you can always use a network tracing tool like [Network Monitor](https://www.microsoft.com/download/details.aspx?id=4865) or [Fiddler](http://www.telerik.com/fiddler) to examine the network traffic and view the request and response payloads.</span></span> 
  
<span data-ttu-id="95ed3-118">此外，还可以[检测客户端请求](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)，以增强请求和响应中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="95ed3-118">Additionally, you can [instrument your client requests](instrumenting-client-requests-for-ews-and-rest-in-exchange.md) to enhance the information available in requests and responses.</span></span> 
  
<span data-ttu-id="95ed3-119">在获得请求和响应后，请自己询问以下各项：是否正确？</span><span class="sxs-lookup"><span data-stu-id="95ed3-119">After you have the requests and responses, ask yourself the following: Do they look correct?</span></span> <span data-ttu-id="95ed3-120">您的应用程序是否需要发送的值是什么？</span><span class="sxs-lookup"><span data-stu-id="95ed3-120">Are the values that your application is sending expected?</span></span> <span data-ttu-id="95ed3-121">做出的响应是否有意义？</span><span class="sxs-lookup"><span data-stu-id="95ed3-121">Do the responses make sense?</span></span>
  
## <a name="examine-error-codes"></a><span data-ttu-id="95ed3-122">检查错误代码</span><span class="sxs-lookup"><span data-stu-id="95ed3-122">Examine error codes</span></span>

<span data-ttu-id="95ed3-123">有时，错误代码可能会很长一段时间来查明问题，即使乍一看看似乎没有意义也是如此。</span><span class="sxs-lookup"><span data-stu-id="95ed3-123">Sometimes the error code can go a long way toward pinpointing the problem, even if at first glance it doesn't seem to make sense.</span></span> <span data-ttu-id="95ed3-124">该错误是否指示正在[限制](ews-throttling-in-exchange.md)你的客户端？</span><span class="sxs-lookup"><span data-stu-id="95ed3-124">Does the error indicate that your client is being [throttled](ews-throttling-in-exchange.md)?</span></span> <span data-ttu-id="95ed3-125">可能会调用自动发现以[刷新配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)，是否按顺序进行？</span><span class="sxs-lookup"><span data-stu-id="95ed3-125">Perhaps a call to Autodiscover to [refresh configuration information](how-to-refresh-configuration-information-by-using-autodiscover.md) is in order?</span></span> 
  
<span data-ttu-id="95ed3-126">有关处理特定错误的详细信息，请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="95ed3-126">For more information about handling specific errors, see the following articles:</span></span>
  
- [<span data-ttu-id="95ed3-127">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="95ed3-127">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="95ed3-128">在 Exchange 中处理 EWS 中与通知相关的错误</span><span class="sxs-lookup"><span data-stu-id="95ed3-128">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="95ed3-129">在 Exchange 中处理 EWS 中与同步相关的错误</span><span class="sxs-lookup"><span data-stu-id="95ed3-129">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="95ed3-130">在 Exchange 中处理 EWS 中的与删除相关的错误</span><span class="sxs-lookup"><span data-stu-id="95ed3-130">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a><span data-ttu-id="95ed3-131">验证版本</span><span class="sxs-lookup"><span data-stu-id="95ed3-131">Verify versions</span></span>

<span data-ttu-id="95ed3-132">EWS 操作中涉及许多不同的组件，这些组件的版本可能会影响结果。</span><span class="sxs-lookup"><span data-stu-id="95ed3-132">There are a number of different components involved in EWS operations, and the versions of those components can influence the results.</span></span>
  
<span data-ttu-id="95ed3-133">**表1。可能影响 EWS 进程的版本控制组件**</span><span class="sxs-lookup"><span data-stu-id="95ed3-133">**Table 1. Versioned components that can affect EWS processes**</span></span>

|<span data-ttu-id="95ed3-134">**组件**</span><span class="sxs-lookup"><span data-stu-id="95ed3-134">**Component**</span></span>|<span data-ttu-id="95ed3-135">**EWS Managed API**</span><span class="sxs-lookup"><span data-stu-id="95ed3-135">**EWS Managed API**</span></span>|<span data-ttu-id="95ed3-136">**EWS**</span><span class="sxs-lookup"><span data-stu-id="95ed3-136">**EWS**</span></span>|<span data-ttu-id="95ed3-137">**备注**</span><span class="sxs-lookup"><span data-stu-id="95ed3-137">**Notes**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95ed3-138">请求的服务器版本</span><span class="sxs-lookup"><span data-stu-id="95ed3-138">Requested server version</span></span>  <br/> |<span data-ttu-id="95ed3-139">[ExchangeServiceBase](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="95ed3-139">[ExchangeServiceBase.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="95ed3-140">[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="95ed3-140">[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="95ed3-141">此值控制用于处理 EWS 请求的 EWS 架构的版本。</span><span class="sxs-lookup"><span data-stu-id="95ed3-141">This value controls which version of the EWS schema is used to process the EWS request.</span></span> <span data-ttu-id="95ed3-142">请确保在此处指定的架构版本对要发送的请求有意义。</span><span class="sxs-lookup"><span data-stu-id="95ed3-142">Make sure that the schema version specified here makes sense for the request you are sending.</span></span> <span data-ttu-id="95ed3-143">某些属性和操作在架构的早期版本中不可用。</span><span class="sxs-lookup"><span data-stu-id="95ed3-143">Some properties and operations are not available in earlier versions of the schema.</span></span>  <br/> |
|<span data-ttu-id="95ed3-144">服务器版本</span><span class="sxs-lookup"><span data-stu-id="95ed3-144">The server version</span></span>  <br/> |<span data-ttu-id="95ed3-145">[ExchangeServiceBase](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="95ed3-145">[ExchangeServiceBase.ServerInfo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="95ed3-146">[ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="95ed3-146">[ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx) element</span></span>  <br/> |<span data-ttu-id="95ed3-147">此值由服务器以 EWS 响应的形式返回，并指示处理响应的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="95ed3-147">This value is returned by the server in EWS responses, and indicates the version of the server that processed the response.</span></span> <span data-ttu-id="95ed3-148">请确保此值是您所期望的值。</span><span class="sxs-lookup"><span data-stu-id="95ed3-148">Make sure this value is what you expect.</span></span> <span data-ttu-id="95ed3-149">如果可能，请确保 Exchange 服务器对你的主要版本的 Exchange 运行的是最新的更新。</span><span class="sxs-lookup"><span data-stu-id="95ed3-149">If possible, make sure that the Exchange server is running the most recent update for your major version of Exchange.</span></span>  <br/> |
|<span data-ttu-id="95ed3-150">EWS 托管 API 版本</span><span class="sxs-lookup"><span data-stu-id="95ed3-150">The EWS Managed API version</span></span>  <br/> |<span data-ttu-id="95ed3-151">WebServices 文件的 "产品版本" 属性。</span><span class="sxs-lookup"><span data-stu-id="95ed3-151">The Product version property of the Microsoft.Exchange.WebServices.dll file.</span></span>  <br/> |<span data-ttu-id="95ed3-152">不适用</span><span class="sxs-lookup"><span data-stu-id="95ed3-152">Not applicable</span></span>  <br/> |<span data-ttu-id="95ed3-153">如果使用的是 EWS 托管 API，请确保使用的是[最新版本](https://aka.ms/ews-managed-api-readme)。</span><span class="sxs-lookup"><span data-stu-id="95ed3-153">If you're using the EWS Managed API, make sure that you are using [the most recent version](https://aka.ms/ews-managed-api-readme).</span></span>  <br/> |
   
## <a name="verify-access"></a><span data-ttu-id="95ed3-154">验证访问</span><span class="sxs-lookup"><span data-stu-id="95ed3-154">Verify access</span></span>

<span data-ttu-id="95ed3-155">默认情况下，EWS 处于启用状态，但[可以更改默认值](how-to-control-access-to-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="95ed3-155">EWS is enabled by default, but [defaults can be changed](how-to-control-access-to-ews-in-exchange.md).</span></span> <span data-ttu-id="95ed3-156">使用[set-organizationconfig](https://technet.microsoft.com/library/bb124754.aspx) cmdlet 可确保在服务器上启用 ews，并使用[set-casmailbox](https://technet.microsoft.com/library/aa997571.aspx) cmdlet 来确保为用户的邮箱启用了 ews。</span><span class="sxs-lookup"><span data-stu-id="95ed3-156">Use the [Get-OrganizationConfig](https://technet.microsoft.com/library/bb124754.aspx) cmdlet to make sure that EWS is enabled on the server, and the [Get-CASMailbox](https://technet.microsoft.com/library/aa997571.aspx) cmdlet to make sure that EWS is enabled for the user's mailbox.</span></span> <span data-ttu-id="95ed3-157">此外，请检查 EWS 允许或阻止列表的 cmdlet 响应，并确保您的应用程序不会被阻止使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="95ed3-157">Also check both cmdlet responses for an EWS allow or block list, and make sure that your application isn't blocked from using EWS.</span></span> 
  
<span data-ttu-id="95ed3-158">此外，还应验证 EWS 虚拟目录上的[默认身份验证设置](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)是否尚未修改。</span><span class="sxs-lookup"><span data-stu-id="95ed3-158">You should also verify that the [default authentication settings](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx) on the EWS virtual directory have not been modified.</span></span> 
  
## <a name="try-another-ews-client"></a><span data-ttu-id="95ed3-159">尝试其他 EWS 客户端</span><span class="sxs-lookup"><span data-stu-id="95ed3-159">Try another EWS client</span></span>

<span data-ttu-id="95ed3-160">有时，尝试来自另一个客户端的相同请求并比较结果会很有帮助。</span><span class="sxs-lookup"><span data-stu-id="95ed3-160">Sometimes it is helpful to try the same request from another client and compare results.</span></span> <span data-ttu-id="95ed3-161">如果其他客户端得到不同的结果，有何不同？</span><span class="sxs-lookup"><span data-stu-id="95ed3-161">If another client gets different results, what is different?</span></span> <span data-ttu-id="95ed3-162">在成功的请求和失败的请求之间找出不同的信息可帮助解释特定请求失败的原因。</span><span class="sxs-lookup"><span data-stu-id="95ed3-162">Figuring out what is different between a successful request and a failed request can help explain why a particular request is failing.</span></span>
  
<span data-ttu-id="95ed3-163">当然，您可以编写另一个客户端以供测试，但不必再进行！</span><span class="sxs-lookup"><span data-stu-id="95ed3-163">While you can certainly write another client to test with, you don't have to!</span></span> <span data-ttu-id="95ed3-164">[EWSEditor](http://ewseditor.codeplex.com/)是一个使用 EWS 托管 API 和 ews 的示例客户端。</span><span class="sxs-lookup"><span data-stu-id="95ed3-164">[EWSEditor](http://ewseditor.codeplex.com/) is a sample client that uses the EWS Managed API and EWS.</span></span> <span data-ttu-id="95ed3-165">您可以下载客户端（包括源代码），并使用它来尝试在您的应用程序中出现故障的相同请求。</span><span class="sxs-lookup"><span data-stu-id="95ed3-165">You can download the client (including the source code) and use it to try the same requests that are failing in your application.</span></span> 
  
## <a name="examine-iis-logs"></a><span data-ttu-id="95ed3-166">检查 IIS 日志</span><span class="sxs-lookup"><span data-stu-id="95ed3-166">Examine IIS logs</span></span>

<span data-ttu-id="95ed3-167">如果您有权访问 Exchange 服务器，客户端访问服务器上的 Internet 信息服务（IIS）提供的日志记录功能可以提供有关故障的详细信息。</span><span class="sxs-lookup"><span data-stu-id="95ed3-167">If you have access to the Exchange server, the logging functionality provided by Internet Information Services (IIS) on the Client Access servers can provide more information about failures.</span></span> <span data-ttu-id="95ed3-168">但请记住，IIS 日志将仅在收到 HTTP 错误时才有用。</span><span class="sxs-lookup"><span data-stu-id="95ed3-168">However, keep in mind that IIS logs will only be helpful if you are receiving an HTTP error.</span></span>
  
<span data-ttu-id="95ed3-169">IIS 提供了两种不同的日志记录方法： [iis 日志记录](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)和[失败请求跟踪](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)。</span><span class="sxs-lookup"><span data-stu-id="95ed3-169">IIS provides two different logging methods: [IIS logging](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) and [failed requests tracing](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis).</span></span> <span data-ttu-id="95ed3-170">若要使用 IIS 日志，可以使用[Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)，其中包括许多内置的 EWS 查询。</span><span class="sxs-lookup"><span data-stu-id="95ed3-170">To work with IIS logs, you can use [Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx), which includes a number of built-in EWS queries.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="95ed3-171">后续步骤</span><span class="sxs-lookup"><span data-stu-id="95ed3-171">Next steps</span></span>
<span data-ttu-id="95ed3-172"><a name="bk_NextSteps"> </a></span><span class="sxs-lookup"><span data-stu-id="95ed3-172"><a name="bk_NextSteps"> </a></span></span>

<span data-ttu-id="95ed3-173">现在，您已经了解了可用于进行故障排除的工具和资源，您可能需要帮助了解这些工具提供的信息。</span><span class="sxs-lookup"><span data-stu-id="95ed3-173">Now that you've learned about the tools and resources that you can use to troubleshoot, you might need help understanding the information provided by those tools.</span></span> <span data-ttu-id="95ed3-174">以下是获取帮助的一些选项：</span><span class="sxs-lookup"><span data-stu-id="95ed3-174">The following are some options for getting help:</span></span>
  
- <span data-ttu-id="95ed3-175">[Msdn 上的 Exchange Server 开发论坛](https://social.msdn.microsoft.com/Forums/home?category=exchangeserver)—提出 Msdn Exchange Server 开发社区的问题。</span><span class="sxs-lookup"><span data-stu-id="95ed3-175">[Exchange Server Development forum on MSDN](https://social.msdn.microsoft.com/Forums/home?category=exchangeserver) — Ask a question of the MSDN Exchange Server development community.</span></span> 
    
- <span data-ttu-id="95ed3-176">[StackOverflow](http://stackoverflow.com/tags/ews) —提出有关 StackOverflow 社区的问题。</span><span class="sxs-lookup"><span data-stu-id="95ed3-176">[StackOverflow](http://stackoverflow.com/tags/ews) — Ask a question of the StackOverflow community.</span></span> <span data-ttu-id="95ed3-177">请务必使用 "ews" 标记你的帖子。</span><span class="sxs-lookup"><span data-stu-id="95ed3-177">Be sure to tag your post with "ews".</span></span> 
    
- <span data-ttu-id="95ed3-178">[Microsoft 支持](https://support.microsoft.com/ph/730/en-us)—请联系 microsoft 支持专家以获取帮助。</span><span class="sxs-lookup"><span data-stu-id="95ed3-178">[Microsoft Support](https://support.microsoft.com/ph/730/en-us) — Contact a Microsoft support professional for assistance.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="95ed3-179">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95ed3-179">See also</span></span>


<span data-ttu-id="95ed3-180">另请参阅以下文章：</span><span class="sxs-lookup"><span data-stu-id="95ed3-180">See the following articles:</span></span>
  
- [<span data-ttu-id="95ed3-181">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="95ed3-181">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="95ed3-182">跟踪请求和响应以便解决 EWS 托管 API 应用程序的故障</span><span class="sxs-lookup"><span data-stu-id="95ed3-182">Trace requests and responses to troubleshoot EWS Managed API applications</span></span>](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [<span data-ttu-id="95ed3-183">检测对 EWS 和 REST 在 Exchange 中的客户端请求</span><span class="sxs-lookup"><span data-stu-id="95ed3-183">Instrumenting client requests for EWS and REST in Exchange</span></span>](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [<span data-ttu-id="95ed3-184">Exchange 中的 EWS 限制</span><span class="sxs-lookup"><span data-stu-id="95ed3-184">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    
- [<span data-ttu-id="95ed3-185">使用自动发现刷新配置信息</span><span class="sxs-lookup"><span data-stu-id="95ed3-185">Refresh configuration information by using Autodiscover</span></span>](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [<span data-ttu-id="95ed3-186">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="95ed3-186">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="95ed3-187">在 Exchange 中处理 EWS 中与通知相关的错误</span><span class="sxs-lookup"><span data-stu-id="95ed3-187">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="95ed3-188">在 Exchange 中处理 EWS 中与同步相关的错误</span><span class="sxs-lookup"><span data-stu-id="95ed3-188">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="95ed3-189">在 Exchange 中处理 EWS 中的与删除相关的错误</span><span class="sxs-lookup"><span data-stu-id="95ed3-189">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="95ed3-190">在 IIS 中配置日志记录</span><span class="sxs-lookup"><span data-stu-id="95ed3-190">Configuring Logging in IIS</span></span>](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [<span data-ttu-id="95ed3-191">使用 IIS 7 中的跟踪对失败请求进行故障排除</span><span class="sxs-lookup"><span data-stu-id="95ed3-191">Troubleshooting Failed Requests Using Tracing in IIS 7</span></span>](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [<span data-ttu-id="95ed3-192">引入： Log Parser Studio</span><span class="sxs-lookup"><span data-stu-id="95ed3-192">Introducing: Log Parser Studio</span></span>](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [<span data-ttu-id="95ed3-193">Exchange 虚拟目录的默认设置</span><span class="sxs-lookup"><span data-stu-id="95ed3-193">Default Settings for Exchange Virtual Directories</span></span>](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)
    
<span data-ttu-id="95ed3-194">下载以下内容：</span><span class="sxs-lookup"><span data-stu-id="95ed3-194">Download the following:</span></span>
  
- <span data-ttu-id="95ed3-195">[Microsoft Network Monitor 3.4](https://www.microsoft.com/download/details.aspx?id=4865)（Microsoft 网络监视器 3.4）</span><span class="sxs-lookup"><span data-stu-id="95ed3-195">[Microsoft Network Monitor 3.4](https://www.microsoft.com/download/details.aspx?id=4865)</span></span>
    
- [<span data-ttu-id="95ed3-196">Fiddler</span><span class="sxs-lookup"><span data-stu-id="95ed3-196">Fiddler</span></span>](http://www.telerik.com/fiddler)
    
- [<span data-ttu-id="95ed3-197">EWSEditor</span><span class="sxs-lookup"><span data-stu-id="95ed3-197">EWSEditor</span></span>](http://ewseditor.codeplex.com/)
    
- [<span data-ttu-id="95ed3-198">Exchange Web Services 托管 API</span><span class="sxs-lookup"><span data-stu-id="95ed3-198">Exchange Web Services Managed API</span></span>](https://go.microsoft.com/fwlink/?LinkID=255472)
    

