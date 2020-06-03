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
# <a name="configure-impersonation"></a><span data-ttu-id="51e0b-103">配置模拟</span><span class="sxs-lookup"><span data-stu-id="51e0b-103">Configure impersonation</span></span>

<span data-ttu-id="51e0b-104">了解如何使用 Exchange 命令行管理程序向服务帐户授予模拟角色。</span><span class="sxs-lookup"><span data-stu-id="51e0b-104">Learn how to grant the impersonation role to a service account by using the Exchange Management Shell.</span></span> 
  
<span data-ttu-id="51e0b-105">模拟使呼叫者（如服务应用程序）能够模拟用户帐户。</span><span class="sxs-lookup"><span data-stu-id="51e0b-105">Impersonation enables a caller, such as a service application, to impersonate a user account.</span></span> <span data-ttu-id="51e0b-106">呼叫者可以使用与模拟帐户关联的权限，而不是与呼叫者帐户相关联的权限来执行操作。</span><span class="sxs-lookup"><span data-stu-id="51e0b-106">The caller can perform operations by using the permissions that are associated with the impersonated account instead of the permissions associated with the caller's account.</span></span>
  
<span data-ttu-id="51e0b-107">Exchange Online、作为 Office 365 的一部分的 exchange Online 和从 Exchange 2013 开始的 Exchange 版本使用基于角色的访问控制（RBAC）为帐户分配权限。</span><span class="sxs-lookup"><span data-stu-id="51e0b-107">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013 use role-based access control (RBAC) to assign permissions to accounts.</span></span> <span data-ttu-id="51e0b-108">Exchange server 管理员需要向任何服务帐户授予将使用[get-managementroleassignment](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet 模拟其他用户**ApplicationImpersonation**角色的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="51e0b-108">Your Exchange server administrator will need to grant any service account that will be impersonating other users the **ApplicationImpersonation** role by using the [New-ManagementRoleAssignment](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet.</span></span> 
  
## <a name="configuring-the-applicationimpersonation-role"></a><span data-ttu-id="51e0b-109">配置 ApplicationImpersonation 角色</span><span class="sxs-lookup"><span data-stu-id="51e0b-109">Configuring the ApplicationImpersonation role</span></span>

<span data-ttu-id="51e0b-110">当您或您的交换器服务器管理员分配**ApplicationImpersonation**角色时，请使用**get-managementroleassignment** cmdlet 的以下参数：</span><span class="sxs-lookup"><span data-stu-id="51e0b-110">When you or your Exchanger server administrator assigns the **ApplicationImpersonation** role, use the following parameters of the **New-ManagementRoleAssignment** cmdlet:</span></span> 
  
-  <span data-ttu-id="51e0b-111">_名称_ &ndash;角色分配的友好名称。</span><span class="sxs-lookup"><span data-stu-id="51e0b-111">_Name_ &ndash; The friendly name of the role assignment.</span></span> <span data-ttu-id="51e0b-112">每次分配角色时，都会在 "RBAC 角色" 列表中进行输入。</span><span class="sxs-lookup"><span data-stu-id="51e0b-112">Each time that you assign a role, an entry is made in the RBAC roles list.</span></span> <span data-ttu-id="51e0b-113">您可以使用[get-managementroleassignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet 验证角色分配。</span><span class="sxs-lookup"><span data-stu-id="51e0b-113">You can verify role assignments by using the [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
    
-  <span data-ttu-id="51e0b-114">_角色_ &ndash;要分配的 RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="51e0b-114">_Role_ &ndash; The RBAC role to assign.</span></span> <span data-ttu-id="51e0b-115">设置模拟时，请分配**ApplicationImpersonation**角色。</span><span class="sxs-lookup"><span data-stu-id="51e0b-115">When you set up impersonation, you assign the **ApplicationImpersonation** role.</span></span> 
    
-  <span data-ttu-id="51e0b-116">_用户_ &ndash;服务帐户。</span><span class="sxs-lookup"><span data-stu-id="51e0b-116">_User_ &ndash; The service account.</span></span> 
    
-  <span data-ttu-id="51e0b-117">_CustomRecipientScope_ &ndash;服务帐户可以模拟的用户的范围。</span><span class="sxs-lookup"><span data-stu-id="51e0b-117">_CustomRecipientScope_ &ndash; The scope of users that the service account can impersonate.</span></span> <span data-ttu-id="51e0b-118">仅允许服务帐户模拟指定范围内的其他用户。</span><span class="sxs-lookup"><span data-stu-id="51e0b-118">The service account will only be allowed to impersonate other users within the specified scope.</span></span> <span data-ttu-id="51e0b-119">如果未指定作用域，则会为服务帐户授予对组织中所有用户的**ApplicationImpersonation**角色。</span><span class="sxs-lookup"><span data-stu-id="51e0b-119">If no scope is specified, the service account is granted the **ApplicationImpersonation** role over all users in an organization.</span></span> <span data-ttu-id="51e0b-120">您可以使用[new-managementscope](https://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet 创建自定义管理作用域。</span><span class="sxs-lookup"><span data-stu-id="51e0b-120">You can create custom management scopes by using the [New-ManagementScope](https://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet.</span></span> 
    
<span data-ttu-id="51e0b-121">您需要先执行以下操作，然后才能配置模拟：</span><span class="sxs-lookup"><span data-stu-id="51e0b-121">Before you can configure impersonation, you need:</span></span>
  
- <span data-ttu-id="51e0b-122">Exchange 服务器的管理凭据。</span><span class="sxs-lookup"><span data-stu-id="51e0b-122">Administrative credentials for the Exchange server.</span></span>
    
- <span data-ttu-id="51e0b-123">域管理员凭据，或其他具有创建和分配角色和作用域的权限的凭据。</span><span class="sxs-lookup"><span data-stu-id="51e0b-123">Domain Administrator credentials, or other credentials with the permission to create and assign roles and scopes.</span></span>
    
- <span data-ttu-id="51e0b-124">Exchange 管理工具。</span><span class="sxs-lookup"><span data-stu-id="51e0b-124">Exchange management tools.</span></span> <span data-ttu-id="51e0b-125">这些命令将安装在要运行命令的计算机上。</span><span class="sxs-lookup"><span data-stu-id="51e0b-125">These are installed on the computer from which you will run the commands.</span></span>
    
### <a name="to-configure-impersonation-for-all-users-in-an-organization"></a><span data-ttu-id="51e0b-126">为组织中的所有用户配置模拟</span><span class="sxs-lookup"><span data-stu-id="51e0b-126">To configure impersonation for all users in an organization</span></span>

1. <span data-ttu-id="51e0b-127">打开 Exchange 命令行管理程序。</span><span class="sxs-lookup"><span data-stu-id="51e0b-127">Open the Exchange Management Shell.</span></span> <span data-ttu-id="51e0b-128">从 "开始" 菜单中**All Programs**，选择 "  >  **Microsoft Exchange Server 2013**的所有程序"。</span><span class="sxs-lookup"><span data-stu-id="51e0b-128">From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="51e0b-129">运行**get-managementroleassignment** cmdlet 以将模拟权限添加到指定的用户。</span><span class="sxs-lookup"><span data-stu-id="51e0b-129">Run the **New-ManagementRoleAssignment** cmdlet to add the impersonation permission to the specified user.</span></span> <span data-ttu-id="51e0b-130">下面的示例演示如何将模拟配置为使服务帐户能够模拟组织中的所有其他用户。</span><span class="sxs-lookup"><span data-stu-id="51e0b-130">The following example shows how to configure impersonation to enable a service account to impersonate all other users in an organization.</span></span> 
    
   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### <a name="to-configure-impersonation-for-specific-users-or-groups-of-users"></a><span data-ttu-id="51e0b-131">为特定用户或用户组配置模拟</span><span class="sxs-lookup"><span data-stu-id="51e0b-131">To configure impersonation for specific users or groups of users</span></span>

1. <span data-ttu-id="51e0b-132">打开 Exchange 命令行管理程序。</span><span class="sxs-lookup"><span data-stu-id="51e0b-132">Open the Exchange Management Shell.</span></span> <span data-ttu-id="51e0b-133">从 "开始" 菜单中**All Programs**，选择 "  >  **Microsoft Exchange Server 2013**的所有程序"。</span><span class="sxs-lookup"><span data-stu-id="51e0b-133">From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="51e0b-134">运行**new-managementscope** cmdlet 以创建可向其分配模拟角色的作用域。</span><span class="sxs-lookup"><span data-stu-id="51e0b-134">Run the **New-ManagementScope** cmdlet to create a scope to which the impersonation role can be assigned.</span></span> <span data-ttu-id="51e0b-135">如果现有范围可用，则可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="51e0b-135">If an existing scope is available, you can skip this step.</span></span> <span data-ttu-id="51e0b-136">下面的示例演示如何为特定组创建管理作用域。</span><span class="sxs-lookup"><span data-stu-id="51e0b-136">The following example shows how to create a management scope for a specific group.</span></span> 
    
   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   <span data-ttu-id="51e0b-137">**New-managementscope** Cmdlet 的_RecipientRestrictionFilter_参数定义作用域的成员。</span><span class="sxs-lookup"><span data-stu-id="51e0b-137">The _RecipientRestrictionFilter_ parameter of the **New-ManagementScope** cmdlet defines the members of the scope.</span></span> <span data-ttu-id="51e0b-138">您可以使用**Identity**对象的属性来创建筛选器。</span><span class="sxs-lookup"><span data-stu-id="51e0b-138">You can use the properties of the **Identity** object to create the filter.</span></span> <span data-ttu-id="51e0b-139">下面的示例是一个筛选器，它将结果限制为用户名称为 "john" 的单个用户。</span><span class="sxs-lookup"><span data-stu-id="51e0b-139">The following example is a filter that restricts the result to a single user with the user name "john."</span></span> 
    
   ```powershell
   Name -eq "john"
   ```

3. <span data-ttu-id="51e0b-140">运行**get-managementroleassignment** cmdlet 以添加模拟指定作用域的成员的权限。</span><span class="sxs-lookup"><span data-stu-id="51e0b-140">Run the **New-ManagementRoleAssignment** cmdlet to add the permission to impersonate the members of the specified scope.</span></span> <span data-ttu-id="51e0b-141">下面的示例演示如何配置服务帐户以模拟作用域中的所有用户。</span><span class="sxs-lookup"><span data-stu-id="51e0b-141">The following example shows how to configure a service account to impersonate all users in a scope.</span></span> 
    
   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```


<span data-ttu-id="51e0b-142">管理员授予模拟权限后，您可以使用服务帐户对其他用户的帐户进行呼叫。</span><span class="sxs-lookup"><span data-stu-id="51e0b-142">After your administrator grants impersonation permissions, you can use the service account to make calls against other users' accounts.</span></span> <span data-ttu-id="51e0b-143">您可以使用[get-managementroleassignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet 验证角色分配。</span><span class="sxs-lookup"><span data-stu-id="51e0b-143">You can verify role assignments by using the [Get-ManagementRoleAssignment](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51e0b-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="51e0b-144">See also</span></span>

- [<span data-ttu-id="51e0b-145">Impersonation and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="51e0b-145">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
- [<span data-ttu-id="51e0b-146">ApplicationImpersonation 角色</span><span class="sxs-lookup"><span data-stu-id="51e0b-146">ApplicationImpersonation role</span></span>](https://technet.microsoft.com/library/dd776119%28v=exchg.150%29.aspx)   
- [<span data-ttu-id="51e0b-147">新 Get-managementroleassignment</span><span class="sxs-lookup"><span data-stu-id="51e0b-147">New-ManagementRoleAssignment</span></span>](https://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)    
- [<span data-ttu-id="51e0b-148">Get-managementroleassignment</span><span class="sxs-lookup"><span data-stu-id="51e0b-148">Get-ManagementRoleAssignment</span></span>](https://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
    

