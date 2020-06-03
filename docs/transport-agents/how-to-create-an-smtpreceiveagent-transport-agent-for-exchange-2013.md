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
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>为 Exchange 2013 创建 SmtpReceiveAgent 传输代理

了解如何创建自定义 SmtpReceiveAgent 传输代理以与 Exchange 2013 一起使用。
  
**适用于：** Exchange Server 2013
  
相关的代码段和示例应用程序：

- [Exchange 2013：生成正文转换传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类使您能够在客户端访问服务器或邮箱服务器上的传输服务上扩展前端传输服务的行为。 可以使用这些类来实现传输代理，这些代理旨在在邮件进入您的组织时对其做出响应。 
  
[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类包括下表中列出的事件。 
  
**表1。SmtpReceiveAgent 类事件**

|**Event**|**说明**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |当代理需要仅在 SMTP **AUTH**命令中提供的信息（如接受或拒绝基于所使用的身份验证方法的发送邮件的尝试的代理）时使用。  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |当您的代理需要仅当通过 SMTP 将连接打开到前端传输服务时提供的信息，例如，基于远程 SMTP 服务器的地址或域执行操作的代理时使用。  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |当您的代理需要 SMTP**数据**命令中提供的信息时，请使用此事件。  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |如果代理需要在断开连接时可用的信息（如当前日期和时间），以便执行时间计算，请使用。  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |当代理需要 SMTP **EHLO**命令中提供的信息时使用;例如，如果您的代理根据**EHLO**命令中提供的标识接受或拒绝邮件。  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |当您的代理需要在远程服务器完成身份验证过程后可用的信息时，请使用。例如，对于基于远程 SMTP 服务器或客户端提供的身份验证信息对邮件执行操作的代理。  <br/> |
|[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |当代理必须基于邮件中提供的数据执行操作时使用。 在前端传输服务上不会触发此事件。 如果您的传输代理必须使用此事件，则必须将其安装在邮箱服务器上。  <br/> |
|[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |在代理必须基于提交的邮件的邮件头中提供的信息执行操作时使用。  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>创建自定义 SmtpReceiveAgent 传输代理

下面的过程介绍如何创建自定义 SmtpReceiveAgent 传输代理。 
  
### <a name="to-create-the-transport-agent"></a>创建传输代理

1. 添加对命名空间的引用。
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   您可以在 Exchange 2013 服务器上找到这些命名空间。 当您添加对这些命名空间的引用时，您将有权访问[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)成员以及在 Exchange 2013 中使用的其他类[：构建正文转换传输代理](https://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)示例。 
    
2. 为[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)类实现派生类。 
    
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

   此代码将实例化派生类并重写**CreateAgent**方法，以创建新的自定义代理的实例。 
    
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

   在定义代理类之后，可以添加自定义功能。 在此示例中， [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx)事件被重定向到自定义事件处理程序。 
    
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)    
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

