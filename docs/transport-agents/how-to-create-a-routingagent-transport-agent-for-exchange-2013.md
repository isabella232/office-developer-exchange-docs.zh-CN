---
title: 创建 Exchange 2013 RoutingAgent 传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: 了解如何创建自定义 RoutingAgent 传输代理与 Exchange 2013 一起使用。
ms.openlocfilehash: d07f68494acd26940a4837bbbfc7a0505114bd20
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753067"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="91f14-103">创建 Exchange 2013 RoutingAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="91f14-103">Create a RoutingAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="91f14-104">了解如何创建自定义 RoutingAgent 传输代理与 Exchange 2013 一起使用。</span><span class="sxs-lookup"><span data-stu-id="91f14-104">Find out how to create a custom RoutingAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="91f14-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="91f14-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="91f14-106">相关的代码段和示例应用程序：</span><span class="sxs-lookup"><span data-stu-id="91f14-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="91f14-107">Exchange 2013： 构建带宽日志记录传输代理</span><span class="sxs-lookup"><span data-stu-id="91f14-107">Exchange 2013: Build a bandwidth logging transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
<span data-ttu-id="91f14-108">[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)和[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类是旨在运行 Exchange Server 2013 邮箱服务器上的传输服务上的传输代理的基类。</span><span class="sxs-lookup"><span data-stu-id="91f14-108">The [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) and [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) classes are the base classes for transport agents that are designed to run on the transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="91f14-109">[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类提供了为其可能在您 RoutingAgent 传输代理中实现处理程序下表中列出的事件。</span><span class="sxs-lookup"><span data-stu-id="91f14-109">The [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) class provides the events listed in the following table for which you might implement handlers in your RoutingAgent transport agent.</span></span> 
  
<span data-ttu-id="91f14-110">**表 1。RoutingAgent 类事件**</span><span class="sxs-lookup"><span data-stu-id="91f14-110">**Table 1. RoutingAgent class events**</span></span>

|<span data-ttu-id="91f14-111">**事件**</span><span class="sxs-lookup"><span data-stu-id="91f14-111">**Event**</span></span>|<span data-ttu-id="91f14-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="91f14-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91f14-113">OnCategorizedMessage</span><span class="sxs-lookup"><span data-stu-id="91f14-113">OnCategorizedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |<span data-ttu-id="91f14-114">如果需要，发生后服务器执行内容转换。</span><span class="sxs-lookup"><span data-stu-id="91f14-114">Occurs after the server performs content conversion, if it is required.</span></span>  <br/> |
|[<span data-ttu-id="91f14-115">OnResolvedMessage</span><span class="sxs-lookup"><span data-stu-id="91f14-115">OnResolvedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |<span data-ttu-id="91f14-116">已解决所有收件人的邮件后，在由路由之前，发生此事件。</span><span class="sxs-lookup"><span data-stu-id="91f14-116">Occurs after all the recipients of the message have been resolved and before routing is determined.</span></span>  <br/> |
|[<span data-ttu-id="91f14-117">OnRoutedMessage</span><span class="sxs-lookup"><span data-stu-id="91f14-117">OnRoutedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |<span data-ttu-id="91f14-118">如果需要，发生后将邮件路由到下一个跃点服务器，并执行内容转换。</span><span class="sxs-lookup"><span data-stu-id="91f14-118">Occurs after the server routes the message to the next hop and performs content conversion, if required.</span></span> <span data-ttu-id="91f14-119">服务器可能使用更多资源处理比[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件中的每条消息，因为服务器将执行任何所需的内容转换和确定邮件路由中的下一个跃点之前，它在[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件处理程序中执行代码。</span><span class="sxs-lookup"><span data-stu-id="91f14-119">The server might use more resources to process each message in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event than the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event because the server will perform any necessary content conversion and determine the next hop in the route for the message before it executes the code in the [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) event handler.</span></span>  <br/> |
|[<span data-ttu-id="91f14-120">OnSubmittedMessage</span><span class="sxs-lookup"><span data-stu-id="91f14-120">OnSubmittedMessage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |<span data-ttu-id="91f14-121">邮件脱离提交队列后发生。</span><span class="sxs-lookup"><span data-stu-id="91f14-121">Occurs after the message is taken off the submit queue.</span></span> <span data-ttu-id="91f14-122">如果您 RoutingAgent 传输代理不需要内容转换、 已解析的收件人或传送的数据，请使用[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件。</span><span class="sxs-lookup"><span data-stu-id="91f14-122">Use the [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) event if your RoutingAgent transport agent does not require content conversion, resolved recipients, or routing data.</span></span>  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a><span data-ttu-id="91f14-123">创建自定义 RoutingAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="91f14-123">Creating a custom RoutingAgent transport agent</span></span>

<span data-ttu-id="91f14-124">以下过程介绍如何创建自定义 RoutingAgent 传输代理。</span><span class="sxs-lookup"><span data-stu-id="91f14-124">The following procedure describes how to create a custom RoutingAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="91f14-125">创建传输代理</span><span class="sxs-lookup"><span data-stu-id="91f14-125">To create the transport agent</span></span>

1. <span data-ttu-id="91f14-126">添加命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="91f14-126">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   <span data-ttu-id="91f14-127">Exchange 服务器上，您可以找到这些命名空间。</span><span class="sxs-lookup"><span data-stu-id="91f14-127">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="91f14-128">通过添加对这些命名空间的引用，您将有权[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)成员以及其他中使用的类[Exchange 2013： 生成带宽日志记录传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)示例。</span><span class="sxs-lookup"><span data-stu-id="91f14-128">By adding a reference to these namespaces, you will have access to the [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a bandwidth logging transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa) sample.</span></span> 
    
2. <span data-ttu-id="91f14-129">实现[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)类派生的类。</span><span class="sxs-lookup"><span data-stu-id="91f14-129">Implement the derived class for the [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span> 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   <span data-ttu-id="91f14-130">此代码将实例化派生的类，重写**CreateAgent**方法以创建新自定义代理的实例。</span><span class="sxs-lookup"><span data-stu-id="91f14-130">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="91f14-131">此外可以在此类，以执行自定义代码重写其他方法，例如**关闭**。</span><span class="sxs-lookup"><span data-stu-id="91f14-131">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> 
    
3. <span data-ttu-id="91f14-132">定义您的代理。</span><span class="sxs-lookup"><span data-stu-id="91f14-132">Define your agent.</span></span>
    
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

   <span data-ttu-id="91f14-133">定义您的代理类后，您可以将您添加自定义功能。</span><span class="sxs-lookup"><span data-stu-id="91f14-133">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="91f14-134">在此示例中的两个事件[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)和[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)重定向到自定义事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="91f14-134">In this example, the two events [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) and [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="91f14-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="91f14-135">See also</span></span>

- [<span data-ttu-id="91f14-136">传输代理 Exchange 2013 中的概念</span><span class="sxs-lookup"><span data-stu-id="91f14-136">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="91f14-137">Exchange 2013 的传输代理引用</span><span class="sxs-lookup"><span data-stu-id="91f14-137">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="91f14-138">RoutingAgentFactory</span><span class="sxs-lookup"><span data-stu-id="91f14-138">RoutingAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [<span data-ttu-id="91f14-139">RoutingAgent</span><span class="sxs-lookup"><span data-stu-id="91f14-139">RoutingAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

