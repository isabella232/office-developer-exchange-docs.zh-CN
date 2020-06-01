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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465651"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>Exchange 的 POX 自动发现 web 服务参考

查找 Exchange 中的 POX 自动发现服务的参考信息。
  
自动发现服务提供了您的应用程序用来创建与 Exchange 服务器的连接的配置信息。 您可以使用 "纯旧 XML" （POX）自动发现服务发送仅包含 XML 负载的邮件，而不使用任何封闭 SOAP 信封，以查找客户端应用程序为连接到 Exchange 所必须具有的设置。
  
> [!NOTE]
> 对于面向以 Exchange Server 2010 开头的 Exchange 版本的客户端，我们建议使用 SOAP 自动发现服务，而不是 POX 自动发现服务。 目标为 Exchange 2007 的客户端必须使用 POX 自动发现服务。 建议使用 .NET Framework 的客户端使用 EWS 托管 API，因为它包含一个可靠且经过充分测试的 POX 自动发现客户端。 有关 EWS 托管 API 的详细信息，请参阅[开始使用 Ews 托管 api 客户端应用程序](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。 
  
本节提供有关在 POX 自动发现请求重定向和响应中返回的用户设置期间在客户端和服务器之间发送的 XML 元素的信息。 XML 元素引用包含元素所表示的内容的摘要，以及使用元素的潜在元素层次结构的说明。 本文档包含在客户端和服务器之间发送的 XML 实例。 POX 自动发现服务没有显式架构。
  
本节中的文章提供了用于通过使用 POX 自动发现服务检索自动发现配置信息的邮件的示例和说明。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [Exchange 的 POX 自动发现请求](pox-autodiscover-request-for-exchange.md)
    
- [Exchange 的 POX 自动发现响应](pox-autodiscover-response-for-exchange.md)
    
- [Exchange 的 POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)   
- [Exchange 的 SOAP 自动发现 web 服务参考](soap-autodiscover-web-service-reference-for-exchange.md)
- [开始使用 Exchange 中的 Web 服务](../exchange-web-services/start-using-web-services-in-exchange.md)
    

