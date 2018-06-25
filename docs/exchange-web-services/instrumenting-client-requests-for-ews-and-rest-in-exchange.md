---
title: 在 Exchange 检测 EWS 和 REST 的客户端请求
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: 了解 EWS 和 REST 请求和响应，可帮助您监视和解决 Exchange 应用程序中的 HTTP 标头。
ms.openlocfilehash: bcf362952c29956729c44397043a56bf3603d0af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752910"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>在 Exchange 检测 EWS 和 REST 的客户端请求

了解 EWS 和 REST 请求和响应，可帮助您监视和解决 Exchange 应用程序中的 HTTP 标头。
  
这曾经发生在您？ 您的应用程序的用户报告时发生的错误。 您想要调查，但不能重现问题。 对于用户，消失了错误和剩下非常少的可操作数据。 低效不是吗？ 让我们看一下如何主动做好准备对于此方案，并希望避免失望将来。
  
## <a name="add-instrumentation-to-requests"></a>添加对请求的规范

我们建议您将附加 HTTP 标头添加到您的请求，以便于进行故障。 以便可以在如果您需要更高版本检索，您应记录的某个位置 （例如，日志文件） 中此信息。 这是非常有用的时检查网络流量和也是非常有用，如果您与 Microsoft 支持部门联系以寻求帮助。
  
**表 1。请求标头的疑难解答**

|**HTTP 标头 (EWS)**|**EWS 托管 API 等效项**|**备注**|
|:-----|:-----|:-----|
|用户代理  <br/> |[ExchangeService.UserAgent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |设置为标识客户端应用程序的唯一值。<br/><br/> 使用相同的值的所有应用程序发送允许 Microsoft 帮助解决呼叫失败的请求，应该会在发生。  <br/> |
|客户端请求 id  <br/> |[ExchangeService.ClientRequestId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |此设置为您的应用程序发送的每个请求的不同唯一值。<br/><br/> 我们建议您使用的 GUID。 此唯一标识符旨在用于关联两个系统之间的活动的出现错误。  <br/> |
|返回客户端请求 id  <br/> |[ExchangeService.ReturnClientRequestId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |此设置为**true**以信号到 Exchange 服务器，它应在相应的响应中返回您客户端请求 id 的值。<br/><br/> 您可以使用此关联请求和响应网络跟踪或 EWS 托管 API 跟踪。  <br/> |
|X ClientStatistics  <br/> |[ExchangeService.SendClientLatencies](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |如果您的应用程序访问 Exchange Online 或 Exchange Online 作为 Office 365 的一部分，用于向 Microsoft[报告 EWS 延迟](#bk_ReportLatency)。  <br/> |
   
## <a name="log-information-from-responses"></a>来自响应的日志信息

就像您的客户端可以向其发送的请求添加其他检测，Exchange 会将其他检测向 HTTP 标头的窗体中的响应。 您的客户端应捕获转请求 instrumentation 信息以及此信息。
  
> [!NOTE]
> 如果您使用 EWS 托管 API，没有直接等效项的 HTTP 标头。 但是，可以通过[ExchangeService.HttpResponseHeaders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx)属性访问所有 HTTP 响应标头。 
  
**表 2。HTTP 响应标头**

|**HTTP 标头**|**说明**|
|:-----|:-----|
|请求 id  <br/> |对应于此响应该请求服务器生成的 ID。  <br/> |
|客户端请求 id  <br/> |请求中的客户端请求 id 标头的值。<br/><br/> 此标头才存在，如果请求包含返回客户端请求 id 标头，具有值为**true**。  <br/> |
|X-feserver  <br/> |处理请求的客户端访问服务器的 FQDN。  <br/> |
|X-targetbeserver  <br/> |处理请求的邮箱服务器的 FQDN。  <br/> |
|X-diaginfo  <br/> |附加诊断信息，具体取决于该请求。  <br/> |
|x-ms 诊断  <br/> | 此标头才适用如果请求中使用 OAuth 身份验证。<br/><br/> 它包含指定的 OAuth 身份验证失败的原因的显式错误代码。<br/><br/> 它采用以下格式：`errorId;reason="reason"error_type="error type"`<br/><br/> **原因**字段是可读错误的说明。<br/><br/> **ErrorId**字段是一个整数，和**错误\_类型**字段的字符串表示形式的整数，如下所示：<ul><li>2000000： 无效\_签名</li><li>2000001： 无效\_标记</li><li>  2000002： 令牌\_过期</li><li>2000003： 无效\_资源</li><li>2000004： 无效\_租户  </li><li>2000005： 无效\_用户</li><li>2000006： 无效\_客户端</li><li>2000007： 内部\_错误</li><li>2000008： 无效\_授予</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>向 Microsoft 报告 EWS 延迟
<a name="bk_ReportLatency"> </a>

如果您的应用程序使用 EWS 托管 API 或 EWS 连接到 Exchange Online，您可以直接向 Microsoft 报告 EWS 请求中的延迟。 通过 X ClientStatistics 请求标头传递信息。 如果您使用 EWS 托管 API，您只需执行的[ExchangeService.SendClientLatencies](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx)属性设置为**true**。 如果您使用 EWS，您需要测量之间发出请求和接收响应的时间，然后将 X ClientStatistics 标头添加到您的应用程序发送，使用以下格式的下一个 EWS 请求。
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
我们维护这些延迟的报告，并使用它们持续改进 Exchange Online 中的 EWS 服务。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_ReportLatency"> </a>

添加客户端检测到您的应用程序后，您更好地做好如果出现错误。 如果发生这种情况，您可以使用您检测数据到[解决您的应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)。
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
- [跟踪请求和响应解决 EWS 托管 API 应用程序](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [工具和资源来解决 exchange 的 EWS 应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

