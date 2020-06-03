---
title: Exchange 中的 EWS XML 元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- Exchange
api_type:
- schema
ms.assetid: 4653466a-a596-456f-bbff-7da4ef1d18d3
description: 在 Exchange 中查找 EWS XML 元素的参考信息。
localization_priority: Priority
ms.openlocfilehash: 29b90ad137141e30484ef804b6fcb6bb049ef3e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526114"
---
# <a name="ews-xml-elements-in-exchange"></a><span data-ttu-id="16387-103">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="16387-103">EWS XML elements in Exchange</span></span>

<span data-ttu-id="16387-104">在 Exchange 中查找 EWS XML 元素的参考信息。</span><span class="sxs-lookup"><span data-stu-id="16387-104">Find reference information for the EWS XML elements in Exchange.</span></span>
  
<span data-ttu-id="16387-105">Exchange Web 服务（EWS）是基于 SOAP 的 web 服务，这意味着在客户端和服务器之间发送的请求和响应消息由 XML 元素组成。</span><span class="sxs-lookup"><span data-stu-id="16387-105">Exchange Web Services (EWS) is a SOAP-based web service, which means that the request and response messages that are sent between the client and server are comprised of XML elements.</span></span> <span data-ttu-id="16387-106">本节中的文档基于在客户端和服务器之间发送的 XML 实例。</span><span class="sxs-lookup"><span data-stu-id="16387-106">The documentation in this section is based on the XML instances that are sent between the client and server.</span></span> <span data-ttu-id="16387-107">XML 实例是在 WSDL 和 schema 文件中定义的，这些文件位于承载 EWS 的虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="16387-107">The XML instances are defined in the WSDL and schema files that are located in the virtual directory that hosts EWS.</span></span> <span data-ttu-id="16387-108">如果您是已通过身份验证的用户，则可以使用以下 Url 浏览到 WSDL 和 schema 文件，其中 \<yourclientaccessserver\> 是客户端访问服务器的名称：</span><span class="sxs-lookup"><span data-stu-id="16387-108">If you are an authenticated user, you can browse to the WSDL and schema files by using the following URLs, where \<yourclientaccessserver\> is the name of your Client Access server:</span></span>
  
- <span data-ttu-id="16387-109">http:// \<yourclientaccessserver\> /ews/服务-wsdl 文件的位置。</span><span class="sxs-lookup"><span data-stu-id="16387-109">http://\<yourclientaccessserver\>.com/ews/services.wsdl — The location of the WSDL file.</span></span>
    
- <span data-ttu-id="16387-110">http:// \<yourclientaccessserver\> /ews/消息（xsd）-邮件架构的位置。</span><span class="sxs-lookup"><span data-stu-id="16387-110">http://\<yourclientaccessserver\>.com/ews/messages.xsd — The location of the messages schema.</span></span>
    
- <span data-ttu-id="16387-111">http:// \<yourclientaccessserver\> /ews/类型 .xsd-类型架构的位置。</span><span class="sxs-lookup"><span data-stu-id="16387-111">http://\<yourclientaccessserver\>.com/ews/types.xsd — The location of the types schema.</span></span>
    
<span data-ttu-id="16387-112">描述 EWS XML 元素的架构文件提供了可用于请求-响应邮件交互的 XML 结构的一般路线图。</span><span class="sxs-lookup"><span data-stu-id="16387-112">The schema files that describe the EWS XML elements provide a general roadmap of the XML structure that is possible for request-response message interactions.</span></span> <span data-ttu-id="16387-113">在客户端和服务器之间发送的实际 XML 结构根据所调用的操作、所请求的信息和服务器端设置的不同而不同。</span><span class="sxs-lookup"><span data-stu-id="16387-113">The actual XML structure that is sent between client and server varies according to the operation that is called, the information requested, and the server-side settings.</span></span>
  
<span data-ttu-id="16387-114">EWS WSDL 文件（wsdl.exe）不完全符合 WSDL 标准，因为它不包含 WSDL 服务定义。</span><span class="sxs-lookup"><span data-stu-id="16387-114">The EWS WSDL file, services.wsdl, does not fully conform to the WSDL standard because it does not include a WSDL service definition.</span></span> <span data-ttu-id="16387-115">这是因为，EWS 不适合在具有预定义地址的计算机上托管。</span><span class="sxs-lookup"><span data-stu-id="16387-115">This is because EWS is not designed to be hosted on a computer that has a predefined address.</span></span> <span data-ttu-id="16387-116">您可以使用自动发现服务来获取 EWS 终结点地址。</span><span class="sxs-lookup"><span data-stu-id="16387-116">You can use the Autodiscover service to get the EWS endpoint address.</span></span> <span data-ttu-id="16387-117">某些客户端对象模型生成器会分析 WSDL，并且可能会遇到错误条件，因为 WSDL 文件不包含 WSDL 服务定义。</span><span class="sxs-lookup"><span data-stu-id="16387-117">Some client-side object model generators parse the WSDL and can encounter an error condition because the WSDL file does not contain a WSDL service definition.</span></span> <span data-ttu-id="16387-118">如果您的对象模型生成器遇到错误，则可以插入占位符 WSDL 服务定义。</span><span class="sxs-lookup"><span data-stu-id="16387-118">If your object model generator encounters an error, you can insert a placeholder WSDL service definition.</span></span>
  
> [!TIP]
> <span data-ttu-id="16387-119">如果使用 .NET Framework 开发应用程序，我们建议使用[EWS 托管 API](http://aka.ms/ews-managed-api-readme)，而不是对象模型生成器。</span><span class="sxs-lookup"><span data-stu-id="16387-119">If you are using the .NET Framework to develop your application, we recommend that you use the [EWS Managed API](http://aka.ms/ews-managed-api-readme), rather than an object model generator.</span></span> <span data-ttu-id="16387-120">EWS 托管 API 提供易于使用的对象模型来处理 EWS XML 的序列化和反序列化。</span><span class="sxs-lookup"><span data-stu-id="16387-120">The EWS Managed API provides an easy-to-use object model to handle the serialization and deserialization of the EWS XML.</span></span> <span data-ttu-id="16387-121">有关详细信息，请参阅[开始使用 EWS 托管 API 客户端应用程序](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="16387-121">For more information, see [Get started with EWS Managed API client applications](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="16387-122">消息 .xsd 架构文件包含 SOAP 正文中顶级元素的元素定义。</span><span class="sxs-lookup"><span data-stu-id="16387-122">The messages.xsd schema file contains the element definitions for the top-level elements in the SOAP body.</span></span> <span data-ttu-id="16387-123">除了错误响应代码，邮件中的大多数定义都是特定于操作的。</span><span class="sxs-lookup"><span data-stu-id="16387-123">With the exception of the error response codes, most of the definitions in messages.xsd are specific to an operation.</span></span> <span data-ttu-id="16387-124">类型 .xsd 架构包含 SOAP 标头的定义以及在各个操作之间共享的所有通用定义。</span><span class="sxs-lookup"><span data-stu-id="16387-124">The types.xsd schema contains the definitions for the SOAP headers and all the common definitions that are shared across operations.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16387-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="16387-125">See also</span></span>

- [<span data-ttu-id="16387-126">Exchange 的 EWS 引用</span><span class="sxs-lookup"><span data-stu-id="16387-126">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="16387-127">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="16387-127">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
- [<span data-ttu-id="16387-128">在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务</span><span class="sxs-lookup"><span data-stu-id="16387-128">Explore the EWS Managed API, EWS, and web services in Exchange</span></span>](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [<span data-ttu-id="16387-129">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="16387-129">Start using web services in Exchange</span></span>](../exchange-web-services/start-using-web-services-in-exchange.md)
- [<span data-ttu-id="16387-130">Exchange 自动发现</span><span class="sxs-lookup"><span data-stu-id="16387-130">Autodiscover for Exchange</span></span>](../exchange-web-services/autodiscover-for-exchange.md)
    

