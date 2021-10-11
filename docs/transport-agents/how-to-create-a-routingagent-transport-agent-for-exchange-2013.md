---
title: 为 Exchange 2013 创建 RoutingAgent 传输代理
manager: sethgros
ms.date: 09/21/2021
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f0e745f-9289-4f31-8877-926692a8c133
description: 了解如何创建自定义 RoutingAgent 传输代理以用于 Exchange 2013。
ms.openlocfilehash: 89c70e7d021b9b2cc46f65ee3bbff334430fecc7
ms.sourcegitcommit: f13a3a4a61fa23ca6414b7c96ddf087adbe3dc9e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/11/2021
ms.locfileid: "60262209"
---
# <a name="create-a-routingagent-transport-agent-for-exchange-2013"></a>为 Exchange 2013 创建 RoutingAgent 传输代理

了解如何创建自定义 RoutingAgent 传输代理以用于 Exchange 2013。
  
**适用于：Exchange Server** 2013 年 10 月
  
相关代码段和示例应用：

- [Exchange 2013：构建带宽日志记录传输代理](/exchange/client-developer/transport-agents/transport-agent-code-samples-for-exchange-2013.md)
  
[RoutingAgentFactory](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564164(v=exchg.150))和[RoutingAgent](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564421(v=exchg.150))类是设计为在 Exchange Server 2013 邮箱服务器上运行传输代理的基类。 [RoutingAgent](https://docs.microsoft.com/previous-versions/office/exchange-server-api/aa564421(v=exchg.150))类提供下表中列出的事件，您可以在 RoutingAgent 传输代理中为这些事件实现处理程序。 
  
**表 1.RoutingAgent 类事件**

|**Event**|**说明**|
|:-----|:-----|
|[OnCategorizedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnCategorizedMessage.aspx) <br/> |在服务器执行内容转换（如果需要）之后发生。  <br/> |
|[OnResolvedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnResolvedMessage.aspx) <br/> |在解析邮件的所有收件人之后和确定路由之前发生。  <br/> |
|[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx) <br/> |在服务器将邮件路由到下一个跃点并执行内容转换（如果需要）之后发生。 服务器可能使用比[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx)事件更多的资源来处理[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件的每封邮件，因为服务器将执行任何必要的内容转换并确定邮件路由中的下一个跃点，然后再在[OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)事件处理程序中执行代码。  <br/> |
|[OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) <br/> |在邮件从提交队列关闭后发生。 如果 RoutingAgent 传输代理不需要内容转换、解析的收件人或路由数据，请使用 [OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) 事件。  <br/> |
   
## <a name="creating-a-custom-routingagent-transport-agent"></a>创建自定义 RoutingAgent 传输代理

以下过程介绍如何创建自定义 RoutingAgent 传输代理。 
  
### <a name="to-create-the-transport-agent"></a>创建传输代理

1. 添加对命名空间的引用。
    
   ```cs
      using Microsoft.Exchange.Data.Mime;
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Routing;
  
   ```

   您可以在您的 Exchange 服务器上找到这些命名空间。 通过添加对这些命名空间的引用，您将有权访问[RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)成员以及[Exchange 2013： Build a bandwidth logging transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-d61a4aaa)示例中使用的其他类。 
    
2. 为 [RoutingAgentFactory 类实现派生](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) 类。 
    
   ```cs
      public class BandwidthLoggerFactory : RoutingAgentFactory
      {
          public override RoutingAgent CreateAgent(SmtpServer server)
          {
              return new BandwidthLogger(server);
          }
      }
  
   ```

   此代码将实例化派生的类并重写 **CreateAgent** 方法以创建新的自定义代理的实例。 其他方法（如 **Close）** 也可以重写在此类中以执行自定义代码。 
    
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

   定义代理类后，可以添加自定义功能。 本示例中 [，OnSubmittedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnSubmittedMessage.aspx) 和 [OnRoutedMessage](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.OnRoutedMessage.aspx)这两个事件被重定向到自定义事件处理程序。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)    
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)    
- [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)    
- [RoutingAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgent.aspx)
    

