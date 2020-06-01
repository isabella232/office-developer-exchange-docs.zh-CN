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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462372"
---
# <a name="creating-transport-agents-for-exchange-2013"></a><span data-ttu-id="2f9aa-103">创建 Exchange 2013 的传输代理</span><span class="sxs-lookup"><span data-stu-id="2f9aa-103">Creating transport agents for Exchange 2013</span></span>

<span data-ttu-id="2f9aa-104">查找有关如何为 Exchange 2013 创建自定义传输代理的信息，以及创建自定义代理的系统要求。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-104">Find information about how to create custom transport agents for Exchange 2013, and the system requirements for creating a custom agent.</span></span>
  
<span data-ttu-id="2f9aa-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="2f9aa-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="2f9aa-106">Exchange Server 2013 包括几个可用于处理邮件的传输代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-106">Exchange Server 2013 includes several transport agents that you can use to process messages.</span></span> <span data-ttu-id="2f9aa-107">通过使用 Exchange 附带的程序集，您可以创建自己的自定义代理，以根据您的组织的需要执行特定任务。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-107">By using the assemblies that come with Exchange, you can create your own custom agents to perform specific tasks according to the needs of your organization.</span></span> <span data-ttu-id="2f9aa-108">例如，可以使用 SmtpReceiveAgent 传输代理来截获通过 SMTP 协议接收的邮件，并处理邮件以转换正文的格式，以包含预设格式的文本。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-108">For example, you can use an SmtpReceiveAgent transport agent to intercept messages that are received via the SMTP protocol and process the message to convert the format of the body to contain preformatted text.</span></span> <span data-ttu-id="2f9aa-109">您可以使用 RoutingAgent 传输代理在路由到另一台服务器时记录通过该服务器传递的邮件。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-109">You can use a RoutingAgent transport agent to log the messages that pass through the server on route to another server.</span></span> <span data-ttu-id="2f9aa-110">您还可以创建更复杂的功能，使用多种类型的代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-110">You can also create more complex features that make use of more than one type of agent.</span></span> <span data-ttu-id="2f9aa-111">例如，若要创建防病毒代理，可以实现 SmtpReceiveAgent 和 RoutingAgent 代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-111">For example, to create an antivirus agent, you can implement an SmtpReceiveAgent and a RoutingAgent agent.</span></span> <span data-ttu-id="2f9aa-112">如果网络上有一个不支持 SMTP 协议的组件，则可以使用 DeliveryAgent 传输代理处理您的 Exchange 服务器和外部组件之间的通信。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-112">If you have a component on your network that does not support the SMTP protocol, you can use a DeliveryAgent transport agent to handle the communication between your Exchange server and your external component.</span></span> 
  
<span data-ttu-id="2f9aa-113">本文提供了有关创建您自己的传输代理所涉及的先决条件和任务的信息。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-113">This article provides information about the prerequisites for and tasks involved in creating your own transport agent.</span></span> <span data-ttu-id="2f9aa-114">有关创建特定传输代理的信息，请参阅[create a RoutingAgent transport agent For exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)，[为 Exchange 2013 创建 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)，并[创建 exchange 2013 的 DeliveryAgent 传输代理](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-114">For information about creating specific transport agents, see [Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span></span>
  
## <a name="prerequisites-for-creating-a-transport-agent"></a><span data-ttu-id="2f9aa-115">创建传输代理的先决条件</span><span class="sxs-lookup"><span data-stu-id="2f9aa-115">Prerequisites for creating a transport agent</span></span>
<span data-ttu-id="2f9aa-116"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="2f9aa-116"><a name="bk_prerequisites"> </a></span></span>

<span data-ttu-id="2f9aa-117">以下是实现传输代理所需的先决条件：</span><span class="sxs-lookup"><span data-stu-id="2f9aa-117">The following are the prerequisites that you need in order to implement a transport agent:</span></span>
  
- <span data-ttu-id="2f9aa-118">运行 Exchange 2013 的计算机，它运行客户端访问服务器或边缘传输服务器上的前端传输服务，或邮箱服务器上的传输服务。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-118">A computer running Exchange 2013 that is running the Front End Transport service on a Client Access or Edge Transport server, or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="2f9aa-119">有关 Exchange 2013 中的服务器角色体系结构的信息，请参阅[exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-119">For information about the server role architecture in Exchange 2013, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span></span>
    
- <span data-ttu-id="2f9aa-120">传输代理类的以下程序集：</span><span class="sxs-lookup"><span data-stu-id="2f9aa-120">The following assemblies for the transport agent classes:</span></span>
    
  - <span data-ttu-id="2f9aa-121">Microsoft. .dll</span><span class="sxs-lookup"><span data-stu-id="2f9aa-121">Microsoft.Exchange.Data.dll</span></span>
    
  - <span data-ttu-id="2f9aa-122">Microsoft. 公共 .dll</span><span class="sxs-lookup"><span data-stu-id="2f9aa-122">Microsoft.Exchange.Data.Common.dll</span></span>
    
  - <span data-ttu-id="2f9aa-123">Microsoft. .dll</span><span class="sxs-lookup"><span data-stu-id="2f9aa-123">Microsoft.Exchange.Transport.dll</span></span>
    
- <span data-ttu-id="2f9aa-124">.NET Framework 4。5</span><span class="sxs-lookup"><span data-stu-id="2f9aa-124">The .NET Framework 4.5</span></span>
    
<span data-ttu-id="2f9aa-125">此外，我们还建议您安装 Visual Studio 2012。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-125">We also recommend that you install Visual Studio 2012.</span></span> <span data-ttu-id="2f9aa-126">您可以使用 Visual Basic .NET 或 c # 来实现传输代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-126">You can implement transport agents by using either Visual Basic .NET or C#.</span></span>
  
## <a name="referencing-the-assemblies"></a><span data-ttu-id="2f9aa-127">引用程序集</span><span class="sxs-lookup"><span data-stu-id="2f9aa-127">Referencing the assemblies</span></span>
<span data-ttu-id="2f9aa-128"><a name="bk_ReferenceAssemblies"> </a></span><span class="sxs-lookup"><span data-stu-id="2f9aa-128"><a name="bk_ReferenceAssemblies"> </a></span></span>

<span data-ttu-id="2f9aa-129">Exchange 2013 提供了支持 Exchange 传输行为扩展的类库。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-129">Exchange 2013 provides a library of classes that support the extension of Exchange transport behavior.</span></span> <span data-ttu-id="2f9aa-130">这些类需要 .NET Framework 4.5。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-130">These classes require the .NET Framework 4.5.</span></span> <span data-ttu-id="2f9aa-131">您可以使用 Visual Studio 2012 基于这些类实现传输代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-131">You can implement transport agents based on these classes by using Visual Studio 2012.</span></span>
  
<span data-ttu-id="2f9aa-132">Exchange 2013 安装程序安装用于传输代理开发的程序集，并在全局程序集缓存（GAC）中注册这些程序集。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-132">The Exchange 2013 installer installs assemblies that are used for transport agent development and registers them in the global assembly cache (GAC).</span></span> <span data-ttu-id="2f9aa-133">若要开始实现传输代理，请创建一个对类库项目中的 "数据传输" 程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-133">To begin implementing a transport agent, create a reference to the Microsoft.Exchange.Data.Transport assembly in a class library project.</span></span>
  
## <a name="implementing-a-transport-agent"></a><span data-ttu-id="2f9aa-134">实现传输代理</span><span class="sxs-lookup"><span data-stu-id="2f9aa-134">Implementing a transport agent</span></span>
<span data-ttu-id="2f9aa-135"><a name="bk_implementationExample"> </a></span><span class="sxs-lookup"><span data-stu-id="2f9aa-135"><a name="bk_implementationExample"> </a></span></span>

<span data-ttu-id="2f9aa-136">下面的示例演示从[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类派生的类的最小实现。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-136">The following example shows a minimal implementation of classes that derive from the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="2f9aa-137">如果为同一事件安装并注册了多个传输代理，则即使一个代理删除了邮件项目中的所有收件人，也会调用所有代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-137">If multiple transport agents are installed and registered for the same event, all agents will be invoked, even if one agent removes all the recipients from a mail item.</span></span> <span data-ttu-id="2f9aa-138">> 为了避免未经处理的错误或不可预知的行为，传输代理应处理邮件项目上的收件人计数等于零的情况。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-138">> To avoid unhandled errors or unpredictable behavior, your transport agent should handle cases in which the recipient count on a mail item is equal to zero.</span></span> 
  
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

## <a name="installing-and-enabling-an-agent"></a><span data-ttu-id="2f9aa-139">安装和启用代理</span><span class="sxs-lookup"><span data-stu-id="2f9aa-139">Installing and enabling an agent</span></span>
<span data-ttu-id="2f9aa-140"><a name="bk_InstallEnable"> </a></span><span class="sxs-lookup"><span data-stu-id="2f9aa-140"><a name="bk_InstallEnable"> </a></span></span>

<span data-ttu-id="2f9aa-141">将代理编译到 DLL 之后，必须在开发 Exchange 服务器上安装并启用代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-141">After you compile your agent to a DLL, you must install and enable the agent on your development Exchange server.</span></span> <span data-ttu-id="2f9aa-142">在 Exchange 命令行管理程序中，使用[get-transportagent](https://technet.microsoft.com/library/aa997998.aspx) cmdlet 安装代理，并使用[get-transportagent](https://technet.microsoft.com/library/bb124921.aspx) cmdlet 启用代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-142">In the Exchange Management Shell, use the [Install-TransportAgent](https://technet.microsoft.com/library/aa997998.aspx) cmdlet to install your agent, and the [Enable-TransportAgent](https://technet.microsoft.com/library/bb124921.aspx) cmdlet to enable your agent.</span></span> <span data-ttu-id="2f9aa-143">有关如何使用 Exchange 命令行管理程序的信息，请参阅[Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-143">For information about how to use the Exchange Management Shell, see [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="2f9aa-144">传输代理对其遇到的所有电子邮件都具有完全访问权限。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-144">Transport agents have full access to all email messages that they encounter.</span></span> <span data-ttu-id="2f9aa-145">Exchange 2013 不限制传输代理的行为。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-145">Exchange 2013 does not restrict the behavior of a transport agent.</span></span> <span data-ttu-id="2f9aa-146">不稳定或包含安全缺陷的传输代理可能会影响 Exchange 2013 的稳定性和安全性。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-146">Transport agents that are unstable or that contain security flaws might affect the stability and security of Exchange 2013.</span></span> <span data-ttu-id="2f9aa-147">因此，应仅安装完全信任且已经过完全测试的传输代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-147">Therefore, you should only install transport agents that you fully trust and that have been fully tested.</span></span> 
  
<span data-ttu-id="2f9aa-148">当您使用**get-transportagent** cmdlet 安装代理时，Exchange 命令行管理程序将对程序集保持锁定。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-148">When you use the **Install-TransportAgent** cmdlet to install an agent, the Exchange Management Shell keeps a lock on the assembly.</span></span> <span data-ttu-id="2f9aa-149">若要释放对程序集的锁定，必须关闭用于安装代理的 Exchange 命令行管理程序实例。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-149">To release the lock on the assembly, you must close the instance of the Exchange Management Shell that you used to install the agent.</span></span> <span data-ttu-id="2f9aa-150">在释放锁定之前，您将无法更新程序集。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-150">You will be unable to update the assembly until you release the lock.</span></span> 
  
<span data-ttu-id="2f9aa-151">下面的示例演示如何使用 Exchange 命令行管理程序来安装和启用名为 MyAgent 的代理，方法是使用从名为 MyAgents 的[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)派生的类。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-151">The following example shows how to use the Exchange Management Shell to install and enable an agent named MyAgent by using a class derived from [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) named MyAgents.MyAgentFactory.</span></span> 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
<span data-ttu-id="2f9aa-152">此示例在安装了代理的服务器上命名代理 MyCustomAgent。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-152">This example names the agent MyCustomAgent on the server on which the agent is installed.</span></span> <span data-ttu-id="2f9aa-153">下面的示例展示了如何启用名为 MyCustomAgent 的代理。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-153">The following example shows how to enable the agent named MyCustomAgent.</span></span>
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
<span data-ttu-id="2f9aa-154">若要管理客户端访问服务器上的前端传输服务中的传输代理，请将以下值添加到命令： `-TransportService FrontEnd` 。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-154">To manage a transport agent in the Front End Transport service on a Client Access server, add the following value to the command:  `-TransportService FrontEnd`.</span></span> <span data-ttu-id="2f9aa-155">例如，若要查看前端传输服务中的传输代理，请运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-155">For example, to view the transport agents in the Front End Transport service, run the following command.</span></span>
  
 `Get-TransportAgent -TransportService FrontEnd`
  
<span data-ttu-id="2f9aa-156">有关安装、启用和管理代理的详细信息，请参阅[管理传输代理](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2f9aa-156">For more information about installing, enabling, and managing your agent, see [Manage Transport Agents](https://technet.microsoft.com/library/bb125175%28v=exchg.150%29.aspx).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="2f9aa-157">本节内容</span><span class="sxs-lookup"><span data-stu-id="2f9aa-157">In this section</span></span>
<span data-ttu-id="2f9aa-158"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="2f9aa-158"><a name="bk_inthissection"> </a></span></span>

- [<span data-ttu-id="2f9aa-159">为 Exchange 2013 创建 RoutingAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="2f9aa-159">Create a RoutingAgent transport agent for Exchange 2013</span></span>](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="2f9aa-160">为 Exchange 2013 创建 SmtpReceiveAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="2f9aa-160">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="2f9aa-161">为 Exchange 2013 创建 DeliveryAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="2f9aa-161">Create a DeliveryAgent transport agent for Exchange 2013</span></span>](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="2f9aa-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f9aa-162">See also</span></span>

- [<span data-ttu-id="2f9aa-163">Exchange 2013 中的传输代理概念</span><span class="sxs-lookup"><span data-stu-id="2f9aa-163">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)   
- [<span data-ttu-id="2f9aa-164">Exchange 2013 的传输代理参考</span><span class="sxs-lookup"><span data-stu-id="2f9aa-164">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    

