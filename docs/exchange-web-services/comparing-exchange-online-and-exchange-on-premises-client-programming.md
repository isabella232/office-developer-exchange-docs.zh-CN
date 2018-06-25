---
title: 比较 Exchange Online 和 Exchange 内部部署客户端编程 （英文）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: 了解如何创建 EWS 托管 API 或针对 Exchange Online 和 Exchange 内部部署的工作方式的 EWS 客户端应用程序的设计注意事项。
ms.openlocfilehash: 87c6ee476e06b50c339901bf61020b0fc98f8486
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752731"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>比较 Exchange Online 和 Exchange 内部部署客户端编程 （英文）

了解如何创建 EWS 托管 API 或针对 Exchange Online 和 Exchange 内部部署的工作方式的 EWS 客户端应用程序的设计注意事项。
  
在多数情况下，客户端和 web 服务 Exchange 这些目标中的将无论是否目标是 Exchange Online，Exchange Online 作为 Office 365 的一部分的相同方式或 Exchange 本地服务器。 有，但是，一些例外，您需要确保您的应用程序可以处理它们。 使用本文中的信息可帮助您设计您的客户端来设定这两个 Exchange Online 和 Exchange 内部部署。

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>自动发现的客户端编程注意事项

[自动发现](autodiscover-for-exchange.md)提供 Exchange 客户端的配置的信息。 客户端应用程序可以发现其中有三种方法，具体取决于是否在客户端面向的 Exchange Online 或 Exchange 内部部署的配置信息。 
  
**表 1。自动发现服务类型和 Exchange 适用性**

|**自动发现服务类型**|**适用于**|
|:-----|:-----|
|[SOAP 自动发现](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online 和版本的 Exchange 内部部署与 Exchange 2010 启动  <br/> |
|[POX 自动发现](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online 和版本的 Exchange 内部部署与 Exchange 2007 启动  <br/> |
|[服务连接点 (SCP) 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |版本的 Exchange 内部部署与 Exchange 2007 启动  <br/> |
   
除了了客户端的配置信息的 SOAP POX 自动发现还返回的 Exchange 服务版本和指示是否将服务承载的 Exchange Online。 在不同元素中，根据您使用的自动发现的类型，则返回此信息。
  
**表 2。返回服务版本和 Exchange Online 承载信息的自动发现元素**

|**自动发现服务类型**|**包含服务版本的 XML 元素**|**指示用户是否具有 Exchange Online 帐户的 XML 元素**|
|:-----|:-----|:-----|
|SOAP 自动发现  <br/> |具有**CasVersion**文本值的[设置 (SOAP)](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx)元素。  <br/> |具有**UserMSOnline**文本值的[设置 (SOAP)](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx)元素。  <br/> |
|POX 自动发现  <br/> |[ServerVersion (POX)](http://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
确保您的客户端捕获此信息，以便它可以指定[功能集](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)，可在 Exchange 服务器上的目标。 这很有用，以确定您的客户端是否可以预期不同的行为，基于用户的邮箱是否位于 Exchange Online 或 Exchange 内部部署组织。 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>面向 Exchange Online 的应用程序中的测试和日志文件

Exchange Online 不提供访问 EWS 协议日志文件、 EWS 性能计数器和本地 Exchange 服务器可用的 EWS 相关服务事件。 对这些访问很有用，但是，在发现您的应用程序时它与 EWS 交互的执行。 请确保您测试针对测试 Exchange 内部部署服务器应用程序，以便您可以优化性能。 如果可能，可以[更改的限制设置](http://technet.microsoft.com/en-us/library/bb232205%28v=exchg.150%29.aspx#Policies)在您的测试服务器，以匹配 Exchange Online 的限制设置，以便您可以评估您的应用程序连接到 Exchange Online 时的行为。 
  
> [!TIP]
> 您可以使用[EWSRelentless](https://ewsrelentless.codeplex.com/)工具执行 EWS 负载测试。 您可以使用此工具与测试服务器、 EWS 协议日志、 EWS 性能计数器，服务事件和限制设置 EWS 更好地了解 EWS 如何执行负载下。 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>限制设置和 Exchange Online

[EWS 限制设置](ews-throttling-in-exchange.md)的默认值是不同的 Exchange Online 比 Exchange 内部部署。 此外，您无法更改 Exchange Online 限制设置。 您可以使用 Exchange 命令行管理程序 cmdlet 可以发现 Exchange 内部部署; 的限制设置但是，这些 cmdlet 未启用 Exchange Online。 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Exchange 命令行管理程序 cmdlet 和配置设置

数 cmdlet 可以直接或间接会影响 web 服务 Api 在 Exchange Online 和 Exchange 内部部署。 不能用于 Exchange Online 中以下 Cmdlet:
  
- 限制设置 
    
- 虚拟目录设置 
    
- 身份验证设置
    
有关适用于 Exchange Online cmdlet 的详细信息，请参阅[Exchange Online 中的 PowerShell cmdlet](http://help.outlook.com/en-us/140/dd575549.aspx)。 有关 cmdlet 可供 Exchange 内部部署有关详细信息，请参阅[Exchange 2013 cmdlets](http://technet.microsoft.com/en-us/library/bb124413%28v=exchg.150%29.aspx)。
  
## <a name="client-affinity-and-network-load-balancers"></a>客户端关联性和网络负载平衡器
<a name="affinity"> </a>

大多数 EWS 通信不需要客户端参与维护与 Exchange 的相关性。 对邮箱事件的订阅并要求客户端提供 cookie 和其他信息以维护维护的用户的邮箱事件队列的 Exchange 服务器的关联。 Exchange Server 2010 使用 exchangecookie 维护跨网络负载平衡器的客户端相关性。 Exchange Online 和版本的 Exchange 内部部署 Exchange 2013 从开始使用[X AnchorMailbox 标头、 X PreferServerAffinity 页眉和 X BackEndOverrideCookie cookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained)维护邮箱通知的相关性。 
  
## <a name="authentication"></a>身份验证
<a name="auth"> </a>

客户端可以与 Exchange Online 使用进行身份验证 Basic 或 OAuth。 版本的 Exchange 内部部署 Exchange 2013 从开始使用 NTLM 默认设置。但是，就可以配置 Exchange 内部部署为使用基本身份验证以及。 
  
## <a name="client-latency-diagnostics"></a>客户端延迟诊断
<a name="diag"> </a>

Exchange Online 收集如果这些报告的客户端延迟诊断。 这有助于 Microsoft 技术支持解决与 Exchange Online 的连接问题。 Exchange 内部部署不会收集客户端延迟诊断。 如果您的客户端针对 Exchange 内部部署，客户端无法报告延迟诊断到服务器。
  
## <a name="functionality-in-the-ews-managed-api"></a>功能中的 ews 托管 API
<a name="ewsma"> </a>

EWS 托管 API 公开的特定于 Exchange 内部部署，如服务点连接查找和特定于 Exchange Online 中，如客户端延迟报告某些功能某些功能。 请注意，可能为某些之前实现 EWS 托管 API 在 Exchange Online 中实现的功能。 
  
以下 EWS 托管 API 功能仅适用于 Exchange Online:
  
- 客户端延迟报告
    
- 基本预身份验证
    
- 请求在响应中返回的了申请 Id 的能力
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>Exchange Online 的计划和 Exchange Server 版本中的 API 功能
<a name="exo"> </a>

在不同 Office 365 和 Exchange Online 计划中，或 Exchange 服务器的标准版和企业版本中，可能提供不同的功能集。 请注意，某些 API 功能可能不可用到具体取决于 Exchange Online 的计划或 Exchange Server edition 承载用户的邮箱客户端应用程序。 
  
**表 3。计划和版本之间的 API 功能变体**

|**API 功能**|**计划或 edition 注意事项**|
|:-----|:-----|
|EWS 访问帐户，除了通过 Exchange 模拟  <br/> |不允许在[为企业的 Office 365-Kiosk 计划](http://office.microsoft.com/en-us/business/compare-office-365-kiosk-plans-FX103178917.aspx)。  <br/> |
|统一消息 (UM)  <br/> |仅适用于 Office 365 企业版 (E3) 计划、 Exchange Online 计划 2 和 Exchange Server 2013 Enterprise 版本。  <br/> |
|Active Directory 域服务 (AD DS) 集成  <br/> |与 Office 365 小型企业版和 Office 365 小型企业高级版计划不可用。  <br/> |
|信息权限管理存档，和法律保留项  <br/> |仅适用于 Office 365 企业版 （E3 和 E4） 计划。  <br/> |
|数据丢失保护  <br/> |仅适用于 Office 365 企业版计划、 Exchange Online 计划 2 和 Exchange Server 2013 Enterprise 版本。  <br/> |
   
由于可以更改功能的可用性，我们建议您查看用于计算功能的可用性可能如何影响您的客户端的 Exchange Online 的计划和 Exchange Server 版本。 您还可以设计您的客户端使用[GetServiceConfiguration 操作](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)或发送实现功能的操作的测试请求检查功能的可用性。 如果功能不可用，将此类表示服务器响应。 
  
## <a name="other-considerations"></a>其他注意事项
<a name="other"> </a>

您可以执行以下时面向 Exchange 内部部署，但不是 Exchange Online:
  
- 创建 Exchange 服务器安装了客户端。 
    
- 安装[自定义传输代理](../transport-agents/transport-agents-in-exchange-2013.md)的可能影响的传送和创建和使用 EWS 和其他客户端发送的消息的内容。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
- [比较 Exchange Online 和 Exchange Server 2013](http://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [比较 Office 365 的业务计划](http://office.microsoft.com/en-us/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless-EWS 负载生成工具](https://ewsrelentless.codeplex.com/)
- [Exchange 和 EWS 托管 API 中的 web 服务 API 功能可用性](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [限制在 Exchange 中的 EWS](ews-throttling-in-exchange.md)
    

