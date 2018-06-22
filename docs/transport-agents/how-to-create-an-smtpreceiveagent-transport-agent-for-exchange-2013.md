---
title: 创建 Exchange 2013 SmtpReceiveAgent 传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: 了解如何创建自定义 SmtpReceiveAgent 传输代理与 Exchange 2013 一起使用。
ms.openlocfilehash: a74d5baae6334c5e17acb6335206964b48f320e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753183"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="a3f26-103">创建 Exchange 2013 SmtpReceiveAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="a3f26-103">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="a3f26-104">了解如何创建自定义 SmtpReceiveAgent 传输代理与 Exchange 2013 一起使用。</span><span class="sxs-lookup"><span data-stu-id="a3f26-104">Find out how to create a custom SmtpReceiveAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="a3f26-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3f26-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="a3f26-106">相关的代码段和示例应用程序：</span><span class="sxs-lookup"><span data-stu-id="a3f26-106">Related code snippets and sample apps:</span></span>

- [<span data-ttu-id="a3f26-107">Exchange 2013： 构建正文转换传输代理</span><span class="sxs-lookup"><span data-stu-id="a3f26-107">Exchange 2013: Build a body conversion transport agent</span></span>](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
<span data-ttu-id="a3f26-108">[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类使您能够扩展客户端访问服务器上的前端传输服务或邮箱服务器上的传输服务的行为。</span><span class="sxs-lookup"><span data-stu-id="a3f26-108">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes enable you to extend the behavior of the Front End Transport service on a Client Access Server or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="a3f26-109">您可以使用这些类实现旨在响应消息，如它们进入组织的传输代理。</span><span class="sxs-lookup"><span data-stu-id="a3f26-109">You can use these classes to implement transport agents that are designed to respond to messages as they come into your organization.</span></span> 
  
<span data-ttu-id="a3f26-110">[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类包含下表中列出的事件。</span><span class="sxs-lookup"><span data-stu-id="a3f26-110">The [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes include the events listed in the following table.</span></span> 
  
<span data-ttu-id="a3f26-111">**表 1。SmtpReceiveAgent 类事件**</span><span class="sxs-lookup"><span data-stu-id="a3f26-111">**Table 1. SmtpReceiveAgent class events**</span></span>

|<span data-ttu-id="a3f26-112">**事件**</span><span class="sxs-lookup"><span data-stu-id="a3f26-112">**Event**</span></span>|<span data-ttu-id="a3f26-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="a3f26-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a3f26-114">OnAuthCommand</span><span class="sxs-lookup"><span data-stu-id="a3f26-114">OnAuthCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |<span data-ttu-id="a3f26-115">当您的代理需要仅在 SMTP**身份验证**命令，如代理接受或拒绝中提供的信息的使用尝试传递邮件基于使用的身份验证方法的类型。</span><span class="sxs-lookup"><span data-stu-id="a3f26-115">Use when your agent requires information that is provided only in the SMTP **AUTH** command, such as an agent that accepts or rejects attempts to deliver a message based on the type of authentication method used.</span></span>  <br/> |
|[<span data-ttu-id="a3f26-116">OnConnect</span><span class="sxs-lookup"><span data-stu-id="a3f26-116">OnConnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |<span data-ttu-id="a3f26-117">当您的代理需要仅当连接到前端传输服务，如代理执行基于地址或域的远程 SMTP 服务器的操作，通过 SMTP 打开时提供的信息的使用。</span><span class="sxs-lookup"><span data-stu-id="a3f26-117">Use when your agent requires information that is provided only when a connection is opened via SMTP to the Front End Transport service, such as an agent that performs an action based on the address or domain of the remote SMTP server.</span></span>  <br/> |
|[<span data-ttu-id="a3f26-118">OnDataCommand</span><span class="sxs-lookup"><span data-stu-id="a3f26-118">OnDataCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |<span data-ttu-id="a3f26-119">使用此事件时您代理需要 SMTP**数据**命令中提供的信息。</span><span class="sxs-lookup"><span data-stu-id="a3f26-119">Use this event when your agent requires information that is provided in the SMTP **DATA** command.</span></span>  <br/> |
|[<span data-ttu-id="a3f26-120">OnDisconnect</span><span class="sxs-lookup"><span data-stu-id="a3f26-120">OnDisconnect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |<span data-ttu-id="a3f26-121">当您的代理需要断开连接，才能执行时间计算当前日期和时间，如时可用的信息的使用。</span><span class="sxs-lookup"><span data-stu-id="a3f26-121">Use when your agent requires information that is available at the time of disconnection, such as the current date and time, in order to perform time calculations.</span></span>  <br/> |
|[<span data-ttu-id="a3f26-122">OnEhloCommand</span><span class="sxs-lookup"><span data-stu-id="a3f26-122">OnEhloCommand</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |<span data-ttu-id="a3f26-123">当您的代理需要 SMTP **EHLO**命令; 中提供的信息的使用例如，如果您的代理接受或拒绝消息基于**EHLO**命令中提供的标识。</span><span class="sxs-lookup"><span data-stu-id="a3f26-123">Use when your agent requires information that is provided in the SMTP **EHLO** command; for example, if your agent accepts or rejects messages based on the identity provided in the **EHLO** command.</span></span>  <br/> |
|[<span data-ttu-id="a3f26-124">OnEndOfAuthentication</span><span class="sxs-lookup"><span data-stu-id="a3f26-124">OnEndOfAuthentication</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |<span data-ttu-id="a3f26-125">当您的代理需要远程服务器完成身份验证过程中; 后提供信息的使用例如，对于基于由远程 SMTP 服务器或客户端提供的身份验证信息一条消息执行操作的代理。</span><span class="sxs-lookup"><span data-stu-id="a3f26-125">Use when your agent requires information that is available after the remote server completes the authentication process; for example, for an agent that performs an action on a message based on the authentication information provided by the remote SMTP server or client.</span></span>  <br/> |
|[<span data-ttu-id="a3f26-126">OnEndOfData</span><span class="sxs-lookup"><span data-stu-id="a3f26-126">OnEndOfData</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |<span data-ttu-id="a3f26-127">您的代理必须执行基于数据，可在邮件中操作时使用。</span><span class="sxs-lookup"><span data-stu-id="a3f26-127">Use when your agent must perform an action based on data that is available in the message.</span></span> <span data-ttu-id="a3f26-128">在前端传输服务将不触发此事件。</span><span class="sxs-lookup"><span data-stu-id="a3f26-128">This event will not fire on the Front End Transport service.</span></span> <span data-ttu-id="a3f26-129">如果您传输代理必须使用此事件，必须在邮箱服务器上安装它。</span><span class="sxs-lookup"><span data-stu-id="a3f26-129">If your transport agent has to use this event, you have to install it on a Mailbox server.</span></span>  <br/> |
|[<span data-ttu-id="a3f26-130">OnEndOfHeaders</span><span class="sxs-lookup"><span data-stu-id="a3f26-130">OnEndOfHeaders</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |<span data-ttu-id="a3f26-131">您的代理必须根据执行操作的提交的邮件头中可用的信息时使用。</span><span class="sxs-lookup"><span data-stu-id="a3f26-131">Use when your agent must perform an action based on information that is available in the headers of the submitted message.</span></span>  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a><span data-ttu-id="a3f26-132">创建自定义 SmtpReceiveAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="a3f26-132">Creating a custom SmtpReceiveAgent transport agent</span></span>

<span data-ttu-id="a3f26-133">以下过程介绍如何创建自定义 SmtpReceiveAgent 传输代理。</span><span class="sxs-lookup"><span data-stu-id="a3f26-133">The following procedure describes how to create a custom SmtpReceiveAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="a3f26-134">创建传输代理</span><span class="sxs-lookup"><span data-stu-id="a3f26-134">To create the transport agent</span></span>

1. <span data-ttu-id="a3f26-135">添加命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="a3f26-135">Add references to the namespaces.</span></span>
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   <span data-ttu-id="a3f26-136">在 Exchange 2013 服务器上，您可以找到这些命名空间。</span><span class="sxs-lookup"><span data-stu-id="a3f26-136">You can find these namespaces on your Exchange 2013 server.</span></span> <span data-ttu-id="a3f26-137">以及其他中使用的类添加时对这些命名空间的引用，您都将有权[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)成员[Exchange 2013： 构建正文转换传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)示例。</span><span class="sxs-lookup"><span data-stu-id="a3f26-137">When you add a reference to these namespaces, you will have access to the [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) members as well as other classes used in the [Exchange 2013: Build a body conversion transport agent](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0) sample.</span></span> 
    
2. <span data-ttu-id="a3f26-138">实现[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)类派生的类。</span><span class="sxs-lookup"><span data-stu-id="a3f26-138">Implement the derived class for the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) class.</span></span> 
    
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

   <span data-ttu-id="a3f26-139">此代码将实例化派生的类，重写**CreateAgent**方法以创建新自定义代理的实例。</span><span class="sxs-lookup"><span data-stu-id="a3f26-139">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> 
    
3. <span data-ttu-id="a3f26-140">定义您的代理。</span><span class="sxs-lookup"><span data-stu-id="a3f26-140">Define your agent.</span></span>
    
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

   <span data-ttu-id="a3f26-141">定义您的代理类后，您可以添加您自定义功能。</span><span class="sxs-lookup"><span data-stu-id="a3f26-141">After you define your agent class, you can add your custom functionality.</span></span> <span data-ttu-id="a3f26-142">本示例中， [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx)事件将重定向到自定义事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="a3f26-142">In this example, the [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) event is redirected to your custom event handler.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a3f26-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a3f26-143">See also</span></span>

- [<span data-ttu-id="a3f26-144">传输代理 Exchange 2013 中的概念</span><span class="sxs-lookup"><span data-stu-id="a3f26-144">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)    
- [<span data-ttu-id="a3f26-145">Exchange 2013 的传输代理引用</span><span class="sxs-lookup"><span data-stu-id="a3f26-145">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="a3f26-146">SmtpReceiveAgentFactory</span><span class="sxs-lookup"><span data-stu-id="a3f26-146">SmtpReceiveAgentFactory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [<span data-ttu-id="a3f26-147">SmtpReceiveAgent</span><span class="sxs-lookup"><span data-stu-id="a3f26-147">SmtpReceiveAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

