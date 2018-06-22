---
title: EWS 应用程序类型
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ca4e8b90-d0d8-4d55-aa92-19e21659d4f5
description: 了解有关您可以使用 EWS 在 Exchange 中创建的应用程序的最常见类型。
ms.openlocfilehash: 1ce739f453ba1bc6f1b5d38edae3776daa562ffb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752711"
---
# <a name="ews-application-types"></a>EWS 应用程序类型

了解有关您可以使用 EWS 在 Exchange 中创建的应用程序的最常见类型。
  
[EWS 和 Exchange 体系结构](ews-applications-and-the-exchange-architecture.md)提供统一的开发模型，可用来创建最常见类型的应用程序中以一致的方式，其中包括： 
  
- [客户端应用程序](#bk_clientapps)— 使用 EWS 访问 Exchange 数据的独立应用程序。 Outlook 和 Outlook Web App 是客户端应用程序的示例。 
    
- [门户应用程序](#bk_portalapps)— 包括的信息来扩展现有 web 页的应用程序检索 exchange，例如忙/闲或联系人信息。 检索 Exchange 数据的 SharePoint web 部件是门户应用程序的示例。 
    
- [服务应用程序](#bk_serviceapps)— 背景用于集成或同步到现有系统从交换数据的作业。 例如，应用程序同步 Exchange 到 CRM 应用程序的联系人信息。 
    
这些应用程序模型中的每个可用基本的常见代码来检索信息交换-从，因此不需要更改用于检索客户端、 门户或服务应用程序之间的项信息的 EWS 代码。 从到下一个应用程序可能更改的内容是邮箱访问和身份验证机制。 例如，客户端应用程序通常使用用户直接访问和基本或 NTLM 身份验证，而服务应用程序可能使用模拟的邮箱访问和 OAuth 身份验证。
  
## <a name="client-applications"></a>客户端应用程序
<a name="bk_clientapps"> </a>

EWS 客户端应用程序是任何独立应用程序使用 EWS 检索从 Exchange 存储的信息。 EWS 客户端应用程序使用直接客户端访问或委派从邮箱存储检索数据的访问权限。 以下是使用 EWS 的客户端应用程序的一些示例：
  
- Outlook 的邮件提示、 可用性和用户 OOF 状态等功能
    
- 适用于设备的 OWA
    
- Outlook for Mac 2011
    
- Lync 的可用性信息
    
客户端应用程序通常使用直接访问和基本或 NTLM 身份验证，以便用户仅限于访问自己的登录凭据自己邮箱中的信息。 此外应支持客户端应用程序代理的有权访问其他用户的邮箱的权限的用户的访问。
  
## <a name="portal-applications"></a>门户应用程序
<a name="bk_portalapps"> </a>

门户应用程序扩展现有 web 页或门户以包括页上的个性化组件的 Exchange 邮箱信息。 SharePoint web 部件的最常见的门户应用程序和向用户提供个性化体验通过提供到 Exchange 邮箱数据，例如未读的邮件、 最新邮件和日历事件，用于在其常查看的视图SharePoint 门户页面。 EWS 门户应用程序可以使用直接客户端访问、 代理访问或模拟从邮箱存储检索数据。 Exchange 2013 和 SharePoint 2013 支持的服务器到服务器身份验证的 OAuth 授权协议，因为 OAuth 提供的最无缝且安全的身份验证方法。
  
## <a name="service-applications"></a>服务应用程序
<a name="bk_serviceapps"> </a>

服务应用程序通常是内置的现有应用程序扩展到要关联之间系统和 Exchange 存储的数据交换后台作业。 服务应用程序通常不具有用户界面和使用模拟或 OAuth 身份验证和访问。 创建模拟用户的服务帐户是 EWS 服务应用程序中常见，因为这样可以授予一个单个帐户的权限模拟用户组，并执行这些帐户的邮箱操作。 例如，EWS 服务应用程序可同步之间使用的服务帐户和模拟营销中 CRM 解决方案和 Exchange 通讯组列表的数据。
  
## <a name="see-also"></a>另请参阅


- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
    
- [EWS 应用程序和 Exchange 体系结构](ews-applications-and-the-exchange-architecture.md)
    
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
    

