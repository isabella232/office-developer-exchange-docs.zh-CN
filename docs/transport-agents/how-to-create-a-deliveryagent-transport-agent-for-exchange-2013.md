---
title: 为 Exchange 2013 创建 DeliveryAgent 传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4af904d7-b315-4849-92b1-66018f76ffdf
description: 了解如何创建自定义 DeliveryAgent 传输代理以用于 Exchange 2013。
ms.openlocfilehash: b465c3bbd4658bea700d5be9f4eb16ae81693717
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526931"
---
# <a name="create-a-deliveryagent-transport-agent-for-exchange-2013"></a>为 Exchange 2013 创建 DeliveryAgent 传输代理

了解如何创建自定义 DeliveryAgent 传输代理以用于 Exchange 2013。
  
**适用于：Exchange Server** 2013
  
[DeliveryAgentFactory \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx)和[DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx)类是传输代理的基类，这些代理设计为在 Exchange Server 2013 邮箱服务器上运行。 您可以在 DeliveryAgent 传输代理中为下表中列出的 [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) 类提供的事件实现处理程序。 
  
**表 1.DeliveryAgent 类事件**

|**Event**|**说明**|
|:-----|:-----|
|[OnCloseConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) <br/> |在传递最后一个邮件项目并关闭连接后发生。  <br/> |
|[OnDeliverMailItem](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) <br/> |在准备好传递邮件项目时发生。  <br/> |
|[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx) <br/> |在打开传递代理进行邮件传递时发生。  <br/> |
   
## <a name="creating-a-custom-deliveryagent-transport-agent"></a>创建自定义 DeliveryAgent 传输代理

以下过程介绍如何创建自定义 DeliveryAgent 传输代理。 
  
### <a name="to-create-the-transport-agent"></a>创建传输代理

1. 添加对命名空间的引用。
    
   ```cs
        using Microsoft.Exchange.Data.Transport;
        using Microsoft.Exchange.Data.Transport.Delivery;
    
   ```

   您可以在您的 Exchange 服务器上找到这些命名空间。 通过添加对这些命名空间的引用，你将有权访问 [DeliveryAgent](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent(v=exchg.150).aspx) 成员。 
    
2. 实现[DeliveryAgentFactory 类的派生 \<Manager\> ](https://msdn.microsoft.com/library/dd877550(v=exchg.150).aspx)类。 
    
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

   此代码将实例化派生的类并重写 **CreateAgent** 方法以创建新的自定义代理的实例。 其他方法（如 **Close）** 也可以重写在此类中以执行自定义代码。 创建 [DeliveryAgentManager](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.aspx) 类以覆盖 [SupportedDeliveryProtocol](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Delivery.DeliveryAgentManager.SupportedDeliveryProtocol.aspx) 属性并设置代理将使用的协议。 
    
3. 定义代理。
    
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

   定义代理类后，可以添加自定义功能。 本示例中，三个事件 OnCloseConnection、OnDeliverMailItem 和[OnOpenConnection](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.onopenconnection(v=exchg.150).aspx)被重定向到自定义事件处理程序。 [](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.oncloseconnection(v=exchg.150).aspx) [](https://msdn.microsoft.com/library/microsoft.exchange.data.transport.delivery.deliveryagent.ondelivermailitem(v=exchg.150).aspx) 
    
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)          

 