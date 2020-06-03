---
title: 跟踪对 EWS 托管 API 应用程序进行故障排除的请求和响应
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 186c1d1d-b8dc-4914-b3cd-6fada7ecd877
description: 了解如何跟踪 EWS 请求和响应以解决 EWS 托管 API 应用程序中的错误。
localization_priority: Priority
ms.openlocfilehash: dd225030d62a2e8211b7063ee78a59fd1a070263
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455854"
---
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a>跟踪对 EWS 托管 API 应用程序进行故障排除的请求和响应

了解如何跟踪 EWS 请求和响应以解决 EWS 托管 API 应用程序中的错误。
  
调试基于 web 服务的应用程序可能很困难，因为部分处理在您可能无法访问的远程计算机上执行。 由于无法在服务器上单步执行代码，因此查看在客户端和服务器之间发送的 XML 请求和响应可能会很有帮助，以确定导致错误的应用程序的哪个部分。 
  
如果您使用 EWS，则您已具有对 XML 请求和响应的访问权限;您可以在代码中放置一个断点，以查看服务器对您的请求的响应，以便对问题进行故障排除。 如果您使用的是 EWS 托管 API，则不能直接访问 EWS 请求和响应。 但是，可以对[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象使用跟踪方法来捕获 XML 请求和响应，然后可以使用 XML 确定代码不工作的原因。 

例如，如果您未正确设置属性，则可能会收到意外响应，您可以使用跟踪输出查看 XML 请求和响应以标识错误。 EWS 托管 API 中的跟踪输出还可帮助您手动生成用于创建 EWS 应用程序的 XML 请求。 如果您使用 EWS，则可以使用 EWS 托管 API 创建一个小型应用程序，对其进行跟踪，然后使用 XML 请求信息来帮助您构建 EWS 请求。 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a>启用对 ExchangeService 对象的跟踪
<a name="bk_EnableTracing"> </a>

若要启用跟踪，请为您的应用程序创建一个[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并设置跟踪属性，如下面的示例所示。 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

将[TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx)属性设置为**true**后，匹配跟踪标记的所有请求都将发送到指定的跟踪侦听器。 您可以指定单个跟踪标记，也可以通过将多个跟踪标记与逻辑**or**组合在一起指定。 您可以使用[TraceFlags 枚举](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx)指定 EWS 和自动发现请求和响应的值。 
  
## <a name="implementing-a-tracelistener-object"></a>实现 TraceListener 对象
<a name="bk_traceListener"> </a>

您可以将[TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx)属性设置为**true** ，以将 XML 请求和响应输出到应用程序，如控制台窗口。 如果要控制跟踪输出并将其保存到文件中，我们建议您实现[TraceListener 类](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx)对象。 下面的代码示例演示一个实现[ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx)接口的简单对象，并将跟踪请求和响应存储在 XML 文件或文本文件中。 
  
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

- [开始使用 Exchange 中的 Web 服务](start-using-web-services-in-exchange.md)
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)    
- [引用 EWS 托管 API 集](how-to-reference-the-ews-managed-api-assembly.md)    
- [使用 EWS 托管 API 与 EWS 进行通信](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

