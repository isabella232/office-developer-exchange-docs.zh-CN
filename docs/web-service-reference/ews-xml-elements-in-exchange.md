---
title: Exchange 中的 EWS XML 元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Exchange
api_type:
- schema
ms.assetid: 4653466a-a596-456f-bbff-7da4ef1d18d3
description: 在 Exchange 中查找参考信息的 EWS XML 元素。
ms.openlocfilehash: 046a985ae4696616d28a0891ffe0aa8cc0552307
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754180"
---
# <a name="ews-xml-elements-in-exchange"></a><span data-ttu-id="0a8ed-103">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0a8ed-103">EWS XML elements in Exchange</span></span>

<span data-ttu-id="0a8ed-104">在 Exchange 中查找参考信息的 EWS XML 元素。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-104">Find reference information for the EWS XML elements in Exchange.</span></span>
  
<span data-ttu-id="0a8ed-105">Exchange Web Services (EWS) 是一个基于 SOAP web 服务，这意味着在客户端和服务器之间发送的请求和响应消息所组成的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-105">Exchange Web Services (EWS) is a SOAP-based web service, which means that the request and response messages that are sent between the client and server are comprised of XML elements.</span></span> <span data-ttu-id="0a8ed-106">本节中的文档基于客户端和服务器之间发送的 XML 实例。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-106">The documentation in this section is based on the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="0a8ed-107">在承载 EWS 虚拟目录中的位置的 WSDL 和架构文件中定义的 XML 实例。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-107">The XML instances are defined in the WSDL and schema files that are located in the virtual directory that hosts EWS.</span></span> <span data-ttu-id="0a8ed-108">如果您是经过身份验证的用户，您可以浏览到所 WSDL 和架构文件使用以下 Url，其中\<yourclientaccessserver\>是您的客户端访问服务器的名称：</span><span class="sxs-lookup"><span data-stu-id="0a8ed-108">If you are an authenticated user, you can browse to the WSDL and schema files by using the following URLs, where \<yourclientaccessserver\> is the name of your Client Access server:</span></span>
  
- <span data-ttu-id="0a8ed-109">http://\<yourclientaccessserver\>.com/ews/services.wsdl — WSDL 文件的位置。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-109">http://\<yourclientaccessserver\>.com/ews/services.wsdl — The location of the WSDL file.</span></span>
    
- <span data-ttu-id="0a8ed-110">http://\<yourclientaccessserver\>.com/ews/messages.xsd — 消息架构的位置。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-110">http://\<yourclientaccessserver\>.com/ews/messages.xsd — The location of the messages schema.</span></span>
    
- <span data-ttu-id="0a8ed-111">http://\<yourclientaccessserver\>.com/ews/types.xsd — 类型架构的位置。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-111">http://\<yourclientaccessserver\>.com/ews/types.xsd — The location of the types schema.</span></span>
    
<span data-ttu-id="0a8ed-112">描述 EWS XML 元素的架构文件提供可能为请求响应消息交互的 XML 结构的常规路线图。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-112">The schema files that describe the EWS XML elements provide a general roadmap of the XML structure that is possible for request-response message interactions.</span></span> <span data-ttu-id="0a8ed-113">客户端和服务器之间发送的实际 XML 结构会有所不同，根据调用的操作、 请求的信息和服务器端设置。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-113">The actual XML structure that is sent between client and server varies according to the operation that is called, the information requested, and the server-side settings.</span></span>
  
<span data-ttu-id="0a8ed-114">EWS WSDL 文件、 services.wsdl，不完全符合 WSDL 标准因为它不包括 WSDL 服务定义。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-114">The EWS WSDL file, services.wsdl, does not fully conform to the WSDL standard because it does not include a WSDL service definition.</span></span> <span data-ttu-id="0a8ed-115">这是因为 EWS 不旨在承载有预定义的地址的计算机上。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-115">This is because EWS is not designed to be hosted on a computer that has a predefined address.</span></span> <span data-ttu-id="0a8ed-116">您可以使用自动发现服务获取 EWS 终结点地址。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-116">You can use the Autodiscover service to get the EWS endpoint address.</span></span> <span data-ttu-id="0a8ed-117">有些客户端对象模型生成器分析 WSDL 和可能会遇到错误条件，因为 WSDL 文件不包含 WSDL 服务定义。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-117">Some client-side object model generators parse the WSDL and can encounter an error condition because the WSDL file does not contain a WSDL service definition.</span></span> <span data-ttu-id="0a8ed-118">如果您对象模型生成器遇到错误，您可以插入 WSDL 服务定义一个占位符。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-118">If your object model generator encounters an error, you can insert a placeholder WSDL service definition.</span></span>
  
> [!TIP]
> <span data-ttu-id="0a8ed-119">如果您使用.NET Framework 开发应用程序，我们建议您使用[EWS 托管 API](http://aka.ms/ews-managed-api-readme)，而不是对象模型生成器。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-119">If you are using the .NET Framework to develop your application, we recommend that you use the [EWS Managed API](http://aka.ms/ews-managed-api-readme), rather than an object model generator.</span></span> <span data-ttu-id="0a8ed-120">EWS 托管 API 提供了易于使用对象模型来处理的序列化和反序列化的 EWS XML。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-120">The EWS Managed API provides an easy-to-use object model to handle the serialization and deserialization of the EWS XML.</span></span> <span data-ttu-id="0a8ed-121">有关详细信息，请参阅[入门 EWS 托管 API 客户端应用程序](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-121">For more information, see [Get started with EWS Managed API client applications](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="0a8ed-122">Messages.xsd 架构文件包含的元素定义的 SOAP 正文中的顶级元素。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-122">The messages.xsd schema file contains the element definitions for the top-level elements in the SOAP body.</span></span> <span data-ttu-id="0a8ed-123">错误响应代码，除外了特定于操作大部分 messages.xsd 中的定义。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-123">With the exception of the error response codes, most of the definitions in messages.xsd are specific to an operation.</span></span> <span data-ttu-id="0a8ed-124">Types.xsd 架构包含 SOAP 标头的定义和共享跨操作的所有常见的定义。</span><span class="sxs-lookup"><span data-stu-id="0a8ed-124">The types.xsd schema contains the definitions for the SOAP headers and all the common definitions that are shared across operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0a8ed-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a8ed-125">See also</span></span>

- [<span data-ttu-id="0a8ed-126">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="0a8ed-126">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="0a8ed-127">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="0a8ed-127">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="0a8ed-128">在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务</span><span class="sxs-lookup"><span data-stu-id="0a8ed-128">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [<span data-ttu-id="0a8ed-129">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="0a8ed-129">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
- [<span data-ttu-id="0a8ed-130">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="0a8ed-130">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
    

