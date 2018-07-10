---
title: Exchange 2013 的代理配置文件元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Agents
api_type:
- schema
ms.assetid: 3047653b-d712-46c1-ae0a-73f3975f5e9d
description: Exchange 2013 中的 agents.config 和 fetagents.config 配置文件中查找信息的 XML 元素。
ms.openlocfilehash: dd58c4bc21a968db2ca5b13e0c53f7058b29f233
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753062"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a><span data-ttu-id="3a6bf-103">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="3a6bf-103">Agents configuration file elements for Exchange 2013</span></span>

<span data-ttu-id="3a6bf-104">Exchange 2013 中的 agents.config 和 fetagents.config 配置文件中查找信息的 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-104">Find information about the XML elements in the agents.config and fetagents.config configuration file in Exchange 2013.</span></span>
  
<span data-ttu-id="3a6bf-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="3a6bf-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="3a6bf-106">在客户端访问或邮箱服务器角色安装在 Exchange 服务器上时，安装程序将创建 XML 文件包含有关服务器安装的代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-106">When you install the Client Access or the Mailbox server role on an Exchange server, the installer creates an XML file that contains configuration information about agents that are installed on the server.</span></span> <span data-ttu-id="3a6bf-107">您不能直接写入此文件。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-107">You cannot write directly to this file.</span></span> 
  
<span data-ttu-id="3a6bf-108">前端传输服务客户端访问服务器上运行，并将写入到一个名为 fetagents.config 文件。传输服务和邮箱传输服务在邮箱服务器上运行并写入到一个名为 agents.config 文件。Fetagents.config 和 agents.config 文件将具有已客户端访问服务器角色和邮箱服务器角色的计算机。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-108">The Front End Transport service runs on Client Access servers and writes to a file named fetagents.config. The Transport service and the Mailbox Transport service run on Mailbox servers, and write to a file named agents.config. A computer that has both the Client Access server role and the Mailbox server role will have both a fetagents.config and an agents.config file.</span></span> 
  
<span data-ttu-id="3a6bf-109">写入这些文件的唯一受支持的方法是在 Exchange 命令行管理程序中使用的传输代理 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-109">The only supported way to write to these files is by using the transport agent cmdlets in the Exchange Management Shell.</span></span> <span data-ttu-id="3a6bf-110">有关传输代理 cmdlet 的信息，请参阅 TechNet 上的[邮件流 Cmdlet](http://technet.microsoft.com/zh-cn/library/aa998553%28v=exchg.150%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-110">For information about the transport agent cmdlets, see [Mail Flow Cmdlets](http://technet.microsoft.com/zh-cn/library/aa998553%28v=exchg.150%29.aspx) on TechNet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3a6bf-111">为了区别扩展的客户端访问服务器上的前端传输服务的代理和邮箱服务器上的传输服务，请传输代理 cmdlet 具有_TransportService_参数值为"集线器"传输服务和前端传输服务的"前端"。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-111">To distinguish between agents that extend the Front End Transport service on the Client Access server and the Transport service on the Mailbox server, transport agent cmdlets have a  _TransportService_ parameter with a value of "Hub" for the Transport service and "FrontEnd" for the Front End Transport service.</span></span> 
  
<span data-ttu-id="3a6bf-112">您可以阅读 agents.config 或 fetagents.config 文件，以确定存在和一个或多个代理服务器上的配置信息。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-112">You can read the agents.config or fetagents.config file to determine the presence of and configuration information for one or more agents on the server.</span></span> <span data-ttu-id="3a6bf-113">本文档提供可用于读取 agents.config 文件或 fetagents.config 中的信息的引用。这两个这些文件的格式是相同的。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-113">This documentation provides a reference that you can use to read the information in either the agents.config file or the fetagents.config. The format for both of these files is the same.</span></span> <span data-ttu-id="3a6bf-114">本文档并未提供有关如何编写对文件的信息。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-114">This documentation does not provide information about how to write to the files.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="3a6bf-115">使用不受支持的方法写入 agents.config 文件或 fetagents.config 可能会产生意外的结果，包括失败的传输服务或传输代理。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-115">Using unsupported methods to write to the agents.config file or fetagents.config can produce unexpected results, including failure of the transport service or transport agents, or both.</span></span> <span data-ttu-id="3a6bf-116">不写入直接对这些文件。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-116">Do not write directly to either of these files.</span></span> <span data-ttu-id="3a6bf-117">使用 Exchange 命令行管理程序传输代理 cmdlet 用于向这些文件写入仅受支持的方法。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-117">The only supported method for writing to these files is by using the Exchange Management Shell transport agent cmdlets.</span></span> 
  
## <a name="location-of-the-transport-agent-configuration-files"></a><span data-ttu-id="3a6bf-118">传输代理配置文件的位置</span><span class="sxs-lookup"><span data-stu-id="3a6bf-118">Location of the transport agent configuration files</span></span>
<span data-ttu-id="3a6bf-119"><a name="bk_ConfigLoc"> </a></span><span class="sxs-lookup"><span data-stu-id="3a6bf-119"></span></span>

<span data-ttu-id="3a6bf-120">安装 Exchange 2013 时，安装程序创建的 XML 文件的 agents.config.template 或 fetagents.config.template，具体取决于服务器角色安装，在名为\<ExchangeInstallFolder\>\TransportRoles\Agents文件夹 (其中\<ExchangeInstallFolder\>是您安装 Exchange 2013 的文件夹)。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-120">When you install Exchange 2013, the installer creates an XML file that is named either agents.config.template or fetagents.config.template, depending on the server role installed, in the \<ExchangeInstallFolder\>\TransportRoles\Agents folder (where \<ExchangeInstallFolder\> is the folder in which you installed Exchange 2013).</span></span> <span data-ttu-id="3a6bf-121">如果安装了客户端访问服务器角色，Exchange 2013 fetagents.config.template 文件复制到 fetagents.config。如果您安装邮箱服务器角色，Exchange 2013 agents.config.template 文件复制到 agents.config。Exchange 2013 读取和写入此文件，当您更改在服务器上的传输代理配置。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-121">If you install the Client Access server role, Exchange 2013 copies the fetagents.config.template file to fetagents.config. If you install the Mailbox server role, Exchange 2013 copies the agents.config.template file to agents.config. Exchange 2013 reads and writes this file when you change the transport agents configuration on the server.</span></span>
  
## <a name="verifying-a-transport-agent-installation"></a><span data-ttu-id="3a6bf-122">验证传输代理安装</span><span class="sxs-lookup"><span data-stu-id="3a6bf-122">Verifying a transport agent installation</span></span>
<span data-ttu-id="3a6bf-123"><a name="bk_verifyinstall"> </a></span><span class="sxs-lookup"><span data-stu-id="3a6bf-123"></span></span>

<span data-ttu-id="3a6bf-124">您可以使用.NET Framework 提供读取和验证 agents.config 或 fetagents.config XML 文件的 XML 功能。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-124">You can use the XML capabilities that the .NET Framework provides to read and validate the agents.config or the fetagents.config XML file.</span></span> <span data-ttu-id="3a6bf-125">若要验证的安装和配置的传输代理，读取 XML 配置文件中的，并找到对应于传输代理的[代理](agent.md)元素。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-125">To verify the installation and configuration of a transport agent, read the XML in the configuration file and find the [agent](agent.md) element that corresponds to the transport agent.</span></span> <span data-ttu-id="3a6bf-126">特定传输代理**代理**元素不存在，如果未安装传输代理。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-126">If an **agent** element for the specific transport agent does not exist, the transport agent is not installed.</span></span> <span data-ttu-id="3a6bf-127">如果安装了传输代理，您可以阅读**代理**元素以确定其配置的属性。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-127">If the transport agent is installed, you can read the attributes of the **agent** element to determine its configuration.</span></span> 
  
## <a name="configuration-file-element-hierarchy"></a><span data-ttu-id="3a6bf-128">配置文件的元素层次结构</span><span class="sxs-lookup"><span data-stu-id="3a6bf-128">Configuration file element hierarchy</span></span>
<span data-ttu-id="3a6bf-129"><a name="bk_elementref"> </a></span><span class="sxs-lookup"><span data-stu-id="3a6bf-129"></span></span>

<span data-ttu-id="3a6bf-130">下面的代码演示配置 XML 文件中的元素层次结构。</span><span class="sxs-lookup"><span data-stu-id="3a6bf-130">The following code shows the element hierarchy in the configuration XML file.</span></span>
  
```XML
<configuration>
    <mexRuntime>
        <monitoring>
            <agentExecution/>
            <messageSnapshot/>
        </monitoring>
        <agentList>
            <agent/>
            <agent/>
            <agent />
        </agentList>
    </mexRuntim>
</configuration>
```

## <a name="in-this-section"></a><span data-ttu-id="3a6bf-131">本节内容</span><span class="sxs-lookup"><span data-stu-id="3a6bf-131">In this section</span></span>
<span data-ttu-id="3a6bf-132"><a name="bk_elementreflist"> </a></span><span class="sxs-lookup"><span data-stu-id="3a6bf-132"></span></span>

- [<span data-ttu-id="3a6bf-133">代理</span><span class="sxs-lookup"><span data-stu-id="3a6bf-133">agent</span></span>](agent.md)
    
- [<span data-ttu-id="3a6bf-134">agentExecution</span><span class="sxs-lookup"><span data-stu-id="3a6bf-134">agentExecution</span></span>](agentexecution.md)
    
- [<span data-ttu-id="3a6bf-135">agentList</span><span class="sxs-lookup"><span data-stu-id="3a6bf-135">agentList</span></span>](agentlist.md)
    
- [<span data-ttu-id="3a6bf-136">configuration</span><span class="sxs-lookup"><span data-stu-id="3a6bf-136">configuration</span></span>](configuration.md)
    
- [<span data-ttu-id="3a6bf-137">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="3a6bf-137">messageSnapshot</span></span>](messagesnapshot.md)
    
- [<span data-ttu-id="3a6bf-138">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="3a6bf-138">mexRuntime</span></span>](mexruntime.md)
    
- [<span data-ttu-id="3a6bf-139">监控</span><span class="sxs-lookup"><span data-stu-id="3a6bf-139">monitoring</span></span>](monitoring.md)
    
## <a name="see-also"></a><span data-ttu-id="3a6bf-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a6bf-140">See also</span></span>

- [<span data-ttu-id="3a6bf-141">在 Exchange 传输代理</span><span class="sxs-lookup"><span data-stu-id="3a6bf-141">Transport agents in Exchange</span></span>](transport-agents-in-exchange-2013.md)
- [<span data-ttu-id="3a6bf-142">传输代理 Exchange 2013 中的概念</span><span class="sxs-lookup"><span data-stu-id="3a6bf-142">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="3a6bf-143">Exchange 2013 的传输代理引用</span><span class="sxs-lookup"><span data-stu-id="3a6bf-143">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
- [<span data-ttu-id="3a6bf-144">传输代理 Exchange 2013 中的命名空间</span><span class="sxs-lookup"><span data-stu-id="3a6bf-144">Transport agent namespaces in Exchange 2013</span></span>](transport-agent-namespaces-in-exchange-2013.md)
- [<span data-ttu-id="3a6bf-145">邮件流 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3a6bf-145">Mail Flow Cmdlets</span></span>](https://docs.microsoft.com/zh-cn/powershell/exchange/?view=exchange-ps)
    

