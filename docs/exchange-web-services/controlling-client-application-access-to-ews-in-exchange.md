---
title: 控制对 Exchange 中的 EWS 的客户端应用程序访问
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: 了解用于管理对 EWS 的客户端应用程序访问的选项。
localization_priority: Priority
ms.openlocfilehash: b887b8167e3d38946b1d6caffe12655ded89569f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528459"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a><span data-ttu-id="45693-103">控制对 Exchange 中的 EWS 的客户端应用程序访问</span><span class="sxs-lookup"><span data-stu-id="45693-103">Controlling client application access to EWS in Exchange</span></span>

<span data-ttu-id="45693-104">了解用于管理对 EWS 的客户端应用程序访问的选项。</span><span class="sxs-lookup"><span data-stu-id="45693-104">Learn about the options for managing client application access to EWS.</span></span>
  
<span data-ttu-id="45693-105">您创建的任何 EWS 客户端应用程序都必须被授予对 Exchange Online、Exchange Online 作为 Office 365 的一部分的访问权限，或从 Exchange 2013 开始的 exchange 版本，然后才能调用 EWS 操作。</span><span class="sxs-lookup"><span data-stu-id="45693-105">Any EWS client application that you create must be granted access to Exchange Online, Exchange Online as part of Office 365, or version of Exchange starting with Exchange 2013 before it can call EWS operations.</span></span> <span data-ttu-id="45693-106">测试或生产服务器管理员可以使用 Exchange 命令行管理程序来限制所有用户和应用程序、单个用户或单个应用程序对 EWS 的访问权限。</span><span class="sxs-lookup"><span data-stu-id="45693-106">Test or production server administrators can use the Exchange Management Shell to limit access to EWS either for all users and applications, for individual users, or for individual applications.</span></span> <span data-ttu-id="45693-107">EWS 的访问控制基于域帐户。</span><span class="sxs-lookup"><span data-stu-id="45693-107">Access control for EWS is based on domain accounts.</span></span> <span data-ttu-id="45693-108">当使用由本地安全机构进行身份验证的凭据建立连接时，服务器将返回一个错误，指示只有域帐户可以连接。</span><span class="sxs-lookup"><span data-stu-id="45693-108">When a connection is made with credentials that are authenticated by the local security authority, the server returns an error that indicates that only domain accounts can connect.</span></span> 
  
## <a name="access-control-for-ews-clients-and-users"></a><span data-ttu-id="45693-109">EWS 客户端和用户的访问控制</span><span class="sxs-lookup"><span data-stu-id="45693-109">Access control for EWS clients and users</span></span>
<span data-ttu-id="45693-110"><a name="bk_configure"> </a></span><span class="sxs-lookup"><span data-stu-id="45693-110"><a name="bk_configure"> </a></span></span>

<span data-ttu-id="45693-111">您的测试或生产服务器管理员可以通过以下方式为连接到 EWS 的客户端配置访问控制：</span><span class="sxs-lookup"><span data-stu-id="45693-111">Your test or production server administrator can configure access control for clients that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="45693-112">通过阻止所有客户端应用程序进行连接。</span><span class="sxs-lookup"><span data-stu-id="45693-112">By blocking all client applications from connecting.</span></span>
    
- <span data-ttu-id="45693-113">通过仅允许特定客户端应用程序进行连接。</span><span class="sxs-lookup"><span data-stu-id="45693-113">By allowing specific client applications only to connect.</span></span>
    
- <span data-ttu-id="45693-114">允许任何客户端应用程序连接，但特别阻止的任何客户端应用程序除外。</span><span class="sxs-lookup"><span data-stu-id="45693-114">By allowing any client application to connect except those that are specifically blocked.</span></span>
    
- <span data-ttu-id="45693-115">允许任何客户端应用程序进行连接。</span><span class="sxs-lookup"><span data-stu-id="45693-115">By allowing any client application to connect.</span></span>
    
<span data-ttu-id="45693-116">应用程序由其在 HTTP web 请求中发送的用户代理字符串进行标识。</span><span class="sxs-lookup"><span data-stu-id="45693-116">Applications are identified by the user agent string that they send in the HTTP web request.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="45693-117">应用程序级别的阻止不是一项安全功能。</span><span class="sxs-lookup"><span data-stu-id="45693-117">Application-level blocking is not a security feature.</span></span> <span data-ttu-id="45693-118">用户代理字符串很容易被欺骗。</span><span class="sxs-lookup"><span data-stu-id="45693-118">The user agent string is easily spoofed.</span></span> <span data-ttu-id="45693-119">如果允许应用程序访问 EWS，则应用程序必须仍然存在服务器在应用程序可以连接到 EWS 之前进行身份验证的凭据。</span><span class="sxs-lookup"><span data-stu-id="45693-119">If an application is allowed access to EWS, the application must still present credentials that the server authenticates before the application can connect to EWS.</span></span> 
  
<span data-ttu-id="45693-120">管理员还可以通过以下方式为连接到 EWS 的邮箱所有者配置访问控制：</span><span class="sxs-lookup"><span data-stu-id="45693-120">Administrators can also configure access control for mailbox owners that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="45693-121">通过阻止或允许整个组织。</span><span class="sxs-lookup"><span data-stu-id="45693-121">By blocking or allowing an entire organization.</span></span>
    
- <span data-ttu-id="45693-122">通过阻止或允许由基于角色的身份验证作用域标识的一组用户，其中包括或排除不具有 EWS 访问权限的邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="45693-122">By blocking or allowing a group of users identified by a role-based authentication scope that includes or excludes mailbox owners that do not have access to EWS.</span></span>
    
- <span data-ttu-id="45693-123">通过阻止或允许单个邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="45693-123">By blocking or allowing an individual mailbox owner.</span></span>
    
<span data-ttu-id="45693-124">特定访问控制设置将覆盖常规访问控制设置。</span><span class="sxs-lookup"><span data-stu-id="45693-124">Specific access control settings override general access control settings.</span></span> <span data-ttu-id="45693-125">例如，如果组织拒绝 EWS 访问，但单个邮箱所有者允许应用程序访问，则允许单个设置 prevails 和访问。</span><span class="sxs-lookup"><span data-stu-id="45693-125">For example, if an organization denies EWS access but an individual mailbox owner is allowed application access, the individual setting prevails and access is allowed.</span></span> 
  
## <a name="delegation-and-ews-access-management"></a><span data-ttu-id="45693-126">委派和 EWS 访问管理</span><span class="sxs-lookup"><span data-stu-id="45693-126">Delegation and EWS access management</span></span>
<span data-ttu-id="45693-127"><a name="bk_delegation"> </a></span><span class="sxs-lookup"><span data-stu-id="45693-127"><a name="bk_delegation"> </a></span></span>

<span data-ttu-id="45693-128">如果委派对 EWS 不具有访问权限的用户使用客户端应用程序，则即使主体用户具有 EWS 访问权限，也无法通过使用 EWS 访问主体用户的邮箱。</span><span class="sxs-lookup"><span data-stu-id="45693-128">When delegate users who do not have access to EWS use your client application, they will not be able to access the principal user's mailbox by using EWS, even if the principal user has EWS access.</span></span> <span data-ttu-id="45693-129">如果代理用户具有 EWS 访问权限，则该代理将能够使用您的 EWS 客户端应用程序访问主体用户的邮箱，即使主体用户不具有 EWS 访问权限也是如此。</span><span class="sxs-lookup"><span data-stu-id="45693-129">If the delegate user has EWS access, the delegate will be able to use your EWS client application to access the principal user's mailbox even if the principal user does not have EWS access.</span></span> 
  
## <a name="impersonation-and-ews-access-management"></a><span data-ttu-id="45693-130">模拟和 EWS 访问管理</span><span class="sxs-lookup"><span data-stu-id="45693-130">Impersonation and EWS access management</span></span>
<span data-ttu-id="45693-131"><a name="bk_impersonation"> </a></span><span class="sxs-lookup"><span data-stu-id="45693-131"><a name="bk_impersonation"> </a></span></span>

<span data-ttu-id="45693-132">代表邮箱所有者连接到 EWS 的客户端应用程序可能无法使用邮箱所有者的 EWS 设置。</span><span class="sxs-lookup"><span data-stu-id="45693-132">Client applications that connect to EWS on behalf of mailbox owners might not be able to use the EWS settings of the mailbox owner.</span></span> <span data-ttu-id="45693-133">例如，对公司的电子邮件进行存档的应用程序必须连接到 EWS，而不考虑邮箱用户的设置。</span><span class="sxs-lookup"><span data-stu-id="45693-133">For example, an application that archives email messages for a company has to connect to EWS regardless of what the mailbox users' settings are.</span></span> <span data-ttu-id="45693-134">其他应用程序（如邮件客户端）必须使用邮箱所有者的 EWS 设置。</span><span class="sxs-lookup"><span data-stu-id="45693-134">Other applications, such as mail clients, do have to use the mailbox owner's EWS settings.</span></span> 
  
<span data-ttu-id="45693-135">管理员应为他们在其服务器上使用的每个应用程序或应用程序类创建一个模拟帐户。</span><span class="sxs-lookup"><span data-stu-id="45693-135">Administrators should create an impersonation account for each application or application class that they use on their server.</span></span> <span data-ttu-id="45693-136">这将使管理员能够为没有 EWS 权限的所有用户配置基于角色的访问控制作用域。</span><span class="sxs-lookup"><span data-stu-id="45693-136">This will enable the administrator to configure the role-based access control scope for all users that do not have EWS permissions.</span></span> 
  
<span data-ttu-id="45693-137">若要启用模拟帐户，测试或生产服务器管理员应执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="45693-137">To enable impersonation accounts, your test or production server administrator should do one of the following:</span></span> 
  
- <span data-ttu-id="45693-138">将 "已通过身份验证的用户" 组添加到 "之前的 Win2K" 兼容访问组。</span><span class="sxs-lookup"><span data-stu-id="45693-138">Add the Authenticated Users group to the Pre-Win2K Compatible Access Group.</span></span> 
    
- <span data-ttu-id="45693-139">将 "Exchange 服务器" 组添加到 "Windows 授权访问" 组。</span><span class="sxs-lookup"><span data-stu-id="45693-139">Add the Exchange Servers group to the Windows Authorization Access group.</span></span> 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a><span data-ttu-id="45693-140">用于 access management 的 Exchange 命令行管理程序 cmdlet</span><span class="sxs-lookup"><span data-stu-id="45693-140">Exchange Management Shell cmdlets for access management</span></span>
<span data-ttu-id="45693-141"><a name="bk_cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="45693-141"><a name="bk_cmdlets"> </a></span></span>

<span data-ttu-id="45693-142">管理员使用以下 Exchange 命令行管理程序 cmdlet 来配置 EWS 访问控制：</span><span class="sxs-lookup"><span data-stu-id="45693-142">Administrators use the following Exchange Management Shell cmdlets to configure EWS access controls:</span></span> 
  
- [<span data-ttu-id="45693-143">Get-CASMailbox</span><span class="sxs-lookup"><span data-stu-id="45693-143">Get-CASMailbox</span></span>](https://technet.microsoft.com/library/bb124754.aspx)   
- [<span data-ttu-id="45693-144">Set-CASMailbox</span><span class="sxs-lookup"><span data-stu-id="45693-144">Set-CASMailbox</span></span>](https://technet.microsoft.com/library/bb125264.aspx)   
- [<span data-ttu-id="45693-145">Set-organizationconfig</span><span class="sxs-lookup"><span data-stu-id="45693-145">Get-OrganizationConfig</span></span>](https://technet.microsoft.com/library/aa997571.aspx)   
- [<span data-ttu-id="45693-146">Set-organizationconfig</span><span class="sxs-lookup"><span data-stu-id="45693-146">Set-OrganizationConfig</span></span>](https://technet.microsoft.com/library/aa997443.aspx)
    
## <a name="see-also"></a><span data-ttu-id="45693-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="45693-147">See also</span></span>

- [<span data-ttu-id="45693-148">开始使用 Exchange 中的 Web 服务</span><span class="sxs-lookup"><span data-stu-id="45693-148">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)  
- [<span data-ttu-id="45693-149">在 Exchange 中控制对 EWS 的访问</span><span class="sxs-lookup"><span data-stu-id="45693-149">Control access to EWS in Exchange</span></span>](how-to-control-access-to-ews-in-exchange.md)
- [<span data-ttu-id="45693-150">Exchange Server PowerShell （Exchange 命令行管理程序）</span><span class="sxs-lookup"><span data-stu-id="45693-150">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [<span data-ttu-id="45693-151">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="45693-151">Windows PowerShell</span></span>](https://msdn.microsoft.com/library/dd835506%28v=vs.85%29.aspx)
    

