---
title: 使用 EWS 在 Exchange 管理用户访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: 了解用于管理用户帐户访问您的 Exchange 服务器，您的选项。
ms.openlocfilehash: d93f521f08f93b44b4ecc1f258b03ed24ebdd3dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752915"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a>使用 EWS 在 Exchange 管理用户访问

了解用于管理用户帐户访问您的 Exchange 服务器，您的选项。
  
Exchange Web Services (EWS) 和 EWS 托管 API 提供有限的操作的可用来管理 Exchange Online、 Exchange Online 作为 Office 365 的一部分或的开头 Exchange 2013 的 Exchange 版本上的帐户。 管理委派并设置其他帐户的文件夹的访问权限，可以使用下面的图中所示的操作。 
  
**委托和文件夹访问 EWS 操作**

![EWS 用户管理选项。](media/Exchange_ManagingUserAccess_1.png)
  
如果您的应用程序需要其他控制 Exchange 服务器上的帐户，您可以使用 Exchange 命令行管理程序 cmdlet 管理帐户。 您可以通过执行以下某项操作来呼叫的 Exchange 命令行管理程序 cmdlet:
  
- 编写使用 C# 或 Visual Basic 调用的 Exchange 命令行管理程序 cmdlet 的应用程序。 您可以查看[Exchange Management Shell API 文档](../management/exchange-management-shell.md)，以了解如何调用 cmdlet 中的示例代码。 
    
- 使用 Windows PowerShell 和 Windows PowerShell 脚本呼叫 Exchange Management Shell cmdlet。 您可以找到[Exchange Server PowerShell (Exchange Management Shell)](https://docs.microsoft.com/en-us/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)，以及介绍如何使用它们的示例的完整列表。 
    
## <a name="see-also"></a>另请参阅

- [EWS 应用程序设置](setting-up-your-ews-application.md)   
- [Exchange 2013 Cmdlet](https://docs.microsoft.com/en-us/powershell/exchange/?view=exchange-ps)  
    

