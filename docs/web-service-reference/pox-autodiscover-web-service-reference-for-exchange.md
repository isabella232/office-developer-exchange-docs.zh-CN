---
title: Exchange 的 POX 自动发现 web 服务参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: 查找 Exchange 中的 POX 自动发现服务的参考信息。
ms.openlocfilehash: 3c0ca368f4427be7759e2db58fb418b4822dea8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465651"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="883b3-103">Exchange 的 POX 自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="883b3-103">POX Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="883b3-104">查找 Exchange 中的 POX 自动发现服务的参考信息。</span><span class="sxs-lookup"><span data-stu-id="883b3-104">Find reference information for the POX Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="883b3-105">自动发现服务提供了您的应用程序用来创建与 Exchange 服务器的连接的配置信息。</span><span class="sxs-lookup"><span data-stu-id="883b3-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="883b3-106">您可以使用 "纯旧 XML" （POX）自动发现服务发送仅包含 XML 负载的邮件，而不使用任何封闭 SOAP 信封，以查找客户端应用程序为连接到 Exchange 所必须具有的设置。</span><span class="sxs-lookup"><span data-stu-id="883b3-106">You can use the "plain old XML" (POX) Autodiscover service to send messages that consist only of XML payloads, without any enclosing SOAP envelopes, in order to locate the settings that a client application must have in order to connect to Exchange.</span></span>
  
> [!NOTE]
> <span data-ttu-id="883b3-107">对于面向以 Exchange Server 2010 开头的 Exchange 版本的客户端，我们建议使用 SOAP 自动发现服务，而不是 POX 自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="883b3-107">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="883b3-108">目标为 Exchange 2007 的客户端必须使用 POX 自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="883b3-108">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="883b3-109">建议使用 .NET Framework 的客户端使用 EWS 托管 API，因为它包含一个可靠且经过充分测试的 POX 自动发现客户端。</span><span class="sxs-lookup"><span data-stu-id="883b3-109">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested POX Autodiscover client.</span></span> <span data-ttu-id="883b3-110">有关 EWS 托管 API 的详细信息，请参阅[开始使用 Ews 托管 api 客户端应用程序](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="883b3-110">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="883b3-111">本节提供有关在 POX 自动发现请求重定向和响应中返回的用户设置期间在客户端和服务器之间发送的 XML 元素的信息。</span><span class="sxs-lookup"><span data-stu-id="883b3-111">This section provides information about the XML elements that are sent between the client and server during POX Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="883b3-112">XML 元素引用包含元素所表示的内容的摘要，以及使用元素的潜在元素层次结构的说明。</span><span class="sxs-lookup"><span data-stu-id="883b3-112">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that use the element.</span></span> <span data-ttu-id="883b3-113">本文档包含在客户端和服务器之间发送的 XML 实例。</span><span class="sxs-lookup"><span data-stu-id="883b3-113">This documentation covers the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="883b3-114">POX 自动发现服务没有显式架构。</span><span class="sxs-lookup"><span data-stu-id="883b3-114">The POX Autodiscover service does not have an explicit schema.</span></span>
  
<span data-ttu-id="883b3-115">本节中的文章提供了用于通过使用 POX 自动发现服务检索自动发现配置信息的邮件的示例和说明。</span><span class="sxs-lookup"><span data-stu-id="883b3-115">The articles in this section provide examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the POX Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="883b3-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="883b3-116">In this section</span></span>
<span data-ttu-id="883b3-117"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="883b3-117"><a name="bk_InThisSection"> </a></span></span>

- [<span data-ttu-id="883b3-118">Exchange 的 POX 自动发现请求</span><span class="sxs-lookup"><span data-stu-id="883b3-118">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
    
- [<span data-ttu-id="883b3-119">Exchange 的 POX 自动发现响应</span><span class="sxs-lookup"><span data-stu-id="883b3-119">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)
    
- [<span data-ttu-id="883b3-120">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="883b3-120">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="883b3-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="883b3-121">See also</span></span>

- [<span data-ttu-id="883b3-122">Exchange 的自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="883b3-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="883b3-123">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="883b3-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)   
- [<span data-ttu-id="883b3-124">Exchange 的 SOAP 自动发现 web 服务参考</span><span class="sxs-lookup"><span data-stu-id="883b3-124">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="883b3-125">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="883b3-125">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

