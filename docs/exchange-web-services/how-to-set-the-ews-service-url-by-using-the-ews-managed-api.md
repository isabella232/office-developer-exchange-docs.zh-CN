---
title: 使用 EWS 托管 API 设置 EWS 服务 URL
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: cddf6525-1c04-484b-a911-56c2f0f1f7b6
description: 查找有关如何在 EMS 托管 API 应用程序中设置 EWS 服务 URL 的信息。
localization_priority: Priority
ms.openlocfilehash: 5ba79b48d4eb4fec62110448c5924de16b67ce10
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456725"
---
# <a name="set-the-ews-service-url-by-using-the-ews-managed-api"></a><span data-ttu-id="404d4-103">使用 EWS 托管 API 设置 EWS 服务 URL</span><span class="sxs-lookup"><span data-stu-id="404d4-103">Set the EWS service URL by using the EWS Managed API</span></span>

<span data-ttu-id="404d4-104">查找有关如何在 EMS 托管 API 应用程序中设置 EWS 服务 URL 的信息。</span><span class="sxs-lookup"><span data-stu-id="404d4-104">Find information about how to set the EWS service URL in your EWS Managed API application.</span></span>
  
<span data-ttu-id="404d4-p101">服务 URL 是 Exchange 用于与 Exchange Web Services (EWS) 通信的地址。当您的 EWS Managed API 应用程序具有此地址，并且有相应的权限[与 EWS 通信](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)后，即可调用 [ExchangeService 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)。内部部署 Exchange 服务器的服务 URL 可能如下所示。</span><span class="sxs-lookup"><span data-stu-id="404d4-p101">The service URL is the address that Exchange uses to communicate with Exchange Web Services (EWS). After your EWS Managed API application has this address, and has appropriate access to [communicate with EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md), it can make calls to the [ExchangeService class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx). The service URL for an on-premises Exchange server might look like the following.</span></span> 
  
```HTML
https://computer.domain.contoso.com/EWS/Exchange.asmx
```

<span data-ttu-id="404d4-p102">您可以通过多种方式在应用程序中设置 EWS URL。我们建议使用[自动发现服务](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)获取 URL，因为在大量服务器中，如果邮箱迁移到另一台服务器，URL 可能会更改。但是，因为调用自动发现可能需要一段时间，并且如果您需要在短时间内进行多次调用，可能会减缓您的应用程序的速度，您可能需要缓存从自动发现获取的 URL 值并使用此缓存值手动设置 EWS 服务 URL。这将改进应用程序的性能，只需确保当服务器上的值发生变更时使用自动发现定期更新您的缓存值即可。</span><span class="sxs-lookup"><span data-stu-id="404d4-p102">You can set the EWS URL in your application in a couple of ways. We recommend that you use the [Autodiscover service](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx) to get the URL because in a large forest of servers, the URL can change if the mailbox is migrated to another server. However, because calling Autodiscover can take some time and can slow down your application if you need to make multiple calls in a short period of time, you might want to cache the URL value you get from Autodiscover and manually set the EWS service URL with this cached value. This will improve the performance of your application; just make sure that you use Autodiscover to update your cached value periodically in case the value changes on the server.</span></span> 
  
## <a name="set-the-ews-service-url-by-using-the-autodiscover-service"></a><span data-ttu-id="404d4-112">使用自动发现服务设置 EWS 服务 URL</span><span class="sxs-lookup"><span data-stu-id="404d4-112">Set the EWS service URL by using the Autodiscover service</span></span>
<span data-ttu-id="404d4-113"><a name="bk_SetURLusingAutoDiscover"> </a></span><span class="sxs-lookup"><span data-stu-id="404d4-113"><a name="bk_SetURLusingAutoDiscover"> </a></span></span>

<span data-ttu-id="404d4-p103">[AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) 方法使用电子邮件地址设置 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 终结点，并使您的应用程序可以使用 **ExchangeService** 代理类中包含的任何方法。以下示例显示如何使用 **AutodiscoverURL** 方法。</span><span class="sxs-lookup"><span data-stu-id="404d4-p103">The [AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) method uses the email address to set the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) endpoint and enables your application to use any methods included in the **ExchangeService** proxy classes. The following example shows how to use the **AutodiscoverURL** method.</span></span> 
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.AutodiscoverUrl("User1@contoso.com");

```

## <a name="set-the-exchange-service-url-manually"></a><span data-ttu-id="404d4-116">手动设置 Exchange 服务 URL</span><span class="sxs-lookup"><span data-stu-id="404d4-116">Set the Exchange service URL manually</span></span>
<span data-ttu-id="404d4-117"><a name="bk_SetURLmanually"> </a></span><span class="sxs-lookup"><span data-stu-id="404d4-117"><a name="bk_SetURLmanually"> </a></span></span>

<span data-ttu-id="404d4-p104">以下示例显示如何使用缓存值设置 EWS 服务 URL。在执行此操作之前，确保使用自动发现服务获取 EWS URL。</span><span class="sxs-lookup"><span data-stu-id="404d4-p104">The following example shows you how to set the EWS service URL by using a cached value. Before you do this, make sure to use the Autodiscover service to get the EWS URL.</span></span>
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.Url = new Uri("https://computername.domain.contoso.com/EWS/Exchange.asmx");

```

## <a name="see-also"></a><span data-ttu-id="404d4-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="404d4-120">See also</span></span>

- [<span data-ttu-id="404d4-121">EWS 托管 API 客户端应用程序入门</span><span class="sxs-lookup"><span data-stu-id="404d4-121">Get started with EWS Managed API client applications</span></span>](get-started-with-ews-managed-api-client-applications.md)   
- [<span data-ttu-id="404d4-122">设置 Exchange 应用程序开发环境</span><span class="sxs-lookup"><span data-stu-id="404d4-122">Setting up your Exchange application development environment</span></span>](setting-up-your-exchange-application-development-environment.md)   
- [<span data-ttu-id="404d4-123">在 Exchange 中控制对 EWS 的访问</span><span class="sxs-lookup"><span data-stu-id="404d4-123">Control access to EWS in Exchange</span></span>](how-to-control-access-to-ews-in-exchange.md) 
- [<span data-ttu-id="404d4-124">使用 EWS 托管 API 与 EWS 进行通信</span><span class="sxs-lookup"><span data-stu-id="404d4-124">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)  
- [<span data-ttu-id="404d4-125">使用自动发现查找连接点</span><span class="sxs-lookup"><span data-stu-id="404d4-125">Use Autodiscover to find connection points</span></span>](how-to-use-autodiscover-to-find-connection-points.md)
    

