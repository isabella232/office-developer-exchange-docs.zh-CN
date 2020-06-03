---
title: 检测对 EWS 和 REST 在 Exchange 中的客户端请求
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: 了解 EWS 和 REST 请求中的 HTTP 标头，以及可帮助您监视 Exchange 应用程序并对其进行故障排除的响应。
ms.openlocfilehash: 3a8ce889ec7a6b9e70ec25a95ac248902f48ca6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456302"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>检测对 EWS 和 REST 在 Exchange 中的客户端请求

了解 EWS 和 REST 请求中的 HTTP 标头，以及可帮助您监视 Exchange 应用程序并对其进行故障排除的响应。
  
是否曾对你发生这种情况？ 您的应用程序的用户报告了意外错误。 您想要调查，但不能再现。 用户的错误已消失，并且你已离开非常少可操作的数据。 令人沮丧，不是吗？ 让我们来看看如何主动准备此方案，并避免将来出现挫折。
  
## <a name="add-instrumentation-to-requests"></a>向请求添加检测

建议您向请求添加其他 HTTP 标头，以便于进行故障排除。 应将此信息记录保留在某个位置（例如，在日志文件中），以便稍后在需要时检索此信息。 这在检查网络流量时很有帮助，如果你联系 Microsoft 支持部门寻求帮助，也很有用。
  
**表1。用于故障排除的请求标头**

|**HTTP 标头（EWS）**|**EWS 托管 API 等效项**|**备注**|
|:-----|:-----|:-----|
|用户代理  <br/> |[ExchangeService。 UserAgent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |将此值设置为标识客户端应用程序的唯一值。<br/><br/> 如果你的应用程序发送的所有请求使用相同的值，Microsoft 可以在出现呼叫故障时帮助解决呼叫故障。  <br/> |
|客户端请求 id  <br/> |[ExchangeService。 ClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |对于您的应用程序发送的每个请求，请将此值设置为不同的唯一值。<br/><br/> 建议使用 GUID。 此唯一标识符用于在两个系统之间关联活动，以便在发生错误时进行关联。  <br/> |
|返回-客户端请求 id  <br/> |[ExchangeService。 ReturnClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |将此值设置为**true** ，以向 Exchange 服务器发出信号，告知 Exchange 服务器它应在相应的响应中返回客户端请求 id 的值。<br/><br/> 您可以使用此项在网络跟踪或 EWS 托管 API 跟踪中关联请求和响应。  <br/> |
|X-ClientStatistics  <br/> |[ExchangeService。 SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |用于向 Microsoft[报告 EWS 延迟](#bk_ReportLatency)（如果应用程序作为 Office 365 的一部分访问 exchange Online 或 exchange online）。  <br/> |
   
## <a name="log-information-from-responses"></a>记录响应中的信息

正如您的客户端可以向其发送的请求中添加额外的规范一样，Exchange 会将其他检测添加到 HTTP 头形式的响应中。 您的客户端应捕获此信息以与请求检测信息一起使用。
  
> [!NOTE]
> 如果使用 EWS 托管 API，则 HTTP 头没有直接等效项。 但是，可以通过[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx)属性访问所有 HTTP 响应头。 
  
**表2。HTTP 响应头**

|**HTTP 标头**|**说明**|
|:-----|:-----|
|请求 id  <br/> |与此响应对应的请求的服务器生成 ID。  <br/> |
|客户端请求 id  <br/> |请求中的客户端请求 id 标头的值。<br/><br/> 仅当请求包含的返回客户端请求 id 标头的值**为 true**时，才会出现此标头。  <br/> |
|X-FEServer  <br/> |处理请求的客户端访问服务器的 FQDN。  <br/> |
|X-TargetBEServer  <br/> |处理请求的邮箱服务器的 FQDN。  <br/> |
|X-X-diaginfo  <br/> |其他诊断信息，具体取决于请求。  <br/> |
|x-ms-诊断  <br/> | 只有在请求中使用 OAuth 身份验证时，此标头才适用。<br/><br/> 它包含显式错误代码，用于指定 OAuth 身份验证失败的原因。<br/><br/> 它采用以下格式：`errorId;reason="reason"error_type="error type"`<br/><br/> **原因**字段是可读的错误的说明。<br/><br/> **ErrorId**字段是一个整数，**错误 \_ 类型**字段是该整数的字符串表示形式，如下所示：<ul><li>2000000： \_ 签名无效</li><li>2000001： \_ 令牌无效</li><li>  2000002：令牌已 \_ 过期</li><li>2000003： \_ 资源无效</li><li>2000004： \_ 租户无效  </li><li>2000005： \_ 用户无效</li><li>2000006： \_ 客户端无效</li><li>2000007：内部 \_ 错误</li><li>2000008： \_ 授予无效</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>向 Microsoft 报告 EWS 延迟
<a name="bk_ReportLatency"> </a>

如果应用程序使用 EWS 托管 API 或 EWS 连接到 Exchange Online，则可以将 EWS 请求中的延迟直接报告给 Microsoft。 通过 ClientStatistics 请求标头传递信息。 如果您使用 EWS 托管 API，您只需将[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx)属性设置为**true**。 如果使用 EWS，则需要测量发出请求和接收响应之间的时间，然后使用以下格式将 ClientStatistics 头添加到应用程序发送的下一个 EWS 请求。
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
我们维护这些延迟的报告，并使用它们在 Exchange Online 中持续改进 EWS 服务。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_ReportLatency"> </a>

向应用程序添加了客户端规范后，如果出现问题，则会更好地进行准备。 如果发生这种情况，您可以使用检测数据对[应用程序进行故障排除](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)。
  
## <a name="see-also"></a>另请参阅

- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)
- [跟踪请求和响应以便解决 EWS 托管 API 应用程序的故障](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [工具和资源来解决 exchange 的 EWS 应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

