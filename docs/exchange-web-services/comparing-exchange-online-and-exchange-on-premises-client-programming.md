---
title: 比较 Exchange Online 和 Exchange 本地客户端编程
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3c2eabe4-52bc-461e-a6dd-f65f22f16e50
description: 了解创建 EWS 托管 API 或 EWS 客户端应用程序的设计注意事项，该应用程序适用于本地Exchange Online Exchange应用程序。
ms.openlocfilehash: 438965656e31eca586d06a5e0b6794c0eda87621
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512286"
---
# <a name="comparing-exchange-online-and-exchange-on-premises-client-programming"></a>比较 Exchange Online 和 Exchange 本地客户端编程

了解创建 EWS 托管 API 或 EWS 客户端应用程序的设计注意事项，该应用程序适用于本地Exchange Online Exchange应用程序。
  
大多数情况下，Exchange中面向的客户端和 Web 服务将以相同方式工作，无论目标是 Exchange Online、Exchange Online 作为 Office 365 的一部分还是 Exchange 本地服务器。 但是，存在一些例外情况，您需要确保应用程序可以处理它们。 使用本文中的信息可帮助您将客户端设计为面向本地Exchange Online Exchange客户端。

<a name="autodiscover"> </a>

## <a name="autodiscover-client-programming-considerations"></a>自动发现客户端编程注意事项

[自动发现](autodiscover-for-exchange.md)为客户端Exchange信息。 客户端应用程序可以通过以下三种方法之一发现其配置信息，具体取决于客户端是面向Exchange Online还是Exchange内部部署。 
  
**表 1.自动发现服务类型和Exchange适用性**

|**自动发现服务类型**|**适用对象**|
|:-----|:-----|
|[SOAP 自动发现](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online 2010 Exchange起本地部署 Exchange版本  <br/> |
|[POX 自动发现](autodiscover-for-exchange.md#bk_Options) <br/> |Exchange Online 2007 Exchange起本地部署 Exchange版本  <br/> |
|[服务连接点 (SCP) 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md) <br/> |自 2007 Exchange起本地部署Exchange版本  <br/> |
   
除了客户端配置信息之外，该 SOAP 和 POX 自动发现还返回 Exchange 服务版本，并指示该服务是否由 Exchange Online。 此信息在不同的元素中返回，具体取决于使用的自动发现类型。
  
**表 2.返回服务版本和托管信息Exchange Online自动发现元素**

|**自动发现服务类型**|**包含服务版本的 XML 元素**|**XML 元素，指示用户是否有Exchange Online帐户**|
|:-----|:-----|:-----|
|SOAP 自动发现  <br/> |[使用 casVersion (值)](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) **SOAP** 元素。  <br/> |[设置 (SOAP)](https://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) **UserMSOnline** 文本值的元素。  <br/> |
|POX 自动发现  <br/> |[ServerVersion (POX)](https://msdn.microsoft.com/library/2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a%28Office.15%29.aspx) <br/> |**MicrosoftOnline** <br/> |
   
确保客户端捕获此信息，以便它可以面向在 Exchange 服务器上可用的[](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)功能集。 这可用于根据用户邮箱位于内部部署组织中还是本地Exchange Online Exchange预期不同的行为。 

<a name="testing"> </a>

## <a name="testing-and-log-files-in-applications-that-target-exchange-online"></a>在面向用户的应用程序中测试和Exchange Online

Exchange Online不提供对 EWS 协议日志文件、EWS 性能计数器和 EWS 相关服务事件的访问权限，这些事件在本地服务器中Exchange可用。 但是，在发现应用程序与 EWS 交互时如何执行这些访问非常有用。 请确保针对本地服务器测试Exchange，以便优化其性能。 如果可能，可以更改测试[](https://technet.microsoft.com/library/bb232205%28v=exchg.150%29.aspx#Policies)服务器上限制设置以匹配 Exchange Online 限制设置，以便评估应用程序在连接到 Exchange Online 时的行为方式。 
  
> [!TIP]
> 可以使用 [EWSRelentless](https://ewsrelentless.codeplex.com/) 工具执行 EWS 负载测试。 可以将此工具与测试服务器、EWS 协议日志、EWS 性能计数器、服务事件和 EWS 限制设置一同使用，以更好地了解 EWS 在负载下如何执行。 

<a name="throttling"> </a>

## <a name="throttling-settings-and-exchange-online"></a>限制设置和Exchange Online

[EWS](ews-throttling-in-exchange.md)限制设置的默认值对于内部部署Exchange Online它们Exchange不同。 此外，您无法更改Exchange Online限制设置。 可以使用命令行Exchange cmdlet 发现本地Exchange限制设置;但是，这些 cmdlet 未启用Exchange Online。 

<a name="ems"> </a>

## <a name="exchange-management-shell-cmdlets-and-configuration-settings"></a>Exchange命令行管理程序 cmdlet 和配置设置

许多 cmdlet 可以直接或间接影响本地和本地Exchange Online Exchange Web 服务 API。 Cmdlet 不适用于以下Exchange Online：
  
- 限制设置 
    
- 虚拟目录设置 
    
- 身份验证设置
    
有关可用于 Exchange Online cmdlet 的详细信息，请参阅 Exchange Online 中的[PowerShell cmdlet。](http://help.outlook.com/140/dd575549.aspx) 有关可用于本地部署Exchange [cmdlet，请参阅 Exchange 2013 cmdlet。](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx)
  
## <a name="client-affinity-and-network-load-balancers"></a>客户端相关性和网络负载平衡器
<a name="affinity"> </a>

大多数 EWS 通信不要求客户端参与保持与 Exchange。 对邮箱事件的订阅需要客户端提供 Cookie 和其他信息，以保持与维护用户邮箱事件队列的 Exchange 服务器之间的相关性。 Exchange Server 2010 使用 exchangecookie 在网络负载平衡器中维护客户端相关性。 Exchange Online Exchange 2013 起本地 Exchange 的 Exchange 和版本使用[X-AnchorMailbox 标头、X-PreferServerAffinity 标头和 X-BackEndOverrideCookie](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_howmaintained) Cookie 维护邮箱通知的关联性。 
  
## <a name="authentication"></a>身份验证
<a name="auth"> </a>

客户端可以使用 Basic Exchange Online OAuth 对客户端进行身份验证。 自 2013 Exchange起本地部署Exchange默认使用 NTLM;但是，可以将本地Exchange配置为使用基本身份验证。 
  
## <a name="client-latency-diagnostics"></a>客户端延迟诊断
<a name="diag"> </a>

Exchange Online报告时收集客户端延迟诊断。 这有助于 Microsoft 支持解决与 Exchange Online 的连接Exchange Online。 Exchange本地部署不会收集客户端延迟诊断。 如果客户端面向Exchange，则客户端无法向服务器报告延迟诊断。
  
## <a name="functionality-in-the-ews-managed-api"></a>EWS 托管 API 中的功能
<a name="ewsma"> </a>

EWS 托管 API 公开了一些特定于本地 Exchange 的功能（如服务点连接查找）和特定于 Exchange Online 的一些功能（如客户端延迟报告）。 请注意，某些功能可以在 EWS 托管 API 中Exchange Online EWS 托管 API 中实现。 
  
以下 EWS 托管 API 功能仅适用于Exchange Online：
  
- 客户端延迟报告
    
- 基本预身份验证
    
- 请求在响应中返回 RequestId 的能力
    
## <a name="api-features-in-exchange-online-plans-and-exchange-server-editions"></a>Exchange Online和Exchange Server中的 API 功能
<a name="exo"> </a>

不同的功能集可能在不同Office 365和Exchange Online计划中提供，也可能在 Exchange Server 标准和企业版本中提供。 请注意，根据托管用户邮箱的 Exchange Online 或 Exchange Server 版本，某些 API 功能可能无法供客户端应用程序使用。 
   
由于功能可用性可能会更改，我们建议你查看Exchange Online版本Exchange Server评估功能可用性对客户端的影响。 您还可以使用 [GetServiceConfiguration](how-to-get-service-configuration-information-by-using-ews-in-exchange.md) 操作或发送针对实现这些功能的操作的测试请求，将客户端设计为检查功能可用性。 如果此功能不可用，则来自服务器的响应将指出这一点。 
  
## <a name="other-considerations"></a>其他注意事项
<a name="other"> </a>

在面向本地用户时Exchange执行下列操作，Exchange Online：
  
- 创建安装在 Exchange 上的客户端。 
    
- 安装 [可能影响您](../transport-agents/transport-agents-in-exchange-2013.md) 创建并随 EWS 和其他客户端发送的邮件的传递和内容的自定义传输代理。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
- [比较 Exchange Online 和 Exchange Server 2013](https://blogs.technet.com/b/exchange/archive/2012/09/19/comparing-exchange-online-and-exchange-server-2013.aspx)  
- [比较Office 365计划的所有项目](https://office.microsoft.com/business/compare-all-office-365-for-business-plans-FX104051403.aspx)
- [EwsRelentless - EWS 负载生成工具](https://ewsrelentless.codeplex.com/)
- [Web 服务 API 功能在 Exchange 和 EWS 托管 API 中的可用性](web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md)
- [Exchange 中的 EWS 限制](ews-throttling-in-exchange.md)
    

