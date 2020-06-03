---
title: Exchange 中 EWS 的配置选项
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: 查找有关您的 EWS 客户端可以访问的配置设置的信息，以及可影响您的 EWS 客户端的可配置 Exchange 设置。
ms.openlocfilehash: 55f927b7b301bdfaa298bcd254b18a00cf1692d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456155"
---
# <a name="configuration-options-for-ews-in-exchange"></a>Exchange 中 EWS 的配置选项

查找有关您的 EWS 客户端可以访问的配置设置的信息，以及可影响您的 EWS 客户端的可配置 Exchange 设置。 
  
许多配置设置可能会影响您的 EWS 客户端应用程序可以执行的操作。 这些配置设置为： 
  
- 只读的或可读写的客户端。
    
- 在承载 EWS 服务的 Exchange 服务器上访问。
    
客户端可以访问 Exchange Online 上的设置、作为 Office 365 的一部分的 Exchange Online 和内部部署 Exchange 服务器。 Exchange 管理员可以使用所有内部部署 Exchange 服务器设置;但是，并不是所有这些设置都可用于 Exchange Online 租户管理员。 本文介绍了客户端、Exchange Server 管理员和 Exchange Online 租户管理员可以访问的配置设置。
  
## <a name="configuration-settings-that-clients-can-access"></a>客户端可以访问的配置设置

您的客户端应用程序可以从 Exchange 服务器获取和设置许多配置选项。 自动发现服务提供所有 EWS 应用程序所需的配置设置。 其他配置设置用于特定应用场景。 
  
**表1。为 EWS 客户端提供配置选项的 Web 服务功能**

|**功能**|**说明**|
|:-----|:-----|
|自动发现服务  <br/> |[自动发现服务](autodiscover-for-exchange.md)为客户端应用程序提供了配置信息，以便客户端可以自动配置自己以与 EWS 进行通信。  <br/> |
|邮箱中存储的自定义配置信息  <br/> |您可以使用多个选项之一将[自定义配置信息存储](persistent-application-settings-in-ews-in-exchange.md)在邮箱中：用户配置对象、自定义项或扩展属性。  <br/> |
|委派管理  <br/> | EWS 提供用于管理对邮箱的代理访问的 CRUD 操作。 委派是已被授予访问其他用户的邮箱权限的用户。<br/><br/>  您可以使用[委派管理操作](https://msdn.microsoft.com/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management)来启用使用 ews 的委派管理，或者，如果您使用的是 EWS 托管 API，则可以使用以下方法：<br/><br/>- [ExchangeService。 AddDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService。 GetDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService。 UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService。 RemoveDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|电子数据展示搜索配置  <br/> |电子数据展示客户端应用程序可以获取包括电子数据展示搜索查询、可搜索邮箱列表和就地邮箱保留标识符的[搜索配置信息](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx)。  <br/> |
|文件夹权限  <br/> |文件夹权限限制用户可在公用文件夹中执行的操作，如果是代理访问，代理可以在其他用户的文件夹中执行的操作。 可以使用[folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法或[GetFolder 操作](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)来访问每个文件夹的权限集，包括公用文件夹、共享私人文件夹或用户具有代理访问权限的文件夹。  <br/> |
|邮件提示、统一消息或保护规则  <br/> |[GetServiceConfiguration 操作](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)提供有关邮件提示、统一消息和保护规则的只读[服务配置信息](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)。  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>管理员可以在 Exchange 服务器上访问的配置设置

大多数客户端应用场景不需要更改服务器配置设置;但是，某些方案确实如此。 例如，若要使中间层应用程序能够充当用户，您需要在服务器上设置 Exchange 模拟。 请注意，某些设置只能在本地 Exchange 服务器上进行访问。 如果您针对的是 Exchange Online，则客户端应用程序可能需要使用默认设置。
  
**表2。影响 EWS 客户端的 Exchange server 配置选项**

|**功能**|**可从 Exchange Online 访问？**|**有关详细信息，请参阅 .。。**|
|:-----|:-----|:-----|
|虚拟目录设置（包括身份验证）  <br/> |否  <br/> |[Set-webservicesvirtualdirectory](https://technet.microsoft.com/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-webservicesvirtualdirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|自动发现  <br/> |否  <br/> |[New-autodiscovervirtualdirectory](https://technet.microsoft.com/library/aa996819%28v=exchg.150%29.aspx) <br/> [New-autodiscovervirtualdirectory](https://technet.microsoft.com/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|合规性  <br/> |是  <br/> |[存档](https://technet.microsoft.com/library/dd979800%28v=exchg.150%29.aspx) <br/> [电子数据展示](https://technet.microsoft.com/library/dd298021%28v=exchg.150%29.aspx) <br/> [保留挂起](https://technet.microsoft.com/library/dd335168%28v=exchg.150%29.aspx) <br/> [数据丢失防护](https://technet.microsoft.com/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|委派管理  <br/> |是  <br/> |[Manage Permissions for Recipients](https://technet.microsoft.com/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Exchange 模拟  <br/> |是  <br/> |[配置 Exchange 模拟](https://msdn.microsoft.com/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|邮件提示、统一消息或保护规则  <br/> |是  <br/> |[邮件提示](https://technet.microsoft.com/library/jj649091%28v=exchg.150%29.aspx) <br/> [统一消息 Cmdlet](https://technet.microsoft.com/library/aa997665%28v=exchg.150%29.aspx) <br/> [Outlook 保护规则](https://technet.microsoft.com/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|限制  <br/> |否  <br/> |[限制设置](ews-throttling-in-exchange.md) <br/> |
|用户代理筛选  <br/> |是  <br/> |[用户代理筛选](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>另请参阅

- [使用 Exchange 中的 EWS 获取服务配置信息](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)   
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

