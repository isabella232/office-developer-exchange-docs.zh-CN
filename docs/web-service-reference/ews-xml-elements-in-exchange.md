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
# <a name="ews-xml-elements-in-exchange"></a>Exchange 中的 EWS XML 元素

在 Exchange 中查找 EWS XML 元素的参考信息。
  
Exchange Web 服务（EWS）是基于 SOAP 的 web 服务，这意味着在客户端和服务器之间发送的请求和响应消息由 XML 元素组成。 本节中的文档基于在客户端和服务器之间发送的 XML 实例。 XML 实例是在 WSDL 和 schema 文件中定义的，这些文件位于承载 EWS 的虚拟目录中。 如果您是已通过身份验证的用户，则可以使用以下 Url 浏览到 WSDL 和 schema 文件，其中 \<yourclientaccessserver\> 是客户端访问服务器的名称：
  
- http:// \<yourclientaccessserver\> /ews/服务-wsdl 文件的位置。
    
- http:// \<yourclientaccessserver\> /ews/消息（xsd）-邮件架构的位置。
    
- http:// \<yourclientaccessserver\> /ews/类型 .xsd-类型架构的位置。
    
描述 EWS XML 元素的架构文件提供了可用于请求-响应邮件交互的 XML 结构的一般路线图。 在客户端和服务器之间发送的实际 XML 结构根据所调用的操作、所请求的信息和服务器端设置的不同而不同。
  
EWS WSDL 文件（wsdl.exe）不完全符合 WSDL 标准，因为它不包含 WSDL 服务定义。 这是因为，EWS 不适合在具有预定义地址的计算机上托管。 您可以使用自动发现服务来获取 EWS 终结点地址。 某些客户端对象模型生成器会分析 WSDL，并且可能会遇到错误条件，因为 WSDL 文件不包含 WSDL 服务定义。 如果您的对象模型生成器遇到错误，则可以插入占位符 WSDL 服务定义。
  
> [!TIP]
> 如果使用 .NET Framework 开发应用程序，我们建议使用[EWS 托管 API](http://aka.ms/ews-managed-api-readme)，而不是对象模型生成器。 EWS 托管 API 提供易于使用的对象模型来处理 EWS XML 的序列化和反序列化。 有关详细信息，请参阅[开始使用 EWS 托管 API 客户端应用程序](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。 
  
消息 .xsd 架构文件包含 SOAP 正文中顶级元素的元素定义。 除了错误响应代码，邮件中的大多数定义都是特定于操作的。 类型 .xsd 架构包含 SOAP 标头的定义以及在各个操作之间共享的所有通用定义。
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 引用](ews-reference-for-exchange.md)
- [Exchange 中的 EWS 操作](ews-operations-in-exchange.md)
- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
    

