---
title: SOAP Exchange 2013 自动发现 XML 元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ae18a5b3-ae44-4cff-8654-db8028565e01
description: 在 Exchange 查找 SOAP 自动发现 web 服务的 XML 元素引用信息。
ms.openlocfilehash: 7201ef33060691df70b63d06b2045e1120b0610f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827517"
---
# <a name="soap-autodiscover-xml-elements-for-exchange-2013"></a><span data-ttu-id="263a7-103">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="263a7-103">SOAP Autodiscover XML elements for Exchange 2013</span></span>

<span data-ttu-id="263a7-104">在 Exchange 查找 SOAP 自动发现 web 服务的 XML 元素引用信息。</span><span class="sxs-lookup"><span data-stu-id="263a7-104">Find XML element reference information for the SOAP Autodiscover web service in Exchange.</span></span>
  
<span data-ttu-id="263a7-105">本节中的文档基于客户端和服务器之间发送的 SOAP 自动发现 XML 元素实例。</span><span class="sxs-lookup"><span data-stu-id="263a7-105">The documentation in this section is based on the SOAP Autodiscover XML element instances that are sent between the client and server.</span></span> <span data-ttu-id="263a7-106">此 XML 实例文档基于位于虚拟目录承载 SOAP 自动发现服务的 WSDL 和架构文件。</span><span class="sxs-lookup"><span data-stu-id="263a7-106">This XML instance documentation is based on the WSDL and schema files that are located in the virtual directory that hosts the SOAP Autodiscover service.</span></span> <span data-ttu-id="263a7-107">通过使用的 URL 类似于以下任一情况下，经过身份验证的用户可以浏览到所 WSDL 和架构文件：</span><span class="sxs-lookup"><span data-stu-id="263a7-107">Authenticated users can browse to the WSDL and schema files by using a URL that is similar to one of the following:</span></span>
  
- <span data-ttu-id="263a7-108">http://\<yourclientaccessserver\>.com/autodiscover/services.wsdl 或http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl— WSDL 文件的位置。</span><span class="sxs-lookup"><span data-stu-id="263a7-108">http://\<yourclientaccessserver\>.com/autodiscover/services.wsdl or http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/services.wsdl — The location of the WSDL file.</span></span>
    
- <span data-ttu-id="263a7-109">http://\<yourclientaccessserver\>.com/autodiscover/messages.xsd 或http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd— 消息架构的位置。</span><span class="sxs-lookup"><span data-stu-id="263a7-109">http://\<yourclientaccessserver\>.com/autodiscover/messages.xsd or http://autodiscover.\<yourclientaccessserver\>.com/autodiscover/messages.xsd — The location of the messages schema.</span></span>
    
<span data-ttu-id="263a7-110">SOAP 自动发现 WSDL 和架构文件的位置而异 Exchange 安装。</span><span class="sxs-lookup"><span data-stu-id="263a7-110">The location of the SOAP Autodiscover WSDL and schema files varies based on the Exchange installation.</span></span>
  
<span data-ttu-id="263a7-111">Messages.xsd 架构文件描述可自动发现 SOAP 标头和 SOAP 正文中发送的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="263a7-111">The messages.xsd schema file describes the XML elements that can be sent in an Autodiscover SOAP header and SOAP body.</span></span> <span data-ttu-id="263a7-112">此文件提供什么 XML 结构可为给定的请求响应消息交互的常规路线图。</span><span class="sxs-lookup"><span data-stu-id="263a7-112">This file provides a general roadmap of what the XML structure can be for a given request-response message interaction.</span></span> <span data-ttu-id="263a7-113">客户端和服务器之间发送的实际 XML 结构基于选项和使用它的上下文。</span><span class="sxs-lookup"><span data-stu-id="263a7-113">The actual XML structure that is sent between the client and server is based on the options and the context in which it is used.</span></span> <span data-ttu-id="263a7-114">架构文件定义 XML 是可能。</span><span class="sxs-lookup"><span data-stu-id="263a7-114">The schema files define what XML is possible.</span></span> <span data-ttu-id="263a7-115">实际范围的 XML，并通过线路发送基于调用的操作，将请求的信息和服务器端设置。</span><span class="sxs-lookup"><span data-stu-id="263a7-115">The actual range of XML that is sent over the wire is based on which operation is called, the requested information, and the server-side settings.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="263a7-116">相关部分</span><span class="sxs-lookup"><span data-stu-id="263a7-116">Related sections</span></span>
<span data-ttu-id="263a7-117"><a name="bk_RelatedSections"> </a></span><span class="sxs-lookup"><span data-stu-id="263a7-117"></span></span>

- [<span data-ttu-id="263a7-118">Exchange SOAP 自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="263a7-118">SOAP Autodiscover web service reference for Exchange</span></span>](soap-autodiscover-web-service-reference-for-exchange.md)
    
- [<span data-ttu-id="263a7-119">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="263a7-119">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
    
- [<span data-ttu-id="263a7-120">Exchange 统一的消息 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="263a7-120">Unified Messaging web service reference for Exchange</span></span>](unified-messaging-web-service-reference-for-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="263a7-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="263a7-121">See also</span></span>

- [<span data-ttu-id="263a7-122">Exchange 的自动发现 web 服务引用</span><span class="sxs-lookup"><span data-stu-id="263a7-122">Autodiscover web service reference for Exchange</span></span>](autodiscover-web-service-reference-for-exchange.md)
- [<span data-ttu-id="263a7-123">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="263a7-123">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
- [<span data-ttu-id="263a7-124">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="263a7-124">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
    
