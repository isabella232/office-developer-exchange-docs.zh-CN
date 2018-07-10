---
title: 在 Exchange 使用 EWS 设置另一个用户的文件夹权限
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: 了解如何使用 EWS 的 EWS 托管 API 在 Exchange 文件夹上设置权限级别。
ms.openlocfilehash: 5bf570612d6349628e7f3abf858daa33daa13745
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752888"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a><span data-ttu-id="e8010-103">在 Exchange 使用 EWS 设置另一个用户的文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-103">Set folder permissions for another user by using EWS in Exchange</span></span>

<span data-ttu-id="e8010-104">了解如何使用 EWS 的 EWS 托管 API 在 Exchange 文件夹上设置权限级别。</span><span class="sxs-lookup"><span data-stu-id="e8010-104">Learn how to set permission levels on a folder by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="e8010-105">文件夹级权限允许用户访问另一个用户的邮箱中的一个或多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-105">Folder-level permissions enable users to access one or more folders in another user's mailbox.</span></span> <span data-ttu-id="e8010-106">文件夹权限类似委派访问权限，但它们按以下方式有所区别：</span><span class="sxs-lookup"><span data-stu-id="e8010-106">Folder permissions are similar to delegate access, but they differ in the following ways:</span></span> 
  
- <span data-ttu-id="e8010-107">文件夹权限不启用用户"代表发送"或"发送为"另一个用户。</span><span class="sxs-lookup"><span data-stu-id="e8010-107">Folder permissions do not enable a user to "send on behalf of" or "send as" another user.</span></span> <span data-ttu-id="e8010-108">它们仅允许访问文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-108">They only enable access to folders.</span></span> <span data-ttu-id="e8010-109">用户可以在这些文件夹中，创建项目，但他们不能向他们发送。</span><span class="sxs-lookup"><span data-stu-id="e8010-109">Users can create items in those folders, but they can't send them.</span></span>
    
- <span data-ttu-id="e8010-110">您可以设置邮箱中的任何文件夹文件夹权限，但仅可以将代理添加到的日历、 联系人、 收件箱、 日记、 备注和任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-110">You can set folder permissions on any folder in the mailbox, but you can only add a delegate to the Calendar, Contacts, Inbox, Journal, Notes, and Tasks folders.</span></span>
    
- <span data-ttu-id="e8010-111">您可以设置多个[特定文件夹的权限](#bk_folderperms)。</span><span class="sxs-lookup"><span data-stu-id="e8010-111">You can set a number of [permissions on a specific folder](#bk_folderperms).</span></span> <span data-ttu-id="e8010-112">在添加代理时，您可以指定一个仅[五个权限级别](delegate-access-and-ews-in-exchange.md#bk_delegateperms)。</span><span class="sxs-lookup"><span data-stu-id="e8010-112">When you add a delegate, you can assign one of only [five permission levels](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span>
    
- <span data-ttu-id="e8010-113">您可以设置文件夹权限匿名和默认用户。</span><span class="sxs-lookup"><span data-stu-id="e8010-113">You can set folder permissions for anonymous and default users.</span></span> <span data-ttu-id="e8010-114">您只能授予给已启用邮件的帐户的代理访问。</span><span class="sxs-lookup"><span data-stu-id="e8010-114">You can only grant delegate access to a mail-enabled account.</span></span>
    
<span data-ttu-id="e8010-115">如果您熟悉访问控制项 (Ace) 和随机访问控制列表 (Dacl)，您就会知道用户只能有一个每个文件夹的权限集。</span><span class="sxs-lookup"><span data-stu-id="e8010-115">If you're familiar with Access Control Entries (ACEs) and Discretionary Access Control Lists (DACLs), you know that a user can only have one set of permissions for each folder.</span></span> <span data-ttu-id="e8010-116">如果您尝试添加一组权限的用户，他们已有一组权限，您将收到错误。</span><span class="sxs-lookup"><span data-stu-id="e8010-116">If you try to add a set of permissions for a user and they already have a set of permissions, you'll get an error.</span></span> <span data-ttu-id="e8010-117">当添加、 删除或更新的文件夹的权限时，您获取的当前 DACL、 添加或删除任何 Ace，，然后发送更新的 DACL。</span><span class="sxs-lookup"><span data-stu-id="e8010-117">When you add, remove, or update permissions on a folder, you get the current DACL, add or remove any ACEs, and then send the updated DACL.</span></span> <span data-ttu-id="e8010-118">不能添加多个相同的用户的 Ace。</span><span class="sxs-lookup"><span data-stu-id="e8010-118">You cannot add multiple ACEs for the same user.</span></span> <span data-ttu-id="e8010-119">使用 EWS 托管 API 更新权限时，您需要删除的用户的当前 ACE，然后将其新的 ACE 添加到集合。</span><span class="sxs-lookup"><span data-stu-id="e8010-119">When you update permissions by using the EWS Managed API, you need to remove the user's current ACE and then add their new ACE to the collection.</span></span> <span data-ttu-id="e8010-120">如果您正在使用 EWS，您只需替换 Ace 前一组新的。</span><span class="sxs-lookup"><span data-stu-id="e8010-120">If you're using EWS, you just replace the previous set of ACEs with the new ones.</span></span>
  
<span data-ttu-id="e8010-121">如果您发出多个权限更改一个文件夹，您可以批量添加、 删除或更新 — 仅请注意，您不能批处理用户更新多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-121">If you're making multiple permission changes to a single folder, you can batch additions, removals, or updates —just note that you cannot batch user updates on multiple folders.</span></span> <span data-ttu-id="e8010-122">在单个文件夹，获取权限所需的一个呼叫和第二个呼叫需要更新该文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-122">One call is required to get the permissions on a single folder, and a second call is required to update the permissions on that folder.</span></span> <span data-ttu-id="e8010-123">当添加、 删除或更新用户权限时，您可以使用相同的两种方法调用或为每项任务的操作。</span><span class="sxs-lookup"><span data-stu-id="e8010-123">When you add, remove, or update user permissions, you use the same two method calls or operations for each task.</span></span>
  
<span data-ttu-id="e8010-124">**表 1。EWS 托管 API 方法和 EWS 操作设置文件夹权限**</span><span class="sxs-lookup"><span data-stu-id="e8010-124">**Table 1. EWS Managed API methods and EWS operations for setting folder permissions**</span></span>

|<span data-ttu-id="e8010-125">如果您希望...</span><span class="sxs-lookup"><span data-stu-id="e8010-125">If you want to…</span></span>|<span data-ttu-id="e8010-126">使用此 EWS 托管 API 方法...</span><span class="sxs-lookup"><span data-stu-id="e8010-126">Use this EWS Managed API method…</span></span>|<span data-ttu-id="e8010-127">使用此 EWS 操作...</span><span class="sxs-lookup"><span data-stu-id="e8010-127">Use this EWS operation…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e8010-128">启用、 删除或更新文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-128">Enable, remove, or update folder permissions</span></span>  <br/> |<span data-ttu-id="e8010-129">[Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)跟[Folder.Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8010-129">[Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="e8010-130">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)跟[UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8010-130">[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="e8010-131">创建一个文件夹，并定义文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-131">Create a folder and define folder permissions</span></span>  <br/> |[<span data-ttu-id="e8010-132">Folder.Save</span><span class="sxs-lookup"><span data-stu-id="e8010-132">Folder.Save</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="e8010-133">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="e8010-133">CreateFolder</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a><span data-ttu-id="e8010-134">文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-134">Folder permissions</span></span>
<span data-ttu-id="e8010-135"><a name="bk_folderperms"> </a></span><span class="sxs-lookup"><span data-stu-id="e8010-135"></span></span>

<span data-ttu-id="e8010-136">当谈到在特定文件夹上设置文件夹权限，您有很多的选项。</span><span class="sxs-lookup"><span data-stu-id="e8010-136">You have quite a few options when it comes to setting folder permissions on a specific folder.</span></span> <span data-ttu-id="e8010-137">您可以在文件夹权限级别设置为每个用户，将一组预定义的单个权限添加到 DACL，也可以在文件夹设置单个权限，但不能混合和匹配。</span><span class="sxs-lookup"><span data-stu-id="e8010-137">You can set a permission level on a folder for each user, which adds a set of predefined individual permissions to the DACL, or you can set individual permissions on a folder — but you can't mix and match.</span></span>
  
<span data-ttu-id="e8010-138">可用单个权限如下：</span><span class="sxs-lookup"><span data-stu-id="e8010-138">The following individual permissions are available:</span></span>
  
- <span data-ttu-id="e8010-139">可以创建</span><span class="sxs-lookup"><span data-stu-id="e8010-139">Can create</span></span>
- <span data-ttu-id="e8010-140">可以创建子文件夹</span><span class="sxs-lookup"><span data-stu-id="e8010-140">Can create subfolders</span></span>    
- <span data-ttu-id="e8010-141">为文件夹所有者</span><span class="sxs-lookup"><span data-stu-id="e8010-141">Is folder owner</span></span>    
- <span data-ttu-id="e8010-142">是可见的文件夹</span><span class="sxs-lookup"><span data-stu-id="e8010-142">Is folder visible</span></span>    
- <span data-ttu-id="e8010-143">是文件夹联系人</span><span class="sxs-lookup"><span data-stu-id="e8010-143">Is folder contact</span></span>    
- <span data-ttu-id="e8010-144">编辑项目</span><span class="sxs-lookup"><span data-stu-id="e8010-144">Edit items</span></span>    
- <span data-ttu-id="e8010-145">删除项目</span><span class="sxs-lookup"><span data-stu-id="e8010-145">Delete items</span></span>    
- <span data-ttu-id="e8010-146">读取项目</span><span class="sxs-lookup"><span data-stu-id="e8010-146">Read items</span></span>
    
<span data-ttu-id="e8010-147">此外，下列权限级别提供了，其定义子集单个权限和值，如表 2 中所示：</span><span class="sxs-lookup"><span data-stu-id="e8010-147">In addition, the following permission levels are available, which define a subset of individual permissions and values, as shown in Table 2:</span></span>
  
- <span data-ttu-id="e8010-148">无</span><span class="sxs-lookup"><span data-stu-id="e8010-148">None</span></span>    
- <span data-ttu-id="e8010-149">Owner</span><span class="sxs-lookup"><span data-stu-id="e8010-149">Owner</span></span>    
- <span data-ttu-id="e8010-150">PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="e8010-150">PublishingEditor</span></span>    
- <span data-ttu-id="e8010-151">Editor</span><span class="sxs-lookup"><span data-stu-id="e8010-151">Editor</span></span>    
- <span data-ttu-id="e8010-152">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="e8010-152">PublishingAuthor</span></span>    
- <span data-ttu-id="e8010-153">作者</span><span class="sxs-lookup"><span data-stu-id="e8010-153">Author</span></span>    
- <span data-ttu-id="e8010-154">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="e8010-154">NoneditingAuthor</span></span>    
- <span data-ttu-id="e8010-155">Reviewer</span><span class="sxs-lookup"><span data-stu-id="e8010-155">Reviewer</span></span>    
- <span data-ttu-id="e8010-156">参与者</span><span class="sxs-lookup"><span data-stu-id="e8010-156">Contributor</span></span>   
- <span data-ttu-id="e8010-157">自定义-无法由应用程序设置此值。</span><span class="sxs-lookup"><span data-stu-id="e8010-157">Custom - This value cannot be set by the application.</span></span> <span data-ttu-id="e8010-158">如果应用程序包括自定义集合的单个权限，则服务器将设置此值。</span><span class="sxs-lookup"><span data-stu-id="e8010-158">The server sets this value if the application includes a custom collection of individual permissions.</span></span>    
- <span data-ttu-id="e8010-159">FreeBusyTimeOnly-这可以仅在上设置日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-159">FreeBusyTimeOnly - This can only be set on Calendar folders.</span></span>   
- <span data-ttu-id="e8010-160">FreeBusyTimeAndSubjectAndLocation-这可以仅在上设置日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-160">FreeBusyTimeAndSubjectAndLocation - This can only be set on Calendar folders.</span></span>
    
<span data-ttu-id="e8010-161">下表显示的单个权限所应用的默认基于权限级别。</span><span class="sxs-lookup"><span data-stu-id="e8010-161">The following table shows which individual permissions are applied by default based on permission level.</span></span>
  
<span data-ttu-id="e8010-162">**表 2。由权限级别的单个权限**</span><span class="sxs-lookup"><span data-stu-id="e8010-162">**Table 2. Individual permissions by permission level**</span></span>

|<span data-ttu-id="e8010-163">权限级别</span><span class="sxs-lookup"><span data-stu-id="e8010-163">Permission level</span></span>|<span data-ttu-id="e8010-164">可以创建项目</span><span class="sxs-lookup"><span data-stu-id="e8010-164">Can create items</span></span>|<span data-ttu-id="e8010-165">可以创建子文件夹</span><span class="sxs-lookup"><span data-stu-id="e8010-165">Can create sub folders</span></span>|<span data-ttu-id="e8010-166">为文件夹所有者</span><span class="sxs-lookup"><span data-stu-id="e8010-166">Is folder owner</span></span>|<span data-ttu-id="e8010-167">是可见的文件夹</span><span class="sxs-lookup"><span data-stu-id="e8010-167">Is folder visible</span></span>|<span data-ttu-id="e8010-168">是文件夹联系人</span><span class="sxs-lookup"><span data-stu-id="e8010-168">Is folder contact</span></span>|<span data-ttu-id="e8010-169">编辑项目</span><span class="sxs-lookup"><span data-stu-id="e8010-169">Edit items</span></span>|<span data-ttu-id="e8010-170">删除项目</span><span class="sxs-lookup"><span data-stu-id="e8010-170">Delete items</span></span>|<span data-ttu-id="e8010-171">可以阅读项目</span><span class="sxs-lookup"><span data-stu-id="e8010-171">Can read items</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e8010-172">无</span><span class="sxs-lookup"><span data-stu-id="e8010-172">None</span></span>  <br/> |<span data-ttu-id="e8010-173">False</span><span class="sxs-lookup"><span data-stu-id="e8010-173">False</span></span>  <br/> |<span data-ttu-id="e8010-174">False</span><span class="sxs-lookup"><span data-stu-id="e8010-174">False</span></span>  <br/> |<span data-ttu-id="e8010-175">False</span><span class="sxs-lookup"><span data-stu-id="e8010-175">False</span></span>  <br/> |<span data-ttu-id="e8010-176">False</span><span class="sxs-lookup"><span data-stu-id="e8010-176">False</span></span>  <br/> |<span data-ttu-id="e8010-177">False</span><span class="sxs-lookup"><span data-stu-id="e8010-177">False</span></span>  <br/> |<span data-ttu-id="e8010-178">无</span><span class="sxs-lookup"><span data-stu-id="e8010-178">None</span></span>  <br/> |<span data-ttu-id="e8010-179">无</span><span class="sxs-lookup"><span data-stu-id="e8010-179">None</span></span>  <br/> |<span data-ttu-id="e8010-180">无</span><span class="sxs-lookup"><span data-stu-id="e8010-180">None</span></span>  <br/> |
|<span data-ttu-id="e8010-181">Owner</span><span class="sxs-lookup"><span data-stu-id="e8010-181">Owner</span></span>  <br/> |<span data-ttu-id="e8010-182">True</span><span class="sxs-lookup"><span data-stu-id="e8010-182">True</span></span>  <br/> |<span data-ttu-id="e8010-183">True</span><span class="sxs-lookup"><span data-stu-id="e8010-183">True</span></span>  <br/> |<span data-ttu-id="e8010-184">True</span><span class="sxs-lookup"><span data-stu-id="e8010-184">True</span></span>  <br/> |<span data-ttu-id="e8010-185">True</span><span class="sxs-lookup"><span data-stu-id="e8010-185">True</span></span>  <br/> |<span data-ttu-id="e8010-186">True</span><span class="sxs-lookup"><span data-stu-id="e8010-186">True</span></span>  <br/> |<span data-ttu-id="e8010-187">所有</span><span class="sxs-lookup"><span data-stu-id="e8010-187">All</span></span>  <br/> |<span data-ttu-id="e8010-188">所有</span><span class="sxs-lookup"><span data-stu-id="e8010-188">All</span></span>  <br/> |<span data-ttu-id="e8010-189">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e8010-189">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e8010-190">PublishingEditor</span><span class="sxs-lookup"><span data-stu-id="e8010-190">PublishingEditor</span></span>  <br/> |<span data-ttu-id="e8010-191">True</span><span class="sxs-lookup"><span data-stu-id="e8010-191">True</span></span>  <br/> |<span data-ttu-id="e8010-192">True</span><span class="sxs-lookup"><span data-stu-id="e8010-192">True</span></span>  <br/> |<span data-ttu-id="e8010-193">False</span><span class="sxs-lookup"><span data-stu-id="e8010-193">False</span></span>  <br/> |<span data-ttu-id="e8010-194">True</span><span class="sxs-lookup"><span data-stu-id="e8010-194">True</span></span>  <br/> |<span data-ttu-id="e8010-195">False</span><span class="sxs-lookup"><span data-stu-id="e8010-195">False</span></span>  <br/> |<span data-ttu-id="e8010-196">所有</span><span class="sxs-lookup"><span data-stu-id="e8010-196">All</span></span>  <br/> |<span data-ttu-id="e8010-197">所有</span><span class="sxs-lookup"><span data-stu-id="e8010-197">All</span></span>  <br/> |<span data-ttu-id="e8010-198">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e8010-198">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e8010-199">Editor</span><span class="sxs-lookup"><span data-stu-id="e8010-199">Editor</span></span>  <br/> |<span data-ttu-id="e8010-200">True</span><span class="sxs-lookup"><span data-stu-id="e8010-200">True</span></span>  <br/> |<span data-ttu-id="e8010-201">False</span><span class="sxs-lookup"><span data-stu-id="e8010-201">False</span></span>  <br/> |<span data-ttu-id="e8010-202">False</span><span class="sxs-lookup"><span data-stu-id="e8010-202">False</span></span>  <br/> |<span data-ttu-id="e8010-203">True</span><span class="sxs-lookup"><span data-stu-id="e8010-203">True</span></span>  <br/> |<span data-ttu-id="e8010-204">False</span><span class="sxs-lookup"><span data-stu-id="e8010-204">False</span></span>  <br/> |<span data-ttu-id="e8010-205">所有</span><span class="sxs-lookup"><span data-stu-id="e8010-205">All</span></span>  <br/> |<span data-ttu-id="e8010-206">所有</span><span class="sxs-lookup"><span data-stu-id="e8010-206">All</span></span>  <br/> |<span data-ttu-id="e8010-207">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e8010-207">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e8010-208">PublishingAuthor</span><span class="sxs-lookup"><span data-stu-id="e8010-208">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="e8010-209">True</span><span class="sxs-lookup"><span data-stu-id="e8010-209">True</span></span>  <br/> |<span data-ttu-id="e8010-210">True</span><span class="sxs-lookup"><span data-stu-id="e8010-210">True</span></span>  <br/> |<span data-ttu-id="e8010-211">False</span><span class="sxs-lookup"><span data-stu-id="e8010-211">False</span></span>  <br/> |<span data-ttu-id="e8010-212">True</span><span class="sxs-lookup"><span data-stu-id="e8010-212">True</span></span>  <br/> |<span data-ttu-id="e8010-213">False</span><span class="sxs-lookup"><span data-stu-id="e8010-213">False</span></span>  <br/> |<span data-ttu-id="e8010-214">拥有</span><span class="sxs-lookup"><span data-stu-id="e8010-214">Owned</span></span>  <br/> |<span data-ttu-id="e8010-215">拥有</span><span class="sxs-lookup"><span data-stu-id="e8010-215">Owned</span></span>  <br/> |<span data-ttu-id="e8010-216">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e8010-216">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e8010-217">作者</span><span class="sxs-lookup"><span data-stu-id="e8010-217">Author</span></span>  <br/> |<span data-ttu-id="e8010-218">True</span><span class="sxs-lookup"><span data-stu-id="e8010-218">True</span></span>  <br/> |<span data-ttu-id="e8010-219">False</span><span class="sxs-lookup"><span data-stu-id="e8010-219">False</span></span>  <br/> |<span data-ttu-id="e8010-220">False</span><span class="sxs-lookup"><span data-stu-id="e8010-220">False</span></span>  <br/> |<span data-ttu-id="e8010-221">True</span><span class="sxs-lookup"><span data-stu-id="e8010-221">True</span></span>  <br/> |<span data-ttu-id="e8010-222">False</span><span class="sxs-lookup"><span data-stu-id="e8010-222">False</span></span>  <br/> |<span data-ttu-id="e8010-223">拥有</span><span class="sxs-lookup"><span data-stu-id="e8010-223">Owned</span></span>  <br/> |<span data-ttu-id="e8010-224">拥有</span><span class="sxs-lookup"><span data-stu-id="e8010-224">Owned</span></span>  <br/> |<span data-ttu-id="e8010-225">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e8010-225">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e8010-226">NoneditingAuthor</span><span class="sxs-lookup"><span data-stu-id="e8010-226">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="e8010-227">True</span><span class="sxs-lookup"><span data-stu-id="e8010-227">True</span></span>  <br/> |<span data-ttu-id="e8010-228">False</span><span class="sxs-lookup"><span data-stu-id="e8010-228">False</span></span>  <br/> |<span data-ttu-id="e8010-229">False</span><span class="sxs-lookup"><span data-stu-id="e8010-229">False</span></span>  <br/> |<span data-ttu-id="e8010-230">True</span><span class="sxs-lookup"><span data-stu-id="e8010-230">True</span></span>  <br/> |<span data-ttu-id="e8010-231">False</span><span class="sxs-lookup"><span data-stu-id="e8010-231">False</span></span>  <br/> |<span data-ttu-id="e8010-232">无</span><span class="sxs-lookup"><span data-stu-id="e8010-232">None</span></span>  <br/> |<span data-ttu-id="e8010-233">拥有</span><span class="sxs-lookup"><span data-stu-id="e8010-233">Owned</span></span>  <br/> |<span data-ttu-id="e8010-234">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e8010-234">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e8010-235">Reviewer</span><span class="sxs-lookup"><span data-stu-id="e8010-235">Reviewer</span></span>  <br/> |<span data-ttu-id="e8010-236">False</span><span class="sxs-lookup"><span data-stu-id="e8010-236">False</span></span>  <br/> |<span data-ttu-id="e8010-237">False</span><span class="sxs-lookup"><span data-stu-id="e8010-237">False</span></span>  <br/> |<span data-ttu-id="e8010-238">False</span><span class="sxs-lookup"><span data-stu-id="e8010-238">False</span></span>  <br/> |<span data-ttu-id="e8010-239">True</span><span class="sxs-lookup"><span data-stu-id="e8010-239">True</span></span>  <br/> |<span data-ttu-id="e8010-240">False</span><span class="sxs-lookup"><span data-stu-id="e8010-240">False</span></span>  <br/> |<span data-ttu-id="e8010-241">无</span><span class="sxs-lookup"><span data-stu-id="e8010-241">None</span></span>  <br/> |<span data-ttu-id="e8010-242">无</span><span class="sxs-lookup"><span data-stu-id="e8010-242">None</span></span>  <br/> |<span data-ttu-id="e8010-243">FullDetails</span><span class="sxs-lookup"><span data-stu-id="e8010-243">FullDetails</span></span>  <br/> |
|<span data-ttu-id="e8010-244">参与者</span><span class="sxs-lookup"><span data-stu-id="e8010-244">Contributor</span></span>  <br/> |<span data-ttu-id="e8010-245">True</span><span class="sxs-lookup"><span data-stu-id="e8010-245">True</span></span>  <br/> |<span data-ttu-id="e8010-246">False</span><span class="sxs-lookup"><span data-stu-id="e8010-246">False</span></span>  <br/> |<span data-ttu-id="e8010-247">False</span><span class="sxs-lookup"><span data-stu-id="e8010-247">False</span></span>  <br/> |<span data-ttu-id="e8010-248">True</span><span class="sxs-lookup"><span data-stu-id="e8010-248">True</span></span>  <br/> |<span data-ttu-id="e8010-249">False</span><span class="sxs-lookup"><span data-stu-id="e8010-249">False</span></span>  <br/> |<span data-ttu-id="e8010-250">无</span><span class="sxs-lookup"><span data-stu-id="e8010-250">None</span></span>  <br/> |<span data-ttu-id="e8010-251">无</span><span class="sxs-lookup"><span data-stu-id="e8010-251">None</span></span>  <br/> |<span data-ttu-id="e8010-252">无</span><span class="sxs-lookup"><span data-stu-id="e8010-252">None</span></span>  <br/> |
   
<span data-ttu-id="e8010-253">如果文件夹级权限请求中指定非自定义权限级别，您无需指定单个权限设置。</span><span class="sxs-lookup"><span data-stu-id="e8010-253">If you specify a non-custom permission level in the folder-level permissions request, you don't need to specify the individual permission settings.</span></span> <span data-ttu-id="e8010-254">如果您指定单个权限设置的权限级别时，将在响应中返回**ErrorInvalidPermissionSettings**错误。</span><span class="sxs-lookup"><span data-stu-id="e8010-254">If you do specify an individual permission when you set a permission level, an **ErrorInvalidPermissionSettings** error will be returned in the response.</span></span> 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="e8010-255">使用 EWS 托管 API 中添加文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-255">Adding folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="e8010-256"><a name="bk_enableewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e8010-256"></span></span>

<span data-ttu-id="e8010-257">下面的代码示例演示如何使用 EWS 托管 API 为：</span><span class="sxs-lookup"><span data-stu-id="e8010-257">The following code example shows how to use the EWS Managed API to:</span></span> 
  
- <span data-ttu-id="e8010-258">创建新的[FolderPermission](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx)对象的新用户。</span><span class="sxs-lookup"><span data-stu-id="e8010-258">Create a new [FolderPermission](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) object for the new user.</span></span> 
    
- <span data-ttu-id="e8010-259">通过使用[Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法获取当前文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-259">Get the current permissions for a folder by using the [Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
    
- <span data-ttu-id="e8010-260">将新**FolderPermissions**添加到[Folder.Permissions](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="e8010-260">Add the new **FolderPermissions** to the [Folder.Permissions](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) property.</span></span> 
    
- <span data-ttu-id="e8010-261">调用[Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)方法以保存到服务器的新权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-261">Call the [Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the new permissions to the server.</span></span> 
    
<span data-ttu-id="e8010-262">此示例假定该**服务**的邮箱所有者是有效的[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="e8010-262">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void EnableFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.Permissions);
    // Specify the SMTP address of the new user and the folder permissions level.
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
    
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, WellKnownFolderName.SentItems, propSet);
 
    // Add the permissions for the new user to the Sent Items DACL.
    sentItemsFolder.Permissions.Add(fldperm);
    // This call results in a UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

<span data-ttu-id="e8010-263">下面的代码行指定的权限级别。</span><span class="sxs-lookup"><span data-stu-id="e8010-263">The following line of code specifies the permission level.</span></span>
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

<span data-ttu-id="e8010-264">如果您想要使用自定义权限级别，请改为使用此代码。</span><span class="sxs-lookup"><span data-stu-id="e8010-264">If you want to use the custom permission level, use this code instead.</span></span>
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

<span data-ttu-id="e8010-265">使用自定义权限级别创建**FolderPermission**对象时，可以设置任何或所有可写[FolderPermission 属性](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e8010-265">You can set any or all of the writable [FolderPermission properties](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) when you create a **FolderPermission** object with a custom permission level.</span></span> <span data-ttu-id="e8010-266">但请注意， [FolderPermissionLevel](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx)从不显式设置为**自定义**应用程序。</span><span class="sxs-lookup"><span data-stu-id="e8010-266">Note, however, that the [FolderPermissionLevel](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) is never explicitly set to **Custom** by the application.</span></span> <span data-ttu-id="e8010-267">**FolderPermissionLevel**设置为自定义中，仅当您创建**FolderPermission**对象并设置单个权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-267">The **FolderPermissionLevel** is set to Custom only when you create a **FolderPermission** object and set individual permissions.</span></span> 
  
## <a name="adding-folder-permissions-by-using-ews"></a><span data-ttu-id="e8010-268">使用 EWS 添加文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-268">Adding folder permissions by using EWS</span></span>
<span data-ttu-id="e8010-269"><a name="bk_enableews"> </a></span><span class="sxs-lookup"><span data-stu-id="e8010-269"></span></span>

<span data-ttu-id="e8010-270">下面的 EWS 代码示例演示如何通过检索当前权限，然后提交新的权限的列表添加到特定文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-270">The following EWS code examples show how to add permissions to a specific folder by retrieving the current permissions and then submitting a list of new permissions.</span></span>
  
<span data-ttu-id="e8010-271">第一步是发送[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)请求，其中[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)值指定要在其中添加权限 （在此示例中的已发送邮件文件夹） 的文件夹和[FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)值包含文件夹： PermissionSet。</span><span class="sxs-lookup"><span data-stu-id="e8010-271">The first step is to send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request, where the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to add permissions (the Sent Items folder in this example) and the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="e8010-272">此请求将检索指定的文件夹的权限设置。</span><span class="sxs-lookup"><span data-stu-id="e8010-272">This request will retrieve the permission settings for the folder specified.</span></span> 
  
<span data-ttu-id="e8010-273">这也是 EWS 托管 API 将调用**绑定**到[添加文件夹权限](#bk_enableewsma)方法时发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="e8010-273">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [add folder permissions](#bk_enableewsma).</span></span>
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:GetFolder>
        <m:FolderShape>
          <t:BaseShape>IdOnly</t:BaseShape>
          <t:AdditionalProperties>
            <t:FieldURI FieldURI="folder:PermissionSet" />
          </t:AdditionalProperties>
        </m:FolderShape>
        <m:FolderIds>
          <t:DistinguishedFolderId Id="sentitems" />
        </m:FolderIds>
      </m:GetFolder>
    </soap:Body>
  </soap:Envelope>
```

<span data-ttu-id="e8010-274">服务器响应包含**NoError**，这表明该文件夹已成功检索[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的[GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)消息的**GetFolder**请求。</span><span class="sxs-lookup"><span data-stu-id="e8010-274">The server responds to the **GetFolder** request with a [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="e8010-275">为便于阅读变短了[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)和[ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="e8010-275">The [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) and [ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) values have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="CgAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="e8010-276">接下来，使用**UpdateFolder**操作发送更新的[PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)，其中包括新的用户[权限](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e8010-276">Next, use the **UpdateFolder** operation to send the updated [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx), which includes the [Permission](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) for the new user.</span></span> <span data-ttu-id="e8010-277">请注意[UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)操作中包括各自的文件夹的[SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx)元素将覆盖所有文件夹的权限设置。</span><span class="sxs-lookup"><span data-stu-id="e8010-277">Note that including the [SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) element for the respective folder in the [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation will overwrite all the permission settings on the folder.</span></span> <span data-ttu-id="e8010-278">同样，包括**UpdateFolder**操作的[DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx)选项也将删除所有文件夹的权限设置。</span><span class="sxs-lookup"><span data-stu-id="e8010-278">Likewise, including the [DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) option of the **UpdateFolder** operation will also delete all the permission settings on the folder.</span></span> 
  
<span data-ttu-id="e8010-279">这也是在调用**Update**方法中添加[文件夹权限](#bk_enableewsma)时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="e8010-279">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [add folder permissions](#bk_enableewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="CgAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
                      </t:UserId>
                      <t:PermissionLevel>Editor</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e8010-280">下面的代码行指定的权限级别。</span><span class="sxs-lookup"><span data-stu-id="e8010-280">The following line of code specifies the permission level.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="e8010-281">如果您想要使用自定义权限级别，请改为使用此代码。</span><span class="sxs-lookup"><span data-stu-id="e8010-281">If you want to use the custom permission level, use this code instead.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress> sadie@contoso.com </t:PrimarySmtpAddress>
    </t:UserId>
    <t:CanCreateItems>true</t:CanCreateItems>
    <t:CanCreateSubFolders>true</t:CanCreateSubFolders>
    <t:IsFolderOwner>false</t:IsFolderOwner>
    <t:IsFolderVisible>false</t:IsFolderVisible>
    <t:IsFolderContact>false</t:IsFolderContact>
    <t:EditItems>None</t:EditItems>
    <t:DeleteItems>None</t:DeleteItems>
    <t:ReadItems>None</t:ReadItems>
    <t:PermissionLevel>Custom</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="e8010-282">服务器响应**UpdateFolder**请求使用[UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)消息，其中包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，这表明已成功更新文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-282">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully.</span></span>
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="e8010-283">使用 EWS 托管 API 删除文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-283">Removing folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="e8010-284"><a name="bk_removeewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e8010-284"></span></span>

<span data-ttu-id="e8010-285">下面的代码示例演示如何使用 EWS 托管 API 删除特定的文件夹，除了默认选中并且是匿名的权限，对所有用户权限：</span><span class="sxs-lookup"><span data-stu-id="e8010-285">The following code example shows how to use the EWS Managed API to remove all user permissions on a specific folder, except for the default and anonymous permissions, by:</span></span>
  
1. <span data-ttu-id="e8010-286">使用**Bind**方法获取当前文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-286">Getting the current permissions for a folder by using the **Bind** method.</span></span> 
    
2. <span data-ttu-id="e8010-287">循环访问**权限**集合并删除单个用户的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-287">Iterating through the **Permissions** collection and removing permissions for individual users.</span></span> 
    
3. <span data-ttu-id="e8010-288">在调用**Update**方法保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="e8010-288">Calling the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="e8010-289">此示例删除所有用户权限的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-289">This example removes all user permissions on a folder.</span></span> <span data-ttu-id="e8010-290">如果您想要修改此示例删除仅为某个特定用户的权限，更改以下代码来标识显示名称的行或 SMTP 地址的用户。</span><span class="sxs-lookup"><span data-stu-id="e8010-290">If you want to modify this example to remove permissions only for a specific user, change the following line of code to identify either the display name or SMTP address of the user.</span></span>
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

<span data-ttu-id="e8010-291">此示例假定该**服务**的邮箱所有者是有效的[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="e8010-291">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void RemoveFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.FirstClassProperties, FolderSchema.Permissions);
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, new FolderId(WellKnownFolderName.SentItems, "primary@contoso.com"), propSet);
    // Iterate through the collection of permissions and remove permissions for any 
    // user with a display name or SMTP address. This leaves the anonymous and 
    // default user permissions unchanged. 
    if (sentItemsFolder.Permissions.Count != 0)
    {
        for (int t = 0; t < sentItemsFolder.Permissions.Count; t++)
        {
            // Find any permissions associated with the specified user and remove them from the DACL
            if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
            {
                sentItemsFolder.Permissions.Remove(sentItemsFolder.Permissions[t]);
            }
        }
    }
    // This call results in an UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

## <a name="removing-folder-permissions-by-using-ews"></a><span data-ttu-id="e8010-292">使用 EWS 删除文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-292">Removing folder permissions by using EWS</span></span>
<span data-ttu-id="e8010-293"><a name="bk_removeews"> </a></span><span class="sxs-lookup"><span data-stu-id="e8010-293"></span></span>

<span data-ttu-id="e8010-294">下面的 EWS 代码示例演示如何删除所有的特定的文件夹，除了默认选中并且是匿名权限的用户权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-294">The following EWS code examples show how to remove all user permissions on a specific folder, except for the default and anonymous permissions.</span></span>
  
<span data-ttu-id="e8010-295">首先，将其中[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)值指定要删除的权限 （在此示例中的已发送邮件文件夹） 的文件夹和[FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)值包含文件夹： PermissionSet [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)请求发送。</span><span class="sxs-lookup"><span data-stu-id="e8010-295">First, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request where the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to remove permissions (the Sent Items folder in this example) and the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="e8010-296">此请求将检索[PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)为指定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="e8010-296">This request will retrieve the [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) for the folder specified.</span></span> 
  
<span data-ttu-id="e8010-297">这也是 EWS 托管 API 将调用**绑定**到[删除文件夹权限](#bk_removeewsma)方法时发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="e8010-297">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:PermissionSet" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e8010-298">服务器响应包含**NoError**，这表明该文件夹已成功检索[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的[GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)消息的**GetFolder**请求。</span><span class="sxs-lookup"><span data-stu-id="e8010-298">The server responds to the **GetFolder** request with a [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="e8010-299">为便于阅读变短了**文件夹 Id**和**ParentFolderId**元素的值。</span><span class="sxs-lookup"><span data-stu-id="e8010-299">The values of the **FolderId** and **ParentFolderId** elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="EAAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
              <t:ParentFolderId Id="CQAAAA=="
                                ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>Drafts</t:DisplayName>
              <t:TotalCount>0</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:EffectiveRights>
                <t:CreateAssociated>true</t:CreateAssociated>
                <t:CreateContents>true</t:CreateContents>
                <t:CreateHierarchy>true</t:CreateHierarchy>
                <t:Delete>true</t:Delete>
                <t:Modify>true</t:Modify>
                <t:Read>true</t:Read>
                <t:ViewPrivateItems>true</t:ViewPrivateItems>
              </t:EffectiveRights>
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
                      <t:PrimarySmtpAddress>sadie@Contoso.com</t:PrimarySmtpAddress>
                      <t:DisplayName>Sadie Daniels</t:DisplayName>
                    </t:UserId>
                    <t:CanCreateItems>true</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>true</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>All</t:EditItems>
                    <t:DeleteItems>All</t:DeleteItems>
                    <t:ReadItems>FullDetails</t:ReadItems>
                    <t:PermissionLevel>Editor</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
              <t:UnreadCount>0</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="e8010-300">接下来，使用**UpdateFolder**操作发送更新的**PermissionSet**，其中不包含对已删除的用户的**权限**。</span><span class="sxs-lookup"><span data-stu-id="e8010-300">Next, use the **UpdateFolder** operation to send the updated **PermissionSet**, which does not include the **Permission** for the removed user.</span></span> 
  
<span data-ttu-id="e8010-301">这也是在调用**Update**方法删除[文件夹权限](#bk_removeewsma)时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="e8010-301">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="EAAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="e8010-302">服务器响应**UpdateFolder**请求使用**UpdateFolderResponse**消息，其中包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，这表明已成功更新。</span><span class="sxs-lookup"><span data-stu-id="e8010-302">The server responds to the **UpdateFolder** request with an **UpdateFolderResponse** message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the update was successful.</span></span>
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="e8010-303">使用 EWS 托管 API 更新文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-303">Updating folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="e8010-304"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="e8010-304"></span></span>

<span data-ttu-id="e8010-305">您还可以通过使用 EWS 托管 API 更新文件夹特定文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-305">You can also update folder permissions for a specific folder by using the EWS Managed API.</span></span> <span data-ttu-id="e8010-306">若要更新的权限：</span><span class="sxs-lookup"><span data-stu-id="e8010-306">To update the permissions:</span></span> 
  
1. <span data-ttu-id="e8010-307">[删除文件夹权限](#bk_removeewsma)的过时的权限，但不是调用**Update**方法 （尚未）。</span><span class="sxs-lookup"><span data-stu-id="e8010-307">[Remove the folder permissions](#bk_removeewsma) for the outdated permissions, but do not call the **Update** method (yet).</span></span> 
    
2. <span data-ttu-id="e8010-308">[添加新的或更改用户的文件夹权限](#bk_enableewsma)。</span><span class="sxs-lookup"><span data-stu-id="e8010-308">[Add folder permissions for the new or changed users](#bk_enableewsma).</span></span>
    
3. <span data-ttu-id="e8010-309">调用**Update**方法以保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="e8010-309">Call the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="e8010-310">如果您尝试添加两个相同的用户的权限集，您将收到带有以下描述**ServiceResponseException**错误:"指定的权限集包含重复 UserIds"。</span><span class="sxs-lookup"><span data-stu-id="e8010-310">If you try to add two sets of permissions for the same user, you will receive a **ServiceResponseException** error with the following description: "The specified permission set contains duplicate UserIds".</span></span> <span data-ttu-id="e8010-311">在这种情况下，从**Permission**集合中，删除当前的权限，然后**Permission**集合中添加新的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-311">In that case, remove the current permissions from the **Permission** collection, then add the new permissions to the **Permission** collection.</span></span> 
  
## <a name="updating-folder-permissions-by-using-ews"></a><span data-ttu-id="e8010-312">使用 EWS 更新文件夹权限</span><span class="sxs-lookup"><span data-stu-id="e8010-312">Updating folder permissions by using EWS</span></span>
<span data-ttu-id="e8010-313"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="e8010-313"></span></span>

<span data-ttu-id="e8010-314">您可以使用 EWS 通过组合的删除和添加过程来更新文件夹为特定的文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-314">You can also update folder permissions for specific folders by using EWS by combining the removal and addition process.</span></span> <span data-ttu-id="e8010-315">若要更新的权限：</span><span class="sxs-lookup"><span data-stu-id="e8010-315">To update the permissions:</span></span> 
  
1. <span data-ttu-id="e8010-316">通过使用**GetFolder**操作来检索文件夹的当前权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-316">Retrieve the folder's current permissions by using the **GetFolder** operation.</span></span> 
    
2. <span data-ttu-id="e8010-317">通过使用**UpdateFolder**操作发送更新的列表的权限。</span><span class="sxs-lookup"><span data-stu-id="e8010-317">Send an updated list of permissions by using the **UpdateFolder** operation.</span></span> 
    
<span data-ttu-id="e8010-318">这些是相同的两个操作通过 EWS 使用到[启用](#bk_enableews)或[删除的访问](#bk_removeews)。</span><span class="sxs-lookup"><span data-stu-id="e8010-318">These are the same two operations you use to [enable](#bk_enableews) or [remove access](#bk_removeews) by using EWS.</span></span> <span data-ttu-id="e8010-319">唯一的区别是当您收到**GetFolder**响应，它将包含一个为用户设置的**权限**。</span><span class="sxs-lookup"><span data-stu-id="e8010-319">The only difference is that when you receive the **GetFolder** response, it will contain a **Permission** set for user.</span></span> <span data-ttu-id="e8010-320">只需将该现有**权限**元素替换为新的**权限**元素，然后再发送的新**权限**值或值的**UpdateFolder**操作。</span><span class="sxs-lookup"><span data-stu-id="e8010-320">Simply replace that existing **Permission** element with the new **Permission** element, and then send the **UpdateFolder** operation with the new **Permission** value or values.</span></span> 
  
<span data-ttu-id="e8010-321">如果您尝试添加两个相同的用户的权限集，您将收到**ErrorDuplicateUserIdsSpecified** **ResponseCode**值。</span><span class="sxs-lookup"><span data-stu-id="e8010-321">If you try to add two sets of permissions for the same user, you will receive a **ResponseCode** value of **ErrorDuplicateUserIdsSpecified**.</span></span> <span data-ttu-id="e8010-322">在这种情况下，请求中删除过时的用户权限值，然后重试该请求。</span><span class="sxs-lookup"><span data-stu-id="e8010-322">In that case, remove the outdated Permission value for the user from the request and then retry the request.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e8010-323">后续步骤</span><span class="sxs-lookup"><span data-stu-id="e8010-323">Next steps</span></span>

<span data-ttu-id="e8010-324">授予用户对特定文件夹的权限后，用户可以访问文件夹作为代理人。</span><span class="sxs-lookup"><span data-stu-id="e8010-324">After you give a user permission to a specific folder, the user can access the folder as a delegate.</span></span> <span data-ttu-id="e8010-325">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="e8010-325">For more information, see:</span></span>
  
- [<span data-ttu-id="e8010-326">作为 Exchange 中使用 EWS 代理人的访问电子邮件</span><span class="sxs-lookup"><span data-stu-id="e8010-326">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="e8010-327">在 Exchange 中使用 EWS 作为代理人访问日历</span><span class="sxs-lookup"><span data-stu-id="e8010-327">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="e8010-328">作为代理人在 Exchange 使用 EWS 访问联系人</span><span class="sxs-lookup"><span data-stu-id="e8010-328">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="e8010-329">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8010-329">See also</span></span>

- [<span data-ttu-id="e8010-330">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="e8010-330">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="e8010-331">添加和删除代理人，在 Exchange 使用 EWS</span><span class="sxs-lookup"><span data-stu-id="e8010-331">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="e8010-332">文件夹和交换中的 EWS 中的项目</span><span class="sxs-lookup"><span data-stu-id="e8010-332">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    

