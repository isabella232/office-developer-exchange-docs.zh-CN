---
title: 为 Exchange 2013 创建 DeliveryAgent 传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: 了解如何创建自定义 DeliveryAgent 传输代理以与 Exchange 2013 一起使用。
ms.openlocfilehash: b349f0b6d835ba3d6195b43e80d1dcd21750bf82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527570"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a><span data-ttu-id="cc89f-103">为 Exchange 2013 创建 DeliveryAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="cc89f-103">Create a DeliveryAgent transport agent for Exchange 2013</span></span>

<span data-ttu-id="cc89f-104">了解如何创建自定义 DeliveryAgent 传输代理以与 Exchange 2013 一起使用。</span><span class="sxs-lookup"><span data-stu-id="cc89f-104">Find out how to create a custom DeliveryAgent transport agent to use with Exchange 2013.</span></span>
  
<span data-ttu-id="cc89f-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc89f-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="cc89f-106">[DeliveryAgentFactory \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx)和[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx)类是用于传输代理的基类，这些类旨在在 Exchange Server 2013 邮箱服务器上的传输服务上运行。</span><span class="sxs-lookup"><span data-stu-id="cc89f-106">The [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) and [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) classes are the base classes for transport agents that are designed to run on the Transport service on an Exchange Server 2013 Mailbox server.</span></span> <span data-ttu-id="cc89f-107">您可以在 DeliveryAgent 传输代理中为下表中列出的[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx)类提供的事件实现处理程序。</span><span class="sxs-lookup"><span data-stu-id="cc89f-107">You might implement handlers in your DeliveryAgent transport agent for the events provided by the [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) class that are listed in the following table.</span></span> 
  
<span data-ttu-id="cc89f-108">**表1。DeliveryAgent 类事件**</span><span class="sxs-lookup"><span data-stu-id="cc89f-108">**Table 1. DeliveryAgent class events**</span></span>

|<span data-ttu-id="cc89f-109">**Event**</span><span class="sxs-lookup"><span data-stu-id="cc89f-109">**Event**</span></span>|<span data-ttu-id="cc89f-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="cc89f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc89f-111">[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="cc89f-111">[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="cc89f-112">在最后一个邮件项传递且连接关闭之后发生。</span><span class="sxs-lookup"><span data-stu-id="cc89f-112">Occurs after the last mail item has been delivered and the connection is closed.</span></span>  <br/> |
|<span data-ttu-id="cc89f-113">[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="cc89f-113">[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="cc89f-114">当已准备好传递邮件项目时发生此事件。</span><span class="sxs-lookup"><span data-stu-id="cc89f-114">Occurs when a mail item is ready to be delivered.</span></span>  <br/> |
|<span data-ttu-id="cc89f-115">[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)</span><span class="sxs-lookup"><span data-stu-id="cc89f-115">[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)</span></span> <br/> |<span data-ttu-id="cc89f-116">打开传递代理进行邮件传递时发生。</span><span class="sxs-lookup"><span data-stu-id="cc89f-116">Occurs when the delivery agent is opened for mail delivery.</span></span>  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a><span data-ttu-id="cc89f-117">创建自定义 DeliveryAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="cc89f-117">Creating a custom DeliveryAgent transport agent</span></span>

<span data-ttu-id="cc89f-118">下面的过程介绍如何创建自定义 DeliveryAgent 传输代理。</span><span class="sxs-lookup"><span data-stu-id="cc89f-118">The following procedure describes how to create a custom DeliveryAgent transport agent.</span></span> 
  
### <a name="to-create-the-transport-agent"></a><span data-ttu-id="cc89f-119">创建传输代理</span><span class="sxs-lookup"><span data-stu-id="cc89f-119">To create the transport agent</span></span>

1. <span data-ttu-id="cc89f-120">添加对命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="cc89f-120">Add references to the namespaces.</span></span>
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   <span data-ttu-id="cc89f-121">您可以在您的 Exchange 服务器上找到这些命名空间。</span><span class="sxs-lookup"><span data-stu-id="cc89f-121">You can find these namespaces on your Exchange server.</span></span> <span data-ttu-id="cc89f-122">通过添加对这些命名空间的引用，您将有权访问[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx)成员。</span><span class="sxs-lookup"><span data-stu-id="cc89f-122">By adding a reference to these namespaces, you will have access to the [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) members.</span></span> 
    
2. <span data-ttu-id="cc89f-123">为[DeliveryAgentFactory \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx)类实现派生类。</span><span class="sxs-lookup"><span data-stu-id="cc89f-123">Implement the derived class for the [DeliveryAgentFactory\<Manager\>](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx) class.</span></span> 
    
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

   <span data-ttu-id="cc89f-124">此代码将实例化派生类并重写**CreateAgent**方法，以创建新的自定义代理的实例。</span><span class="sxs-lookup"><span data-stu-id="cc89f-124">This code will instantiate the derived class and override the **CreateAgent** method to create an instance of your new custom agent.</span></span> <span data-ttu-id="cc89f-125">此外，还可以在此类中重写其他方法（如**Close**），以执行自定义代码。</span><span class="sxs-lookup"><span data-stu-id="cc89f-125">Additional methods, such as **Close**, can also be overridden in this class to execute custom code.</span></span> <span data-ttu-id="cc89f-126">创建一个[DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx)类以重写[SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx)属性，并设置您的代理将使用的协议。</span><span class="sxs-lookup"><span data-stu-id="cc89f-126">A [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) class is created to override the [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) property and set the protocol your agent will use.</span></span> 
    
3. <span data-ttu-id="cc89f-127">定义代理。</span><span class="sxs-lookup"><span data-stu-id="cc89f-127">Define your agent.</span></span>
    
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

   <span data-ttu-id="cc89f-128">在定义代理类之后，可以添加自定义功能。</span><span class="sxs-lookup"><span data-stu-id="cc89f-128">After you define your agent class, you can add you custom functionality.</span></span> <span data-ttu-id="cc89f-129">在此示例中，将三个事件、 [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx)、 [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)和[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)重定向到您的自定义事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="cc89f-129">In this example, the three events, [OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx), [OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx), and [OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx), are redirected to your custom event handlers.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="cc89f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cc89f-130">See also</span></span>

- [<span data-ttu-id="cc89f-131">Exchange 2013 中的传输代理概念</span><span class="sxs-lookup"><span data-stu-id="cc89f-131">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="cc89f-132">Exchange 2013 的传输代理参考</span><span class="sxs-lookup"><span data-stu-id="cc89f-132">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)          

 