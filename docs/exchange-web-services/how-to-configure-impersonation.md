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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752759"
---
# <a name="configure-impersonation"></a><span data-ttu-id="b9080-103">配置模拟</span><span class="sxs-lookup"><span data-stu-id="b9080-103">Configure impersonation</span></span>

<span data-ttu-id="b9080-104">了解如何使用 Exchange 命令行管理程序授予权限的服务帐户模拟角色。</span><span class="sxs-lookup"><span data-stu-id="b9080-104">Learn how to grant the impersonation role to a service account by using the Exchange Management Shell.</span></span> 
  
<span data-ttu-id="b9080-105">模拟使呼叫者，如服务应用程序，以模拟的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="b9080-105">Impersonation enables a caller, such as a service application, to impersonate a user account.</span></span> <span data-ttu-id="b9080-106">呼叫者可以通过使用与模拟而不是与呼叫者的帐户关联的权限的帐户关联的权限来执行操作。</span><span class="sxs-lookup"><span data-stu-id="b9080-106">The caller can perform operations by using the permissions that are associated with the impersonated account instead of the permissions associated with the caller's account.</span></span>
  
<span data-ttu-id="b9080-107">Exchange Online、 Exchange Online 作为 Office 365 的一部分和版本的 Exchange 开头 Exchange 2013 使用基于角色的访问控制 (RBAC) 分配到帐户的权限。</span><span class="sxs-lookup"><span data-stu-id="b9080-107">Exchange Online, Exchange Online as part of Office 365, and versions of Exchange starting with Exchange 2013 use role-based access control (RBAC) to assign permissions to accounts.</span></span> <span data-ttu-id="b9080-108">您的 Exchange 服务器管理员将需要使用[New-managementroleassignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet**通过 ApplicationImpersonation**角色授予将模拟其他用户的任何服务帐户。</span><span class="sxs-lookup"><span data-stu-id="b9080-108">Your Exchange server administrator will need to grant any service account that will be impersonating other users the **ApplicationImpersonation** role by using the [New-ManagementRoleAssignment](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx) cmdlet.</span></span> 
  
## <a name="configuring-the-applicationimpersonation-role"></a><span data-ttu-id="b9080-109">配置通过 ApplicationImpersonation 角色</span><span class="sxs-lookup"><span data-stu-id="b9080-109">Configuring the ApplicationImpersonation role</span></span>

<span data-ttu-id="b9080-110">当您或您交换器服务器管理员赋予**ApplicationImpersonation**角色时，使用**New-managementroleassignment** cmdlet 的以下参数：</span><span class="sxs-lookup"><span data-stu-id="b9080-110">When you or your Exchanger server administrator assigns the **ApplicationImpersonation** role, use the following parameters of the **New-ManagementRoleAssignment** cmdlet:</span></span> 
  
-  <span data-ttu-id="b9080-111">_名称_&ndash;的角色分配的友好名称。</span><span class="sxs-lookup"><span data-stu-id="b9080-111">_Name_ &ndash; The friendly name of the role assignment.</span></span> <span data-ttu-id="b9080-112">分配角色，每次在 RBAC 角色列表中所做的条目。</span><span class="sxs-lookup"><span data-stu-id="b9080-112">Each time that you assign a role, an entry is made in the RBAC roles list.</span></span> <span data-ttu-id="b9080-113">您可以使用[Get-managementroleassignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet 来验证角色分配。</span><span class="sxs-lookup"><span data-stu-id="b9080-113">You can verify role assignments by using the [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
    
-  <span data-ttu-id="b9080-114">_角色_&ndash;的 RBAC 角色分配。</span><span class="sxs-lookup"><span data-stu-id="b9080-114">_Role_ &ndash; The RBAC role to assign.</span></span> <span data-ttu-id="b9080-115">时将模拟设置，您将**通过 ApplicationImpersonation**角色分配。</span><span class="sxs-lookup"><span data-stu-id="b9080-115">When you set up impersonation, you assign the **ApplicationImpersonation** role.</span></span> 
    
-  <span data-ttu-id="b9080-116">_用户_&ndash;的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="b9080-116">_User_ &ndash; The service account.</span></span> 
    
-  <span data-ttu-id="b9080-117">_CustomRecipientScope_&ndash;的服务帐户可以模拟的用户的范围。</span><span class="sxs-lookup"><span data-stu-id="b9080-117">_CustomRecipientScope_ &ndash; The scope of users that the service account can impersonate.</span></span> <span data-ttu-id="b9080-118">仅允许模拟指定范围内的其他用户的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="b9080-118">The service account will only be allowed to impersonate other users within the specified scope.</span></span> <span data-ttu-id="b9080-119">如果没有指定范围，服务帐户对组织中的所有用户授予**ApplicationImpersonation**角色。</span><span class="sxs-lookup"><span data-stu-id="b9080-119">If no scope is specified, the service account is granted the **ApplicationImpersonation** role over all users in an organization.</span></span> <span data-ttu-id="b9080-120">您可以使用[New-managementscope](http://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet 创建自定义管理作用域。</span><span class="sxs-lookup"><span data-stu-id="b9080-120">You can create custom management scopes by using the [New-ManagementScope](http://msdn.microsoft.com/library/1ea1f474-69d6-48c0-9beb-bfa4442c5dab.aspx) cmdlet.</span></span> 
    
<span data-ttu-id="b9080-121">您可以配置模拟之前，您需要：</span><span class="sxs-lookup"><span data-stu-id="b9080-121">Before you can configure impersonation, you need:</span></span>
  
- <span data-ttu-id="b9080-122">Exchange server 的的管理凭据。</span><span class="sxs-lookup"><span data-stu-id="b9080-122">Administrative credentials for the Exchange server.</span></span>
    
- <span data-ttu-id="b9080-123">域管理员凭据或有权创建并分配角色和范围其他凭据。</span><span class="sxs-lookup"><span data-stu-id="b9080-123">Domain Administrator credentials, or other credentials with the permission to create and assign roles and scopes.</span></span>
    
- <span data-ttu-id="b9080-124">Exchange 管理工具。</span><span class="sxs-lookup"><span data-stu-id="b9080-124">Exchange management tools.</span></span> <span data-ttu-id="b9080-125">将从中运行命令的计算机上安装这些。</span><span class="sxs-lookup"><span data-stu-id="b9080-125">These are installed on the computer from which you will run the commands.</span></span>
    
### <a name="to-configure-impersonation-for-all-users-in-an-organization"></a><span data-ttu-id="b9080-126">若要在组织中配置的所有用户模拟</span><span class="sxs-lookup"><span data-stu-id="b9080-126">To configure impersonation for all users in an organization</span></span>

1. <span data-ttu-id="b9080-127">打开 Exchange Management Shell。</span><span class="sxs-lookup"><span data-stu-id="b9080-127">Open the Exchange Management Shell.</span></span> <span data-ttu-id="b9080-128">从开始菜单中，选择**所有程序** > **Microsoft Exchange Server 2013**。</span><span class="sxs-lookup"><span data-stu-id="b9080-128">From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="b9080-129">运行**New-managementroleassignment** cmdlet 将模拟权限添加到指定的用户。</span><span class="sxs-lookup"><span data-stu-id="b9080-129">Run the **New-ManagementRoleAssignment** cmdlet to add the impersonation permission to the specified user.</span></span> <span data-ttu-id="b9080-130">下面的示例演示如何配置模拟启用模拟组织中的所有其他用户的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="b9080-130">The following example shows how to configure impersonation to enable a service account to impersonate all other users in an organization.</span></span> 
    
   ```powershell
   New-ManagementRoleAssignment -name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount 
   ```

### <a name="to-configure-impersonation-for-specific-users-or-groups-of-users"></a><span data-ttu-id="b9080-131">配置特定用户或组的用户模拟</span><span class="sxs-lookup"><span data-stu-id="b9080-131">To configure impersonation for specific users or groups of users</span></span>

1. <span data-ttu-id="b9080-132">打开 Exchange Management Shell。</span><span class="sxs-lookup"><span data-stu-id="b9080-132">Open the Exchange Management Shell.</span></span> <span data-ttu-id="b9080-133">从开始菜单中，选择**所有程序** > **Microsoft Exchange Server 2013**。</span><span class="sxs-lookup"><span data-stu-id="b9080-133">From the Start menu, choose **All Programs** > **Microsoft Exchange Server 2013**.</span></span> 
    
2. <span data-ttu-id="b9080-134">运行**New-managementscope** cmdlet 创建一个作用域，可以为其分配模拟角色。</span><span class="sxs-lookup"><span data-stu-id="b9080-134">Run the **New-ManagementScope** cmdlet to create a scope to which the impersonation role can be assigned.</span></span> <span data-ttu-id="b9080-135">如果现有作用域为可用，您可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="b9080-135">If an existing scope is available, you can skip this step.</span></span> <span data-ttu-id="b9080-136">下面的示例演示如何创建一组特定的管理作用域。</span><span class="sxs-lookup"><span data-stu-id="b9080-136">The following example shows how to create a management scope for a specific group.</span></span> 
    
   ```powershell
    New-ManagementScope -Name:scopeName -RecipientRestrictionFilter:recipientFilter
   ```

   <span data-ttu-id="b9080-137">**New-managementscope** cmdlet 的_RecipientRestrictionFilter_参数定义作用域的成员。</span><span class="sxs-lookup"><span data-stu-id="b9080-137">The _RecipientRestrictionFilter_ parameter of the **New-ManagementScope** cmdlet defines the members of the scope.</span></span> <span data-ttu-id="b9080-138">**标识**对象的属性可用于创建筛选器。</span><span class="sxs-lookup"><span data-stu-id="b9080-138">You can use the properties of the **Identity** object to create the filter.</span></span> <span data-ttu-id="b9080-139">下面的示例是一个筛选器，将结果限制为单个用户以方法是用户名称"john。"</span><span class="sxs-lookup"><span data-stu-id="b9080-139">The following example is a filter that restricts the result to a single user with the user name "john."</span></span> 
    
   ```powershell
   Name -eq "john"
   ```

3. <span data-ttu-id="b9080-140">运行**New-managementroleassignment** cmdlet 将用于模拟指定作用域的成员的权限。</span><span class="sxs-lookup"><span data-stu-id="b9080-140">Run the **New-ManagementRoleAssignment** cmdlet to add the permission to impersonate the members of the specified scope.</span></span> <span data-ttu-id="b9080-141">下面的示例演示如何配置模拟范围中的所有用户的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="b9080-141">The following example shows how to configure a service account to impersonate all users in a scope.</span></span> 
    
   ```powershell
    New-ManagementRoleAssignment -Name:impersonationAssignmentName -Role:ApplicationImpersonation -User:serviceAccount -CustomRecipientWriteScope:scopeName
    
   ```


<span data-ttu-id="b9080-142">您的管理员授予模拟权限后，您可以使用的服务帐户进行呼叫针对其他用户的帐户。</span><span class="sxs-lookup"><span data-stu-id="b9080-142">After your administrator grants impersonation permissions, you can use the service account to make calls against other users' accounts.</span></span> <span data-ttu-id="b9080-143">您可以使用[Get-managementroleassignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet 来验证角色分配。</span><span class="sxs-lookup"><span data-stu-id="b9080-143">You can verify role assignments by using the [Get-ManagementRoleAssignment](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx) cmdlet.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b9080-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b9080-144">See also</span></span>

- [<span data-ttu-id="b9080-145">Impersonation and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="b9080-145">Impersonation and EWS in Exchange</span></span>](impersonation-and-ews-in-exchange.md)
- [<span data-ttu-id="b9080-146">ApplicationImpersonation 角色</span><span class="sxs-lookup"><span data-stu-id="b9080-146">ApplicationImpersonation role</span></span>](http://technet.microsoft.com/zh-cn/library/dd776119%28v=exchg.150%29.aspx)   
- [<span data-ttu-id="b9080-147">新 ManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b9080-147">New-ManagementRoleAssignment</span></span>](http://msdn.microsoft.com/library/34d4f2e3-f2c5-49e1-a6a9-1366da65a78c.aspx)    
- [<span data-ttu-id="b9080-148">Get-managementroleassignment</span><span class="sxs-lookup"><span data-stu-id="b9080-148">Get-ManagementRoleAssignment</span></span>](http://msdn.microsoft.com/library/a3a6ee46-061b-444a-8639-43a416309445.aspx)
    

