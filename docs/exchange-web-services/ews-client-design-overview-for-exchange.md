---
title: EWS exchange 的客户端设计概述
manager: sethgros
ms.date: 3/11/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: b26f67aa-7c66-4d7d-98b3-746f26ab37f4
description: 了解如何使用 EWS 开发针对 Exchange 的设计注意事项。
ms.openlocfilehash: ea0e1ad3f8402d19a6163f3320a2a17f08f3ea2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752721"
---
# <a name="ews-client-design-overview-for-exchange"></a><span data-ttu-id="b3da8-103">EWS exchange 的客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="b3da8-103">EWS client design overview for Exchange</span></span>

<span data-ttu-id="b3da8-104">了解如何使用 EWS 开发针对 Exchange 的设计注意事项。</span><span class="sxs-lookup"><span data-stu-id="b3da8-104">Learn about the design considerations for developing with EWS for Exchange.</span></span> 
  
<span data-ttu-id="b3da8-105">本文提供有关设计 Exchange Web Services (EWS) 应用程序的概述信息。</span><span class="sxs-lookup"><span data-stu-id="b3da8-105">This article provides overview information about designing an Exchange Web Services (EWS) application.</span></span> <span data-ttu-id="b3da8-106">您可以使用此信息来确定是否 EWS 运行状况不用于您的应用程序的右 API 和如果哪种类型的客户端实现的则应使用。</span><span class="sxs-lookup"><span data-stu-id="b3da8-106">You can use this information to determine whether EWS is the right API for your application, and if so, what type of client implementation you should use.</span></span> <span data-ttu-id="b3da8-107">本文还提供用于设计 Office 365、 Exchange Online 和 Exchange 版本可以针对应用程序的最佳实践信息从 Exchange 2007，在一个代码库、 和面向内部部署 Exchange 的重要决策点开始与面向 Exchange Online 的服务器。</span><span class="sxs-lookup"><span data-stu-id="b3da8-107">This article also provides best practice information for designing applications that can target Office 365, Exchange Online, and versions of Exchange starting with Exchange 2007, in one code base, and important decision points for targeting on-premises Exchange servers versus targeting Exchange Online.</span></span>
  
## <a name="is-ews-the-right-api-for-your-application"></a><span data-ttu-id="b3da8-108">是 EWS 应用程序的右 API？</span><span class="sxs-lookup"><span data-stu-id="b3da8-108">Is EWS the right API for your application?</span></span>
<span data-ttu-id="b3da8-109"><a name="IsEWSRight"> </a></span><span class="sxs-lookup"><span data-stu-id="b3da8-109"></span></span>

<span data-ttu-id="b3da8-110">设计您的应用程序之前，务必要考虑 EWS 是否为您的右 API。</span><span class="sxs-lookup"><span data-stu-id="b3da8-110">Before you begin to design your application, it is important to consider whether EWS is the right API for you.</span></span> <span data-ttu-id="b3da8-111">如果您要开发针对 Exchange 服务器或 Exchange Online，EWS 运行状况不首选的客户端访问技术。</span><span class="sxs-lookup"><span data-stu-id="b3da8-111">If you are developing against Exchange Server or Exchange Online, EWS is the preferred client access technology.</span></span> <span data-ttu-id="b3da8-112">启动与 Exchange 2007 的 Exchange 版本的客户端访问开发主要已重点放在 EWS。</span><span class="sxs-lookup"><span data-stu-id="b3da8-112">Client access development for versions of Exchange starting with Exchange 2007 has primarily been focused on EWS.</span></span> <span data-ttu-id="b3da8-113">在 Outlook 中实现的新客户端访问功能使用 EWS，包括 Exchange 2007 中引入的外出 (OOF) 和可用性功能和 Exchange 2010 中引入的邮件提示和获取聊天室功能。</span><span class="sxs-lookup"><span data-stu-id="b3da8-113">New client access functionality that is implemented in Outlook uses EWS, including the Out of Office (OOF) and Availability features introduced in Exchange 2007, and the MailTips and Get Rooms functionality introduced in Exchange 2010.</span></span> <span data-ttu-id="b3da8-114">这表示用于开发 Exchange 客户端应用程序的内部和外部合作伙伴的 ews 提交的投资。</span><span class="sxs-lookup"><span data-stu-id="b3da8-114">This represents a committed investment in EWS for both internal and external partners who develop Exchange client applications.</span></span>
  
<span data-ttu-id="b3da8-115">EWS 运行状况不 Exchange 客户端应用程序的主要客户端访问 API。</span><span class="sxs-lookup"><span data-stu-id="b3da8-115">EWS is the primary client access API for your Exchange client applications.</span></span> <span data-ttu-id="b3da8-116">但是，在某些情况下，您可以考虑客户端应用程序开发的其他 Exchange Api。</span><span class="sxs-lookup"><span data-stu-id="b3da8-116">However, in some cases, you might consider other Exchange APIs for client application development.</span></span> <span data-ttu-id="b3da8-117">例如，Exchange ActiveSync 提供 EWS 通过以下优点：</span><span class="sxs-lookup"><span data-stu-id="b3da8-117">For example, Exchange ActiveSync provides the following advantages over EWS:</span></span>
  
- <span data-ttu-id="b3da8-118">XML 结构具有已标记化，以使 Exchange ActiveSync 更紧凑协议。</span><span class="sxs-lookup"><span data-stu-id="b3da8-118">The XML structure has been tokenized to make Exchange ActiveSync a more compact protocol.</span></span>  
- <span data-ttu-id="b3da8-119">Exchange ActiveSync 包含一种策略机制，以控制客户端访问并提供其他可靠的企业移动消息解决方案。</span><span class="sxs-lookup"><span data-stu-id="b3da8-119">Exchange ActiveSync contains a policy mechanism to control client access and to provide other robust enterprise mobile messaging solutions.</span></span>
    
> [!NOTE]
> <span data-ttu-id="b3da8-120">您将需要开发 Exchange ActiveSync 客户端许可证。</span><span class="sxs-lookup"><span data-stu-id="b3da8-120">You need a license in order to develop Exchange ActiveSync clients.</span></span> <span data-ttu-id="b3da8-121">若要了解有关 Exchange ActiveSync 和 EWS 之间的差异的信息，请参阅[Exchange ActiveSync 和 Exchange Web Services (EWS) 之间的选择](http://msdn.microsoft.com/en-us/library/dn144954%28v=exchg.140%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b3da8-121">To learn about the differences between Exchange ActiveSync and EWS, see [Choosing between Exchange ActiveSync and Exchange Web Services (EWS)](http://msdn.microsoft.com/en-us/library/dn144954%28v=exchg.140%29.aspx).</span></span> 
  
<span data-ttu-id="b3da8-122">MAPI over HTTP 的 RPC 是 Exchange 客户端应用程序的另一个可编程性选项。</span><span class="sxs-lookup"><span data-stu-id="b3da8-122">MAPI RPC over HTTP is another programmability option for Exchange client applications.</span></span> <span data-ttu-id="b3da8-123">但是，MAPI over HTTP 的 RPC 不提供客户端和服务器之间通信直观的界面。</span><span class="sxs-lookup"><span data-stu-id="b3da8-123">However, MAPI RPC over HTTP does not provide an intuitive interface for communicating between clients and the server.</span></span>
  
<span data-ttu-id="b3da8-124">有关 Exchange 开发技术的详细信息，请参阅[在 Exchange 浏览 EWS 托管 API 和 EWS，web services](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="b3da8-124">For more information about Exchange development technologies, see [Explore the EWS Managed API, EWS, and web services in Exchange](explore-the-ews-managed-api-ews-and-web-services-in-exchange.md).</span></span>
  
## <a name="options-for-ews-client-development"></a><span data-ttu-id="b3da8-125">EWS 客户端开发选项</span><span class="sxs-lookup"><span data-stu-id="b3da8-125">Options for EWS client development</span></span>
<span data-ttu-id="b3da8-126"><a name="EWSClientOptions"> </a></span><span class="sxs-lookup"><span data-stu-id="b3da8-126"></span></span>

<span data-ttu-id="b3da8-127">为使用 EWS 开发针对 Exchange 提供了几个选项。</span><span class="sxs-lookup"><span data-stu-id="b3da8-127">Several options are available for developing against Exchange by using EWS.</span></span> <span data-ttu-id="b3da8-128">为您的最佳选项取决于开发平台、 工具、 可实现和贵组织的应用程序要求。</span><span class="sxs-lookup"><span data-stu-id="b3da8-128">The best option for you will depend on the development platform, tools, available implementations, and application requirements for your organization.</span></span> <span data-ttu-id="b3da8-129">以下是四个主要选项可用于构建 EWS 客户端应用程序：</span><span class="sxs-lookup"><span data-stu-id="b3da8-129">The following are the four primary options that are available for building EWS client applications:</span></span>
  
- <span data-ttu-id="b3da8-130">EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="b3da8-130">The EWS Managed API</span></span>
- <span data-ttu-id="b3da8-131">EWS Java API</span><span class="sxs-lookup"><span data-stu-id="b3da8-131">The EWS Java API</span></span>
- <span data-ttu-id="b3da8-132">EWS 的自动生成代理</span><span class="sxs-lookup"><span data-stu-id="b3da8-132">The EWS autogenerated proxies</span></span>
- <span data-ttu-id="b3da8-133">自定义的 EWS 客户端 API</span><span class="sxs-lookup"><span data-stu-id="b3da8-133">A custom EWS client API</span></span>
    
### <a name="ews-managed-api"></a><span data-ttu-id="b3da8-134">EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="b3da8-134">EWS Managed API</span></span>

<span data-ttu-id="b3da8-135">[EWS 托管 API](http://aka.ms/ews-managed-api-readme)为自定义 web 服务客户端。</span><span class="sxs-lookup"><span data-stu-id="b3da8-135">The [EWS Managed API](http://aka.ms/ews-managed-api-readme) is a custom web service client.</span></span> <span data-ttu-id="b3da8-136">它是.NET Framework 应用程序的标准客户端访问 API。</span><span class="sxs-lookup"><span data-stu-id="b3da8-136">It is the standard client access API for .NET Framework applications.</span></span> 
  
<span data-ttu-id="b3da8-137">下面是一些使用 EWS 托管 API 的好处：</span><span class="sxs-lookup"><span data-stu-id="b3da8-137">The following are some of the benefits of using the EWS Managed API:</span></span>
  
- <span data-ttu-id="b3da8-138">它提供直观的对象模型。</span><span class="sxs-lookup"><span data-stu-id="b3da8-138">It provides an intuitive object model.</span></span>   
- <span data-ttu-id="b3da8-139">它使抽象化 WSDL 和架构文件中的服务说明的复杂性。</span><span class="sxs-lookup"><span data-stu-id="b3da8-139">It abstracts the complexities of the service description in the WSDL and schema files.</span></span>   
- <span data-ttu-id="b3da8-140">它包括客户端的业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="b3da8-140">It includes client-side business logic.</span></span>   
- <span data-ttu-id="b3da8-141">它处理 web 请求和响应对象序列化和反序列化操作。</span><span class="sxs-lookup"><span data-stu-id="b3da8-141">It handles the web requests and responses and object serialization and deserialization.</span></span>   
- <span data-ttu-id="b3da8-142">它是 Microsoft 支持。</span><span class="sxs-lookup"><span data-stu-id="b3da8-142">It is Microsoft-supported.</span></span>
    
<span data-ttu-id="b3da8-143">但请注意，EWS 托管 API 不是一个完整的解决方案。</span><span class="sxs-lookup"><span data-stu-id="b3da8-143">Note, however, that the EWS Managed API is not a complete solution.</span></span> <span data-ttu-id="b3da8-144">某些功能不是在 EWS 托管 API 实现的。</span><span class="sxs-lookup"><span data-stu-id="b3da8-144">Some functionality is not implemented in the EWS Managed API.</span></span> <span data-ttu-id="b3da8-145">尽管 EWS 托管 API 不实现 EWS 的所有功能，它可能的最佳选择客户端应用程序开发，原因如下：</span><span class="sxs-lookup"><span data-stu-id="b3da8-145">Although the EWS Managed API doesn't implement all EWS functionality, it might be the best choice for your client application development, for the following reasons:</span></span>
  
- <span data-ttu-id="b3da8-146">您可以使用.NET Framework 开发。</span><span class="sxs-lookup"><span data-stu-id="b3da8-146">You can use the .NET Framework for development.</span></span>
- <span data-ttu-id="b3da8-147">它还实现自动发现，除了 EWS 对象模型的大多数部件。</span><span class="sxs-lookup"><span data-stu-id="b3da8-147">It implements Autodiscover in addition to most parts of the EWS object model.</span></span>
- <span data-ttu-id="b3da8-148">它可实现 EWS， [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)类中使用的客户端的业务逻辑。</span><span class="sxs-lookup"><span data-stu-id="b3da8-148">It implements client-side business logic for working with EWS, in the [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) class.</span></span> 
    
<span data-ttu-id="b3da8-149">您可以选择使用 EWS web 服务 API 而不是 EWS 托管 API 出于以下原因之一：</span><span class="sxs-lookup"><span data-stu-id="b3da8-149">You might choose to use the EWS web service API instead of the EWS Managed API for any of the following reasons:</span></span>
  
- <span data-ttu-id="b3da8-150">您的应用程序不使用.NET Framework。</span><span class="sxs-lookup"><span data-stu-id="b3da8-150">Your application does not use the .NET Framework.</span></span> 
- <span data-ttu-id="b3da8-151">您不想要分发的 EWS 托管 API 的程序集。</span><span class="sxs-lookup"><span data-stu-id="b3da8-151">You don't want to distribute the EWS Managed API assembly.</span></span> 
- <span data-ttu-id="b3da8-152">您的应用程序使用 EWS 托管 API 中不实现的功能。</span><span class="sxs-lookup"><span data-stu-id="b3da8-152">Your application uses features that aren't implemented in the EWS Managed API.</span></span>
    
<span data-ttu-id="b3da8-153">若要了解详细信息，请参阅[入门 EWS 托管 API 客户端应用程序](get-started-with-ews-managed-api-client-applications.md)。</span><span class="sxs-lookup"><span data-stu-id="b3da8-153">To learn more, see [Get started with EWS Managed API client applications](get-started-with-ews-managed-api-client-applications.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="b3da8-154">[!注释] EWS 托管 API 现在已经作为开放源项目在 [GitHub](http://aka.ms/ews-managed-api-github) 上可用。</span><span class="sxs-lookup"><span data-stu-id="b3da8-154">The EWS Managed API is now available as an open source project on [GitHub](http://aka.ms/ews-managed-api-github).</span></span> <span data-ttu-id="b3da8-155">您可以使用开放源代码库到：</span><span class="sxs-lookup"><span data-stu-id="b3da8-155">You can use the open source library to:</span></span> 
> - <span data-ttu-id="b3da8-156">为 API 提供缺陷修复和增强功能。</span><span class="sxs-lookup"><span data-stu-id="b3da8-156">Contribute bug fixes and enhancements to the API.</span></span> 
> - <span data-ttu-id="b3da8-157">在修补程序和增强功能在正式的版本中可用之前获取它们。</span><span class="sxs-lookup"><span data-stu-id="b3da8-157">Get fixes and enhancements before they are available in an official release.</span></span>
> - <span data-ttu-id="b3da8-158">访问最全面且最新的 API 实现，将其用作参考或在新的平台上创建新库。</span><span class="sxs-lookup"><span data-stu-id="b3da8-158">Access the most comprehensive and up-to-date implementation of the API, to use as a reference or to create new libraries on new platforms.</span></span>
> 
> <span data-ttu-id="b3da8-159">我们欢迎 GitHub 通过您[的贡献](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md)。</span><span class="sxs-lookup"><span data-stu-id="b3da8-159">We welcome your [contributions](https://github.com/OfficeDev/ews-managed-api/blob/master/CONTRIBUTING.md) via GitHub.</span></span> 
  
### <a name="ews-java-api"></a><span data-ttu-id="b3da8-160">EWS Java API</span><span class="sxs-lookup"><span data-stu-id="b3da8-160">EWS Java API</span></span>

<span data-ttu-id="b3da8-161">EWS Java API 是在[GitHub](https://github.com/OfficeDev/ews-java-api)可更新并扩展由社区的开放源代码项目。</span><span class="sxs-lookup"><span data-stu-id="b3da8-161">The EWS Java API is an open source project on [GitHub](https://github.com/OfficeDev/ews-java-api) that can be updated and extended by the community.</span></span> <span data-ttu-id="b3da8-162">它 stylistically 类似于[EWS 托管 API](http://msdn.microsoft.com/en-us/library/office/jj220535%28v=exchg.80%29.aspx) ，并通过线路中使用 EWS SOAP 请求和响应。</span><span class="sxs-lookup"><span data-stu-id="b3da8-162">It is stylistically similar to the [EWS Managed API](http://msdn.microsoft.com/en-us/library/office/jj220535%28v=exchg.80%29.aspx) and uses EWS SOAP requests and responses over the wire.</span></span> <span data-ttu-id="b3da8-163">尽管您无法通过 EWS Java API，使用[最近创建](http://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/)的开放源代码项目访问所有[EWS SOAP 操作](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx)，但我们要查找到社区此桥梁。</span><span class="sxs-lookup"><span data-stu-id="b3da8-163">Although you can't access all [EWS SOAP operations](http://msdn.microsoft.com/library/cf6fd871-9a65-4f34-8557-c8c71dd7ce09%28Office.15%29.aspx) by using the EWS Java API, with the [recent creation](http://blogs.office.com/2014/08/28/open-sourcing-exchange-web-services-ews-java-api/) of the open source project, we are looking to the community to bridge this gap.</span></span> <span data-ttu-id="b3da8-164">请注意，Microsoft 支持与相应的支持合同，将解决 EWS SOAP 协议，但不是 EWS Java API 本身与相关的任何问题。</span><span class="sxs-lookup"><span data-stu-id="b3da8-164">Note that Microsoft Support, with an appropriate support contract, will address any questions related to the EWS SOAP protocol but not the EWS Java API itself.</span></span> <span data-ttu-id="b3da8-165">EWS Java API 仅供[GitHub](https://github.com/OfficeDev/ews-java-api)上下载和社区的贡献。</span><span class="sxs-lookup"><span data-stu-id="b3da8-165">The EWS Java API is available for download and community contribution on [GitHub](https://github.com/OfficeDev/ews-java-api).</span></span>
  
### <a name="ews-autogenerated-proxies"></a><span data-ttu-id="b3da8-166">EWS 自动生成的代理</span><span class="sxs-lookup"><span data-stu-id="b3da8-166">EWS autogenerated proxies</span></span>

<span data-ttu-id="b3da8-167">自动生成客户端 Api 生成从 EWS WSDL 和 XML 架构定义。</span><span class="sxs-lookup"><span data-stu-id="b3da8-167">Autogenerated client APIs are generated from the EWS WSDL and XML schema definitions.</span></span> <span data-ttu-id="b3da8-168">客户端对象模型生成器是可用于许多语言。</span><span class="sxs-lookup"><span data-stu-id="b3da8-168">Client object model generators are available for many languages.</span></span> <span data-ttu-id="b3da8-169">一般情况下，自动生成对象模型管理对象序列化和反序列化操作。</span><span class="sxs-lookup"><span data-stu-id="b3da8-169">In general, the autogenerated object models manage object serialization and deserialization.</span></span> <span data-ttu-id="b3da8-170">它们不包含业务逻辑和自动生成过程通常会使对象模型使用较低直观的项目。</span><span class="sxs-lookup"><span data-stu-id="b3da8-170">They do not include business logic and the autogeneration process often creates artifacts that make the object model less intuitive to use.</span></span> <span data-ttu-id="b3da8-171">Exchange 支持介绍发送和接收的客户端，但不是的对象模型的 XML。</span><span class="sxs-lookup"><span data-stu-id="b3da8-171">Exchange support covers the XML that is sent and received by the client but not the object model.</span></span>
  
### <a name="custom-ews-client-api"></a><span data-ttu-id="b3da8-172">自定义 EWS 客户端 API</span><span class="sxs-lookup"><span data-stu-id="b3da8-172">Custom EWS client API</span></span>

<span data-ttu-id="b3da8-173">对于某些应用程序使用一小组 EWS 功能，您可以创建自定义客户端 API 与 Exchange 进行通信。</span><span class="sxs-lookup"><span data-stu-id="b3da8-173">For some applications that use a small set of EWS functionality, you might create a custom client API to communicate with Exchange.</span></span> <span data-ttu-id="b3da8-174">这使您可以使用较少的系统资源。</span><span class="sxs-lookup"><span data-stu-id="b3da8-174">This enables you to consume fewer system resources.</span></span> <span data-ttu-id="b3da8-175">这很有用的客户端的内存约束的设备，如运行微.net 客户端上运行。</span><span class="sxs-lookup"><span data-stu-id="b3da8-175">This is useful for clients that run on memory-constrained devices, such as clients running the .NET Micro Framework.</span></span>
  
## <a name="ews-client-features"></a><span data-ttu-id="b3da8-176">EWS 客户端功能</span><span class="sxs-lookup"><span data-stu-id="b3da8-176">EWS client features</span></span>
<span data-ttu-id="b3da8-177"><a name="EWSFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="b3da8-177"></span></span>

<span data-ttu-id="b3da8-178">无论您选择的开发选项，您应考虑如何在您的客户端中实现 EWS 功能。</span><span class="sxs-lookup"><span data-stu-id="b3da8-178">Regardless of the development option that you choose, you should consider how EWS features are implemented in your client.</span></span> <span data-ttu-id="b3da8-179">功能的可用性取决于 EWS 架构版本的应用程序的目标。</span><span class="sxs-lookup"><span data-stu-id="b3da8-179">Feature availability is based on the EWS schema version that your application targets.</span></span> <span data-ttu-id="b3da8-180">因为 EWS 架构和转发-兼容，如果您创建应用程序的目标早期的架构版本，如 Exchange Server 2007 SP1，您的应用程序也能够针对更高版本的架构版本，如 Exchange Server 2013 SP1服务，以及 Exchange Online。</span><span class="sxs-lookup"><span data-stu-id="b3da8-180">Because EWS schemas are backward- and forward-compatible, if you create an application that targets an earlier schema version, such as Exchange Server 2007 SP1, your application will also work against a later schema version, such as the Exchange Server 2013 SP1 service, as well as Exchange Online.</span></span> 
  
<span data-ttu-id="b3da8-181">由于特性和功能更新驱动的架构，我们建议您在该目标您想要在客户端应用程序中实现的 EWS 功能使用最早的常见代码库。</span><span class="sxs-lookup"><span data-stu-id="b3da8-181">Because features and feature updates are driven by the schema, we recommend that you use the earliest common code base that targets the EWS features that you want to implement in your client application.</span></span> <span data-ttu-id="b3da8-182">多个应用程序可以目标 Exchange2007_SP1 版本，因为 Exchange 2007 SP1 架构包含几乎所有核心 Exchange 功能用于处理项目和 Exchange 存储中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="b3da8-182">Many applications can target the Exchange2007_SP1 version, because the Exchange 2007 SP1 schema contains almost all the core Exchange functionality for working with items and folders in the Exchange store.</span></span> <span data-ttu-id="b3da8-183">我们建议您保留对每个 EWS 架构版本代码分叉。</span><span class="sxs-lookup"><span data-stu-id="b3da8-183">We recommend that you maintain code forks for each EWS schema version.</span></span> <span data-ttu-id="b3da8-184">以下是当前可用的架构版本。</span><span class="sxs-lookup"><span data-stu-id="b3da8-184">The following are the schema versions that are currently available.</span></span> 
  
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

<span data-ttu-id="b3da8-185">架构版本会保留在**ExchangeVersionType**简单类型。</span><span class="sxs-lookup"><span data-stu-id="b3da8-185">The schema versions are maintained in the **ExchangeVersionType** simple type.</span></span> 
  
<span data-ttu-id="b3da8-186">有关每个 EWS 架构版本中可用的功能的信息，请参阅[Exchange 中的 EWS 架构版本](ews-schema-versions-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="b3da8-186">For information about the features that are available in each EWS schema version, see [EWS schema versions in Exchange](ews-schema-versions-in-exchange.md).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="b3da8-187">本节内容</span><span class="sxs-lookup"><span data-stu-id="b3da8-187">In this section</span></span>
<span data-ttu-id="b3da8-188"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="b3da8-188"></span></span>

- [<span data-ttu-id="b3da8-189">Exchange 和 EWS 托管 API 中的 web 服务 API 功能可用性</span><span class="sxs-lookup"><span data-stu-id="b3da8-189">Web service API feature availability in Exchange and the EWS Managed API</span></span>](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
    
- [<span data-ttu-id="b3da8-190">Exchange 中的 EWS 架构版本</span><span class="sxs-lookup"><span data-stu-id="b3da8-190">EWS schema versions in Exchange</span></span>](ews-schema-versions-in-exchange.md)
    
- [<span data-ttu-id="b3da8-191">Exchange 中的 EWS 的配置选项</span><span class="sxs-lookup"><span data-stu-id="b3da8-191">Configuration options for EWS in Exchange</span></span>](configuration-options-for-ews-in-exchange.md)
    
- [<span data-ttu-id="b3da8-192">比较 Exchange Online 和 Exchange 内部部署客户端编程 （英文）</span><span class="sxs-lookup"><span data-stu-id="b3da8-192">Comparing Exchange Online and Exchange on-premises client programming</span></span>](comparing-exchange-online-and-exchange-on-premises-client-programming.md)
    
- [<span data-ttu-id="b3da8-193">限制在 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="b3da8-193">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    
- [<span data-ttu-id="b3da8-194">EWS 托管 API 的重新分发要求</span><span class="sxs-lookup"><span data-stu-id="b3da8-194">Redistribution requirements for the EWS Managed API</span></span>](redistribution-requirements-for-the-ews-managed-api.md)
    
- [<span data-ttu-id="b3da8-195">在 Exchange 检测 EWS 和 REST 的客户端请求</span><span class="sxs-lookup"><span data-stu-id="b3da8-195">Instrumenting client requests for EWS and REST in Exchange</span></span>](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="b3da8-196">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b3da8-196">See also</span></span>
 
- [<span data-ttu-id="b3da8-197">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="b3da8-197">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="b3da8-198">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="b3da8-198">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md) 
- [<span data-ttu-id="b3da8-199">EWS 应用程序类型</span><span class="sxs-lookup"><span data-stu-id="b3da8-199">EWS application types</span></span>](ews-application-types.md)
    

