---
title: Exchange 命令行管理程序
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8cc0c4fa-9e13-45cb-88da-0486f2ac1bd0
description: 查找有关如何使用命令行管理Exchange程序开发用于管理Exchange的信息。
ms.openlocfilehash: ee1cbcb174c7153ca6cd9bb089580b372bf9029b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516150"
---
# <a name="exchange-management-shell"></a>Exchange 命令行管理程序

查找有关如何使用命令行管理Exchange程序开发用于管理Exchange的信息。
  
**适用于：Exchange Online |** Exchange Server 2013 |Office 365
  
Exchange 命令行管理程序基于 Windows PowerShell 平台提供了一组丰富的命令，用于管理 Exchange Online、Exchange Online 作为 Office 365 的一部分或本地版本的 Exchange（从Exchange 2013 年。 可以使用 Exchange 命令行管理程序 创建两种类型的工具：在 Windows PowerShell 环境中工作的命令行脚本，以及通过托管接口使用 Exchange 命令行管理程序 cmdlet 的工具。 您可以使用托管应用程序创建标准Windows或基于 Web 的 UI 来管理 Exchange 服务器。 
  
## <a name="what-you-need-to-know-about-the-exchange-management-shell"></a>有关命令行管理程序Exchange内容

|如果想知道|请参阅这个|
|:-----|:-----|
|可用性  <br/> |Exchange命令行管理程序命令安装在从 2007 Exchange 2007 Exchange所有服务器上。<br/>客户端应用程序可以部署在运行 Windows PowerShell 2.0 的任何计算机上。<br/> 有关访问命令行管理程序的信息，请参阅 Exchange Server [PowerShell (Exchange Management Shell) ](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)。  <br/> |
|语言和工具  <br/> |可以在任何文本Exchange创建命令行管理程序脚本。<br/>可以使用许多第三方工具之一创建Windows PowerShell命令行管理程序Exchange脚本。  <br/> 命令行[Exchange程序对象模型](exchange-management-shell-namespaces.md)基于.NET Framework。<br/>可以使用任何 .NET 语言来开发Exchange命令行管理程序应用程序。  <br/> |
|可用测试和调试工具  <br/> |可以使用许多第三方应用程序之一来测试和调试命令行Exchange脚本。  <br/> 可以使用命令行Visual Studio第三方工具来测试和调试命令行管理程序Exchange托管应用程序。  <br/> |
|服务器平台要求  <br/> |可以在安装了 Exchange 2.0 的任何 Exchange 服务器上使用 Windows PowerShell 命令行管理程序。  <br/> |
|客户端平台要求  <br/> |Exchange命令行管理程序客户端应用程序Windows PowerShell 2.0。  <br/> |
|Permissions  <br/> |运行Exchange命令行管理程序应用程序需要用户对命令行管理程序存储上受影响的数据具有基于角色Exchange权限。<br/>有关基于角色的访问控制详细信息，请参阅 [了解基于角色的访问控制](https://technet.microsoft.com/library/dd298183.aspx)。  <br/> |
   
本节中的文章介绍Exchange管理工具的命令行管理程序Exchange功能。 有关规划、配置或维护Exchange，请参阅[Exchange网站。](https://docs.microsoft.com/exchange/)
  
## <a name="in-this-section"></a>本节内容

- [创建 Exchange 命令行管理程序工具](create-exchange-management-shell-tools.md)
    
- [Exchange 命令行管理程序命名空间](exchange-management-shell-namespaces.md)
    
## <a name="see-also"></a>另请参阅
  
- [Windows PowerShell文档](https://docs.microsoft.com/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-6)
- [PowerShell 脚本](https://docs.microsoft.com/powershell/scripting/powershell-scripting?view=powershell-6)
    

