---
title: Impersonation and EWS in Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: 了解如何以及何时在 Exchange 服务应用程序中使用模拟。
localization_priority: Priority
ms.openlocfilehash: 8151b3d83421786d99ee0c82eaf4f7a5c0721f25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466610"
---
# <a name="impersonation-and-ews-in-exchange"></a><span data-ttu-id="8c21e-103">Impersonation and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="8c21e-103">Impersonation and EWS in Exchange</span></span>

<span data-ttu-id="8c21e-104">了解如何以及何时在 Exchange[服务应用程序](ews-application-types.md)中使用模拟。</span><span class="sxs-lookup"><span data-stu-id="8c21e-104">Learn how and when to use impersonation in your Exchange [service applications](ews-application-types.md).</span></span>
  
<span data-ttu-id="8c21e-105">您可以通过以下三种方式之一使用户能够访问其他用户的邮箱：</span><span class="sxs-lookup"><span data-stu-id="8c21e-105">You can enable users to access other users' mailboxes in one of three ways:</span></span>
  
- <span data-ttu-id="8c21e-106">通过添加委派并为每个代理指定权限。</span><span class="sxs-lookup"><span data-stu-id="8c21e-106">By adding delegates and specifying permissions for each delegate.</span></span>
    
- <span data-ttu-id="8c21e-107">通过直接修改文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="8c21e-107">By modifying folder permissions directly.</span></span>
    
- <span data-ttu-id="8c21e-108">通过使用模拟。</span><span class="sxs-lookup"><span data-stu-id="8c21e-108">By using impersonation.</span></span>
    
<span data-ttu-id="8c21e-109">何时应选择模拟而不是委派或文件夹权限？</span><span class="sxs-lookup"><span data-stu-id="8c21e-109">When should you choose impersonation over delegation or folder permissions?</span></span> <span data-ttu-id="8c21e-110">以下指南将帮助您做出决定：</span><span class="sxs-lookup"><span data-stu-id="8c21e-110">The following guidelines will help you decide:</span></span>
  
- <span data-ttu-id="8c21e-111">当您希望提供用户对文件夹的访问权限但不希望用户具有 "代表发送" 权限时，可使用文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="8c21e-111">Use folder permissions when you want to provide a user access to a folder but do not want the user to have "send on behalf of" permissions.</span></span> 
    
- <span data-ttu-id="8c21e-112">如果要授予一个用户代表另一个用户执行工作的权限，请使用委派访问权限。</span><span class="sxs-lookup"><span data-stu-id="8c21e-112">Use delegate access when you want to give one user permission to perform work on behalf of another user.</span></span> <span data-ttu-id="8c21e-113">通常情况下，这是一对一或一对一的权限，例如，管理管理员日历的单个管理助理，或者是管理一组会议室的日历的单一聊天室计划程序。</span><span class="sxs-lookup"><span data-stu-id="8c21e-113">Typically, this is a one-to-one or one-to-a-few permission - for example, a single administrative assistant managing the calendar for an administrator, or a single room scheduler managing the calendars for a group of meeting rooms.</span></span>
    
- <span data-ttu-id="8c21e-114">当您有需要访问多个邮箱并 "充当" 邮箱所有者的服务应用程序时，请使用模拟。</span><span class="sxs-lookup"><span data-stu-id="8c21e-114">Use impersonation when you have a service application that needs to access multiple mailboxes and "act as" the mailbox owner.</span></span>
    
<span data-ttu-id="8c21e-115">当您处理多个邮箱时，模拟是最佳选择，因为您可以轻松授予一个服务帐户对数据库中每个邮箱的访问权限。</span><span class="sxs-lookup"><span data-stu-id="8c21e-115">Impersonation is the best choice when you're dealing with multiple mailboxes because you can easily grant one service account access to every mailbox in a database.</span></span> <span data-ttu-id="8c21e-116">委派和文件夹权限最适用于仅授予几个用户的访问权限，因为您必须将权限单独添加到每个邮箱。</span><span class="sxs-lookup"><span data-stu-id="8c21e-116">Delegation and folder permissions are best when you're only granting access to a few users, because you have to add permissions individually to each mailbox.</span></span> <span data-ttu-id="8c21e-117">图1显示了每种类型的访问权限之间的一些差异。</span><span class="sxs-lookup"><span data-stu-id="8c21e-117">Figure 1 shows some of the differences between each type of access.</span></span>
  
<span data-ttu-id="8c21e-118">**图1。访问其他用户的邮箱的方法**</span><span class="sxs-lookup"><span data-stu-id="8c21e-118">**Figure 1. Ways to access other users' mailboxes**</span></span>

![显示邮箱访问类型、邮箱所有者与每种类型的委派之间的关系以及权限类型的图表。代表委派权限和/或文件夹权限发送。用于模拟的发送身份权限。](media/Ex15_Delegate_Overview.png)
  
<span data-ttu-id="8c21e-122">模拟非常适合于连接到 Exchange Online 的应用程序、Exchange Online 作为 Office 365 的一部分以及 Exchange 的本地版本，以及执行操作（如存档电子邮件、在假期中自动为用户设置 OOF）或任何其他需要该应用程序充当邮箱所有者的任务。</span><span class="sxs-lookup"><span data-stu-id="8c21e-122">Impersonation is ideal for applications that connect to Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange and perform operations, such as archiving email, setting OOF automatically for users on vacation, or any other task that requires that the application act as the owner of a mailbox.</span></span> <span data-ttu-id="8c21e-123">当应用程序使用模拟发送邮件时，电子邮件似乎将从邮箱所有者发送。</span><span class="sxs-lookup"><span data-stu-id="8c21e-123">When an application uses impersonation to send a message, the email appears to be sent from the mailbox owner.</span></span> <span data-ttu-id="8c21e-124">收件人无法知道该邮件是由服务帐户发送的。</span><span class="sxs-lookup"><span data-stu-id="8c21e-124">There is no way for the recipient to know the mail was sent by the service account.</span></span> <span data-ttu-id="8c21e-125">另一方面，委派将授予另一个邮箱帐户代表邮箱所有者执行操作的权限。</span><span class="sxs-lookup"><span data-stu-id="8c21e-125">Delegation, on the other hand, gives another mailbox account permission to act on behalf of a mailbox owner.</span></span> <span data-ttu-id="8c21e-126">当代理发送电子邮件时，"发件人" 值标识邮箱所有者，"发件人" 值标识发送邮件的代理。</span><span class="sxs-lookup"><span data-stu-id="8c21e-126">When an email message is sent by a delegate, the "from" value identifies the mailbox owner, and the "sender" value identifies the delegate that sent the mail.</span></span> 
  
## <a name="security-considerations-for-impersonation"></a><span data-ttu-id="8c21e-127">模拟的安全注意事项</span><span class="sxs-lookup"><span data-stu-id="8c21e-127">Security considerations for impersonation</span></span>

<span data-ttu-id="8c21e-128">模拟使呼叫者能够模拟给定的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="8c21e-128">Impersonation enables a caller to impersonate a given user account.</span></span> <span data-ttu-id="8c21e-129">这样，调用方可以使用与模拟帐户关联的权限（而不是与呼叫者帐户关联的权限）执行操作。</span><span class="sxs-lookup"><span data-stu-id="8c21e-129">This enables the caller to perform operations by using the permissions that are associated with the impersonated account, instead of the permissions that are associated with the caller's account.</span></span> <span data-ttu-id="8c21e-130">出于此原因，应注意以下安全注意事项：</span><span class="sxs-lookup"><span data-stu-id="8c21e-130">For this reason, you should be aware of the following security considerations:</span></span>
  
- <span data-ttu-id="8c21e-131">只有已通过 Exchange server 管理员授予**ApplicationImpersonation**角色的帐户才能使用模拟。</span><span class="sxs-lookup"><span data-stu-id="8c21e-131">Only accounts that have been granted the **ApplicationImpersonation** role by an Exchange server administrator can use impersonation.</span></span> 
    
- <span data-ttu-id="8c21e-132">应创建将模拟限制为指定帐户组的管理作用域。</span><span class="sxs-lookup"><span data-stu-id="8c21e-132">You should create a management scope that limits impersonation to a specified group of accounts.</span></span> <span data-ttu-id="8c21e-133">如果不创建管理作用域，则会向组织中的所有帐户授予**ApplicationImpersonation**角色。</span><span class="sxs-lookup"><span data-stu-id="8c21e-133">If you do not create a management scope, the **ApplicationImpersonation** role is granted to all accounts in an organization.</span></span> 
    
- <span data-ttu-id="8c21e-134">通常情况下， **ApplicationImpersonation**角色被授予专用于特定应用程序或应用程序组的服务帐户，而不是用户帐户。</span><span class="sxs-lookup"><span data-stu-id="8c21e-134">Typically, the **ApplicationImpersonation** role is granted to a service account dedicated to a particular application or group of applications, rather than a user account.</span></span> <span data-ttu-id="8c21e-135">您可以根据需要创建任意多个服务帐户。</span><span class="sxs-lookup"><span data-stu-id="8c21e-135">You can create as many or as few service accounts as you need.</span></span> 
    
<span data-ttu-id="8c21e-136">您可以阅读有关[配置模拟](how-to-configure-impersonation.md)的详细信息，但应与 Exchange 管理员合作，以确保使用符合组织的安全要求的[权限和访问权限](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)创建所需的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="8c21e-136">You can read more about [configuring impersonation](how-to-configure-impersonation.md), but you should work with your Exchange administrator to ensure that the service accounts that you need are created with the [permissions and access](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) that meet the security requirements of your organization.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="8c21e-137">本节内容</span><span class="sxs-lookup"><span data-stu-id="8c21e-137">In this section</span></span>

- [<span data-ttu-id="8c21e-138">配置模拟</span><span class="sxs-lookup"><span data-stu-id="8c21e-138">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="8c21e-139">确定要模拟的帐户</span><span class="sxs-lookup"><span data-stu-id="8c21e-139">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="8c21e-140">使用 Exchange 模拟添加约会</span><span class="sxs-lookup"><span data-stu-id="8c21e-140">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
## <a name="see-also"></a><span data-ttu-id="8c21e-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8c21e-141">See also</span></span>


- [<span data-ttu-id="8c21e-142">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="8c21e-142">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="8c21e-143">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="8c21e-143">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
    
- [<span data-ttu-id="8c21e-144">Exchange 2013 权限</span><span class="sxs-lookup"><span data-stu-id="8c21e-144">Exchange 2013 Permissions</span></span>](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

