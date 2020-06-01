---
title: 使用 Exchange 中的 EWS 管理用户访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 48f0170c-8786-405f-86cb-568b7314a425
description: 了解用于管理用户帐户对 Exchange 服务器的访问权限的选项。
ms.openlocfilehash: 476292d4db206f22cd84134ce2b46957e9fe85fc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456240"
---
# <a name="managing-user-access-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 管理用户访问

了解用于管理用户帐户对 Exchange 服务器的访问权限的选项。
  
Exchange Web 服务（EWS）和 EWS 托管 API 提供有限数量的操作，可用于管理 Exchange Online 上的帐户、Exchange Online 作为 Office 365 的一部分或从 Exchange 2013 开始的 Exchange 版本。 您可以使用下图中所示的操作来管理委派和为其他帐户设置文件夹访问权限。 
  
**用于委派和文件夹访问的 EWS 操作**

![EWS 用户管理选项。](media/Exchange_ManagingUserAccess_1.png)
  
如果您的应用程序需要对 Exchange 服务器上的帐户进行更多控制，则可以使用 Exchange 命令行管理程序 cmdlet 来管理帐户。 您可以通过执行以下操作之一来调用 Exchange 命令行管理程序 cmdlet：
  
- 使用 c # 或 Visual Basic 编写调用 Exchange 命令行管理程序 cmdlet 的应用程序。 您可以查看[Exchange 命令行管理程序 API 文档](../management/exchange-management-shell.md)中的示例代码，以了解如何调用 cmdlet。 
    
- 使用 Windows PowerShell 和 Windows PowerShell 脚本调用 Exchange 命令行管理程序 cmdlet。 您可以找到[Exchange Server PowerShell （Exchange 命令行管理程序）](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)的完整列表，以及演示如何使用它们的示例。 
    
## <a name="see-also"></a>另请参阅

- [设置 EWS 应用程序](setting-up-your-ews-application.md)   
- [Exchange 2013 Cmdlet](https://docs.microsoft.com/powershell/exchange/?view=exchange-ps)  
    

