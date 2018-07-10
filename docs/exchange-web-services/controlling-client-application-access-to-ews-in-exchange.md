---
title: 在 Exchange 控制客户端应用程序访问 EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60ac3f7b-ba8a-4c93-99f7-c27002caff93
description: 了解用于管理客户端应用程序访问 EWS 的选项。
ms.openlocfilehash: 29a640178afc9814a0b2232225ae4307e49afed2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752706"
---
# <a name="controlling-client-application-access-to-ews-in-exchange"></a><span data-ttu-id="d0df6-103">在 Exchange 控制客户端应用程序访问 EWS</span><span class="sxs-lookup"><span data-stu-id="d0df6-103">Controlling client application access to EWS in Exchange</span></span>

<span data-ttu-id="d0df6-104">了解用于管理客户端应用程序访问 EWS 的选项。</span><span class="sxs-lookup"><span data-stu-id="d0df6-104">Learn about the options for managing client application access to EWS.</span></span>
  
<span data-ttu-id="d0df6-105">您创建任何 EWS 客户端应用程序必须授予访问 Exchange Online 中，为 Office 365 的一部分或 Exchange 版本的 Exchange Online 开头 Exchange 2013，才能调用 EWS 操作。</span><span class="sxs-lookup"><span data-stu-id="d0df6-105">Any EWS client application that you create must be granted access to Exchange Online, Exchange Online as part of Office 365, or version of Exchange starting with Exchange 2013 before it can call EWS operations.</span></span> <span data-ttu-id="d0df6-106">测试或生产服务器管理员可以使用 Exchange 命令行管理程序来限制对 EWS 的所有用户和应用程序，为各个用户，或单独的应用程序的访问。</span><span class="sxs-lookup"><span data-stu-id="d0df6-106">Test or production server administrators can use the Exchange Management Shell to limit access to EWS either for all users and applications, for individual users, or for individual applications.</span></span> <span data-ttu-id="d0df6-107">EWS 的访问控制基于域帐户。</span><span class="sxs-lookup"><span data-stu-id="d0df6-107">Access control for EWS is based on domain accounts.</span></span> <span data-ttu-id="d0df6-108">当使用通过本地安全机构进行身份验证的凭据进行连接时，服务器将返回一条错误，指示可以连接仅域帐户。</span><span class="sxs-lookup"><span data-stu-id="d0df6-108">When a connection is made with credentials that are authenticated by the local security authority, the server returns an error that indicates that only domain accounts can connect.</span></span> 
  
## <a name="access-control-for-ews-clients-and-users"></a><span data-ttu-id="d0df6-109">EWS 客户端和用户的访问控制</span><span class="sxs-lookup"><span data-stu-id="d0df6-109">Access control for EWS clients and users</span></span>
<span data-ttu-id="d0df6-110"><a name="bk_configure"> </a></span><span class="sxs-lookup"><span data-stu-id="d0df6-110"></span></span>

<span data-ttu-id="d0df6-111">测试或生产服务器管理员可以配置为按以下方式连接到 EWS 的客户端访问控制：</span><span class="sxs-lookup"><span data-stu-id="d0df6-111">Your test or production server administrator can configure access control for clients that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="d0df6-112">通过阻止连接的所有客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="d0df6-112">By blocking all client applications from connecting.</span></span>
    
- <span data-ttu-id="d0df6-113">通过允许特定客户端应用程序仅连接。</span><span class="sxs-lookup"><span data-stu-id="d0df6-113">By allowing specific client applications only to connect.</span></span>
    
- <span data-ttu-id="d0df6-114">通过允许任何客户端应用程序连接除外明确阻止。</span><span class="sxs-lookup"><span data-stu-id="d0df6-114">By allowing any client application to connect except those that are specifically blocked.</span></span>
    
- <span data-ttu-id="d0df6-115">通过允许任何客户端应用程序连接。</span><span class="sxs-lookup"><span data-stu-id="d0df6-115">By allowing any client application to connect.</span></span>
    
<span data-ttu-id="d0df6-116">由发送 HTTP web 请求中的用户代理字符串标识应用程序。</span><span class="sxs-lookup"><span data-stu-id="d0df6-116">Applications are identified by the user agent string that they send in the HTTP web request.</span></span>
  
> [!安全注释]<span data-ttu-id="d0df6-117"> 应用程序级阻止不安全功能。</span><span class="sxs-lookup"><span data-stu-id="d0df6-117"> Application-level blocking is not a security feature.</span></span> <span data-ttu-id="d0df6-118">容易造假用户代理字符串。</span><span class="sxs-lookup"><span data-stu-id="d0df6-118">The user agent string is easily spoofed.</span></span> <span data-ttu-id="d0df6-119">如果 EWS 访问允许应用程序，则该应用程序必须仍提供凭据的服务器进行身份验证应用程序可以连接到 EWS 之前。</span><span class="sxs-lookup"><span data-stu-id="d0df6-119">If an application is allowed access to EWS, the application must still present credentials that the server authenticates before the application can connect to EWS.</span></span> 
  
<span data-ttu-id="d0df6-120">管理员还可以配置为按以下方式连接到 EWS 的邮箱所有者的访问控制：</span><span class="sxs-lookup"><span data-stu-id="d0df6-120">Administrators can also configure access control for mailbox owners that connect to EWS in the following ways:</span></span> 
  
- <span data-ttu-id="d0df6-121">通过阻止或允许整个组织。</span><span class="sxs-lookup"><span data-stu-id="d0df6-121">By blocking or allowing an entire organization.</span></span>
    
- <span data-ttu-id="d0df6-122">通过阻止或允许一组用户标识的基于角色的身份验证的范围包含或排除是否有权访问 EWS 的邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="d0df6-122">By blocking or allowing a group of users identified by a role-based authentication scope that includes or excludes mailbox owners that do not have access to EWS.</span></span>
    
- <span data-ttu-id="d0df6-123">通过阻止或允许单个邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="d0df6-123">By blocking or allowing an individual mailbox owner.</span></span>
    
<span data-ttu-id="d0df6-124">特定的访问控制设置重写常规的访问控制设置。</span><span class="sxs-lookup"><span data-stu-id="d0df6-124">Specific access control settings override general access control settings.</span></span> <span data-ttu-id="d0df6-125">例如，如果组织拒绝 EWS 访问，但允许应用程序访问各个邮箱所有者，单个设置生效，并允许访问。</span><span class="sxs-lookup"><span data-stu-id="d0df6-125">For example, if an organization denies EWS access but an individual mailbox owner is allowed application access, the individual setting prevails and access is allowed.</span></span> 
  
## <a name="delegation-and-ews-access-management"></a><span data-ttu-id="d0df6-126">委派和 EWS 访问管理</span><span class="sxs-lookup"><span data-stu-id="d0df6-126">Delegation and EWS access management</span></span>
<span data-ttu-id="d0df6-127"><a name="bk_delegation"> </a></span><span class="sxs-lookup"><span data-stu-id="d0df6-127"></span></span>

<span data-ttu-id="d0df6-128">当委托用户不具有访问 EWS 使用客户端应用程序，它们将不能使用访问主体用户邮箱 EWS，即使主体用户具有 EWS 访问。</span><span class="sxs-lookup"><span data-stu-id="d0df6-128">When delegate users who do not have access to EWS use your client application, they will not be able to access the principal user's mailbox by using EWS, even if the principal user has EWS access.</span></span> <span data-ttu-id="d0df6-129">如果代理用户具有的 EWS 访问，代理将能够使用 EWS 客户端应用程序访问主体用户的邮箱，即使主体用户不具有 EWS 访问。</span><span class="sxs-lookup"><span data-stu-id="d0df6-129">If the delegate user has EWS access, the delegate will be able to use your EWS client application to access the principal user's mailbox even if the principal user does not have EWS access.</span></span> 
  
## <a name="impersonation-and-ews-access-management"></a><span data-ttu-id="d0df6-130">模拟和 EWS 访问管理</span><span class="sxs-lookup"><span data-stu-id="d0df6-130">Impersonation and EWS access management</span></span>
<span data-ttu-id="d0df6-131"><a name="bk_impersonation"> </a></span><span class="sxs-lookup"><span data-stu-id="d0df6-131"></span></span>

<span data-ttu-id="d0df6-132">连接到 EWS 代表邮箱所有者的客户端应用程序可能无法使用 EWS 设置邮箱所有者。</span><span class="sxs-lookup"><span data-stu-id="d0df6-132">Client applications that connect to EWS on behalf of mailbox owners might not be able to use the EWS settings of the mailbox owner.</span></span> <span data-ttu-id="d0df6-133">例如，存档的应用程序电子邮件消息的公司已连接到 EWS 无论哪些邮箱用户的设置。</span><span class="sxs-lookup"><span data-stu-id="d0df6-133">For example, an application that archives email messages for a company has to connect to EWS regardless of what the mailbox users' settings are.</span></span> <span data-ttu-id="d0df6-134">其他应用程序，如邮件客户端，不必要使用邮箱所有者的 EWS 设置。</span><span class="sxs-lookup"><span data-stu-id="d0df6-134">Other applications, such as mail clients, do have to use the mailbox owner's EWS settings.</span></span> 
  
<span data-ttu-id="d0df6-135">管理员应创建模拟帐户为每个应用程序或他们在其服务器使用的应用程序类。</span><span class="sxs-lookup"><span data-stu-id="d0df6-135">Administrators should create an impersonation account for each application or application class that they use on their server.</span></span> <span data-ttu-id="d0df6-136">这将使管理员能够配置没有 EWS 权限的所有用户的基于角色的访问控制范围。</span><span class="sxs-lookup"><span data-stu-id="d0df6-136">This will enable the administrator to configure the role-based access control scope for all users that do not have EWS permissions.</span></span> 
  
<span data-ttu-id="d0df6-137">若要启用模拟帐户，测试或生产服务器管理员应执行以下任一操作：</span><span class="sxs-lookup"><span data-stu-id="d0df6-137">To enable impersonation accounts, your test or production server administrator should do one of the following:</span></span> 
  
- <span data-ttu-id="d0df6-138">向之前 Win2K 兼容 Access 组添加 Authenticated Users 组。</span><span class="sxs-lookup"><span data-stu-id="d0df6-138">Add the Authenticated Users group to the Pre-Win2K Compatible Access Group.</span></span> 
    
- <span data-ttu-id="d0df6-139">向 Windows 授权 Access 组添加 Exchange 服务器组。</span><span class="sxs-lookup"><span data-stu-id="d0df6-139">Add the Exchange Servers group to the Windows Authorization Access group.</span></span> 
    
## <a name="exchange-management-shell-cmdlets-for-access-management"></a><span data-ttu-id="d0df6-140">用于访问管理 Exchange 命令行管理程序 cmdlet</span><span class="sxs-lookup"><span data-stu-id="d0df6-140">Exchange Management Shell cmdlets for access management</span></span>
<span data-ttu-id="d0df6-141"><a name="bk_cmdlets"> </a></span><span class="sxs-lookup"><span data-stu-id="d0df6-141"></span></span>

<span data-ttu-id="d0df6-142">管理员使用下面的 Exchange 命令行管理程序 cmdlet 配置 EWS 访问控制：</span><span class="sxs-lookup"><span data-stu-id="d0df6-142">Administrators use the following Exchange Management Shell cmdlets to configure EWS access controls:</span></span> 
  
- [<span data-ttu-id="d0df6-143">Get-casmailbox</span><span class="sxs-lookup"><span data-stu-id="d0df6-143">Get-CASMailbox</span></span>](http://technet.microsoft.com/zh-cn/library/bb124754.aspx)
    
- [<span data-ttu-id="d0df6-144">设置 CASMailbox</span><span class="sxs-lookup"><span data-stu-id="d0df6-144">Set-CASMailbox</span></span>](http://technet.microsoft.com/zh-cn/library/bb125264.aspx)
    
- [<span data-ttu-id="d0df6-145">Get-organizationconfig</span><span class="sxs-lookup"><span data-stu-id="d0df6-145">Get-OrganizationConfig</span></span>](http://technet.microsoft.com/zh-cn/library/aa997571.aspx)
    
- [<span data-ttu-id="d0df6-146">Set-organizationconfig</span><span class="sxs-lookup"><span data-stu-id="d0df6-146">Set-OrganizationConfig</span></span>](http://technet.microsoft.com/zh-cn/library/aa997443.aspx)
    
## <a name="see-also"></a><span data-ttu-id="d0df6-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0df6-147">See also</span></span>

- [<span data-ttu-id="d0df6-148">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="d0df6-148">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)  
- [<span data-ttu-id="d0df6-149">在 Exchange 控制对 EWS 的访问</span><span class="sxs-lookup"><span data-stu-id="d0df6-149">Control access to EWS in Exchange</span></span>](how-to-control-access-to-ews-in-exchange.md)
- [<span data-ttu-id="d0df6-150">Exchange Server PowerShell （Exchange 命令行管理程序）</span><span class="sxs-lookup"><span data-stu-id="d0df6-150">Exchange Server PowerShell (Exchange Management Shell)</span></span>](https://docs.microsoft.com/zh-cn/powershell/exchange/exchange-server/exchange-management-shell?view=exchange-ps)
- [<span data-ttu-id="d0df6-151">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d0df6-151">Windows PowerShell</span></span>](http://msdn.microsoft.com/zh-cn/library/dd835506%28v=vs.85%29.aspx)
    

