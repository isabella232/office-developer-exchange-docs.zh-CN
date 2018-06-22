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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752883"
---
# <a name="trace-requests-and-responses-to-troubleshoot-ews-managed-api-apps"></a><span data-ttu-id="454c7-103">跟踪请求和响应解决 EWS 托管 API 应用程序</span><span class="sxs-lookup"><span data-stu-id="454c7-103">Trace requests and responses to troubleshoot EWS Managed API apps</span></span>

<span data-ttu-id="454c7-104">找出如何跟踪 EWS 请求和响应解决 EWS 托管 API 应用程序中的错误。</span><span class="sxs-lookup"><span data-stu-id="454c7-104">Find out how to trace EWS requests and responses to troubleshoot errors in your EWS Managed API application.</span></span>
  
<span data-ttu-id="454c7-105">调试 web 基于服务的应用程序可能会变得比较困难，因为您可能无法访问远程计算机上执行处理的一部分。</span><span class="sxs-lookup"><span data-stu-id="454c7-105">Debugging a web service-based application can be difficult because part of the processing is performed on a remote computer that you might not have access to.</span></span> <span data-ttu-id="454c7-106">因为您无法在服务器上逐行执行代码，很有帮助若要查看的 XML 请求和确定应用程序的哪一部分导致了错误的客户端和服务器之间发送的响应。</span><span class="sxs-lookup"><span data-stu-id="454c7-106">Because you cannot step through the code on the server, it can be helpful to see the XML requests and responses that are sent between the client and the server to determine which part of the application is causing an error.</span></span> 
  
<span data-ttu-id="454c7-107">如果您使用 EWS，您已有权访问 XML 请求和响应;您可以将断开点放在您的代码以查看您的请求以便解决问题的服务器的响应。</span><span class="sxs-lookup"><span data-stu-id="454c7-107">If you are using EWS, you already have access to the XML request and response; you can put a break point in your code to review the server's response to your request in order to troubleshoot an issue.</span></span> <span data-ttu-id="454c7-108">如果您正在使用 EWS 托管 API，您无需直接访问 EWS 请求和响应。</span><span class="sxs-lookup"><span data-stu-id="454c7-108">If you're using the EWS Managed API, you don't have direct access to the EWS request and response.</span></span> <span data-ttu-id="454c7-109">但是，可以使用[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象上的跟踪方法以捕获 XML 请求和响应，并可以使用 XML 来确定为什么您的代码不起作用。</span><span class="sxs-lookup"><span data-stu-id="454c7-109">However, you can use tracing methods on the [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object to capture the XML request and response, and you can then use the XML to determine why your code is not working.</span></span> 

<span data-ttu-id="454c7-110">例如，如果您未正确设置属性，您可能会得到意外的响应，并可用于跟踪输出看以标识错误的 XML 请求和响应。</span><span class="sxs-lookup"><span data-stu-id="454c7-110">For example, if you did not set a property correctly, you might get an unexpected response, and you can use the trace output to look at the XML request and response to identify the error.</span></span> <span data-ttu-id="454c7-111">EWS 托管 API 的跟踪输出还有助于您手动构建创建 EWS 应用程序的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="454c7-111">The trace output from the EWS Managed API can also help you manually build the XML request to create your EWS application.</span></span> <span data-ttu-id="454c7-112">如果您使用 EWS，您可以使用 EWS 托管 API 创建一个小应用程序、 跟踪，并将 XML 请求信息可帮助您构建 EWS 请求。</span><span class="sxs-lookup"><span data-stu-id="454c7-112">If you are using EWS, you can create a small application by using EWS Managed API, trace it, and then use the XML request information to help you build your EWS request.</span></span> 
  
## <a name="enabling-tracing-on-the-exchangeservice-object"></a><span data-ttu-id="454c7-113">ExchangeService 对象上启用跟踪</span><span class="sxs-lookup"><span data-stu-id="454c7-113">Enabling tracing on the ExchangeService object</span></span>
<span data-ttu-id="454c7-114"><a name="bk_EnableTracing"> </a></span><span class="sxs-lookup"><span data-stu-id="454c7-114"></span></span>

<span data-ttu-id="454c7-115">若要启用跟踪，创建您的应用程序， [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和设置跟踪属性，如下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="454c7-115">To enable tracing, create an [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for your application, and set the tracing properties as shown in the following example.</span></span> 
  
```cs
ExchangeService service = new ExchangeService(ExchangeVersion.Exchange2010);
service.TraceListener = ITraceListenerInstance;
// Optional flags to indicate the requests and responses to trace.
service.TraceFlags = TraceFlags.EwsRequest | TraceFlags.EwsResponse
service.TraceEnabled = true;

```

<span data-ttu-id="454c7-116">将[TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx)属性设置为**true**后，跟踪标志相匹配的所有请求将都发送给指定的跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="454c7-116">After you set the [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true**, all requests that match the trace flags will be sent to the specified trace listener.</span></span> <span data-ttu-id="454c7-117">您可以指定单个跟踪标志，也可以通过将它们与逻辑**OR**组合指定多个跟踪标志。</span><span class="sxs-lookup"><span data-stu-id="454c7-117">You can specify a single trace flag, or you can specify multiple trace flags by combining them with a logical **OR**.</span></span> <span data-ttu-id="454c7-118">[TraceFlags 枚举](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx)可用于指定值 EWS 和自动发现请求和响应。</span><span class="sxs-lookup"><span data-stu-id="454c7-118">You can use the [TraceFlags enumeration](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.traceflags%28v=exchg.80%29.aspx) to specify values for EWS and for Autodiscover requests and responses.</span></span> 
  
## <a name="implementing-a-tracelistener-object"></a><span data-ttu-id="454c7-119">实现 TraceListener 对象</span><span class="sxs-lookup"><span data-stu-id="454c7-119">Implementing a TraceListener object</span></span>
<span data-ttu-id="454c7-120"><a name="bk_traceListener"> </a></span><span class="sxs-lookup"><span data-stu-id="454c7-120"></span></span>

<span data-ttu-id="454c7-121">您可以将[TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx)属性设置为**true**以输出的 XML 请求和响应对您的应用程序，如控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="454c7-121">You can set the [TraceEnabled](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.traceenabled%28v=exchg.80%29.aspx) property to **true** to output the XML requests and responses to your application, such as a console window.</span></span> <span data-ttu-id="454c7-122">如果您希望控制跟踪输出，并将其保存到文件，我们建议您实现[TraceListener 类](http://msdn.microsoft.com/en-us/library/system.diagnostics.tracelistener.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="454c7-122">If you want to control the trace output and save it to a file, we recommend that you implement a [TraceListener class](http://msdn.microsoft.com/en-us/library/system.diagnostics.tracelistener.aspx) object.</span></span> <span data-ttu-id="454c7-123">下面的代码示例演示一个简单的对象的实现[ITraceListener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx)接口和 XML 或文本文件中存储的跟踪的请求和响应。</span><span class="sxs-lookup"><span data-stu-id="454c7-123">The following code example shows a simple object that implements the [ITraceListener](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itracelistener%28v=exchg.80%29.aspx) interface and stores the traced requests and responses in XML or text files.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="454c7-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="454c7-124">See also</span></span>

- [<span data-ttu-id="454c7-125">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="454c7-125">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
- [<span data-ttu-id="454c7-126">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="454c7-126">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)    
- [<span data-ttu-id="454c7-127">EWS 托管 API 程序集参考</span><span class="sxs-lookup"><span data-stu-id="454c7-127">Reference the EWS Managed API assembly</span></span>](how-to-reference-the-ews-managed-api-assembly.md)    
- [<span data-ttu-id="454c7-128">使用 EWS 托管 API 与 EWS 通信</span><span class="sxs-lookup"><span data-stu-id="454c7-128">Communicate with EWS by using the EWS Managed API</span></span>](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)
    

