---
title: 创建 Exchange 2013 的传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: 查找有关如何创建 Exchange 2013 的自定义传输代理和创建自定义代理的系统要求的信息。
ms.openlocfilehash: 6146e37c44441bed1d30d08f71ede255dba26440
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753061"
---
# <a name="creating-transport-agents-for-exchange-2013"></a>创建 Exchange 2013 的传输代理

查找有关如何创建 Exchange 2013 的自定义传输代理和创建自定义代理的系统要求的信息。
  
**适用于：** Exchange Server 2013
  
Exchange Server 2013 包括几个可用于处理邮件的传输代理。 通过使用 Exchange 附带的程序集，您可以创建您自己的自定义代理执行根据贵组织的需要的特定任务。 例如，您可以使用截距邮件的 SMTP 协议和处理转换的正文包含预设格式的文本格式的消息通过接收的 SmtpReceiveAgent 传输代理。 您可以使用 RoutingAgent 传输代理登录通过服务器的路由路径传递到另一台服务器的消息。 您还可以创建更复杂功能使使用多个类型的代理。 例如，若要创建的防病毒代理，您可以实现 SmtpReceiveAgent 和 RoutingAgent 代理。 如果您不支持的 SMTP 协议的网络中有一个组件，您可以使用 DeliveryAgent 传输代理处理您的 Exchange 服务器和外部组件之间的通信。 
  
本文提供了有关先决条件和创建自己的传输代理中所涉及的任务的信息。 有关创建特定传输代理的信息，请参阅[创建 Exchange 2013 RoutingAgent 传输代理](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)、[创建 Exchange 2013 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)和[创建 DeliveryAgent 传输代理的Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)。
  
## <a name="prerequisites-for-creating-a-transport-agent"></a>创建传输代理的先决条件
<a name="bk_prerequisites"> </a>

以下是您需要实现传输代理的先决条件：
  
- 运行 Exchange 2013 客户端访问或边缘传输服务器或邮箱服务器上的传输服务上运行的前端传输服务的计算机。 有关 Exchange 2013 中的服务器角色体系结构的信息，请参阅[在 Exchange 2013 传输代理概念](transport-agent-concepts-in-exchange-2013.md)。
    
- 传输代理类的以下程序集：
    
  - Microsoft.Exchange.Data.dll
    
  - Microsoft.Exchange.Data.Common.dll
    
  - Microsoft.Exchange.Transport.dll
    
- .NET Framework 4.5
    
我们还建议您在安装 Visual Studio 2012。 您可以通过使用 Visual Basic.NET 或 C# 实现传输代理。
  
## <a name="referencing-the-assemblies"></a>引用程序集
<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 提供了支持 Exchange 传输行为的扩展的类的库。 这些类需要.NET Framework 4.5。 您可以实现通过使用 Visual Studio 2012 基于这些类的传输代理。
  
Exchange 2013 安装程序安装用于传输代理开发的程序集，并在全局程序集缓存 (GAC) 中注册它们。 若要开始实施传输代理，创建一个类库项目中的 Microsoft.Exchange.Data.Transport 程序集的引用。
  
## <a name="implementing-a-transport-agent"></a>实现传输代理
<a name="bk_implementationExample"> </a>

下面的示例演示最小的[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类派生的类的实现。 
  
> [!CAUTION]
> 如果多个传输代理是安装并注册相同的事件，将调用所有代理，即使一个代理从邮件项目中删除所有收件人。 > 到避免未经处理的错误或不可预测的行为，传输代理应处理顺序邮件项目上的收件人计数等于零的情况。 
  
```cs
using System;
using System.Collections.Generic;
using System.Text;
using Microsoft.Exchange.Data.Transport;
using Microsoft.Exchange.Data.Transport.Smtp;
namespace MyAgents
{
    public sealed class MyAgentFactory : SmtpReceiveAgentFactory
    {
        public override SmtpReceiveAgent CreateAgent(SmtpServer server)
        {
            return new MyAgent();
        }
    }
    public class MyAgent : SmtpReceiveAgent
    {
        public MyAgent()
        {
            this.OnEndOfData += new EndOfDataEventHandler(MyEndOfDataHandler);
        }
        private void MyEndOfDataHandler (ReceiveMessageEventSource source, EndOfDataEventArgs e)
        {
            // The following line appends text to the subject of the message that caused the event.
            e.MailItem.Message.Subject += " - this text appended by MyAgent";
        }
    }
}
```

```vb
Imports System
Imports System.Collections.Generic
Imports System.Text
Imports Microsoft.Exchange.Data.Transport
Imports Microsoft.Exchange.Data.Transport.Smtp
Namespace MyAgents
    NotInheritable Class MyAgentFactory
        Inherits SmtpReceiveAgentFactory
        Public Overrides Function CreateAgent(ByVal server as SmtpServer) As SmtpReceiveAgent
            Return New MyAgent
        End Function
    End Class
    Public Class MyAgent
        Inherits SmtpReceiveAgent
        Private Sub MyEndOfDataHandler(ByVal source As ReceiveMessageEventSource, ByVal e As EndOfDataEventArgs) Handles Me.OnEndOfData
            ' The following line appends text to the subject of the message that caused the event.
            e.MailItem.Message.Subject &amp;= e.MailItem.Message.Subject + " - this text appended by MyAgent"
        End Sub
    End Class
End Namespace
```

## <a name="installing-and-enabling-an-agent"></a>安装和启用代理
<a name="bk_InstallEnable"> </a>

编译到 DLL 您代理之后，您必须安装和开发 Exchange 服务器上启用代理。 在 Exchange 命令行管理程序，使用[Install-transportagent](http://technet.microsoft.com/en-us/library/aa997998.aspx) cmdlet 来安装您的代理，并使用[Enable-transportagent](http://technet.microsoft.com/en-us/library/bb124921.aspx) cmdlet 启用您的代理。 有关如何使用 Exchange 命令行管理程序的信息，请参阅[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。
  
> [!CAUTION]
> 传输代理已对他们所遇到的所有电子邮件的完全访问权限。 Exchange 2013 不会限制传输代理的行为。 传输代理不稳定或包含安全漏洞的可能影响的稳定性和 Exchange 2013 的安全性。 因此，您应只安装完全信任并经过充分测试传输代理。 
  
当您使用**Install-transportagent** cmdlet 安装代理时，Exchange 命令行管理程序组件上保留锁。 若要解除对程序集的锁定，必须关闭 Exchange Management Shell 您用来安装代理的实例。 您将无法更新该程序集，直到解除锁定。 
  
下面的示例演示如何使用 Exchange 命令行管理程序来安装和启用使用从名为 MyAgents.MyAgentFactory [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)派生的类名为 MyAgent 代理。 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
本示例名称在其安装代理服务器上的代理 MyCustomAgent。 下面的示例演示如何启用名为 MyCustomAgent 的代理。
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
若要管理传输代理的客户端访问服务器上的前端传输服务中，为命令添加以下值： `-TransportService FrontEnd`。 例如，若要查看的前端传输服务中的传输代理，运行以下命令。
  
 `Get-TransportAgent -TransportService FrontEnd`
  
有关安装的详细信息，启用和管理您的代理，请参阅[管理传输代理](http://technet.microsoft.com/en-us/library/bb125175%28v=exchg.150%29.aspx)。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [创建 Exchange 2013 RoutingAgent 传输代理](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [创建 Exchange 2013 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [创建 Exchange 2013 DeliveryAgent 传输代理](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [传输代理 Exchange 2013 中的概念](transport-agent-concepts-in-exchange-2013.md)   
- [Exchange 2013 的传输代理引用](transport-agent-reference-for-exchange-2013.md)
    

