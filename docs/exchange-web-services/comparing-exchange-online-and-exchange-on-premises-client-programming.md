---
title: 比较 Exchange Online 和 Exchange 本地客户端编程
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: 了解有关创建可用于 Exchange Online 和 Exchange 本地 Exchange 的 EWS 托管 API 或 EWS 客户端应用程序的设计注意事项。
ms.openlocfilehash: 8b4dbae5cadfed377aa3a7179144a7cea68bc35c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456162"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>比较 Exchange Online 和 Exchange 本地客户端编程

了解有关创建可用于 Exchange Online 和 Exchange 本地 Exchange 的 EWS 托管 API 或 EWS 客户端应用程序的设计注意事项。
  
大多数情况下，客户端和 Exchange 中的 web 服务将以相同的方式工作，无论目标是 Exchange Online、Exchange Online 还是 Office 365 的一部分，还是 Exchange 本地服务器。 但有一些例外情况，您需要确保您的应用程序可以处理它们。 使用本文中的信息可帮助您设计客户端以同时面向 Exchange Online 和 Exchange 内部部署。

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>自动发现客户端编程注意事项

[自动发现](autodiscover-for-exchange.md)提供了 Exchange 客户端的配置信息。 客户端应用程序可以通过三种方式之一发现其配置信息，具体取决于客户端是面向 Exchange Online 还是本地 Exchange。 
  
**表1。自动发现服务类型和 Exchange 适用性**

|**自动发现服务类型**|**适用于**|
|:-----|:-----|
|[SOAP 自动发现](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online 和本地 Exchange 版本（从 Exchange 2010 开始）  <br/> |
|[POX 自动发现](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online 和本地 Exchange 版本（从 Exchange 2007 开始）  <br/> |
|[服务连接点（SCP）查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |从 Exchange 2007 开始的 Exchange 内部版本  <br/> |
   
除了客户端配置信息之外，SOAP 和 POX 自动发现还返回 Exchange 服务版本，并指示该服务是否由 Exchange Online 托管。 此信息在不同的元素中返回，具体取决于您使用的自动发现的类型。
  
**表2。返回服务版本和 Exchange Online 托管信息的自动发现元素**

|**自动发现服务类型**|**包含服务版本的 XML 元素**|**指示用户是否具有 Exchange Online 帐户的 XML 元素**|
|:-----|:-----|:-----|
|SOAP 自动发现  <br/> |使用**CasVersion**文本值[设置（SOAP）](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx)元素。  <br/> |使用**UserMSOnline**文本值[设置（SOAP）](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx)元素。  <br/> |
|POX 自动发现  <br/> |[ServerVersion （POX）](https://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
确保您的客户端捕获此信息，以便它能够针对 Exchange 服务器上提供的[功能集](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)。 这可用于根据用户的邮箱位于 Exchange Online 组织还是 Exchange 内部部署组织，确定客户端是否可以预期不同的行为。 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>在面向 Exchange Online 的应用程序中测试和记录文件

Exchange Online 不提供对在本地 Exchange 服务器上可用的 EWS 协议日志文件、EWS 性能计数器和 EWS 相关的服务事件的访问权限。 但是，在发现应用程序与 EWS 交互时，对这些权限的访问很有用。 请确保针对测试 Exchange 内部部署服务器测试应用程序，以便优化其性能。 如果可能，可以将测试服务器上[的限制设置更改](https://technet.microsoft.com/library/bb232205%28v=exchg.150%29.aspx#Policies)为与 exchange online 的限制设置相匹配，以便您可以评估应用程序连接到 Exchange online 时的行为。 
  
> [!TIP]
> 您可以使用[EWSRelentless](https://ewsrelentless.codeplex.com/)工具执行 EWS 负载测试。 您可以将此工具与测试服务器、EWS 协议日志、EWS 性能计数器、服务事件和 EWS 限制设置结合使用，以更好地理解 EWS 在负载下的执行情况。 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>限制设置和 Exchange Online

Exchange Online 的[EWS 限制设置](ews-throttling-in-exchange.md)的默认值与 Exchange 本地 exchange 的默认值不同。 此外，不能更改 Exchange Online 限制设置。 您可以使用 Exchange 命令行管理程序 cmdlet 来发现本地 Exchange 的限制设置;但是，不会为 Exchange Online 启用这些 cmdlet。 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Exchange 命令行管理程序 cmdlet 和配置设置

许多 cmdlet 可以直接或间接地影响 Exchange Online 和 Exchange 内部部署中的 web 服务 Api。 Cmdlet 在 Exchange Online 中不可用于以下内容：
  
- 限制设置 
    
- 虚拟目录设置 
    
- 身份验证设置
    
有关可用于 Exchange Online 的 cmdlet 的详细信息，请参阅[Exchange online 中的 PowerShell cmdlet](http://help.outlook.com/140/dd575549.aspx)。 有关可用于 Exchange 本地的 cmdlet 的详细信息，请参阅[exchange 2013 cmdlet](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx)。
  
## <a name="client-affinity-and-network-load-balancers"></a>客户端相关性和网络负载平衡器
<a name="affinity"> </a>

大多数 EWS 通信不要求客户端参与与 Exchange 的保持关系。 对邮箱事件的订阅需要客户端提供 cookie 和其他信息来维护与维护用户的邮箱事件队列的 Exchange 服务器的相关性。 Exchange Server 2010 使用 exchangecookie 维护跨网络负载平衡器的客户端相关性。 Exchange Online 和本地 Exchange 版本（从 Exchange 2013 开始）使用[x-anchormailbox 头、x-PreferServerAffinity 头和 x-BackEndOverrideCookie cookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained)来维护邮箱通知的相关性。 
  
## <a name="authentication"></a>身份验证
<a name="auth"> </a>

客户端可以使用基本或 OAuth 通过 Exchange Online 进行身份验证。 从 Exchange 2013 开始的 Exchange 内部版本在默认情况下使用 NTLM。但是，也可以将本地 Exchange 配置为使用基本身份验证。 
  
## <a name="client-latency-diagnostics"></a>客户端延迟诊断
<a name="diag"> </a>

Exchange Online 收集客户端延迟诊断（如果报告）。 这有助于 Microsoft 支持解决 Exchange Online 的连接问题。 Exchange 本地不会收集客户端延迟诊断。 如果您的客户端以本地 Exchange 为目标，客户端将无法向服务器报告延迟诊断。
  
## <a name="functionality-in-the-ews-managed-api"></a>EWS 托管 API 中的功能
<a name="ewsma"> </a>

EWS 托管 API 公开一些特定于 Exchange 本地的功能，如服务点连接查找，以及特定于 Exchange Online 的一些功能，如客户端延迟报告。 请注意，在在 EWS 托管 API 中实现某些功能之前，可能会在 Exchange Online 中实现这些功能。 
  
下面的 EWS 托管 API 功能仅适用于 Exchange Online：
  
- 客户端延迟报告
    
- 基本预身份验证
    
- 能够请求在响应中返回 RequestId
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>Exchange Online 计划和 Exchange Server 版本中的 API 功能
<a name="exo"> </a>

不同的功能集可能在不同的 Office 365 和 Exchange Online 计划中，或者在 Exchange Server 的标准版和企业版中可用。 请注意，您的客户端应用程序可能无法使用某些 API 功能，具体取决于承载用户邮箱的 Exchange Online 计划或 Exchange Server 版本。 
  
**表3。跨计划和版本的 API 功能差异**

|**API 功能**|**计划或版本注意事项**|
|:-----|:-----|

|对帐户的 EWS 访问（通过 Exchange 模拟除外）  <br/> |在[Office 365 for business 中不允许-Kiosk 计划](https://office.microsoft.com/business/compare-office-365-kiosk-plans-FX103178917.aspx)。  <br/> |


|统一消息（UM）  <br/> |仅适用于 Office 365 企业版（E3）计划、Exchange Online 计划2和 Exchange Server 2013 企业版。  <br/> | |Active Directory 域服务（AD DS）集成  <br/> |不适用于 Office 365 小型企业版和 Office 365 小型企业高级版计划。  <br/> | |信息权限管理、存档和法律保留  <br/> |仅适用于 Office 365 企业版（E3 和 E4）计划。  <br/> | |数据丢失保护  <br/> |仅适用于 Office 365 企业版计划、Exchange Online 计划2和 Exchange Server 2013 企业版。  <br/> |
   
由于功能可用性可能会发生更改，因此建议您查看 Exchange Online 计划和 Exchange Server 版本，以评估功能可用性对客户端有何影响。 您还可以通过使用[GetServiceConfiguration 操作](how-to-get-service-configuration-information-by-using-ews-in-exchange.md)或通过发送实现功能的操作的测试请求，来设计客户端，以检查功能可用性。 如果功能不可用，则来自服务器的响应将指示这样。 
  
## <a name="other-considerations"></a>其他注意事项
<a name="other"> </a>

在面向 Exchange 本地（而非 Exchange Online）时，您可以执行以下操作：
  
- 创建一个安装在 Exchange 服务器上的客户端。 
    
- 安装可影响您使用 EWS 和其他客户端创建和发送的邮件的传递和内容的[自定义传输代理](../transport-agents/transport-agents-in-exchange-2013.md)。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
- [比较 Exchange Online 和 Exchange Server 2013](https://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [比较所有 Office 365 for business 计划](https://office.microsoft.com/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless-EWS 加载生成工具](https://ewsrelentless.codeplex.com/)
- [Exchange 和 EWS 托管 API 中的 Web 服务 API 功能可用性](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [Exchange 中的 EWS 限制](ews-throttling-in-exchange.md)
    

