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
# <a name="agents-configuration-file-elements-for-exchange-2013"></a>Exchange 2013 的代理配置文件元素

查找有关 Exchange 2013 中的代理 .config 和 fetagents 配置文件中的 XML 元素的信息。
  
**适用于：** Exchange Server 2013
  
当您在 Exchange 服务器上安装客户端访问或邮箱服务器角色时，安装程序将创建一个 XML 文件，其中包含有关安装在服务器上的代理的配置信息。 您不能直接写入此文件。 
  
前端传输服务在客户端访问服务器上运行，并写入到名为 fetagents 的文件中。传输服务和邮箱传输服务在邮箱服务器上运行，并写入到名为 agent 的文件中。同时具有客户端访问服务器角色和邮箱服务器角色的计算机将同时具有 fetagents 和代理 .config 文件。 
  
写入这些文件的唯一受支持的方法是使用 Exchange 命令行管理程序中的传输代理 cmdlet。 有关传输代理 cmdlet 的信息，请参阅 TechNet 上的[邮件流 cmdlet](https://technet.microsoft.com/library/aa998553%28v=exchg.150%29.aspx) 。 
  
> [!NOTE]
> 若要区分在客户端访问服务器上扩展前端传输服务的代理和邮箱服务器上的传输服务，传输代理 cmdlet 具有一个_set-transportservice_参数，其中包含值为 "Hub" 的传输服务和前端传输服务的 "前端"。 
  
您可以读取代理 .config 或 fetagents 文件，以确定服务器上的一个或多个代理的状态和配置信息。 本文档提供了一个引用，可用于读取代理 .config 文件或 fetagents 中的信息。这两个文件的格式相同。 本文档不提供有关如何写入文件的信息。
  
> [!CAUTION]
> 使用不受支持的方法写入代理 .config 文件或 fetagents 可能会产生意外的结果，包括失败的传输服务或传输代理，或者两者兼有。 不要直接写入这些文件中的任何一个。 写入这些文件的唯一受支持的方法是使用 Exchange 命令行管理程序传输代理 cmdlet。 
  
## <a name="location-of-the-transport-agent-configuration-files"></a>传输代理配置文件的位置
<a name="bk_ConfigLoc"> </a>

安装 Exchange 2013 时，安装程序将根据所安装的服务器角色创建一个名为 "fetagents" 或 "" 的 XML 文件。在 " \<ExchangeInstallFolder\> \TransportRoles\Agents" 文件夹中（其中 \<ExchangeInstallFolder\> 是您在其中安装 Exchange 2013 的文件夹）中的 "模板"。 如果您安装了客户端访问服务器角色，则 Exchange 2013 会将 fetagents 文件复制到 fetagents。如果安装了邮箱服务器角色，Exchange 2013 会将代理 .config 文件复制到代理 .config。当您在服务器上更改传输代理配置时，Exchange 2013 将读取并写入此文件。
  
## <a name="verifying-a-transport-agent-installation"></a>验证传输代理安装
<a name="bk_verifyinstall"> </a>

您可以使用 .NET Framework 提供的 XML 功能来读取和验证代理 .config 或 fetagents XML 文件。 若要验证传输代理的安装和配置，请阅读配置文件中的 XML，并查找与传输代理对应的[agent](agent.md)元素。 如果特定传输代理的**代理**元素不存在，则不会安装传输代理。 如果已安装传输代理，则可以读取**agent**元素的属性以确定其配置。 
  
## <a name="configuration-file-element-hierarchy"></a>配置文件元素层次结构
<a name="bk_elementref"> </a>

以下代码显示配置 XML 文件中的元素层次结构。
  
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
    
- [监视](monitoring.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 中的传输代理](transport-agents-in-exchange-2013.md)
- [Exchange 2013 中的传输代理概念](transport-agent-concepts-in-exchange-2013.md)
- [Exchange 2013 的传输代理参考](transport-agent-reference-for-exchange-2013.md)
- [Exchange 2013 中的传输代理命名空间](transport-agent-namespaces-in-exchange-2013.md)
- [邮件流 Cmdlet](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)
    

