---
title: Exchange 的 SOAP 自动发现 web 服务参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: 在 Exchange 中查找 SOAP 自动发现服务的引用信息。
ms.openlocfilehash: bfca8e8e260a6262d12542bd6834894a2375453f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468423"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>Exchange 的 SOAP 自动发现 web 服务参考

在 Exchange 中查找 SOAP 自动发现服务的引用信息。
  
自动发现服务提供了您的应用程序用来创建与 Exchange 服务器的连接的配置信息。 您可以使用 SOAP 自动发现服务在客户端应用程序和 Exchange 服务器之间发送邮件，以找到应用程序将用于连接到 Exchange 的设置。 与 POX 自动发现服务不同，SOAP 自动发现服务允许对许多用户的设置进行批量自动发现请求，并更精确地控制响应中返回的设置。 
  
> [!NOTE]
> 对于面向以 Exchange Server 2010 开头的 Exchange 版本的客户端，我们建议使用 SOAP 自动发现服务（而不是 POX 自动发现服务）。 目标为 Exchange 2007 的客户端必须使用 POX 自动发现服务。 建议使用 .NET Framework 的客户端使用 EWS 托管 API，因为它包含一个可靠且经过充分测试的 SOAP 自动发现客户端。 有关 EWS 托管 API 的详细信息，请参阅[开始使用 Ews 托管 api 客户端应用程序](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。 
  
本节提供有关在 SOAP 自动发现请求重定向期间以及在响应中返回的用户设置期间在客户端和服务器之间发送的 XML 元素的信息。 XML 元素引用包含元素所表示的内容的摘要，以及包含元素的潜在元素层次结构的说明。 
  
本节中的文章介绍了如何在客户端和服务器之间发送的 XML 实例。 可以在承载 SOAP 自动发现服务的服务器的虚拟目录中找到描述这些元素的架构。
  
本节中的 WSDL 操作主题概述了操作的功能以及操作请求和响应示例。 您可以使用提供的版本信息来确定您要使用的功能是否在您运行的产品版本中可用。 操作主题中的示例还有助于了解在发送到服务器和从服务器发送的 SOAP 消息中包含的 XML 的结构。
  
此部分还提供了用于通过使用 SOAP 自动发现服务检索自动发现配置信息的消息的示例和说明。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)
    
- [GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)
    
- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
    
- [GetOrganizationRelationshipSettings 操作（SOAP）](getorganizationrelationshipsettings-operation-soap.md)
    
- [Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅


- [Exchange 的自动发现 web 服务参考](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
- [使用自动发现查找连接点](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [使用自动发现从 Exchange 获取用户设置](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [获取来自 Exchange 服务器的域设置](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

