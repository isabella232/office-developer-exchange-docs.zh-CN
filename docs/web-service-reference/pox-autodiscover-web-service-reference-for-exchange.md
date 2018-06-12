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
# <a name="pox-autodiscover-web-service-reference-for-exchange"></a>Exchange POX 自动发现 web 服务引用

在 Exchange 查找 POX 自动发现服务的参考信息。
  
自动发现服务提供了您的应用程序使用创建连接到 Exchange 服务器的配置信息。 您可以使用"普通旧 XML"(POX) 自动发现服务发送邮件仅组成的 XML 有效负荷，没有任何封闭的 SOAP 信封，为定位客户端应用程序必须具有才能连接到 Exchange 的设置。
  
> [!NOTE]
> 目标版本的 Exchange 开头 Exchange Server 2010 中的客户端，我们建议您而不是 POX 自动发现服务使用 SOAP 自动发现服务。 面向 Exchange 2007 的客户端必须使用 POX 自动发现服务。 我们建议使用.NET Framework 的客户端使用 EWS 托管 API，因为它包含可靠且经过充分测试 POX 自动发现客户端。 有关 EWS 托管 API 的详细信息，请参阅[Get started with EWS 托管 API 客户端应用程序](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。 
  
本节提供有关 POX 自动发现请求重定向和响应中返回的用户设置过程中的客户端和服务器之间发送的 XML 元素的信息。 XML 元素引用包含元素所表示的汇总和使用元素的潜在元素层次结构的说明。 本文档介绍了客户端和服务器之间发送的 XML 实例。 POX 自动发现服务没有显式架构。
  
本节中的文章提供了示例以及用于使用 POX 自动发现服务中检索自动发现配置信息的邮件的说明。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [Exchange POX 自动发现请求](pox-autodiscover-request-for-exchange.md)
    
- [Exchange POX 自动发现响应](pox-autodiscover-response-for-exchange.md)
    
- [Exchange POX 自动发现 XML 元素](pox-autodiscover-xml-elements-for-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 的自动发现 web 服务引用](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)   
- [Exchange SOAP 自动发现 web 服务引用](soap-autodiscover-web-service-reference-for-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

