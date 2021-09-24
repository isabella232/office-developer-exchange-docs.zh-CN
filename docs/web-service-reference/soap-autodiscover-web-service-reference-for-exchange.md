---
title: SOAP 自动发现 Web 服务参考Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: 查找 SOAP 自动发现服务在 Exchange 中的参考信息。
ms.openlocfilehash: 488862f5797abfd71d33c916fa96970ab300a2c0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521352"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>SOAP 自动发现 Web 服务参考Exchange

查找 SOAP 自动发现服务在 Exchange 中的参考信息。
  
自动发现服务提供应用程序用于创建与服务器连接的配置Exchange信息。 您可以使用 SOAP 自动发现服务在客户端应用程序与 Exchange 服务器之间发送消息，以找到应用程序用于连接到 Exchange。 与 POX 自动发现服务不同，SOAP 自动发现服务允许针对许多用户的设置的批量自动发现请求，并更精细地控制响应中返回的设置。 
  
> [!NOTE]
> 对于从 Exchange Server Exchange 2010 开始面向 Exchange 版本的客户端，建议使用 SOAP 自动发现服务 (而不是 POX 自动发现) 。 面向 2007 Exchange的客户端必须使用 POX 自动发现服务。 我们建议使用 EWS .NET Framework的客户端使用 EWS 托管 API，因为它包含一个可靠且经过良好测试的 SOAP 自动发现客户端。 有关 EWS 托管 API 详细信息，请参阅 [EWS 托管 API 客户端应用程序入门](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)。 
  
本节提供有关在 SOAP 自动发现请求重定向期间在客户端和服务器之间发送的 XML 元素以及响应中返回的用户设置的信息。 XML 元素引用包含元素表示的内容的摘要以及包含元素的潜在元素层次结构的说明。 
  
本节中的文章介绍在客户端和服务器之间发送的 XML 实例。 可以在承载 SOAP 自动发现服务的服务器的虚拟目录中找到描述这些元素的架构。
  
本节中的 WSDL 操作主题概述了操作功能、操作请求和响应示例。 可以使用所提供的版本信息来确定要使用的功能在所运行的产品版本中是否可用。 操作主题中的示例还可帮助您了解发送到服务器和从服务器发送的 SOAP 消息中包含的 XML 的结构。
  
本节还提供了使用 SOAP 自动发现服务检索自动发现配置信息时所使用的消息的示例和说明。 
  
## <a name="in-this-section"></a>本节内容
<a name="bk_InThisSection"> </a>

- [GetDomainSettings 操作 (SOAP)](getdomainsettings-operation-soap.md)
    
- [GetFederationInformation 操作 (SOAP)](getfederationinformation-operation-soap.md)
    
- [GetUserSettings 操作 (SOAP)](getusersettings-operation-soap.md)
    
- [GetOrganizationRelationshipSettings 操作 (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [Exchange 2013 的 SOAP 自动发现 XML 元素](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅


- [自动发现 Web 服务引用Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
- [使用自动发现查找连接点](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [使用自动发现从 Exchange 获取用户设置](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [获取来自 Exchange 服务器的域设置](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [开始使用 Exchange 中的 Web 服务](../exchange-web-services/start-using-web-services-in-exchange.md)
    

