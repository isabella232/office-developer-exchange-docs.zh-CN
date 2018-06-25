---
title: 跟踪请求和响应解决 EWS 托管 API 应用程序
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 186c1d1d-b8dc-4914-b3cd-6fada7ecd877
description: 找出如何跟踪 EWS 请求和响应解决 EWS 托管 API 应用程序中的错误。
ms.openlocfilehash: 056a1f84c4172b0404975d6fc35f9ecd7395ecdb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752883"
---
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a>跟踪请求和响应解决 EWS 托管 API 应用程序

找出如何跟踪 EWS 请求和响应解决 EWS 托管 API 应用程序中的错误。
  
调试 web 基于服务的应用程序可能会变得比较困难，因为您可能无法访问远程计算机上执行处理的一部分。 因为您无法在服务器上逐行执行代码，很有帮助若要查看的 XML 请求和确定应用程序的哪一部分导致了错误的客户端和服务器之间发送的响应。 
  
如果您使用 EWS，您已有权访问 XML 请求和响应;您可以将断开点放在您的代码以查看您的请求以便解决问题的服务器的响应。 如果您正在使用 EWS 托管 API，您无需直接访问 EWS 请求和响应。 但是，可以使用[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象上的跟踪方法以捕获 XML 请求和响应，并可以使用 XML 来确定为什么您的代码不起作用。 

例如，如果您未正确设置属性，您可能会得到意外的响应，并可用于跟踪输出看以标识错误的 XML 请求和响应。 EWS 托管 API 的跟踪输出还有助于您手动构建创建 EWS 应用程序的 XML 请求。 如果您使用 EWS，您可以使用 EWS 托管 API 创建一个小应用程序、 跟踪，并将 XML 请求信息可帮助您构建 EWS 请求。 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a>ExchangeService 对象上启用跟踪
<a name="bk_EnableTracing"> </a>

若要启用跟踪，创建您的应用程序， [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和设置跟踪属性，如下面的示例中所示。 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

将[TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx)属性设置为**true**后，跟踪标志相匹配的所有请求将都发送给指定的跟踪侦听器。 您可以指定单个跟踪标志，也可以通过将它们与逻辑**OR**组合指定多个跟踪标志。 [TraceFlags 枚举](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx)可用于指定值 EWS 和自动发现请求和响应。 
  
## <a name="implementing-a-tracelistener-object"></a>实现 TraceListener 对象
<a name="bk_traceListener"> </a>

您可以将[TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx)属性设置为**true**以输出的 XML 请求和响应对您的应用程序，如控制台窗口。 如果您希望控制跟踪输出，并将其保存到文件，我们建议您实现[TraceListener 类](http://msdn.microsoft.com/en-us/library/system.diagnostics.tracelistener.aspx)对象。 下面的代码示例演示一个简单的对象的实现[ITraceListener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx)接口和 XML 或文本文件中存储的跟踪的请求和响应。 
  
```cs
class TraceListener : ITraceListener
{
    #region ITraceListener Members
    public void Trace(string traceType, string traceMessage)
    {
      CreateXMLTextFile(traceType, traceMessage.ToString());
    }
    #endregion
    private void CreateXMLTextFile(string fileName, string traceContent)
    {
      // Create a new XML file for the trace information.
      try
      {
        // If the trace data is valid XML, create an XmlDocument object and save.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.Load(traceContent);
        xmlDoc.Save(fileName + ".xml");
      }
      catch
      {
        // If the trace data is not valid XML, save it as a text document.
        System.IO.File.WriteAllText(fileName + ".txt", traceContent);
      }
    }
}

```

## <a name="see-also"></a>另请参阅

- [Start using web services in Exchange](start-using-web-services-in-exchange.md)
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)    
- [EWS 托管 API 程序集参考](how-to-reference-the-ews-managed-api-assembly.md)    
- [使用 EWS 托管 API 与 EWS 通信](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

