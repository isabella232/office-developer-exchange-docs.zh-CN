---
title: 创建 Exchange 2013 的传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: 查找有关如何为 Exchange 2013 创建自定义传输代理的信息，以及创建自定义代理的系统要求。
ms.openlocfilehash: cb1cd180817524fe29a100a48d90444c75a77510
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462372"
---
# <a name="creating-transport-agents-for-exchange-2013"></a>创建 Exchange 2013 的传输代理

查找有关如何为 Exchange 2013 创建自定义传输代理的信息，以及创建自定义代理的系统要求。
  
**适用于：** Exchange Server 2013
  
Exchange Server 2013 包括几个可用于处理邮件的传输代理。 通过使用 Exchange 附带的程序集，您可以创建自己的自定义代理，以根据您的组织的需要执行特定任务。 例如，可以使用 SmtpReceiveAgent 传输代理来截获通过 SMTP 协议接收的邮件，并处理邮件以转换正文的格式，以包含预设格式的文本。 您可以使用 RoutingAgent 传输代理在路由到另一台服务器时记录通过该服务器传递的邮件。 您还可以创建更复杂的功能，使用多种类型的代理。 例如，若要创建防病毒代理，可以实现 SmtpReceiveAgent 和 RoutingAgent 代理。 如果网络上有一个不支持 SMTP 协议的组件，则可以使用 DeliveryAgent 传输代理处理您的 Exchange 服务器和外部组件之间的通信。 
  
本文提供了有关创建您自己的传输代理所涉及的先决条件和任务的信息。 有关创建特定传输代理的信息，请参阅[create a RoutingAgent transport agent For exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)，[为 Exchange 2013 创建 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)，并[创建 exchange 2013 的 DeliveryAgent 传输代理](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)。
  
## <a name="prerequisites-for-creating-a-transport-agent"></a>创建传输代理的先决条件
<a name="bk_prerequisites"> </a>

以下是实现传输代理所需的先决条件：
  
- 运行 Exchange 2013 的计算机，它运行客户端访问服务器或边缘传输服务器上的前端传输服务，或邮箱服务器上的传输服务。 有关 Exchange 2013 中的服务器角色体系结构的信息，请参阅[exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)。
    
- 传输代理类的以下程序集：
    
  - Microsoft. .dll
    
  - Microsoft. 公共 .dll
    
  - Microsoft. .dll
    
- .NET Framework 4。5
    
此外，我们还建议您安装 Visual Studio 2012。 您可以使用 Visual Basic .NET 或 c # 来实现传输代理。
  
## <a name="referencing-the-assemblies"></a>引用程序集
<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 提供了支持 Exchange 传输行为扩展的类库。 这些类需要 .NET Framework 4.5。 您可以使用 Visual Studio 2012 基于这些类实现传输代理。
  
Exchange 2013 安装程序安装用于传输代理开发的程序集，并在全局程序集缓存（GAC）中注册这些程序集。 若要开始实现传输代理，请创建一个对类库项目中的 "数据传输" 程序集的引用。
  
## <a name="implementing-a-transport-agent"></a>实现传输代理
<a name="bk_implementationExample"> </a>

下面的示例演示从[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类派生的类的最小实现。 
  
> [!CAUTION]
> 如果为同一事件安装并注册了多个传输代理，则即使一个代理删除了邮件项目中的所有收件人，也会调用所有代理。 > 为了避免未经处理的错误或不可预知的行为，传输代理应处理邮件项目上的收件人计数等于零的情况。 
  
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

将代理编译到 DLL 之后，必须在开发 Exchange 服务器上安装并启用代理。 在 Exchange 命令行管理程序中，使用[get-transportagent](https://technet.microsoft.com/library/aa997998.aspx) cmdlet 安装代理，并使用[get-transportagent](https://technet.microsoft.com/library/bb124921.aspx) cmdlet 启用代理。 有关如何使用 Exchange 命令行管理程序的信息，请参阅[Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。
  
> [!CAUTION]
> 传输代理对其遇到的所有电子邮件都具有完全访问权限。 Exchange 2013 不限制传输代理的行为。 不稳定或包含安全缺陷的传输代理可能会影响 Exchange 2013 的稳定性和安全性。 因此，应仅安装完全信任且已经过完全测试的传输代理。 
  
当您使用**get-transportagent** cmdlet 安装代理时，Exchange 命令行管理程序将对程序集保持锁定。 若要释放对程序集的锁定，必须关闭用于安装代理的 Exchange 命令行管理程序实例。 在释放锁定之前，您将无法更新程序集。 
  
下面的示例演示如何使用 Exchange 命令行管理程序来安装和启用名为 MyAgent 的代理，方法是使用从名为 MyAgents 的[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)派生的类。 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
此示例在安装了代理的服务器上命名代理 MyCustomAgent。 下面的示例展示了如何启用名为 MyCustomAgent 的代理。
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
若要管理客户端访问服务器上的前端传输服务中的传输代理，请将以下值添加到命令： `-TransportService FrontEnd` 。 例如，若要查看前端传输服务中的传输代理，请运行以下命令。
  
 `Get-TransportAgent -TransportService FrontEnd`
  
有关安装、启用和管理代理的详细信息，请参阅[管理传输代理](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx)。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [为 Exchange 2013 创建 RoutingAgent 传输代理](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [为 Exchange 2013 创建 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [为 Exchange 2013 创建 DeliveryAgent 传输代理](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)   
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)
    

