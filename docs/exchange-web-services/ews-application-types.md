---
title: EWS 应用程序类型
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: ca4e8b90-d0d8-4d55-aa92-19e21659d4f5
description: 了解您可以使用 Exchange 中的 EWS 创建的最常见的应用程序类型。
localization_priority: Priority
ms.openlocfilehash: 02bbe039adaec1054ab33f642f3bf14a7ba22b90
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455427"
---
# <a name="ews-application-types"></a>EWS 应用程序类型

了解您可以使用 Exchange 中的 EWS 创建的最常见的应用程序类型。
  
[EWS 和 Exchange 体系结构](ews-applications-and-the-exchange-architecture.md)提供了统一的开发模型，可用于以一致的方式创建最常见类型的应用程序，其中包括以下内容： 
  
- [客户端应用程序](#bk_clientapps)—使用 EWS 访问 Exchange 数据的独立应用程序。 Outlook 和 Outlook Web App 是客户端应用程序的示例。 
    
- [门户应用程序](#bk_portalapps)：通过包含从 Exchange 检索的信息（如忙/闲或联系人信息）扩展现有网页的应用程序。 检索 Exchange 数据的 SharePoint web 部件是门户应用程序的一个示例。 
    
- [服务应用程序](#bk_serviceapps)-用于将 Exchange 中的数据集成或同步到现有系统中的后台作业。 例如，将 Exchange 中的联系人信息同步到 CRM 应用程序的应用程序。 
    
其中的每个应用程序模型都可以使用通用基本代码从 Exchange 中检索信息，因此您无需更改用于检索客户端、门户或服务应用程序之间的项目信息的 EWS 代码。 从一个应用程序到下一个应用程序可能会发生变化的是邮箱访问和身份验证机制。 例如，客户端应用程序通常使用直接用户访问和基本或 NTLM 身份验证，而服务应用程序可能会对邮箱访问和 OAuth 身份验证使用模拟。
  
## <a name="client-applications"></a>客户端应用程序
<a name="bk_clientapps"> </a>

EWS 客户端应用程序是任何独立应用程序，它使用 EWS 从 Exchange 存储中检索信息。 EWS 客户端应用程序使用直接客户端访问或代理访问从邮箱存储中检索数据。 以下是使用 EWS 的客户端应用程序的一些示例：
  
- Outlook，在邮件提示、可用性和用户 OOF 状态等功能中
    
- 适用于设备的 OWA
    
- Outlook for Mac 2011
    
- Lync，用于提供可用性信息
    
客户端应用程序通常使用直接访问和基本或 NTLM 身份验证，以便用户只能使用自己的登录凭据访问自己邮箱中的信息。 客户端应用程序还应为已授予访问其他用户的邮箱权限的用户支持代理访问。
  
## <a name="portal-applications"></a>门户应用程序
<a name="bk_portalapps"> </a>

门户应用程序扩展现有网页或门户以将 Exchange 邮箱信息包含为页面的个性化组件。 SharePoint web 部件是最常见的门户应用程序，它通过提供 Exchange 邮箱数据中的视图（如未读邮件、最新邮件和日历事件，以及用户通常查看的 SharePoint 门户页）来为用户提供个性化体验。 EWS 门户应用程序可以使用直接客户端访问、委派访问或模拟从邮箱存储中检索数据。 由于 Exchange 2013 和 SharePoint 2013 都支持用于服务器到服务器身份验证的 OAuth 授权协议，因此 OAuth 提供最严密、最安全的身份验证方法。
  
## <a name="service-applications"></a>服务应用程序
<a name="bk_serviceapps"> </a>

服务应用程序通常是现有应用程序中内置的一种后台作业，该作业可扩展到 Exchange 以在系统与 Exchange 存储之间关联数据。 服务应用程序通常没有用户界面，使用模拟或 OAuth 进行身份验证和访问。 创建服务帐户以模拟用户在 EWS 服务应用程序中很常见，因为您可以授予单个帐户以模拟一组用户并对这些帐户执行邮箱操作。 例如，EWS 服务应用程序可以使用服务帐户和模拟在 CRM 解决方案和 Exchange 通讯组中的市场营销列表之间同步数据。
  
## <a name="see-also"></a>另请参阅


- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)
    
- [EWS 应用程序和 Exchange 体系结构](ews-applications-and-the-exchange-architecture.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

