---
title: 在 Exchange 维护一组订阅和邮箱服务器之间的关联
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bda4094-88c3-4f61-9219-6ee70f6e81cf
description: 了解有关维护一组订阅和邮箱服务器之间的关联。
ms.openlocfilehash: 7cfbfb5cc19e092c37e3d48a7fcc4f27023516e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752798"
---
# <a name="maintain-affinity-between-a-group-of-subscriptions-and-the-mailbox-server-in-exchange"></a><span data-ttu-id="26d36-103">在 Exchange 维护一组订阅和邮箱服务器之间的关联</span><span class="sxs-lookup"><span data-stu-id="26d36-103">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>

<span data-ttu-id="26d36-104">了解有关维护一组订阅和邮箱服务器之间的关联。</span><span class="sxs-lookup"><span data-stu-id="26d36-104">Find out about maintaining the affinity between a group of subscriptions and the Mailbox server.</span></span>
  
<span data-ttu-id="26d36-105">关联是与特定邮箱服务器的请求和响应消息序列的关联。</span><span class="sxs-lookup"><span data-stu-id="26d36-105">Affinity is the association of a sequence of request and response messages with a particular Mailbox server.</span></span> <span data-ttu-id="26d36-106">Exchange 中的大多数功能，由服务器处理关联。</span><span class="sxs-lookup"><span data-stu-id="26d36-106">For most functionality in Exchange, affinity is handled by the server.</span></span> <span data-ttu-id="26d36-107">通知，但是，将引发异常。</span><span class="sxs-lookup"><span data-stu-id="26d36-107">Notifications, however, are an exception.</span></span> <span data-ttu-id="26d36-108">客户端是负责维护通知订阅与邮箱服务器的关联。</span><span class="sxs-lookup"><span data-stu-id="26d36-108">The client is responsible for maintaining the affinity with the Mailbox server for notification subscriptions.</span></span> <span data-ttu-id="26d36-109">启用此关联的负载平衡器和客户端和服务器到路由通知订阅和到维护订阅的邮箱服务器的相关的请求之间的客户端访问服务器。</span><span class="sxs-lookup"><span data-stu-id="26d36-109">This affinity enables the load balancer and Client Access servers between the client and the server to route notification subscriptions and related requests to the Mailbox server that maintains the subscription.</span></span> <span data-ttu-id="26d36-110">不关联，请求可能路由到不包括客户端的订阅，这会导致出错[ErrorSubscriptionNotFound](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)要返回的不同邮箱服务器。</span><span class="sxs-lookup"><span data-stu-id="26d36-110">Without affinity, the request might get routed to a different Mailbox server that does not include the client's subscriptions, which can cause an [ErrorSubscriptionNotFound](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) error to be returned.</span></span> 
  
## <a name="how-is-affinity-maintained"></a><span data-ttu-id="26d36-111">如何维护关联？</span><span class="sxs-lookup"><span data-stu-id="26d36-111">How is affinity maintained?</span></span>
<span data-ttu-id="26d36-112"><a name="bk_howmaintained"> </a></span><span class="sxs-lookup"><span data-stu-id="26d36-112"></span></span>

<span data-ttu-id="26d36-113">Exchange 中的相关性是基于 cookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-113">Affinity in Exchange is cookie based.</span></span> <span data-ttu-id="26d36-114">客户端通过在订阅请求中，包括特定的标头触发 cookie 的创建，然后订阅响应中包含的 cookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-114">The client triggers the creation of the cookie by including specific headers in the subscription request, and then the subscription response contains the cookie.</span></span> <span data-ttu-id="26d36-115">然后，客户端中进行后续请求，以确保将请求路由到正确的邮箱服务器发送的 cookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-115">The client then sends that cookie in subsequent requests to ensure that the request is routed to the right Mailbox server.</span></span>
  
<span data-ttu-id="26d36-116">更具体地说，Exchange 中的相关性是由以下处理：</span><span class="sxs-lookup"><span data-stu-id="26d36-116">More specifically, affinity in Exchange is handled by the following:</span></span> 
  
- <span data-ttu-id="26d36-117">X-AnchorMailbox — 初始订阅请求中包含的 HTTP 标头。</span><span class="sxs-lookup"><span data-stu-id="26d36-117">X-AnchorMailbox — An HTTP header that is included in the initial subscription request.</span></span> <span data-ttu-id="26d36-118">它标识的共享与同一邮箱服务器的关联邮箱的一组中的第一个邮箱。</span><span class="sxs-lookup"><span data-stu-id="26d36-118">It identifies the first mailbox in a group of mailboxes that share affinity with the same Mailbox server.</span></span>
    
- <span data-ttu-id="26d36-119">X-PreferServerAffinity — HTTP 标头的初始订阅请求 X AnchorMailbox 标头中包含，设置为 true，以指示客户端请求关联将维护与邮箱服务器。</span><span class="sxs-lookup"><span data-stu-id="26d36-119">X-PreferServerAffinity — An HTTP header that is included in the initial subscription request with the X-AnchorMailbox header and is set to true to indicate that the client is requesting that affinity be maintained with the Mailbox server.</span></span>
    
- <span data-ttu-id="26d36-120">X-BackEndOverrideCookie — cookie 初始订阅响应中包括并包含用于将后续请求路由到同一邮箱服务器的负载平衡器和客户端访问服务器的 cookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-120">X-BackEndOverrideCookie — A cookie that is included in the initial subscription response and contains a cookie that the load balancer and Client Access server use to route subsequent requests to the same Mailbox server.</span></span>
    
## <a name="how-do-i-maintain-affinity-by-using-the-ews-managed-api-or-ews"></a><span data-ttu-id="26d36-121">如何使用 EWS 托管 API 或 EWS 维护关联？</span><span class="sxs-lookup"><span data-stu-id="26d36-121">How do I maintain affinity by using the EWS Managed API or EWS?</span></span>
<span data-ttu-id="26d36-122"><a name="bk_howdoimaintain"> </a></span><span class="sxs-lookup"><span data-stu-id="26d36-122"></span></span>

<span data-ttu-id="26d36-123">您可以使用相同的步骤来维护多个邮箱订阅和其邮箱服务器，无论您使用的流式处理、 请求或推送通知的相关性和无论是否设定 Exchange 本地服务器或Exchange Online。</span><span class="sxs-lookup"><span data-stu-id="26d36-123">You can use the same steps to maintain affinity for multiple mailbox subscriptions and their Mailbox servers, regardless of whether you are using streaming, pull, or push notifications, and regardless of whether you're targeting an Exchange on-premises server or Exchange Online.</span></span>
  
1. <span data-ttu-id="26d36-124">为每个邮箱，[呼叫自动发现](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)和获取 GroupingInformation 和 ExternalEwsUrl 用户设置。</span><span class="sxs-lookup"><span data-stu-id="26d36-124">For each mailbox, [call Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) and get the GroupingInformation and ExternalEwsUrl user settings.</span></span> <span data-ttu-id="26d36-125">SOAP 自动发现，您使用的[Setting](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx)元素，并对于 POX 自动发现，您可以使用的[GroupingInformation](http://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="26d36-125">For SOAP Autodiscover, you use the [Setting](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) element, and for POX Autodiscover, you use the [GroupingInformation](http://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) element.</span></span> 
    
2. <span data-ttu-id="26d36-126">使用中的自动发现响应，具有相同的 ExternalEwsUrl 和 GroupingInformation 位置邮箱的 GroupingInformation 和 ExternalEwsUrl 设置串联同一组中的值。</span><span class="sxs-lookup"><span data-stu-id="26d36-126">Using the GroupingInformation and ExternalEwsUrl settings from the Autodiscover responses, place mailboxes with the same ExternalEwsUrl and GroupingInformation concatenated value in the same group.</span></span> <span data-ttu-id="26d36-127">如果任何组具有 200 个以上的邮箱，分解组进一步以便每个组具有不超过 200 个邮箱。</span><span class="sxs-lookup"><span data-stu-id="26d36-127">If any groups have more than 200 mailboxes, break the groups down further so that each group has no more than 200 mailboxes.</span></span>
    
3. <span data-ttu-id="26d36-128">创建和使用过程中的剩余一个[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="26d36-128">Create and use one [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) object for the rest of the procedure.</span></span> <span data-ttu-id="26d36-129">当您使用自动维护相同的**ExchangeService**对象、 cookie 和标题 （如果已设置）。</span><span class="sxs-lookup"><span data-stu-id="26d36-129">When you use the same **ExchangeService** object, cookies and headers (when they are set) are automatically maintained.</span></span> <span data-ttu-id="26d36-130">请注意，是否您不打算对单个连接到的组流式订阅，您可以自由地创建的每个模拟用户的不同**ExchangeService**对象。</span><span class="sxs-lookup"><span data-stu-id="26d36-130">Note that if you do not intend to group streaming subscriptions into a single connection, you are free to create a different **ExchangeService** object for each impersonated user.</span></span> 
    
4. <span data-ttu-id="26d36-131">其用户名首次出现时组中的所有用户的字母顺序都排序的用户[发送预订](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)请求 （我们在指此用户作为定位邮箱用户）。</span><span class="sxs-lookup"><span data-stu-id="26d36-131">[Send a subscription](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) request for the user whose user name appears first when all users in the group are sorted alphabetically (we'll refer to this user as the anchor mailbox user).</span></span> <span data-ttu-id="26d36-132">执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="26d36-132">Do the following:</span></span> 
    
  - <span data-ttu-id="26d36-133">设置为定位邮箱用户的 SMTP 地址的值包括 X AnchorMailbox 标头。</span><span class="sxs-lookup"><span data-stu-id="26d36-133">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user.</span></span>
    
  - <span data-ttu-id="26d36-134">包括 X PreferServerAffinity 标头，具有值设置为 true。</span><span class="sxs-lookup"><span data-stu-id="26d36-134">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="26d36-135">使用[通过 ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)角色 （ [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)类型）。</span><span class="sxs-lookup"><span data-stu-id="26d36-135">Use the [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
5. <span data-ttu-id="26d36-136">在订阅响应中，获取 X BackEndOverrideCookie 值。</span><span class="sxs-lookup"><span data-stu-id="26d36-136">In the subscription response, get the X-BackEndOverrideCookie value.</span></span> <span data-ttu-id="26d36-137">在每个后续预订请求此组中的用户中包含此值。</span><span class="sxs-lookup"><span data-stu-id="26d36-137">Include this value in each of the subsequent subscription requests for users in this group.</span></span>
    
6. <span data-ttu-id="26d36-138">为每个组中的其他用户，发送预订请求，并执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="26d36-138">For each additional user in the group, send a subscription request and do the following:</span></span>
    
  - <span data-ttu-id="26d36-139">设置为组定位邮箱用户的 SMTP 地址的值包括 X AnchorMailbox 标头。</span><span class="sxs-lookup"><span data-stu-id="26d36-139">Include the X-AnchorMailbox header with a value set to the SMTP address of the anchor mailbox user for the group.</span></span>
    
  - <span data-ttu-id="26d36-140">包括 X PreferServerAffinity 标头，具有值设置为 true。</span><span class="sxs-lookup"><span data-stu-id="26d36-140">Include the X-PreferServerAffinity header with a value set to true.</span></span>
    
  - <span data-ttu-id="26d36-141">包括定位邮箱用户的订阅响应中返回 X BackEndOverrideCookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-141">Include the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response.</span></span>
    
  - <span data-ttu-id="26d36-142">使用[通过 ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)角色 （ [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx)类型）。</span><span class="sxs-lookup"><span data-stu-id="26d36-142">Use the [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) role (the [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) type).</span></span> 
    
    <span data-ttu-id="26d36-143">请注意，服务器使用的 X PreferServerAffinity 和 X BackendOverrideCookie 值一起执行路由到邮箱服务器。</span><span class="sxs-lookup"><span data-stu-id="26d36-143">Note that the server uses the X-PreferServerAffinity and X-BackendOverrideCookie values together to perform the routing to the mailbox server.</span></span> <span data-ttu-id="26d36-144">X AnchorMailbox 标头也是必需的但如果其他两个值都无效，则忽略该服务器。</span><span class="sxs-lookup"><span data-stu-id="26d36-144">The X-AnchorMailbox header is also required, but is ignored by the server if the other two values are valid.</span></span> <span data-ttu-id="26d36-145">如果 X AnchorMailbox 和 X PreferServerAffinity 位于请求和 X BackendOverrideCookie 未包含，X AnchorMailbox 值用于将请求路由。</span><span class="sxs-lookup"><span data-stu-id="26d36-145">If X-AnchorMailbox and X-PreferServerAffinity are in a request and X-BackendOverrideCookie is not included, the X-AnchorMailbox value is used to route the requests.</span></span>
    
    <span data-ttu-id="26d36-146">X PreferServerAffinity 和 X BackendOverrideCookie 值执行路由，如果定位邮箱以往移动到另一个组或服务器，因为逻辑未更改，因为 X BackendOverrideCookie 将请求路由到正确的服务器组。</span><span class="sxs-lookup"><span data-stu-id="26d36-146">Because the X-PreferServerAffinity and X-BackendOverrideCookie values perform the routing, if the anchor mailbox ever moves to another group or server, the logic does not change because the X-BackendOverrideCookie will route the request to the correct server for the group.</span></span>
    
7. <span data-ttu-id="26d36-147">单个[GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx)或[GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx)请求发送组，并执行下列操作：</span><span class="sxs-lookup"><span data-stu-id="26d36-147">Send a single [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) requests for the group, and do the following:</span></span> 
    
  - <span data-ttu-id="26d36-148">包含每个组中的邮箱的单个订阅响应中返回的[SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="26d36-148">Include the [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values returned in each of the individual subscription responses for mailboxes in the group.</span></span> 
    
  - <span data-ttu-id="26d36-149">如果超过 200 订阅存在组中，创建多个请求。</span><span class="sxs-lookup"><span data-stu-id="26d36-149">If more than 200 subscriptions exist for the group, create multiple requests.</span></span> <span data-ttu-id="26d36-150">要包含在请求中的[SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx)值的最大数目是 200。</span><span class="sxs-lookup"><span data-stu-id="26d36-150">The maximum number of [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values to include in a request is 200.</span></span> 
    
  - <span data-ttu-id="26d36-151">如果您需要更多连接比供目标邮箱，，使用的服务帐户模拟组; 定位邮箱否则，不要使用模拟。</span><span class="sxs-lookup"><span data-stu-id="26d36-151">If you need more connections than are available to the target mailbox, use the service account to impersonate the anchor mailbox for the group; otherwise, do not use impersonation.</span></span> <span data-ttu-id="26d36-152">理想情况下，您想要模拟每个[GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx)或[GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx)请求唯一邮箱，以便您永远不会遇到限制的限制。</span><span class="sxs-lookup"><span data-stu-id="26d36-152">Ideally, you want to impersonate a unique mailbox per [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) or [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) request so that you never encounter throttling limits.</span></span> 
    
  - <span data-ttu-id="26d36-153">如果您需要[更多连接比供目标邮箱](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling);，使用 ApplicationImpersonation否则，不要使用 ApplicationImpersonation。</span><span class="sxs-lookup"><span data-stu-id="26d36-153">Use ApplicationImpersonation if you need [more connections than are available to the target mailbox](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling); otherwise, do not use ApplicationImpersonation.</span></span>
    
  - <span data-ttu-id="26d36-154">包括 X PreferServerAffinity 标头，并将其设置为 true。</span><span class="sxs-lookup"><span data-stu-id="26d36-154">Include the X-PreferServerAffinity header and set it to true.</span></span> <span data-ttu-id="26d36-155">如果您使用的您在步骤 2 中创建的**ExchangeService**对象，此值是自动包含。</span><span class="sxs-lookup"><span data-stu-id="26d36-155">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
  - <span data-ttu-id="26d36-156">包括组 (X-BackEndOverrideCookie 定位邮箱用户的订阅响应中返回) X BackEndOverrideCookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-156">Include the X-BackEndOverrideCookie for the group (the X-BackEndOverrideCookie that was returned in the anchor mailbox user's subscription response).</span></span> <span data-ttu-id="26d36-157">如果您使用的您在步骤 2 中创建的**ExchangeService**对象，此值是自动包含。</span><span class="sxs-lookup"><span data-stu-id="26d36-157">This value is automatically included if you are using the **ExchangeService** object that you created in step 2.</span></span> 
    
8. <span data-ttu-id="26d36-158">将返回的事件传递到单独的线程的处理。</span><span class="sxs-lookup"><span data-stu-id="26d36-158">Pass the returned events to a separate thread for processing.</span></span>
    
## <a name="what-throttling-values-do-i-need-to-take-into-consideration"></a><span data-ttu-id="26d36-159">考虑需要哪些限制值？</span><span class="sxs-lookup"><span data-stu-id="26d36-159">What throttling values do I need to take into consideration?</span></span>
<span data-ttu-id="26d36-160"><a name="bk_throttling"> </a></span><span class="sxs-lookup"><span data-stu-id="26d36-160"></span></span>

<span data-ttu-id="26d36-161">当您规划您通知的实现，您需要考虑两个值： 的连接，数和订阅数。</span><span class="sxs-lookup"><span data-stu-id="26d36-161">As you plan your notification implementation, you'll want to take two values into consideration: the number of connections, and the number of subscriptions.</span></span> <span data-ttu-id="26d36-162">下表列出了每个[限制](ews-throttling-in-exchange.md)设置的默认值和如何使用的设置。</span><span class="sxs-lookup"><span data-stu-id="26d36-162">The following table lists the default values for each [throttling](ews-throttling-in-exchange.md) setting and how the settings are used.</span></span> <span data-ttu-id="26d36-163">对于每个值，预算分配到的目标邮箱中。</span><span class="sxs-lookup"><span data-stu-id="26d36-163">For each value, the budget is allocated to the target mailbox.</span></span> <span data-ttu-id="26d36-164">因此，使用模拟即可其他连接是必需的步骤在很多情况。</span><span class="sxs-lookup"><span data-stu-id="26d36-164">For this reason, using impersonation to gain additional connections is a required step in many scenarios.</span></span> 
  
<span data-ttu-id="26d36-165">**表 1。默认限制值**</span><span class="sxs-lookup"><span data-stu-id="26d36-165">**Table 1. Default throttling values**</span></span>

|<span data-ttu-id="26d36-166">**区域的注意事项**</span><span class="sxs-lookup"><span data-stu-id="26d36-166">**Area of consideration**</span></span>|<span data-ttu-id="26d36-167">**限制设置**</span><span class="sxs-lookup"><span data-stu-id="26d36-167">**Throttling setting**</span></span>|<span data-ttu-id="26d36-168">**默认值**</span><span class="sxs-lookup"><span data-stu-id="26d36-168">**Default value**</span></span>|<span data-ttu-id="26d36-169">**说明**</span><span class="sxs-lookup"><span data-stu-id="26d36-169">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="26d36-170">流式连接</span><span class="sxs-lookup"><span data-stu-id="26d36-170">Streaming connections</span></span>  <br/> |<span data-ttu-id="26d36-171">默认悬挂连接限制</span><span class="sxs-lookup"><span data-stu-id="26d36-171">Default hanging connection limit</span></span>  <br/> |<span data-ttu-id="26d36-172">exchange 10 联机</span><span class="sxs-lookup"><span data-stu-id="26d36-172">10 for Exchange Online</span></span>  <br/> <span data-ttu-id="26d36-173">Exchange 2013 的 3</span><span class="sxs-lookup"><span data-stu-id="26d36-173">3 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="26d36-174">一次服务器上打开的最大并发帐户可以具有的流式连接数。</span><span class="sxs-lookup"><span data-stu-id="26d36-174">The maximum number of concurrent streaming connections that an account can have open on the server at one time.</span></span> <span data-ttu-id="26d36-175">要在此限制内，与通过 ApplicationImpersonation 角色分配的目标邮箱中，使用的服务帐户和时获取进行流式处理的事件模拟的第一个用户，每个订阅 ID 组中。</span><span class="sxs-lookup"><span data-stu-id="26d36-175">To work within this limit, use a service account with the ApplicationImpersonation role assigned for the target mailboxes, and impersonate the first user in each subscription ID group when getting streamed events.</span></span>  <br/> |
|<span data-ttu-id="26d36-176">提取或推送连接</span><span class="sxs-lookup"><span data-stu-id="26d36-176">Pull or push connections</span></span>  <br/> |<span data-ttu-id="26d36-177">EWSMaxConcurrency</span><span class="sxs-lookup"><span data-stu-id="26d36-177">EWSMaxConcurrency</span></span>  <br/> |<span data-ttu-id="26d36-178">27</span><span class="sxs-lookup"><span data-stu-id="26d36-178">27</span></span>  <br/> |<span data-ttu-id="26d36-179">最大并发请求订阅或推送连接 （已接收但尚未响应的请求） 数的帐户可以打开的服务器上一次。</span><span class="sxs-lookup"><span data-stu-id="26d36-179">The maximum number of concurrent pull or push connections (requests that have been received but not yet responded to) that an account can have open on the server at one time.</span></span>  <br/> |
|<span data-ttu-id="26d36-180">订阅</span><span class="sxs-lookup"><span data-stu-id="26d36-180">Subscriptions</span></span>  <br/> |<span data-ttu-id="26d36-181">EWSMaxSubscriptions</span><span class="sxs-lookup"><span data-stu-id="26d36-181">EWSMaxSubscriptions</span></span>  <br/> |<span data-ttu-id="26d36-182">20 个 exchange Online</span><span class="sxs-lookup"><span data-stu-id="26d36-182">20 for Exchange Online</span></span>  <br/> <span data-ttu-id="26d36-183">Exchange 2013 的 5000</span><span class="sxs-lookup"><span data-stu-id="26d36-183">5000 for Exchange 2013</span></span>  <br/> |<span data-ttu-id="26d36-184">最大 nonexpired 帐户可以一次的订阅数。</span><span class="sxs-lookup"><span data-stu-id="26d36-184">The maximum number of nonexpired subscriptions that an account can have at one time.</span></span> <span data-ttu-id="26d36-185">在服务器上创建订阅时，此值是递减。</span><span class="sxs-lookup"><span data-stu-id="26d36-185">This value is decremented when the subscription is created on the server.</span></span>  <br/> |
   
<span data-ttu-id="26d36-186">下面的示例演示预算任何目标邮箱和服务帐户的目标邮箱分配了[通过 ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)角色之间的处理方式。</span><span class="sxs-lookup"><span data-stu-id="26d36-186">The following example shows how budgets are handled between any target mailbox and the service account that has the [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) role assigned for the target mailboxes.</span></span> 
  
- <span data-ttu-id="26d36-187">ServiceAccount1 (sa1) 模拟许多用户 （m1、 m2、 m3，等等），并创建每个邮箱的订阅。</span><span class="sxs-lookup"><span data-stu-id="26d36-187">ServiceAccount1 (sa1) impersonates many users (m1, m2, m3, and so on) and creates subscriptions for each mailbox.</span></span> <span data-ttu-id="26d36-188">请注意，当创建订阅的订阅所有者是 sa1，以便当 sa1 订阅与打开的连接，强制实施 EWS 订阅归 sa1。</span><span class="sxs-lookup"><span data-stu-id="26d36-188">Note that when the subscriptions are created, the subscription owner is sa1, so when sa1 opens a connection with the subscriptions, EWS enforces that the subscriptions are owned by sa1.</span></span>
    
- <span data-ttu-id="26d36-189">Sa1 可以按以下方式打开连接：</span><span class="sxs-lookup"><span data-stu-id="26d36-189">Sa1 can open the connection in the following ways:</span></span>
    
1. <span data-ttu-id="26d36-190">不模拟，因此连接负责针对 sa1。</span><span class="sxs-lookup"><span data-stu-id="26d36-190">Without impersonation, so the connection is charged against sa1.</span></span>
    
2. <span data-ttu-id="26d36-191">通过模拟任何用户 — 例如 m1 —，以便连接负责对 m1 的预算的副本。</span><span class="sxs-lookup"><span data-stu-id="26d36-191">By impersonating any of the users — m1 for example — so that the connection is charged against a copy of m1's budget.</span></span> <span data-ttu-id="26d36-192">(M1 本身可以使用 Exchange Online 中，打开 10 个连接和模拟 m1 的所有服务帐户可以通过使用复制的预算都打开 10 个连接。)</span><span class="sxs-lookup"><span data-stu-id="26d36-192">(M1 itself can open ten connections by using Exchange Online, and all service accounts impersonating m1 can open ten connections by using the copied budget.)</span></span>
    
- <span data-ttu-id="26d36-193">如果已命中的连接限制，以下解决方法将可用：</span><span class="sxs-lookup"><span data-stu-id="26d36-193">If the connection limit is hit, the following workarounds are available:</span></span>
    
  - <span data-ttu-id="26d36-194">如果使用选项 1，则管理员可以创建多个服务帐户模拟其他用户。</span><span class="sxs-lookup"><span data-stu-id="26d36-194">If option 1 is used, the administrator can create multiple service accounts to impersonate additional users.</span></span>
    
  - <span data-ttu-id="26d36-195">如果使用选项 2，则该代码可模拟另一个用户 — 例如 m2。</span><span class="sxs-lookup"><span data-stu-id="26d36-195">If option 2 is used, the code can impersonate another user — m2 for example.</span></span>
    
## <a name="example-maintaining-affinity-between-a-group-of-subscriptions-and-the-mailbox-server"></a><span data-ttu-id="26d36-196">示例： 维护一组订阅和邮箱服务器之间的关联</span><span class="sxs-lookup"><span data-stu-id="26d36-196">Example: Maintaining affinity between a group of subscriptions and the Mailbox server</span></span>
<span data-ttu-id="26d36-197"><a name="bk_ce"> </a></span><span class="sxs-lookup"><span data-stu-id="26d36-197"></span></span>

<span data-ttu-id="26d36-198">一样，看它在操作。</span><span class="sxs-lookup"><span data-stu-id="26d36-198">Okay, let's see it in action.</span></span> <span data-ttu-id="26d36-199">下面的代码示例演示如何组用户并使用 X AnchorMailbox 和 X PreferServerAffinity 标头和 X BackendOverrideCookie cookie 维护与邮箱服务器的关联。</span><span class="sxs-lookup"><span data-stu-id="26d36-199">The following code example shows you how to group users and use the X-AnchorMailbox and X-PreferServerAffinity headers and the X-BackendOverrideCookie cookie to maintain affinity with the Mailbox server.</span></span> <span data-ttu-id="26d36-200">因为邮件头和 cookie 的相关性的文章中的主重要性，本示例重点介绍的 EWS XML 请求和响应。</span><span class="sxs-lookup"><span data-stu-id="26d36-200">Because the headers and the cookie are of primary importance in the affinity story, this example focuses on the EWS XML requests and responses.</span></span> <span data-ttu-id="26d36-201">若要使用 EWS 托管 API 创建的订阅请求和响应正文，请参阅[有关使用 EWS 在 Exchange 邮箱事件的流通知](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)和[提取有关使用 EWS 在 Exchange 邮箱事件的通知](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="26d36-201">To use the EWS Managed API to create the body of the subscription requests and responses, see [Stream notifications about mailbox events by using EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) and [Pull notifications about mailbox events by using EWS in Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="26d36-202">本节包括的额外步骤特定于维护关联，并将标头添加到您的请求。</span><span class="sxs-lookup"><span data-stu-id="26d36-202">This section includes additional steps particular to maintaining affinity and adding the headers to your requests.</span></span>
  
<span data-ttu-id="26d36-203">本示例具有四个用户： alfred@contoso.com、 alisa@contoso.com、 ronnie@contoso.com 和 sadie@contoso.com。</span><span class="sxs-lookup"><span data-stu-id="26d36-203">This example has four users: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com, and sadie@contoso.com.</span></span> <span data-ttu-id="26d36-204">下图显示的 GroupingInformation 和 ExternalEwsUrl[自动发现设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)的用户。</span><span class="sxs-lookup"><span data-stu-id="26d36-204">The following figure shows the GroupingInformation and ExternalEwsUrl [Autodiscover settings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) for the users.</span></span> 
  
<span data-ttu-id="26d36-205">**图 1。用于组邮箱的自动发现设置**</span><span class="sxs-lookup"><span data-stu-id="26d36-205">**Figure 1. Autodiscover settings used to group mailboxes**</span></span>

![此表格显示每个用户的 GroupingInformation 和 ExternalEwsUrl 值。](media/Exchange2013_NotificationAffinityAutoDResults.png)
  
<span data-ttu-id="26d36-207">使用自动发现响应中的设置，邮箱由的 GroupingInformation 和 ExternalEwsUrl 设置串联值分组。</span><span class="sxs-lookup"><span data-stu-id="26d36-207">Using the settings from the Autodiscover responses, the mailboxes are grouped by the concatenated value of the GroupingInformation and ExternalEwsUrl settings.</span></span> <span data-ttu-id="26d36-208">本示例中，阿尔和 Sadie 具有相同的值，因此它们位于一个组和 Alisa 和 Ronnie 共享相同的值，以便它们位于另一个组。</span><span class="sxs-lookup"><span data-stu-id="26d36-208">In this example, Alfred and Sadie have the same values, so they are in one group, and Alisa and Ronnie share the same values, so they are in another group.</span></span>
  
<span data-ttu-id="26d36-209">**图 2。创建邮箱组**</span><span class="sxs-lookup"><span data-stu-id="26d36-209">**Figure 2. Creating mailbox groups**</span></span>

![此表格显示如何使用 Autodiscover 设置创建邮箱组。](media/Exchange2013_NotificationAffinityGrouping.png)
  
<span data-ttu-id="26d36-211">在此示例中，我们将专注上组 a。我们会为组 B，使用相同的步骤，但使用不同的 X AnchorMailbox 值为该组。</span><span class="sxs-lookup"><span data-stu-id="26d36-211">For the purpose of this example, we'll focus on Group A. We would use the same steps for group B, but use a different X-AnchorMailbox value for that group.</span></span>
  
<span data-ttu-id="26d36-212">使用[通过 ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)，设置为 X AnchorMailbox 标头创建订阅请求定位邮箱 (alfred@contoso.com)，其电子邮件地址和 X PreferServerAffinity 标头值为 true。</span><span class="sxs-lookup"><span data-stu-id="26d36-212">Using [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx), create the subscription request for the anchor mailbox (alfred@contoso.com), with the X-AnchorMailbox header set to the their email address and an X-PreferServerAffinity header value of true.</span></span> <span data-ttu-id="26d36-213">设置以下两个标头值将触发要创建的响应 X BackEndOverrideCookie 的服务器。</span><span class="sxs-lookup"><span data-stu-id="26d36-213">Setting these two header values will trigger the server to create an X-BackEndOverrideCookie for the response.</span></span>
  
<span data-ttu-id="26d36-214">如果您正在使用 EWS 托管 API，使用[HttpHeaders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)[Add](http://msdn.microsoft.com/EN-US/library/cy7xta5e)方法将两个标头添加到您的订阅请求，如下所示。</span><span class="sxs-lookup"><span data-stu-id="26d36-214">If you're using the EWS Managed API, use the [HttpHeaders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)[Add](http://msdn.microsoft.com/EN-US/library/cy7xta5e) method to add the two headers to your subscription request, as shown.</span></span> 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", Mailbox.SMTPAddress);
service.HttpHeaders.Add("X-PreferServerAffinity", "true");
```

<span data-ttu-id="26d36-215">因此，阿尔的订阅请求如下所示。</span><span class="sxs-lookup"><span data-stu-id="26d36-215">So Alfred's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="26d36-216">以下 XML 消息是阿尔的订阅请求的响应并包括 X BackEndOverrideCookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-216">The following XML message is the response to Alfred's subscription request, and it includes the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="26d36-217">重新发送此 cookie 用于此组中的用户的所有后续请求。</span><span class="sxs-lookup"><span data-stu-id="26d36-217">Resend this cookie for all subsequent requests for users in this group.</span></span> <span data-ttu-id="26d36-218">请注意，则响应中还包含其他 cookie，如使用 Exchange 2010 exchangecookie cookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-218">Notice that the response also contains additional cookies, such as the exchangecookie cookie used by Exchange 2010.</span></span> <span data-ttu-id="26d36-219">Exchange Online、 Exchange Online 作为 Office 365 的一部分和版本的 Exchange 开头 Exchange 2013，忽略 exchangecookie，如果它包括在后续订阅请求。</span><span class="sxs-lookup"><span data-stu-id="26d36-219">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013, ignore exchangecookie if it is included in subsequent subscription requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=ddb8c383aef34c7694132aa679744feb; expires=Thu, 25-Sep-2014 18:42:45 GMT; path=/;
    HttpOnly
Set-Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295; path=/; secure; HttpOnly
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
    expires=Wed, 25-Sep-2013 18:52:49 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="26d36-220">使用从阿尔的响应的 X BackEndOverrideCookie 和 X AnchorMailbox 标题中，为 Sadie 创建订阅请求，组 A.Sadie 订阅请求的其他成员如下所示。</span><span class="sxs-lookup"><span data-stu-id="26d36-220">Using the X-BackEndOverrideCookie from Alfred's response and the X-AnchorMailbox header, the subscription request is created for Sadie, the other member of Group A. Sadie's subscription request looks like this.</span></span>
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@consoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@consoso.com </t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="26d36-221">Sadie 的订阅响应如下所示。</span><span class="sxs-lookup"><span data-stu-id="26d36-221">Sadie's subscription response looks like this.</span></span> <span data-ttu-id="26d36-222">请注意，不包括 X BackEndOverrideCookie。</span><span class="sxs-lookup"><span data-stu-id="26d36-222">Note that it does not include the X-BackEndOverrideCookie.</span></span> <span data-ttu-id="26d36-223">客户端负责缓存将来的请求的值。</span><span class="sxs-lookup"><span data-stu-id="26d36-223">The client is responsible for caching that value for future requests.</span></span>
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=640ea858f69d47ff8cce8b44c337f6d9; path=/
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
   expires= Wed, 25-Sep-2013 18:53:06 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="26d36-224">使用订阅响应的[SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx)值，为组中的所有订阅创建[GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx)操作请求。</span><span class="sxs-lookup"><span data-stu-id="26d36-224">Using the [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) values from the subscription responses, a [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) operation request was created for all the subscriptions in the group.</span></span> <span data-ttu-id="26d36-225">有此组中的不超过 200 订阅，因为它们是所有发送一个请求中。</span><span class="sxs-lookup"><span data-stu-id="26d36-225">Because there are less than 200 subscriptions in this group, they are all sent in one request.</span></span> <span data-ttu-id="26d36-226">X PreferServerAffinity 标头被设置为 true 和 X BackEndOverrideCookie 是包含。</span><span class="sxs-lookup"><span data-stu-id="26d36-226">The X-PreferServerAffinity header is set to true and the X-BackEndOverrideCookie is included.</span></span> 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:GetStreamingEvents>
      <m:SubscriptionIds>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</t:SubscriptionId>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</t:SubscriptionId>
      </m:SubscriptionIds>
      <m:ConnectionTimeout>10</m:ConnectionTimeout>
    </m:GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="26d36-227">返回的事件然后处理传递到单独的线程。</span><span class="sxs-lookup"><span data-stu-id="26d36-227">The returned events are then passed to a separate thread for processing.</span></span>
  
## <a name="how-has-affinity-changed"></a><span data-ttu-id="26d36-228">如何更改关联？</span><span class="sxs-lookup"><span data-stu-id="26d36-228">How has affinity changed?</span></span>
<span data-ttu-id="26d36-229"><a name="bk_howchanged"> </a></span><span class="sxs-lookup"><span data-stu-id="26d36-229"></span></span>

<span data-ttu-id="26d36-230">在 Exchange 2010，订阅维护在客户端访问服务器上，如图 3 中所示。</span><span class="sxs-lookup"><span data-stu-id="26d36-230">In Exchange 2010, subscriptions are maintained on the Client Access server, as shown in Figure 3.</span></span> <span data-ttu-id="26d36-231">在版本的 Exchange 晚于 Exchange 2010，订阅将一直在邮箱服务器上，如图 4 中所示。</span><span class="sxs-lookup"><span data-stu-id="26d36-231">In versions of Exchange later than Exchange 2010, subscriptions are maintained on the Mailbox server, as shown in Figure 4.</span></span>
  
<span data-ttu-id="26d36-232">**图 3。维护 Exchange 2010 中的关联的过程**</span><span class="sxs-lookup"><span data-stu-id="26d36-232">**Figure 3. Process for maintaining affinity in Exchange 2010**</span></span>

![此插图显示 Exchange 2010 中客户端访问服务器上的活动订阅表的维护方式。](media/Exchange2013_NoficationAffinity2010.png)
  
<span data-ttu-id="26d36-234">**图 4。维护 Exchange Online 和 Exchange 2013 中的关联的过程**</span><span class="sxs-lookup"><span data-stu-id="26d36-234">**Figure 4. Process for maintaining affinity in Exchange Online and Exchange 2013**</span></span>

![此插图显示 Exchange Server 和 Exchange Online 中的负载平衡器和客户端访问服务器路由如何向维护活动订阅表的邮箱服务器发出请求。](media/Exchange2013_NoficationAffinity2013.png)
  
<span data-ttu-id="26d36-236">在 Exchange 2010 客户端仅知道负载平衡器的地址，并由服务器返回 exchangecookie 确保将请求路由到正确的客户端访问服务器。</span><span class="sxs-lookup"><span data-stu-id="26d36-236">In Exchange 2010, the client only knows the address of the load balancer, and the exchangecookie that is returned by the server ensures that the request is routed to the right Client Access server.</span></span> <span data-ttu-id="26d36-237">但是，在更高版本、 负载平衡器和客户端访问服务器角色都安装了到达的邮箱服务器之前相应路由的请求。</span><span class="sxs-lookup"><span data-stu-id="26d36-237">However, in later versions, the load balancer and the Client Access server roles both have to route the requests appropriately before they get to the Mailbox server.</span></span> <span data-ttu-id="26d36-238">若要执行，还需要其他信息，这是引入的新邮件头和 cookie 的原因。</span><span class="sxs-lookup"><span data-stu-id="26d36-238">To do that, additional information is required, which is why the new headers and cookie were introduced.</span></span> <span data-ttu-id="26d36-239">[通知订阅、 邮箱事件和 Exchange 中的 EWS](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)的文章介绍如何在 Exchange 2013 中维护订阅。</span><span class="sxs-lookup"><span data-stu-id="26d36-239">The article [Notification subscriptions, mailbox events, and EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) explains how subscriptions are maintained in Exchange 2013.</span></span> 
  
<span data-ttu-id="26d36-240">您可能会注意到 Exchange 2010 使用 exchangecookie 仍然返回更高版本。</span><span class="sxs-lookup"><span data-stu-id="26d36-240">You might notice that the exchangecookie that Exchange 2010 uses is still returned by later versions.</span></span> <span data-ttu-id="26d36-241">在请求中，包括此 cookie 中的没有损害，但更高版本的 Exchange 忽略它。</span><span class="sxs-lookup"><span data-stu-id="26d36-241">There's no harm in including this cookie in requests, but later versions of Exchange ignore it.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26d36-242">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26d36-242">See also</span></span>

- [<span data-ttu-id="26d36-243">Notification subscriptions, mailbox events, and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="26d36-243">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [<span data-ttu-id="26d36-244">有关在 Exchange 中使用 EWS 邮箱事件流通知</span><span class="sxs-lookup"><span data-stu-id="26d36-244">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="26d36-245">在 Exchange 使用 EWS 提取有关邮箱事件的通知</span><span class="sxs-lookup"><span data-stu-id="26d36-245">Pull notifications about mailbox events by using EWS in Exchange</span></span>](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [<span data-ttu-id="26d36-246">在 Exchange 处理与通知相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="26d36-246">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
- [<span data-ttu-id="26d36-247">管理 EWS 订阅关联的变化...</span><span class="sxs-lookup"><span data-stu-id="26d36-247">Changes in Managing Affinity for EWS Subscriptions…</span></span>](http://blogs.msdn.com/b/mstehle/archive/2013/04/17/changes-in-managing-affinity-for-ews-subscriptions.aspx)
- [<span data-ttu-id="26d36-248">限制在 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="26d36-248">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

