---
title: Exchange 的 EWS 客户端设计概述
manager: sethgros
ms.date: 3/11/2016
ms.audience: Developer
ms.assetid: b26f67aa-7c66-4d7d-98b3-746f26ab37f4
description: 了解使用 EWS 为 Exchange 进行开发时的设计注意事项。
localization_priority: Priority
ms.openlocfilehash: 0ac4fe1be0800008af572ebc296e004aa29d8daf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455420"
---
# <a name="ews-client-design-overview-for-exchange"></a><span data-ttu-id="67b42-103">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="67b42-103">EWS client design overview for Exchange</span></span>

<span data-ttu-id="67b42-104">了解使用 EWS 为 Exchange 进行开发时的设计注意事项。</span><span class="sxs-lookup"><span data-stu-id="67b42-104">Learn about the design considerations for developing with EWS for Exchange.</span></span> 
  
<span data-ttu-id="67b42-105">本文提供有关设计 Exchange Web 服务（EWS）应用程序的概述信息。</span><span class="sxs-lookup"><span data-stu-id="67b42-105">This article provides overview information about designing an Exchange Web Services (EWS) application.</span></span> <span data-ttu-id="67b42-106">您可以使用此信息来确定 EWS 是否为您的应用程序正确的 API，如果是，则应使用哪种类型的客户端实现。</span><span class="sxs-lookup"><span data-stu-id="67b42-106">You can use this information to determine whether EWS is the right API for your application, and if so, what type of client implementation you should use.</span></span> <span data-ttu-id="67b42-107">本文还提供了最佳实践信息，用于设计可将 Office 365、Exchange Online 和 Exchange 的版本从 Exchange 2007、一个代码库和目标目标本地 Exchange 服务器（与目标 Exchange Online 相关的重要决策点）组成的应用程序。</span><span class="sxs-lookup"><span data-stu-id="67b42-107">This article also provides best practice information for designing applications that can target Office 365, Exchange Online, and versions of Exchange starting with Exchange 2007, in one code base, and important decision points for targeting on-premises Exchange servers versus targeting Exchange Online.</span></span>
  
## <a name="is-ews-the-right-api-for-your-application"></a><span data-ttu-id="67b42-108">是否适合您的应用程序的 EWS API？</span><span class="sxs-lookup"><span data-stu-id="67b42-108">Is EWS the right API for your application?</span></span>
<span data-ttu-id="67b42-109"><a name="IsEWSRight"> </a></span><span class="sxs-lookup"><span data-stu-id="67b42-109"><a name="IsEWSRight"> </a></span></span>

<span data-ttu-id="67b42-110">在开始设计应用程序之前，请务必考虑 EWS 是否为你提供了正确的 API。</span><span class="sxs-lookup"><span data-stu-id="67b42-110">Before you begin to design your application, it is important to consider whether EWS is the right API for you.</span></span> <span data-ttu-id="67b42-111">如果要针对 Exchange Server 或 Exchange Online 进行开发，则 EWS 是首选的客户端访问技术。</span><span class="sxs-lookup"><span data-stu-id="67b42-111">If you are developing against Exchange Server or Exchange Online, EWS is the preferred client access technology.</span></span> <span data-ttu-id="67b42-112">从 Exchange 2007 开始的 Exchange 版本的客户端访问开发主要是以 EWS 为重点。</span><span class="sxs-lookup"><span data-stu-id="67b42-112">Client access development for versions of Exchange starting with Exchange 2007 has primarily been focused on EWS.</span></span> <span data-ttu-id="67b42-113">在 Outlook 中实施的新客户端访问功能使用 EWS，包括 Exchange 2007 中引入的外出（OOF）和可用性功能，以及 Exchange 2010 中引入的邮件提示和获取聊天室功能。</span><span class="sxs-lookup"><span data-stu-id="67b42-113">New client access functionality that is implemented in Outlook uses EWS, including the Out of Office (OOF) and Availability features introduced in Exchange 2007, and the MailTips and Get Rooms functionality introduced in Exchange 2010.</span></span> <span data-ttu-id="67b42-114">这表示开发 Exchange 客户端应用程序的内部和外部合作伙伴在 EWS 中提交的投资。</span><span class="sxs-lookup"><span data-stu-id="67b42-114">This represents a committed investment in EWS for both internal and external partners who develop Exchange client applications.</span></span>
  
<span data-ttu-id="67b42-115">EWS 是您的 Exchange 客户端应用程序的主要客户端访问 API。</span><span class="sxs-lookup"><span data-stu-id="67b42-115">EWS is the primary client access API for your Exchange client applications.</span></span> <span data-ttu-id="67b42-116">但是，在某些情况下，您可能会考虑其他用于客户端应用程序开发的 Exchange Api。</span><span class="sxs-lookup"><span data-stu-id="67b42-116">However, in some cases, you might consider other Exchange APIs for client application development.</span></span> <span data-ttu-id="67b42-117">例如，Exchange ActiveSync 提供了与 EWS 相比的以下优势：</span><span class="sxs-lookup"><span data-stu-id="67b42-117">For example, Exchange ActiveSync provides the following advantages over EWS:</span></span>
  
- <span data-ttu-id="67b42-118">已对 XML 结构进行了标记，以使 Exchange ActiveSync 成为一种更紧凑的协议。</span><span class="sxs-lookup"><span data-stu-id="67b42-118">The XML structure has been tokenized to make Exchange ActiveSync a more compact protocol.</span></span>  
- <span data-ttu-id="67b42-119">Exchange ActiveSync 包含用于控制客户端访问和提供其他强健的企业移动消息解决方案的策略机制。</span><span class="sxs-lookup"><span data-stu-id="67b42-119">Exchange ActiveSync contains a policy mechanism to control client access and to provide other robust enterprise mobile messaging solutions.</span></span>
    
> [!NOTE]
> <span data-ttu-id="67b42-120">您需要许可证才能开发 Exchange ActiveSync 客户端。</span><span class="sxs-lookup"><span data-stu-id="67b42-120">You need a license in order to develop Exchange ActiveSync clients.</span></span> <span data-ttu-id="67b42-121">若要了解 Exchange ActiveSync 和 EWS 之间的差异，请参阅[在 Exchange activesync 和 Exchange Web 服务（EWS）之间进行选择](https://msdn.microsoft.com/library/dn144954%28v=exchg.140%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="67b42-121">To learn about the differences between Exchange ActiveSync and EWS, see [Choosing between Exchange ActiveSync and Exchange Web Services (EWS)](https://msdn.microsoft.com/library/dn144954%28v=exchg.140%29.aspx).</span></span> 
  
<span data-ttu-id="67b42-122">MAPI RPC over HTTP 是 Exchange 客户端应用程序的另一个可编程性选项。</span><span class="sxs-lookup"><span data-stu-id="67b42-122">MAPI RPC over HTTP is another programmability option for Exchange client applications.</span></span> <span data-ttu-id="67b42-123">但是，MAPI RPC over HTTP 不提供直观的接口用于在客户端和服务器之间进行通信。</span><span class="sxs-lookup"><span data-stu-id="67b42-123">However, MAPI RPC over HTTP does not provide an intuitive interface for communicating between clients and the server.</span></span>
  
<span data-ttu-id="67b42-124">有关 Exchange 开发技术的详细信息，请参阅[在 exchange 中浏览 EWS 托管 API、ews 和 web 服务](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="67b42-124">For more information about Exchange development technologies, see [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span></span>
  
## <a name="options-for-ews-client-development"></a><span data-ttu-id="67b42-125">EWS 客户端开发的选项</span><span class="sxs-lookup"><span data-stu-id="67b42-125">Options for EWS client development</span></span>
<span data-ttu-id="67b42-126"><a name="EWSClientOptions"> </a></span><span class="sxs-lookup"><span data-stu-id="67b42-126"><a name="EWSClientOptions"> </a></span></span>

<span data-ttu-id="67b42-127">有几个选项可用于使用 EWS 针对 Exchange 进行开发。</span><span class="sxs-lookup"><span data-stu-id="67b42-127">Several options are available for developing against Exchange by using EWS.</span></span> <span data-ttu-id="67b42-128">您的最佳选择将取决于您的组织的开发平台、工具、可用的实现和应用程序要求。</span><span class="sxs-lookup"><span data-stu-id="67b42-128">The best option for you will depend on the development platform, tools, available implementations, and application requirements for your organization.</span></span> <span data-ttu-id="67b42-129">以下是可用于构建 EWS 客户端应用程序的四个主要选项：</span><span class="sxs-lookup"><span data-stu-id="67b42-129">The following are the four primary options that are available for building EWS client applications:</span></span>
  
- <span data-ttu-id="67b42-130">EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="67b42-130">The EWS Managed API</span></span>
- <span data-ttu-id="67b42-131">EWS Java API</span><span class="sxs-lookup"><span data-stu-id="67b42-131">The EWS Java API</span></span>
- <span data-ttu-id="67b42-132">EWS 自动生成代理</span><span class="sxs-lookup"><span data-stu-id="67b42-132">The EWS autogenerated proxies</span></span>
- <span data-ttu-id="67b42-133">自定义 EWS 客户端 API</span><span class="sxs-lookup"><span data-stu-id="67b42-133">A custom EWS client API</span></span>
    
### <a name="ews-managed-api"></a><span data-ttu-id="67b42-134">EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="67b42-134">EWS Managed API</span></span>

<span data-ttu-id="67b42-135">[EWS 托管 API](https://aka.ms/ews-managed-api-readme)是一个自定义 web 服务客户端。</span><span class="sxs-lookup"><span data-stu-id="67b42-135">The [EWS Managed API](https://aka.ms/ews-managed-api-readme) is a custom web service client.</span></span> <span data-ttu-id="67b42-136">它是用于 .NET Framework 应用程序的标准客户端访问 API。</span><span class="sxs-lookup"><span data-stu-id="67b42-136">It is the standard client access API for .NET Framework applications.</span></span> 
  
<span data-ttu-id="67b42-137">以下是使用 EWS 托管 API 的一些优点：</span><span class="sxs-lookup"><span data-stu-id="67b42-137">The following are some of the benefits of using the EWS Managed API:</span></span>
  
- <span data-ttu-id="67b42-138">它提供直观的对象模型。</span><span class="sxs-lookup"><span data-stu-id="67b42-138">It provides an intuitive object model.</span></span>   
- <span data-ttu-id="67b42-139">它简要介绍了 WSDL 和 schema 文件中的服务说明的复杂性。</span><span class="sxs-lookup"><span data-stu-id="67b42-139">It abstracts the complexities of the service description in the WSDL and schema files.</span></span>   
- <span data-ttu-id="67b42-140">它包括客户端业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="67b42-140">It includes client-side business logic.</span></span>   
- <span data-ttu-id="67b42-141">它处理 web 请求和响应以及对象序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="67b42-141">It handles the web requests and responses and object serialization and deserialization.</span></span>   
- <span data-ttu-id="67b42-142">它是 Microsoft 支持的。</span><span class="sxs-lookup"><span data-stu-id="67b42-142">It is Microsoft-supported.</span></span>
    
<span data-ttu-id="67b42-143">但请注意，EWS 托管 API 并不是一个完整的解决方案。</span><span class="sxs-lookup"><span data-stu-id="67b42-143">Note, however, that the EWS Managed API is not a complete solution.</span></span> <span data-ttu-id="67b42-144">在 EWS 托管 API 中不实现某些功能。</span><span class="sxs-lookup"><span data-stu-id="67b42-144">Some functionality is not implemented in the EWS Managed API.</span></span> <span data-ttu-id="67b42-145">虽然 EWS 托管 API 不实现所有 EWS 功能，但它可能是客户端应用程序开发的最佳选择，原因如下：</span><span class="sxs-lookup"><span data-stu-id="67b42-145">Although the EWS Managed API doesn't implement all EWS functionality, it might be the best choice for your client application development, for the following reasons:</span></span>
  
- <span data-ttu-id="67b42-146">您可以使用 .NET Framework 进行开发。</span><span class="sxs-lookup"><span data-stu-id="67b42-146">You can use the .NET Framework for development.</span></span>
- <span data-ttu-id="67b42-147">它除了可实现 EWS 对象模型的大多数部分之外，还实现自动发现。</span><span class="sxs-lookup"><span data-stu-id="67b42-147">It implements Autodiscover in addition to most parts of the EWS object model.</span></span>
- <span data-ttu-id="67b42-148">它实现了在[ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)类中使用 EWS 的客户端业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="67b42-148">It implements client-side business logic for working with EWS, in the [ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class.</span></span> 
    
<span data-ttu-id="67b42-149">出于以下任一原因，您可以选择使用 EWS web 服务 API 而不是 EWS 托管 API：</span><span class="sxs-lookup"><span data-stu-id="67b42-149">You might choose to use the EWS web service API instead of the EWS Managed API for any of the following reasons:</span></span>
  
- <span data-ttu-id="67b42-150">您的应用程序不使用 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="67b42-150">Your application does not use the .NET Framework.</span></span> 
- <span data-ttu-id="67b42-151">您不希望分发 EWS 托管 API 程序集。</span><span class="sxs-lookup"><span data-stu-id="67b42-151">You don't want to distribute the EWS Managed API assembly.</span></span> 
- <span data-ttu-id="67b42-152">您的应用程序使用在 EWS 托管 API 中未实现的功能。</span><span class="sxs-lookup"><span data-stu-id="67b42-152">Your application uses features that aren't implemented in the EWS Managed API.</span></span>
    
<span data-ttu-id="67b42-153">若要了解详细信息，请参阅[EWS 托管 API 客户端应用程序入门](get-started-with-ews-managed-api-client-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="67b42-153">To learn more, see [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="67b42-154">EWS 托管 API 现已作为 [GitHub](https://aka.ms/ews-managed-api-github) 上的开源项目推出。</span><span class="sxs-lookup"><span data-stu-id="67b42-154">The EWS Managed API is now available as an open source project on [GitHub](https://aka.ms/ews-managed-api-github).</span></span> <span data-ttu-id="67b42-155">你可以使用开源库进行以下操作：</span><span class="sxs-lookup"><span data-stu-id="67b42-155">You can use the open source library to:</span></span> 
> - <span data-ttu-id="67b42-156">为 API 提供缺陷修复和增强功能。</span><span class="sxs-lookup"><span data-stu-id="67b42-156">Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="67b42-157">在修补程序和增强功能在正式的版本中可用之前获取它们。</span><span class="sxs-lookup"><span data-stu-id="67b42-157">Get fixes and enhancements before they are available in an official release.</span></span>
> - <span data-ttu-id="67b42-158">访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。</span><span class="sxs-lookup"><span data-stu-id="67b42-158">Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.</span></span>
> 
> <span data-ttu-id="67b42-159">欢迎你通过 GitHub 做出[贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。</span><span class="sxs-lookup"><span data-stu-id="67b42-159">We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
### <a name="ews-java-api"></a><span data-ttu-id="67b42-160">EWS Java API</span><span class="sxs-lookup"><span data-stu-id="67b42-160">EWS Java API</span></span>

<span data-ttu-id="67b42-161">EWS Java API 是[GitHub](https://github.com/OfficeDev/ews-java-api)上的开放源代码项目，可由社区进行更新和扩展。</span><span class="sxs-lookup"><span data-stu-id="67b42-161">The EWS Java API is an open source project on [GitHub](https://github.com/OfficeDev/ews-java-api) that can be updated and extended by the community.</span></span> <span data-ttu-id="67b42-162">Stylistically 类似于[Ews 托管 API](https://msdn.microsoft.com/library/office/jj220535%28v=exchg.80%29.aspx) ，并通过线路使用 ews SOAP 请求和响应。</span><span class="sxs-lookup"><span data-stu-id="67b42-162">It is stylistically similar to the [EWS Managed API](https://msdn.microsoft.com/library/office/jj220535%28v=exchg.80%29.aspx) and uses EWS SOAP requests and responses over the wire.</span></span> <span data-ttu-id="67b42-163">尽管不能使用 EWS Java API 访问所有[EWS SOAP 操作](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)，但在[最近创建](https://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/)的开放源代码项目中，我们正在寻求社区弥补此缺口。</span><span class="sxs-lookup"><span data-stu-id="67b42-163">Although you can't access all [EWS SOAP operations](https://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) by using the EWS Java API, with the [recent creation](https://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/) of the open source project, we are looking to the community to bridge this gap.</span></span> <span data-ttu-id="67b42-164">请注意，具有适当支持合同的 Microsoft 支持将解决与 EWS SOAP 协议（而非 EWS Java API 本身）相关的任何问题。</span><span class="sxs-lookup"><span data-stu-id="67b42-164">Note that Microsoft Support, with an appropriate support contract, will address any questions related to the EWS SOAP protocol but not the EWS Java API itself.</span></span> <span data-ttu-id="67b42-165">在[GitHub](https://github.com/OfficeDev/ews-java-api)上可下载和社区贡献的 EWS Java API。</span><span class="sxs-lookup"><span data-stu-id="67b42-165">The EWS Java API is available for download and community contribution on [GitHub](https://github.com/OfficeDev/ews-java-api).</span></span>

  
### <a name="ews-autogenerated-proxies"></a><span data-ttu-id="67b42-166">EWS 自动生成代理</span><span class="sxs-lookup"><span data-stu-id="67b42-166">EWS autogenerated proxies</span></span>

<span data-ttu-id="67b42-167">自动生成的客户端 Api 是从 EWS WSDL 和 XML 架构定义生成的。</span><span class="sxs-lookup"><span data-stu-id="67b42-167">Autogenerated client APIs are generated from the EWS WSDL and XML schema definitions.</span></span> <span data-ttu-id="67b42-168">客户端对象模型生成器可用于多种语言。</span><span class="sxs-lookup"><span data-stu-id="67b42-168">Client object model generators are available for many languages.</span></span> <span data-ttu-id="67b42-169">通常情况下，自动生成的对象模型会管理对象的序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="67b42-169">In general, the autogenerated object models manage object serialization and deserialization.</span></span> <span data-ttu-id="67b42-170">它们不包括业务逻辑，并且自动生成过程通常会创建项目，以使对象模型不太直观，可供使用。</span><span class="sxs-lookup"><span data-stu-id="67b42-170">They do not include business logic and the autogeneration process often creates artifacts that make the object model less intuitive to use.</span></span> <span data-ttu-id="67b42-171">Exchange 支持涵盖客户端（而不是对象模型）发送和接收的 XML。</span><span class="sxs-lookup"><span data-stu-id="67b42-171">Exchange support covers the XML that is sent and received by the client but not the object model.</span></span>
  
### <a name="custom-ews-client-api"></a><span data-ttu-id="67b42-172">自定义 EWS 客户端 API</span><span class="sxs-lookup"><span data-stu-id="67b42-172">Custom EWS client API</span></span>

<span data-ttu-id="67b42-173">对于某些使用一小部分 EWS 功能的应用程序，您可以创建自定义客户端 API 以与 Exchange 进行通信。</span><span class="sxs-lookup"><span data-stu-id="67b42-173">For some applications that use a small set of EWS functionality, you might create a custom client API to communicate with Exchange.</span></span> <span data-ttu-id="67b42-174">这使您可以消耗更少的系统资源。</span><span class="sxs-lookup"><span data-stu-id="67b42-174">This enables you to consume fewer system resources.</span></span> <span data-ttu-id="67b42-175">对于在内存有限的设备（如运行 .NET 微框架的客户端）上运行的客户端，这非常有用。</span><span class="sxs-lookup"><span data-stu-id="67b42-175">This is useful for clients that run on memory-constrained devices, such as clients running the .NET Micro Framework.</span></span>
  
## <a name="ews-client-features"></a><span data-ttu-id="67b42-176">EWS 客户端功能</span><span class="sxs-lookup"><span data-stu-id="67b42-176">EWS client features</span></span>
<span data-ttu-id="67b42-177"><a name="EWSFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="67b42-177"><a name="EWSFeatures"> </a></span></span>

<span data-ttu-id="67b42-178">无论您选择哪种开发选项，都应考虑如何在客户端中实现 EWS 功能。</span><span class="sxs-lookup"><span data-stu-id="67b42-178">Regardless of the development option that you choose, you should consider how EWS features are implemented in your client.</span></span> <span data-ttu-id="67b42-179">功能可用性基于应用程序的目标 EWS 架构版本。</span><span class="sxs-lookup"><span data-stu-id="67b42-179">Feature availability is based on the EWS schema version that your application targets.</span></span> <span data-ttu-id="67b42-180">由于 EWS 架构是向后和向前兼容的，因此，如果您创建一个面向早期架构版本的应用程序（如 Exchange Server 2007 SP1），您的应用程序还将针对更高版本的架构版本（如 Exchange Server 2013 SP1 服务）以及 Exchange Online 运行。</span><span class="sxs-lookup"><span data-stu-id="67b42-180">Because EWS schemas are backward- and forward-compatible, if you create an application that targets an earlier schema version, such as Exchange Server 2007 SP1, your application will also work against a later schema version, such as the Exchange Server 2013 SP1 service, as well as Exchange Online.</span></span> 
  
<span data-ttu-id="67b42-181">由于功能和功能更新由架构驱动，因此我们建议使用针对要在客户端应用程序中实现的 EWS 功能的最早通用基本代码。</span><span class="sxs-lookup"><span data-stu-id="67b42-181">Because features and feature updates are driven by the schema, we recommend that you use the earliest common code base that targets the EWS features that you want to implement in your client application.</span></span> <span data-ttu-id="67b42-182">由于 Exchange 2007 SP1 架构包含几乎所有用于在 Exchange 存储中处理项目和文件夹的核心 Exchange 功能，因此许多应用程序可以面向 Exchange2007_SP1 版本。</span><span class="sxs-lookup"><span data-stu-id="67b42-182">Many applications can target the Exchange2007_SP1 version, because the Exchange 2007 SP1 schema contains almost all the core Exchange functionality for working with items and folders in the Exchange store.</span></span> <span data-ttu-id="67b42-183">我们建议您为每个 EWS 架构版本维护代码派生。</span><span class="sxs-lookup"><span data-stu-id="67b42-183">We recommend that you maintain code forks for each EWS schema version.</span></span> <span data-ttu-id="67b42-184">以下是当前可用的架构版本。</span><span class="sxs-lookup"><span data-stu-id="67b42-184">The following are the schema versions that are currently available.</span></span> 
  
```XML
  <xs:simpleType name="ExchangeVersionType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange2007" />
      <xs:enumeration value="Exchange2007_SP1" />
      <xs:enumeration value="Exchange2010" />
      <xs:enumeration value="Exchange2010_SP1" />
      <xs:enumeration value="Exchange2010_SP2" />
      <xs:enumeration value="Exchange2013" />
      <xs:enumeration value="Exchange2013_SP1" />
    </xs:restriction>
  </xs:simpleType>
```

<span data-ttu-id="67b42-185">架构版本在**ExchangeVersionType**简单类型中维护。</span><span class="sxs-lookup"><span data-stu-id="67b42-185">The schema versions are maintained in the **ExchangeVersionType** simple type.</span></span> 
  
<span data-ttu-id="67b42-186">有关每个 EWS 架构版本中提供的功能的信息，请参阅[Exchange 中的 EWS 架构版本](ews-schema-versions-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="67b42-186">For information about the features that are available in each EWS schema version, see [EWS schema versions in Exchange](ews-schema-versions-in-exchange.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="67b42-187">本节内容</span><span class="sxs-lookup"><span data-stu-id="67b42-187">In this section</span></span>
<span data-ttu-id="67b42-188"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="67b42-188"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="67b42-189">Exchange 和 EWS 托管 API 中的 Web 服务 API 功能可用性</span><span class="sxs-lookup"><span data-stu-id="67b42-189">Web service API feature availability in Exchange and the EWS Managed API</span></span>](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)   
- [<span data-ttu-id="67b42-190">Exchange 中的 EWS 架构版本</span><span class="sxs-lookup"><span data-stu-id="67b42-190">EWS schema versions in Exchange</span></span>](ews-schema-versions-in-exchange.md)  
- [<span data-ttu-id="67b42-191">Exchange 中 EWS 的配置选项</span><span class="sxs-lookup"><span data-stu-id="67b42-191">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)  
- [<span data-ttu-id="67b42-192">比较 Exchange Online 和 Exchange 本地客户端编程</span><span class="sxs-lookup"><span data-stu-id="67b42-192">Comparing Exchange Online and Exchange on-premises client programming</span></span>](comparing-exchange-online-and-exchange-on-premises-client-programming.md)   
- [<span data-ttu-id="67b42-193">Exchange 中的 EWS 限制</span><span class="sxs-lookup"><span data-stu-id="67b42-193">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)  
- [<span data-ttu-id="67b42-194">EWS 托管 API 的再分发要求</span><span class="sxs-lookup"><span data-stu-id="67b42-194">Redistribution requirements for the EWS Managed API</span></span>](redistribution-requirements-for-the-ews-managed-api.md)  
- [<span data-ttu-id="67b42-195">检测对 EWS 和 REST 在 Exchange 中的客户端请求</span><span class="sxs-lookup"><span data-stu-id="67b42-195">Instrumenting client requests for EWS and REST in Exchange</span></span>](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="67b42-196">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67b42-196">See also</span></span>
 
- [<span data-ttu-id="67b42-197">开始使用 Exchange 中的 Web 服务</span><span class="sxs-lookup"><span data-stu-id="67b42-197">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="67b42-198">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="67b42-198">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md) 
- [<span data-ttu-id="67b42-199">EWS 应用程序类型</span><span class="sxs-lookup"><span data-stu-id="67b42-199">EWS application types</span></span>](ews-application-types.md)
    

