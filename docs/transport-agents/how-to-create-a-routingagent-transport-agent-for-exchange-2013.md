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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463697"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>为 Exchange 2013 创建 RoutingAgent 传输代理

了解如何创建自定义 RoutingAgent 传输代理以与 Exchange 2013 一起使用。
  
**适用于：** Exchange Server 2013
  
相关的代码段和示例应用程序：

- [Exchange 2013：构建带宽日志记录传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)和[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类是用于传输代理的基类，这些类旨在在 Exchange Server 2013 邮箱服务器上的传输服务上运行。 [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类提供下表中列出的可在您的 RoutingAgent 传输代理中实现其处理程序的事件。 
  
**表1。RoutingAgent 类事件**

|**Event**|**说明**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |在服务器执行内容转换（如果需要）时，发生此事件。  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |在解决邮件的所有收件人和确定路由之前发生。  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |在服务器将邮件路由到下一个跃点并执行内容转换（如果需要）之后，发生此事件。 服务器可能会使用更多资源处理[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件中的每个邮件，而不是[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件，因为在执行[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件处理程序中的代码之前，服务器将执行任何必要的内容转换并确定邮件路由中的下一个跃点。  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |在邮件离开提交队列之后发生。 如果 RoutingAgent 传输代理不需要内容转换、解析的收件人或路由数据，则使用[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件。  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>创建自定义 RoutingAgent 传输代理

下面的过程介绍如何创建自定义 RoutingAgent 传输代理。 
  
### <a name="to-create-the-transport-agent"></a>创建传输代理

1. 添加对命名空间的引用。
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   您可以在您的 Exchange 服务器上找到这些命名空间。 通过添加对这些命名空间的引用，您将有权访问[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)成员以及 Exchange 2013 中使用的其他类[：构建带宽日志记录传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)示例。 
    
2. 为[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)类实现派生类。 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   此代码将实例化派生类并重写**CreateAgent**方法，以创建新的自定义代理的实例。 此外，还可以在此类中重写其他方法（如**Close**），以执行自定义代码。 
    
3. 定义代理。
    
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

   在定义代理类之后，可以添加自定义功能。 在此示例中，将两个事件[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)和[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)重定向到自定义事件处理程序。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)    
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

