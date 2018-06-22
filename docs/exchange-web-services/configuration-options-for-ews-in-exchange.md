---
title: Exchange 中的 EWS 的配置选项
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6562639-9366-4a13-9fdb-2fa737833329
description: 查找有关可以访问 EWS 客户端的配置设置会影响您 EWS 的客户端的可配置 Exchange 设置的信息。
ms.openlocfilehash: d6c2866abf3dc16c77d84355afb9d86b0a9934c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752708"
---
# <a name="configuration-options-for-ews-in-exchange"></a>Exchange 中的 EWS 的配置选项

查找有关可以访问 EWS 客户端的配置设置会影响您 EWS 的客户端的可配置 Exchange 设置的信息。 
  
很多配置设置会影响 EWS 客户端应用程序可以执行的操作。 这些配置设置已： 
  
- 只读或可读-写从客户端。
    
- 访问 EWS 服务承载的 Exchange 服务器上。
    
客户端可以访问 Exchange Online、 Exchange Online 作为 Office 365 的一部分和本地 Exchange 服务器上的设置。 所有内部部署 Exchange 服务器设置都可向 Exchange 管理员;但是，不是所有这些设置可供 Exchange Online 租户管理员。 本文介绍哪些客户端配置设置、 Exchange 服务器管理员和 Exchange Online 租户管理员可以访问。
  
## <a name="configuration-settings-that-clients-can-access"></a>客户端可以访问的配置设置

客户端应用程序可以获取和设置数从 Exchange 服务器的配置选项。 自动发现服务提供了所有的 EWS 应用程序需要的配置设置。 其他配置设置用于特定应用程序方案。 
  
**表 1。提供用于 EWS 客户端的配置选项的 web 服务功能**

|**功能**|**说明**|
|:-----|:-----|
|自动发现服务  <br/> |以便您的客户端可以自动配置本身与 EWS 进行通信，[自动发现服务](autodiscover-for-exchange.md)将为您的客户端应用程序提供配置信息。  <br/> |
|邮箱中存储的自定义配置信息  <br/> |您可以使用您的邮箱中[存储自定义配置信息](persistent-application-settings-in-ews-in-exchange.md)的多个选项之一： 用户配置对象、 自定义项或扩展的属性。  <br/> |
|管理工作委派给  <br/> | EWS 提供用于管理邮箱的代理访问的 CRUD 操作。 代理人是已被授予另一个用户的邮箱的访问权的用户。<br/><br/>  您可以使用[委托管理操作](http://msdn.microsoft.com/en-us/library/bb409286%28v=exchg.150%29.aspx#bk_delegate_management)使用 EWS，启用委托管理，或者，如果您正在使用 EWS 托管 API，您可以使用以下方法：<br/><br/>- [ExchangeService.AddDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.adddelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.GetDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getdelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.UpdateDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) <br/>- [ExchangeService.RemoveDelegates](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.removedelegates%28v=exchg.80%29.aspx) <br/> |
|电子数据展示搜索配置  <br/> |电子数据展示客户端应用程序可以获取[搜索配置信息](http://msdn.microsoft.com/library/8a54a6dc-110c-4972-a8bc-5ddb43c4b857%28Office.15%29.aspx)，包括电子数据展示搜索查询，可搜索邮箱的列表和保留就地邮箱的标识符。  <br/> |
|文件夹权限  <br/> |文件夹权限限制在公用文件夹中，用户可以执行哪些操作，对于代理访问，代理人可以做什么另一个用户的文件夹中。 您可以使用[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法或[GetFolder 操作](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)访问每个文件夹，包括公用文件夹、 共享的专用文件夹或向其用户具有委派访问的文件夹的权限集。  <br/> |
|邮件提示、 统一消息，或保护规则  <br/> |[GetServiceConfiguration 操作](http://msdn.microsoft.com/library/070cbfe5-325a-4955-8e4a-8230ea0459a7%28Office.15%29.aspx)提供的邮件提示、 统一消息和保护规则的只读的[服务配置信息](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)。  <br/> |
   
## <a name="configuration-settings-that-administrators-can-access-on-the-exchange-server"></a>管理员可以访问 Exchange 服务器的配置设置

大多数客户端应用程序方案不需要更改服务器配置设置;但是，某些情况下执行操作。 例如，若要启用要用作用户的中间层应用程序，您需要在服务器上设置 Exchange 模拟。 请注意，某些设置只能访问内部部署 Exchange 服务器上。 如果您面向的 Exchange Online，您的客户端应用程序可能需要使用默认设置。
  
**表 2。影响 EWS 客户端的 Exchange 服务器配置选项**

|**功能**|**从 Exchange Online 可访问？**|**有关详细信息，请参阅...**|
|:-----|:-----|:-----|
|虚拟目录设置 （包括身份验证）  <br/> |否  <br/> |[Get-webservicesvirtualdirectory](http://technet.microsoft.com/en-us/library/aa998810%28v=exchg.150%29.aspx) <br/> [Set-webservicesvirtualdirectory](http://technet.microsoft.com/en-us/library/aa997233%28v=exchg.150%29.aspx) <br/> |
|自动发现  <br/> |否  <br/> |[Get-autodiscovervirtualdirectory](http://technet.microsoft.com/en-us/library/aa996819%28v=exchg.150%29.aspx) <br/> [设置 AutodiscoverVirtualDirectory](http://technet.microsoft.com/en-us/library/aa998601%28v=exchg.150%29.aspx) <br/> |
|合规性  <br/> |是  <br/> |[存档](http://technet.microsoft.com/en-us/library/dd979800%28v=exchg.150%29.aspx) <br/> [电子数据展示](http://technet.microsoft.com/en-us/library/dd298021%28v=exchg.150%29.aspx) <br/> [保留挂起](http://technet.microsoft.com/en-us/library/dd335168%28v=exchg.150%29.aspx) <br/> [数据丢失防护](http://technet.microsoft.com/en-us/library/jj150527%28v=exchg.150%29.aspx) <br/> |
|管理工作委派给  <br/> |是  <br/> |[管理收件人的权限](http://technet.microsoft.com/en-us/library/jj919240%28v=exchg.150%29.aspx) <br/> |
|Exchange 模拟  <br/> |是  <br/> |[配置 Exchange 模拟](http://msdn.microsoft.com/en-us/library/bb204095%28EXCHG.140%29.aspx) <br/> |
|邮件提示、 统一消息，或保护规则  <br/> |是  <br/> |[邮件提示](http://technet.microsoft.com/en-us/library/jj649091%28v=exchg.150%29.aspx) <br/> [统一消息 Cmdlet](http://technet.microsoft.com/en-us/library/aa997665%28v=exchg.150%29.aspx) <br/> [Outlook 保护规则](http://technet.microsoft.com/en-us/library/dd638178%28v=exchg.150%29.aspx) <br/> |
|限制  <br/> |否  <br/> |[限制设置](ews-throttling-in-exchange.md) <br/> |
|筛选的用户代理  <br/> |是  <br/> |[筛选的用户代理](how-to-control-access-to-ews-in-exchange.md) <br/> |
   
## <a name="see-also"></a>另请参阅

- [要在 Exchange 使用 EWS 获取服务配置信息](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [Start using web services in Exchange](start-using-web-services-in-exchange.md)   
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

