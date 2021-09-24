---
title: 部署中 EWS 的配置Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: 查找有关您的 EWS 客户端可以访问的配置设置以及可Exchange EWS 客户端的可配置配置设置的信息。
ms.openlocfilehash: ed7667086b36897fd07031526e5a4657a120d505
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522283"
---
# <a name="configuration-options-for-ews-in-exchange"></a>部署中 EWS 的配置Exchange

查找有关您的 EWS 客户端可以访问的配置设置以及可Exchange EWS 客户端的可配置配置设置的信息。 
  
许多配置设置会影响 EWS 客户端应用程序可以执行哪些操作。 这些配置设置包括： 
  
- 客户端中的只读或可读写。
    
- 在承载 EWS Exchange服务器上访问。
    
客户端可以访问本地Exchange Online、Exchange Online作为Office 365的一部分以及本地Exchange设置。 所有本地Exchange服务器设置都可供管理员Exchange使用;但是，并非所有这些设置都可供租户Exchange Online使用。 本文介绍租户管理员Exchange Server管理员Exchange Online哪些配置设置。
  
## <a name="configuration-settings-that-clients-can-access"></a>客户端可以访问的配置设置

客户端应用程序可以从客户端服务器获取和设置Exchange选项。 所有 EWS 应用程序所需的配置设置都由自动发现服务提供。 其他配置设置用于特定应用程序方案。 
  
**表 1.为 EWS 客户端提供配置选项的 Web 服务功能**

|**功能**|**说明**|
|:-----|:-----|
|自动发现服务  <br/> |自动 [发现服务](autodiscover-for-exchange.md) 向客户端应用程序提供配置信息，以便客户端可以自动配置自身以与 EWS 通信。  <br/> |
|邮箱中存储的自定义配置信息  <br/> |可以使用以下几种选项之一在邮箱[](persistent-application-settings-in-ews-in-exchange.md)中存储自定义配置信息：用户配置对象、自定义项目或扩展属性。  <br/> |
|委派管理  <br/> | EWS 提供了用于管理对邮箱的委派访问的 CRUD 操作。 代理是已授予访问其他用户邮箱的权限的用户。<br/><br/>  可以使用委派管理 [操作](https://msdn.microsoft.com/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management) 通过 EWS 启用委派管理，或者，如果使用的是 EWS 托管 API，可以使用下列方法：<br/><br/>- [ExchangeService.AddDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.GetDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.RemoveDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|电子数据展示搜索配置  <br/> |电子数据展示客户端应用程序 [可以获取搜索](https://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx) 配置信息，其中包括电子数据展示搜索查询、可搜索邮箱列表和就地邮箱保留的标识符。  <br/> |
|文件夹权限  <br/> |文件夹权限限制用户可以在公用文件夹中执行哪些操作，在委派访问权限的情况下，代理可以在其他用户的文件夹中执行哪些操作。 可以使用 [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) 方法或 [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) 操作访问每个文件夹的权限集，包括公用文件夹、共享专用文件夹或用户具有委派访问权限的文件夹。  <br/> |
|邮件提示、统一消息或保护规则  <br/> |[GetServiceConfiguration 操作](https://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)为[邮件提示、](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)统一消息和保护规则提供只读服务配置信息。  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>管理员可以在管理服务器上访问的配置Exchange设置

大多数客户端应用程序方案不需要更改服务器配置设置;但是，有一些方案。 例如，若要使中间层应用程序充当用户，您需要在服务器上Exchange模拟"。 请注意，某些设置只能在内部部署服务器上Exchange访问。 如果您面向 Exchange Online，则客户端应用程序可能需要使用默认设置。
  
**表 2.Exchange影响 EWS 客户端的服务器配置选项**

|**功能**|**可从 Exchange Online？**|**有关详细信息，请参阅...**|
|:-----|:-----|:-----|
|虚拟目录设置 (包括身份验证)   <br/> |否  <br/> |[Get-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-WebServicesVirtualDirectory](https://technet.microsoft.com/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|自动发现  <br/> |否  <br/> |[Get-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa996819%28v=exchg.150%29.aspx) <br/> [Set-AutodiscoverVirtualDirectory](https://technet.microsoft.com/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|合规性  <br/> |是  <br/> |[存档](https://technet.microsoft.com/library/dd979800%28v=exchg.150%29.aspx) <br/> [电子数据展示](https://technet.microsoft.com/library/dd298021%28v=exchg.150%29.aspx) <br/> [保留挂起](https://technet.microsoft.com/library/dd335168%28v=exchg.150%29.aspx) <br/> [数据丢失防护](https://technet.microsoft.com/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|委派管理  <br/> |是  <br/> |[Manage Permissions for Recipients](https://technet.microsoft.com/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Exchange模拟  <br/> |是  <br/> |[配置Exchange模拟](https://msdn.microsoft.com/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|邮件提示、统一消息或保护规则  <br/> |是  <br/> |[邮件提示](https://technet.microsoft.com/library/jj649091%28v=exchg.150%29.aspx) <br/> [统一消息 Cmdlet](https://technet.microsoft.com/library/aa997665%28v=exchg.150%29.aspx) <br/> [Outlook 保护规则](https://technet.microsoft.com/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|限制  <br/> |否  <br/> |[限制设置](ews-throttling-in-exchange.md) <br/> |
|用户代理筛选  <br/> |是  <br/> |[用户代理筛选](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>另请参阅

- [使用 EWS 获取服务配置Exchange](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)   
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

