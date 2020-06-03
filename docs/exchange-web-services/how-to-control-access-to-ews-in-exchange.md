---
title: 在 Exchange 中控制对 EWS 的访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: 了解如何控制用户、应用程序或整个组织对 EWS 的访问。
localization_priority: Priority
ms.openlocfilehash: bd65b099ab15c1514945d8a1cfa4e9b1428a4755
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456876"
---
# <a name="control-access-to-ews-in-exchange"></a><span data-ttu-id="407fe-103">在 Exchange 中控制对 EWS 的访问</span><span class="sxs-lookup"><span data-stu-id="407fe-103">Control access to EWS in Exchange</span></span>

<span data-ttu-id="407fe-104">了解如何控制用户、应用程序或整个组织对 EWS 的访问。</span><span class="sxs-lookup"><span data-stu-id="407fe-104">Find out how to control access to EWS for users, applications, or the entire organization.</span></span>
  
<span data-ttu-id="407fe-105">无论您是在应用程序中直接使用 EWS 托管 API （或 EWS），您都可以控制对 Exchange Web 服务（EWS）的访问。</span><span class="sxs-lookup"><span data-stu-id="407fe-105">Whether you are using the EWS Managed API, or EWS directly, in your application, you can control access to Exchange Web Services (EWS).</span></span> <span data-ttu-id="407fe-106">如果您具有对 Exchange 服务器的管理员访问权限，则可以通过使用 Exchange 命令行管理程序来控制对 EWS 的访问权限，对每个用户和每个应用程序进行全局访问。</span><span class="sxs-lookup"><span data-stu-id="407fe-106">If you have administrator access to your Exchange server, you can manage access to EWS by using the Exchange Management Shell to control access globally, for each user, and for each application.</span></span>
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a><span data-ttu-id="407fe-107">用于配置访问控制的 Exchange 命令行管理程序 cmdlet</span><span class="sxs-lookup"><span data-stu-id="407fe-107">Exchange Management Shell cmdlets for configuring access control</span></span>
<span data-ttu-id="407fe-108"><a name="bk_Cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="407fe-108"><a name="bk_Cmdlets"> </a></span></span>

<span data-ttu-id="407fe-109">您可以使用以下 Exchange 命令行管理程序 cmdlet 查看当前的访问配置和设置 EWS 访问控制：</span><span class="sxs-lookup"><span data-stu-id="407fe-109">You can use the following Exchange Management Shell cmdlets to view the current access configuration and set EWS access controls:</span></span>
  
- <span data-ttu-id="407fe-110">[Set-casmailbox](https://technet.microsoft.com/library/bb124754.aspx) -显示为特定邮箱设置的参数。</span><span class="sxs-lookup"><span data-stu-id="407fe-110">[Get-CASMailbox](https://technet.microsoft.com/library/bb124754.aspx) - Shows you what parameters are set for a particular mailbox.</span></span>   
- <span data-ttu-id="407fe-111">[Set-set-casmailbox](https://technet.microsoft.com/library/bb125264.aspx) -设置特定邮箱的参数。</span><span class="sxs-lookup"><span data-stu-id="407fe-111">[Set-CASMailbox](https://technet.microsoft.com/library/bb125264.aspx) - Sets parameters for a particular mailbox.</span></span>    
- <span data-ttu-id="407fe-112">[Set-organizationconfig](https://technet.microsoft.com/library/aa997571.aspx) -显示整个组织的参数。</span><span class="sxs-lookup"><span data-stu-id="407fe-112">[Get-OrganizationConfig](https://technet.microsoft.com/library/aa997571.aspx) - Shows you the parameters for the entire organization.</span></span>    
- <span data-ttu-id="407fe-113">[Set-set-organizationconfig](https://technet.microsoft.com/library/aa997443.aspx) -设置整个组织的参数。</span><span class="sxs-lookup"><span data-stu-id="407fe-113">[Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443.aspx) - Sets the parameters for the entire organization.</span></span> 

<span data-ttu-id="407fe-114"><a name="bk_Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="407fe-114"><a name="bk_Examples"> </a></span></span>

## <a name="examples-controlling-access-to-ews"></a><span data-ttu-id="407fe-115">示例：控制对 EWS 的访问</span><span class="sxs-lookup"><span data-stu-id="407fe-115">Examples: Controlling access to EWS</span></span>

<span data-ttu-id="407fe-116">我们来看看几个方案，向您介绍如何控制对应用程序的访问。</span><span class="sxs-lookup"><span data-stu-id="407fe-116">Let's take a look at a few scenarios that show you how you can control access to your application.</span></span>
  
<span data-ttu-id="407fe-117">**表1。用于控制对 EWS 的访问的命令**</span><span class="sxs-lookup"><span data-stu-id="407fe-117">**Table 1. Commands for controlling access to EWS**</span></span>

|<span data-ttu-id="407fe-118">如果您想要</span><span class="sxs-lookup"><span data-stu-id="407fe-118">If you want to</span></span> |<span data-ttu-id="407fe-119">使用此命令</span><span class="sxs-lookup"><span data-stu-id="407fe-119">Use this command</span></span>|
|:-----|:-----|
|<span data-ttu-id="407fe-120">阻止所有客户端应用程序使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-120">Block all client applications from using EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/><span data-ttu-id="407fe-121">这将允许 AllowList 中列出的应用程序进行连接。</span><span class="sxs-lookup"><span data-stu-id="407fe-121">This allows applications listed in the AllowList to connect.</span></span> <span data-ttu-id="407fe-122">在此示例中，AllowList 中不包含任何应用程序，因此任何应用程序都不能使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-122">In this example, no applications are included in the AllowList, so no applications can use EWS.</span></span> |
|<span data-ttu-id="407fe-123">允许客户端应用程序列表使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-123">Allow a list of client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/><span data-ttu-id="407fe-124">这将允许特定应用程序使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-124">This allows specific applications to use EWS.</span></span> <span data-ttu-id="407fe-125">在此示例中，允许具有以 "OWA/" 开头的用户代理字符串的任何应用程序访问权限。</span><span class="sxs-lookup"><span data-stu-id="407fe-125">In this example, any application that has a user agent string that starts with "OWA/" is allowed access.</span></span> |
|<span data-ttu-id="407fe-126">允许所有客户端应用程序使用 EWS，但特别被阻止的应用程序除外。</span><span class="sxs-lookup"><span data-stu-id="407fe-126">Allow all client applications to use EWS except those that are specifically blocked.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/><span data-ttu-id="407fe-127">本示例仅阻止应用程序使用具有以 "OWA/" 开头的用户代理字符串的 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-127">This example only blocks applications from using EWS that have a user agent string that starts with "OWA/".</span></span> |
|<span data-ttu-id="407fe-128">允许所有客户端应用程序使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-128">Allow all client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> <span data-ttu-id="407fe-129">由于未指定阻止列表，所有应用程序都可以使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-129">Because no BlockList is specified, all applications can use EWS.</span></span> |
|<span data-ttu-id="407fe-130">阻止整个组织使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-130">Block the entire organization from using EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$false` |
|<span data-ttu-id="407fe-131">允许整个组织使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-131">Allow the entire organization to use EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$true`|
|<span data-ttu-id="407fe-132">阻止单个邮箱使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-132">Block an individual mailbox from using EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|<span data-ttu-id="407fe-133">允许单个邮箱使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="407fe-133">Allow an individual mailbox to use EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a><span data-ttu-id="407fe-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="407fe-134">See also</span></span>

- [<span data-ttu-id="407fe-135">设置 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="407fe-135">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="407fe-136">控制对 Exchange 中的 EWS 的客户端应用程序访问</span><span class="sxs-lookup"><span data-stu-id="407fe-136">Controlling client application access to EWS in Exchange</span></span>](controlling-client-application-access-to-ews-in-exchange.md)   
- [<span data-ttu-id="407fe-137">Exchange Server PowerShell （Exchange 命令行管理程序）</span><span class="sxs-lookup"><span data-stu-id="407fe-137">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [<span data-ttu-id="407fe-138">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="407fe-138">Windows PowerShell</span></span>](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

