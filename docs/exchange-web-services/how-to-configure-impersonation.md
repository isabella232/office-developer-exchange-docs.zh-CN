---
title: 配置模拟
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: efcef39f-e26d-4eed-95ac-36a5bf8c089f
description: 了解如何使用 Exchange 命令行管理程序向服务帐户授予模拟角色。
localization_priority: Priority
ms.openlocfilehash: f8fe95536213e347840af082d765a9cc2fbce819
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455896"
---
# <a name="configure-impersonation"></a>配置模拟

了解如何使用 Exchange 命令行管理程序向服务帐户授予模拟角色。 
  
模拟使呼叫者（如服务应用程序）能够模拟用户帐户。 呼叫者可以使用与模拟帐户关联的权限，而不是与呼叫者帐户相关联的权限来执行操作。
  
Exchange Online、作为 Office 365 的一部分的 exchange Online 和从 Exchange 2013 开始的 Exchange 版本使用基于角色的访问控制（RBAC）为帐户分配权限。 Exchange server 管理员需要向任何服务帐户授予将使用[get-managementroleassignment](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet 模拟其他用户**ApplicationImpersonation**角色的服务帐户。 
  
## <a name="configuring-the-applicationimpersonation-role"></a>配置 ApplicationImpersonation 角色

当您或您的交换器服务器管理员分配**ApplicationImpersonation**角色时，请使用**get-managementroleassignment** cmdlet 的以下参数： 
  
-  _名称_ &ndash;角色分配的友好名称。 每次分配角色时，都会在 "RBAC 角色" 列表中进行输入。 您可以使用[get-managementroleassignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet 验证角色分配。 
    
-  _角色_ &ndash;要分配的 RBAC 角色。 设置模拟时，请分配**ApplicationImpersonation**角色。 
    
-  _用户_ &ndash;服务帐户。 
    
-  _CustomRecipientScope_ &ndash;服务帐户可以模拟的用户的范围。 仅允许服务帐户模拟指定范围内的其他用户。 如果未指定作用域，则会为服务帐户授予对组织中所有用户的**ApplicationImpersonation**角色。 您可以使用[new-managementscope](https://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet 创建自定义管理作用域。 
    
您需要先执行以下操作，然后才能配置模拟：
  
- Exchange 服务器的管理凭据。
    
- 域管理员凭据，或其他具有创建和分配角色和作用域的权限的凭据。
    
- Exchange 管理工具。 这些命令将安装在要运行命令的计算机上。
    
### <a name="to-configure-impersonation-for-all-users-in-an-organization"></a>为组织中的所有用户配置模拟

1. 打开 Exchange 命令行管理程序。 从 "开始" 菜单中**All Programs**，选择 "  >  **Microsoft Exchange Server 2013**的所有程序"。 
    
2. 运行**get-managementroleassignment** cmdlet 以将模拟权限添加到指定的用户。 下面的示例演示如何将模拟配置为使服务帐户能够模拟组织中的所有其他用户。 
    
   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### <a name="to-configure-impersonation-for-specific-users-or-groups-of-users"></a>为特定用户或用户组配置模拟

1. 打开 Exchange 命令行管理程序。 从 "开始" 菜单中**All Programs**，选择 "  >  **Microsoft Exchange Server 2013**的所有程序"。 
    
2. 运行**new-managementscope** cmdlet 以创建可向其分配模拟角色的作用域。 如果现有范围可用，则可以跳过此步骤。 下面的示例演示如何为特定组创建管理作用域。 
    
   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   **New-managementscope** Cmdlet 的_RecipientRestrictionFilter_参数定义作用域的成员。 您可以使用**Identity**对象的属性来创建筛选器。 下面的示例是一个筛选器，它将结果限制为用户名称为 "john" 的单个用户。 
    
   ```powershell
   Name -eq "john"
   ```

3. 运行**get-managementroleassignment** cmdlet 以添加模拟指定作用域的成员的权限。 下面的示例演示如何配置服务帐户以模拟作用域中的所有用户。 
    
   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```


管理员授予模拟权限后，您可以使用服务帐户对其他用户的帐户进行呼叫。 您可以使用[get-managementroleassignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet 验证角色分配。 
  
## <a name="see-also"></a>另请参阅

- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
- [ApplicationImpersonation 角色](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)   
- [新 Get-managementroleassignment](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)    
- [Get-managementroleassignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
    

