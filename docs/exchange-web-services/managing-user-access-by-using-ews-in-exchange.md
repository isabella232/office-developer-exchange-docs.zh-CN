---
title: 使用 EWS 管理用户对Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: 了解管理用户帐户对 Exchange 服务器的访问权限的选项。
ms.openlocfilehash: 431f61a0cbdfcc522eb1481399ffab1f31df9e62
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520974"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a>使用 EWS 管理用户对Exchange

了解管理用户帐户对 Exchange 服务器的访问权限的选项。
  
ExchangeWeb 服务 (EWS) 和 EWS 托管 API 提供有限数量的操作，可用于管理 Exchange Online 上的帐户、Exchange Online 作为 Office 365 的一部分或 Exchange 版本（从 Exchange 2013 开始）。 可以使用下图中显示的操作来管理代理并设置其他帐户的文件夹访问权限。 
  
**用于委派和文件夹访问的 EWS 操作**

![EWS 用户管理选项。](media/Exchange_ManagingUserAccess_1.png)
  
如果应用程序需要额外控制 Exchange 上的帐户，可以使用 Exchange 命令行管理程序 cmdlet 管理帐户。 可以通过执行以下操作Exchange调用命令行管理程序 cmdlet：
  
- 使用调用命令行C# cmdlet Visual Basic或Exchange编写应用程序。 你可以查看命令行管理程序 API 文档中Exchange[代码](../management/exchange-management-shell.md)，了解如何调用 cmdlet。 
    
- 使用 Windows PowerShell 和 Windows PowerShell 脚本调用 Exchange 命令行管理程序 cmdlet。 你可以找到[PowerShell ](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)Exchange Server命令行管理 (Exchange的完整) ，以及显示如何使用它们的示例。 
    
## <a name="see-also"></a>另请参阅

- [设置 EWS 应用程序](setting-up-your-ews-application.md)   
- [Exchange 2013 Cmdlet](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)  
    

