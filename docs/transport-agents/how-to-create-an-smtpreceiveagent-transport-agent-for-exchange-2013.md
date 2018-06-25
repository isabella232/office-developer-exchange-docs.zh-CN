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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753183"
---
# <a name="create-an-smtpreceiveagent-transport-agent-for-exchange-2013"></a>创建 Exchange 2013 SmtpReceiveAgent 传输代理

了解如何创建自定义 SmtpReceiveAgent 传输代理与 Exchange 2013 一起使用。
  
**适用于：** Exchange Server 2013
  
相关的代码段和示例应用程序：

- [Exchange 2013： 构建正文转换传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)
  
[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类使您能够扩展客户端访问服务器上的前端传输服务或邮箱服务器上的传输服务的行为。 您可以使用这些类实现旨在响应消息，如它们进入组织的传输代理。 
  
[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类包含下表中列出的事件。 
  
**表 1。SmtpReceiveAgent 类事件**

|**事件**|**说明**|
|:-----|:-----|
|[OnAuthCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnAuthCommand.aspx) <br/> |当您的代理需要仅在 SMTP**身份验证**命令，如代理接受或拒绝中提供的信息的使用尝试传递邮件基于使用的身份验证方法的类型。  <br/> |
|[OnConnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnConnect.aspx) <br/> |当您的代理需要仅当连接到前端传输服务，如代理执行基于地址或域的远程 SMTP 服务器的操作，通过 SMTP 打开时提供的信息的使用。  <br/> |
|[OnDataCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDataCommand.aspx) <br/> |使用此事件时您代理需要 SMTP**数据**命令中提供的信息。  <br/> |
|[OnDisconnect](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnDisconnect.aspx) <br/> |当您的代理需要断开连接，才能执行时间计算当前日期和时间，如时可用的信息的使用。  <br/> |
|[OnEhloCommand](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEhloCommand.aspx) <br/> |当您的代理需要 SMTP **EHLO**命令; 中提供的信息的使用例如，如果您的代理接受或拒绝消息基于**EHLO**命令中提供的标识。  <br/> |
|[OnEndOfAuthentication](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfAuthentication.aspx) <br/> |当您的代理需要远程服务器完成身份验证过程中; 后提供信息的使用例如，对于基于由远程 SMTP 服务器或客户端提供的身份验证信息一条消息执行操作的代理。  <br/> |
|[OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx) <br/> |您的代理必须执行基于数据，可在邮件中操作时使用。 在前端传输服务将不触发此事件。 如果您传输代理必须使用此事件，必须在邮箱服务器上安装它。  <br/> |
|[OnEndOfHeaders](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfHeaders.aspx) <br/> |您的代理必须根据执行操作的提交的邮件头中可用的信息时使用。  <br/> |
   
## <a name="creating-a-custom-smtpreceiveagent-transport-agent"></a>创建自定义 SmtpReceiveAgent 传输代理

以下过程介绍如何创建自定义 SmtpReceiveAgent 传输代理。 
  
### <a name="to-create-the-transport-agent"></a>创建传输代理

1. 添加命名空间的引用。
    
   ```cs
      using Microsoft.Exchange.Data.Transport;
      using Microsoft.Exchange.Data.Transport.Smtp;
      using Microsoft.Exchange.Data.Transport.Email;
      using Microsoft.Exchange.Data.TextConverters;
  
   ```

   在 Exchange 2013 服务器上，您可以找到这些命名空间。 以及其他中使用的类添加时对这些命名空间的引用，您都将有权[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)成员[Exchange 2013： 构建正文转换传输代理](http://code.msdn.microsoft.com/Exchange/Exchange-2013-Build-a-body-ed36ecb0)示例。 
    
2. 实现[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)类派生的类。 
    
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

   此代码将实例化派生的类，重写**CreateAgent**方法以创建新自定义代理的实例。 
    
3. 定义您的代理。
    
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

   定义您的代理类后，您可以添加您自定义功能。 本示例中， [OnEndOfData](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.OnEndOfData.aspx)事件将重定向到自定义事件处理程序。 
    
## <a name="see-also"></a>另请参阅

- [传输代理 Exchange 2013 中的概念](transport-agent-concepts-in-exchange-2013.md)    
- [Exchange 2013 的传输代理引用](transport-agent-reference-for-exchange-2013.md)    
- [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)    
- [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)
    

