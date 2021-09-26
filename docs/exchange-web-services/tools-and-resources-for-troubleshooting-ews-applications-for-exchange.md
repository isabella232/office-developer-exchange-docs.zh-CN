---
title: 用于对 Exchange 的 EWS 应用程序进行故障排除的工具和资源
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: 查找可帮助你解决 EWS 托管 API 或 EWS 应用程序问题的资源。
localization_priority: Priority
ms.openlocfilehash: 8a65b06cf911cd033d7fe5fe1b4566a7496de784
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542580"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>用于对 Exchange 的 EWS 应用程序进行故障排除的工具和资源

查找可帮助你解决 EWS 托管 API 或 EWS 应用程序问题的资源。
  
事情并不总是按计划进行。 有时 EWS 请求失败，或提供意外结果。 这可能令人沮丧，尤其是在原因不明显时。 希望这永远不会发生，但如果这样，本文将提供可用于帮助解决问题的工具和资源的信息。
  
> [!NOTE]
> 本文提供了一般疑难解答建议和疑难解答信息源。 遗憾的是，无法提供详细的故障排除步骤。 有关对特定错误进行故障排除的帮助，请参阅 [后续步骤](#bk_NextSteps)。 
  
## <a name="examine-the-soap-requests-and-responses"></a>检查 SOAP 请求和响应

如果工作不正常，能够看到发生了什么真的很有帮助。 调查 EWS 或 EWS 托管 API 的问题时，第一条查询是检查应用程序通过网络发送的请求以及服务器发送回的响应。
  
EWS 托管 API 使用其[内置跟踪功能](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)使检查 SOAP 请求和响应变得容易。 如果正在使用 EWS，你可能有或可能没有访问类似跟踪功能的权限，具体取决于用于发送请求的平台或类。 但是，你始终可以使用网络跟踪工具（如[网络监视器](https://www.microsoft.com/download/details.aspx?id=4865)或 [Fiddler](http://www.telerik.com/fiddler)）来检查网络流量并查看请求和响应负载。 
  
此外，你可以[检测客户端请求](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)以增加请求和响应中可用的信息。 
  
收到请求和响应后，询问你自己：它们看起来是否正确？ 应用程序发送的值是否符合预期？ 响应是否有意义？
  
## <a name="examine-error-codes"></a>检查错误代码

有时，错误代码对查明问题大有帮助，即使第一次看到似乎没有意义。 该错误是否表明客户端受到[限制](ews-throttling-in-exchange.md)？ 是否可以调用自动发现来[刷新配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)？ 
  
有关处理特定错误的详细信息，请参阅以下文章：
  
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [在 Exchange 中处理 EWS 中与通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中与同步相关的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中与删除相关的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>验证版本

EWS 操作涉及许多不同组件，这些组件的版本可能会影响结果。
  
**表 1.可能影响 EWS 进程的版本控制组件**

|**组件**|**EWS 托管 API**|**EWS**|**注释**|
|:-----|:-----|:-----|:-----|
|已请求的服务器版本  <br/> |[ExchangeServiceBase.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) 属性  <br/> |[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx) 元素  <br/> |该值控制使用哪个版本的 EWS 架构来处理 EWS 请求。 确保此处指定的架构版本对你发送的请求有意义。 某些属性和操作在架构的早期版本中不可用。  <br/> |
|服务器版本  <br/> |[ExchangeServiceBase.ServerInfo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx) 属性  <br/> |[ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx) 元素  <br/> |该值由服务器在 EWS 响应中返回，并指示处理响应的服务器的版本。 确保此值符合预期。 如果可能，请确保 Exchange 服务器运行 Exchange 主要版本的最新更新。  <br/> |
|EWS 托管 API 版本  <br/> |Microsoft.Exchange.WebServices.dll 文件的产品版本属性。  <br/> |不适用  <br/> |如果使用的是 EWS 托管 API，请确保使用的是[最新版本](https://aka.ms/ews-managed-api-readme)。  <br/> |
   
## <a name="verify-access"></a>验证访问

默认情况下启用 EWS，但[可以更改默认值](how-to-control-access-to-ews-in-exchange.md)。 使用 [Get-OrganizationConfig](https://technet.microsoft.com/library/bb124754.aspx) cmdlet 确保在服务器上启用 EWS，并使用 [Get-CASMailbox](https://technet.microsoft.com/library/aa997571.aspx) cmdlet 确保为用户邮箱启用 EWS。 还要检查 EWS 允许或阻止列表的两个 cmdlet 响应，并确保应用程序没有阻止使用 EWS。 
  
还应验证 EWS 虚拟目录上的[默认身份验证设置](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)是否尚未修改。 
  
## <a name="try-another-ews-client"></a>尝试其他 EWS 客户端

有时，尝试来自另一个客户端的相同请求并比较结果会很有帮助。 如果另一个客户端得到不同的结果，有什么不同？ 找出成功请求和失败请求之间的区别有助于解释特定请求失败的原因。
  
尽管你当然可以编写要测试的另一个客户端，但不必这样！ [EWSEditor](http://ewseditor.codeplex.com/) 是使用 EWS 托管 API 和 EWS 的示例客户端。 你可以下载客户端（包含源代码）并使用它以尝试应用程序中失败的相同请求。 
  
## <a name="examine-iis-logs"></a>检查 IIS 日志

如果你有权访问 Exchange 服务器，则客户端访问服务器上的 Internet Information Services (IIS) 提供的日志记录功能可以提供有关故障的详细信息。 但是，请注意，IIS 日志仅在你收到 HTTP 错误时有用。
  
IIS 提供了两种不同的日志记录方法：[IIS 日志记录](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)和[失败请求跟踪](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)。 若要使用 IIS 日志，可以使用 [Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)，其中包含大量内置 EWS 查询。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_NextSteps"> </a>

现在，你已了解可用于排除故障的工具和资源，你可能需要帮助以了解这些工具提供的信息。 以下是获取帮助的一些选项：
  
- [MSDN 上的 Exchange 服务器开发论坛](https://social.msdn.microsoft.com/Forums/home?category=exchangeserver) - 向 MSDN Exchange 服务器开发社区提问。 
    
- [StackOverflow](http://stackoverflow.com/tags/ews) - 向 StackOverflow 社区提问。 请务必使用“ews”标记帖子。 
    
- [Microsoft 支持](https://support.microsoft.com/ph/730/en-us) - 联系 Microsoft 支持专业人员寻求帮助。 
    
## <a name="see-also"></a>另请参阅


另请参阅以下文章：
  
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [跟踪请求和响应以便解决 EWS 托管 API 应用程序的故障](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [在 Exchange 中检测 EWS 和 REST 的客户端请求](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [Exchange 中的 EWS 限制](ews-throttling-in-exchange.md)
    
- [使用自动发现刷新配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [在 Exchange 中处理 EWS 中与通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中与同步相关的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中与删除相关的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [在 IIS 中配置日志记录](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [使用 IIS 7 中的跟踪对失败请求进行故障排除](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [介绍：Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Exchange 虚拟目录的默认设置](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)
    
下载以下内容：
  
- [Microsoft 网络监视器 3.4](https://www.microsoft.com/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [Exchange Web 服务托管 API](https://www.nuget.org/packages/Microsoft.Exchange.WebServices/)
