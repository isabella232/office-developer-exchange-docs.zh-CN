---
title: Exchange Web Services (EWS) 托管 API 参考
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
api_type:
- schema
ms.assetid: c6ca36f4-a67c-4e3c-aae7-9ead7b704e15
description: 了解有关在 EWS 托管 API 中包含的命名空间。
localization_priority: Priority
ms.openlocfilehash: aa5dd71bf1e9962611a8ea8471aca0c60aa232e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466750"
---
# <a name="ews-managed-api-reference"></a>EWS 托管 API 参考

**适用于**：EWS 托管 API | Exchange Online | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 | Office 365

Exchange Web Services (EWS) 托管 API 包括两个 API：Microsoft.Exchange.WebServices.dll 和 Microsoft.Exchange.WebServices.Auth.dll。

## <a name="ews-managed-api-namespaces"></a>EWS 托管 API 命名空间

|命名空间 |说明 |
|:---------|:-----------|
|[Microsoft.Exchange.WebServices.Auth.Validation](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.auth.validation?view=exchange-ews-api) |包含用于验证从 Exchange 服务器发送的用户标识令牌的类型和方法。 Microsoft.Exchange.WebServices.Auth.Validation 命名空间适用于面向 Exchange Online 的客户端和 Exchange Server 2013 以后的 Exchange 版本。 此命名空间包含在 Microsoft.Exchange.WebServices.Auth.dll API 中。|
|[Microsoft.Exchange.WebServices.Autodiscover](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.autodiscover?view=exchange-ews-api)|包含用于与由 Exchange Server 托管的自动发现服务进行通信的类型。 此命名空间也用于查找 Active Directory 域服务 (AD DS) 中的服务连接点对象。 自动发现服务向 EWS 客户端提供配置信息。 这使客户端能够面向适当的服务 URL。<br/><br/>命名空间功能可用于面向在 Microsoft Exchange Server 2007 中引入的 POX 自动发现服务，服务连接点对象将查找客户端是否联接了域，或 Exchange Server 2010 中引入的 SOAP 自动发现终结点。 此命名空间中的主要类型是 [AutodiscoverService 类](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.autodiscover.autodiscoverservice?view=exchange-ews-api)。 此命名空间包含在 Microsoft.Exchange.WebServices.dll API 中。|
|[Microsoft.Exchange.WebServices.Data](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data?view=exchange-ews-api)| 包含通过 EWS 与 Exchange Server 进行通信的类型。 此命名空间提供核心 EWS 托管 API 功能。 此命名空间中的主要类型是 [ExchangeService 类](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice?view=exchange-ews-api)。|

## <a name="see-also"></a>另请参阅

- [Exchange Web 服务参考](web-services-reference-for-exchange.md)
- [探索 Exchange 中 EWS 托管 API、EWS 和 Web 服务](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [EWS 中的新增功能和 Exchange 中的 其他 Web 服务](../exchange-web-services/whats-new-in-ews-and-other-web-services-in-exchange.md)
- [开始使用 Exchange 中的 Web 服务](../exchange-web-services/start-using-web-services-in-exchange.md)
- [开发 Exchange Web 服务客户端](../exchange-web-services/develop-web-service-clients-for-exchange.md)

