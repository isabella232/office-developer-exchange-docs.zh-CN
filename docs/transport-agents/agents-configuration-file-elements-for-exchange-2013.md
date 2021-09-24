---
title: Exchange 2013 的代理配置文件元素
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Agents
api_type:
- schema
ms.assetid: 3047653b-d712-46c1-ae0a-73f3975f5e9d
description: 查找有关 2013 年 agents.config 和 fetagents.config 配置文件Exchange XML 元素的信息。
ms.openlocfilehash: bdf394130f7818c5b956e8b15eed86a6318b9698
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510419"
---
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Exchange 2013 的代理配置文件元素

查找有关 2013 年 agents.config 和 fetagents.config 配置文件Exchange XML 元素的信息。
  
**适用于：Exchange Server** 2013
  
当您在 Exchange 服务器上安装客户端访问或邮箱服务器角色时，安装程序会创建一个 XML 文件，其中包含有关服务器上安装的代理的配置信息。 不能直接写入此文件。 
  
前端传输服务在客户端访问服务器上运行，并写入名为 fetagents.config。传输服务和邮箱传输服务在邮箱服务器上运行，并写入名为 agents.config。同时具有客户端访问服务器角色和邮箱服务器角色的计算机将具有 fetagents.config 和 agents.config 文件。 
  
写入这些文件的唯一受支持的方法就是使用命令行管理程序中的传输Exchange cmdlet。 有关传输代理 cmdlet 的信息，请参阅 TechNet[上的邮件Flow Cmdlet。](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) 
  
> [!NOTE]
> 为了区分在客户端访问服务器上扩展前端传输服务的代理和邮箱服务器上传输服务的代理，传输代理 cmdlet 的  _TransportService_ 参数的值为"Hub"，而前端传输服务的值为"FrontEnd"。 
  
可以读取 agents.config 或 fetagents.config 文件，以确定服务器上是否存在一个或多个代理以及配置信息。 本文档提供了一个参考，您可以使用该参考来读取文档或agents.config文件中fetagents.config。这两个文件的格式相同。 本文档不提供如何写入文件的信息。
  
> [!CAUTION]
> 使用不受支持的方法写入agents.config或fetagents.config可能会产生意外结果，包括传输服务或传输代理失败，或同时出现这两种结果。 不要直接写入其中任一文件。 写入这些文件的唯一受支持方法是使用 Exchange 命令行管理程序传输代理 cmdlet。 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>传输代理配置文件的位置
<a name="bk_ConfigLoc"> </a>

安装 Exchange 2013 时，安装程序会创建一个名为 agents.config.template 或 fetagents.config.template 的 XML 文件，该文件位于 \TransportRoles\Agents 文件夹 (其中是安装 \<ExchangeInstallFolder\> Exchange 2013) 的文件夹，具体取决于安装的服务器角色。 \<ExchangeInstallFolder\> 如果安装客户端访问服务器角色，Exchange 2013 将 fetagents.config.template 文件复制到fetagents.config。如果安装邮箱服务器角色，Exchange 2013 将 agents.config.template 文件复制到agents.config。Exchange更改服务器上传输代理配置时，2013 会读取和写入此文件。
  
## <a name="verifying-a-transport-agent-installation"></a>验证传输代理安装
<a name="bk_verifyinstall"> </a>

您可以使用应用程序提供的 XML 功能.NET Framework读取和验证 agents.config 或 fetagents.config XML 文件。 若要验证传输代理的安装和配置，请阅读配置文件中的 XML 并查找与传输代理对应的代理[](agent.md)元素。 如果 **特定** 传输代理的代理元素不存在，则不安装传输代理。 如果安装了传输代理，您可以读取 **代理** 元素的属性以确定其配置。 
  
## <a name="configuration-file-element-hierarchy"></a>配置文件元素层次结构
<a name="bk_elementref"> </a>

以下代码显示了配置 XML 文件的元素层次结构。
  
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

- [agent](agent.md)
    
- [agentExecution](agentexecution.md)
    
- [agentList](agentlist.md)
    
- [configuration](configuration.md)
    
- [messageSnapshot](messagesnapshot.md)
    
- [mexRuntime](mexruntime.md)
    
- [监视](monitoring.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 中的传输代理](transport-agents-in-exchange-2013.md)
- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)
- [Exchange 2013 中的传输代理命名空间](transport-agent-namespaces-in-exchange-2013.md)
- [邮件Flow Cmdlet](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

