---
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.assetid: 6c969133-6036-448b-af39-a3caf9917e98
description: 查找 Exchange 中的 web 服务的参考信息。
localization_priority: Priority
ms.openlocfilehash: 8bdb3d6c4244bf8e0f092f5a9ffa3de5e8f1c3c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467345"
---
# <a name="web-services-reference-for-exchange"></a>Exchange 的 Web 服务参考

查找 Exchange 中的 web 服务的参考信息。
  
此部分包括面向 Exchange Online 中的 Api 的参考信息、Exchange Online 作为 Office 365 的一部分以及从 Exchange Server 2007 开始的 Exchange 版本。 本部分包含以下内容：
  
- [Exchange 的 EWS 参考](ews-reference-for-exchange.md)—包含 Exchange Web 服务（EWS） API 的 API 参考文档。 这是用于创建连接到 Exchange 以获取邮箱信息访问权限的客户端和服务的主要 API。 此内容包含有关 EWS 中可用的操作的信息，以及 XML 参考文档，提供了有关发送到 Exchange 和从 Exchange 接收的实例 XML 的信息。 
    
- [Ews 托管 api 参考](ews-managed-api-reference-for-exchange.md)—包含 EWS 托管 API 的 API 参考文档。 EWS 托管 API 是一个简单且功能齐全的界面，用于开发和扩展使用 EWS 的应用程序。 
    
- [自动发现的 exchange web 服务参考](autodiscover-web-service-reference-for-exchange.md)—包含针对 exchange 提供的自动发现服务的 XML API 参考。 自动发现 Api 为客户端应用程序提供了设置信息，使其能够自动发现 Exchange 服务终结点。 
    
- [Exchange 的统一消息 web 服务参考](unified-messaging-web-service-reference-for-exchange.md)—包含统一消息（UM） web 服务的 XML API 参考。 UM web 服务提供客户端应用程序对 Exchange 中的 UM 功能的访问权限。 请注意，EWS 还提供了 UM 功能。 
    
- [EWS 生成的 Exchange 对象模型](ews-generated-object-models-reference-for-exchange.md)—包含 ExchangeWebServices 命名空间中自动生成的代理类的 API 引用。 
    
    > [!NOTE]
    > 对于基于 .net framework 3.5 的 .NET Framework 版本的客户端，建议您使用 EWS 托管 API 来访问 EWS。 有关详细信息，请参阅[开始使用 EWS 托管 API 客户端应用程序](../exchange-web-services/get-started-with-ews-managed-api-client-applications.md)。 
  
有关要使用的 Api 集的信息，请参阅[Exchange 的 EWS 客户端设计概述](../exchange-web-services/ews-client-design-overview-for-exchange.md)。
  
Exchange XML 引用基于在客户端和服务器之间发送的 XML 实例。 在 EWS 和 SOAP 自动发现服务的 WSDL 和 XSD 文件中对 XML 进行了介绍。 UM web 服务和 POX 自动发现服务没有已发布的 WSDL 和 schema 文件来描述其结构。 不具有架构文件的服务的 XML 引用基于在客户端和服务之间交换时可以观察和捕获的 XML 实例。
  
## <a name="see-also"></a>另请参阅

- [在 Exchange 中浏览 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Start using web services in Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Exchange 自动发现](../exchange-web-services/autodiscover-for-exchange.md)
    

