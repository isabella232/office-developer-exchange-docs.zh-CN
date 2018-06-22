---
title: 模拟和 Exchange 中的 EWS
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: 了解如何以及何时在您的 Exchange 服务应用程序中使用模拟。
ms.openlocfilehash: f8a215874475034f0d147b80a05cae414e6438f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752899"
---
# <a name="impersonation-and-ews-in-exchange"></a><span data-ttu-id="c4f3f-103">模拟和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c4f3f-103">Impersonation and EWS in Exchange</span></span>

<span data-ttu-id="c4f3f-104">了解如何以及何时在您的 Exchange[服务应用程序](ews-application-types.md)中使用模拟。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-104">Learn how and when to use impersonation in your Exchange [service applications](ews-application-types.md).</span></span>
  
<span data-ttu-id="c4f3f-105">您可以让用户能够访问其他用户的邮箱的三种方式之一：</span><span class="sxs-lookup"><span data-stu-id="c4f3f-105">You can enable users to access other users' mailboxes in one of three ways:</span></span>
  
- <span data-ttu-id="c4f3f-106">添加代理人，并指定每个代理人的权限。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-106">By adding delegates and specifying permissions for each delegate.</span></span>
    
- <span data-ttu-id="c4f3f-107">通过直接修改文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-107">By modifying folder permissions directly.</span></span>
    
- <span data-ttu-id="c4f3f-108">使用模拟。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-108">By using impersonation.</span></span>
    
<span data-ttu-id="c4f3f-109">何时您应通过委派或文件夹的权限中选择模拟</span><span class="sxs-lookup"><span data-stu-id="c4f3f-109">When should you choose impersonation over delegation or folder permissions?</span></span> <span data-ttu-id="c4f3f-110">以下指南将帮助您决定：</span><span class="sxs-lookup"><span data-stu-id="c4f3f-110">The following guidelines will help you decide:</span></span>
  
- <span data-ttu-id="c4f3f-111">当您想要提供用户访问的文件夹，但不是希望用户具有"代表发送"权限，请使用文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-111">Use folder permissions when you want to provide a user access to a folder but do not want the user to have "send on behalf of" permissions.</span></span> 
    
- <span data-ttu-id="c4f3f-112">您想要赋予一个用户的权限以执行代表另一个用户工作时使用代理访问。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-112">Use delegate access when you want to give one user permission to perform work on behalf of another user.</span></span> <span data-ttu-id="c4f3f-113">通常，这是一个一对一或一个到几权限-例如，管理日历的管理员或管理一组会议室的日历的单个会议室计划单个行政助理。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-113">Typically, this is a one-to-one or one-to-a-few permission - for example, a single administrative assistant managing the calendar for an administrator, or a single room scheduler managing the calendars for a group of meeting rooms.</span></span>
    
- <span data-ttu-id="c4f3f-114">需要访问多个邮箱和"作为"邮箱所有者的服务应用程序后，请使用模拟。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-114">Use impersonation when you have a service application that needs to access multiple mailboxes and "act as" the mailbox owner.</span></span>
    
<span data-ttu-id="c4f3f-115">模拟时您处理与多个邮箱因为您可以轻松地一个服务帐户授予访问权限的每个邮箱数据库中的最佳选择。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-115">Impersonation is the best choice when you're dealing with multiple mailboxes because you can easily grant one service account access to every mailbox in a database.</span></span> <span data-ttu-id="c4f3f-116">委派和文件夹权限是最佳时要仅对少数用户授权访问因为您需要为每个邮箱单独添加权限。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-116">Delegation and folder permissions are best when you're only granting access to a few users, because you have to add permissions individually to each mailbox.</span></span> <span data-ttu-id="c4f3f-117">图 1 显示了一些每种类型的访问之间的差异。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-117">Figure 1 shows some of the differences between each type of access.</span></span>
  
<span data-ttu-id="c4f3f-118">**图 1。方式访问其他用户的邮箱**</span><span class="sxs-lookup"><span data-stu-id="c4f3f-118">**Figure 1. Ways to access other users' mailboxes**</span></span>

![显示邮箱访问类型、邮箱所有者与每种类型的委派之间的关系以及权限类型的图表。代表委派权限和/或文件夹权限发送。用于模拟的发送身份权限。](media/Ex15_Delegate_Overview.png)
  
<span data-ttu-id="c4f3f-122">模拟非常适合于连接到 Exchange Online 中，Exchange Online 作为 Office 365 的一部分的应用程序和本地 Exchange 版本以及执行操作，如存档电子邮件、 设置 OOF 自动用户度假或任何其他任务需要应用程序用作邮箱的所有者的。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-122">Impersonation is ideal for applications that connect to Exchange Online, Exchange Online as part of Office 365, and on-premises versions of Exchange and perform operations, such as archiving email, setting OOF automatically for users on vacation, or any other task that requires that the application act as the owner of a mailbox.</span></span> <span data-ttu-id="c4f3f-123">当应用程序使用模拟时发送一条消息时，显示从邮箱所有者发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-123">When an application uses impersonation to send a message, the email appears to be sent from the mailbox owner.</span></span> <span data-ttu-id="c4f3f-124">没有要了解的服务帐户已发送邮件的收件人方法。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-124">There is no way for the recipient to know the mail was sent by the service account.</span></span> <span data-ttu-id="c4f3f-125">委派，另一方面，使其他邮箱帐户权限，才能代表邮箱所有者操作。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-125">Delegation, on the other hand, gives another mailbox account permission to act on behalf of a mailbox owner.</span></span> <span data-ttu-id="c4f3f-126">当由代理发送一封电子邮件时，"从"值标识邮箱所有者，并且"发件人"值标识已发送邮件的代理人。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-126">When an email message is sent by a delegate, the "from" value identifies the mailbox owner, and the "sender" value identifies the delegate that sent the mail.</span></span> 
  
## <a name="security-considerations-for-impersonation"></a><span data-ttu-id="c4f3f-127">模拟的安全注意事项</span><span class="sxs-lookup"><span data-stu-id="c4f3f-127">Security considerations for impersonation</span></span>

<span data-ttu-id="c4f3f-128">模拟使呼叫者可以模拟的给定的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-128">Impersonation enables a caller to impersonate a given user account.</span></span> <span data-ttu-id="c4f3f-129">这样呼叫者使用模拟的帐户，而不是与呼叫者的帐户相关联的权限与关联的权限执行操作。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-129">This enables the caller to perform operations by using the permissions that are associated with the impersonated account, instead of the permissions that are associated with the caller's account.</span></span> <span data-ttu-id="c4f3f-130">因此，您应了解以下安全注意事项：</span><span class="sxs-lookup"><span data-stu-id="c4f3f-130">For this reason, you should be aware of the following security considerations:</span></span>
  
- <span data-ttu-id="c4f3f-131">已由 Exchange 服务器管理员授予**ApplicationImpersonation**角色的帐户可以使用模拟。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-131">Only accounts that have been granted the **ApplicationImpersonation** role by an Exchange server administrator can use impersonation.</span></span> 
    
- <span data-ttu-id="c4f3f-132">您应创建一个管理作用域限制模拟至一组指定的帐户。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-132">You should create a management scope that limits impersonation to a specified group of accounts.</span></span> <span data-ttu-id="c4f3f-133">如果未创建管理作用域，则**ApplicationImpersonation**角色授予在组织中的所有帐户。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-133">If you do not create a management scope, the **ApplicationImpersonation** role is granted to all accounts in an organization.</span></span> 
    
- <span data-ttu-id="c4f3f-134">通常，**通过 ApplicationImpersonation**角色授予专用于特定应用程序或应用程序的组的服务帐户，而不是用户帐户。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-134">Typically, the **ApplicationImpersonation** role is granted to a service account dedicated to a particular application or group of applications, rather than a user account.</span></span> <span data-ttu-id="c4f3f-135">您可以根据需要您可以创建多个或尽可能少的服务帐户。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-135">You can create as many or as few service accounts as you need.</span></span> 
    
<span data-ttu-id="c4f3f-136">您可以阅读更多有关[配置模拟](how-to-configure-impersonation.md)，但您应使用您的 Exchange 管理员以确保所需的服务帐户创建的[权限和访问](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx)满足的安全要求与您组织。</span><span class="sxs-lookup"><span data-stu-id="c4f3f-136">You can read more about [configuring impersonation](how-to-configure-impersonation.md), but you should work with your Exchange administrator to ensure that the service accounts that you need are created with the [permissions and access](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx) that meet the security requirements of your organization.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="c4f3f-137">本节内容</span><span class="sxs-lookup"><span data-stu-id="c4f3f-137">In this section</span></span>

- [<span data-ttu-id="c4f3f-138">配置模拟</span><span class="sxs-lookup"><span data-stu-id="c4f3f-138">Configure impersonation</span></span>](how-to-configure-impersonation.md)
    
- [<span data-ttu-id="c4f3f-139">确定要模拟的帐户</span><span class="sxs-lookup"><span data-stu-id="c4f3f-139">Identify the account to impersonate</span></span>](how-to-identify-the-account-to-impersonate.md)
    
- [<span data-ttu-id="c4f3f-140">使用 Exchange 模拟添加约会</span><span class="sxs-lookup"><span data-stu-id="c4f3f-140">Add appointments by using Exchange impersonation</span></span>](how-to-add-appointments-by-using-exchange-impersonation.md)
    
## <a name="see-also"></a><span data-ttu-id="c4f3f-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c4f3f-141">See also</span></span>


- [<span data-ttu-id="c4f3f-142">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="c4f3f-142">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="c4f3f-143">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c4f3f-143">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c4f3f-144">Exchange 2013 权限</span><span class="sxs-lookup"><span data-stu-id="c4f3f-144">Exchange 2013 Permissions</span></span>](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx)
    

