---
title: 为 Exchange 2013 创建 RoutingAgent 传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: 了解如何创建自定义 RoutingAgent 传输代理以与 Exchange 2013 一起使用。
ms.openlocfilehash: 9acf30be0dd795098f757effaa34b2e72183b000
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463697"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="4b0dd-103">为 Exchange 2013 创建 RoutingAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="4b0dd-103">Create a RoutingAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="4b0dd-104">了解如何创建自定义 RoutingAgent 传输代理以与 Exchange 2013 一起使用。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-104">Find out how to create a custom RoutingAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="4b0dd-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b0dd-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="4b0dd-106">相关的代码段和示例应用程序：</span><span class="sxs-lookup"><span data-stu-id="4b0dd-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="4b0dd-107">Exchange 2013：构建带宽日志记录传输代理</span><span class="sxs-lookup"><span data-stu-id="4b0dd-107">Exchange 2013: Build a bandwidth logging transport agent</span></span>](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
<span data-ttu-id="4b0dd-108">[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)和[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类是用于传输代理的基类，这些类旨在在 Exchange Server 2013 邮箱服务器上的传输服务上运行。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-108">The [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) and [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) classes are the base classes for transport agents that are designed to run on the transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="4b0dd-109">[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类提供下表中列出的可在您的 RoutingAgent 传输代理中实现其处理程序的事件。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-109">The [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) class provides the events listed in the following table for which you might implement handlers in your RoutingAgent transport agent.</span></span> 
  
<span data-ttu-id="4b0dd-110">**表1。RoutingAgent 类事件**</span><span class="sxs-lookup"><span data-stu-id="4b0dd-110">**Table 1. RoutingAgent class events**</span></span>

|<span data-ttu-id="4b0dd-111">**Event**</span><span class="sxs-lookup"><span data-stu-id="4b0dd-111">**Event**</span></span>|<span data-ttu-id="4b0dd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b0dd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b0dd-113">OnCategorizedMessage</span><span class="sxs-lookup"><span data-stu-id="4b0dd-113">OnCategorizedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |<span data-ttu-id="4b0dd-114">在服务器执行内容转换（如果需要）时，发生此事件。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-114">Occurs after the server performs content conversion, if it is required.</span></span>  <br/> |
|[<span data-ttu-id="4b0dd-115">OnResolvedMessage</span><span class="sxs-lookup"><span data-stu-id="4b0dd-115">OnResolvedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |<span data-ttu-id="4b0dd-116">在解决邮件的所有收件人和确定路由之前发生。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-116">Occurs after all the recipients of the message have been resolved and before routing is determined.</span></span>  <br/> |
|[<span data-ttu-id="4b0dd-117">OnRoutedMessage</span><span class="sxs-lookup"><span data-stu-id="4b0dd-117">OnRoutedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |<span data-ttu-id="4b0dd-118">在服务器将邮件路由到下一个跃点并执行内容转换（如果需要）之后，发生此事件。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-118">Occurs after the server routes the message to the next hop and performs content conversion, if required.</span></span> <span data-ttu-id="4b0dd-119">服务器可能会使用更多资源处理[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件中的每个邮件，而不是[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件，因为在执行[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件处理程序中的代码之前，服务器将执行任何必要的内容转换并确定邮件路由中的下一个跃点。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-119">The server might use more resources to process each message in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event than the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event because the server will perform any necessary content conversion and determine the next hop in the route for the message before it executes the code in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event handler.</span></span>  <br/> |
|[<span data-ttu-id="4b0dd-120">OnSubmittedMessage</span><span class="sxs-lookup"><span data-stu-id="4b0dd-120">OnSubmittedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |<span data-ttu-id="4b0dd-121">在邮件离开提交队列之后发生。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-121">Occurs after the message is taken off the submit queue.</span></span> <span data-ttu-id="4b0dd-122">如果 RoutingAgent 传输代理不需要内容转换、解析的收件人或路由数据，则使用[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-122">Use the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event if your RoutingAgent transport agent does not require content conversion, resolved recipients, or routing data.</span></span>  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a><span data-ttu-id="4b0dd-123">创建自定义 RoutingAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="4b0dd-123">Creating a custom RoutingAgent transport agent</span></span>

<span data-ttu-id="4b0dd-124">下面的过程介绍如何创建自定义 RoutingAgent 传输代理。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-124">The following procedure describes how to create a custom RoutingAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="4b0dd-125">创建传输代理</span><span class="sxs-lookup"><span data-stu-id="4b0dd-125">To create the transport agent</span></span>

1. <span data-ttu-id="4b0dd-126">添加对命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-126">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   <span data-ttu-id="4b0dd-127">您可以在您的 Exchange 服务器上找到这些命名空间。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-127">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="4b0dd-128">通过添加对这些命名空间的引用，您将有权访问[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)成员以及 Exchange 2013 中使用的其他类[：构建带宽日志记录传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)示例。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-128">By adding a reference to these namespaces, you will have access to the [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a bandwidth logging transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) sample.</span></span> 
    
2. <span data-ttu-id="4b0dd-129">为[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)类实现派生类。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-129">Implement the derived class for the [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span> 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   <span data-ttu-id="4b0dd-130">此代码将实例化派生类并重写**CreateAgent**方法，以创建新的自定义代理的实例。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-130">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="4b0dd-131">此外，还可以在此类中重写其他方法（如**Close**），以执行自定义代码。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-131">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> 
    
3. <span data-ttu-id="4b0dd-132">定义代理。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-132">Define your agent.</span></span>
    
   ```cs
      public class BandwidthLogger : RoutingAgent
      {
          // Your custom code goes here
          public BandwidthLogger(SmtpServer server)
          {
              Debug.WriteLine(logPrefix + "Agent constructor");
              this.server = server;
              this.OnSubmittedMessage += SubmittedMessage;
              this.OnRoutedMessage += RoutedMessage;
          }
      }
  
   ```

   <span data-ttu-id="4b0dd-133">在定义代理类之后，可以添加自定义功能。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-133">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="4b0dd-134">在此示例中，将两个事件[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)和[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)重定向到自定义事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="4b0dd-134">In this example, the two events [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) and [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4b0dd-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b0dd-135">See also</span></span>

- [<span data-ttu-id="4b0dd-136">Exchange 2013 中的传输代理概念</span><span class="sxs-lookup"><span data-stu-id="4b0dd-136">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="4b0dd-137">Exchange 2013 的传输代理参考</span><span class="sxs-lookup"><span data-stu-id="4b0dd-137">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="4b0dd-138">RoutingAgentFactory</span><span class="sxs-lookup"><span data-stu-id="4b0dd-138">RoutingAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [<span data-ttu-id="4b0dd-139">RoutingAgent</span><span class="sxs-lookup"><span data-stu-id="4b0dd-139">RoutingAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

