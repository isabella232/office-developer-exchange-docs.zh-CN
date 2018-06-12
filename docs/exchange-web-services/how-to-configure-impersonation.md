---
title: 配置模拟
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: efcef39f-e26d-4eed-95ac-36a5bf8c089f
description: 了解如何使用 Exchange 命令行管理程序授予权限的服务帐户模拟角色。
ms.openlocfilehash: 57ccef48a7553bcc06e3b3ae940b376b8555ef84
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752759"
---
# <a name="configure-impersonation"></a>配置模拟

了解如何使用 Exchange 命令行管理程序授予权限的服务帐户模拟角色。 
  
模拟使呼叫者，如服务应用程序，以模拟的用户帐户。 呼叫者可以通过使用与模拟而不是与呼叫者的帐户关联的权限的帐户关联的权限来执行操作。
  
Exchange Online、 Exchange Online 作为 Office 365 的一部分和版本的 Exchange 开头 Exchange 2013 使用基于角色的访问控制 (RBAC) 分配到帐户的权限。 您的 Exchange 服务器管理员将需要使用[New-managementroleassignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet**通过 ApplicationImpersonation**角色授予将模拟其他用户的任何服务帐户。 
  
## <a name="configuring-the-applicationimpersonation-role"></a>配置通过 ApplicationImpersonation 角色

当您或您交换器服务器管理员赋予**ApplicationImpersonation**角色时，使用**New-managementroleassignment** cmdlet 的以下参数： 
  
-  _名称_&ndash;的角色分配的友好名称。 分配角色，每次在 RBAC 角色列表中所做的条目。 您可以使用[Get-managementroleassignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet 来验证角色分配。 
    
-  _角色_&ndash;的 RBAC 角色分配。 时将模拟设置，您将**通过 ApplicationImpersonation**角色分配。 
    
-  _用户_&ndash;的服务帐户。 
    
-  _CustomRecipientScope_&ndash;的服务帐户可以模拟的用户的范围。 仅允许模拟指定范围内的其他用户的服务帐户。 如果没有指定范围，服务帐户对组织中的所有用户授予**ApplicationImpersonation**角色。 您可以使用[New-managementscope](http://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet 创建自定义管理作用域。 
    
您可以配置模拟之前，您需要：
  
- Exchange server 的的管理凭据。
    
- 域管理员凭据或有权创建并分配角色和范围其他凭据。
    
- Exchange 管理工具。 将从中运行命令的计算机上安装这些。
    
### <a name="to-configure-impersonation-for-all-users-in-an-organization"></a>若要在组织中配置的所有用户模拟

1. 打开 Exchange Management Shell。 从开始菜单中，选择**所有程序** > **Microsoft Exchange Server 2013**。 
    
2. 运行**New-managementroleassignment** cmdlet 将模拟权限添加到指定的用户。 下面的示例演示如何配置模拟启用模拟组织中的所有其他用户的服务帐户。 
    
   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### <a name="to-configure-impersonation-for-specific-users-or-groups-of-users"></a>配置特定用户或组的用户模拟

1. 打开 Exchange Management Shell。 从开始菜单中，选择**所有程序** > **Microsoft Exchange Server 2013**。 
    
2. 运行**New-managementscope** cmdlet 创建一个作用域，可以为其分配模拟角色。 如果现有作用域为可用，您可以跳过此步骤。 下面的示例演示如何创建一组特定的管理作用域。 
    
   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   **New-managementscope** cmdlet 的_RecipientRestrictionFilter_参数定义作用域的成员。 **标识**对象的属性可用于创建筛选器。 下面的示例是一个筛选器，将结果限制为单个用户以方法是用户名称"john。" 
    
   ```powershell
   Name -eq "john"
   ```

3. 运行**New-managementroleassignment** cmdlet 将用于模拟指定作用域的成员的权限。 下面的示例演示如何配置模拟范围中的所有用户的服务帐户。 
    
   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```


您的管理员授予模拟权限后，您可以使用的服务帐户进行呼叫针对其他用户的帐户。 您可以使用[Get-managementroleassignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet 来验证角色分配。 
  
## <a name="see-also"></a>另请参阅

- [Impersonation and EWS in Exchange](impersonation-and-ews-in-exchange.md)
- [ApplicationImpersonation 角色](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx)   
- [新 ManagementRoleAssignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)    
- [Get-managementroleassignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
    

