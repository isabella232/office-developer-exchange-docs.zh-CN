---
title: 创建 Exchange 2013 DeliveryAgent 传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: 了解如何创建自定义 DeliveryAgent 传输代理与 Exchange 2013 一起使用。
ms.openlocfilehash: 44ee5dc465f4435f0b835d264331cb719fe875c1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753057"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="c3a35-103">创建 Exchange 2013 DeliveryAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="c3a35-103">Create a DeliveryAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="c3a35-104">了解如何创建自定义 DeliveryAgent 传输代理与 Exchange 2013 一起使用。</span><span class="sxs-lookup"><span data-stu-id="c3a35-104">Find out how to create a custom DeliveryAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="c3a35-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="c3a35-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="c3a35-106">[DeliveryAgentFactory\<管理器\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx)类且旨在运行 Exchange Server 2013 邮箱服务器上的传输服务上的传输代理的基类。</span><span class="sxs-lookup"><span data-stu-id="c3a35-106">The [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) and [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) classes are the base classes for transport agents that are designed to run on the Transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="c3a35-107">您可能在下表中列出的事件[DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx)类提供您 DeliveryAgent 传输代理中实现处理程序。</span><span class="sxs-lookup"><span data-stu-id="c3a35-107">You might implement handlers in your DeliveryAgent transport agent for the events provided by the [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) class that are listed in the following table.</span></span> 
  
<span data-ttu-id="c3a35-108">**表 1。DeliveryAgent 类事件**</span><span class="sxs-lookup"><span data-stu-id="c3a35-108">**Table 1. DeliveryAgent class events**</span></span>

|<span data-ttu-id="c3a35-109">**事件**</span><span class="sxs-lookup"><span data-stu-id="c3a35-109">**Event**</span></span>|<span data-ttu-id="c3a35-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="c3a35-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c3a35-111">OnCloseConnection</span><span class="sxs-lookup"><span data-stu-id="c3a35-111">OnCloseConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) <br/> |<span data-ttu-id="c3a35-112">最后一个邮件项目已传递并且连接关闭之后发生。</span><span class="sxs-lookup"><span data-stu-id="c3a35-112">Occurs after the last mail item has been delivered and the connection is closed.</span></span>  <br/> |
|[<span data-ttu-id="c3a35-113">OnDeliverMailItem</span><span class="sxs-lookup"><span data-stu-id="c3a35-113">OnDeliverMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx) <br/> |<span data-ttu-id="c3a35-114">已准备好传送邮件项目时发生。</span><span class="sxs-lookup"><span data-stu-id="c3a35-114">Occurs when a mail item is ready to be delivered.</span></span>  <br/> |
|[<span data-ttu-id="c3a35-115">OnOpenConnection</span><span class="sxs-lookup"><span data-stu-id="c3a35-115">OnOpenConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) <br/> |<span data-ttu-id="c3a35-116">传递代理打开针对邮件传递时，发生此事件。</span><span class="sxs-lookup"><span data-stu-id="c3a35-116">Occurs when the delivery agent is opened for mail delivery.</span></span>  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a><span data-ttu-id="c3a35-117">创建自定义 DeliveryAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="c3a35-117">Creating a custom DeliveryAgent transport agent</span></span>

<span data-ttu-id="c3a35-118">以下过程介绍如何创建自定义 DeliveryAgent 传输代理。</span><span class="sxs-lookup"><span data-stu-id="c3a35-118">The following procedure describes how to create a custom DeliveryAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="c3a35-119">创建传输代理</span><span class="sxs-lookup"><span data-stu-id="c3a35-119">To create the transport agent</span></span>

1. <span data-ttu-id="c3a35-120">添加命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="c3a35-120">Add references to the namespaces.</span></span>
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   <span data-ttu-id="c3a35-121">Exchange 服务器上，您可以找到这些命名空间。</span><span class="sxs-lookup"><span data-stu-id="c3a35-121">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="c3a35-122">通过添加对这些命名空间的引用，您将有权[DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx)成员。</span><span class="sxs-lookup"><span data-stu-id="c3a35-122">By adding a reference to these namespaces, you will have access to the [DeliveryAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx) members.</span></span> 
    
2. <span data-ttu-id="c3a35-123">实现的派生的类[DeliveryAgentFactory\<管理器\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx)类。</span><span class="sxs-lookup"><span data-stu-id="c3a35-123">Implement the derived class for the [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx) class.</span></span> 
    
   ```cs
      public class MyDeliveryAgentFactory : DeliveryAgentFactory<MyDeliveryAgentFactory.MyDeliveryAgentManager>
      {
          static MyDeliveryAgentFactory()
          {
          }
          public override DeliveryAgent CreateAgent(SmtpServer server)
          {
              return new MyDeliveryAgent(server);
          }
          public sealed class MyDeliveryAgentManager : DeliveryAgentManager
          {
              /// <summary>
              /// Gets the supported delivery protocol.
              /// </summary>
              public override string SupportedDeliveryProtocol
              {
                  get { return "MyProtocol"; }
              }
          }
      }
  
   ```

   <span data-ttu-id="c3a35-124">此代码将实例化派生的类，重写**CreateAgent**方法以创建新自定义代理的实例。</span><span class="sxs-lookup"><span data-stu-id="c3a35-124">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="c3a35-125">此外可以在此类，以执行自定义代码重写其他方法，例如**关闭**。</span><span class="sxs-lookup"><span data-stu-id="c3a35-125">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> <span data-ttu-id="c3a35-126">创建一个[DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx)类重写[SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx)属性和设置您的代理将使用的协议。</span><span class="sxs-lookup"><span data-stu-id="c3a35-126">A [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) class is created to override the [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) property and set the protocol your agent will use.</span></span> 
    
3. <span data-ttu-id="c3a35-127">定义您的代理。</span><span class="sxs-lookup"><span data-stu-id="c3a35-127">Define your agent.</span></span>
    
   ```cs
      public class MyDeliveryAgent : DeliveryAgent
      {
          public MyDeliveryAgent(SmtpServer server)
          {
              this.OnCloseConnection += CloseConnection;
              this.OnDeliverMailItem += DeliverMailItem;
              this.OnOpenConnection += OpenConnection;
          }
      }
  
   ```

   <span data-ttu-id="c3a35-128">定义您的代理类后，您可以将您添加自定义功能。</span><span class="sxs-lookup"><span data-stu-id="c3a35-128">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="c3a35-129">在此示例中的三个事件， [OnCloseConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) 、 [OnDeliverMailItem](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx)和[OnOpenConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) ，重定向到自定义事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="c3a35-129">In this example, the three events, [OnCloseConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnCloseConnection.aspx) , [OnDeliverMailItem](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnDeliverMailItem.aspx) and [OnOpenConnection](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgent.OnOpenConnection.aspx) , are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c3a35-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c3a35-130">See also</span></span>

- [<span data-ttu-id="c3a35-131">传输代理 Exchange 2013 中的概念</span><span class="sxs-lookup"><span data-stu-id="c3a35-131">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="c3a35-132">Exchange 2013 的传输代理引用</span><span class="sxs-lookup"><span data-stu-id="c3a35-132">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)    
- [<span data-ttu-id="c3a35-133">DeliveryAgentFactory\<管理器\></span><span class="sxs-lookup"><span data-stu-id="c3a35-133">DeliveryAgentFactory\<Manager\></span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentFactory`1.aspx)   
- [<span data-ttu-id="c3a35-134">DeliveryAgent</span><span class="sxs-lookup"><span data-stu-id="c3a35-134">DeliveryAgent</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.DeliveryType.DeliveryAgent.aspx)    
- [<span data-ttu-id="c3a35-135">DeliveryAgentManager</span><span class="sxs-lookup"><span data-stu-id="c3a35-135">DeliveryAgentManager</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx)
    

