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
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Exchange 2013 的代理配置文件元素

Exchange 2013 中的 agents.config 和 fetagents.config 配置文件中查找信息的 XML 元素。
  
**适用于：** Exchange Server 2013
  
在客户端访问或邮箱服务器角色安装在 Exchange 服务器上时，安装程序将创建 XML 文件包含有关服务器安装的代理的配置信息。 您不能直接写入此文件。 
  
前端传输服务客户端访问服务器上运行，并将写入到一个名为 fetagents.config 文件。传输服务和邮箱传输服务在邮箱服务器上运行并写入到一个名为 agents.config 文件。Fetagents.config 和 agents.config 文件将具有已客户端访问服务器角色和邮箱服务器角色的计算机。 
  
写入这些文件的唯一受支持的方法是在 Exchange 命令行管理程序中使用的传输代理 cmdlet。 有关传输代理 cmdlet 的信息，请参阅 TechNet 上的[邮件流 Cmdlet](http://technet.microsoft.com/en-us/library/aa998553%28v=exchg.150%29.aspx) 。 
  
> [!NOTE]
> 为了区别扩展的客户端访问服务器上的前端传输服务的代理和邮箱服务器上的传输服务，请传输代理 cmdlet 具有_TransportService_参数值为"集线器"传输服务和前端传输服务的"前端"。 
  
您可以阅读 agents.config 或 fetagents.config 文件，以确定存在和一个或多个代理服务器上的配置信息。 本文档提供可用于读取 agents.config 文件或 fetagents.config 中的信息的引用。这两个这些文件的格式是相同的。 本文档并未提供有关如何编写对文件的信息。
  
> [!CAUTION]
> 使用不受支持的方法写入 agents.config 文件或 fetagents.config 可能会产生意外的结果，包括失败的传输服务或传输代理。 不写入直接对这些文件。 使用 Exchange 命令行管理程序传输代理 cmdlet 用于向这些文件写入仅受支持的方法。 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>传输代理配置文件的位置
<a name="bk_ConfigLoc"> </a>

安装 Exchange 2013 时，安装程序创建的 XML 文件的 agents.config.template 或 fetagents.config.template，具体取决于服务器角色安装，在名为\<ExchangeInstallFolder\>\TransportRoles\Agents文件夹 (其中\<ExchangeInstallFolder\>是您安装 Exchange 2013 的文件夹)。 如果安装了客户端访问服务器角色，Exchange 2013 fetagents.config.template 文件复制到 fetagents.config。如果您安装邮箱服务器角色，Exchange 2013 agents.config.template 文件复制到 agents.config。Exchange 2013 读取和写入此文件，当您更改在服务器上的传输代理配置。
  
## <a name="verifying-a-transport-agent-installation"></a>验证传输代理安装
<a name="bk_verifyinstall"> </a>

您可以使用.NET Framework 提供读取和验证 agents.config 或 fetagents.config XML 文件的 XML 功能。 若要验证的安装和配置的传输代理，读取 XML 配置文件中的，并找到对应于传输代理的[代理](agent.md)元素。 特定传输代理**代理**元素不存在，如果未安装传输代理。 如果安装了传输代理，您可以阅读**代理**元素以确定其配置的属性。 
  
## <a name="configuration-file-element-hierarchy"></a>配置文件的元素层次结构
<a name="bk_elementref"> </a>

下面的代码演示配置 XML 文件中的元素层次结构。
  
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

## <a name="in-this-section"></a>本节内容
<a name="bk_elementreflist"> </a>

- [代理](agent.md)
    
- [agentExecution](agentexecution.md)
    
- [agentList](agentlist.md)
    
- [configuration](configuration.md)
    
- [messageSnapshot](messagesnapshot.md)
    
- [mexRuntime](mexruntime.md)
    
- [监控](monitoring.md)
    
## <a name="see-also"></a>另请参阅

- [在 Exchange 传输代理](transport-agents-in-exchange-2013.md)
- [传输代理 Exchange 2013 中的概念](transport-agent-concepts-in-exchange-2013.md)
- [Exchange 2013 的传输代理引用](transport-agent-reference-for-exchange-2013.md)
- [传输代理 Exchange 2013 中的命名空间](transport-agent-namespaces-in-exchange-2013.md)
- [邮件流 Cmdlet](https://docs.microsoft.com/en-us/powershell/exchange/?view=exchange-ps)
    

