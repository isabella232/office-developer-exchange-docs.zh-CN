---
title: 使用 Exchange 中的 EWS 为另一个用户设置文件夹权限
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来设置文件夹的权限级别。
ms.openlocfilehash: e25f1a49a430e8c95829d404fa53451b76cab167
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455868"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a><span data-ttu-id="ae137-103">使用 Exchange 中的 EWS 为另一个用户设置文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-103">Set folder permissions for another user by using EWS in Exchange</span></span>

<span data-ttu-id="ae137-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来设置文件夹的权限级别。</span><span class="sxs-lookup"><span data-stu-id="ae137-104">Learn how to set permission levels on a folder by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="ae137-105">通过文件夹级权限，用户可以访问其他用户的邮箱中的一个或多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="ae137-105">Folder-level permissions enable users to access one or more folders in another user's mailbox.</span></span> <span data-ttu-id="ae137-106">文件夹权限类似于代理访问，但它们的区别在于以下几种：</span><span class="sxs-lookup"><span data-stu-id="ae137-106">Folder permissions are similar to delegate access, but they differ in the following ways:</span></span> 
  
- <span data-ttu-id="ae137-107">文件夹权限不允许用户 "代表发送" 或 "代理发送" 其他用户。</span><span class="sxs-lookup"><span data-stu-id="ae137-107">Folder permissions do not enable a user to "send on behalf of" or "send as" another user.</span></span> <span data-ttu-id="ae137-108">他们只启用对文件夹的访问。</span><span class="sxs-lookup"><span data-stu-id="ae137-108">They only enable access to folders.</span></span> <span data-ttu-id="ae137-109">用户可以在这些文件夹中创建项目，但不能发送它们。</span><span class="sxs-lookup"><span data-stu-id="ae137-109">Users can create items in those folders, but they can't send them.</span></span>
    
- <span data-ttu-id="ae137-110">可以在邮箱中的任何文件夹上设置文件夹权限，但只能将代理添加到 "日历"、"联系人"、"收件箱"、"日记"、"便笺" 和 "任务" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="ae137-110">You can set folder permissions on any folder in the mailbox, but you can only add a delegate to the Calendar, Contacts, Inbox, Journal, Notes, and Tasks folders.</span></span>
    
- <span data-ttu-id="ae137-111">您可以设置[特定文件夹](#bk_folderperms)的多个权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-111">You can set a number of [permissions on a specific folder](#bk_folderperms).</span></span> <span data-ttu-id="ae137-112">在添加委派时，可以仅分配[五个权限级别](delegate-access-and-ews-in-exchange.md#bk_delegateperms)之一。</span><span class="sxs-lookup"><span data-stu-id="ae137-112">When you add a delegate, you can assign one of only [five permission levels](delegate-access-and-ews-in-exchange.md#bk_delegateperms).</span></span>
    
- <span data-ttu-id="ae137-113">您可以为匿名用户和默认用户设置文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-113">You can set folder permissions for anonymous and default users.</span></span> <span data-ttu-id="ae137-114">您只能将代理访问权限授予已启用邮件的帐户。</span><span class="sxs-lookup"><span data-stu-id="ae137-114">You can only grant delegate access to a mail-enabled account.</span></span>
    
<span data-ttu-id="ae137-115">如果您熟悉访问控制条目（Ace）和随机访问控制列表（Dacl），您就会知道用户每个文件夹只能有一组权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-115">If you're familiar with Access Control Entries (ACEs) and Discretionary Access Control Lists (DACLs), you know that a user can only have one set of permissions for each folder.</span></span> <span data-ttu-id="ae137-116">如果您尝试为用户添加一组权限，并且这些权限已经具有一组权限，则会出现错误。</span><span class="sxs-lookup"><span data-stu-id="ae137-116">If you try to add a set of permissions for a user and they already have a set of permissions, you'll get an error.</span></span> <span data-ttu-id="ae137-117">在对文件夹添加、删除或更新权限时，您将获得当前的 DACL，添加或删除任何 Ace，然后发送更新的 DACL。</span><span class="sxs-lookup"><span data-stu-id="ae137-117">When you add, remove, or update permissions on a folder, you get the current DACL, add or remove any ACEs, and then send the updated DACL.</span></span> <span data-ttu-id="ae137-118">您不能为同一个用户添加多个 Ace。</span><span class="sxs-lookup"><span data-stu-id="ae137-118">You cannot add multiple ACEs for the same user.</span></span> <span data-ttu-id="ae137-119">当您使用 EWS 托管 API 更新权限时，您需要删除用户的当前 ACE，然后将其新的 ACE 添加到集合中。</span><span class="sxs-lookup"><span data-stu-id="ae137-119">When you update permissions by using the EWS Managed API, you need to remove the user's current ACE and then add their new ACE to the collection.</span></span> <span data-ttu-id="ae137-120">如果使用的是 EWS，只需使用新的 Ace 替换之前的 Ace 集。</span><span class="sxs-lookup"><span data-stu-id="ae137-120">If you're using EWS, you just replace the previous set of ACEs with the new ones.</span></span>
  
<span data-ttu-id="ae137-121">如果对单个文件夹进行了多个权限更改，则可以批量添加、删除或更新，只需注意您不能在多个文件夹上对用户更新进行批处理。</span><span class="sxs-lookup"><span data-stu-id="ae137-121">If you're making multiple permission changes to a single folder, you can batch additions, removals, or updates —just note that you cannot batch user updates on multiple folders.</span></span> <span data-ttu-id="ae137-122">若要获取对单个文件夹的权限，需要执行一次调用，以更新该文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-122">One call is required to get the permissions on a single folder, and a second call is required to update the permissions on that folder.</span></span> <span data-ttu-id="ae137-123">在添加、删除或更新用户权限时，对每个任务使用相同的两个方法调用或操作。</span><span class="sxs-lookup"><span data-stu-id="ae137-123">When you add, remove, or update user permissions, you use the same two method calls or operations for each task.</span></span>
  
<span data-ttu-id="ae137-124">**表1。用于设置文件夹权限的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="ae137-124">**Table 1. EWS Managed API methods and EWS operations for setting folder permissions**</span></span>

|<span data-ttu-id="ae137-125">如果您想要 .。。</span><span class="sxs-lookup"><span data-stu-id="ae137-125">If you want to…</span></span>|<span data-ttu-id="ae137-126">使用此 EWS 托管 API 方法 .。。</span><span class="sxs-lookup"><span data-stu-id="ae137-126">Use this EWS Managed API method…</span></span>|<span data-ttu-id="ae137-127">使用此 EWS 操作 .。。</span><span class="sxs-lookup"><span data-stu-id="ae137-127">Use this EWS operation…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ae137-128">启用、删除或更新文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-128">Enable, remove, or update folder permissions</span></span>  <br/> |<span data-ttu-id="ae137-129">先[绑定文件夹](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) [. 更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae137-129">[Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) followed by [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx)</span></span> <br/> |<span data-ttu-id="ae137-130">[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)后接[UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ae137-130">[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) followed by [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)</span></span> <br/> |
|<span data-ttu-id="ae137-131">创建文件夹并定义文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-131">Create a folder and define folder permissions</span></span>  <br/> |[<span data-ttu-id="ae137-132">文件夹。保存</span><span class="sxs-lookup"><span data-stu-id="ae137-132">Folder.Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="ae137-133">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="ae137-133">CreateFolder</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a><span data-ttu-id="ae137-134">文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-134">Folder permissions</span></span>
<span data-ttu-id="ae137-135"><a name="bk_folderperms"> </a></span><span class="sxs-lookup"><span data-stu-id="ae137-135"><a name="bk_folderperms"> </a></span></span>

<span data-ttu-id="ae137-136">在对特定文件夹设置文件夹权限时，有很多选项。</span><span class="sxs-lookup"><span data-stu-id="ae137-136">You have quite a few options when it comes to setting folder permissions on a specific folder.</span></span> <span data-ttu-id="ae137-137">您可以为每个用户设置一个文件夹上的权限级别，这将为 DACL 添加一组预定义的单个权限，也可以对文件夹设置单个权限，但不能混合和匹配。</span><span class="sxs-lookup"><span data-stu-id="ae137-137">You can set a permission level on a folder for each user, which adds a set of predefined individual permissions to the DACL, or you can set individual permissions on a folder — but you can't mix and match.</span></span>
  
<span data-ttu-id="ae137-138">以下各个权限可用：</span><span class="sxs-lookup"><span data-stu-id="ae137-138">The following individual permissions are available:</span></span>
  
- <span data-ttu-id="ae137-139">可以创建</span><span class="sxs-lookup"><span data-stu-id="ae137-139">Can create</span></span>
- <span data-ttu-id="ae137-140">可以创建子文件夹</span><span class="sxs-lookup"><span data-stu-id="ae137-140">Can create subfolders</span></span>    
- <span data-ttu-id="ae137-141">是文件夹所有者</span><span class="sxs-lookup"><span data-stu-id="ae137-141">Is folder owner</span></span>    
- <span data-ttu-id="ae137-142">文件夹是否可见</span><span class="sxs-lookup"><span data-stu-id="ae137-142">Is folder visible</span></span>    
- <span data-ttu-id="ae137-143">是文件夹联系人</span><span class="sxs-lookup"><span data-stu-id="ae137-143">Is folder contact</span></span>    
- <span data-ttu-id="ae137-144">编辑项目</span><span class="sxs-lookup"><span data-stu-id="ae137-144">Edit items</span></span>    
- <span data-ttu-id="ae137-145">删除项目</span><span class="sxs-lookup"><span data-stu-id="ae137-145">Delete items</span></span>    
- <span data-ttu-id="ae137-146">读取项目</span><span class="sxs-lookup"><span data-stu-id="ae137-146">Read items</span></span>
    
<span data-ttu-id="ae137-147">此外，还提供了以下权限级别，其中定义了各个权限和值的子集，如表2中所示：</span><span class="sxs-lookup"><span data-stu-id="ae137-147">In addition, the following permission levels are available, which define a subset of individual permissions and values, as shown in Table 2:</span></span>
  
- <span data-ttu-id="ae137-148">无</span><span class="sxs-lookup"><span data-stu-id="ae137-148">None</span></span>    
- <span data-ttu-id="ae137-149">所有者</span><span class="sxs-lookup"><span data-stu-id="ae137-149">Owner</span></span>    
- <span data-ttu-id="ae137-150">Publishingeditorcreateitems</span><span class="sxs-lookup"><span data-stu-id="ae137-150">PublishingEditor</span></span>    
- <span data-ttu-id="ae137-151">编辑器</span><span class="sxs-lookup"><span data-stu-id="ae137-151">Editor</span></span>    
- <span data-ttu-id="ae137-152">Publishingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="ae137-152">PublishingAuthor</span></span>    
- <span data-ttu-id="ae137-153">作者</span><span class="sxs-lookup"><span data-stu-id="ae137-153">Author</span></span>    
- <span data-ttu-id="ae137-154">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="ae137-154">NoneditingAuthor</span></span>    
- <span data-ttu-id="ae137-155">Reviewer</span><span class="sxs-lookup"><span data-stu-id="ae137-155">Reviewer</span></span>    
- <span data-ttu-id="ae137-156">参与者</span><span class="sxs-lookup"><span data-stu-id="ae137-156">Contributor</span></span>   
- <span data-ttu-id="ae137-157">Custom-应用程序不能设置此值。</span><span class="sxs-lookup"><span data-stu-id="ae137-157">Custom - This value cannot be set by the application.</span></span> <span data-ttu-id="ae137-158">如果应用程序包含单个权限的自定义集合，则服务器将设置此值。</span><span class="sxs-lookup"><span data-stu-id="ae137-158">The server sets this value if the application includes a custom collection of individual permissions.</span></span>    
- <span data-ttu-id="ae137-159">FreeBusyTimeOnly-只能在日历文件夹上设置此设置。</span><span class="sxs-lookup"><span data-stu-id="ae137-159">FreeBusyTimeOnly - This can only be set on Calendar folders.</span></span>   
- <span data-ttu-id="ae137-160">FreeBusyTimeAndSubjectAndLocation-只能在日历文件夹上设置此设置。</span><span class="sxs-lookup"><span data-stu-id="ae137-160">FreeBusyTimeAndSubjectAndLocation - This can only be set on Calendar folders.</span></span>
    
<span data-ttu-id="ae137-161">下表显示了默认情况下基于权限级别应用的各个权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-161">The following table shows which individual permissions are applied by default based on permission level.</span></span>
  
<span data-ttu-id="ae137-162">**表2。按权限级别的各个权限**</span><span class="sxs-lookup"><span data-stu-id="ae137-162">**Table 2. Individual permissions by permission level**</span></span>

|<span data-ttu-id="ae137-163">权限级别</span><span class="sxs-lookup"><span data-stu-id="ae137-163">Permission level</span></span>|<span data-ttu-id="ae137-164">可以创建项目</span><span class="sxs-lookup"><span data-stu-id="ae137-164">Can create items</span></span>|<span data-ttu-id="ae137-165">可以创建子文件夹</span><span class="sxs-lookup"><span data-stu-id="ae137-165">Can create sub folders</span></span>|<span data-ttu-id="ae137-166">是文件夹所有者</span><span class="sxs-lookup"><span data-stu-id="ae137-166">Is folder owner</span></span>|<span data-ttu-id="ae137-167">文件夹是否可见</span><span class="sxs-lookup"><span data-stu-id="ae137-167">Is folder visible</span></span>|<span data-ttu-id="ae137-168">是文件夹联系人</span><span class="sxs-lookup"><span data-stu-id="ae137-168">Is folder contact</span></span>|<span data-ttu-id="ae137-169">编辑项目</span><span class="sxs-lookup"><span data-stu-id="ae137-169">Edit items</span></span>|<span data-ttu-id="ae137-170">删除项目</span><span class="sxs-lookup"><span data-stu-id="ae137-170">Delete items</span></span>|<span data-ttu-id="ae137-171">可以读取项目</span><span class="sxs-lookup"><span data-stu-id="ae137-171">Can read items</span></span>|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ae137-172">无</span><span class="sxs-lookup"><span data-stu-id="ae137-172">None</span></span>  <br/> |<span data-ttu-id="ae137-173">False</span><span class="sxs-lookup"><span data-stu-id="ae137-173">False</span></span>  <br/> |<span data-ttu-id="ae137-174">False</span><span class="sxs-lookup"><span data-stu-id="ae137-174">False</span></span>  <br/> |<span data-ttu-id="ae137-175">False</span><span class="sxs-lookup"><span data-stu-id="ae137-175">False</span></span>  <br/> |<span data-ttu-id="ae137-176">False</span><span class="sxs-lookup"><span data-stu-id="ae137-176">False</span></span>  <br/> |<span data-ttu-id="ae137-177">False</span><span class="sxs-lookup"><span data-stu-id="ae137-177">False</span></span>  <br/> |<span data-ttu-id="ae137-178">无</span><span class="sxs-lookup"><span data-stu-id="ae137-178">None</span></span>  <br/> |<span data-ttu-id="ae137-179">无</span><span class="sxs-lookup"><span data-stu-id="ae137-179">None</span></span>  <br/> |<span data-ttu-id="ae137-180">无</span><span class="sxs-lookup"><span data-stu-id="ae137-180">None</span></span>  <br/> |
|<span data-ttu-id="ae137-181">所有者</span><span class="sxs-lookup"><span data-stu-id="ae137-181">Owner</span></span>  <br/> |<span data-ttu-id="ae137-182">True</span><span class="sxs-lookup"><span data-stu-id="ae137-182">True</span></span>  <br/> |<span data-ttu-id="ae137-183">True</span><span class="sxs-lookup"><span data-stu-id="ae137-183">True</span></span>  <br/> |<span data-ttu-id="ae137-184">True</span><span class="sxs-lookup"><span data-stu-id="ae137-184">True</span></span>  <br/> |<span data-ttu-id="ae137-185">True</span><span class="sxs-lookup"><span data-stu-id="ae137-185">True</span></span>  <br/> |<span data-ttu-id="ae137-186">True</span><span class="sxs-lookup"><span data-stu-id="ae137-186">True</span></span>  <br/> |<span data-ttu-id="ae137-187">所有</span><span class="sxs-lookup"><span data-stu-id="ae137-187">All</span></span>  <br/> |<span data-ttu-id="ae137-188">所有</span><span class="sxs-lookup"><span data-stu-id="ae137-188">All</span></span>  <br/> |<span data-ttu-id="ae137-189">FullDetails</span><span class="sxs-lookup"><span data-stu-id="ae137-189">FullDetails</span></span>  <br/> |
|<span data-ttu-id="ae137-190">Publishingeditorcreateitems</span><span class="sxs-lookup"><span data-stu-id="ae137-190">PublishingEditor</span></span>  <br/> |<span data-ttu-id="ae137-191">True</span><span class="sxs-lookup"><span data-stu-id="ae137-191">True</span></span>  <br/> |<span data-ttu-id="ae137-192">True</span><span class="sxs-lookup"><span data-stu-id="ae137-192">True</span></span>  <br/> |<span data-ttu-id="ae137-193">False</span><span class="sxs-lookup"><span data-stu-id="ae137-193">False</span></span>  <br/> |<span data-ttu-id="ae137-194">True</span><span class="sxs-lookup"><span data-stu-id="ae137-194">True</span></span>  <br/> |<span data-ttu-id="ae137-195">False</span><span class="sxs-lookup"><span data-stu-id="ae137-195">False</span></span>  <br/> |<span data-ttu-id="ae137-196">所有</span><span class="sxs-lookup"><span data-stu-id="ae137-196">All</span></span>  <br/> |<span data-ttu-id="ae137-197">所有</span><span class="sxs-lookup"><span data-stu-id="ae137-197">All</span></span>  <br/> |<span data-ttu-id="ae137-198">FullDetails</span><span class="sxs-lookup"><span data-stu-id="ae137-198">FullDetails</span></span>  <br/> |
|<span data-ttu-id="ae137-199">编辑器</span><span class="sxs-lookup"><span data-stu-id="ae137-199">Editor</span></span>  <br/> |<span data-ttu-id="ae137-200">True</span><span class="sxs-lookup"><span data-stu-id="ae137-200">True</span></span>  <br/> |<span data-ttu-id="ae137-201">False</span><span class="sxs-lookup"><span data-stu-id="ae137-201">False</span></span>  <br/> |<span data-ttu-id="ae137-202">False</span><span class="sxs-lookup"><span data-stu-id="ae137-202">False</span></span>  <br/> |<span data-ttu-id="ae137-203">True</span><span class="sxs-lookup"><span data-stu-id="ae137-203">True</span></span>  <br/> |<span data-ttu-id="ae137-204">False</span><span class="sxs-lookup"><span data-stu-id="ae137-204">False</span></span>  <br/> |<span data-ttu-id="ae137-205">所有</span><span class="sxs-lookup"><span data-stu-id="ae137-205">All</span></span>  <br/> |<span data-ttu-id="ae137-206">所有</span><span class="sxs-lookup"><span data-stu-id="ae137-206">All</span></span>  <br/> |<span data-ttu-id="ae137-207">FullDetails</span><span class="sxs-lookup"><span data-stu-id="ae137-207">FullDetails</span></span>  <br/> |
|<span data-ttu-id="ae137-208">Publishingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="ae137-208">PublishingAuthor</span></span>  <br/> |<span data-ttu-id="ae137-209">True</span><span class="sxs-lookup"><span data-stu-id="ae137-209">True</span></span>  <br/> |<span data-ttu-id="ae137-210">True</span><span class="sxs-lookup"><span data-stu-id="ae137-210">True</span></span>  <br/> |<span data-ttu-id="ae137-211">False</span><span class="sxs-lookup"><span data-stu-id="ae137-211">False</span></span>  <br/> |<span data-ttu-id="ae137-212">True</span><span class="sxs-lookup"><span data-stu-id="ae137-212">True</span></span>  <br/> |<span data-ttu-id="ae137-213">False</span><span class="sxs-lookup"><span data-stu-id="ae137-213">False</span></span>  <br/> |<span data-ttu-id="ae137-214">所有权</span><span class="sxs-lookup"><span data-stu-id="ae137-214">Owned</span></span>  <br/> |<span data-ttu-id="ae137-215">所有权</span><span class="sxs-lookup"><span data-stu-id="ae137-215">Owned</span></span>  <br/> |<span data-ttu-id="ae137-216">FullDetails</span><span class="sxs-lookup"><span data-stu-id="ae137-216">FullDetails</span></span>  <br/> |
|<span data-ttu-id="ae137-217">作者</span><span class="sxs-lookup"><span data-stu-id="ae137-217">Author</span></span>  <br/> |<span data-ttu-id="ae137-218">True</span><span class="sxs-lookup"><span data-stu-id="ae137-218">True</span></span>  <br/> |<span data-ttu-id="ae137-219">False</span><span class="sxs-lookup"><span data-stu-id="ae137-219">False</span></span>  <br/> |<span data-ttu-id="ae137-220">False</span><span class="sxs-lookup"><span data-stu-id="ae137-220">False</span></span>  <br/> |<span data-ttu-id="ae137-221">True</span><span class="sxs-lookup"><span data-stu-id="ae137-221">True</span></span>  <br/> |<span data-ttu-id="ae137-222">False</span><span class="sxs-lookup"><span data-stu-id="ae137-222">False</span></span>  <br/> |<span data-ttu-id="ae137-223">所有权</span><span class="sxs-lookup"><span data-stu-id="ae137-223">Owned</span></span>  <br/> |<span data-ttu-id="ae137-224">所有权</span><span class="sxs-lookup"><span data-stu-id="ae137-224">Owned</span></span>  <br/> |<span data-ttu-id="ae137-225">FullDetails</span><span class="sxs-lookup"><span data-stu-id="ae137-225">FullDetails</span></span>  <br/> |
|<span data-ttu-id="ae137-226">Noneditingauthorcreateitems</span><span class="sxs-lookup"><span data-stu-id="ae137-226">NoneditingAuthor</span></span>  <br/> |<span data-ttu-id="ae137-227">True</span><span class="sxs-lookup"><span data-stu-id="ae137-227">True</span></span>  <br/> |<span data-ttu-id="ae137-228">False</span><span class="sxs-lookup"><span data-stu-id="ae137-228">False</span></span>  <br/> |<span data-ttu-id="ae137-229">False</span><span class="sxs-lookup"><span data-stu-id="ae137-229">False</span></span>  <br/> |<span data-ttu-id="ae137-230">True</span><span class="sxs-lookup"><span data-stu-id="ae137-230">True</span></span>  <br/> |<span data-ttu-id="ae137-231">False</span><span class="sxs-lookup"><span data-stu-id="ae137-231">False</span></span>  <br/> |<span data-ttu-id="ae137-232">无</span><span class="sxs-lookup"><span data-stu-id="ae137-232">None</span></span>  <br/> |<span data-ttu-id="ae137-233">所有权</span><span class="sxs-lookup"><span data-stu-id="ae137-233">Owned</span></span>  <br/> |<span data-ttu-id="ae137-234">FullDetails</span><span class="sxs-lookup"><span data-stu-id="ae137-234">FullDetails</span></span>  <br/> |
|<span data-ttu-id="ae137-235">Reviewer</span><span class="sxs-lookup"><span data-stu-id="ae137-235">Reviewer</span></span>  <br/> |<span data-ttu-id="ae137-236">False</span><span class="sxs-lookup"><span data-stu-id="ae137-236">False</span></span>  <br/> |<span data-ttu-id="ae137-237">False</span><span class="sxs-lookup"><span data-stu-id="ae137-237">False</span></span>  <br/> |<span data-ttu-id="ae137-238">False</span><span class="sxs-lookup"><span data-stu-id="ae137-238">False</span></span>  <br/> |<span data-ttu-id="ae137-239">True</span><span class="sxs-lookup"><span data-stu-id="ae137-239">True</span></span>  <br/> |<span data-ttu-id="ae137-240">False</span><span class="sxs-lookup"><span data-stu-id="ae137-240">False</span></span>  <br/> |<span data-ttu-id="ae137-241">无</span><span class="sxs-lookup"><span data-stu-id="ae137-241">None</span></span>  <br/> |<span data-ttu-id="ae137-242">无</span><span class="sxs-lookup"><span data-stu-id="ae137-242">None</span></span>  <br/> |<span data-ttu-id="ae137-243">FullDetails</span><span class="sxs-lookup"><span data-stu-id="ae137-243">FullDetails</span></span>  <br/> |
|<span data-ttu-id="ae137-244">参与者</span><span class="sxs-lookup"><span data-stu-id="ae137-244">Contributor</span></span>  <br/> |<span data-ttu-id="ae137-245">True</span><span class="sxs-lookup"><span data-stu-id="ae137-245">True</span></span>  <br/> |<span data-ttu-id="ae137-246">False</span><span class="sxs-lookup"><span data-stu-id="ae137-246">False</span></span>  <br/> |<span data-ttu-id="ae137-247">False</span><span class="sxs-lookup"><span data-stu-id="ae137-247">False</span></span>  <br/> |<span data-ttu-id="ae137-248">True</span><span class="sxs-lookup"><span data-stu-id="ae137-248">True</span></span>  <br/> |<span data-ttu-id="ae137-249">False</span><span class="sxs-lookup"><span data-stu-id="ae137-249">False</span></span>  <br/> |<span data-ttu-id="ae137-250">无</span><span class="sxs-lookup"><span data-stu-id="ae137-250">None</span></span>  <br/> |<span data-ttu-id="ae137-251">无</span><span class="sxs-lookup"><span data-stu-id="ae137-251">None</span></span>  <br/> |<span data-ttu-id="ae137-252">无</span><span class="sxs-lookup"><span data-stu-id="ae137-252">None</span></span>  <br/> |
   
<span data-ttu-id="ae137-253">如果您在文件夹级权限请求中指定非自定义权限级别，则无需指定单独的权限设置。</span><span class="sxs-lookup"><span data-stu-id="ae137-253">If you specify a non-custom permission level in the folder-level permissions request, you don't need to specify the individual permission settings.</span></span> <span data-ttu-id="ae137-254">如果您在设置权限级别时指定了单个权限，则会在响应中返回一个**ErrorInvalidPermissionSettings**错误。</span><span class="sxs-lookup"><span data-stu-id="ae137-254">If you do specify an individual permission when you set a permission level, an **ErrorInvalidPermissionSettings** error will be returned in the response.</span></span> 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="ae137-255">使用 EWS 托管 API 添加文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-255">Adding folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="ae137-256"><a name="bk_enableewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ae137-256"><a name="bk_enableewsma"> </a></span></span>

<span data-ttu-id="ae137-257">下面的代码示例演示如何使用 EWS 托管 API 执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="ae137-257">The following code example shows how to use the EWS Managed API to:</span></span> 
  
- <span data-ttu-id="ae137-258">为新用户创建新的[FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx)对象。</span><span class="sxs-lookup"><span data-stu-id="ae137-258">Create a new [FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) object for the new user.</span></span> 
    
- <span data-ttu-id="ae137-259">使用[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法获取文件夹的当前权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-259">Get the current permissions for a folder by using the [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
    
- <span data-ttu-id="ae137-260">将新的**FolderPermissions**添加到[文件夹。权限](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="ae137-260">Add the new **FolderPermissions** to the [Folder.Permissions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) property.</span></span> 
    
- <span data-ttu-id="ae137-261">调用[Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)方法以将新权限保存到服务器。</span><span class="sxs-lookup"><span data-stu-id="ae137-261">Call the [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the new permissions to the server.</span></span> 
    
<span data-ttu-id="ae137-262">本示例假定**服务**是邮箱所有者的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且该用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="ae137-262">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="ae137-263">下面的代码行指定权限级别。</span><span class="sxs-lookup"><span data-stu-id="ae137-263">The following line of code specifies the permission level.</span></span>
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

<span data-ttu-id="ae137-264">如果要使用自定义权限级别，请改为使用此代码。</span><span class="sxs-lookup"><span data-stu-id="ae137-264">If you want to use the custom permission level, use this code instead.</span></span>
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

<span data-ttu-id="ae137-265">在创建具有自定义权限级别的**FolderPermission**对象时，可以设置任意或所有可写[FolderPermission 属性](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ae137-265">You can set any or all of the writable [FolderPermission properties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) when you create a **FolderPermission** object with a custom permission level.</span></span> <span data-ttu-id="ae137-266">但请注意， [FolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx)永远不会显式设置为由应用程序**自定义**。</span><span class="sxs-lookup"><span data-stu-id="ae137-266">Note, however, that the [FolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) is never explicitly set to **Custom** by the application.</span></span> <span data-ttu-id="ae137-267">仅当创建**FolderPermission**对象并设置各个权限时， **FolderPermissionLevel**设置为 Custom。</span><span class="sxs-lookup"><span data-stu-id="ae137-267">The **FolderPermissionLevel** is set to Custom only when you create a **FolderPermission** object and set individual permissions.</span></span> 
  
## <a name="adding-folder-permissions-by-using-ews"></a><span data-ttu-id="ae137-268">使用 EWS 添加文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-268">Adding folder permissions by using EWS</span></span>
<span data-ttu-id="ae137-269"><a name="bk_enableews"> </a></span><span class="sxs-lookup"><span data-stu-id="ae137-269"><a name="bk_enableews"> </a></span></span>

<span data-ttu-id="ae137-270">下面的 EWS 代码示例演示如何通过检索当前权限，然后提交新权限列表，向特定文件夹添加权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-270">The following EWS code examples show how to add permissions to a specific folder by retrieving the current permissions and then submitting a list of new permissions.</span></span>
  
<span data-ttu-id="ae137-271">第一步是发送[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)请求，其中[DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)值指定要在其中添加权限的文件夹（在此示例中为 "已发送的项目" 文件夹）， [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)值包括 folder： PermissionSet。</span><span class="sxs-lookup"><span data-stu-id="ae137-271">The first step is to send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request, where the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to add permissions (the Sent Items folder in this example) and the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="ae137-272">此请求将检索指定文件夹的权限设置。</span><span class="sxs-lookup"><span data-stu-id="ae137-272">This request will retrieve the permission settings for the folder specified.</span></span> 
  
<span data-ttu-id="ae137-273">这也是在调用**Bind**方法[添加文件夹权限](#bk_enableewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="ae137-273">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [add folder permissions](#bk_enableewsma).</span></span>
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ae137-274">服务器使用[GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)邮件响应**GetFolder**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示已成功检索该文件夹。</span><span class="sxs-lookup"><span data-stu-id="ae137-274">The server responds to the **GetFolder** request with a [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="ae137-275">为了提高可读性， [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)和[ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx)值已缩短。</span><span class="sxs-lookup"><span data-stu-id="ae137-275">The [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) and [ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) values have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="ae137-276">接下来，使用**UpdateFolder**操作发送更新的[PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)，其中包括新用户的[权限](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ae137-276">Next, use the **UpdateFolder** operation to send the updated [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx), which includes the [Permission](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) for the new user.</span></span> <span data-ttu-id="ae137-277">请注意，包括[UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)操作中各个文件夹的[SetFolderField](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx)元素将覆盖文件夹中的所有权限设置。</span><span class="sxs-lookup"><span data-stu-id="ae137-277">Note that including the [SetFolderField](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) element for the respective folder in the [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation will overwrite all the permission settings on the folder.</span></span> <span data-ttu-id="ae137-278">同样，包括**UpdateFolder**操作的[DeleteFolderField](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx)选项也会删除文件夹上的所有权限设置。</span><span class="sxs-lookup"><span data-stu-id="ae137-278">Likewise, including the [DeleteFolderField](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) option of the **UpdateFolder** operation will also delete all the permission settings on the folder.</span></span> 
  
<span data-ttu-id="ae137-279">这也是在调用**Update**方法[添加文件夹权限](#bk_enableewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="ae137-279">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [add folder permissions](#bk_enableewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ae137-280">下面的代码行指定权限级别。</span><span class="sxs-lookup"><span data-stu-id="ae137-280">The following line of code specifies the permission level.</span></span>
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

<span data-ttu-id="ae137-281">如果要使用自定义权限级别，请改为使用此代码。</span><span class="sxs-lookup"><span data-stu-id="ae137-281">If you want to use the custom permission level, use this code instead.</span></span>
  
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

<span data-ttu-id="ae137-282">服务器使用[UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)邮件响应**UpdateFolder**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示该文件夹已成功更新。</span><span class="sxs-lookup"><span data-stu-id="ae137-282">The server responds to the **UpdateFolder** request with an [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was updated successfully.</span></span>
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="ae137-283">使用 EWS 托管 API 删除文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-283">Removing folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="ae137-284"><a name="bk_removeewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ae137-284"><a name="bk_removeewsma"> </a></span></span>

<span data-ttu-id="ae137-285">下面的代码示例演示如何使用 EWS 托管 API 删除特定文件夹（默认权限和匿名权限除外）的所有用户权限，具体方法为：</span><span class="sxs-lookup"><span data-stu-id="ae137-285">The following code example shows how to use the EWS Managed API to remove all user permissions on a specific folder, except for the default and anonymous permissions, by:</span></span>
  
1. <span data-ttu-id="ae137-286">使用**Bind**方法获取文件夹的当前权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-286">Getting the current permissions for a folder by using the **Bind** method.</span></span> 
    
2. <span data-ttu-id="ae137-287">循环访问**权限**集合，并移除单个用户的权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-287">Iterating through the **Permissions** collection and removing permissions for individual users.</span></span> 
    
3. <span data-ttu-id="ae137-288">调用**Update**方法以保存更改。</span><span class="sxs-lookup"><span data-stu-id="ae137-288">Calling the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="ae137-289">本示例将删除对文件夹的所有用户权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-289">This example removes all user permissions on a folder.</span></span> <span data-ttu-id="ae137-290">如果要修改此示例以仅删除特定用户的权限，请更改以下代码行，以标识用户的显示名称或 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="ae137-290">If you want to modify this example to remove permissions only for a specific user, change the following line of code to identify either the display name or SMTP address of the user.</span></span>
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

<span data-ttu-id="ae137-291">本示例假定**服务**是邮箱所有者的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且该用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="ae137-291">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object for the mailbox owner and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="removing-folder-permissions-by-using-ews"></a><span data-ttu-id="ae137-292">使用 EWS 删除文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-292">Removing folder permissions by using EWS</span></span>
<span data-ttu-id="ae137-293"><a name="bk_removeews"> </a></span><span class="sxs-lookup"><span data-stu-id="ae137-293"><a name="bk_removeews"> </a></span></span>

<span data-ttu-id="ae137-294">下面的 EWS 代码示例展示了如何删除对特定文件夹的所有用户权限，默认权限和匿名权限除外。</span><span class="sxs-lookup"><span data-stu-id="ae137-294">The following EWS code examples show how to remove all user permissions on a specific folder, except for the default and anonymous permissions.</span></span>
  
<span data-ttu-id="ae137-295">首先，发送[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)请求，其中[DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)值指定要在其中删除权限的文件夹（此示例中的 "已发送的项目" 文件夹）， [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)值包括 folder： PermissionSet。</span><span class="sxs-lookup"><span data-stu-id="ae137-295">First, send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) request where the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) value specifies the folder in which to remove permissions (the Sent Items folder in this example) and the [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) value includes folder:PermissionSet.</span></span> <span data-ttu-id="ae137-296">此请求将检索指定文件夹的[PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="ae137-296">This request will retrieve the [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) for the folder specified.</span></span> 
  
<span data-ttu-id="ae137-297">这也是在调用**Bind**方法以[删除文件夹权限](#bk_removeewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="ae137-297">This is also the XML request that the EWS Managed API sends when you call the **Bind** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ae137-298">服务器使用[GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)邮件响应**GetFolder**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示已成功检索该文件夹。</span><span class="sxs-lookup"><span data-stu-id="ae137-298">The server responds to the **GetFolder** request with a [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the folder was retrieved successfully.</span></span> <span data-ttu-id="ae137-299">为了提高可读性， **FolderId**和**ParentFolderId**元素的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="ae137-299">The values of the **FolderId** and **ParentFolderId** elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="ae137-300">接下来，使用**UpdateFolder**操作发送更新的**PermissionSet**，其中不包括已删除用户的**权限**。</span><span class="sxs-lookup"><span data-stu-id="ae137-300">Next, use the **UpdateFolder** operation to send the updated **PermissionSet**, which does not include the **Permission** for the removed user.</span></span> 
  
<span data-ttu-id="ae137-301">这也是在调用**Update**方法以[删除文件夹权限](#bk_removeewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="ae137-301">This is also the XML request that the EWS Managed API sends when you call the **Update** method to [remove folder permissions](#bk_removeewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="ae137-302">服务器使用**UpdateFolderResponse**邮件响应**UpdateFolder**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值为**NoError**，表示更新已成功。</span><span class="sxs-lookup"><span data-stu-id="ae137-302">The server responds to the **UpdateFolder** request with an **UpdateFolderResponse** message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the update was successful.</span></span>
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a><span data-ttu-id="ae137-303">使用 EWS 托管 API 更新文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-303">Updating folder permissions by using the EWS Managed API</span></span>
<span data-ttu-id="ae137-304"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="ae137-304"><a name="bk_updateewsma"> </a></span></span>

<span data-ttu-id="ae137-305">您还可以使用 EWS 托管 API 更新特定文件夹的文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-305">You can also update folder permissions for a specific folder by using the EWS Managed API.</span></span> <span data-ttu-id="ae137-306">若要更新权限，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="ae137-306">To update the permissions:</span></span> 
  
1. <span data-ttu-id="ae137-307">删除对过期权限的[文件夹权限](#bk_removeewsma)，但不要调用**Update**方法（尚不调用）。</span><span class="sxs-lookup"><span data-stu-id="ae137-307">[Remove the folder permissions](#bk_removeewsma) for the outdated permissions, but do not call the **Update** method (yet).</span></span> 
    
2. <span data-ttu-id="ae137-308">[为新的或更改的用户添加文件夹权限](#bk_enableewsma)。</span><span class="sxs-lookup"><span data-stu-id="ae137-308">[Add folder permissions for the new or changed users](#bk_enableewsma).</span></span>
    
3. <span data-ttu-id="ae137-309">调用**Update**方法以保存更改。</span><span class="sxs-lookup"><span data-stu-id="ae137-309">Call the **Update** method to save the changes.</span></span> 
    
<span data-ttu-id="ae137-310">如果您尝试为同一用户添加两组权限，您将收到**ServiceResponseException**错误，并显示以下说明： "指定的权限集包含重复的 UserIds"。</span><span class="sxs-lookup"><span data-stu-id="ae137-310">If you try to add two sets of permissions for the same user, you will receive a **ServiceResponseException** error with the following description: "The specified permission set contains duplicate UserIds".</span></span> <span data-ttu-id="ae137-311">在这种情况下，从**权限**集合中删除当前权限，然后将新权限添加到**权限**集合中。</span><span class="sxs-lookup"><span data-stu-id="ae137-311">In that case, remove the current permissions from the **Permission** collection, then add the new permissions to the **Permission** collection.</span></span> 
  
## <a name="updating-folder-permissions-by-using-ews"></a><span data-ttu-id="ae137-312">使用 EWS 更新文件夹权限</span><span class="sxs-lookup"><span data-stu-id="ae137-312">Updating folder permissions by using EWS</span></span>
<span data-ttu-id="ae137-313"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="ae137-313"><a name="bk_updateews"> </a></span></span>

<span data-ttu-id="ae137-314">您还可以通过使用 EWS 组合删除和添加过程来更新特定文件夹的文件夹权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-314">You can also update folder permissions for specific folders by using EWS by combining the removal and addition process.</span></span> <span data-ttu-id="ae137-315">若要更新权限，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="ae137-315">To update the permissions:</span></span> 
  
1. <span data-ttu-id="ae137-316">使用**GetFolder**操作检索文件夹的当前权限。</span><span class="sxs-lookup"><span data-stu-id="ae137-316">Retrieve the folder's current permissions by using the **GetFolder** operation.</span></span> 
    
2. <span data-ttu-id="ae137-317">使用**UpdateFolder**操作发送已更新的权限列表。</span><span class="sxs-lookup"><span data-stu-id="ae137-317">Send an updated list of permissions by using the **UpdateFolder** operation.</span></span> 
    
<span data-ttu-id="ae137-318">这两个操作用于[启用](#bk_enableews)或删除使用 EWS 的[访问权限](#bk_removeews)。</span><span class="sxs-lookup"><span data-stu-id="ae137-318">These are the same two operations you use to [enable](#bk_enableews) or [remove access](#bk_removeews) by using EWS.</span></span> <span data-ttu-id="ae137-319">唯一的区别是，当您收到**GetFolder**响应时，它将包含用户的**权限**集。</span><span class="sxs-lookup"><span data-stu-id="ae137-319">The only difference is that when you receive the **GetFolder** response, it will contain a **Permission** set for user.</span></span> <span data-ttu-id="ae137-320">只需将该现有**权限**元素替换为新的**权限**元素，然后使用新**权限**值或值发送**UpdateFolder**操作。</span><span class="sxs-lookup"><span data-stu-id="ae137-320">Simply replace that existing **Permission** element with the new **Permission** element, and then send the **UpdateFolder** operation with the new **Permission** value or values.</span></span> 
  
<span data-ttu-id="ae137-321">如果您尝试为同一用户添加两组权限，您将收到**ResponseCode**值**ErrorDuplicateUserIdsSpecified**。</span><span class="sxs-lookup"><span data-stu-id="ae137-321">If you try to add two sets of permissions for the same user, you will receive a **ResponseCode** value of **ErrorDuplicateUserIdsSpecified**.</span></span> <span data-ttu-id="ae137-322">在这种情况下，请从请求中删除用户的过期权限值，然后重试该请求。</span><span class="sxs-lookup"><span data-stu-id="ae137-322">In that case, remove the outdated Permission value for the user from the request and then retry the request.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ae137-323">后续步骤</span><span class="sxs-lookup"><span data-stu-id="ae137-323">Next steps</span></span>

<span data-ttu-id="ae137-324">授予用户对特定文件夹的权限后，用户可以将该文件夹作为代理访问。</span><span class="sxs-lookup"><span data-stu-id="ae137-324">After you give a user permission to a specific folder, the user can access the folder as a delegate.</span></span> <span data-ttu-id="ae137-325">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="ae137-325">For more information, see:</span></span>
  
- [<span data-ttu-id="ae137-326">在 Exchange 中使用 EWS 以代理的形式访问电子邮件</span><span class="sxs-lookup"><span data-stu-id="ae137-326">Access email as a delegate by using EWS in Exchange</span></span>](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ae137-327">在 Exchange 中使用 EWS 作为代理访问日历</span><span class="sxs-lookup"><span data-stu-id="ae137-327">Access a calendar as a delegate by using EWS in Exchange</span></span>](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="ae137-328">在 Exchange 中使用 EWS 以代理的形式访问联系人</span><span class="sxs-lookup"><span data-stu-id="ae137-328">Access contacts as a delegate by using EWS in Exchange</span></span>](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="ae137-329">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ae137-329">See also</span></span>

- [<span data-ttu-id="ae137-330">代理访问和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="ae137-330">Delegate access and EWS in Exchange</span></span>](delegate-access-and-ews-in-exchange.md)   
- [<span data-ttu-id="ae137-331">使用 Exchange 中的 EWS 添加和删除委派</span><span class="sxs-lookup"><span data-stu-id="ae137-331">Add and remove delegates by using EWS in Exchange</span></span>](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="ae137-332">文件夹和交换中的 EWS 中的项目</span><span class="sxs-lookup"><span data-stu-id="ae137-332">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)
    

