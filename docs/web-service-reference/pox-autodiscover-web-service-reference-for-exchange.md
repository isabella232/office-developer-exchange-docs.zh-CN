---
title: POX 自动发现 Web 服务参考Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 877152f0-f4b1-4f63-b2ce-924f4bdf2d20
description: 查找 POX 自动发现服务的参考信息Exchange。
ms.openlocfilehash: b28ea64a82960a84dee06c5055ee915614f4fde7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516417"
---
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>POX 自动发现 Web 服务参考Exchange

查找 POX 自动发现服务的参考信息Exchange。
  
自动发现服务提供应用程序用于创建与服务器连接的配置Exchange信息。 您可以使用"纯旧 XML" (POX) 自动发现服务发送仅包含 XML 有效负载（没有任何封闭 SOAP 信封）的邮件，以便找到客户端应用程序连接到 Exchange 时必须具有的设置。
  
> [!NOTE]
> 对于从 Exchange 2010 Exchange Server版本的客户端，建议使用 SOAP 自动发现服务，而不是 POX 自动发现服务。 面向 2007 Exchange的客户端必须使用 POX 自动发现服务。 我们建议使用 EWS .NET Framework的客户端使用 EWS 托管 API，因为它包含一个可靠且经过良好测试的 POX 自动发现客户端。 有关 EWS 托管 API 详细信息，请参阅 [EWS 托管 API 客户端应用程序入门](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。 
  
本节提供有关在 POX 自动发现请求重定向期间在客户端和服务器之间发送的 XML 元素以及响应中返回的用户设置的信息。 XML 元素引用包含元素表示的内容的摘要以及使用该元素的潜在元素层次结构的说明。 本文档介绍在客户端和服务器之间发送的 XML 实例。 POX 自动发现服务没有显式架构。
  
本节中的文章提供了使用 POX 自动发现服务检索自动发现配置信息时所使用的邮件的示例和说明。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [POX 自动发现请求Exchange](pox-autodiscover-request-for-exchange.md)
    
- [POX 自动发现响应Exchange](pox-autodiscover-response-for-exchange.md)
    
- [用于存储的 POX 自动发现 XML Exchange](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [自动发现 Web 服务引用Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)   
- [SOAP 自动发现 Web 服务参考Exchange](soap-autodiscover-web-service-reference-for-exchange.md)
- [开始使用 Exchange 中的 Web 服务](../exchange-web-services/start-using-web-services-in-exchange.md)
    

