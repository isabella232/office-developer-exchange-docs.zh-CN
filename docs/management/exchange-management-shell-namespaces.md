---
title: Exchange 命令行管理程序命名空间
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ff849238-06b7-4891-884b-c51ce0f1ebbc
description: 查找 exchange 中 Exchange 命令行管理程序的命名空间的相关信息。
ms.openlocfilehash: 370c3e6cde48662eba8c62ad20e42fb716e66f2d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435812"
---
# <a name="exchange-management-shell-namespaces"></a><span data-ttu-id="88034-103">Exchange 命令行管理程序命名空间</span><span class="sxs-lookup"><span data-stu-id="88034-103">Exchange Management Shell namespaces</span></span>

<span data-ttu-id="88034-104">查找 exchange 中 Exchange 命令行管理程序的命名空间的相关信息。</span><span class="sxs-lookup"><span data-stu-id="88034-104">Find information about the namespaces for the Exchange Management Shell in Exchange.</span></span>
  
<span data-ttu-id="88034-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="88034-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="88034-106">Exchange Online 命令行管理程序 for Exchange Online、Exchange Online 作为 Office 365 的一部分，或者从 Exchange 2013 开始的 Exchange 版本通过由**System. Management** namespace 公开的类型与 Windows PowerShell 环境进行交互。</span><span class="sxs-lookup"><span data-stu-id="88034-106">Exchange Management Shell applications for Exchange Online, Exchange Online as part of Office 365, or a version of Exchange starting with Exchange 2013 interact with the Windows PowerShell environment through the types that are exposed by the **System.Management.Automation** namespace.</span></span> <span data-ttu-id="88034-107">Exchange 命令行管理程序 cmdlet 使用大量的 Exchange 库中的类型。</span><span class="sxs-lookup"><span data-stu-id="88034-107">The Exchange Management Shell cmdlets use types from a number of Exchange libraries.</span></span> <span data-ttu-id="88034-108">本节提供了有关 exchange 库中的类型和接口的参考信息，这些信息由 Exchange 命令行管理程序 cmdlet 使用。</span><span class="sxs-lookup"><span data-stu-id="88034-108">This section provides reference information about the types and interfaces from the Exchange libraries that are used by Exchange Management Shell cmdlets.</span></span> 
  
<span data-ttu-id="88034-109">Exchange 命令行管理程序包含以下命名空间：</span><span class="sxs-lookup"><span data-stu-id="88034-109">The Exchange Management Shell contains the following namespaces:</span></span>
  
- [<span data-ttu-id="88034-110">Microsoft. 配置任务</span><span class="sxs-lookup"><span data-stu-id="88034-110">Microsoft.Exchange.Configuration.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Configuration.Tasks.aspx)
    
- [<span data-ttu-id="88034-111">Microsoft. Data</span><span class="sxs-lookup"><span data-stu-id="88034-111">Microsoft.Exchange.Data</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.aspx)
    
- [<span data-ttu-id="88034-112">Microsoft. Data. 目录</span><span class="sxs-lookup"><span data-stu-id="88034-112">Microsoft.Exchange.Data.Directory</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.aspx)
    
- [<span data-ttu-id="88034-113">Microsoft.. Management</span><span class="sxs-lookup"><span data-stu-id="88034-113">Microsoft.Exchange.Data.Directory.Management</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Management.aspx)
    
- [<span data-ttu-id="88034-114">Microsoft. Data. 权限</span><span class="sxs-lookup"><span data-stu-id="88034-114">Microsoft.Exchange.Data.Directory.Permission</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Permission.aspx)
    
- [<span data-ttu-id="88034-115">Microsoft. 数据。收件人</span><span class="sxs-lookup"><span data-stu-id="88034-115">Microsoft.Exchange.Data.Directory.Recipient</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.Recipient.aspx)
    
- [<span data-ttu-id="88034-116">SystemConfiguration 的数据。</span><span class="sxs-lookup"><span data-stu-id="88034-116">Microsoft.Exchange.Data.Directory.SystemConfiguration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Directory.SystemConfiguration.aspx)
    
- [<span data-ttu-id="88034-117">Microsoft. 数据 Mapi</span><span class="sxs-lookup"><span data-stu-id="88034-117">Microsoft.Exchange.Data.Mapi</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Mapi.aspx)
    
- [<span data-ttu-id="88034-118">Microsoft Get-queuedigest</span><span class="sxs-lookup"><span data-stu-id="88034-118">Microsoft.Exchange.Data.QueueDigest</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.QueueDigest.aspx)
    
- [<span data-ttu-id="88034-119">Microsoft QueueViewer</span><span class="sxs-lookup"><span data-stu-id="88034-119">Microsoft.Exchange.Data.QueueViewer</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.QueueViewer.aspx)
    
- [<span data-ttu-id="88034-120">Microsoft RightsManagement</span><span class="sxs-lookup"><span data-stu-id="88034-120">Microsoft.Exchange.Data.RightsManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.RightsManagement.aspx)
    
- [<span data-ttu-id="88034-121">Microsoft. Data. Storage</span><span class="sxs-lookup"><span data-stu-id="88034-121">Microsoft.Exchange.Data.Storage</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.aspx)
    
- [<span data-ttu-id="88034-122">ActiveMonitoring 的数据。</span><span class="sxs-lookup"><span data-stu-id="88034-122">Microsoft.Exchange.Data.Storage.ActiveMonitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.ActiveMonitoring.aspx)
    
- [<span data-ttu-id="88034-123">Microsoft. Storage. Management</span><span class="sxs-lookup"><span data-stu-id="88034-123">Microsoft.Exchange.Data.Storage.Management</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.Management.aspx)
    
- [<span data-ttu-id="88034-124">Microsoft. 存储. 管理迁移</span><span class="sxs-lookup"><span data-stu-id="88034-124">Microsoft.Exchange.Data.Storage.Management.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.Management.Migration.aspx)
    
- [<span data-ttu-id="88034-125">StoreConfigurableType 的数据。</span><span class="sxs-lookup"><span data-stu-id="88034-125">Microsoft.Exchange.Data.Storage.StoreConfigurableType</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Storage.StoreConfigurableType.aspx)
    
- [<span data-ttu-id="88034-126">Microsoft EdgeSync</span><span class="sxs-lookup"><span data-stu-id="88034-126">Microsoft.Exchange.EdgeSync.Validation</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.EdgeSync.Validation.aspx)
    
- [<span data-ttu-id="88034-127">MailboxReplicationService</span><span class="sxs-lookup"><span data-stu-id="88034-127">Microsoft.Exchange.MailboxReplicationService</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MailboxReplicationService.aspx)
    
- [<span data-ttu-id="88034-128">Microsoft AgentTasks</span><span class="sxs-lookup"><span data-stu-id="88034-128">Microsoft.Exchange.Management.AgentTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.AgentTasks.aspx)
    
- [<span data-ttu-id="88034-129">Microsoft ClassificationDefinitions</span><span class="sxs-lookup"><span data-stu-id="88034-129">Microsoft.Exchange.Management.ClassificationDefinitions</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ClassificationDefinitions.aspx)
    
- [<span data-ttu-id="88034-130">Microsoft. 管理扩展</span><span class="sxs-lookup"><span data-stu-id="88034-130">Microsoft.Exchange.Management.Extension</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Extension.aspx)
    
- [<span data-ttu-id="88034-131">Microsoft FfoReporting</span><span class="sxs-lookup"><span data-stu-id="88034-131">Microsoft.Exchange.Management.FfoReporting</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.FfoReporting.aspx)
    
- [<span data-ttu-id="88034-132">FfoReporting 的常见情况</span><span class="sxs-lookup"><span data-stu-id="88034-132">Microsoft.Exchange.Management.FfoReporting.Common</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.FfoReporting.Common.aspx)
    
- [<span data-ttu-id="88034-133">AddressRewrite 中的 MessagingPolicies</span><span class="sxs-lookup"><span data-stu-id="88034-133">Microsoft.Exchange.Management.MessagingPolicies.AddressRewrite</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.MessagingPolicies.AddressRewrite.aspx)
    
- [<span data-ttu-id="88034-134">Microsoft. 迁移</span><span class="sxs-lookup"><span data-stu-id="88034-134">Microsoft.Exchange.Management.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Migration.aspx)
    
- [<span data-ttu-id="88034-135">Microsoft OutlookProtectionRules</span><span class="sxs-lookup"><span data-stu-id="88034-135">Microsoft.Exchange.Management.OutlookProtectionRules</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.OutlookProtectionRules.aspx)
    
- [<span data-ttu-id="88034-136">Microsoft PolicyNudges</span><span class="sxs-lookup"><span data-stu-id="88034-136">Microsoft.Exchange.Management.PolicyNudges</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.PolicyNudges.aspx)
    
- [<span data-ttu-id="88034-137">Microsoft ProvisioningTasks</span><span class="sxs-lookup"><span data-stu-id="88034-137">Microsoft.Exchange.Management.ProvisioningTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ProvisioningTasks.aspx)
    
- [<span data-ttu-id="88034-138">Microsoft RecipientTasks</span><span class="sxs-lookup"><span data-stu-id="88034-138">Microsoft.Exchange.Management.RecipientTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.RecipientTasks.aspx)
    
- [<span data-ttu-id="88034-139">ReportingTask 的常见情况</span><span class="sxs-lookup"><span data-stu-id="88034-139">Microsoft.Exchange.Management.ReportingTask.Common</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.Common.aspx)
    
- [<span data-ttu-id="88034-140">ReportingTask （查询）</span><span class="sxs-lookup"><span data-stu-id="88034-140">Microsoft.Exchange.Management.ReportingTask.Query</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.Query.aspx)
    
- [<span data-ttu-id="88034-141">TenantReport 中的 ReportingTask</span><span class="sxs-lookup"><span data-stu-id="88034-141">Microsoft.Exchange.Management.ReportingTask.TenantReport</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.ReportingTask.TenantReport.aspx)
    
- [<span data-ttu-id="88034-142">Microsoft RightsManagement</span><span class="sxs-lookup"><span data-stu-id="88034-142">Microsoft.Exchange.Management.RightsManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.RightsManagement.aspx)
    
- [<span data-ttu-id="88034-143">Microsoft. Management. 共享</span><span class="sxs-lookup"><span data-stu-id="88034-143">Microsoft.Exchange.Management.Sharing</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Sharing.aspx)
    
- [<span data-ttu-id="88034-144">Microsoft StoreTasks</span><span class="sxs-lookup"><span data-stu-id="88034-144">Microsoft.Exchange.Management.StoreTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.StoreTasks.aspx)
    
- [<span data-ttu-id="88034-145">Microsoft. 监察管理</span><span class="sxs-lookup"><span data-stu-id="88034-145">Microsoft.Exchange.Management.Supervision</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Supervision.aspx)
    
- [<span data-ttu-id="88034-146">Microsoft SystemConfigurationTasks</span><span class="sxs-lookup"><span data-stu-id="88034-146">Microsoft.Exchange.Management.SystemConfigurationTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.SystemConfigurationTasks.aspx)
    
- [<span data-ttu-id="88034-147">Microsoft. Management. Tasks</span><span class="sxs-lookup"><span data-stu-id="88034-147">Microsoft.Exchange.Management.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tasks.aspx)
    
- [<span data-ttu-id="88034-148">Microsoft. 管理工具</span><span class="sxs-lookup"><span data-stu-id="88034-148">Microsoft.Exchange.Management.Tools</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tools.aspx)
    
- [<span data-ttu-id="88034-149">Microsoft. Management. 跟踪</span><span class="sxs-lookup"><span data-stu-id="88034-149">Microsoft.Exchange.Management.Tracking</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.Tracking.aspx)
    
- [<span data-ttu-id="88034-150">Microsoft TransportLogSearchTasks</span><span class="sxs-lookup"><span data-stu-id="88034-150">Microsoft.Exchange.Management.TransportLogSearchTasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Management.TransportLogSearchTasks.aspx)
    
- [<span data-ttu-id="88034-151">MessagingPolicies. "CompliancePrograms"</span><span class="sxs-lookup"><span data-stu-id="88034-151">Microsoft.Exchange.MessagingPolicies.CompliancePrograms.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.CompliancePrograms.Tasks.aspx)
    
- [<span data-ttu-id="88034-152">MessagingPolicies 日志</span><span class="sxs-lookup"><span data-stu-id="88034-152">Microsoft.Exchange.MessagingPolicies.Journaling</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.Journaling.aspx)
    
- [<span data-ttu-id="88034-153">MessagingPolicies. "任务"</span><span class="sxs-lookup"><span data-stu-id="88034-153">Microsoft.Exchange.MessagingPolicies.Rules.Tasks</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.MessagingPolicies.Rules.Tasks.aspx)
    
- [<span data-ttu-id="88034-154">"Microsoft Exchange. 迁移"</span><span class="sxs-lookup"><span data-stu-id="88034-154">Microsoft.Exchange.Migration</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Migration.aspx)
    
- [<span data-ttu-id="88034-155">Microsoft. Monitoring</span><span class="sxs-lookup"><span data-stu-id="88034-155">Microsoft.Exchange.Monitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Monitoring.aspx)
    
- [<span data-ttu-id="88034-156">ActiveMonitoring 的</span><span class="sxs-lookup"><span data-stu-id="88034-156">Microsoft.Exchange.Monitoring.ActiveMonitoring</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Monitoring.ActiveMonitoring.aspx)
    
- [<span data-ttu-id="88034-157">（通常为订阅）</span><span class="sxs-lookup"><span data-stu-id="88034-157">Microsoft.Exchange.Transport.Sync.Common.Subscription</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.aspx)
    
- [<span data-ttu-id="88034-158">". 常见." 连接</span><span class="sxs-lookup"><span data-stu-id="88034-158">Microsoft.Exchange.Transport.Sync.Common.Subscription.Connect</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Connect.aspx)
    
- [<span data-ttu-id="88034-159">DeltaSync 中的 "."</span><span class="sxs-lookup"><span data-stu-id="88034-159">Microsoft.Exchange.Transport.Sync.Common.Subscription.DeltaSync</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.DeltaSync.aspx)
    
- [<span data-ttu-id="88034-160">（如订阅）公共订阅</span><span class="sxs-lookup"><span data-stu-id="88034-160">Microsoft.Exchange.Transport.Sync.Common.Subscription.Imap</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Imap.aspx)
    
- [<span data-ttu-id="88034-161">（如 "）"。</span><span class="sxs-lookup"><span data-stu-id="88034-161">Microsoft.Exchange.Transport.Sync.Common.Subscription.Pim</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Pim.aspx)
    
- [<span data-ttu-id="88034-162">（如订阅）。常用。</span><span class="sxs-lookup"><span data-stu-id="88034-162">Microsoft.Exchange.Transport.Sync.Common.Subscription.Pop</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.Transport.Sync.Common.Subscription.Pop.aspx)
    
- [<span data-ttu-id="88034-163">Microsoft. 古兰经</span><span class="sxs-lookup"><span data-stu-id="88034-163">Microsoft.Exchange.UM.Rpc</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.UM.Rpc.aspx)
    
- [<span data-ttu-id="88034-164">Microsoft UMCommon</span><span class="sxs-lookup"><span data-stu-id="88034-164">Microsoft.Exchange.UM.UMCommon</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.UM.UMCommon.aspx)
    
- [<span data-ttu-id="88034-165">WorkloadManagement</span><span class="sxs-lookup"><span data-stu-id="88034-165">Microsoft.Exchange.WorkloadManagement</span></span>](https://msdn.microsoft.com/library/Microsoft.Exchange.WorkloadManagement.aspx)
    
## <a name="see-also"></a><span data-ttu-id="88034-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="88034-166">See also</span></span>

- [<span data-ttu-id="88034-167">Exchange 命令行管理程序</span><span class="sxs-lookup"><span data-stu-id="88034-167">Exchange Management Shell</span></span>](exchange-management-shell.md)  
- [<span data-ttu-id="88034-168">创建 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="88034-168">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md) 
- [<span data-ttu-id="88034-169">Exchange 命令行管理程序 cmdlet 的输入和输出类型</span><span class="sxs-lookup"><span data-stu-id="88034-169">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)
    

