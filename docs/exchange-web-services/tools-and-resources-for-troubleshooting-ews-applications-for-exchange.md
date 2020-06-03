---
title: 工具和资源来解决 exchange 的 EWS 应用程序
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: 查找可帮助您对 EWS 托管 API 或 EWS 应用程序进行故障排除的资源。
localization_priority: Priority
ms.openlocfilehash: 7c7cbe8c93edec5ad99df079c6eb96286c1ba063
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463739"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>工具和资源来解决 exchange 的 EWS 应用程序

查找可帮助您对 EWS 托管 API 或 EWS 应用程序进行故障排除的资源。
  
有些事情并不总是按计划进行。 有时 EWS 请求失败，或提供意外的结果。 这可能会令人沮丧，尤其是当原因不明显时。 但愿这永远不会发生，但如果是这样，本文将提供有关工具和资源的信息，您可以使用这些工具和资源来帮助您解决问题。
  
> [!NOTE]
> 本文提供了有关疑难解答信息的一般故障排除建议和源。 遗憾的是，不能提供详细的故障排除步骤。 有关解决特定错误的帮助，请参阅[后续步骤](#bk_NextSteps)。 
  
## <a name="examine-the-soap-requests-and-responses"></a>检查 SOAP 请求和响应

当事情不能正常运行时，它确实有助于查看发生的情况。 在调查 EWS 或 EWS 托管 API 的问题时，第一行查询是检查您的应用程序通过网络发送的请求以及服务器发送回的响应。
  
EWS 托管 API 使 SOAP 请求和响应易于通过其[内置跟踪功能](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)进行检查。 如果使用 EWS，则可能会也可能无法访问类似的跟踪功能，具体取决于用于发送请求的平台或类。 但是，您始终可以使用网络跟踪工具（如[网络监视器](https://www.microsoft.com/download/details.aspx?id=4865)或[Fiddler](http://www.telerik.com/fiddler) ）来检查网络流量并查看请求和响应负载。 
  
此外，还可以[检测客户端请求](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)，以增强请求和响应中提供的信息。 
  
在获得请求和响应后，请自己询问以下各项：是否正确？ 您的应用程序是否需要发送的值是什么？ 做出的响应是否有意义？
  
## <a name="examine-error-codes"></a>检查错误代码

有时，错误代码可能会很长一段时间来查明问题，即使乍一看看似乎没有意义也是如此。 该错误是否指示正在[限制](ews-throttling-in-exchange.md)你的客户端？ 可能会调用自动发现以[刷新配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)，是否按顺序进行？ 
  
有关处理特定错误的详细信息，请参阅以下文章：
  
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [在 Exchange 中处理 EWS 中与通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中与同步相关的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中的与删除相关的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>验证版本

EWS 操作中涉及许多不同的组件，这些组件的版本可能会影响结果。
  
**表1。可能影响 EWS 进程的版本控制组件**

|**组件**|**EWS Managed API**|**EWS**|**备注**|
|:-----|:-----|:-----|:-----|
|请求的服务器版本  <br/> |[ExchangeServiceBase](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)属性  <br/> |[RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)元素  <br/> |此值控制用于处理 EWS 请求的 EWS 架构的版本。 请确保在此处指定的架构版本对要发送的请求有意义。 某些属性和操作在架构的早期版本中不可用。  <br/> |
|服务器版本  <br/> |[ExchangeServiceBase](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx)属性  <br/> |[ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx)元素  <br/> |此值由服务器以 EWS 响应的形式返回，并指示处理响应的服务器的版本。 请确保此值是您所期望的值。 如果可能，请确保 Exchange 服务器对你的主要版本的 Exchange 运行的是最新的更新。  <br/> |
|EWS 托管 API 版本  <br/> |WebServices 文件的 "产品版本" 属性。  <br/> |不适用  <br/> |如果使用的是 EWS 托管 API，请确保使用的是[最新版本](https://aka.ms/ews-managed-api-readme)。  <br/> |
   
## <a name="verify-access"></a>验证访问

默认情况下，EWS 处于启用状态，但[可以更改默认值](how-to-control-access-to-ews-in-exchange.md)。 使用[set-organizationconfig](https://technet.microsoft.com/library/bb124754.aspx) cmdlet 可确保在服务器上启用 ews，并使用[set-casmailbox](https://technet.microsoft.com/library/aa997571.aspx) cmdlet 来确保为用户的邮箱启用了 ews。 此外，请检查 EWS 允许或阻止列表的 cmdlet 响应，并确保您的应用程序不会被阻止使用 EWS。 
  
此外，还应验证 EWS 虚拟目录上的[默认身份验证设置](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)是否尚未修改。 
  
## <a name="try-another-ews-client"></a>尝试其他 EWS 客户端

有时，尝试来自另一个客户端的相同请求并比较结果会很有帮助。 如果其他客户端得到不同的结果，有何不同？ 在成功的请求和失败的请求之间找出不同的信息可帮助解释特定请求失败的原因。
  
当然，您可以编写另一个客户端以供测试，但不必再进行！ [EWSEditor](http://ewseditor.codeplex.com/)是一个使用 EWS 托管 API 和 ews 的示例客户端。 您可以下载客户端（包括源代码），并使用它来尝试在您的应用程序中出现故障的相同请求。 
  
## <a name="examine-iis-logs"></a>检查 IIS 日志

如果您有权访问 Exchange 服务器，客户端访问服务器上的 Internet 信息服务（IIS）提供的日志记录功能可以提供有关故障的详细信息。 但请记住，IIS 日志将仅在收到 HTTP 错误时才有用。
  
IIS 提供了两种不同的日志记录方法： [iis 日志记录](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)和[失败请求跟踪](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)。 若要使用 IIS 日志，可以使用[Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)，其中包括许多内置的 EWS 查询。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_NextSteps"> </a>

现在，您已经了解了可用于进行故障排除的工具和资源，您可能需要帮助了解这些工具提供的信息。 以下是获取帮助的一些选项：
  
- [Msdn 上的 Exchange Server 开发论坛](https://social.msdn.microsoft.com/Forums/home?category=exchangeserver)—提出 Msdn Exchange Server 开发社区的问题。 
    
- [StackOverflow](http://stackoverflow.com/tags/ews) —提出有关 StackOverflow 社区的问题。 请务必使用 "ews" 标记你的帖子。 
    
- [Microsoft 支持](https://support.microsoft.com/ph/730/en-us)—请联系 microsoft 支持专家以获取帮助。 
    
## <a name="see-also"></a>另请参阅


另请参阅以下文章：
  
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [跟踪请求和响应以便解决 EWS 托管 API 应用程序的故障](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [检测对 EWS 和 REST 在 Exchange 中的客户端请求](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [Exchange 中的 EWS 限制](ews-throttling-in-exchange.md)
    
- [使用自动发现刷新配置信息](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [在 Exchange 中处理 EWS 中与通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中与同步相关的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中的与删除相关的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [在 IIS 中配置日志记录](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [使用 IIS 7 中的跟踪对失败请求进行故障排除](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [引入： Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Exchange 虚拟目录的默认设置](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)
    
下载以下内容：
  
- [Microsoft Network Monitor 3.4](https://www.microsoft.com/download/details.aspx?id=4865)（Microsoft 网络监视器 3.4）
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [Exchange Web Services 托管 API](https://go.microsoft.com/fwlink/?LinkID=255472)
    

