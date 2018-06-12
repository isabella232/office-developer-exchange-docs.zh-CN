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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754180"
---
# <a name="ews-xml-elements-in-exchange"></a>Exchange 中的 EWS XML 元素

在 Exchange 中查找参考信息的 EWS XML 元素。
  
Exchange Web Services (EWS) 是一个基于 SOAP web 服务，这意味着在客户端和服务器之间发送的请求和响应消息所组成的 XML 元素。 本节中的文档基于客户端和服务器之间发送的 XML 实例。 在承载 EWS 虚拟目录中的位置的 WSDL 和架构文件中定义的 XML 实例。 如果您是经过身份验证的用户，您可以浏览到所 WSDL 和架构文件使用以下 Url，其中\<yourclientaccessserver\>是您的客户端访问服务器的名称：
  
- http://\<yourclientaccessserver\>.com/ews/services.wsdl — WSDL 文件的位置。
    
- http://\<yourclientaccessserver\>.com/ews/messages.xsd — 消息架构的位置。
    
- http://\<yourclientaccessserver\>.com/ews/types.xsd — 类型架构的位置。
    
描述 EWS XML 元素的架构文件提供可能为请求响应消息交互的 XML 结构的常规路线图。 客户端和服务器之间发送的实际 XML 结构会有所不同，根据调用的操作、 请求的信息和服务器端设置。
  
EWS WSDL 文件、 services.wsdl，不完全符合 WSDL 标准因为它不包括 WSDL 服务定义。 这是因为 EWS 不旨在承载有预定义的地址的计算机上。 您可以使用自动发现服务获取 EWS 终结点地址。 有些客户端对象模型生成器分析 WSDL 和可能会遇到错误条件，因为 WSDL 文件不包含 WSDL 服务定义。 如果您对象模型生成器遇到错误，您可以插入 WSDL 服务定义一个占位符。
  
> [!TIP]
> 如果您使用.NET Framework 开发应用程序，我们建议您使用[EWS 托管 API](http://aka.ms/ews-managed-api-readme)，而不是对象模型生成器。 EWS 托管 API 提供了易于使用对象模型来处理的序列化和反序列化的 EWS XML。 有关详细信息，请参阅[入门 EWS 托管 API 客户端应用程序](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。 
  
Messages.xsd 架构文件包含的元素定义的 SOAP 正文中的顶级元素。 错误响应代码，除外了特定于操作大部分 messages.xsd 中的定义。 Types.xsd 架构包含 SOAP 标头的定义和共享跨操作的所有常见的定义。
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)
- [Exchange 中的 EWS 操作](ews-operations-in-exchange.md)
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
    

