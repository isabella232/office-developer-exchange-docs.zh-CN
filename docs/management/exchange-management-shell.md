---
title: Exchange 命令行管理程序
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: 查找有关如何使用 Exchange 命令行管理程序开发 Exchange server 管理工具的信息。
ms.openlocfilehash: 38e75339a4ad97cf8ff99e1cbe9c01059e157941
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44435805"
---
# <a name="exchange-management-shell"></a>Exchange 命令行管理程序

查找有关如何使用 Exchange 命令行管理程序开发 Exchange server 管理工具的信息。
  
**适用于：** Exchange Online |Exchange Server 2013 |Office 365
  
Exchange 命令行管理程序基于 Windows PowerShell 平台提供了一组丰富的命令，用于管理 Exchange Online、作为 Office 365 的一部分的 Exchange Online 或从 Exchange 2013 开始的 Exchange 内部部署版本。 您可以使用 Exchange 命令行管理程序创建两种类型的工具：在 Windows PowerShell 环境中工作的命令行脚本，以及通过托管接口使用 Exchange 命令行管理程序 cmdlet 的工具。 您可以使用托管应用程序创建标准的 Windows 或基于 web 的 UI 来管理 Exchange 服务器。 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>您需要了解的有关 Exchange 命令行管理程序的信息

|如果你想要了解|请参阅这个|
|:-----|:-----|
|供应情况  <br/> |Exchange 命令行管理程序命令安装在所有运行 Exchange 版本（以 Exchange 2007 开头）的服务器上。<br/>客户端应用程序可以部署在运行 Windows PowerShell 2.0 的任何计算机上。<br/> 有关访问命令行管理程序的信息，请参阅[Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。  <br/> |
|语言和工具  <br/> |您可以在任何文本编辑器中创建 Exchange 命令行管理程序脚本。<br/>您可以使用许多第三方工具之一来创建可用于 Exchange 命令行管理程序的 Windows PowerShell 脚本。  <br/> [Exchange 命令行管理程序对象模型](exchange-management-shell-namespaces.md)基于 .net Framework。<br/>可以使用任何 .NET 语言开发 Exchange 命令行管理程序应用程序。  <br/> |
|可用测试和调试工具  <br/> |您可以使用许多第三方应用程序之一来测试和调试 Exchange 命令行管理程序脚本。  <br/> 您可以使用 Visual Studio 和第三方工具来测试和调试托管 Exchange 命令行管理程序应用程序。  <br/> |
|服务器平台要求  <br/> |您可以在安装了 Windows PowerShell 2.0 的任何 Exchange 服务器上使用 Exchange 命令行管理程序。  <br/> |
|客户端平台要求  <br/> |Exchange 命令行管理程序客户端应用程序需要 Windows PowerShell 2.0。  <br/> |
|Permissions  <br/> |运行 Exchange 命令行管理程序应用程序要求用户对 Exchange 存储上受影响的数据具有基于角色的访问控制权限。<br/>有关基于角色的访问控制的详细信息，请参阅[了解基于角色的访问控制](https://technet.microsoft.com/library/dd298183.aspx)。  <br/> |
   
本节中的文章介绍了 Exchange 命令行管理程序功能，对于创建 Exchange 管理工具来说非常重要。 有关规划、配置或维护 Exchange 的信息，请参阅[exchange](https://docs.microsoft.com/exchange/)网站。
  
## <a name="in-this-section"></a>本节内容

- [创建 Exchange 命令行管理程序工具](create-exchange-management-shell-tools.md)
    
- [Exchange 命令行管理程序命名空间](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>另请参阅
  
- [Windows PowerShell 文档](https://docs.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [PowerShell 脚本](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6)
    

