---
title: Exchange 的 SOAP 自动发现 web 服务参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: 在 Exchange 中查找 SOAP 自动发现服务的引用信息。
ms.openlocfilehash: bfca8e8e260a6262d12542bd6834894a2375453f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468423"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="8486d-103">Exchange 的 SOAP 自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="8486d-103">SOAP Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="8486d-104">在 Exchange 中查找 SOAP 自动发现服务的引用信息。</span><span class="sxs-lookup"><span data-stu-id="8486d-104">Find reference information for the SOAP Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="8486d-105">自动发现服务提供了您的应用程序用来创建与 Exchange 服务器的连接的配置信息。</span><span class="sxs-lookup"><span data-stu-id="8486d-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="8486d-106">您可以使用 SOAP 自动发现服务在客户端应用程序和 Exchange 服务器之间发送邮件，以找到应用程序将用于连接到 Exchange 的设置。</span><span class="sxs-lookup"><span data-stu-id="8486d-106">You can use the SOAP Autodiscover service to send messages between the client application and the Exchange server to locate the settings the application will use to connect to Exchange.</span></span> <span data-ttu-id="8486d-107">与 POX 自动发现服务不同，SOAP 自动发现服务允许对许多用户的设置进行批量自动发现请求，并更精确地控制响应中返回的设置。</span><span class="sxs-lookup"><span data-stu-id="8486d-107">Unlike the POX Autodiscover service, the SOAP Autodiscover service allows for batched Autodiscover requests for many users' settings and more granular control over which settings are returned in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8486d-108">对于面向以 Exchange Server 2010 开头的 Exchange 版本的客户端，我们建议使用 SOAP 自动发现服务（而不是 POX 自动发现服务）。</span><span class="sxs-lookup"><span data-stu-id="8486d-108">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service (instead of the POX Autodiscover service).</span></span> <span data-ttu-id="8486d-109">目标为 Exchange 2007 的客户端必须使用 POX 自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="8486d-109">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="8486d-110">建议使用 .NET Framework 的客户端使用 EWS 托管 API，因为它包含一个可靠且经过充分测试的 SOAP 自动发现客户端。</span><span class="sxs-lookup"><span data-stu-id="8486d-110">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested SOAP Autodiscover client.</span></span> <span data-ttu-id="8486d-111">有关 EWS 托管 API 的详细信息，请参阅[开始使用 Ews 托管 api 客户端应用程序](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="8486d-111">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="8486d-112">本节提供有关在 SOAP 自动发现请求重定向期间以及在响应中返回的用户设置期间在客户端和服务器之间发送的 XML 元素的信息。</span><span class="sxs-lookup"><span data-stu-id="8486d-112">This section provides information about the XML elements that are sent between the client and server during SOAP Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="8486d-113">XML 元素引用包含元素所表示的内容的摘要，以及包含元素的潜在元素层次结构的说明。</span><span class="sxs-lookup"><span data-stu-id="8486d-113">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that contain the element.</span></span> 
  
<span data-ttu-id="8486d-114">本节中的文章介绍了如何在客户端和服务器之间发送的 XML 实例。</span><span class="sxs-lookup"><span data-stu-id="8486d-114">The articles in this section describe the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="8486d-115">可以在承载 SOAP 自动发现服务的服务器的虚拟目录中找到描述这些元素的架构。</span><span class="sxs-lookup"><span data-stu-id="8486d-115">The schema that describes these elements can be found in the virtual directory of the server that hosts the SOAP Autodiscover service.</span></span>
  
<span data-ttu-id="8486d-116">本节中的 WSDL 操作主题概述了操作的功能以及操作请求和响应示例。</span><span class="sxs-lookup"><span data-stu-id="8486d-116">The WSDL operation topics in this section provide an overview of what the operation does and operation request and response examples.</span></span> <span data-ttu-id="8486d-117">您可以使用提供的版本信息来确定您要使用的功能是否在您运行的产品版本中可用。</span><span class="sxs-lookup"><span data-stu-id="8486d-117">You can use the version information provided to determine whether the features that you want to use are available in the product version that you are running.</span></span> <span data-ttu-id="8486d-118">操作主题中的示例还有助于了解在发送到服务器和从服务器发送的 SOAP 消息中包含的 XML 的结构。</span><span class="sxs-lookup"><span data-stu-id="8486d-118">The examples in the operation topics also help you to understand the structure of the XML that is included in the SOAP messages that are sent to and from the server.</span></span>
  
<span data-ttu-id="8486d-119">此部分还提供了用于通过使用 SOAP 自动发现服务检索自动发现配置信息的消息的示例和说明。</span><span class="sxs-lookup"><span data-stu-id="8486d-119">This section also provides examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the SOAP Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="8486d-120">本节内容</span><span class="sxs-lookup"><span data-stu-id="8486d-120">In this section</span></span>
<span data-ttu-id="8486d-121"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="8486d-121"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="8486d-122">GetDomainSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8486d-122">GetDomainSettings operation (SOAP)</span></span>](getdomainsettings-operation-soap.md)
    
- [<span data-ttu-id="8486d-123">GetFederationInformation 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8486d-123">GetFederationInformation operation (SOAP)</span></span>](getfederationinformation-operation-soap.md)
    
- [<span data-ttu-id="8486d-124">GetUserSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="8486d-124">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)
    
- [<span data-ttu-id="8486d-125">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="8486d-125">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)
    
- [<span data-ttu-id="8486d-126">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="8486d-126">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="8486d-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8486d-127">See also</span></span>


- [<span data-ttu-id="8486d-128">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="8486d-128">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="8486d-129">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="8486d-129">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="8486d-130">使用自动发现查找连接点</span><span class="sxs-lookup"><span data-stu-id="8486d-130">Use Autodiscover to find connection points</span></span>](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [<span data-ttu-id="8486d-131">使用自动发现从 Exchange 获取用户设置</span><span class="sxs-lookup"><span data-stu-id="8486d-131">Get user settings from Exchange by using Autodiscover</span></span>](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [<span data-ttu-id="8486d-132">获取来自 Exchange 服务器的域设置</span><span class="sxs-lookup"><span data-stu-id="8486d-132">Get domain settings from an Exchange server</span></span>](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [<span data-ttu-id="8486d-133">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="8486d-133">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

