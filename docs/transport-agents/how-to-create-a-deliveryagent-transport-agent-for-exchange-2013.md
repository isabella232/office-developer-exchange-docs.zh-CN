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
ms.openlocfilehash: bc36c7b5e0fb8006c5927d423d7767dcc7382ce0
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353306"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a>创建 Exchange 2013 DeliveryAgent 传输代理

了解如何创建自定义 DeliveryAgent 传输代理与 Exchange 2013 一起使用。
  
**适用于：** Exchange Server 2013
  
[DeliveryAgentFactory\<管理器\>](https://msdn.microsoft.com/en-us/library/dd877550(v=exchg.150).aspx) [DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx)类且旨在运行 Exchange Server 2013 邮箱服务器上的传输服务上的传输代理的基类。 您可能在下表中列出的事件[DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx)类提供您 DeliveryAgent 传输代理中实现处理程序。 
  
**表 1。DeliveryAgent 类事件**

|"事件"|**说明**|
|:-----|:-----|
|[OnCloseConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) <br/> |最后一个邮件项目已传递并且连接关闭之后发生。  <br/> |
|[OnDeliverMailItem](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) <br/> |已准备好传送邮件项目时发生。  <br/> |
|[OnOpenConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx) <br/> |传递代理打开针对邮件传递时，发生此事件。  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a>创建自定义 DeliveryAgent 传输代理

以下过程介绍如何创建自定义 DeliveryAgent 传输代理。 
  
### <a name="to-create-the-transport-agent"></a>创建传输代理

1. 添加命名空间的引用。
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   Exchange 服务器上，您可以找到这些命名空间。 通过添加对这些命名空间的引用，您将有权[DeliveryAgent](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx)成员。 
    
2. 实现的派生的类[DeliveryAgentFactory\<管理器\>](https://msdn.microsoft.com/en-us/library/dd877550(v=exchg.150).aspx)类。 
    
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

   此代码将实例化派生的类，重写**CreateAgent**方法以创建新自定义代理的实例。 此外可以在此类，以执行自定义代码重写其他方法，例如**关闭**。 创建一个[DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx)类重写[SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx)属性和设置您的代理将使用的协议。 
    
3. 定义您的代理。
    
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

   定义您的代理类后，您可以将您添加自定义功能。 在此示例、 三个事件、 [OnCloseConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx)、 [OnDeliverMailItem](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx)和[OnOpenConnection](https://msdn.microsoft.com/en-us/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)，将重定向至您的自定义事件处理程序。 
    
## <a name="see-also"></a>另请参阅

- [传输代理 Exchange 2013 中的概念](transport-agent-concepts-in-exchange-2013.md)
- [Exchange 2013 的传输代理引用](transport-agent-reference-for-exchange-2013.md)          

 