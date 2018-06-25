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
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>创建 Exchange 2013 RoutingAgent 传输代理

了解如何创建自定义 RoutingAgent 传输代理与 Exchange 2013 一起使用。
  
**适用于：** Exchange Server 2013
  
相关的代码段和示例应用程序：

- [Exchange 2013： 构建带宽日志记录传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)
  
[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)和[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类是旨在运行 Exchange Server 2013 邮箱服务器上的传输服务上的传输代理的基类。 [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)类提供了为其可能在您 RoutingAgent 传输代理中实现处理程序下表中列出的事件。 
  
**表 1。RoutingAgent 类事件**

|**事件**|**说明**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |如果需要，发生后服务器执行内容转换。  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |已解决所有收件人的邮件后，在由路由之前，发生此事件。  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |如果需要，发生后将邮件路由到下一个跃点服务器，并执行内容转换。 服务器可能使用更多资源处理比[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件中的每条消息，因为服务器将执行任何所需的内容转换和确定邮件路由中的下一个跃点之前，它在[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件处理程序中执行代码。  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |邮件脱离提交队列后发生。 如果您 RoutingAgent 传输代理不需要内容转换、 已解析的收件人或传送的数据，请使用[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件。  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>创建自定义 RoutingAgent 传输代理

以下过程介绍如何创建自定义 RoutingAgent 传输代理。 
  
### <a name="to-create-the-transport-agent"></a>创建传输代理

1. 添加命名空间的引用。
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   Exchange 服务器上，您可以找到这些命名空间。 通过添加对这些命名空间的引用，您将有权[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)成员以及其他中使用的类[Exchange 2013： 生成带宽日志记录传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)示例。 
    
2. 实现[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)类派生的类。 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   此代码将实例化派生的类，重写**CreateAgent**方法以创建新自定义代理的实例。 此外可以在此类，以执行自定义代码重写其他方法，例如**关闭**。 
    
3. 定义您的代理。
    
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

   定义您的代理类后，您可以将您添加自定义功能。 在此示例中的两个事件[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)和[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)重定向到自定义事件处理程序。 
    
## <a name="see-also"></a>另请参阅

- [传输代理 Exchange 2013 中的概念](transport-agent-concepts-in-exchange-2013.md)    
- [Exchange 2013 的传输代理引用](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

