---
title: 为 Exchange 2013 创建传输代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d291ab78-7cdd-4dbe-a5f4-9dc8e9650a33
description: 查找有关如何为 Exchange 2013 创建自定义传输代理的信息，以及创建自定义代理的系统要求。
ms.openlocfilehash: ea5ae1fab85fde781cb365a21b7a40ccd52955b3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520953"
---
# <a name="creating-transport-agents-for-exchange-2013"></a>为 Exchange 2013 创建传输代理

查找有关如何为 Exchange 2013 创建自定义传输代理的信息，以及创建自定义代理的系统要求。
  
**适用于：Exchange Server** 2013
  
Exchange Server 2013 包括多个可用于处理邮件的传输代理。 通过使用 Exchange，您可以创建自己的自定义代理，以根据组织的需要执行特定任务。 例如，您可以使用 SmtpReceiveAgent 传输代理截获通过 SMTP 协议接收的邮件，并处理邮件以转换正文的格式以包含预设格式的文本。 可以使用 RoutingAgent 传输代理记录通过服务器路由到另一台服务器的邮件。 您还可以创建使用多种类型的代理的更复杂的功能。 例如，若要创建防病毒代理，可以实施 SmtpReceiveAgent 和 RoutingAgent 代理。 如果您的网络上有一个不支持 SMTP 协议的组件，您可以使用 DeliveryAgent 传输代理来处理 Exchange 服务器和外部组件之间的通信。 
  
本文提供有关创建自己的传输代理的先决条件和涉及的任务的信息。 有关创建特定传输代理的信息，请参阅 Create [a RoutingAgent transport agent for Exchange 2013、Create](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md) [an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)和[Create a DeliveryAgent transport agent for Exchange 2013。](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
  
## <a name="prerequisites-for-creating-a-transport-agent"></a>创建传输代理的先决条件
<a name="bk_prerequisites"> </a>

以下是实现传输代理所需的先决条件：
  
- 运行 Exchange 2013 的计算机，该计算机在客户端访问或边缘传输服务器上运行前端传输服务，或在邮箱服务器上运行传输服务。 有关 Exchange 2013 中的服务器角色体系结构的信息，请参阅[transport agent concepts in Exchange 2013。](transport-agent-concepts-in-exchange-2013.md)
    
- 传输代理类的以下程序集：
    
  - Microsoft.Exchange.Data.dll
    
  - Microsoft.Exchange.Data.Common.dll
    
  - Microsoft.Exchange.Transport.dll
    
- The .NET Framework 4.5
    
我们还建议您安装 Visual Studio 2012。 可以使用 .NET 或 Visual Basic 实现传输C#。
  
## <a name="referencing-the-assemblies"></a>引用程序集
<a name="bk_ReferenceAssemblies"> </a>

Exchange 2013 提供了一个类库，这些类支持传输Exchange扩展。 这些类需要 .NET Framework 4.5。 通过使用 2012，您可以基于这些类Visual Studio代理。
  
the Exchange 2013 installer installs assemblies that are used for transport agent development and registers them in the global assembly cache (GAC) . 若要开始实现传输代理，请创建对 Microsoft 的引用。Exchange。类库项目中的 Data.Transport 程序集。
  
## <a name="implementing-a-transport-agent"></a>实现传输代理
<a name="bk_implementationExample"> </a>

下面的示例演示从 [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) 和 [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) 类派生的类的最少实现。 
  
> [!CAUTION]
> 如果为同一事件安装并注册了多个传输代理，将调用所有代理，即使一个代理从邮件项目中删除所有收件人。 > 为了避免未经处理的错误或不可预知的行为，传输代理应处理邮件项目的收件人计数等于零的情况。 
  
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

将代理编译为 DLL 后，必须在开发服务器上安装并启用Exchange代理。 在命令行Exchange命令行管理程序中，使用[Install-TransportAgent](https://technet.microsoft.com/library/aa997998.aspx) cmdlet 安装代理，使用[Enable-TransportAgent](https://technet.microsoft.com/library/bb124921.aspx) cmdlet 启用代理。 有关如何使用命令行管理程序Exchange，请参阅 Exchange Server [PowerShell (Exchange Management Shell) 。 ](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
  
> [!CAUTION]
> 传输代理对其遇到的所有电子邮件都具有完全访问权限。 Exchange 2013 不限制传输代理的行为。 不稳定或包含安全缺陷的传输代理可能会影响 2013 Exchange的安全性。 因此，只应安装完全信任且经过完全测试的传输代理。 
  
使用 **Install-TransportAgent** cmdlet 安装代理时，Exchange命令行管理程序对程序集保持锁定。 若要解除对程序集的锁定，必须关闭用于安装Exchange命令行管理程序的实例。 在解除锁定之前，将无法更新程序集。 
  
以下示例演示如何使用 Exchange 命令行管理程序，通过使用派生自名为 MyAgents.MyAgentFactory 的[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)的类来安装和启用名为 MyAgent 的代理。 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
本示例将安装代理的服务器上代理 MyCustomAgent 命名。 以下示例演示如何启用名为 MyCustomAgent 的代理。
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
若要在客户端访问服务器的前端传输服务中管理传输代理，请向命令中添加以下值  `-TransportService FrontEnd` ：。 例如，若要查看前端传输服务中的传输代理，请运行以下命令。
  
 `Get-TransportAgent -TransportService FrontEnd`
  
有关安装、启用和管理代理的信息，请参阅管理 [传输代理](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx)。
  
## <a name="in-this-section"></a>本节内容
<a name="bk_inthissection"> </a>

- [为 Exchange 2013 创建 RoutingAgent 传输代理](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [为 Exchange 2013 创建 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [为 Exchange 2013 创建 DeliveryAgent 传输代理](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)   
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)
    

