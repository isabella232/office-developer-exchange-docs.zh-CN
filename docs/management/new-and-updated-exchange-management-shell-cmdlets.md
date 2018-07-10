---
title: 新增和经过更新的 Exchange 命令行管理程序 cmdlet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5941a439-94d2-4133-81fc-7240863a13df
description: 查找有关 what's new in Exchange 命令行管理程序在 Exchange 信息。
ms.openlocfilehash: 906e078ab6d500a2cb3d364957ffc2fee67a06b4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753066"
---
# <a name="new-and-updated-exchange-management-shell-cmdlets"></a><span data-ttu-id="15ef6-103">新增和经过更新的 Exchange 命令行管理程序 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-103">New and updated Exchange Management Shell cmdlets</span></span>

<span data-ttu-id="15ef6-104">查找有关 what's new in Exchange 命令行管理程序在 Exchange 信息。</span><span class="sxs-lookup"><span data-stu-id="15ef6-104">Find information about what's new in the Exchange Management Shell in Exchange.</span></span>
  
<span data-ttu-id="15ef6-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="15ef6-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="15ef6-106">本文提供有关新 Exchange Management shell cmdlet、 中，修改过的 cmdlet 和 Exchange Online、 Exchange Online 作为 Office 365 的一部分或 Exchange 内部部署版本中删除了 cmdlet 的信息。</span><span class="sxs-lookup"><span data-stu-id="15ef6-106">This article provides information about new Exchange Management shell cmdlets, cmdlets that were modified in, and cmdlets that were removed from Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange.</span></span>
  
## <a name="new-and-updated-cmdlets-in-exchange-2013-sp1"></a><span data-ttu-id="15ef6-107">Exchange 2013 SP1 中的新增和经过更新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-107">New and updated cmdlets in Exchange 2013 SP1</span></span>

### <a name="new-cmdlets"></a><span data-ttu-id="15ef6-108">新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-108">New cmdlets</span></span>

<span data-ttu-id="15ef6-109">生成 15.00.0847.032 (Exchange Server 2013 SP1) 中引入了以下 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="15ef6-109">The following cmdlets were introduced in build 15.00.0847.032 (Exchange Server 2013 SP1):</span></span>
  
- <span data-ttu-id="15ef6-110">**Get-authredirect**</span><span class="sxs-lookup"><span data-stu-id="15ef6-110">**Get-AuthRedirect**</span></span>
    
- <span data-ttu-id="15ef6-111">**新 AuthRedirect**</span><span class="sxs-lookup"><span data-stu-id="15ef6-111">**New-AuthRedirect**</span></span>
    
- <span data-ttu-id="15ef6-112">**Remove-authredirect**</span><span class="sxs-lookup"><span data-stu-id="15ef6-112">**Remove-AuthRedirect**</span></span>
    
- <span data-ttu-id="15ef6-113">**Set-authredirect**</span><span class="sxs-lookup"><span data-stu-id="15ef6-113">**Set-AuthRedirect**</span></span>
    
- <span data-ttu-id="15ef6-114">**新 DataClassification**</span><span class="sxs-lookup"><span data-stu-id="15ef6-114">**New-DataClassification**</span></span>
    
- <span data-ttu-id="15ef6-115">**删除 DataClassification**</span><span class="sxs-lookup"><span data-stu-id="15ef6-115">**Remove-DataClassification**</span></span>
    
- <span data-ttu-id="15ef6-116">**Set-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="15ef6-116">**Set-DataClassification**</span></span>
    
- <span data-ttu-id="15ef6-117">**新指纹**</span><span class="sxs-lookup"><span data-stu-id="15ef6-117">**New-FingerPrint**</span></span>
    
- <span data-ttu-id="15ef6-118">**Get MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="15ef6-118">**Get-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="15ef6-119">**新 MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="15ef6-119">**New-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="15ef6-120">**删除 MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="15ef6-120">**Remove-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="15ef6-121">**设置 MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="15ef6-121">**Set-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="15ef6-122">**Get-omeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="15ef6-122">**Get-OMEConfiguration**</span></span>
    
- <span data-ttu-id="15ef6-123">**Set-omeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="15ef6-123">**Set-OMEConfiguration**</span></span>
    
- <span data-ttu-id="15ef6-124">**Get-smimeconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-124">**Get-SmimeConfig**</span></span>
    
- <span data-ttu-id="15ef6-125">**Set-smimeconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-125">**Set-SmimeConfig**</span></span>
    
- <span data-ttu-id="15ef6-126">**Get-intraorganizationconfiguration**</span><span class="sxs-lookup"><span data-stu-id="15ef6-126">**Get-IntraOrganizationConfiguration**</span></span>
    
- <span data-ttu-id="15ef6-127">**Get-intraorganizationconnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-127">**Get-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="15ef6-128">**新 IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-128">**New-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="15ef6-129">**删除 IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-129">**Remove-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="15ef6-130">**设置 IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-130">**Set-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="15ef6-131">**Get-historicalsearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-131">**Get-HistoricalSearch**</span></span>
    
- <span data-ttu-id="15ef6-132">**Start-historicalsearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-132">**Start-HistoricalSearch**</span></span>
    
- <span data-ttu-id="15ef6-133">**Stop-historicalsearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-133">**Stop-HistoricalSearch**</span></span>
    
- <span data-ttu-id="15ef6-134">**新 SearchDocumentFormat**</span><span class="sxs-lookup"><span data-stu-id="15ef6-134">**New-SearchDocumentFormat**</span></span>
    
- <span data-ttu-id="15ef6-135">**删除 SearchDocumentFormat**</span><span class="sxs-lookup"><span data-stu-id="15ef6-135">**Remove-SearchDocumentFormat**</span></span>
    
### <a name="updated-cmdlets"></a><span data-ttu-id="15ef6-136">更新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-136">Updated cmdlets</span></span>

<span data-ttu-id="15ef6-137">生成 15.00.0847.032 (Exchange 2013 SP1) 中已更新以下 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="15ef6-137">The following cmdlets were updated in build 15.00.0847.032 (Exchange 2013 SP1):</span></span>
  
- <span data-ttu-id="15ef6-138">**Get AuditLogSearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-138">**Get-AuditLogSearch**</span></span>
    
- <span data-ttu-id="15ef6-139">**Get-quarantinemessage**</span><span class="sxs-lookup"><span data-stu-id="15ef6-139">**Get-QuarantineMessage**</span></span>
    
- <span data-ttu-id="15ef6-140">**新 InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-140">**New-InboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-141">**新 MailboxDatabase**</span><span class="sxs-lookup"><span data-stu-id="15ef6-141">**New-MailboxDatabase**</span></span>
    
- <span data-ttu-id="15ef6-142">**新细节**</span><span class="sxs-lookup"><span data-stu-id="15ef6-142">**New-PublicFolderMoveRequest**</span></span>
    
- <span data-ttu-id="15ef6-143">**New-transportrule**</span><span class="sxs-lookup"><span data-stu-id="15ef6-143">**New-TransportRule**</span></span>
    
- <span data-ttu-id="15ef6-144">**Set-frontendtransportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-144">**Set-FrontendTransportService**</span></span>
    
- <span data-ttu-id="15ef6-145">**Set-inboundconnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-145">**Set-InboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-146">**设置邮箱**</span><span class="sxs-lookup"><span data-stu-id="15ef6-146">**Set-Mailbox**</span></span>
    
- <span data-ttu-id="15ef6-147">**Set-mailboxtransportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-147">**Set-MailboxTransportService**</span></span>
    
- <span data-ttu-id="15ef6-148">**Set-moverequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-148">**Set-MoveRequest**</span></span>
    
- <span data-ttu-id="15ef6-149">**Set-organizationconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-149">**Set-OrganizationConfig**</span></span>
    
- <span data-ttu-id="15ef6-150">**Set-owamailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-150">**Set-OwaMailboxPolicy**</span></span>
    
- <span data-ttu-id="15ef6-151">**Set-owavirtualdirectory**</span><span class="sxs-lookup"><span data-stu-id="15ef6-151">**Set-OwaVirtualDirectory**</span></span>
    
- <span data-ttu-id="15ef6-152">**设置传输配置**</span><span class="sxs-lookup"><span data-stu-id="15ef6-152">**Set-TransportConfig**</span></span>
    
- <span data-ttu-id="15ef6-153">**Set-transportrule**</span><span class="sxs-lookup"><span data-stu-id="15ef6-153">**Set-TransportRule**</span></span>
    
- <span data-ttu-id="15ef6-154">**Set-transportserver**</span><span class="sxs-lookup"><span data-stu-id="15ef6-154">**Set-TransportServer**</span></span>
    
- <span data-ttu-id="15ef6-155">**Set-transportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-155">**Set-TransportService**</span></span>
    
- <span data-ttu-id="15ef6-156">**Test-mrshealth**</span><span class="sxs-lookup"><span data-stu-id="15ef6-156">**Test-MRSHealth**</span></span>
    
- <span data-ttu-id="15ef6-157">**测试 OAuthConnectivity**</span><span class="sxs-lookup"><span data-stu-id="15ef6-157">**Test-OAuthConnectivity**</span></span>
    
### <a name="removed-cmdlets"></a><span data-ttu-id="15ef6-158">删除的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-158">Removed cmdlets</span></span>

<span data-ttu-id="15ef6-159">从生成 15.00.0847.032 (Exchange 2013 SP1) 中删除了以下 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="15ef6-159">The following cmdlets were removed from build 15.00.0847.032 (Exchange 2013 SP1):</span></span>
  
- <span data-ttu-id="15ef6-160">**Get AvailabilityReportOutage**</span><span class="sxs-lookup"><span data-stu-id="15ef6-160">**Get-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="15ef6-161">**新 AvailabilityReportOutage**</span><span class="sxs-lookup"><span data-stu-id="15ef6-161">**New-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="15ef6-162">**删除 AvailabilityReportOutage**</span><span class="sxs-lookup"><span data-stu-id="15ef6-162">**Remove-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="15ef6-163">**设置 AvailabilityReportOutage**</span><span class="sxs-lookup"><span data-stu-id="15ef6-163">**Set-AvailabilityReportOutage**</span></span>
    
## <a name="new-and-updated-cmdlets-in-exchange-2013"></a><span data-ttu-id="15ef6-164">Exchange 2013 中的新增和经过更新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-164">New and updated cmdlets in Exchange 2013</span></span>

### <a name="new-cmdlets"></a><span data-ttu-id="15ef6-165">新 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-165">New cmdlets</span></span>
<span data-ttu-id="15ef6-166"><a name="bk_new"> </a></span><span class="sxs-lookup"><span data-stu-id="15ef6-166"></span></span>

<span data-ttu-id="15ef6-167">Exchange 2013 中引入了以下 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="15ef6-167">The following cmdlets were introduced in Exchange 2013:</span></span>
  
- <span data-ttu-id="15ef6-168">**Get-activesyncdeviceautoblockthreshold**</span><span class="sxs-lookup"><span data-stu-id="15ef6-168">**Get-ActiveSyncDeviceAutoblockThreshold**</span></span>
    
- <span data-ttu-id="15ef6-169">**Set-activesyncdeviceautoblockthreshold**</span><span class="sxs-lookup"><span data-stu-id="15ef6-169">**Set-ActiveSyncDeviceAutoblockThreshold**</span></span>
    
- <span data-ttu-id="15ef6-170">**禁用应用程序**</span><span class="sxs-lookup"><span data-stu-id="15ef6-170">**Disable-App**</span></span>
    
- <span data-ttu-id="15ef6-171">**启用应用程序**</span><span class="sxs-lookup"><span data-stu-id="15ef6-171">**Enable-App**</span></span>
    
- <span data-ttu-id="15ef6-172">**获取应用程序**</span><span class="sxs-lookup"><span data-stu-id="15ef6-172">**Get-App**</span></span>
    
- <span data-ttu-id="15ef6-173">**新应用程序**</span><span class="sxs-lookup"><span data-stu-id="15ef6-173">**New-App**</span></span>
    
- <span data-ttu-id="15ef6-174">**删除应用程序**</span><span class="sxs-lookup"><span data-stu-id="15ef6-174">**Remove-App**</span></span>
    
- <span data-ttu-id="15ef6-175">**设置应用程序**</span><span class="sxs-lookup"><span data-stu-id="15ef6-175">**Set-App**</span></span>
    
- <span data-ttu-id="15ef6-176">**Get-authconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-176">**Get-AuthConfig**</span></span>
    
- <span data-ttu-id="15ef6-177">**Set-authconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-177">**Set-AuthConfig**</span></span>
    
- <span data-ttu-id="15ef6-178">**Get-authserver**</span><span class="sxs-lookup"><span data-stu-id="15ef6-178">**Get-AuthServer**</span></span>
    
- <span data-ttu-id="15ef6-179">**新认证服务器**</span><span class="sxs-lookup"><span data-stu-id="15ef6-179">**New-AuthServer**</span></span>
    
- <span data-ttu-id="15ef6-180">**Remove-authserver**</span><span class="sxs-lookup"><span data-stu-id="15ef6-180">**Remove-AuthServer**</span></span>
    
- <span data-ttu-id="15ef6-181">**Set-authserver**</span><span class="sxs-lookup"><span data-stu-id="15ef6-181">**Set-AuthServer**</span></span>
    
- <span data-ttu-id="15ef6-182">**新 AvailabilityConfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-182">**New-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="15ef6-183">**删除 AvailabilityConfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-183">**Remove-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="15ef6-184">**Get-calendardiagnosticanalysis**</span><span class="sxs-lookup"><span data-stu-id="15ef6-184">**Get-CalendarDiagnosticAnalysis**</span></span>
    
- <span data-ttu-id="15ef6-185">**Get-classificationrulecollection**</span><span class="sxs-lookup"><span data-stu-id="15ef6-185">**Get-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="15ef6-186">**新 ClassificationRuleCollection**</span><span class="sxs-lookup"><span data-stu-id="15ef6-186">**New-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="15ef6-187">**Remove-classificationrulecollection**</span><span class="sxs-lookup"><span data-stu-id="15ef6-187">**Remove-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="15ef6-188">**Set-classificationrulecollection**</span><span class="sxs-lookup"><span data-stu-id="15ef6-188">**Set-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="15ef6-189">**Get ConnectSubscription**</span><span class="sxs-lookup"><span data-stu-id="15ef6-189">**Get-ConnectSubscription**</span></span>
    
- <span data-ttu-id="15ef6-190">**新 ConnectSubscription**</span><span class="sxs-lookup"><span data-stu-id="15ef6-190">**New-ConnectSubscription**</span></span>
    
- <span data-ttu-id="15ef6-191">**删除 ConnectSubscription**</span><span class="sxs-lookup"><span data-stu-id="15ef6-191">**Remove-ConnectSubscription**</span></span>
    
- <span data-ttu-id="15ef6-192">**设置 ConnectSubscription**</span><span class="sxs-lookup"><span data-stu-id="15ef6-192">**Set-ConnectSubscription**</span></span>
    
- <span data-ttu-id="15ef6-193">**Get-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="15ef6-193">**Get-DataClassification**</span></span>
    
- <span data-ttu-id="15ef6-194">**Get DataClassificationConfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-194">**Get-DataClassificationConfig**</span></span>
    
- <span data-ttu-id="15ef6-195">**Get-dlppolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-195">**Get-DlpPolicy**</span></span>
    
- <span data-ttu-id="15ef6-196">**新 DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-196">**New-DlpPolicy**</span></span>
    
- <span data-ttu-id="15ef6-197">**Remove-dlppolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-197">**Remove-DlpPolicy**</span></span>
    
- <span data-ttu-id="15ef6-198">**Set-dlppolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-198">**Set-DlpPolicy**</span></span>
    
- <span data-ttu-id="15ef6-199">**Export-dlppolicycollection**</span><span class="sxs-lookup"><span data-stu-id="15ef6-199">**Export-DlpPolicyCollection**</span></span>
    
- <span data-ttu-id="15ef6-200">**Import-dlppolicycollection**</span><span class="sxs-lookup"><span data-stu-id="15ef6-200">**Import-DlpPolicyCollection**</span></span>
    
- <span data-ttu-id="15ef6-201">**Get-dlppolicytemplate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-201">**Get-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="15ef6-202">**导入 DlpPolicyTemplate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-202">**Import-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="15ef6-203">**Remove-dlppolicytemplate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-203">**Remove-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="15ef6-204">**Get ExchangeServerAccessLicense**</span><span class="sxs-lookup"><span data-stu-id="15ef6-204">**Get-ExchangeServerAccessLicense**</span></span>
    
- <span data-ttu-id="15ef6-205">**Get ExchangeServerAccessLicenseUser**</span><span class="sxs-lookup"><span data-stu-id="15ef6-205">**Get-ExchangeServerAccessLicenseUser**</span></span>
    
- <span data-ttu-id="15ef6-206">**Get FfoMigrationReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-206">**Get-FfoMigrationReport**</span></span>
    
- <span data-ttu-id="15ef6-207">**Get-frontendtransportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-207">**Get-FrontendTransportService**</span></span>
    
- <span data-ttu-id="15ef6-208">**Set-frontendtransportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-208">**Set-FrontendTransportService**</span></span>
    
- <span data-ttu-id="15ef6-209">**添加 GlobalMonitoringOverride**</span><span class="sxs-lookup"><span data-stu-id="15ef6-209">**Add-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="15ef6-210">**Get-globalmonitoringoverride**</span><span class="sxs-lookup"><span data-stu-id="15ef6-210">**Get-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="15ef6-211">**Remove-globalmonitoringoverride**</span><span class="sxs-lookup"><span data-stu-id="15ef6-211">**Remove-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="15ef6-212">**Get GroupActivityReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-212">**Get-GroupActivityReport**</span></span>
    
- <span data-ttu-id="15ef6-213">**Get HealthReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-213">**Get-HealthReport**</span></span>
    
- <span data-ttu-id="15ef6-214">**Get HostedConnectionFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-214">**Get-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-215">**新 HostedConnectionFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-215">**New-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-216">**删除 HostedConnectionFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-216">**Remove-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-217">**Set-hostedconnectionfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-217">**Set-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-218">**Get-hostedcontentfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-218">**Get-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-219">**New-hostedcontentfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-219">**New-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-220">**Remove-hostedcontentfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-220">**Remove-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-221">**Set-hostedcontentfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-221">**Set-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-222">**Get HostedOutboundSpamFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-222">**Get-HostedOutboundSpamFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-223">**设置 HostedOutboundSpamFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-223">**Set-HostedOutboundSpamFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-224">**Remove-hybridconfiguration**</span><span class="sxs-lookup"><span data-stu-id="15ef6-224">**Remove-HybridConfiguration**</span></span>
    
- <span data-ttu-id="15ef6-225">**Get-hybridmailflow**</span><span class="sxs-lookup"><span data-stu-id="15ef6-225">**Get-HybridMailflow**</span></span>
    
- <span data-ttu-id="15ef6-226">**Set-hybridmailflow**</span><span class="sxs-lookup"><span data-stu-id="15ef6-226">**Set-HybridMailflow**</span></span>
    
- <span data-ttu-id="15ef6-227">**Get-hybridmailflowdatacenterips**</span><span class="sxs-lookup"><span data-stu-id="15ef6-227">**Get-HybridMailflowDatacenterIPs**</span></span>
    
- <span data-ttu-id="15ef6-228">**Get InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-228">**Get-InboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-229">**新 InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-229">**New-InboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-230">**删除 InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-230">**Remove-InboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-231">**Set-inboundconnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-231">**Set-InboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-232">**Get MailboxActivityReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-232">**Get-MailboxActivityReport**</span></span>
    
- <span data-ttu-id="15ef6-233">**Disable-mailboxquarantine**</span><span class="sxs-lookup"><span data-stu-id="15ef6-233">**Disable-MailboxQuarantine**</span></span>
    
- <span data-ttu-id="15ef6-234">**Enable-mailboxquarantine**</span><span class="sxs-lookup"><span data-stu-id="15ef6-234">**Enable-MailboxQuarantine**</span></span>
    
- <span data-ttu-id="15ef6-235">**Get-mailboxtransportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-235">**Get-MailboxTransportService**</span></span>
    
- <span data-ttu-id="15ef6-236">**Set-mailboxtransportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-236">**Set-MailboxTransportService**</span></span>
    
- <span data-ttu-id="15ef6-237">**Get MailDetailDlpPolicyReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-237">**Get-MailDetailDlpPolicyReport**</span></span>
    
- <span data-ttu-id="15ef6-238">**Get MailDetailMalwareReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-238">**Get-MailDetailMalwareReport**</span></span>
    
- <span data-ttu-id="15ef6-239">**Get MailDetailReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-239">**Get-MailDetailReport**</span></span>
    
- <span data-ttu-id="15ef6-240">**Get MailDetailSpamReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-240">**Get-MailDetailSpamReport**</span></span>
    
- <span data-ttu-id="15ef6-241">**Get MailDetailTransportRuleReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-241">**Get-MailDetailTransportRuleReport**</span></span>
    
- <span data-ttu-id="15ef6-242">**Get MailFilterListReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-242">**Get-MailFilterListReport**</span></span>
    
- <span data-ttu-id="15ef6-243">**Get MailTrafficPolicyReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-243">**Get-MailTrafficPolicyReport**</span></span>
    
- <span data-ttu-id="15ef6-244">**Get MailTrafficReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-244">**Get-MailTrafficReport**</span></span>
    
- <span data-ttu-id="15ef6-245">**Get MailTrafficSummaryReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-245">**Get-MailTrafficSummaryReport**</span></span>
    
- <span data-ttu-id="15ef6-246">**Get MailTrafficTopReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-246">**Get-MailTrafficTopReport**</span></span>
    
- <span data-ttu-id="15ef6-247">**Get-malwarefilteringserver**</span><span class="sxs-lookup"><span data-stu-id="15ef6-247">**Get-MalwareFilteringServer**</span></span>
    
- <span data-ttu-id="15ef6-248">**Set-malwarefilteringserver**</span><span class="sxs-lookup"><span data-stu-id="15ef6-248">**Set-MalwareFilteringServer**</span></span>
    
- <span data-ttu-id="15ef6-249">**Get-malwarefilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-249">**Get-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-250">**New-malwarefilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-250">**New-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-251">**Remove-malwarefilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-251">**Remove-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-252">**Set-malwarefilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-252">**Set-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="15ef6-253">**Get MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="15ef6-253">**Get-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="15ef6-254">**删除 MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="15ef6-254">**Remove-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="15ef6-255">**继续 MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="15ef6-255">**Resume-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="15ef6-256">**发送 MapiSubmitSystemProbe**</span><span class="sxs-lookup"><span data-stu-id="15ef6-256">**Send-MapiSubmitSystemProbe**</span></span>
    
- <span data-ttu-id="15ef6-257">**重定向邮件**</span><span class="sxs-lookup"><span data-stu-id="15ef6-257">**Redirect-Message**</span></span>
    
- <span data-ttu-id="15ef6-258">**Get-messagetrace**</span><span class="sxs-lookup"><span data-stu-id="15ef6-258">**Get-MessageTrace**</span></span>
    
- <span data-ttu-id="15ef6-259">**Get-messagetracedetail**</span><span class="sxs-lookup"><span data-stu-id="15ef6-259">**Get-MessageTraceDetail**</span></span>
    
- <span data-ttu-id="15ef6-260">**完成 MigrationBatch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-260">**Complete-MigrationBatch**</span></span>
    
- <span data-ttu-id="15ef6-261">**Remove-migrationbatch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-261">**Remove-MigrationBatch**</span></span>
    
- <span data-ttu-id="15ef6-262">**Get-migrationconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-262">**Get-MigrationConfig**</span></span>
    
- <span data-ttu-id="15ef6-263">**Set-migrationconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-263">**Set-MigrationConfig**</span></span>
    
- <span data-ttu-id="15ef6-264">**Get-migrationendpoint**</span><span class="sxs-lookup"><span data-stu-id="15ef6-264">**Get-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="15ef6-265">**新 MigrationEndpoint**</span><span class="sxs-lookup"><span data-stu-id="15ef6-265">**New-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="15ef6-266">**Remove-migrationendpoint**</span><span class="sxs-lookup"><span data-stu-id="15ef6-266">**Remove-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="15ef6-267">**Set-migrationendpoint**</span><span class="sxs-lookup"><span data-stu-id="15ef6-267">**Set-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="15ef6-268">**Get-migrationstatistics**</span><span class="sxs-lookup"><span data-stu-id="15ef6-268">**Get-MigrationStatistics**</span></span>
    
- <span data-ttu-id="15ef6-269">**Get-migrationuser**</span><span class="sxs-lookup"><span data-stu-id="15ef6-269">**Get-MigrationUser**</span></span>
    
- <span data-ttu-id="15ef6-270">**Remove-migrationuser**</span><span class="sxs-lookup"><span data-stu-id="15ef6-270">**Remove-MigrationUser**</span></span>
    
- <span data-ttu-id="15ef6-271">**Get-migrationuserstatistics**</span><span class="sxs-lookup"><span data-stu-id="15ef6-271">**Get-MigrationUserStatistics**</span></span>
    
- <span data-ttu-id="15ef6-272">**Clear-mobiledevice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-272">**Clear-MobileDevice**</span></span>
    
- <span data-ttu-id="15ef6-273">**Get-mobiledevice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-273">**Get-MobileDevice**</span></span>
    
- <span data-ttu-id="15ef6-274">**Remove-mobiledevice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-274">**Remove-MobileDevice**</span></span>
    
- <span data-ttu-id="15ef6-275">**Get-mobiledevicemailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-275">**Get-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="15ef6-276">**新 MobileDeviceMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-276">**New-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="15ef6-277">**Remove-mobiledevicemailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-277">**Remove-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="15ef6-278">**Set-mobiledevicemailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-278">**Set-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="15ef6-279">**Get-mobiledevicestatistics**</span><span class="sxs-lookup"><span data-stu-id="15ef6-279">**Get-MobileDeviceStatistics**</span></span>
    
- <span data-ttu-id="15ef6-280">**Get MonitoringItemHelp**</span><span class="sxs-lookup"><span data-stu-id="15ef6-280">**Get-MonitoringItemHelp**</span></span>
    
- <span data-ttu-id="15ef6-281">**Get-monitoringitemidentity**</span><span class="sxs-lookup"><span data-stu-id="15ef6-281">**Get-MonitoringItemIdentity**</span></span>
    
- <span data-ttu-id="15ef6-282">**调用 MonitoringProbe**</span><span class="sxs-lookup"><span data-stu-id="15ef6-282">**Invoke-MonitoringProbe**</span></span>
    
- <span data-ttu-id="15ef6-283">**获取通知**</span><span class="sxs-lookup"><span data-stu-id="15ef6-283">**Get-Notification**</span></span>
    
- <span data-ttu-id="15ef6-284">**设置通知**</span><span class="sxs-lookup"><span data-stu-id="15ef6-284">**Set-Notification**</span></span>
    
- <span data-ttu-id="15ef6-285">**测试 OAuthConnectivity**</span><span class="sxs-lookup"><span data-stu-id="15ef6-285">**Test-OAuthConnectivity**</span></span>
    
- <span data-ttu-id="15ef6-286">**Get-onpremisesorganization**</span><span class="sxs-lookup"><span data-stu-id="15ef6-286">**Get-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="15ef6-287">**新 OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="15ef6-287">**New-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="15ef6-288">**删除 OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="15ef6-288">**Remove-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="15ef6-289">**Set-onpremisesorganization**</span><span class="sxs-lookup"><span data-stu-id="15ef6-289">**Set-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="15ef6-290">**启用 OrganizationCustomization**</span><span class="sxs-lookup"><span data-stu-id="15ef6-290">**Enable-OrganizationCustomization**</span></span>
    
- <span data-ttu-id="15ef6-291">**Get OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-291">**Get-OutboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-292">**新 OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-292">**New-OutboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-293">**删除 OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-293">**Remove-OutboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-294">**Set-outboundconnector**</span><span class="sxs-lookup"><span data-stu-id="15ef6-294">**Set-OutboundConnector**</span></span>
    
- <span data-ttu-id="15ef6-295">**Get-partnerapplication**</span><span class="sxs-lookup"><span data-stu-id="15ef6-295">**Get-PartnerApplication**</span></span>
    
- <span data-ttu-id="15ef6-296">**新 PartnerApplication**</span><span class="sxs-lookup"><span data-stu-id="15ef6-296">**New-PartnerApplication**</span></span>
    
- <span data-ttu-id="15ef6-297">**删除 PartnerApplication**</span><span class="sxs-lookup"><span data-stu-id="15ef6-297">**Remove-PartnerApplication**</span></span>
    
- <span data-ttu-id="15ef6-298">**Set-partnerapplication**</span><span class="sxs-lookup"><span data-stu-id="15ef6-298">**Set-PartnerApplication**</span></span>
    
- <span data-ttu-id="15ef6-299">**Get-pendingfederateddomain**</span><span class="sxs-lookup"><span data-stu-id="15ef6-299">**Get-PendingFederatedDomain**</span></span>
    
- <span data-ttu-id="15ef6-300">**Set-pendingfederateddomain**</span><span class="sxs-lookup"><span data-stu-id="15ef6-300">**Set-PendingFederatedDomain**</span></span>
    
- <span data-ttu-id="15ef6-301">**Get-policytipconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-301">**Get-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="15ef6-302">**新 PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-302">**New-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="15ef6-303">**删除 PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-303">**Remove-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="15ef6-304">**Set-policytipconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-304">**Set-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="15ef6-305">**Dump-provisioningcache**</span><span class="sxs-lookup"><span data-stu-id="15ef6-305">**Dump-ProvisioningCache**</span></span>
    
- <span data-ttu-id="15ef6-306">**重置 ProvisioningCache**</span><span class="sxs-lookup"><span data-stu-id="15ef6-306">**Reset-ProvisioningCache**</span></span>
    
- <span data-ttu-id="15ef6-307">**Update-publicfoldermailbox**</span><span class="sxs-lookup"><span data-stu-id="15ef6-307">**Update-PublicFolderMailbox**</span></span>
    
- <span data-ttu-id="15ef6-308">**Get PublicFolderMailboxDiagnostics**</span><span class="sxs-lookup"><span data-stu-id="15ef6-308">**Get-PublicFolderMailboxDiagnostics**</span></span>
    
- <span data-ttu-id="15ef6-309">**Get-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-309">**Get-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="15ef6-310">**新 PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-310">**New-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="15ef6-311">**删除 PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-311">**Remove-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="15ef6-312">**Resume-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-312">**Resume-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="15ef6-313">**Set-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-313">**Set-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="15ef6-314">**挂起 PublicFolderMigrationRequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-314">**Suspend-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="15ef6-315">**Get-publicfoldermigrationrequeststatistics**</span><span class="sxs-lookup"><span data-stu-id="15ef6-315">**Get-PublicFolderMigrationRequestStatistics**</span></span>
    
- <span data-ttu-id="15ef6-316">**Get-quarantinemessage**</span><span class="sxs-lookup"><span data-stu-id="15ef6-316">**Get-QuarantineMessage**</span></span>
    
- <span data-ttu-id="15ef6-317">**版本 QuarantineMessage**</span><span class="sxs-lookup"><span data-stu-id="15ef6-317">**Release-QuarantineMessage**</span></span>
    
- <span data-ttu-id="15ef6-318">**Get-queuedigest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-318">**Get-QueueDigest**</span></span>
    
- <span data-ttu-id="15ef6-319">**Get-resourcepolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-319">**Get-ResourcePolicy**</span></span>
    
- <span data-ttu-id="15ef6-320">**新 ResourcePolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-320">**New-ResourcePolicy**</span></span>
    
- <span data-ttu-id="15ef6-321">**Remove-resourcepolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-321">**Remove-ResourcePolicy**</span></span>
    
- <span data-ttu-id="15ef6-322">**Set-resourcepolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-322">**Set-ResourcePolicy**</span></span>
    
- <span data-ttu-id="15ef6-323">**添加 ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-323">**Add-ResubmitRequest**</span></span>
    
- <span data-ttu-id="15ef6-324">**Get-resubmitrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-324">**Get-ResubmitRequest**</span></span>
    
- <span data-ttu-id="15ef6-325">**Remove-resubmitrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-325">**Remove-ResubmitRequest**</span></span>
    
- <span data-ttu-id="15ef6-326">**Set-resubmitrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-326">**Set-ResubmitRequest**</span></span>
    
- <span data-ttu-id="15ef6-327">**Get-servercomponentstate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-327">**Get-ServerComponentState**</span></span>
    
- <span data-ttu-id="15ef6-328">**Set-servercomponentstate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-328">**Set-ServerComponentState**</span></span>
    
- <span data-ttu-id="15ef6-329">**Get-serverhealth**</span><span class="sxs-lookup"><span data-stu-id="15ef6-329">**Get-ServerHealth**</span></span>
    
- <span data-ttu-id="15ef6-330">**Set-servermonitor**</span><span class="sxs-lookup"><span data-stu-id="15ef6-330">**Set-ServerMonitor**</span></span>
    
- <span data-ttu-id="15ef6-331">**添加 ServerMonitoringOverride**</span><span class="sxs-lookup"><span data-stu-id="15ef6-331">**Add-ServerMonitoringOverride**</span></span>
    
- <span data-ttu-id="15ef6-332">**Get-servermonitoringoverride**</span><span class="sxs-lookup"><span data-stu-id="15ef6-332">**Get-ServerMonitoringOverride**</span></span>
    
- <span data-ttu-id="15ef6-333">**Get SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="15ef6-333">**Get-SiteMailbox**</span></span>
    
- <span data-ttu-id="15ef6-334">**新 SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="15ef6-334">**New-SiteMailbox**</span></span>
    
- <span data-ttu-id="15ef6-335">**设置 SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="15ef6-335">**Set-SiteMailbox**</span></span>
    
- <span data-ttu-id="15ef6-336">**测试 SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="15ef6-336">**Test-SiteMailbox**</span></span>
    
- <span data-ttu-id="15ef6-337">**更新 SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="15ef6-337">**Update-SiteMailbox**</span></span>
    
- <span data-ttu-id="15ef6-338">**Get SiteMailboxDiagnostics**</span><span class="sxs-lookup"><span data-stu-id="15ef6-338">**Get-SiteMailboxDiagnostics**</span></span>
    
- <span data-ttu-id="15ef6-339">**Get-sitemailboxprovisioningpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-339">**Get-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="15ef6-340">**新 SiteMailboxProvisioningPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-340">**New-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="15ef6-341">**Remove-sitemailboxprovisioningpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-341">**Remove-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="15ef6-342">**Set-sitemailboxprovisioningpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-342">**Set-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="15ef6-343">**撤消 SoftDeletedMailbox**</span><span class="sxs-lookup"><span data-stu-id="15ef6-343">**Undo-SoftDeletedMailbox**</span></span>
    
- <span data-ttu-id="15ef6-344">**Get StaleMailboxDetailReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-344">**Get-StaleMailboxDetailReport**</span></span>
    
- <span data-ttu-id="15ef6-345">**Get StaleMailboxReport**</span><span class="sxs-lookup"><span data-stu-id="15ef6-345">**Get-StaleMailboxReport**</span></span>
    
- <span data-ttu-id="15ef6-346">**Update-storemailboxstate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-346">**Update-StoreMailboxState**</span></span>
    
- <span data-ttu-id="15ef6-347">**新 SyncMailPublicFolder**</span><span class="sxs-lookup"><span data-stu-id="15ef6-347">**New-SyncMailPublicFolder**</span></span>
    
- <span data-ttu-id="15ef6-348">**Get-transportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-348">**Get-TransportService**</span></span>
    
- <span data-ttu-id="15ef6-349">**Set-transportservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-349">**Set-TransportService**</span></span>
    
- <span data-ttu-id="15ef6-350">**Disable-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="15ef6-350">**Disable-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="15ef6-351">**Enable-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="15ef6-351">**Enable-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="15ef6-352">**Get-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="15ef6-352">**Get-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="15ef6-353">**新 UMCallAnsweringRule**</span><span class="sxs-lookup"><span data-stu-id="15ef6-353">**New-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="15ef6-354">**Remove-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="15ef6-354">**Remove-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="15ef6-355">**Set-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="15ef6-355">**Set-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="15ef6-356">**Get UMCallRouterSettings**</span><span class="sxs-lookup"><span data-stu-id="15ef6-356">**Get-UMCallRouterSettings**</span></span>
    
- <span data-ttu-id="15ef6-357">**设置 UMCallRouterSettings**</span><span class="sxs-lookup"><span data-stu-id="15ef6-357">**Set-UMCallRouterSettings**</span></span>
    
- <span data-ttu-id="15ef6-358">**禁用 UMService**</span><span class="sxs-lookup"><span data-stu-id="15ef6-358">**Disable-UMService**</span></span>
    
- <span data-ttu-id="15ef6-359">**启用 UMService**</span><span class="sxs-lookup"><span data-stu-id="15ef6-359">**Enable-UMService**</span></span>
    
- <span data-ttu-id="15ef6-360">**Get UMService**</span><span class="sxs-lookup"><span data-stu-id="15ef6-360">**Get-UMService**</span></span>
    
- <span data-ttu-id="15ef6-361">**Set-umservice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-361">**Set-UMService**</span></span>
    
- <span data-ttu-id="15ef6-362">**Get UserPhoto**</span><span class="sxs-lookup"><span data-stu-id="15ef6-362">**Get-UserPhoto**</span></span>
    
- <span data-ttu-id="15ef6-363">**删除 UserPhoto**</span><span class="sxs-lookup"><span data-stu-id="15ef6-363">**Remove-UserPhoto**</span></span>
    
- <span data-ttu-id="15ef6-364">**设置 UserPhoto**</span><span class="sxs-lookup"><span data-stu-id="15ef6-364">**Set-UserPhoto**</span></span>
    
- <span data-ttu-id="15ef6-365">**Get-workloadmanagementpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-365">**Get-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="15ef6-366">**新 WorkloadManagementPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-366">**New-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="15ef6-367">**Remove-workloadmanagementpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-367">**Remove-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="15ef6-368">**Get-workloadpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-368">**Get-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="15ef6-369">**新 WorkloadPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-369">**New-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="15ef6-370">**Remove-workloadpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-370">**Remove-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="15ef6-371">**Set-workloadpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-371">**Set-WorkloadPolicy**</span></span>
    
### <a name="modified-cmdlets"></a><span data-ttu-id="15ef6-372">修改的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-372">Modified cmdlets</span></span>
<span data-ttu-id="15ef6-373"><a name="bk_update"> </a></span><span class="sxs-lookup"><span data-stu-id="15ef6-373"></span></span>

<span data-ttu-id="15ef6-374">以下 cmdlet 的输入或输出类型已在 Exchange 2013 中修改:</span><span class="sxs-lookup"><span data-stu-id="15ef6-374">The input or output types for following cmdlets were modified in Exchange 2013:</span></span>
  
- <span data-ttu-id="15ef6-375">**Clear-activesyncdevice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-375">**Clear-ActiveSyncDevice**</span></span>
    
- <span data-ttu-id="15ef6-376">**Remove-activesyncdevice**</span><span class="sxs-lookup"><span data-stu-id="15ef6-376">**Remove-ActiveSyncDevice**</span></span>
    
- <span data-ttu-id="15ef6-377">**Get-activesyncmailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-377">**Get-ActiveSyncMailboxPolicy**</span></span>
    
- <span data-ttu-id="15ef6-378">**新 ActiveSyncMailboxPolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-378">**New-ActiveSyncMailboxPolicy**</span></span>
    
- <span data-ttu-id="15ef6-379">**新 ActiveSyncVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="15ef6-379">**New-ActiveSyncVirtualDirectory**</span></span>
    
- <span data-ttu-id="15ef6-380">**新 AutodiscoverVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="15ef6-380">**New-AutodiscoverVirtualDirectory**</span></span>
    
- <span data-ttu-id="15ef6-381">**Set-availabilityconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-381">**Set-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="15ef6-382">**Enable-exchangecertificate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-382">**Enable-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="15ef6-383">**Export-exchangecertificate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-383">**Export-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="15ef6-384">**Import-exchangecertificate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-384">**Import-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="15ef6-385">**Remove-exchangecertificate**</span><span class="sxs-lookup"><span data-stu-id="15ef6-385">**Remove-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="15ef6-386">**Get-failedcontentindexdocuments**</span><span class="sxs-lookup"><span data-stu-id="15ef6-386">**Get-FailedContentIndexDocuments**</span></span>
    
- <span data-ttu-id="15ef6-387">**Get-federationinformation**</span><span class="sxs-lookup"><span data-stu-id="15ef6-387">**Get-FederationInformation**</span></span>
    
- <span data-ttu-id="15ef6-388">**新 HybridConfiguration**</span><span class="sxs-lookup"><span data-stu-id="15ef6-388">**New-HybridConfiguration**</span></span>
    
- <span data-ttu-id="15ef6-389">**Set-hybridconfiguration**</span><span class="sxs-lookup"><span data-stu-id="15ef6-389">**Set-HybridConfiguration**</span></span>
    
- <span data-ttu-id="15ef6-390">**新邮箱**</span><span class="sxs-lookup"><span data-stu-id="15ef6-390">**New-Mailbox**</span></span>
    
- <span data-ttu-id="15ef6-391">**Resume-mailboxdatabasecopy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-391">**Resume-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="15ef6-392">**Set-mailboxdatabasecopy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-392">**Set-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="15ef6-393">**挂起 MailboxDatabaseCopy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-393">**Suspend-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="15ef6-394">**Update-mailboxdatabasecopy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-394">**Update-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="15ef6-395">**Get-mailboxexportrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-395">**Get-MailboxExportRequest**</span></span>
    
- <span data-ttu-id="15ef6-396">**设置 MailboxExportRequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-396">**Set-MailboxExportRequest**</span></span>
    
- <span data-ttu-id="15ef6-397">**添加 MailboxFolderPermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-397">**Add-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="15ef6-398">**Remove-mailboxfolderpermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-398">**Remove-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="15ef6-399">**设置 MailboxFolderPermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-399">**Set-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="15ef6-400">**Get-mailboximportrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-400">**Get-MailboxImportRequest**</span></span>
    
- <span data-ttu-id="15ef6-401">**Set-mailboximportrequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-401">**Set-MailboxImportRequest**</span></span>
    
- <span data-ttu-id="15ef6-402">**Get-mailboxrestorerequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-402">**Get-MailboxRestoreRequest**</span></span>
    
- <span data-ttu-id="15ef6-403">**设置 MailboxRestoreRequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-403">**Set-MailboxRestoreRequest**</span></span>
    
- <span data-ttu-id="15ef6-404">**Get-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-404">**Get-MailboxSearch**</span></span>
    
- <span data-ttu-id="15ef6-405">**Remove-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-405">**Remove-MailboxSearch**</span></span>
    
- <span data-ttu-id="15ef6-406">**Set-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-406">**Set-MailboxSearch**</span></span>
    
- <span data-ttu-id="15ef6-407">**Start-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-407">**Start-MailboxSearch**</span></span>
    
- <span data-ttu-id="15ef6-408">**Stop-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-408">**Stop-MailboxSearch**</span></span>
    
- <span data-ttu-id="15ef6-409">**Disable-mailpublicfolder**</span><span class="sxs-lookup"><span data-stu-id="15ef6-409">**Disable-MailPublicFolder**</span></span>
    
- <span data-ttu-id="15ef6-410">**Get MailPublicFolder**</span><span class="sxs-lookup"><span data-stu-id="15ef6-410">**Get-MailPublicFolder**</span></span>
    
- <span data-ttu-id="15ef6-411">**设置 MailPublicFolder**</span><span class="sxs-lookup"><span data-stu-id="15ef6-411">**Set-MailPublicFolder**</span></span>
    
- <span data-ttu-id="15ef6-412">**Get-migrationbatch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-412">**Get-MigrationBatch**</span></span>
    
- <span data-ttu-id="15ef6-413">**新 MigrationBatch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-413">**New-MigrationBatch**</span></span>
    
- <span data-ttu-id="15ef6-414">**Set-migrationbatch**</span><span class="sxs-lookup"><span data-stu-id="15ef6-414">**Set-MigrationBatch**</span></span>
    
- <span data-ttu-id="15ef6-415">**测试 MigrationServerAvailability**</span><span class="sxs-lookup"><span data-stu-id="15ef6-415">**Test-MigrationServerAvailability**</span></span>
    
- <span data-ttu-id="15ef6-416">**Get-moverequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-416">**Get-MoveRequest**</span></span>
    
- <span data-ttu-id="15ef6-417">**新 OfflineAddressBook**</span><span class="sxs-lookup"><span data-stu-id="15ef6-417">**New-OfflineAddressBook**</span></span>
    
- <span data-ttu-id="15ef6-418">**Get-organizationconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-418">**Get-OrganizationConfig**</span></span>
    
- <span data-ttu-id="15ef6-419">**Set-organizationconfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-419">**Set-OrganizationConfig**</span></span>
    
- <span data-ttu-id="15ef6-420">**Test-outlookconnectivity**</span><span class="sxs-lookup"><span data-stu-id="15ef6-420">**Test-OutlookConnectivity**</span></span>
    
- <span data-ttu-id="15ef6-421">**测试 OutlookWebServices**</span><span class="sxs-lookup"><span data-stu-id="15ef6-421">**Test-OutlookWebServices**</span></span>
    
- <span data-ttu-id="15ef6-422">**Get-owamailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-422">**Get-OwaMailboxPolicy**</span></span>
    
- <span data-ttu-id="15ef6-423">**新 OwaVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="15ef6-423">**New-OwaVirtualDirectory**</span></span>
    
- <span data-ttu-id="15ef6-424">**新 PowerShellVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="15ef6-424">**New-PowerShellVirtualDirectory**</span></span>
    
- <span data-ttu-id="15ef6-425">**Get-publicfolder**</span><span class="sxs-lookup"><span data-stu-id="15ef6-425">**Get-PublicFolder**</span></span>
    
- <span data-ttu-id="15ef6-426">**新 PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="15ef6-426">**New-PublicFolder**</span></span>
    
- <span data-ttu-id="15ef6-427">**Set-publicfolder**</span><span class="sxs-lookup"><span data-stu-id="15ef6-427">**Set-PublicFolder**</span></span>
    
- <span data-ttu-id="15ef6-428">**添加 PublicFolderClientPermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-428">**Add-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="15ef6-429">**Get-publicfolderclientpermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-429">**Get-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="15ef6-430">**Remove-publicfolderclientpermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-430">**Remove-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="15ef6-431">**Get-publicfolderitemstatistics**</span><span class="sxs-lookup"><span data-stu-id="15ef6-431">**Get-PublicFolderItemStatistics**</span></span>
    
- <span data-ttu-id="15ef6-432">**Get-publicfolderstatistics**</span><span class="sxs-lookup"><span data-stu-id="15ef6-432">**Get-PublicFolderStatistics**</span></span>
    
- <span data-ttu-id="15ef6-433">**获取收件人**</span><span class="sxs-lookup"><span data-stu-id="15ef6-433">**Get-Recipient**</span></span>
    
- <span data-ttu-id="15ef6-434">**设置 ResourceConfig**</span><span class="sxs-lookup"><span data-stu-id="15ef6-434">**Set-ResourceConfig**</span></span>
    
- <span data-ttu-id="15ef6-435">**Test-webservicesconnectivity**</span><span class="sxs-lookup"><span data-stu-id="15ef6-435">**Test-WebServicesConnectivity**</span></span>
    
- <span data-ttu-id="15ef6-436">**新 WebServicesVirtualDirectory**</span><span class="sxs-lookup"><span data-stu-id="15ef6-436">**New-WebServicesVirtualDirectory**</span></span>
    
### <a name="removed-cmdlets"></a><span data-ttu-id="15ef6-437">删除的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-437">Removed cmdlets</span></span>
<span data-ttu-id="15ef6-438"><a name="bk_removed"> </a></span><span class="sxs-lookup"><span data-stu-id="15ef6-438"></span></span>

<span data-ttu-id="15ef6-439">从 Exchange 2013 删除了以下 cmdlet:</span><span class="sxs-lookup"><span data-stu-id="15ef6-439">The following cmdlets were removed from Exchange 2013:</span></span>
  
- <span data-ttu-id="15ef6-440">**更新 FileDistributionService**</span><span class="sxs-lookup"><span data-stu-id="15ef6-440">**Update-FileDistributionService**</span></span>
    
- <span data-ttu-id="15ef6-441">**还原邮箱**</span><span class="sxs-lookup"><span data-stu-id="15ef6-441">**Restore-Mailbox**</span></span>
    
- <span data-ttu-id="15ef6-442">**清理 MailboxDatabase**</span><span class="sxs-lookup"><span data-stu-id="15ef6-442">**Clean-MailboxDatabase**</span></span>
    
- <span data-ttu-id="15ef6-443">**完成迁移**</span><span class="sxs-lookup"><span data-stu-id="15ef6-443">**Complete-Migration**</span></span>
    
- <span data-ttu-id="15ef6-444">**Get MigrationStatus**</span><span class="sxs-lookup"><span data-stu-id="15ef6-444">**Get-MigrationStatus**</span></span>
    
- <span data-ttu-id="15ef6-445">**更新 PublicFolder**</span><span class="sxs-lookup"><span data-stu-id="15ef6-445">**Update-PublicFolder**</span></span>
    
- <span data-ttu-id="15ef6-446">**添加 PublicFolderAdministrativePermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-446">**Add-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="15ef6-447">**Get PublicFolderAdministrativePermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-447">**Get-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="15ef6-448">**删除 PublicFolderAdministrativePermission**</span><span class="sxs-lookup"><span data-stu-id="15ef6-448">**Remove-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="15ef6-449">**新 PublicFolderDatabase**</span><span class="sxs-lookup"><span data-stu-id="15ef6-449">**New-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="15ef6-450">**删除 PublicFolderDatabase**</span><span class="sxs-lookup"><span data-stu-id="15ef6-450">**Remove-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="15ef6-451">**设置 PublicFolderDatabase**</span><span class="sxs-lookup"><span data-stu-id="15ef6-451">**Set-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="15ef6-452">**新 PublicFolderDatabaseRepairRequest**</span><span class="sxs-lookup"><span data-stu-id="15ef6-452">**New-PublicFolderDatabaseRepairRequest**</span></span>
    
- <span data-ttu-id="15ef6-453">**更新 PublicFolderHierarchy**</span><span class="sxs-lookup"><span data-stu-id="15ef6-453">**Update-PublicFolderHierarchy**</span></span>
    
- <span data-ttu-id="15ef6-454">**继续 PublicFolderReplication**</span><span class="sxs-lookup"><span data-stu-id="15ef6-454">**Resume-PublicFolderReplication**</span></span>
    
- <span data-ttu-id="15ef6-455">**挂起 PublicFolderReplication**</span><span class="sxs-lookup"><span data-stu-id="15ef6-455">**Suspend-PublicFolderReplication**</span></span>
    
- <span data-ttu-id="15ef6-456">**开始 RetentionAutoTagLearning**</span><span class="sxs-lookup"><span data-stu-id="15ef6-456">**Start-RetentionAutoTagLearning**</span></span>
    
- <span data-ttu-id="15ef6-457">**测试 SystemHealth**</span><span class="sxs-lookup"><span data-stu-id="15ef6-457">**Test-SystemHealth**</span></span>
    
- <span data-ttu-id="15ef6-458">**禁用 UMServer**</span><span class="sxs-lookup"><span data-stu-id="15ef6-458">**Disable-UMServer**</span></span>
    
- <span data-ttu-id="15ef6-459">**启用 UMServer**</span><span class="sxs-lookup"><span data-stu-id="15ef6-459">**Enable-UMServer**</span></span>
    
- <span data-ttu-id="15ef6-460">**Get-umserver**</span><span class="sxs-lookup"><span data-stu-id="15ef6-460">**Get-UMServer**</span></span>
    
- <span data-ttu-id="15ef6-461">**设置 UMServer**</span><span class="sxs-lookup"><span data-stu-id="15ef6-461">**Set-UMServer**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15ef6-462">另请参阅</span><span class="sxs-lookup"><span data-stu-id="15ef6-462">See also</span></span>

- [<span data-ttu-id="15ef6-463">Exchange 命令行管理程序 cmdlet 输入和输出类型</span><span class="sxs-lookup"><span data-stu-id="15ef6-463">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)    
- [<span data-ttu-id="15ef6-464">使用 Exchange 命令行管理程序中获取邮件用户的列表</span><span class="sxs-lookup"><span data-stu-id="15ef6-464">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)    
- [<span data-ttu-id="15ef6-465">Exchange 2013 cmdlet</span><span class="sxs-lookup"><span data-stu-id="15ef6-465">Exchange 2013 cmdlets</span></span>](http://technet.microsoft.com/zh-cn/library/bb124413%28v=exchg.150%29.aspx)
    

