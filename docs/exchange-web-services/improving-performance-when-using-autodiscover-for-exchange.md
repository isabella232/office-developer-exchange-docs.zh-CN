---
title: 为 Exchange 使用自动发现时提高性能
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e65ff6b2-3810-43ad-9728-27308891b193
description: 了解如何提高性能的应用程序中的自动发现过程。
ms.openlocfilehash: 844b56084b4f0b5e49b4ee095688d58ce469baca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456330"
---
# <a name="improving-performance-when-using-autodiscover-for-exchange"></a><span data-ttu-id="2b68c-103">为 Exchange 使用自动发现时提高性能</span><span class="sxs-lookup"><span data-stu-id="2b68c-103">Improving performance when using Autodiscover for Exchange</span></span>

<span data-ttu-id="2b68c-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何提高性能的应用程序中的自动发现过程。</span><span class="sxs-lookup"><span data-stu-id="2b68c-104">Learn about ways to improve the performance of the Autodiscover process in your application.</span></span>
  
<span data-ttu-id="2b68c-p101">有大量的 like 自动发现的原因。配置应用程序连接到 Exchange 无用户干预太棒了 ！如果您正在阅读本文，您可能已经知道使用和喜欢自动发现，因此我们不会在此处列出的所有原因。相反，我们将讨论潜在缺点： 性能。</span><span class="sxs-lookup"><span data-stu-id="2b68c-p101">There are a lot of reasons to like Autodiscover. Configuring your application to connect to Exchange with no user intervention is great! If you're reading this article, you probably already know all the reasons to use and love Autodiscover, so we won't list them here. Instead, we're going to talk about a potential downside: performance.</span></span>
  
<span data-ttu-id="2b68c-p102">自动发现本身不慢的过程，但它也不是本质上是 fast。[自动发现过程](autodiscover-for-exchange.md)涉及大量的网络活动，并的引入了大量的潜在的延迟。自动发现过程具有三个阶段 ；所有三个有可能影响性能：</span><span class="sxs-lookup"><span data-stu-id="2b68c-p102">Autodiscover isn't inherently a slow process, but it's not inherently fast either. The [Autodiscover process](autodiscover-for-exchange.md) involves a lot of network activity, and that introduces a lot of potential for delays. The Autodiscover process has three phases; all three have the potential to affect performance:</span></span> 
  
- <span data-ttu-id="2b68c-112">定义自动发现终结点候选池  对于在加入域的计算机上运行的应用程序，这可能会涉及[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)，这会涉及与 Active Directory 域服务 (AD DS) 进行通信。</span><span class="sxs-lookup"><span data-stu-id="2b68c-112">Defining the Autodiscover endpoint candidate pool — For applications running on domain-joined computers, this can involve [SCP lookups](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md), which involves communicating with Active Directory Domain Services (AD DS).</span></span>
    
- <span data-ttu-id="2b68c-113">尝试每个候选  这需要对每个应聘者终结点的 HTTP 请求/响应。</span><span class="sxs-lookup"><span data-stu-id="2b68c-113">Trying each candidate — This requires an HTTP request/response to each candidate endpoint.</span></span>
    
- <span data-ttu-id="2b68c-114">尝试其他选择  时在自动发现终结点候选池中的候选不产生的结果，您可以执行未经身份验证的 GET 请求 （HTTP 请求/响应） 和 DNS 查找。</span><span class="sxs-lookup"><span data-stu-id="2b68c-114">Trying other alternatives — When the candidates in your Autodiscover endpoint candidate pool don't produce results, you can do an unauthenticated GET request (HTTP request/response) and a DNS lookup.</span></span>
    
<span data-ttu-id="2b68c-p103">面上这可能看起来不太多。但是，假设其中自动发现终结点候选池是多个或两个 Url，找不到 working 一个之前在池中的最后一个 URL。延迟会变得更显著。因此，可以做什么？</span><span class="sxs-lookup"><span data-stu-id="2b68c-p103">On the surface this might not seem like much. However, imagine a scenario where the Autodiscover endpoint candidate pool is more than one or two URLs, and you don't find a working one until the last URL in your pool. The delay can become a bit more noticeable. So, what can you do?</span></span>
  
## <a name="consider-the-need-for-scp-lookup"></a><span data-ttu-id="2b68c-119">考虑需要为 SCP 查找</span><span class="sxs-lookup"><span data-stu-id="2b68c-119">Consider the need for SCP lookup</span></span>

<span data-ttu-id="2b68c-p104">存在并已配置好 SCP 对象时，他们可以加快自动发现过程。在其他情况下，但是，他们会降低它。如果在您的环境中不使用 SCP，跳过节省时间的自动发现过程的整个 SCP 查找部分。</span><span class="sxs-lookup"><span data-stu-id="2b68c-p104">When SCP objects are present and configured well, they can speed up the Autodiscover process. In other situations, however, they can slow it down. If SCP isn't used in your environment, skip the entire SCP lookup portion of the Autodiscover process to save time.</span></span>
  
<span data-ttu-id="2b68c-p105">EWS 托管 API 使该轻松： 只需将[ExchangeService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablescplookup%28v=exchg.80%29.aspx)属性设为 **false**调用[ExchangeService.AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx)方法之前。如果您正在使用[AutodiscoverService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx)类， [AutodiscoverService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.enablescplookup%28v=exchg.80%29.aspx)属性设置为 **false**在调用其任何方法之前。</span><span class="sxs-lookup"><span data-stu-id="2b68c-p105">The EWS Managed API makes this easy: just set the [ExchangeService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablescplookup%28v=exchg.80%29.aspx) property to **false** before calling the [ExchangeService.AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) method. If you're using the [AutodiscoverService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx) class, set the [AutodiscoverService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.enablescplookup%28v=exchg.80%29.aspx) property to **false** before calling any of its methods.</span></span> 
  
## <a name="use-autodiscover-less-often"></a><span data-ttu-id="2b68c-125">经常使用自动发现较少</span><span class="sxs-lookup"><span data-stu-id="2b68c-125">Use Autodiscover less often</span></span>

<span data-ttu-id="2b68c-p106">自动发现未设计为用于经常使用应用程序。自动发现后面目的是应用程序可以使用它来发现配置信息，然后缓存一段时间内的信息。如果未缓存的配置信息，请考虑添加缓存到您的应用程序，以减少使用自动发现的次数。</span><span class="sxs-lookup"><span data-stu-id="2b68c-p106">Autodiscover isn't designed to be used frequently use by applications. The intent behind Autodiscover is for an application to use it to discover configuration information, and then cache that information for a period of time. If you aren't caching configuration information, consider adding caching to your application to reduce the number of times you use Autodiscover.</span></span>
  
<span data-ttu-id="2b68c-p107">即使您已在缓存，评估缓存配置信息的时间。该标准是[刷新自动发现信息每 24 小时](how-to-refresh-configuration-information-by-using-autodiscover.md)，但您可能能够扩展该时间。您应测试与目标环境，并使用"-生存时间"提出您适合您的配置。</span><span class="sxs-lookup"><span data-stu-id="2b68c-p107">Even if you are already caching, evaluate how long you cache configuration information. The standard is to [refresh Autodiscover information every 24 hours](how-to-refresh-configuration-information-by-using-autodiscover.md), but you might be able to extend that time. You should test with your target environments and come up with a "time-to-live" for your configuration that works for you.</span></span>
  
## <a name="minimize-requested-data"></a><span data-ttu-id="2b68c-132">最小化请求的数据</span><span class="sxs-lookup"><span data-stu-id="2b68c-132">Minimize requested data</span></span>

<span data-ttu-id="2b68c-p108">If you're using the **AutodiscoverService** class in the EWS Managed API, or the [GetUserSettings 操作 (SOAP)](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx) operation via SOAP, you have direct control over what settings are returned in the response. Although you can request quite a few settings, chances are that your application only needs a handful of them. Every setting that you request requires more processing on the server, which means more time waiting for a response. Evaluate the settings you are requesting, and eliminate any that you don't need.</span><span class="sxs-lookup"><span data-stu-id="2b68c-p108">If you're using the **AutodiscoverService** class in the EWS Managed API, or the [GetUserSettings operation (SOAP)](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx) operation via SOAP, you have direct control over what settings are returned in the response. Although you can request quite a few settings, chances are that your application only needs a handful of them. Every setting that you request requires more processing on the server, which means more time waiting for a response. Evaluate the settings you are requesting, and eliminate any that you don't need.</span></span> 
  
<span data-ttu-id="2b68c-p109">如果使用的 EWS 托管 API 中的 **ExchangeService.AutodiscoverUrl** 方法，则无法更改您请求的设置。已经非常高效 ； 但是，此方法它只从 **UserSettingName 枚举**请求的 **ExternalEwsUrl** 和 [InternalEwsUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx) 设置。</span><span class="sxs-lookup"><span data-stu-id="2b68c-p109">If you're using the **ExchangeService.AutodiscoverUrl** method in the EWS Managed API, you cannot change the settings you request. However, this method is already fairly efficient; it only requests the **ExternalEwsUrl** and **InternalEwsUrl** settings from the [UserSettingName enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx).</span></span>
  
<span data-ttu-id="2b68c-139">如果您使用的 POX 自动发现服务，[您不能请求特定的属性](autodiscover-for-exchange.md#bk_Options)。</span><span class="sxs-lookup"><span data-stu-id="2b68c-139">If you're using the POX Autodiscover service, [you cannot request specific properties](autodiscover-for-exchange.md#bk_Options).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2b68c-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2b68c-140">See also</span></span>


- [<span data-ttu-id="2b68c-141">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="2b68c-141">Autodiscover for Exchange</span></span>](autodiscover-for-exchange.md)
    
- [<span data-ttu-id="2b68c-142">通过使用 Exchange 中的 SCP 查找来找到自动发现终结点</span><span class="sxs-lookup"><span data-stu-id="2b68c-142">Find Autodiscover endpoints by using SCP lookup in Exchange</span></span>](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [<span data-ttu-id="2b68c-143">使用自动发现刷新配置信息</span><span class="sxs-lookup"><span data-stu-id="2b68c-143">Refresh configuration information by using Autodiscover</span></span>](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [<span data-ttu-id="2b68c-144">ExchangeService 类</span><span class="sxs-lookup"><span data-stu-id="2b68c-144">ExchangeService class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="2b68c-145">AutodiscoverService 类</span><span class="sxs-lookup"><span data-stu-id="2b68c-145">AutodiscoverService class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx)
    

