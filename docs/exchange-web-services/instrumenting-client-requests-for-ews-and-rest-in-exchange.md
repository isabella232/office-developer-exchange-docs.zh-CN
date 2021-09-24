---
title: 在客户端中检测 EWS 和 REST 的Exchange
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: 了解 EWS 中的 HTTP 标头和 REST 请求和响应，这些请求和响应可帮助您监视您的 Exchange 应用程序。
ms.openlocfilehash: f32a164436a1f8ab06192e71a287f5092fe9a6c4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520988"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>在客户端中检测 EWS 和 REST 的Exchange

了解 EWS 中的 HTTP 标头和 REST 请求和响应，这些请求和响应可帮助您监视您的 Exchange 应用程序。
  
你是否曾经这样过？ 应用程序的用户报告意外错误。 你想要调查，但无法重现它。 用户的错误已消失，你只留下非常少的可操作数据。 很麻烦，不是吗？ 让我们看一下如何主动准备此方案，并希望在将来避免受挫。
  
## <a name="add-instrumentation-to-requests"></a>向请求添加检测

建议向请求添加其他 HTTP 标头，以方便进行故障排除。 您应将此信息的记录保留 (例如，在 日志文件) 中，以便以后可以在需要时进行检索。 这在检查网络流量时很有用，并且如果你联系 Microsoft 支持人员寻求帮助，这也会很有帮助。
  
**表 1.疑难解答的请求标头**

|**EWS (HTTP 标头)**|**EWS 托管 API 等效项**|**注意**|
|:-----|:-----|:-----|
|User-Agent  <br/> |[ExchangeService.UserAgent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |将此值设置为标识客户端应用程序的唯一值。<br/><br/> 如果对应用程序发送的所有请求使用相同的值，Microsoft 可帮助解决呼叫失败问题（如果发生）。  <br/> |
|client-request-id  <br/> |[ExchangeService.ClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |对于应用程序发送的每一个请求，将其设置为不同的唯一值。<br/><br/> 建议使用 GUID。 此唯一标识符用于在出现问题时关联两个系统之间的活动。  <br/> |
|return-client-request-id  <br/> |[ExchangeService.ReturnClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |将此值 **设置为 true** 以向 Exchange 服务器发出信号，指示它应在相应响应中返回客户端请求 id 的值。<br/><br/> 您可以使用它关联网络跟踪或 EWS 托管 API 跟踪中的请求和响应。  <br/> |
|X-ClientStatistics  <br/> |[ExchangeService.SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |用于向 Microsoft 报告[EWS](#bk_ReportLatency)延迟（如果应用程序正在访问 Exchange Online 或 Exchange Online 作为 Office 365 的一Office 365。  <br/> |
   
## <a name="log-information-from-responses"></a>记录来自响应的信息

正如客户端可以向它发送的请求添加其他检测一样，Exchange以 HTTP 标头的形式向响应添加其他检测。 客户端应捕获此信息，以与请求检测信息一起提供。
  
> [!NOTE]
> 如果使用 EWS 托管 API，则 HTTP 标头没有直接等效项。 但是，可以通过 [ExchangeService.HttpResponseHeaders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx) 属性访问所有 HTTP 响应头。 
  
**表 2.HTTP 响应标头**

|**HTTP 标头**|**说明**|
|:-----|:-----|
|request-id  <br/> |对应于此响应的请求的服务器生成的 ID。  <br/> |
|client-request-id  <br/> |请求中的 client-request-id 标头的值。<br/><br/> 只有当请求包含值为 true 的 return-client-request-id 标头时，此标头才 **存在**。  <br/> |
|X-FEServer  <br/> |处理请求的客户端访问服务器的 FQDN。  <br/> |
|X-TargetBEServer  <br/> |处理请求的邮箱服务器的 FQDN。  <br/> |
|X-DiagInfo  <br/> |其他诊断信息，具体取决于请求。  <br/> |
|x-ms-diagnostics  <br/> | 此标头仅在请求中使用的 OAuth 身份验证时适用。<br/><br/> 它包含一个显式错误代码，用于指定 OAuth 身份验证失败的原因。<br/><br/> 它采用以下格式： `errorId;reason="reason"error_type="error type"`<br/><br/> **原因** 字段是可读的错误描述。<br/><br/> **errorId** 字段是一个整数，错误 **类型 \_ 字段是** 该整数的字符串表示形式，如下所示：<ul><li>2000000：签名 \_ 无效</li><li>2000001：令牌 \_ 无效</li><li>  2000002： \_ 令牌已过期</li><li>2000003：资源 \_ 无效</li><li>2000004：租户 \_ 无效  </li><li>2000005：用户 \_ 无效</li><li>2000006：客户端 \_ 无效</li><li>2000007：内部 \_ 错误</li><li>2000008：授予 \_ 无效</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>向 Microsoft 报告 EWS 延迟
<a name="bk_ReportLatency"> </a>

如果您的应用程序使用 EWS 托管 API 或 EWS 连接到 Exchange Online，您可以直接向 Microsoft 报告 EWS 请求中的延迟。 信息通过 X-ClientStatistics 请求标头传递。 如果使用的是 EWS 托管 API，则只要将 [ExchangeService.SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx)属性设置为 **true。** 如果使用的是 EWS，则需要测量发出请求和接收响应之间的时间，然后采用以下格式将 X-ClientStatistics 标头添加到应用程序发送的下一个 EWS 请求中。
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
我们维护有关这些延迟的报告，并使用它们持续改进 Exchange Online。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_ReportLatency"> </a>

将客户端检测添加到应用程序后，如果出现问题，可以更好地做好准备。 如果发生这种情况，可以使用检测数据 [对应用程序进行疑难解答](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)。
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
- [跟踪请求和响应以便解决 EWS 托管 API 应用程序的故障](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [工具和资源来解决 exchange 的 EWS 应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

