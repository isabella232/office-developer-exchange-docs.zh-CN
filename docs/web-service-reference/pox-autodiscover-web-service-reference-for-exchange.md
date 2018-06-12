---
title: Exchange POX 自动发现 web 服务引用
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: 在 Exchange 查找 POX 自动发现服务的参考信息。
ms.openlocfilehash: a8797fe714fd23049094c3ec2475b93fec4282c0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826867"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a><span data-ttu-id="70e23-103">Exchange POX 自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="70e23-103">POX Autodiscover web service reference for Exchange</span></span>

<span data-ttu-id="70e23-104">在 Exchange 查找 POX 自动发现服务的参考信息。</span><span class="sxs-lookup"><span data-stu-id="70e23-104">Find reference information for the POX Autodiscover service in Exchange.</span></span>
  
<span data-ttu-id="70e23-105">自动发现服务提供了您的应用程序使用创建连接到 Exchange 服务器的配置信息。</span><span class="sxs-lookup"><span data-stu-id="70e23-105">The Autodiscover service provides the configuration information that your application uses to create a connection to an Exchange server.</span></span> <span data-ttu-id="70e23-106">您可以使用"普通旧 XML"(POX) 自动发现服务发送邮件仅组成的 XML 有效负荷，没有任何封闭的 SOAP 信封，为定位客户端应用程序必须具有才能连接到 Exchange 的设置。</span><span class="sxs-lookup"><span data-stu-id="70e23-106">You can use the "plain old XML" (POX) Autodiscover service to send messages that consist only of XML payloads, without any enclosing SOAP envelopes, in order to locate the settings that a client application must have in order to connect to Exchange.</span></span>
  
> [!NOTE]
> <span data-ttu-id="70e23-107">目标版本的 Exchange 开头 Exchange Server 2010 中的客户端，我们建议您而不是 POX 自动发现服务使用 SOAP 自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="70e23-107">For clients that target versions of Exchange starting with Exchange Server 2010, we recommend that you use the SOAP Autodiscover service instead of the POX Autodiscover service.</span></span> <span data-ttu-id="70e23-108">面向 Exchange 2007 的客户端必须使用 POX 自动发现服务。</span><span class="sxs-lookup"><span data-stu-id="70e23-108">Clients that target Exchange 2007 have to use the POX Autodiscover service.</span></span> <span data-ttu-id="70e23-109">我们建议使用.NET Framework 的客户端使用 EWS 托管 API，因为它包含可靠且经过充分测试 POX 自动发现客户端。</span><span class="sxs-lookup"><span data-stu-id="70e23-109">We recommend that clients that use the .NET Framework use the EWS Managed API because it contains a robust and well-tested POX Autodiscover client.</span></span> <span data-ttu-id="70e23-110">有关 EWS 托管 API 的详细信息，请参阅[Get started with EWS 托管 API 客户端应用程序](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="70e23-110">For more information about the EWS Managed API, see [Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="70e23-111">本节提供有关 POX 自动发现请求重定向和响应中返回的用户设置过程中的客户端和服务器之间发送的 XML 元素的信息。</span><span class="sxs-lookup"><span data-stu-id="70e23-111">This section provides information about the XML elements that are sent between the client and server during POX Autodiscover request redirections and the user settings that are returned in a response.</span></span> <span data-ttu-id="70e23-112">XML 元素引用包含元素所表示的汇总和使用元素的潜在元素层次结构的说明。</span><span class="sxs-lookup"><span data-stu-id="70e23-112">The XML element reference contains summaries of what the elements represent and a description of the potential element hierarchies that use the element.</span></span> <span data-ttu-id="70e23-113">本文档介绍了客户端和服务器之间发送的 XML 实例。</span><span class="sxs-lookup"><span data-stu-id="70e23-113">This documentation covers the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="70e23-114">POX 自动发现服务没有显式架构。</span><span class="sxs-lookup"><span data-stu-id="70e23-114">The POX Autodiscover service does not have an explicit schema.</span></span>
  
<span data-ttu-id="70e23-115">本节中的文章提供了示例以及用于使用 POX 自动发现服务中检索自动发现配置信息的邮件的说明。</span><span class="sxs-lookup"><span data-stu-id="70e23-115">The articles in this section provide examples and descriptions of the messages that are used to retrieve Autodiscover configuration information by using the POX Autodiscover service.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="70e23-116">本节内容</span><span class="sxs-lookup"><span data-stu-id="70e23-116">In this section</span></span>
<span data-ttu-id="70e23-117"><a name="bk_InThisSection"> </a></span><span class="sxs-lookup"><span data-stu-id="70e23-117"></span></span>

- [<span data-ttu-id="70e23-118">Exchange POX 自动发现请求</span><span class="sxs-lookup"><span data-stu-id="70e23-118">POX Autodiscover request for Exchange</span></span>](pox-autodiscover-request-for-exchange.md)
    
- [<span data-ttu-id="70e23-119">Exchange POX 自动发现响应</span><span class="sxs-lookup"><span data-stu-id="70e23-119">POX Autodiscover response for Exchange</span></span>](pox-autodiscover-response-for-exchange.md)
    
- [<span data-ttu-id="70e23-120">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="70e23-120">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="70e23-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70e23-121">See also</span></span>

- [<span data-ttu-id="70e23-122">Exchange 的自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="70e23-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="70e23-123">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="70e23-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)   
- [<span data-ttu-id="70e23-124">Exchange SOAP 自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="70e23-124">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="70e23-125">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="70e23-125">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    

