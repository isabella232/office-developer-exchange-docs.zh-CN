---
title: 在 Exchange 控制对 EWS 的访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 61e29e54-e3e5-404a-84c0-93b61a25ca58
description: 找出如何控制对 EWS 的用户、 应用程序或整个组织的访问。
ms.openlocfilehash: 956c28faba105ecf2a6b1452abe629ea2fc930e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752754"
---
# <a name="control-access-to-ews-in-exchange"></a><span data-ttu-id="dda87-103">在 Exchange 控制对 EWS 的访问</span><span class="sxs-lookup"><span data-stu-id="dda87-103">Control access to EWS in Exchange</span></span>

<span data-ttu-id="dda87-104">找出如何控制对 EWS 的用户、 应用程序或整个组织的访问。</span><span class="sxs-lookup"><span data-stu-id="dda87-104">Find out how to control access to EWS for users, applications, or the entire organization.</span></span>
  
<span data-ttu-id="dda87-105">无论您使用 EWS 托管 API 或 EWS 直接在您的应用程序，您可以控制访问到 Exchange Web Services (EWS)。</span><span class="sxs-lookup"><span data-stu-id="dda87-105">Whether you are using the EWS Managed API, or EWS directly, in your application, you can control access to Exchange Web Services (EWS).</span></span> <span data-ttu-id="dda87-106">如果您有到 Exchange 服务器的管理员访问权限，您可以使用 Exchange 命令行管理程序来控制访问全局，每个用户，以及每个应用程序管理对 EWS 访问。</span><span class="sxs-lookup"><span data-stu-id="dda87-106">If you have administrator access to your Exchange server, you can manage access to EWS by using the Exchange Management Shell to control access globally, for each user, and for each application.</span></span>
  
## <a name="exchange-management-shell-cmdlets-for-configuring-access-control"></a><span data-ttu-id="dda87-107">Exchange 命令行管理程序 cmdlet 配置的访问控制</span><span class="sxs-lookup"><span data-stu-id="dda87-107">Exchange Management Shell cmdlets for configuring access control</span></span>
<span data-ttu-id="dda87-108"><a name="bk_Cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="dda87-108"></span></span>

<span data-ttu-id="dda87-109">可以使用下面的 Exchange 命令行管理程序 cmdlet 查看当前的访问配置和设置 EWS 访问控制：</span><span class="sxs-lookup"><span data-stu-id="dda87-109">You can use the following Exchange Management Shell cmdlets to view the current access configuration and set EWS access controls:</span></span>
  
- <span data-ttu-id="dda87-110">[Get-casmailbox](http://technet.microsoft.com/zh-cn/library/bb124754.aspx) -显示哪些参数设置为特定邮箱。</span><span class="sxs-lookup"><span data-stu-id="dda87-110">[Get-CASMailbox](http://technet.microsoft.com/zh-cn/library/bb124754.aspx) - Shows you what parameters are set for a particular mailbox.</span></span>   
- <span data-ttu-id="dda87-111">[设置 CASMailbox](http://technet.microsoft.com/zh-cn/library/bb125264.aspx) -特定邮箱的设置参数。</span><span class="sxs-lookup"><span data-stu-id="dda87-111">[Set-CASMailbox](http://technet.microsoft.com/zh-cn/library/bb125264.aspx) - Sets parameters for a particular mailbox.</span></span>    
- <span data-ttu-id="dda87-112">[Get-organizationconfig](http://technet.microsoft.com/zh-cn/library/aa997571.aspx) -显示整个组织的参数。</span><span class="sxs-lookup"><span data-stu-id="dda87-112">[Get-OrganizationConfig](http://technet.microsoft.com/zh-cn/library/aa997571.aspx) - Shows you the parameters for the entire organization.</span></span>    
- <span data-ttu-id="dda87-113">[Set-organizationconfig](http://technet.microsoft.com/zh-cn/library/aa997443.aspx) -设置为整个组织的参数。</span><span class="sxs-lookup"><span data-stu-id="dda87-113">[Set-OrganizationConfig](http://technet.microsoft.com/zh-cn/library/aa997443.aspx) - Sets the parameters for the entire organization.</span></span> 

<span data-ttu-id="dda87-114"><a name="bk_Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="dda87-114"></span></span>

## <a name="examples-controlling-access-to-ews"></a><span data-ttu-id="dda87-115">示例： 控制对 EWS 的访问</span><span class="sxs-lookup"><span data-stu-id="dda87-115">Examples: Controlling access to EWS</span></span>

<span data-ttu-id="dda87-116">让我们看看几个方案演示如何可以控制对您的应用程序的访问。</span><span class="sxs-lookup"><span data-stu-id="dda87-116">Let's take a look at a few scenarios that show you how you can control access to your application.</span></span>
  
<span data-ttu-id="dda87-117">**表 1。用于控制访问 EWS 的命令**</span><span class="sxs-lookup"><span data-stu-id="dda87-117">**Table 1. Commands for controlling access to EWS**</span></span>

|<span data-ttu-id="dda87-118">如果您要</span><span class="sxs-lookup"><span data-stu-id="dda87-118">If you want to</span></span> |<span data-ttu-id="dda87-119">使用此命令</span><span class="sxs-lookup"><span data-stu-id="dda87-119">Use this command</span></span>|
|:-----|:-----|
|<span data-ttu-id="dda87-120">阻止通过 EWS 中的所有客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="dda87-120">Block all client applications from using EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList`<br/><br/><span data-ttu-id="dda87-121">这样 AllowList 中列出的应用程序连接。</span><span class="sxs-lookup"><span data-stu-id="dda87-121">This allows applications listed in the AllowList to connect.</span></span> <span data-ttu-id="dda87-122">本示例中，没有应用程序中都包含 AllowList，因此没有应用程序可以使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="dda87-122">In this example, no applications are included in the AllowList, so no applications can use EWS.</span></span> |
|<span data-ttu-id="dda87-123">允许列表的客户端应用程序使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="dda87-123">Allow a list of client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceAllowList -EwsAllowList:"OWA/*"`<br/><br/><span data-ttu-id="dda87-124">这允许使用 EWS 特定应用程序。</span><span class="sxs-lookup"><span data-stu-id="dda87-124">This allows specific applications to use EWS.</span></span> <span data-ttu-id="dda87-125">本示例中，任何应用程序具有用户代理字符串的开头"OWA /"允许访问。</span><span class="sxs-lookup"><span data-stu-id="dda87-125">In this example, any application that has a user agent string that starts with "OWA/" is allowed access.</span></span> |
|<span data-ttu-id="dda87-126">允许所有客户端应用程序使用 EWS 除外明确阻止。</span><span class="sxs-lookup"><span data-stu-id="dda87-126">Allow all client applications to use EWS except those that are specifically blocked.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList -EwsBlockList:"OWA/*"`<br/> <br/><span data-ttu-id="dda87-127">本示例仅阻止使用具有开头的用户代理字符串的 EWS 的应用程序"OWA /"。</span><span class="sxs-lookup"><span data-stu-id="dda87-127">This example only blocks applications from using EWS that have a user agent string that starts with "OWA/".</span></span> |
|<span data-ttu-id="dda87-128">允许所有客户端应用程序使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="dda87-128">Allow all client applications to use EWS.</span></span> | `Set-OrganizationConfig -EwsApplicationAccessPolicy:EnforceBlockList` <br/><br/> <span data-ttu-id="dda87-129">由于指定没有 BlockList，则所有应用程序可以使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="dda87-129">Because no BlockList is specified, all applications can use EWS.</span></span> |
|<span data-ttu-id="dda87-130">阻止整个组织使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="dda87-130">Block the entire organization from using EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$false` |
|<span data-ttu-id="dda87-131">使整个组织使用 EWS。</span><span class="sxs-lookup"><span data-stu-id="dda87-131">Allow the entire organization to use EWS.</span></span> | `Set-OrganizationConfig -EwsEnabled:$true`|
|<span data-ttu-id="dda87-132">阻止使用 EWS 单个邮箱。</span><span class="sxs-lookup"><span data-stu-id="dda87-132">Block an individual mailbox from using EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$false`|
|<span data-ttu-id="dda87-133">允许使用 EWS 单个邮箱。</span><span class="sxs-lookup"><span data-stu-id="dda87-133">Allow an individual mailbox to use EWS.</span></span> | `Set-CASMailbox -Identity adam@contoso.com -EwsEnabled:$true`|
   
## <a name="see-also"></a><span data-ttu-id="dda87-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dda87-134">See also</span></span>

- [<span data-ttu-id="dda87-135">EWS 应用程序设置</span><span class="sxs-lookup"><span data-stu-id="dda87-135">Setting up your EWS application</span></span>](setting-up-your-ews-application.md)    
- [<span data-ttu-id="dda87-136">在 Exchange 控制客户端应用程序访问 EWS</span><span class="sxs-lookup"><span data-stu-id="dda87-136">Controlling client application access to EWS in Exchange</span></span>](controlling-client-application-access-to-ews-in-exchange.md)   
- [<span data-ttu-id="dda87-137">Exchange Server PowerShell （Exchange 命令行管理程序）</span><span class="sxs-lookup"><span data-stu-id="dda87-137">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/zh-cn/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps) 
- [<span data-ttu-id="dda87-138">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="dda87-138">Windows PowerShell</span></span>](http://msdn.microsoft.com/zh-cn/library/dd835506%28v=vs.85%29.aspx)
    

