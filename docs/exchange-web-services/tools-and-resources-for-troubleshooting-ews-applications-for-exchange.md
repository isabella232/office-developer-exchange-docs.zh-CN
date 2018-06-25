---
title: 工具和资源来解决 exchange 的 EWS 应用程序
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: 查找资源以帮助您解决您 EWS 托管 API 或 EWS 应用程序。
ms.openlocfilehash: d8d8ea736ca3b896642ad06f5987caeba8d8d059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753015"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>工具和资源来解决 exchange 的 EWS 应用程序

查找资源以帮助您解决您 EWS 托管 API 或 EWS 应用程序。
  
按计划并不总是会事项。 有时 EWS 请求失败，或提供意外的结果。 可能会失败，尤其是原因不明显。 可望这永远不会发生，但如果是这样，本文提供了有关工具和资源可用于帮助解决您的问题的信息。
  
> [!NOTE]
> 本文提供故障排除的一般性建议和源的疑难解答信息。 遗憾的是不可能以提供详细的故障排除步骤。 您的特定错误进行疑难解答的帮助，请参阅[下一步步骤](#bk_NextSteps)。 
  
## <a name="examine-the-soap-requests-and-responses"></a>检查的 SOAP 请求和响应

当操作不能正常工作时，它真正有助于将能够看到了什么事。 查询时检查应用程序发送通过网络的请求和响应的服务器发送回调查问题 EWS 或 EWS 托管 API （英文） 是第一行。
  
EWS 托管 API 轻松检查 SOAP 请求和响应与其[内置的跟踪功能](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)。 如果您使用 EWS，您可能或可能无法访问类似的跟踪功能，具体取决于哪些平台或您使用发送您的请求的类。 但是，始终可以使用[网络监视器](http://www.microsoft.com/en-us/download/details.aspx?id=4865)或[Fiddler](http://www.telerik.com/fiddler)网络跟踪工具检查网络流量和查看请求和响应的有效负荷。 
  
此外，您还可以[检测客户端请求](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)以增强请求和响应中提供的信息。 
  
请求和响应后，问自己以下： 执行表现正确？ 是您的应用程序发送预期的值？ 响应意义吗？
  
## <a name="examine-error-codes"></a>检查错误代码

有时的错误代码可以继续对于查明问题，即使它似乎有意义的第一次看到。 此错误指示正在[受到控制](ews-throttling-in-exchange.md)您的客户端？ 可能对自动发现刷新[配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)的调用是顺序？ 
  
有关处理特定错误的详细信息，请参阅以下文章：
  
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [在 Exchange 处理与通知相关 EWS 中的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 处理同步相关 EWS 中的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 处理删除相关 EWS 中的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>验证版本

有 EWS 操作中所涉及的不同组件的数量，这些组件的版本会影响结果。
  
**表 1。可能会影响 EWS 过程的版本控制组件**

|**组件**|**EWS Managed API**|**EWS**|**备注**|
|:-----|:-----|:-----|:-----|
|请求的服务器版本  <br/> |[ExchangeServiceBase.RequestedServerVersion](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)属性  <br/> |[RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)元素  <br/> |此值控制哪个版本的 EWS 架构用于处理 EWS 请求。 请确保，此处指定的架构版本有意义请求所发送。 某些属性和操作不可用在早期版本的架构。  <br/> |
|服务器版本  <br/> |[ExchangeServiceBase.ServerInfo](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx)属性  <br/> |[ServerVersionInfo](http://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx)元素  <br/> |此值由服务器 EWS 响应中返回，并指示处理响应的服务器版本。 确保此值是您的预期。 如果可能，请确保 Exchange 服务器正在运行的主要版本 Exchange 的最新的更新。  <br/> |
|EWS 托管 API 版本  <br/> |Microsoft.Exchange.WebServices.dll 文件的产品版本属性。  <br/> |不适用  <br/> |如果您正在使用 EWS 托管 API，请确保您使用的[最新版本](http://aka.ms/ews-managed-api-readme)。  <br/> |
   
## <a name="verify-access"></a>验证访问权限

EWS 被启用的默认情况下，但[可以更改默认值](how-to-control-access-to-ews-in-exchange.md)。 使用[Get-organizationconfig](http://technet.microsoft.com/en-us/library/bb124754.aspx) cmdlet，以确保 EWS 已启用的服务器上，并使用[Get-casmailbox](http://technet.microsoft.com/en-us/library/aa997571.aspx) cmdlet 以确保 EWS 已启用的用户的邮箱。 此外可以检查这两个 cmdlet 响应的 EWS 允许或阻止列表中，并确保您的应用程序不阻止使用 EWS。 
  
您还应验证尚未修改 EWS 虚拟目录上的[默认身份验证设置](http://technet.microsoft.com/en-us/library/gg247612%28v=exchg.150%29.aspx)。 
  
## <a name="try-another-ews-client"></a>尝试另一个 EWS 客户端

有时非常有用尝试从另一个客户端相同的请求和比较结果。 如果另一个客户端获取不同的结果，什么是不同？ 找出请求成功和失败的请求之间的不同，可以帮助解释特定请求失败的原因。
  
当然，您可以编写测试与另一个客户端，而您没有为 ！ [EWSEditor](http://ewseditor.codeplex.com/)是使用 EWS 托管 API 和 EWS 示例客户端。 您可以下载客户端 （包括源代码），并使用它来尝试相同应用程序中失败的请求。 
  
## <a name="examine-iis-logs"></a>检查 IIS 日志

如果您有权访问 Exchange server，提供在客户端访问服务器上的 Internet 信息服务 (IIS) 日志记录功能可以提供有关失败的详细信息。 但是，请记住，IIS 日志将只能非常有用，如果您收到 HTTP 错误。
  
IIS 提供两种不同的日志记录方法： [IIS 日志记录](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)和[跟踪失败的请求](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)。 若要使用 IIS 日志，您可以使用[Log Parser Studio](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)，其中包括内置 EWS 查询数。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_NextSteps"> </a>

现在，您已了解工具和资源可用于解决，您可能需要了解这些工具提供的信息的帮助。 以下是一些用于获取帮助选项：
  
- [MSDN 上的 Exchange Server 开发论坛](http://social.msdn.microsoft.com/Forums/en-US/home?category=exchangeserver)— 提出 MSDN Exchange Server 开发社区的问题。 
    
- [StackOverflow](http://stackoverflow.com/tags/ews) — 提出 StackOverflow 社区的问题。 请务必标记"ews"与您的帖子。 
    
- [Microsoft 支持](http://support.microsoft.com/ph/730/en-us)— 与 Microsoft 支持专业人员联系以寻求帮助。 
    
## <a name="see-also"></a>另请参阅


请参阅以下文章：
  
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [跟踪请求和响应解决 EWS 托管 API 应用程序](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [在 Exchange 检测 EWS 和 REST 的客户端请求](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [限制在 Exchange 中的 EWS](ews-throttling-in-exchange.md)
    
- [使用自动发现刷新配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [在 Exchange 处理与通知相关 EWS 中的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 处理同步相关 EWS 中的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 处理删除相关 EWS 中的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [在 IIS 中配置日志记录](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [疑难解答失败的请求在 IIS 7 中使用跟踪](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [Log Parser Studio 简介：](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Exchange 虚拟目录的默认设置](http://technet.microsoft.com/en-us/library/gg247612%28v=exchg.150%29.aspx)
    
下载以下组件：
  
- [Microsoft 网络监视器 3.4](http://www.microsoft.com/en-us/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [Exchange Web Services 托管的 API](http://go.microsoft.com/fwlink/?LinkID=255472)
    

