---
title: Exchange SOAP 自动发现 web 服务引用
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: 在 Exchange 中查找参考信息的 SOAP 自动发现服务。
ms.openlocfilehash: 1cb24a8667c71028f3dead78d9fa533dc9547a64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827514"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>Exchange SOAP 自动发现 web 服务引用

在 Exchange 中查找参考信息的 SOAP 自动发现服务。
  
自动发现服务提供了您的应用程序使用创建连接到 Exchange 服务器的配置信息。 您可以使用 SOAP 自动发现服务发送找到设置客户端应用程序与 Exchange 服务器之间的邮件应用程序将用于连接到 Exchange。 与 POX 自动发现服务，不同 SOAP 自动发现服务允许多个用户的设置和哪些设置响应中返回的更精细控制批处理自动发现请求。 
  
> [!NOTE]
> 对于针对开头 Exchange Server 2010 的 Exchange 版本的客户端，我们建议您使用 SOAP 自动发现服务 （而不是 POX 自动发现服务）。 面向 Exchange 2007 的客户端必须使用 POX 自动发现服务。 我们建议使用.NET Framework 的客户端使用 EWS 托管 API，因为它包含可靠且经过充分测试 SOAP 自动发现客户端。 有关 EWS 托管 API 的详细信息，请参阅[Get started with EWS 托管 API 客户端应用程序](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。 
  
本节提供有关 SOAP 自动发现请求重定向和响应中返回的用户设置过程中的客户端和服务器之间发送的 XML 元素的信息。 XML 元素引用包含元素所表示的汇总和潜在的元素层次结构，其中包含元素的说明。 
  
本节中的文章介绍在客户端和服务器之间发送的 XML 实例。 可以承载 SOAP 自动发现服务的服务器的虚拟目录中找到描述这些元素的架构。
  
WSDL 操作本节中的主题提供了执行哪些操作的概述和操作请求和响应示例。 您可以使用提供以确定要使用的功能是否在您运行的产品版本中可用的版本信息。 操作主题中的示例还可以帮助您了解将发送到 / 发送服务器 SOAP 消息中包含的 XML 的结构。
  
本节还提供了示例和用于使用 SOAP 自动发现服务中检索自动发现配置信息的邮件的说明。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)
    
- [GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)
    
- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
    
- [GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [SOAP Exchange 2013 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅


- [Exchange 的自动发现 web 服务引用](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
- [使用 Autodiscover 以查找连接点](http://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [通过使用自动发现 Exchange 中获取用户设置](http://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [从 Exchange 服务器获取域设置](http://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

