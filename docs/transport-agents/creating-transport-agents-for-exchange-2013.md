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
# <a name="creating-transport-agents-for-exchange-2013"></a><span data-ttu-id="47098-103">创建 Exchange 2013 的传输代理</span><span class="sxs-lookup"><span data-stu-id="47098-103">Creating transport agents for Exchange 2013</span></span>

<span data-ttu-id="47098-104">查找有关如何创建 Exchange 2013 的自定义传输代理和创建自定义代理的系统要求的信息。</span><span class="sxs-lookup"><span data-stu-id="47098-104">Find information about how to create custom transport agents for Exchange 2013, and the system requirements for creating a custom agent.</span></span>
  
<span data-ttu-id="47098-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="47098-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="47098-106">Exchange Server 2013 包括几个可用于处理邮件的传输代理。</span><span class="sxs-lookup"><span data-stu-id="47098-106">Exchange Server 2013 includes several transport agents that you can use to process messages.</span></span> <span data-ttu-id="47098-107">通过使用 Exchange 附带的程序集，您可以创建您自己的自定义代理执行根据贵组织的需要的特定任务。</span><span class="sxs-lookup"><span data-stu-id="47098-107">By using the assemblies that come with Exchange, you can create your own custom agents to perform specific tasks according to the needs of your organization.</span></span> <span data-ttu-id="47098-108">例如，您可以使用截距邮件的 SMTP 协议和处理转换的正文包含预设格式的文本格式的消息通过接收的 SmtpReceiveAgent 传输代理。</span><span class="sxs-lookup"><span data-stu-id="47098-108">For example, you can use an SmtpReceiveAgent transport agent to intercept messages that are received via the SMTP protocol and process the message to convert the format of the body to contain preformatted text.</span></span> <span data-ttu-id="47098-109">您可以使用 RoutingAgent 传输代理登录通过服务器的路由路径传递到另一台服务器的消息。</span><span class="sxs-lookup"><span data-stu-id="47098-109">You can use a RoutingAgent transport agent to log the messages that pass through the server on route to another server.</span></span> <span data-ttu-id="47098-110">您还可以创建更复杂功能使使用多个类型的代理。</span><span class="sxs-lookup"><span data-stu-id="47098-110">You can also create more complex features that make use of more than one type of agent.</span></span> <span data-ttu-id="47098-111">例如，若要创建的防病毒代理，您可以实现 SmtpReceiveAgent 和 RoutingAgent 代理。</span><span class="sxs-lookup"><span data-stu-id="47098-111">For example, to create an antivirus agent, you can implement an SmtpReceiveAgent and a RoutingAgent agent.</span></span> <span data-ttu-id="47098-112">如果您不支持的 SMTP 协议的网络中有一个组件，您可以使用 DeliveryAgent 传输代理处理您的 Exchange 服务器和外部组件之间的通信。</span><span class="sxs-lookup"><span data-stu-id="47098-112">If you have a component on your network that does not support the SMTP protocol, you can use a DeliveryAgent transport agent to handle the communication between your Exchange server and your external component.</span></span> 
  
<span data-ttu-id="47098-113">本文提供了有关先决条件和创建自己的传输代理中所涉及的任务的信息。</span><span class="sxs-lookup"><span data-stu-id="47098-113">This article provides information about the prerequisites for and tasks involved in creating your own transport agent.</span></span> <span data-ttu-id="47098-114">有关创建特定传输代理的信息，请参阅[创建 Exchange 2013 RoutingAgent 传输代理](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)、[创建 Exchange 2013 SmtpReceiveAgent 传输代理](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)和[创建 DeliveryAgent 传输代理的Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="47098-114">For information about creating specific transport agents, see [Create a RoutingAgent transport agent for Exchange 2013](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md), [Create an SmtpReceiveAgent transport agent for Exchange 2013](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md), and [Create a DeliveryAgent transport agent for Exchange 2013](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md).</span></span>
  
## <a name="prerequisites-for-creating-a-transport-agent"></a><span data-ttu-id="47098-115">创建传输代理的先决条件</span><span class="sxs-lookup"><span data-stu-id="47098-115">Prerequisites for creating a transport agent</span></span>
<span data-ttu-id="47098-116"><a name="bk_prerequisites"> </a></span><span class="sxs-lookup"><span data-stu-id="47098-116"></span></span>

<span data-ttu-id="47098-117">以下是您需要实现传输代理的先决条件：</span><span class="sxs-lookup"><span data-stu-id="47098-117">The following are the prerequisites that you need in order to implement a transport agent:</span></span>
  
- <span data-ttu-id="47098-118">运行 Exchange 2013 客户端访问或边缘传输服务器或邮箱服务器上的传输服务上运行的前端传输服务的计算机。</span><span class="sxs-lookup"><span data-stu-id="47098-118">A computer running Exchange 2013 that is running the Front End Transport service on a Client Access or Edge Transport server, or the Transport service on a Mailbox server.</span></span> <span data-ttu-id="47098-119">有关 Exchange 2013 中的服务器角色体系结构的信息，请参阅[在 Exchange 2013 传输代理概念](transport-agent-concepts-in-exchange-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="47098-119">For information about the server role architecture in Exchange 2013, see [Transport agent concepts in Exchange 2013](transport-agent-concepts-in-exchange-2013.md).</span></span>
    
- <span data-ttu-id="47098-120">传输代理类的以下程序集：</span><span class="sxs-lookup"><span data-stu-id="47098-120">The following assemblies for the transport agent classes:</span></span>
    
  - <span data-ttu-id="47098-121">Microsoft.Exchange.Data.dll</span><span class="sxs-lookup"><span data-stu-id="47098-121">Microsoft.Exchange.Data.dll</span></span>
    
  - <span data-ttu-id="47098-122">Microsoft.Exchange.Data.Common.dll</span><span class="sxs-lookup"><span data-stu-id="47098-122">Microsoft.Exchange.Data.Common.dll</span></span>
    
  - <span data-ttu-id="47098-123">Microsoft.Exchange.Transport.dll</span><span class="sxs-lookup"><span data-stu-id="47098-123">Microsoft.Exchange.Transport.dll</span></span>
    
- <span data-ttu-id="47098-124">.NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="47098-124">The .NET Framework 4.5</span></span>
    
<span data-ttu-id="47098-125">我们还建议您在安装 Visual Studio 2012。</span><span class="sxs-lookup"><span data-stu-id="47098-125">We also recommend that you install Visual Studio 2012.</span></span> <span data-ttu-id="47098-126">您可以通过使用 Visual Basic.NET 或 C# 实现传输代理。</span><span class="sxs-lookup"><span data-stu-id="47098-126">You can implement transport agents by using either Visual Basic .NET or C#.</span></span>
  
## <a name="referencing-the-assemblies"></a><span data-ttu-id="47098-127">引用程序集</span><span class="sxs-lookup"><span data-stu-id="47098-127">Referencing the assemblies</span></span>
<span data-ttu-id="47098-128"><a name="bk_ReferenceAssemblies"> </a></span><span class="sxs-lookup"><span data-stu-id="47098-128"></span></span>

<span data-ttu-id="47098-129">Exchange 2013 提供了支持 Exchange 传输行为的扩展的类的库。</span><span class="sxs-lookup"><span data-stu-id="47098-129">Exchange 2013 provides a library of classes that support the extension of Exchange transport behavior.</span></span> <span data-ttu-id="47098-130">这些类需要.NET Framework 4.5。</span><span class="sxs-lookup"><span data-stu-id="47098-130">These classes require the .NET Framework 4.5.</span></span> <span data-ttu-id="47098-131">您可以实现通过使用 Visual Studio 2012 基于这些类的传输代理。</span><span class="sxs-lookup"><span data-stu-id="47098-131">You can implement transport agents based on these classes by using Visual Studio 2012.</span></span>
  
<span data-ttu-id="47098-132">Exchange 2013 安装程序安装用于传输代理开发的程序集，并在全局程序集缓存 (GAC) 中注册它们。</span><span class="sxs-lookup"><span data-stu-id="47098-132">The Exchange 2013 installer installs assemblies that are used for transport agent development and registers them in the global assembly cache (GAC).</span></span> <span data-ttu-id="47098-133">若要开始实施传输代理，创建一个类库项目中的 Microsoft.Exchange.Data.Transport 程序集的引用。</span><span class="sxs-lookup"><span data-stu-id="47098-133">To begin implementing a transport agent, create a reference to the Microsoft.Exchange.Data.Transport assembly in a class library project.</span></span>
  
## <a name="implementing-a-transport-agent"></a><span data-ttu-id="47098-134">实现传输代理</span><span class="sxs-lookup"><span data-stu-id="47098-134">Implementing a transport agent</span></span>
<span data-ttu-id="47098-135"><a name="bk_implementationExample"> </a></span><span class="sxs-lookup"><span data-stu-id="47098-135"></span></span>

<span data-ttu-id="47098-136">下面的示例演示最小的[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)和[SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx)类派生的类的实现。</span><span class="sxs-lookup"><span data-stu-id="47098-136">The following example shows a minimal implementation of classes that derive from the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) and [SmtpReceiveAgent](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgent.aspx) classes.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="47098-137">如果多个传输代理是安装并注册相同的事件，将调用所有代理，即使一个代理从邮件项目中删除所有收件人。</span><span class="sxs-lookup"><span data-stu-id="47098-137">If multiple transport agents are installed and registered for the same event, all agents will be invoked, even if one agent removes all the recipients from a mail item.</span></span> <span data-ttu-id="47098-138">> 到避免未经处理的错误或不可预测的行为，传输代理应处理顺序邮件项目上的收件人计数等于零的情况。</span><span class="sxs-lookup"><span data-stu-id="47098-138">> To avoid unhandled errors or unpredictable behavior, your transport agent should handle cases in which the recipient count on a mail item is equal to zero.</span></span> 
  
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

## <a name="installing-and-enabling-an-agent"></a><span data-ttu-id="47098-139">安装和启用代理</span><span class="sxs-lookup"><span data-stu-id="47098-139">Installing and enabling an agent</span></span>
<span data-ttu-id="47098-140"><a name="bk_InstallEnable"> </a></span><span class="sxs-lookup"><span data-stu-id="47098-140"></span></span>

<span data-ttu-id="47098-141">编译到 DLL 您代理之后，您必须安装和开发 Exchange 服务器上启用代理。</span><span class="sxs-lookup"><span data-stu-id="47098-141">After you compile your agent to a DLL, you must install and enable the agent on your development Exchange server.</span></span> <span data-ttu-id="47098-142">在 Exchange 命令行管理程序，使用[Install-transportagent](http://technet.microsoft.com/en-us/library/aa997998.aspx) cmdlet 来安装您的代理，并使用[Enable-transportagent](http://technet.microsoft.com/en-us/library/bb124921.aspx) cmdlet 启用您的代理。</span><span class="sxs-lookup"><span data-stu-id="47098-142">In the Exchange Management Shell, use the [Install-TransportAgent](http://technet.microsoft.com/en-us/library/aa997998.aspx) cmdlet to install your agent, and the [Enable-TransportAgent](http://technet.microsoft.com/en-us/library/bb124921.aspx) cmdlet to enable your agent.</span></span> <span data-ttu-id="47098-143">有关如何使用 Exchange 命令行管理程序的信息，请参阅[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。</span><span class="sxs-lookup"><span data-stu-id="47098-143">For information about how to use the Exchange Management Shell, see [Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="47098-144">传输代理已对他们所遇到的所有电子邮件的完全访问权限。</span><span class="sxs-lookup"><span data-stu-id="47098-144">Transport agents have full access to all email messages that they encounter.</span></span> <span data-ttu-id="47098-145">Exchange 2013 不会限制传输代理的行为。</span><span class="sxs-lookup"><span data-stu-id="47098-145">Exchange 2013 does not restrict the behavior of a transport agent.</span></span> <span data-ttu-id="47098-146">传输代理不稳定或包含安全漏洞的可能影响的稳定性和 Exchange 2013 的安全性。</span><span class="sxs-lookup"><span data-stu-id="47098-146">Transport agents that are unstable or that contain security flaws might affect the stability and security of Exchange 2013.</span></span> <span data-ttu-id="47098-147">因此，您应只安装完全信任并经过充分测试传输代理。</span><span class="sxs-lookup"><span data-stu-id="47098-147">Therefore, you should only install transport agents that you fully trust and that have been fully tested.</span></span> 
  
<span data-ttu-id="47098-148">当您使用**Install-transportagent** cmdlet 安装代理时，Exchange 命令行管理程序组件上保留锁。</span><span class="sxs-lookup"><span data-stu-id="47098-148">When you use the **Install-TransportAgent** cmdlet to install an agent, the Exchange Management Shell keeps a lock on the assembly.</span></span> <span data-ttu-id="47098-149">若要解除对程序集的锁定，必须关闭 Exchange Management Shell 您用来安装代理的实例。</span><span class="sxs-lookup"><span data-stu-id="47098-149">To release the lock on the assembly, you must close the instance of the Exchange Management Shell that you used to install the agent.</span></span> <span data-ttu-id="47098-150">您将无法更新该程序集，直到解除锁定。</span><span class="sxs-lookup"><span data-stu-id="47098-150">You will be unable to update the assembly until you release the lock.</span></span> 
  
<span data-ttu-id="47098-151">下面的示例演示如何使用 Exchange 命令行管理程序来安装和启用使用从名为 MyAgents.MyAgentFactory [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)派生的类名为 MyAgent 代理。</span><span class="sxs-lookup"><span data-stu-id="47098-151">The following example shows how to use the Exchange Management Shell to install and enable an agent named MyAgent by using a class derived from [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) named MyAgents.MyAgentFactory.</span></span> 
  
 `Install-TransportAgent -Name "MyCustomAgent" -TransportAgentFactory "MyAgents.MyAgentFactory" -AssemblyPath "C:\myagents\MyAgent.dll"`
  
<span data-ttu-id="47098-152">本示例名称在其安装代理服务器上的代理 MyCustomAgent。</span><span class="sxs-lookup"><span data-stu-id="47098-152">This example names the agent MyCustomAgent on the server on which the agent is installed.</span></span> <span data-ttu-id="47098-153">下面的示例演示如何启用名为 MyCustomAgent 的代理。</span><span class="sxs-lookup"><span data-stu-id="47098-153">The following example shows how to enable the agent named MyCustomAgent.</span></span>
  
 `Enable-TransportAgent -Name "MyCustomAgent"`
  
<span data-ttu-id="47098-154">若要管理传输代理的客户端访问服务器上的前端传输服务中，为命令添加以下值： `-TransportService FrontEnd`。</span><span class="sxs-lookup"><span data-stu-id="47098-154">To manage a transport agent in the Front End Transport service on a Client Access server, add the following value to the command:  `-TransportService FrontEnd`.</span></span> <span data-ttu-id="47098-155">例如，若要查看的前端传输服务中的传输代理，运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="47098-155">For example, to view the transport agents in the Front End Transport service, run the following command.</span></span>
  
 `Get-TransportAgent -TransportService FrontEnd`
  
<span data-ttu-id="47098-156">有关安装的详细信息，启用和管理您的代理，请参阅[管理传输代理](http://technet.microsoft.com/en-us/library/bb125175%28v=exchg.150%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="47098-156">For more information about installing, enabling, and managing your agent, see [Manage Transport Agents](http://technet.microsoft.com/en-us/library/bb125175%28v=exchg.150%29.aspx).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="47098-157">本节内容</span><span class="sxs-lookup"><span data-stu-id="47098-157">In this section</span></span>
<span data-ttu-id="47098-158"><a name="bk_inthissection"> </a></span><span class="sxs-lookup"><span data-stu-id="47098-158"></span></span>

- [<span data-ttu-id="47098-159">创建 Exchange 2013 RoutingAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="47098-159">Create a RoutingAgent transport agent for Exchange 2013</span></span>](how-to-create-a-routingagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="47098-160">创建 Exchange 2013 SmtpReceiveAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="47098-160">Create an SmtpReceiveAgent transport agent for Exchange 2013</span></span>](how-to-create-an-smtpreceiveagent-transport-agent-for-exchange-2013.md)
    
- [<span data-ttu-id="47098-161">创建 Exchange 2013 DeliveryAgent 传输代理</span><span class="sxs-lookup"><span data-stu-id="47098-161">Create a DeliveryAgent transport agent for Exchange 2013</span></span>](how-to-create-a-deliveryagent-transport-agent-for-exchange-2013.md)
    
## <a name="see-also"></a><span data-ttu-id="47098-162">另请参阅</span><span class="sxs-lookup"><span data-stu-id="47098-162">See also</span></span>

- [<span data-ttu-id="47098-163">传输代理 Exchange 2013 中的概念</span><span class="sxs-lookup"><span data-stu-id="47098-163">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)   
- [<span data-ttu-id="47098-164">Exchange 2013 的传输代理引用</span><span class="sxs-lookup"><span data-stu-id="47098-164">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
    

