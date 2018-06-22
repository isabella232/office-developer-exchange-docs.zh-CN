---
title: Exchange Management Shell
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: 查找有关如何使用 Exchange 命令行管理程序来开发用于 Exchange server 管理工具的信息。
ms.openlocfilehash: 1cb0328bdb0eebda0ce4eda929e1bfb21be451f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753022"
---
# <a name="exchange-management-shell"></a>Exchange Management Shell

查找有关如何使用 Exchange 命令行管理程序来开发用于 Exchange server 管理工具的信息。
  
**适用于：** Exchange Online |Exchange Server 2013 |Office 365
  
Exchange 命令行管理程序提供了一组丰富的命令，基于 Windows PowerShell 平台，用于管理 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 的内部部署版本开头 Exchange 2013。 您可以使用 Exchange 命令行管理程序创建两种工具： 在 Windows PowerShell 环境中内, 工作的命令行脚本和工具的托管接口通过使用 Exchange 命令行管理程序 cmdlet。 托管应用程序可用于创建标准的 Windows 或基于 web 的用户界面来管理 Exchange 服务器。 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>您需要了解的有关 Exchange 命令行管理程序

|如果您想知道有关|请参阅这个|
|:-----|:-----|
|可用性  <br/> |Exchange 命令行管理程序命令安装在运行 Exchange 启动与 Exchange 2007 版本的所有服务器上。<br/>可以在运行 Windows PowerShell 2.0 的任何计算机上部署客户端应用程序。<br/> 有关访问命令行管理程序的信息，请参阅[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。  <br/> |
|语言和工具  <br/> |您可以在任何文本编辑器创建 Exchange 命令行管理程序脚本。<br/>您可以使用许多第三方工具之一创建可与 Exchange 命令行管理程序的 Windows PowerShell 脚本。  <br/> [Exchange 命令行管理程序对象模型](exchange-management-shell-namespaces.md)基于.NET Framework。<br/>您可以使用任何.NET 语言开发 Exchange 命令行管理程序应用程序。  <br/> |
|可用测试和调试工具  <br/> |您可以使用许多第三方应用程序之一测试和调试 Exchange 命令行管理程序脚本。  <br/> 您可以使用 Visual Studio 和第三方工具进行测试和调试托管 Exchange 命令行管理程序应用程序。  <br/> |
|服务器平台要求  <br/> |您可以使用 Exchange 命令行管理程序上已安装的 Windows PowerShell 2.0 任何 Exchange 服务器。  <br/> |
|客户端平台要求  <br/> |Exchange 命令行管理程序客户端应用程序需要 Windows PowerShell 2.0。  <br/> |
|权限  <br/> |运行 Exchange 命令行管理程序应用程序要求用户在 Exchange 存储上具有对受影响的数据的基于角色的访问控制权限。<br/>有关基于角色的访问控制的详细信息，请参阅[Understanding Role Based Access Control](http://technet.microsoft.com/en-us/library/dd298183.aspx)。  <br/> |
   
本节中的文章介绍了用于创建 Exchange 管理工具重要的 Exchange 命令行管理程序功能。 有关规划、 配置或维护 Exchange 的信息，请参阅[Exchange](https://docs.microsoft.com/en-us/exchange/)站点。
  
## <a name="in-this-section"></a>本节内容

- [创建 Exchange 命令行管理程序工具](create-exchange-management-shell-tools.md)
    
- [Exchange 命令行管理程序命名空间](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>另请参阅
  
- [Windows PowerShell 文档](https://docs.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [PowerShell 脚本](https://docs.microsoft.com/en-us/powershell/scripting/powershell-scripting?view=powershell-6)
    

