---
title: 为 Exchange 2013 创建 SmtpReceiveAgent 传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: 了解如何创建自定义 SmtpReceiveAgent 传输代理以与 Exchange 2013 一起使用。
ms.openlocfilehash: 5ba021d02849ffc7e125029f0fd18ebf14c3f8da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459137"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="4fe23-103">为 Exchange 2013 创建 SmtpReceiveAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="4fe23-103">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="4fe23-104">了解如何创建自定义 SmtpReceiveAgent 传输代理以与 Exchange 2013 一起使用。</span><span class="sxs-lookup"><span data-stu-id="4fe23-104">Find out how to create a custom SmtpReceiveAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="4fe23-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="4fe23-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="4fe23-106">相关的代码段和示例应用程序：</span><span class="sxs-lookup"><span data-stu-id="4fe23-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="4fe23-107">Exchange 2013：生成正文转换传输代理</span><span class="sxs-lookup"><span data-stu-id="4fe23-107">Exchange 2013: Build a body conversion transport agent</span></span>](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
<span data-ttu-id="4fe23-108">[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类使您能够在客户端访问服务器或邮箱服务器上的传输服务上扩展前端传输服务的行为。</span><span class="sxs-lookup"><span data-stu-id="4fe23-108">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes enable you to extend the behavior of the Front End Transport service on a Client Access Server or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="4fe23-109">可以使用这些类来实现传输代理，这些代理旨在在邮件进入您的组织时对其做出响应。</span><span class="sxs-lookup"><span data-stu-id="4fe23-109">You can use these classes to implement transport agents that are designed to respond to messages as they come into your organization.</span></span> 
  
<span data-ttu-id="4fe23-110">[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类包括下表中列出的事件。</span><span class="sxs-lookup"><span data-stu-id="4fe23-110">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes include the events listed in the following table.</span></span> 
  
<span data-ttu-id="4fe23-111">**表1。SmtpReceiveAgent 类事件**</span><span class="sxs-lookup"><span data-stu-id="4fe23-111">**Table 1. SmtpReceiveAgent class events**</span></span>

|<span data-ttu-id="4fe23-112">**Event**</span><span class="sxs-lookup"><span data-stu-id="4fe23-112">**Event**</span></span>|<span data-ttu-id="4fe23-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="4fe23-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fe23-114">OnAuthCommand</span><span class="sxs-lookup"><span data-stu-id="4fe23-114">OnAuthCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |<span data-ttu-id="4fe23-115">当代理需要仅在 SMTP **AUTH**命令中提供的信息（如接受或拒绝基于所使用的身份验证方法的发送邮件的尝试的代理）时使用。</span><span class="sxs-lookup"><span data-stu-id="4fe23-115">Use when your agent requires information that is provided only in the SMTP **AUTH** command, such as an agent that accepts or rejects attempts to deliver a message based on the type of authentication method used.</span></span>  <br/> |
|[<span data-ttu-id="4fe23-116">OnConnect</span><span class="sxs-lookup"><span data-stu-id="4fe23-116">OnConnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |<span data-ttu-id="4fe23-117">当您的代理需要仅当通过 SMTP 将连接打开到前端传输服务时提供的信息，例如，基于远程 SMTP 服务器的地址或域执行操作的代理时使用。</span><span class="sxs-lookup"><span data-stu-id="4fe23-117">Use when your agent requires information that is provided only when a connection is opened via SMTP to the Front End Transport service, such as an agent that performs an action based on the address or domain of the remote SMTP server.</span></span>  <br/> |
|[<span data-ttu-id="4fe23-118">OnDataCommand</span><span class="sxs-lookup"><span data-stu-id="4fe23-118">OnDataCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |<span data-ttu-id="4fe23-119">当您的代理需要 SMTP**数据**命令中提供的信息时，请使用此事件。</span><span class="sxs-lookup"><span data-stu-id="4fe23-119">Use this event when your agent requires information that is provided in the SMTP **DATA** command.</span></span>  <br/> |
|[<span data-ttu-id="4fe23-120">OnDisconnect</span><span class="sxs-lookup"><span data-stu-id="4fe23-120">OnDisconnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |<span data-ttu-id="4fe23-121">如果代理需要在断开连接时可用的信息（如当前日期和时间），以便执行时间计算，请使用。</span><span class="sxs-lookup"><span data-stu-id="4fe23-121">Use when your agent requires information that is available at the time of disconnection, such as the current date and time, in order to perform time calculations.</span></span>  <br/> |
|[<span data-ttu-id="4fe23-122">OnEhloCommand</span><span class="sxs-lookup"><span data-stu-id="4fe23-122">OnEhloCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |<span data-ttu-id="4fe23-123">当代理需要 SMTP **EHLO**命令中提供的信息时使用;例如，如果您的代理根据**EHLO**命令中提供的标识接受或拒绝邮件。</span><span class="sxs-lookup"><span data-stu-id="4fe23-123">Use when your agent requires information that is provided in the SMTP **EHLO** command; for example, if your agent accepts or rejects messages based on the identity provided in the **EHLO** command.</span></span>  <br/> |
|[<span data-ttu-id="4fe23-124">OnEndOfAuthentication</span><span class="sxs-lookup"><span data-stu-id="4fe23-124">OnEndOfAuthentication</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |<span data-ttu-id="4fe23-125">当您的代理需要在远程服务器完成身份验证过程后可用的信息时，请使用。例如，对于基于远程 SMTP 服务器或客户端提供的身份验证信息对邮件执行操作的代理。</span><span class="sxs-lookup"><span data-stu-id="4fe23-125">Use when your agent requires information that is available after the remote server completes the authentication process; for example, for an agent that performs an action on a message based on the authentication information provided by the remote SMTP server or client.</span></span>  <br/> |
|[<span data-ttu-id="4fe23-126">OnEndOfData</span><span class="sxs-lookup"><span data-stu-id="4fe23-126">OnEndOfData</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |<span data-ttu-id="4fe23-127">当代理必须基于邮件中提供的数据执行操作时使用。</span><span class="sxs-lookup"><span data-stu-id="4fe23-127">Use when your agent must perform an action based on data that is available in the message.</span></span> <span data-ttu-id="4fe23-128">在前端传输服务上不会触发此事件。</span><span class="sxs-lookup"><span data-stu-id="4fe23-128">This event will not fire on the Front End Transport service.</span></span> <span data-ttu-id="4fe23-129">如果您的传输代理必须使用此事件，则必须将其安装在邮箱服务器上。</span><span class="sxs-lookup"><span data-stu-id="4fe23-129">If your transport agent has to use this event, you have to install it on a Mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="4fe23-130">OnEndOfHeaders</span><span class="sxs-lookup"><span data-stu-id="4fe23-130">OnEndOfHeaders</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |<span data-ttu-id="4fe23-131">在代理必须基于提交的邮件的邮件头中提供的信息执行操作时使用。</span><span class="sxs-lookup"><span data-stu-id="4fe23-131">Use when your agent must perform an action based on information that is available in the headers of the submitted message.</span></span>  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a><span data-ttu-id="4fe23-132">创建自定义 SmtpReceiveAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="4fe23-132">Creating a custom SmtpReceiveAgent transport agent</span></span>

<span data-ttu-id="4fe23-133">下面的过程介绍如何创建自定义 SmtpReceiveAgent 传输代理。</span><span class="sxs-lookup"><span data-stu-id="4fe23-133">The following procedure describes how to create a custom SmtpReceiveAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="4fe23-134">创建传输代理</span><span class="sxs-lookup"><span data-stu-id="4fe23-134">To create the transport agent</span></span>

1. <span data-ttu-id="4fe23-135">添加对命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="4fe23-135">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   <span data-ttu-id="4fe23-136">您可以在 Exchange 2013 服务器上找到这些命名空间。</span><span class="sxs-lookup"><span data-stu-id="4fe23-136">You can find these namespaces on your Exchange 2013 server.</span></span> <span data-ttu-id="4fe23-137">当您添加对这些命名空间的引用时，您将有权访问[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)成员以及在 Exchange 2013 中使用的其他类[：构建正文转换传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)示例。</span><span class="sxs-lookup"><span data-stu-id="4fe23-137">When you add a reference to these namespaces, you will have access to the [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a body conversion transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) sample.</span></span> 
    
2. <span data-ttu-id="4fe23-138">为[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)类实现派生类。</span><span class="sxs-lookup"><span data-stu-id="4fe23-138">Implement the derived class for the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) class.</span></span> 
    
   ```cs
      public class BodyConversionFactory : SmtpReceiveAgentFactory
      {
          /// <summary>
          /// Create a new BodyConversion
          /// </summary>
          /// <param name="server">Exchange server</param>
          /// <returns>A new BodyConversion</returns>
          public override SmtpReceiveAgent CreateAgent(SmtpServer server)
          {
              return new BodyConversion();
          }
      }
  
   ```

   <span data-ttu-id="4fe23-139">此代码将实例化派生类并重写**CreateAgent**方法，以创建新的自定义代理的实例。</span><span class="sxs-lookup"><span data-stu-id="4fe23-139">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> 
    
3. <span data-ttu-id="4fe23-140">定义代理。</span><span class="sxs-lookup"><span data-stu-id="4fe23-140">Define your agent.</span></span>
    
   ```cs
     public class BodyConversion : SmtpReceiveAgent
      {
          // Your custom code goes here
          /// <summary>
          /// The constructor registers an end of data event handler.
          /// </summary>
          public BodyConversion()
          {
              Debug.WriteLine("[BodyConversion] Agent constructor");
              this.OnEndOfData += new EndOfDataEventHandler(this.OnEndOfDataHandler);
          }
      }
  
   ```

   <span data-ttu-id="4fe23-141">在定义代理类之后，可以添加自定义功能。</span><span class="sxs-lookup"><span data-stu-id="4fe23-141">After you define your agent class, you can add your custom functionality.</span></span> <span data-ttu-id="4fe23-142">在此示例中， [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx)事件被重定向到自定义事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="4fe23-142">In this example, the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) event is redirected to your custom event handler.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4fe23-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4fe23-143">See also</span></span>

- [<span data-ttu-id="4fe23-144">Exchange 2013 中的传输代理概念</span><span class="sxs-lookup"><span data-stu-id="4fe23-144">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="4fe23-145">Exchange 2013 的传输代理参考</span><span class="sxs-lookup"><span data-stu-id="4fe23-145">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="4fe23-146">SmtpReceiveAgentFactory</span><span class="sxs-lookup"><span data-stu-id="4fe23-146">SmtpReceiveAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [<span data-ttu-id="4fe23-147">SmtpReceiveAgent</span><span class="sxs-lookup"><span data-stu-id="4fe23-147">SmtpReceiveAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

