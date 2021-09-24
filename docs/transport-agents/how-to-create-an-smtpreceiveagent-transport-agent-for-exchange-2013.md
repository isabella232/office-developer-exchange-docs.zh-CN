---
title: 为 Exchange 2013 创建 SmtpReceiveAgent 传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: cdc7c462-74a7-49d6-95b2-155d783840e9
description: 了解如何创建自定义 SmtpReceiveAgent 传输代理以用于 Exchange 2013。
ms.openlocfilehash: a441f93113798c10421e9073e266c28fd87bca8d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513029"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>为 Exchange 2013 创建 SmtpReceiveAgent 传输代理

了解如何创建自定义 SmtpReceiveAgent 传输代理以用于 Exchange 2013。
  
**适用于：Exchange Server** 2013
  
相关代码段和示例应用：

- [Exchange 2013：构建正文转换传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类使您能够扩展客户端访问服务器或邮箱服务器上传输服务前端传输服务的行为。 可以使用这些类来实现传输代理，这些传输代理旨在响应进入组织的邮件。 
  
[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类包括下表中列出的事件。 
  
**表 1.SmtpReceiveAgent 类事件**

|**Event**|**说明**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |当代理需要仅在 SMTP **AUTH** 命令中提供的信息（例如，根据所使用的身份验证方法类型接受或拒绝传递邮件的尝试）时使用。  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |当代理需要仅在通过 SMTP 打开与前端传输服务的连接（如基于远程 SMTP 服务器的地址或域执行一个操作）时提供的信息时使用。  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |当代理需要 SMTP **DATA** 命令中提供的信息时，请使用此事件。  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |当代理需要断开连接时可用的信息（如当前日期和时间）时使用，以便执行时间计算。  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |在代理需要 SMTP **EHLO** 命令中提供的信息时使用;例如，如果代理根据 **EHLO** 命令中提供的标识接受或拒绝邮件。  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |在代理需要远程服务器完成身份验证过程后可用的信息时使用;例如，对于基于远程 SMTP 服务器或客户端提供的身份验证信息对邮件执行该操作的代理。  <br/> |
|[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |当代理必须基于邮件中可用的数据执行操作时，请使用 。 前端传输服务上不会发生此事件。 如果您的传输代理必须使用此事件，您必须将其安装在邮箱服务器上。  <br/> |
|[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |当代理必须基于提交的邮件头中提供的信息执行一个操作时使用。  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>创建自定义 SmtpReceiveAgent 传输代理

以下过程介绍如何创建自定义 SmtpReceiveAgent 传输代理。 
  
### <a name="to-create-the-transport-agent"></a>创建传输代理

1. 添加对命名空间的引用。
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   您可以在 Exchange 2013 服务器上找到这些命名空间。 当您添加对这些命名空间的引用时，您将有权访问[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)成员以及[Exchange 2013： Build a body conversion transport agent](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)示例中使用的其他类。 
    
2. 为 [SmtpReceiveAgentFactory 类实现派生](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) 类。 
    
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

   此代码将实例化派生的类并重写 **CreateAgent** 方法以创建新的自定义代理的实例。 
    
3. 定义代理。
    
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

   定义代理类后，可以添加自定义功能。 本示例中 [，OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) 事件重定向到自定义事件处理程序。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)    
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

