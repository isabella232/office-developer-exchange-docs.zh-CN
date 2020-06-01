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
description: 查找有关 Exchange 2013 中的代理 .config 和 fetagents 配置文件中的 XML 元素的信息。
ms.openlocfilehash: f19fe8316a78cef668db881e630562d3be8be64a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461567"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a><span data-ttu-id="125a8-103">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="125a8-103">Agents configuration file elements for Exchange 2013</span></span>

<span data-ttu-id="125a8-104">查找有关 Exchange 2013 中的代理 .config 和 fetagents 配置文件中的 XML 元素的信息。</span><span class="sxs-lookup"><span data-stu-id="125a8-104">Find information about the XML elements in the agents.config and fetagents.config configuration file in Exchange 2013.</span></span>
  
<span data-ttu-id="125a8-105">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="125a8-105">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="125a8-106">当您在 Exchange 服务器上安装客户端访问或邮箱服务器角色时，安装程序将创建一个 XML 文件，其中包含有关安装在服务器上的代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="125a8-106">When you install the Client Access or the Mailbox server role on an Exchange server, the installer creates an XML file that contains configuration information about agents that are installed on the server.</span></span> <span data-ttu-id="125a8-107">您不能直接写入此文件。</span><span class="sxs-lookup"><span data-stu-id="125a8-107">You cannot write directly to this file.</span></span> 
  
<span data-ttu-id="125a8-108">前端传输服务在客户端访问服务器上运行，并写入到名为 fetagents 的文件中。传输服务和邮箱传输服务在邮箱服务器上运行，并写入到名为 agent 的文件中。同时具有客户端访问服务器角色和邮箱服务器角色的计算机将同时具有 fetagents 和代理 .config 文件。</span><span class="sxs-lookup"><span data-stu-id="125a8-108">The Front End Transport service runs on Client Access servers and writes to a file named fetagents.config. The Transport service and the Mailbox Transport service run on Mailbox servers, and write to a file named agents.config. A computer that has both the Client Access server role and the Mailbox server role will have both a fetagents.config and an agents.config file.</span></span> 
  
<span data-ttu-id="125a8-109">写入这些文件的唯一受支持的方法是使用 Exchange 命令行管理程序中的传输代理 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="125a8-109">The only supported way to write to these files is by using the transport agent cmdlets in the Exchange Management Shell.</span></span> <span data-ttu-id="125a8-110">有关传输代理 cmdlet 的信息，请参阅 TechNet 上的[邮件流 cmdlet](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="125a8-110">For information about the transport agent cmdlets, see [Mail Flow Cmdlets](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) on TechNet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="125a8-111">若要区分在客户端访问服务器上扩展前端传输服务的代理和邮箱服务器上的传输服务，传输代理 cmdlet 具有一个_set-transportservice_参数，其中包含值为 "Hub" 的传输服务和前端传输服务的 "前端"。</span><span class="sxs-lookup"><span data-stu-id="125a8-111">To distinguish between agents that extend the Front End Transport service on the Client Access server and the Transport service on the Mailbox server, transport agent cmdlets have a  _TransportService_ parameter with a value of "Hub" for the Transport service and "FrontEnd" for the Front End Transport service.</span></span> 
  
<span data-ttu-id="125a8-112">您可以读取代理 .config 或 fetagents 文件，以确定服务器上的一个或多个代理的状态和配置信息。</span><span class="sxs-lookup"><span data-stu-id="125a8-112">You can read the agents.config or fetagents.config file to determine the presence of and configuration information for one or more agents on the server.</span></span> <span data-ttu-id="125a8-113">本文档提供了一个引用，可用于读取代理 .config 文件或 fetagents 中的信息。这两个文件的格式相同。</span><span class="sxs-lookup"><span data-stu-id="125a8-113">This documentation provides a reference that you can use to read the information in either the agents.config file or the fetagents.config. The format for both of these files is the same.</span></span> <span data-ttu-id="125a8-114">本文档不提供有关如何写入文件的信息。</span><span class="sxs-lookup"><span data-stu-id="125a8-114">This documentation does not provide information about how to write to the files.</span></span>
  
> [!CAUTION]
> <span data-ttu-id="125a8-115">使用不受支持的方法写入代理 .config 文件或 fetagents 可能会产生意外的结果，包括失败的传输服务或传输代理，或者两者兼有。</span><span class="sxs-lookup"><span data-stu-id="125a8-115">Using unsupported methods to write to the agents.config file or fetagents.config can produce unexpected results, including failure of the transport service or transport agents, or both.</span></span> <span data-ttu-id="125a8-116">不要直接写入这些文件中的任何一个。</span><span class="sxs-lookup"><span data-stu-id="125a8-116">Do not write directly to either of these files.</span></span> <span data-ttu-id="125a8-117">写入这些文件的唯一受支持的方法是使用 Exchange 命令行管理程序传输代理 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="125a8-117">The only supported method for writing to these files is by using the Exchange Management Shell transport agent cmdlets.</span></span> 
  
## <a name="location-of-the-transport-agent-configuration-files"></a><span data-ttu-id="125a8-118">传输代理配置文件的位置</span><span class="sxs-lookup"><span data-stu-id="125a8-118">Location of the transport agent configuration files</span></span>
<span data-ttu-id="125a8-119"><a name="bk_ConfigLoc"> </a></span><span class="sxs-lookup"><span data-stu-id="125a8-119"><a name="bk_ConfigLoc"> </a></span></span>

<span data-ttu-id="125a8-120">安装 Exchange 2013 时，安装程序将根据所安装的服务器角色创建一个名为 "fetagents" 或 "" 的 XML 文件。在 " \<ExchangeInstallFolder\> \TransportRoles\Agents" 文件夹中（其中 \<ExchangeInstallFolder\> 是您在其中安装 Exchange 2013 的文件夹）中的 "模板"。</span><span class="sxs-lookup"><span data-stu-id="125a8-120">When you install Exchange 2013, the installer creates an XML file that is named either agents.config.template or fetagents.config.template, depending on the server role installed, in the \<ExchangeInstallFolder\>\TransportRoles\Agents folder (where \<ExchangeInstallFolder\> is the folder in which you installed Exchange 2013).</span></span> <span data-ttu-id="125a8-121">如果您安装了客户端访问服务器角色，则 Exchange 2013 会将 fetagents 文件复制到 fetagents。如果安装了邮箱服务器角色，Exchange 2013 会将代理 .config 文件复制到代理 .config。当您在服务器上更改传输代理配置时，Exchange 2013 将读取并写入此文件。</span><span class="sxs-lookup"><span data-stu-id="125a8-121">If you install the Client Access server role, Exchange 2013 copies the fetagents.config.template file to fetagents.config. If you install the Mailbox server role, Exchange 2013 copies the agents.config.template file to agents.config. Exchange 2013 reads and writes this file when you change the transport agents configuration on the server.</span></span>
  
## <a name="verifying-a-transport-agent-installation"></a><span data-ttu-id="125a8-122">验证传输代理安装</span><span class="sxs-lookup"><span data-stu-id="125a8-122">Verifying a transport agent installation</span></span>
<span data-ttu-id="125a8-123"><a name="bk_verifyinstall"> </a></span><span class="sxs-lookup"><span data-stu-id="125a8-123"><a name="bk_verifyinstall"> </a></span></span>

<span data-ttu-id="125a8-124">您可以使用 .NET Framework 提供的 XML 功能来读取和验证代理 .config 或 fetagents XML 文件。</span><span class="sxs-lookup"><span data-stu-id="125a8-124">You can use the XML capabilities that the .NET Framework provides to read and validate the agents.config or the fetagents.config XML file.</span></span> <span data-ttu-id="125a8-125">若要验证传输代理的安装和配置，请阅读配置文件中的 XML，并查找与传输代理对应的[agent](agent.md)元素。</span><span class="sxs-lookup"><span data-stu-id="125a8-125">To verify the installation and configuration of a transport agent, read the XML in the configuration file and find the [agent](agent.md) element that corresponds to the transport agent.</span></span> <span data-ttu-id="125a8-126">如果特定传输代理的**代理**元素不存在，则不会安装传输代理。</span><span class="sxs-lookup"><span data-stu-id="125a8-126">If an **agent** element for the specific transport agent does not exist, the transport agent is not installed.</span></span> <span data-ttu-id="125a8-127">如果已安装传输代理，则可以读取**agent**元素的属性以确定其配置。</span><span class="sxs-lookup"><span data-stu-id="125a8-127">If the transport agent is installed, you can read the attributes of the **agent** element to determine its configuration.</span></span> 
  
## <a name="configuration-file-element-hierarchy"></a><span data-ttu-id="125a8-128">配置文件元素层次结构</span><span class="sxs-lookup"><span data-stu-id="125a8-128">Configuration file element hierarchy</span></span>
<span data-ttu-id="125a8-129"><a name="bk_elementref"> </a></span><span class="sxs-lookup"><span data-stu-id="125a8-129"><a name="bk_elementref"> </a></span></span>

<span data-ttu-id="125a8-130">以下代码显示配置 XML 文件中的元素层次结构。</span><span class="sxs-lookup"><span data-stu-id="125a8-130">The following code shows the element hierarchy in the configuration XML file.</span></span>
  
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

## <a name="in-this-section"></a><span data-ttu-id="125a8-131">本节内容</span><span class="sxs-lookup"><span data-stu-id="125a8-131">In this section</span></span>
<span data-ttu-id="125a8-132"><a name="bk_elementreflist"> </a></span><span class="sxs-lookup"><span data-stu-id="125a8-132"><a name="bk_elementreflist"> </a></span></span>

- [<span data-ttu-id="125a8-133">代理</span><span class="sxs-lookup"><span data-stu-id="125a8-133">agent</span></span>](agent.md)
    
- [<span data-ttu-id="125a8-134">agentExecution</span><span class="sxs-lookup"><span data-stu-id="125a8-134">agentExecution</span></span>](agentexecution.md)
    
- [<span data-ttu-id="125a8-135">agentList</span><span class="sxs-lookup"><span data-stu-id="125a8-135">agentList</span></span>](agentlist.md)
    
- [<span data-ttu-id="125a8-136">configuration</span><span class="sxs-lookup"><span data-stu-id="125a8-136">configuration</span></span>](configuration.md)
    
- [<span data-ttu-id="125a8-137">messageSnapshot</span><span class="sxs-lookup"><span data-stu-id="125a8-137">messageSnapshot</span></span>](messagesnapshot.md)
    
- [<span data-ttu-id="125a8-138">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="125a8-138">mexRuntime</span></span>](mexruntime.md)
    
- [<span data-ttu-id="125a8-139">监视</span><span class="sxs-lookup"><span data-stu-id="125a8-139">monitoring</span></span>](monitoring.md)
    
## <a name="see-also"></a><span data-ttu-id="125a8-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="125a8-140">See also</span></span>

- [<span data-ttu-id="125a8-141">Exchange 中的传输代理</span><span class="sxs-lookup"><span data-stu-id="125a8-141">Transport agents in Exchange</span></span>](transport-agents-in-exchange-2013.md)
- [<span data-ttu-id="125a8-142">Exchange 2013 中的传输代理概念</span><span class="sxs-lookup"><span data-stu-id="125a8-142">Transport agent concepts in Exchange 2013</span></span>](transport-agent-concepts-in-exchange-2013.md)
- [<span data-ttu-id="125a8-143">Exchange 2013 的传输代理参考</span><span class="sxs-lookup"><span data-stu-id="125a8-143">Transport agent reference for Exchange 2013</span></span>](transport-agent-reference-for-exchange-2013.md)
- [<span data-ttu-id="125a8-144">Exchange 2013 中的传输代理命名空间</span><span class="sxs-lookup"><span data-stu-id="125a8-144">Transport agent namespaces in Exchange 2013</span></span>](transport-agent-namespaces-in-exchange-2013.md)
- [<span data-ttu-id="125a8-145">邮件流 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="125a8-145">Mail Flow Cmdlets</span></span>](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

