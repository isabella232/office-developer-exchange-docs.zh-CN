---
title: 新的和更新的 Exchange 命令行管理程序 cmdlet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5941a439-94d2-4133-81fc-7240863a13df
description: 查找有关 exchange 中 Exchange 命令行管理程序中的新增功能的信息。
ms.openlocfilehash: bda6607be20f2a21bc22d472d63615d46634d8ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457142"
---
# <a name="new-and-updated-exchange-management-shell-cmdlets"></a><span data-ttu-id="e2073-103">新的和更新的 Exchange 命令行管理程序 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-103">New and updated Exchange Management Shell cmdlets</span></span>

<span data-ttu-id="e2073-104">查找有关 exchange 中 Exchange 命令行管理程序中的新增功能的信息。</span><span class="sxs-lookup"><span data-stu-id="e2073-104">Find information about what's new in the Exchange Management Shell in Exchange.</span></span>
  
<span data-ttu-id="e2073-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="e2073-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="e2073-106">本文提供有关以下内容的信息：新的 Exchange 命令行管理程序 cmdlet、在中修改的 cmdlet 以及从 Exchange Online、Exchange Online （作为 Office 365 的一部分）或 Exchange 的本地版本中删除的 cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e2073-106">This article provides information about new Exchange Management shell cmdlets, cmdlets that were modified in, and cmdlets that were removed from Exchange Online, Exchange Online as part of Office 365, or an on-premises version of Exchange.</span></span>
  
## <a name="new-and-updated-cmdlets-in-exchange-2013-sp1"></a><span data-ttu-id="e2073-107">Exchange 2013 SP1 中的新增和更新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-107">New and updated cmdlets in Exchange 2013 SP1</span></span>

### <a name="new-cmdlets"></a><span data-ttu-id="e2073-108">New cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-108">New cmdlets</span></span>

<span data-ttu-id="e2073-109">Build 15.00.0847.032 （Exchange Server 2013 SP1）中引入了以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e2073-109">The following cmdlets were introduced in build 15.00.0847.032 (Exchange Server 2013 SP1):</span></span>
  
- <span data-ttu-id="e2073-110">**Authredirect-bearer**</span><span class="sxs-lookup"><span data-stu-id="e2073-110">**Get-AuthRedirect**</span></span>
    
- <span data-ttu-id="e2073-111">**新 Authredirect-bearer**</span><span class="sxs-lookup"><span data-stu-id="e2073-111">**New-AuthRedirect**</span></span>
    
- <span data-ttu-id="e2073-112">**Authredirect-bearer**</span><span class="sxs-lookup"><span data-stu-id="e2073-112">**Remove-AuthRedirect**</span></span>
    
- <span data-ttu-id="e2073-113">**Authredirect-bearer**</span><span class="sxs-lookup"><span data-stu-id="e2073-113">**Set-AuthRedirect**</span></span>
    
- <span data-ttu-id="e2073-114">**新 New-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="e2073-114">**New-DataClassification**</span></span>
    
- <span data-ttu-id="e2073-115">**New-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="e2073-115">**Remove-DataClassification**</span></span>
    
- <span data-ttu-id="e2073-116">**New-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="e2073-116">**Set-DataClassification**</span></span>
    
- <span data-ttu-id="e2073-117">**新-指纹**</span><span class="sxs-lookup"><span data-stu-id="e2073-117">**New-FingerPrint**</span></span>
    
- <span data-ttu-id="e2073-118">**MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="e2073-118">**Get-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="e2073-119">**新 MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="e2073-119">**New-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="e2073-120">**MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="e2073-120">**Remove-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="e2073-121">**MapiVirtualDirectory\***</span><span class="sxs-lookup"><span data-stu-id="e2073-121">**Set-MapiVirtualDirectory\***</span></span>
    
- <span data-ttu-id="e2073-122">**Set-omeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="e2073-122">**Get-OMEConfiguration**</span></span>
    
- <span data-ttu-id="e2073-123">**Set-omeconfiguration**</span><span class="sxs-lookup"><span data-stu-id="e2073-123">**Set-OMEConfiguration**</span></span>
    
- <span data-ttu-id="e2073-124">**Get-smimeconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-124">**Get-SmimeConfig**</span></span>
    
- <span data-ttu-id="e2073-125">**Get-smimeconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-125">**Set-SmimeConfig**</span></span>
    
- <span data-ttu-id="e2073-126">**Get-intraorganizationconfiguration**</span><span class="sxs-lookup"><span data-stu-id="e2073-126">**Get-IntraOrganizationConfiguration**</span></span>
    
- <span data-ttu-id="e2073-127">**IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-127">**Get-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="e2073-128">**新 IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-128">**New-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="e2073-129">**IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-129">**Remove-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="e2073-130">**IntraOrganizationConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-130">**Set-IntraOrganizationConnector**</span></span>
    
- <span data-ttu-id="e2073-131">**Start-historicalsearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-131">**Get-HistoricalSearch**</span></span>
    
- <span data-ttu-id="e2073-132">**启动-Start-historicalsearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-132">**Start-HistoricalSearch**</span></span>
    
- <span data-ttu-id="e2073-133">**Start-historicalsearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-133">**Stop-HistoricalSearch**</span></span>
    
- <span data-ttu-id="e2073-134">**新 Set-searchdocumentformat**</span><span class="sxs-lookup"><span data-stu-id="e2073-134">**New-SearchDocumentFormat**</span></span>
    
- <span data-ttu-id="e2073-135">**Set-searchdocumentformat**</span><span class="sxs-lookup"><span data-stu-id="e2073-135">**Remove-SearchDocumentFormat**</span></span>
    
### <a name="updated-cmdlets"></a><span data-ttu-id="e2073-136">更新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-136">Updated cmdlets</span></span>

<span data-ttu-id="e2073-137">生成15.00.0847.032 中更新了以下 cmdlet （Exchange 2013 SP1）：</span><span class="sxs-lookup"><span data-stu-id="e2073-137">The following cmdlets were updated in build 15.00.0847.032 (Exchange 2013 SP1):</span></span>
  
- <span data-ttu-id="e2073-138">**AuditLogSearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-138">**Get-AuditLogSearch**</span></span>
    
- <span data-ttu-id="e2073-139">**Get-quarantinemessage**</span><span class="sxs-lookup"><span data-stu-id="e2073-139">**Get-QuarantineMessage**</span></span>
    
- <span data-ttu-id="e2073-140">**新 InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-140">**New-InboundConnector**</span></span>
    
- <span data-ttu-id="e2073-141">**新 Set-mailboxdatabase**</span><span class="sxs-lookup"><span data-stu-id="e2073-141">**New-MailboxDatabase**</span></span>
    
- <span data-ttu-id="e2073-142">**新 Get-publicfoldermoverequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-142">**New-PublicFolderMoveRequest**</span></span>
    
- <span data-ttu-id="e2073-143">**新 New-transportrule**</span><span class="sxs-lookup"><span data-stu-id="e2073-143">**New-TransportRule**</span></span>
    
- <span data-ttu-id="e2073-144">**Set-frontendtransportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-144">**Set-FrontendTransportService**</span></span>
    
- <span data-ttu-id="e2073-145">**InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-145">**Set-InboundConnector**</span></span>
    
- <span data-ttu-id="e2073-146">**Set-Mailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-146">**Set-Mailbox**</span></span>
    
- <span data-ttu-id="e2073-147">**Set-mailboxtransportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-147">**Set-MailboxTransportService**</span></span>
    
- <span data-ttu-id="e2073-148">**New-moverequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-148">**Set-MoveRequest**</span></span>
    
- <span data-ttu-id="e2073-149">**Set-organizationconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-149">**Set-OrganizationConfig**</span></span>
    
- <span data-ttu-id="e2073-150">**Set-owamailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-150">**Set-OwaMailboxPolicy**</span></span>
    
- <span data-ttu-id="e2073-151">**Set-owavirtualdirectory**</span><span class="sxs-lookup"><span data-stu-id="e2073-151">**Set-OwaVirtualDirectory**</span></span>
    
- <span data-ttu-id="e2073-152">**Set-transportconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-152">**Set-TransportConfig**</span></span>
    
- <span data-ttu-id="e2073-153">**New-transportrule**</span><span class="sxs-lookup"><span data-stu-id="e2073-153">**Set-TransportRule**</span></span>
    
- <span data-ttu-id="e2073-154">**Set-transportserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-154">**Set-TransportServer**</span></span>
    
- <span data-ttu-id="e2073-155">**Set-transportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-155">**Set-TransportService**</span></span>
    
- <span data-ttu-id="e2073-156">**Test-MRSHealth**</span><span class="sxs-lookup"><span data-stu-id="e2073-156">**Test-MRSHealth**</span></span>
    
- <span data-ttu-id="e2073-157">**Test-Test-oauthconnectivity**</span><span class="sxs-lookup"><span data-stu-id="e2073-157">**Test-OAuthConnectivity**</span></span>
    
### <a name="removed-cmdlets"></a><span data-ttu-id="e2073-158">删除的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-158">Removed cmdlets</span></span>

<span data-ttu-id="e2073-159">已从 build 15.00.0847.032 中删除了以下 cmdlet （Exchange 2013 SP1）：</span><span class="sxs-lookup"><span data-stu-id="e2073-159">The following cmdlets were removed from build 15.00.0847.032 (Exchange 2013 SP1):</span></span>
  
- <span data-ttu-id="e2073-160">**New-availabilityreportoutage**</span><span class="sxs-lookup"><span data-stu-id="e2073-160">**Get-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="e2073-161">**新 New-availabilityreportoutage**</span><span class="sxs-lookup"><span data-stu-id="e2073-161">**New-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="e2073-162">**New-availabilityreportoutage**</span><span class="sxs-lookup"><span data-stu-id="e2073-162">**Remove-AvailabilityReportOutage**</span></span>
    
- <span data-ttu-id="e2073-163">**New-availabilityreportoutage**</span><span class="sxs-lookup"><span data-stu-id="e2073-163">**Set-AvailabilityReportOutage**</span></span>
    
## <a name="new-and-updated-cmdlets-in-exchange-2013"></a><span data-ttu-id="e2073-164">Exchange 2013 中新增和更新的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-164">New and updated cmdlets in Exchange 2013</span></span>

### <a name="new-cmdlets"></a><span data-ttu-id="e2073-165">New cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-165">New cmdlets</span></span>
<span data-ttu-id="e2073-166"><a name="bk_new"> </a></span><span class="sxs-lookup"><span data-stu-id="e2073-166"><a name="bk_new"> </a></span></span>

<span data-ttu-id="e2073-167">Exchange 2013 中引入了以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e2073-167">The following cmdlets were introduced in Exchange 2013:</span></span>
  
- <span data-ttu-id="e2073-168">**Set-activesyncdeviceautoblockthreshold**</span><span class="sxs-lookup"><span data-stu-id="e2073-168">**Get-ActiveSyncDeviceAutoblockThreshold**</span></span>
    
- <span data-ttu-id="e2073-169">**Set-activesyncdeviceautoblockthreshold**</span><span class="sxs-lookup"><span data-stu-id="e2073-169">**Set-ActiveSyncDeviceAutoblockThreshold**</span></span>
    
- <span data-ttu-id="e2073-170">**Disable-App**</span><span class="sxs-lookup"><span data-stu-id="e2073-170">**Disable-App**</span></span>
    
- <span data-ttu-id="e2073-171">**启用-应用程序**</span><span class="sxs-lookup"><span data-stu-id="e2073-171">**Enable-App**</span></span>
    
- <span data-ttu-id="e2073-172">**获取-应用**</span><span class="sxs-lookup"><span data-stu-id="e2073-172">**Get-App**</span></span>
    
- <span data-ttu-id="e2073-173">**新应用程序**</span><span class="sxs-lookup"><span data-stu-id="e2073-173">**New-App**</span></span>
    
- <span data-ttu-id="e2073-174">**Remove-App**</span><span class="sxs-lookup"><span data-stu-id="e2073-174">**Remove-App**</span></span>
    
- <span data-ttu-id="e2073-175">**Set-App**</span><span class="sxs-lookup"><span data-stu-id="e2073-175">**Set-App**</span></span>
    
- <span data-ttu-id="e2073-176">**AuthConfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-176">**Get-AuthConfig**</span></span>
    
- <span data-ttu-id="e2073-177">**AuthConfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-177">**Set-AuthConfig**</span></span>
    
- <span data-ttu-id="e2073-178">**Get-authserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-178">**Get-AuthServer**</span></span>
    
- <span data-ttu-id="e2073-179">**新 Get-authserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-179">**New-AuthServer**</span></span>
    
- <span data-ttu-id="e2073-180">**Get-authserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-180">**Remove-AuthServer**</span></span>
    
- <span data-ttu-id="e2073-181">**Get-authserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-181">**Set-AuthServer**</span></span>
    
- <span data-ttu-id="e2073-182">**新 Get-availabilityconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-182">**New-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="e2073-183">**Get-availabilityconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-183">**Remove-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="e2073-184">**CalendarDiagnosticAnalysis**</span><span class="sxs-lookup"><span data-stu-id="e2073-184">**Get-CalendarDiagnosticAnalysis**</span></span>
    
- <span data-ttu-id="e2073-185">**Get-classificationrulecollection**</span><span class="sxs-lookup"><span data-stu-id="e2073-185">**Get-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="e2073-186">**新 Get-classificationrulecollection**</span><span class="sxs-lookup"><span data-stu-id="e2073-186">**New-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="e2073-187">**Get-classificationrulecollection**</span><span class="sxs-lookup"><span data-stu-id="e2073-187">**Remove-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="e2073-188">**Get-classificationrulecollection**</span><span class="sxs-lookup"><span data-stu-id="e2073-188">**Set-ClassificationRuleCollection**</span></span>
    
- <span data-ttu-id="e2073-189">**Get-connectsubscription**</span><span class="sxs-lookup"><span data-stu-id="e2073-189">**Get-ConnectSubscription**</span></span>
    
- <span data-ttu-id="e2073-190">**新 Get-connectsubscription**</span><span class="sxs-lookup"><span data-stu-id="e2073-190">**New-ConnectSubscription**</span></span>
    
- <span data-ttu-id="e2073-191">**Get-connectsubscription**</span><span class="sxs-lookup"><span data-stu-id="e2073-191">**Remove-ConnectSubscription**</span></span>
    
- <span data-ttu-id="e2073-192">**Get-connectsubscription**</span><span class="sxs-lookup"><span data-stu-id="e2073-192">**Set-ConnectSubscription**</span></span>
    
- <span data-ttu-id="e2073-193">**New-dataclassification**</span><span class="sxs-lookup"><span data-stu-id="e2073-193">**Get-DataClassification**</span></span>
    
- <span data-ttu-id="e2073-194">**Get-dataclassificationconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-194">**Get-DataClassificationConfig**</span></span>
    
- <span data-ttu-id="e2073-195">**DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-195">**Get-DlpPolicy**</span></span>
    
- <span data-ttu-id="e2073-196">**新 DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-196">**New-DlpPolicy**</span></span>
    
- <span data-ttu-id="e2073-197">**DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-197">**Remove-DlpPolicy**</span></span>
    
- <span data-ttu-id="e2073-198">**DlpPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-198">**Set-DlpPolicy**</span></span>
    
- <span data-ttu-id="e2073-199">**Export-DlpPolicyCollection**</span><span class="sxs-lookup"><span data-stu-id="e2073-199">**Export-DlpPolicyCollection**</span></span>
    
- <span data-ttu-id="e2073-200">**Import-DlpPolicyCollection**</span><span class="sxs-lookup"><span data-stu-id="e2073-200">**Import-DlpPolicyCollection**</span></span>
    
- <span data-ttu-id="e2073-201">**Remove-dlppolicytemplate**</span><span class="sxs-lookup"><span data-stu-id="e2073-201">**Get-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="e2073-202">**Import-Remove-dlppolicytemplate**</span><span class="sxs-lookup"><span data-stu-id="e2073-202">**Import-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="e2073-203">**Remove-dlppolicytemplate**</span><span class="sxs-lookup"><span data-stu-id="e2073-203">**Remove-DlpPolicyTemplate**</span></span>
    
- <span data-ttu-id="e2073-204">**ExchangeServerAccessLicense**</span><span class="sxs-lookup"><span data-stu-id="e2073-204">**Get-ExchangeServerAccessLicense**</span></span>
    
- <span data-ttu-id="e2073-205">**ExchangeServerAccessLicenseUser**</span><span class="sxs-lookup"><span data-stu-id="e2073-205">**Get-ExchangeServerAccessLicenseUser**</span></span>
    
- <span data-ttu-id="e2073-206">**FfoMigrationReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-206">**Get-FfoMigrationReport**</span></span>
    
- <span data-ttu-id="e2073-207">**Set-frontendtransportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-207">**Get-FrontendTransportService**</span></span>
    
- <span data-ttu-id="e2073-208">**Set-frontendtransportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-208">**Set-FrontendTransportService**</span></span>
    
- <span data-ttu-id="e2073-209">**外接 Get-globalmonitoringoverride**</span><span class="sxs-lookup"><span data-stu-id="e2073-209">**Add-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="e2073-210">**Get-globalmonitoringoverride**</span><span class="sxs-lookup"><span data-stu-id="e2073-210">**Get-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="e2073-211">**Get-globalmonitoringoverride**</span><span class="sxs-lookup"><span data-stu-id="e2073-211">**Remove-GlobalMonitoringOverride**</span></span>
    
- <span data-ttu-id="e2073-212">**Get-groupactivityreport**</span><span class="sxs-lookup"><span data-stu-id="e2073-212">**Get-GroupActivityReport**</span></span>
    
- <span data-ttu-id="e2073-213">**HealthReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-213">**Get-HealthReport**</span></span>
    
- <span data-ttu-id="e2073-214">**Set-hostedconnectionfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-214">**Get-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-215">**新 Set-hostedconnectionfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-215">**New-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-216">**Set-hostedconnectionfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-216">**Remove-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-217">**Set-hostedconnectionfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-217">**Set-HostedConnectionFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-218">**Set-hostedcontentfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-218">**Get-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-219">**新 Set-hostedcontentfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-219">**New-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-220">**Set-hostedcontentfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-220">**Remove-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-221">**Set-hostedcontentfilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-221">**Set-HostedContentFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-222">**HostedOutboundSpamFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-222">**Get-HostedOutboundSpamFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-223">**HostedOutboundSpamFilterPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-223">**Set-HostedOutboundSpamFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-224">**HybridConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e2073-224">**Remove-HybridConfiguration**</span></span>
    
- <span data-ttu-id="e2073-225">**Get-hybridmailflow**</span><span class="sxs-lookup"><span data-stu-id="e2073-225">**Get-HybridMailflow**</span></span>
    
- <span data-ttu-id="e2073-226">**Get-hybridmailflow**</span><span class="sxs-lookup"><span data-stu-id="e2073-226">**Set-HybridMailflow**</span></span>
    
- <span data-ttu-id="e2073-227">**HybridMailflowDatacenterIPs**</span><span class="sxs-lookup"><span data-stu-id="e2073-227">**Get-HybridMailflowDatacenterIPs**</span></span>
    
- <span data-ttu-id="e2073-228">**InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-228">**Get-InboundConnector**</span></span>
    
- <span data-ttu-id="e2073-229">**新 InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-229">**New-InboundConnector**</span></span>
    
- <span data-ttu-id="e2073-230">**InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-230">**Remove-InboundConnector**</span></span>
    
- <span data-ttu-id="e2073-231">**InboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-231">**Set-InboundConnector**</span></span>
    
- <span data-ttu-id="e2073-232">**Get-mailboxactivityreport**</span><span class="sxs-lookup"><span data-stu-id="e2073-232">**Get-MailboxActivityReport**</span></span>
    
- <span data-ttu-id="e2073-233">**Disable-MailboxQuarantine**</span><span class="sxs-lookup"><span data-stu-id="e2073-233">**Disable-MailboxQuarantine**</span></span>
    
- <span data-ttu-id="e2073-234">**Enable-MailboxQuarantine**</span><span class="sxs-lookup"><span data-stu-id="e2073-234">**Enable-MailboxQuarantine**</span></span>
    
- <span data-ttu-id="e2073-235">**Set-mailboxtransportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-235">**Get-MailboxTransportService**</span></span>
    
- <span data-ttu-id="e2073-236">**Set-mailboxtransportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-236">**Set-MailboxTransportService**</span></span>
    
- <span data-ttu-id="e2073-237">**MailDetailDlpPolicyReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-237">**Get-MailDetailDlpPolicyReport**</span></span>
    
- <span data-ttu-id="e2073-238">**MailDetailMalwareReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-238">**Get-MailDetailMalwareReport**</span></span>
    
- <span data-ttu-id="e2073-239">**MailDetailReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-239">**Get-MailDetailReport**</span></span>
    
- <span data-ttu-id="e2073-240">**MailDetailSpamReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-240">**Get-MailDetailSpamReport**</span></span>
    
- <span data-ttu-id="e2073-241">**Get-maildetailtransportrulereport**</span><span class="sxs-lookup"><span data-stu-id="e2073-241">**Get-MailDetailTransportRuleReport**</span></span>
    
- <span data-ttu-id="e2073-242">**Get-mailfilterlistreport**</span><span class="sxs-lookup"><span data-stu-id="e2073-242">**Get-MailFilterListReport**</span></span>
    
- <span data-ttu-id="e2073-243">**MailTrafficPolicyReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-243">**Get-MailTrafficPolicyReport**</span></span>
    
- <span data-ttu-id="e2073-244">**MailTrafficReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-244">**Get-MailTrafficReport**</span></span>
    
- <span data-ttu-id="e2073-245">**MailTrafficSummaryReport**</span><span class="sxs-lookup"><span data-stu-id="e2073-245">**Get-MailTrafficSummaryReport**</span></span>
    
- <span data-ttu-id="e2073-246">**Get-mailtraffictopreport**</span><span class="sxs-lookup"><span data-stu-id="e2073-246">**Get-MailTrafficTopReport**</span></span>
    
- <span data-ttu-id="e2073-247">**MalwareFilteringServer**</span><span class="sxs-lookup"><span data-stu-id="e2073-247">**Get-MalwareFilteringServer**</span></span>
    
- <span data-ttu-id="e2073-248">**MalwareFilteringServer**</span><span class="sxs-lookup"><span data-stu-id="e2073-248">**Set-MalwareFilteringServer**</span></span>
    
- <span data-ttu-id="e2073-249">**Get-malwarefilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-249">**Get-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-250">**新 Get-malwarefilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-250">**New-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-251">**Get-malwarefilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-251">**Remove-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-252">**Get-malwarefilterpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-252">**Set-MalwareFilterPolicy**</span></span>
    
- <span data-ttu-id="e2073-253">**MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="e2073-253">**Get-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="e2073-254">**MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="e2073-254">**Remove-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="e2073-255">**Resume-MalwareFilterRecoveryItem**</span><span class="sxs-lookup"><span data-stu-id="e2073-255">**Resume-MalwareFilterRecoveryItem**</span></span>
    
- <span data-ttu-id="e2073-256">**发送 MapiSubmitSystemProbe**</span><span class="sxs-lookup"><span data-stu-id="e2073-256">**Send-MapiSubmitSystemProbe**</span></span>
    
- <span data-ttu-id="e2073-257">**Redirect-Message**</span><span class="sxs-lookup"><span data-stu-id="e2073-257">**Redirect-Message**</span></span>
    
- <span data-ttu-id="e2073-258">**MessageTrace**</span><span class="sxs-lookup"><span data-stu-id="e2073-258">**Get-MessageTrace**</span></span>
    
- <span data-ttu-id="e2073-259">**MessageTraceDetail**</span><span class="sxs-lookup"><span data-stu-id="e2073-259">**Get-MessageTraceDetail**</span></span>
    
- <span data-ttu-id="e2073-260">**完整-New-migrationbatch**</span><span class="sxs-lookup"><span data-stu-id="e2073-260">**Complete-MigrationBatch**</span></span>
    
- <span data-ttu-id="e2073-261">**New-migrationbatch**</span><span class="sxs-lookup"><span data-stu-id="e2073-261">**Remove-MigrationBatch**</span></span>
    
- <span data-ttu-id="e2073-262">**Get-migrationconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-262">**Get-MigrationConfig**</span></span>
    
- <span data-ttu-id="e2073-263">**Get-migrationconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-263">**Set-MigrationConfig**</span></span>
    
- <span data-ttu-id="e2073-264">**New-migrationendpoint**</span><span class="sxs-lookup"><span data-stu-id="e2073-264">**Get-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="e2073-265">**新 New-migrationendpoint**</span><span class="sxs-lookup"><span data-stu-id="e2073-265">**New-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="e2073-266">**New-migrationendpoint**</span><span class="sxs-lookup"><span data-stu-id="e2073-266">**Remove-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="e2073-267">**New-migrationendpoint**</span><span class="sxs-lookup"><span data-stu-id="e2073-267">**Set-MigrationEndpoint**</span></span>
    
- <span data-ttu-id="e2073-268">**MigrationStatistics**</span><span class="sxs-lookup"><span data-stu-id="e2073-268">**Get-MigrationStatistics**</span></span>
    
- <span data-ttu-id="e2073-269">**Get-migrationuser**</span><span class="sxs-lookup"><span data-stu-id="e2073-269">**Get-MigrationUser**</span></span>
    
- <span data-ttu-id="e2073-270">**Get-migrationuser**</span><span class="sxs-lookup"><span data-stu-id="e2073-270">**Remove-MigrationUser**</span></span>
    
- <span data-ttu-id="e2073-271">**Get-migrationuserstatistics**</span><span class="sxs-lookup"><span data-stu-id="e2073-271">**Get-MigrationUserStatistics**</span></span>
    
- <span data-ttu-id="e2073-272">**Clear-Clear-mobiledevice**</span><span class="sxs-lookup"><span data-stu-id="e2073-272">**Clear-MobileDevice**</span></span>
    
- <span data-ttu-id="e2073-273">**Clear-mobiledevice**</span><span class="sxs-lookup"><span data-stu-id="e2073-273">**Get-MobileDevice**</span></span>
    
- <span data-ttu-id="e2073-274">**Clear-mobiledevice**</span><span class="sxs-lookup"><span data-stu-id="e2073-274">**Remove-MobileDevice**</span></span>
    
- <span data-ttu-id="e2073-275">**New-mobiledevicemailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-275">**Get-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="e2073-276">**新 New-mobiledevicemailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-276">**New-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="e2073-277">**New-mobiledevicemailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-277">**Remove-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="e2073-278">**New-mobiledevicemailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-278">**Set-MobileDeviceMailboxPolicy**</span></span>
    
- <span data-ttu-id="e2073-279">**MobileDeviceStatistics**</span><span class="sxs-lookup"><span data-stu-id="e2073-279">**Get-MobileDeviceStatistics**</span></span>
    
- <span data-ttu-id="e2073-280">**MonitoringItemHelp**</span><span class="sxs-lookup"><span data-stu-id="e2073-280">**Get-MonitoringItemHelp**</span></span>
    
- <span data-ttu-id="e2073-281">**MonitoringItemIdentity**</span><span class="sxs-lookup"><span data-stu-id="e2073-281">**Get-MonitoringItemIdentity**</span></span>
    
- <span data-ttu-id="e2073-282">**调用 MonitoringProbe**</span><span class="sxs-lookup"><span data-stu-id="e2073-282">**Invoke-MonitoringProbe**</span></span>
    
- <span data-ttu-id="e2073-283">**Get 通知**</span><span class="sxs-lookup"><span data-stu-id="e2073-283">**Get-Notification**</span></span>
    
- <span data-ttu-id="e2073-284">**Set-通知**</span><span class="sxs-lookup"><span data-stu-id="e2073-284">**Set-Notification**</span></span>
    
- <span data-ttu-id="e2073-285">**Test-Test-oauthconnectivity**</span><span class="sxs-lookup"><span data-stu-id="e2073-285">**Test-OAuthConnectivity**</span></span>
    
- <span data-ttu-id="e2073-286">**OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="e2073-286">**Get-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="e2073-287">**新 OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="e2073-287">**New-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="e2073-288">**OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="e2073-288">**Remove-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="e2073-289">**OnPremisesOrganization**</span><span class="sxs-lookup"><span data-stu-id="e2073-289">**Set-OnPremisesOrganization**</span></span>
    
- <span data-ttu-id="e2073-290">**Enable-OrganizationCustomization**</span><span class="sxs-lookup"><span data-stu-id="e2073-290">**Enable-OrganizationCustomization**</span></span>
    
- <span data-ttu-id="e2073-291">**OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-291">**Get-OutboundConnector**</span></span>
    
- <span data-ttu-id="e2073-292">**新 OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-292">**New-OutboundConnector**</span></span>
    
- <span data-ttu-id="e2073-293">**OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-293">**Remove-OutboundConnector**</span></span>
    
- <span data-ttu-id="e2073-294">**OutboundConnector**</span><span class="sxs-lookup"><span data-stu-id="e2073-294">**Set-OutboundConnector**</span></span>
    
- <span data-ttu-id="e2073-295">**Get-partnerapplication**</span><span class="sxs-lookup"><span data-stu-id="e2073-295">**Get-PartnerApplication**</span></span>
    
- <span data-ttu-id="e2073-296">**新 Get-partnerapplication**</span><span class="sxs-lookup"><span data-stu-id="e2073-296">**New-PartnerApplication**</span></span>
    
- <span data-ttu-id="e2073-297">**Get-partnerapplication**</span><span class="sxs-lookup"><span data-stu-id="e2073-297">**Remove-PartnerApplication**</span></span>
    
- <span data-ttu-id="e2073-298">**Get-partnerapplication**</span><span class="sxs-lookup"><span data-stu-id="e2073-298">**Set-PartnerApplication**</span></span>
    
- <span data-ttu-id="e2073-299">**Get-pendingfederateddomain**</span><span class="sxs-lookup"><span data-stu-id="e2073-299">**Get-PendingFederatedDomain**</span></span>
    
- <span data-ttu-id="e2073-300">**Get-pendingfederateddomain**</span><span class="sxs-lookup"><span data-stu-id="e2073-300">**Set-PendingFederatedDomain**</span></span>
    
- <span data-ttu-id="e2073-301">**PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-301">**Get-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="e2073-302">**新 PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-302">**New-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="e2073-303">**PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-303">**Remove-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="e2073-304">**PolicyTipConfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-304">**Set-PolicyTipConfig**</span></span>
    
- <span data-ttu-id="e2073-305">**Dump-Dump-provisioningcache**</span><span class="sxs-lookup"><span data-stu-id="e2073-305">**Dump-ProvisioningCache**</span></span>
    
- <span data-ttu-id="e2073-306">**Reset-Dump-provisioningcache**</span><span class="sxs-lookup"><span data-stu-id="e2073-306">**Reset-ProvisioningCache**</span></span>
    
- <span data-ttu-id="e2073-307">**更新-PublicFolderMailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-307">**Update-PublicFolderMailbox**</span></span>
    
- <span data-ttu-id="e2073-308">**PublicFolderMailboxDiagnostics**</span><span class="sxs-lookup"><span data-stu-id="e2073-308">**Get-PublicFolderMailboxDiagnostics**</span></span>
    
- <span data-ttu-id="e2073-309">**Set-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-309">**Get-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="e2073-310">**新 Set-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-310">**New-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="e2073-311">**Set-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-311">**Remove-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="e2073-312">**Resume-Set-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-312">**Resume-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="e2073-313">**Set-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-313">**Set-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="e2073-314">**挂起-Set-publicfoldermigrationrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-314">**Suspend-PublicFolderMigrationRequest**</span></span>
    
- <span data-ttu-id="e2073-315">**Get-publicfoldermigrationrequeststatistics**</span><span class="sxs-lookup"><span data-stu-id="e2073-315">**Get-PublicFolderMigrationRequestStatistics**</span></span>
    
- <span data-ttu-id="e2073-316">**Get-quarantinemessage**</span><span class="sxs-lookup"><span data-stu-id="e2073-316">**Get-QuarantineMessage**</span></span>
    
- <span data-ttu-id="e2073-317">**发布-Get-quarantinemessage**</span><span class="sxs-lookup"><span data-stu-id="e2073-317">**Release-QuarantineMessage**</span></span>
    
- <span data-ttu-id="e2073-318">**Get-queuedigest**</span><span class="sxs-lookup"><span data-stu-id="e2073-318">**Get-QueueDigest**</span></span>
    
- <span data-ttu-id="e2073-319">**Get-resourcepolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-319">**Get-ResourcePolicy**</span></span>
    
- <span data-ttu-id="e2073-320">**新 Get-resourcepolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-320">**New-ResourcePolicy**</span></span>
    
- <span data-ttu-id="e2073-321">**Get-resourcepolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-321">**Remove-ResourcePolicy**</span></span>
    
- <span data-ttu-id="e2073-322">**Get-resourcepolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-322">**Set-ResourcePolicy**</span></span>
    
- <span data-ttu-id="e2073-323">**外接 ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-323">**Add-ResubmitRequest**</span></span>
    
- <span data-ttu-id="e2073-324">**ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-324">**Get-ResubmitRequest**</span></span>
    
- <span data-ttu-id="e2073-325">**ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-325">**Remove-ResubmitRequest**</span></span>
    
- <span data-ttu-id="e2073-326">**ResubmitRequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-326">**Set-ResubmitRequest**</span></span>
    
- <span data-ttu-id="e2073-327">**Set-servercomponentstate**</span><span class="sxs-lookup"><span data-stu-id="e2073-327">**Get-ServerComponentState**</span></span>
    
- <span data-ttu-id="e2073-328">**Set-servercomponentstate**</span><span class="sxs-lookup"><span data-stu-id="e2073-328">**Set-ServerComponentState**</span></span>
    
- <span data-ttu-id="e2073-329">**Get-serverhealth**</span><span class="sxs-lookup"><span data-stu-id="e2073-329">**Get-ServerHealth**</span></span>
    
- <span data-ttu-id="e2073-330">**ServerMonitor**</span><span class="sxs-lookup"><span data-stu-id="e2073-330">**Set-ServerMonitor**</span></span>
    
- <span data-ttu-id="e2073-331">**外接 Get-servermonitoringoverride**</span><span class="sxs-lookup"><span data-stu-id="e2073-331">**Add-ServerMonitoringOverride**</span></span>
    
- <span data-ttu-id="e2073-332">**Get-servermonitoringoverride**</span><span class="sxs-lookup"><span data-stu-id="e2073-332">**Get-ServerMonitoringOverride**</span></span>
    
- <span data-ttu-id="e2073-333">**SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-333">**Get-SiteMailbox**</span></span>
    
- <span data-ttu-id="e2073-334">**新 SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-334">**New-SiteMailbox**</span></span>
    
- <span data-ttu-id="e2073-335">**SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-335">**Set-SiteMailbox**</span></span>
    
- <span data-ttu-id="e2073-336">**Test-SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-336">**Test-SiteMailbox**</span></span>
    
- <span data-ttu-id="e2073-337">**更新-SiteMailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-337">**Update-SiteMailbox**</span></span>
    
- <span data-ttu-id="e2073-338">**SiteMailboxDiagnostics**</span><span class="sxs-lookup"><span data-stu-id="e2073-338">**Get-SiteMailboxDiagnostics**</span></span>
    
- <span data-ttu-id="e2073-339">**New-sitemailboxprovisioningpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-339">**Get-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="e2073-340">**新 New-sitemailboxprovisioningpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-340">**New-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="e2073-341">**New-sitemailboxprovisioningpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-341">**Remove-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="e2073-342">**New-sitemailboxprovisioningpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-342">**Set-SiteMailboxProvisioningPolicy**</span></span>
    
- <span data-ttu-id="e2073-343">**Undo-SoftDeletedMailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-343">**Undo-SoftDeletedMailbox**</span></span>
    
- <span data-ttu-id="e2073-344">**Get-stalemailboxdetailreport**</span><span class="sxs-lookup"><span data-stu-id="e2073-344">**Get-StaleMailboxDetailReport**</span></span>
    
- <span data-ttu-id="e2073-345">**Get-stalemailboxreport**</span><span class="sxs-lookup"><span data-stu-id="e2073-345">**Get-StaleMailboxReport**</span></span>
    
- <span data-ttu-id="e2073-346">**更新-Update-storemailboxstate**</span><span class="sxs-lookup"><span data-stu-id="e2073-346">**Update-StoreMailboxState**</span></span>
    
- <span data-ttu-id="e2073-347">**新 SyncMailPublicFolder**</span><span class="sxs-lookup"><span data-stu-id="e2073-347">**New-SyncMailPublicFolder**</span></span>
    
- <span data-ttu-id="e2073-348">**Set-transportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-348">**Get-TransportService**</span></span>
    
- <span data-ttu-id="e2073-349">**Set-transportservice**</span><span class="sxs-lookup"><span data-stu-id="e2073-349">**Set-TransportService**</span></span>
    
- <span data-ttu-id="e2073-350">**Disable-Enable-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="e2073-350">**Disable-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="e2073-351">**Enable-Enable-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="e2073-351">**Enable-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="e2073-352">**Enable-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="e2073-352">**Get-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="e2073-353">**新 Enable-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="e2073-353">**New-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="e2073-354">**Enable-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="e2073-354">**Remove-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="e2073-355">**Enable-umcallansweringrule**</span><span class="sxs-lookup"><span data-stu-id="e2073-355">**Set-UMCallAnsweringRule**</span></span>
    
- <span data-ttu-id="e2073-356">**Set-umcallroutersettings**</span><span class="sxs-lookup"><span data-stu-id="e2073-356">**Get-UMCallRouterSettings**</span></span>
    
- <span data-ttu-id="e2073-357">**Set-umcallroutersettings**</span><span class="sxs-lookup"><span data-stu-id="e2073-357">**Set-UMCallRouterSettings**</span></span>
    
- <span data-ttu-id="e2073-358">**Disable-UMService**</span><span class="sxs-lookup"><span data-stu-id="e2073-358">**Disable-UMService**</span></span>
    
- <span data-ttu-id="e2073-359">**Enable-UMService**</span><span class="sxs-lookup"><span data-stu-id="e2073-359">**Enable-UMService**</span></span>
    
- <span data-ttu-id="e2073-360">**Get-UMService**</span><span class="sxs-lookup"><span data-stu-id="e2073-360">**Get-UMService**</span></span>
    
- <span data-ttu-id="e2073-361">**Set-UMService**</span><span class="sxs-lookup"><span data-stu-id="e2073-361">**Set-UMService**</span></span>
    
- <span data-ttu-id="e2073-362">**Set-userphoto**</span><span class="sxs-lookup"><span data-stu-id="e2073-362">**Get-UserPhoto**</span></span>
    
- <span data-ttu-id="e2073-363">**Set-userphoto**</span><span class="sxs-lookup"><span data-stu-id="e2073-363">**Remove-UserPhoto**</span></span>
    
- <span data-ttu-id="e2073-364">**Set-userphoto**</span><span class="sxs-lookup"><span data-stu-id="e2073-364">**Set-UserPhoto**</span></span>
    
- <span data-ttu-id="e2073-365">**WorkloadManagementPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-365">**Get-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="e2073-366">**新 WorkloadManagementPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-366">**New-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="e2073-367">**WorkloadManagementPolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-367">**Remove-WorkloadManagementPolicy**</span></span>
    
- <span data-ttu-id="e2073-368">**Get-workloadpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-368">**Get-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="e2073-369">**新 Get-workloadpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-369">**New-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="e2073-370">**Get-workloadpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-370">**Remove-WorkloadPolicy**</span></span>
    
- <span data-ttu-id="e2073-371">**Get-workloadpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-371">**Set-WorkloadPolicy**</span></span>
    
### <a name="modified-cmdlets"></a><span data-ttu-id="e2073-372">修改的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-372">Modified cmdlets</span></span>
<span data-ttu-id="e2073-373"><a name="bk_update"> </a></span><span class="sxs-lookup"><span data-stu-id="e2073-373"><a name="bk_update"> </a></span></span>

<span data-ttu-id="e2073-374">以下 cmdlet 的输入或输出类型在 Exchange 2013 中进行了修改：</span><span class="sxs-lookup"><span data-stu-id="e2073-374">The input or output types for following cmdlets were modified in Exchange 2013:</span></span>
  
- <span data-ttu-id="e2073-375">**Clear-Clear-activesyncdevice**</span><span class="sxs-lookup"><span data-stu-id="e2073-375">**Clear-ActiveSyncDevice**</span></span>
    
- <span data-ttu-id="e2073-376">**Clear-activesyncdevice**</span><span class="sxs-lookup"><span data-stu-id="e2073-376">**Remove-ActiveSyncDevice**</span></span>
    
- <span data-ttu-id="e2073-377">**New-activesyncmailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-377">**Get-ActiveSyncMailboxPolicy**</span></span>
    
- <span data-ttu-id="e2073-378">**新 New-activesyncmailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-378">**New-ActiveSyncMailboxPolicy**</span></span>
    
- <span data-ttu-id="e2073-379">**新 Set-activesyncvirtualdirectory**</span><span class="sxs-lookup"><span data-stu-id="e2073-379">**New-ActiveSyncVirtualDirectory**</span></span>
    
- <span data-ttu-id="e2073-380">**新 New-autodiscovervirtualdirectory**</span><span class="sxs-lookup"><span data-stu-id="e2073-380">**New-AutodiscoverVirtualDirectory**</span></span>
    
- <span data-ttu-id="e2073-381">**Get-availabilityconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-381">**Set-AvailabilityConfig**</span></span>
    
- <span data-ttu-id="e2073-382">**Enable-Get-exchangecertificate**</span><span class="sxs-lookup"><span data-stu-id="e2073-382">**Enable-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="e2073-383">**Export-Get-exchangecertificate**</span><span class="sxs-lookup"><span data-stu-id="e2073-383">**Export-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="e2073-384">**Import-Get-exchangecertificate**</span><span class="sxs-lookup"><span data-stu-id="e2073-384">**Import-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="e2073-385">**Get-exchangecertificate**</span><span class="sxs-lookup"><span data-stu-id="e2073-385">**Remove-ExchangeCertificate**</span></span>
    
- <span data-ttu-id="e2073-386">**Get-failedcontentindexdocuments**</span><span class="sxs-lookup"><span data-stu-id="e2073-386">**Get-FailedContentIndexDocuments**</span></span>
    
- <span data-ttu-id="e2073-387">**Get-federationinformation**</span><span class="sxs-lookup"><span data-stu-id="e2073-387">**Get-FederationInformation**</span></span>
    
- <span data-ttu-id="e2073-388">**新 HybridConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e2073-388">**New-HybridConfiguration**</span></span>
    
- <span data-ttu-id="e2073-389">**HybridConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e2073-389">**Set-HybridConfiguration**</span></span>
    
- <span data-ttu-id="e2073-390">**New-Mailbox**</span><span class="sxs-lookup"><span data-stu-id="e2073-390">**New-Mailbox**</span></span>
    
- <span data-ttu-id="e2073-391">**Resume-Update-mailboxdatabasecopy**</span><span class="sxs-lookup"><span data-stu-id="e2073-391">**Resume-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="e2073-392">**Update-mailboxdatabasecopy**</span><span class="sxs-lookup"><span data-stu-id="e2073-392">**Set-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="e2073-393">**挂起-Update-mailboxdatabasecopy**</span><span class="sxs-lookup"><span data-stu-id="e2073-393">**Suspend-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="e2073-394">**Update-MailboxDatabaseCopy**</span><span class="sxs-lookup"><span data-stu-id="e2073-394">**Update-MailboxDatabaseCopy**</span></span>
    
- <span data-ttu-id="e2073-395">**New-mailboxexportrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-395">**Get-MailboxExportRequest**</span></span>
    
- <span data-ttu-id="e2073-396">**New-mailboxexportrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-396">**Set-MailboxExportRequest**</span></span>
    
- <span data-ttu-id="e2073-397">**外接 Add-mailboxfolderpermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-397">**Add-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="e2073-398">**Add-mailboxfolderpermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-398">**Remove-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="e2073-399">**Add-mailboxfolderpermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-399">**Set-MailboxFolderPermission**</span></span>
    
- <span data-ttu-id="e2073-400">**New-mailboximportrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-400">**Get-MailboxImportRequest**</span></span>
    
- <span data-ttu-id="e2073-401">**New-mailboximportrequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-401">**Set-MailboxImportRequest**</span></span>
    
- <span data-ttu-id="e2073-402">**New-mailboxrestorerequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-402">**Get-MailboxRestoreRequest**</span></span>
    
- <span data-ttu-id="e2073-403">**New-mailboxrestorerequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-403">**Set-MailboxRestoreRequest**</span></span>
    
- <span data-ttu-id="e2073-404">**New-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-404">**Get-MailboxSearch**</span></span>
    
- <span data-ttu-id="e2073-405">**New-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-405">**Remove-MailboxSearch**</span></span>
    
- <span data-ttu-id="e2073-406">**New-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-406">**Set-MailboxSearch**</span></span>
    
- <span data-ttu-id="e2073-407">**启动-New-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-407">**Start-MailboxSearch**</span></span>
    
- <span data-ttu-id="e2073-408">**New-mailboxsearch**</span><span class="sxs-lookup"><span data-stu-id="e2073-408">**Stop-MailboxSearch**</span></span>
    
- <span data-ttu-id="e2073-409">**Disable-Enable-mailpublicfolder**</span><span class="sxs-lookup"><span data-stu-id="e2073-409">**Disable-MailPublicFolder**</span></span>
    
- <span data-ttu-id="e2073-410">**Enable-mailpublicfolder**</span><span class="sxs-lookup"><span data-stu-id="e2073-410">**Get-MailPublicFolder**</span></span>
    
- <span data-ttu-id="e2073-411">**Enable-mailpublicfolder**</span><span class="sxs-lookup"><span data-stu-id="e2073-411">**Set-MailPublicFolder**</span></span>
    
- <span data-ttu-id="e2073-412">**New-migrationbatch**</span><span class="sxs-lookup"><span data-stu-id="e2073-412">**Get-MigrationBatch**</span></span>
    
- <span data-ttu-id="e2073-413">**新 New-migrationbatch**</span><span class="sxs-lookup"><span data-stu-id="e2073-413">**New-MigrationBatch**</span></span>
    
- <span data-ttu-id="e2073-414">**New-migrationbatch**</span><span class="sxs-lookup"><span data-stu-id="e2073-414">**Set-MigrationBatch**</span></span>
    
- <span data-ttu-id="e2073-415">**Test-Test-migrationserveravailability**</span><span class="sxs-lookup"><span data-stu-id="e2073-415">**Test-MigrationServerAvailability**</span></span>
    
- <span data-ttu-id="e2073-416">**New-moverequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-416">**Get-MoveRequest**</span></span>
    
- <span data-ttu-id="e2073-417">**新 Move-offlineaddressbook**</span><span class="sxs-lookup"><span data-stu-id="e2073-417">**New-OfflineAddressBook**</span></span>
    
- <span data-ttu-id="e2073-418">**Set-organizationconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-418">**Get-OrganizationConfig**</span></span>
    
- <span data-ttu-id="e2073-419">**Set-organizationconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-419">**Set-OrganizationConfig**</span></span>
    
- <span data-ttu-id="e2073-420">**Test-Test-outlookconnectivity**</span><span class="sxs-lookup"><span data-stu-id="e2073-420">**Test-OutlookConnectivity**</span></span>
    
- <span data-ttu-id="e2073-421">**Test-Test-outlookwebservices**</span><span class="sxs-lookup"><span data-stu-id="e2073-421">**Test-OutlookWebServices**</span></span>
    
- <span data-ttu-id="e2073-422">**Set-owamailboxpolicy**</span><span class="sxs-lookup"><span data-stu-id="e2073-422">**Get-OwaMailboxPolicy**</span></span>
    
- <span data-ttu-id="e2073-423">**新 Set-owavirtualdirectory**</span><span class="sxs-lookup"><span data-stu-id="e2073-423">**New-OwaVirtualDirectory**</span></span>
    
- <span data-ttu-id="e2073-424">**新 Get-powershellvirtualdirectory**</span><span class="sxs-lookup"><span data-stu-id="e2073-424">**New-PowerShellVirtualDirectory**</span></span>
    
- <span data-ttu-id="e2073-425">**Set-publicfolder**</span><span class="sxs-lookup"><span data-stu-id="e2073-425">**Get-PublicFolder**</span></span>
    
- <span data-ttu-id="e2073-426">**新 Set-publicfolder**</span><span class="sxs-lookup"><span data-stu-id="e2073-426">**New-PublicFolder**</span></span>
    
- <span data-ttu-id="e2073-427">**Set-publicfolder**</span><span class="sxs-lookup"><span data-stu-id="e2073-427">**Set-PublicFolder**</span></span>
    
- <span data-ttu-id="e2073-428">**外接 Add-publicfolderclientpermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-428">**Add-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="e2073-429">**Add-publicfolderclientpermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-429">**Get-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="e2073-430">**Add-publicfolderclientpermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-430">**Remove-PublicFolderClientPermission**</span></span>
    
- <span data-ttu-id="e2073-431">**Get-publicfolderitemstatistics**</span><span class="sxs-lookup"><span data-stu-id="e2073-431">**Get-PublicFolderItemStatistics**</span></span>
    
- <span data-ttu-id="e2073-432">**Get-publicfolderstatistics**</span><span class="sxs-lookup"><span data-stu-id="e2073-432">**Get-PublicFolderStatistics**</span></span>
    
- <span data-ttu-id="e2073-433">**Get-Recipient**</span><span class="sxs-lookup"><span data-stu-id="e2073-433">**Get-Recipient**</span></span>
    
- <span data-ttu-id="e2073-434">**Set-resourceconfig**</span><span class="sxs-lookup"><span data-stu-id="e2073-434">**Set-ResourceConfig**</span></span>
    
- <span data-ttu-id="e2073-435">**Test-Test-webservicesconnectivity**</span><span class="sxs-lookup"><span data-stu-id="e2073-435">**Test-WebServicesConnectivity**</span></span>
    
- <span data-ttu-id="e2073-436">**新 Set-webservicesvirtualdirectory**</span><span class="sxs-lookup"><span data-stu-id="e2073-436">**New-WebServicesVirtualDirectory**</span></span>
    
### <a name="removed-cmdlets"></a><span data-ttu-id="e2073-437">删除的 cmdlet</span><span class="sxs-lookup"><span data-stu-id="e2073-437">Removed cmdlets</span></span>
<span data-ttu-id="e2073-438"><a name="bk_removed"> </a></span><span class="sxs-lookup"><span data-stu-id="e2073-438"><a name="bk_removed"> </a></span></span>

<span data-ttu-id="e2073-439">从 Exchange 2013 中删除了以下 cmdlet：</span><span class="sxs-lookup"><span data-stu-id="e2073-439">The following cmdlets were removed from Exchange 2013:</span></span>
  
- <span data-ttu-id="e2073-440">**更新-FileDistributionService**</span><span class="sxs-lookup"><span data-stu-id="e2073-440">**Update-FileDistributionService**</span></span>
    
- <span data-ttu-id="e2073-441">**还原-邮箱**</span><span class="sxs-lookup"><span data-stu-id="e2073-441">**Restore-Mailbox**</span></span>
    
- <span data-ttu-id="e2073-442">**Clean-Set-mailboxdatabase**</span><span class="sxs-lookup"><span data-stu-id="e2073-442">**Clean-MailboxDatabase**</span></span>
    
- <span data-ttu-id="e2073-443">**完整迁移**</span><span class="sxs-lookup"><span data-stu-id="e2073-443">**Complete-Migration**</span></span>
    
- <span data-ttu-id="e2073-444">**MigrationStatus**</span><span class="sxs-lookup"><span data-stu-id="e2073-444">**Get-MigrationStatus**</span></span>
    
- <span data-ttu-id="e2073-445">**更新-Set-publicfolder**</span><span class="sxs-lookup"><span data-stu-id="e2073-445">**Update-PublicFolder**</span></span>
    
- <span data-ttu-id="e2073-446">**外接 Remove-publicfolderadministrativepermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-446">**Add-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="e2073-447">**Remove-publicfolderadministrativepermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-447">**Get-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="e2073-448">**Remove-publicfolderadministrativepermission**</span><span class="sxs-lookup"><span data-stu-id="e2073-448">**Remove-PublicFolderAdministrativePermission**</span></span>
    
- <span data-ttu-id="e2073-449">**新 Get-publicfolderdatabase**</span><span class="sxs-lookup"><span data-stu-id="e2073-449">**New-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="e2073-450">**Get-publicfolderdatabase**</span><span class="sxs-lookup"><span data-stu-id="e2073-450">**Remove-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="e2073-451">**Get-publicfolderdatabase**</span><span class="sxs-lookup"><span data-stu-id="e2073-451">**Set-PublicFolderDatabase**</span></span>
    
- <span data-ttu-id="e2073-452">**新 PublicFolderDatabaseRepairRequest**</span><span class="sxs-lookup"><span data-stu-id="e2073-452">**New-PublicFolderDatabaseRepairRequest**</span></span>
    
- <span data-ttu-id="e2073-453">**更新-PublicFolderHierarchy**</span><span class="sxs-lookup"><span data-stu-id="e2073-453">**Update-PublicFolderHierarchy**</span></span>
    
- <span data-ttu-id="e2073-454">**Resume-PublicFolderReplication**</span><span class="sxs-lookup"><span data-stu-id="e2073-454">**Resume-PublicFolderReplication**</span></span>
    
- <span data-ttu-id="e2073-455">**挂起-PublicFolderReplication**</span><span class="sxs-lookup"><span data-stu-id="e2073-455">**Suspend-PublicFolderReplication**</span></span>
    
- <span data-ttu-id="e2073-456">**启动-RetentionAutoTagLearning**</span><span class="sxs-lookup"><span data-stu-id="e2073-456">**Start-RetentionAutoTagLearning**</span></span>
    
- <span data-ttu-id="e2073-457">**Test-Test-systemhealth**</span><span class="sxs-lookup"><span data-stu-id="e2073-457">**Test-SystemHealth**</span></span>
    
- <span data-ttu-id="e2073-458">**Disable-Disable-umserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-458">**Disable-UMServer**</span></span>
    
- <span data-ttu-id="e2073-459">**Enable-Disable-umserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-459">**Enable-UMServer**</span></span>
    
- <span data-ttu-id="e2073-460">**Disable-umserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-460">**Get-UMServer**</span></span>
    
- <span data-ttu-id="e2073-461">**Disable-umserver**</span><span class="sxs-lookup"><span data-stu-id="e2073-461">**Set-UMServer**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2073-462">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e2073-462">See also</span></span>

- [<span data-ttu-id="e2073-463">Exchange 命令行管理程序 cmdlet 的输入和输出类型</span><span class="sxs-lookup"><span data-stu-id="e2073-463">Exchange Management Shell cmdlet input and output types</span></span>](exchange-management-shell-cmdlet-input-and-output-types.md)    
- [<span data-ttu-id="e2073-464">使用 Exchange 命令行管理程序获取邮件用户列表</span><span class="sxs-lookup"><span data-stu-id="e2073-464">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)    
- [<span data-ttu-id="e2073-465">Exchange 2013 cmdlets</span><span class="sxs-lookup"><span data-stu-id="e2073-465">Exchange 2013 cmdlets</span></span>](https://technet.microsoft.com/library/bb124413%28v=exchg.150%29.aspx)
    

