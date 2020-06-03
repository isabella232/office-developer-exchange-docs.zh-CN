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
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a><span data-ttu-id="cff79-103">跟踪对 EWS 托管 API 应用程序进行故障排除的请求和响应</span><span class="sxs-lookup"><span data-stu-id="cff79-103">Trace requests and responses to troubleshoot EWS Managed API apps</span></span>

<span data-ttu-id="cff79-104">了解如何跟踪 EWS 请求和响应以解决 EWS 托管 API 应用程序中的错误。</span><span class="sxs-lookup"><span data-stu-id="cff79-104">Find out how to trace EWS requests and responses to troubleshoot errors in your EWS Managed API application.</span></span>
  
<span data-ttu-id="cff79-105">调试基于 web 服务的应用程序可能很困难，因为部分处理在您可能无法访问的远程计算机上执行。</span><span class="sxs-lookup"><span data-stu-id="cff79-105">Debugging a web service-based application can be difficult because part of the processing is performed on a remote computer that you might not have access to.</span></span> <span data-ttu-id="cff79-106">由于无法在服务器上单步执行代码，因此查看在客户端和服务器之间发送的 XML 请求和响应可能会很有帮助，以确定导致错误的应用程序的哪个部分。</span><span class="sxs-lookup"><span data-stu-id="cff79-106">Because you cannot step through the code on the server, it can be helpful to see the XML requests and responses that are sent between the client and the server to determine which part of the application is causing an error.</span></span> 
  
<span data-ttu-id="cff79-107">如果您使用 EWS，则您已具有对 XML 请求和响应的访问权限;您可以在代码中放置一个断点，以查看服务器对您的请求的响应，以便对问题进行故障排除。</span><span class="sxs-lookup"><span data-stu-id="cff79-107">If you are using EWS, you already have access to the XML request and response; you can put a break point in your code to review the server's response to your request in order to troubleshoot an issue.</span></span> <span data-ttu-id="cff79-108">如果您使用的是 EWS 托管 API，则不能直接访问 EWS 请求和响应。</span><span class="sxs-lookup"><span data-stu-id="cff79-108">If you're using the EWS Managed API, you don't have direct access to the EWS request and response.</span></span> <span data-ttu-id="cff79-109">但是，可以对[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象使用跟踪方法来捕获 XML 请求和响应，然后可以使用 XML 确定代码不工作的原因。</span><span class="sxs-lookup"><span data-stu-id="cff79-109">However, you can use tracing methods on the [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object to capture the XML request and response, and you can then use the XML to determine why your code is not working.</span></span> 

<span data-ttu-id="cff79-110">例如，如果您未正确设置属性，则可能会收到意外响应，您可以使用跟踪输出查看 XML 请求和响应以标识错误。</span><span class="sxs-lookup"><span data-stu-id="cff79-110">For example, if you did not set a property correctly, you might get an unexpected response, and you can use the trace output to look at the XML request and response to identify the error.</span></span> <span data-ttu-id="cff79-111">EWS 托管 API 中的跟踪输出还可帮助您手动生成用于创建 EWS 应用程序的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="cff79-111">The trace output from the EWS Managed API can also help you manually build the XML request to create your EWS application.</span></span> <span data-ttu-id="cff79-112">如果您使用 EWS，则可以使用 EWS 托管 API 创建一个小型应用程序，对其进行跟踪，然后使用 XML 请求信息来帮助您构建 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="cff79-112">If you are using EWS, you can create a small application by using EWS Managed API, trace it, and then use the XML request information to help you build your EWS request.</span></span> 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a><span data-ttu-id="cff79-113">启用对 ExchangeService 对象的跟踪</span><span class="sxs-lookup"><span data-stu-id="cff79-113">Enabling tracing on the ExchangeService object</span></span>
<span data-ttu-id="cff79-114"><a name="bk_EnableTracing"> </a></span><span class="sxs-lookup"><span data-stu-id="cff79-114"><a name="bk_EnableTracing"> </a></span></span>

<span data-ttu-id="cff79-115">若要启用跟踪，请为您的应用程序创建一个[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并设置跟踪属性，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="cff79-115">To enable tracing, create an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for your application, and set the tracing properties as shown in the following example.</span></span> 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

<span data-ttu-id="cff79-116">将[TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx)属性设置为**true**后，匹配跟踪标记的所有请求都将发送到指定的跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="cff79-116">After you set the [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true**, all requests that match the trace flags will be sent to the specified trace listener.</span></span> <span data-ttu-id="cff79-117">您可以指定单个跟踪标记，也可以通过将多个跟踪标记与逻辑**or**组合在一起指定。</span><span class="sxs-lookup"><span data-stu-id="cff79-117">You can specify a single trace flag, or you can specify multiple trace flags by combining them with a logical **OR**.</span></span> <span data-ttu-id="cff79-118">您可以使用[TraceFlags 枚举](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx)指定 EWS 和自动发现请求和响应的值。</span><span class="sxs-lookup"><span data-stu-id="cff79-118">You can use the [TraceFlags enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) to specify values for EWS and for Autodiscover requests and responses.</span></span> 
  
## <a name="implementing-a-tracelistener-object"></a><span data-ttu-id="cff79-119">实现 TraceListener 对象</span><span class="sxs-lookup"><span data-stu-id="cff79-119">Implementing a TraceListener object</span></span>
<span data-ttu-id="cff79-120"><a name="bk_traceListener"> </a></span><span class="sxs-lookup"><span data-stu-id="cff79-120"><a name="bk_traceListener"> </a></span></span>

<span data-ttu-id="cff79-121">您可以将[TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx)属性设置为**true** ，以将 XML 请求和响应输出到应用程序，如控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="cff79-121">You can set the [TraceEnabled](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true** to output the XML requests and responses to your application, such as a console window.</span></span> <span data-ttu-id="cff79-122">如果要控制跟踪输出并将其保存到文件中，我们建议您实现[TraceListener 类](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="cff79-122">If you want to control the trace output and save it to a file, we recommend that you implement a [TraceListener class](https://msdn.microsoft.com/library/system.diagnostics.tracelistener.aspx) object.</span></span> <span data-ttu-id="cff79-123">下面的代码示例演示一个实现[ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx)接口的简单对象，并将跟踪请求和响应存储在 XML 文件或文本文件中。</span><span class="sxs-lookup"><span data-stu-id="cff79-123">The following code example shows a simple object that implements the [ITraceListener](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) interface and stores the traced requests and responses in XML or text files.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="cff79-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cff79-124">See also</span></span>

- [<span data-ttu-id="cff79-125">开始使用 Exchange 中的 Web 服务</span><span class="sxs-lookup"><span data-stu-id="cff79-125">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="cff79-126">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="cff79-126">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)    
- [<span data-ttu-id="cff79-127">引用 EWS 托管 API 集</span><span class="sxs-lookup"><span data-stu-id="cff79-127">Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)    
- [<span data-ttu-id="cff79-128">使用 EWS 托管 API 与 EWS 进行通信</span><span class="sxs-lookup"><span data-stu-id="cff79-128">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

