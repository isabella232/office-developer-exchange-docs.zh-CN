---
title: DistinguishedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedFolderId
api_type:
- schema
ms.assetid: 50018162-2941-4227-8a5b-d6b4686bb32f
description: DistinguishedFolderId 元素标识可以通过名称引用的文件夹。 如果您不使用此元素，您必须使用文件夹 Id 元素来识别文件夹。
ms.openlocfilehash: 834166be3d882fa8c0533cfcc2999600430b82ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753960"
---
# <a name="distinguishedfolderid"></a><span data-ttu-id="836b0-104">DistinguishedFolderId</span><span class="sxs-lookup"><span data-stu-id="836b0-104">DistinguishedFolderId</span></span>

<span data-ttu-id="836b0-105">**DistinguishedFolderId**元素标识可以通过名称引用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-105">The **DistinguishedFolderId** element identifies folders that can be referenced by name.</span></span> <span data-ttu-id="836b0-106">如果您不使用此元素，您必须使用[文件夹 Id](folderid.md)元素来识别文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-106">If you do not use this element, you must use the [FolderId](folderid.md) element to identify a folder.</span></span> 
  
```XML
<DistinguishedFolderId Id="" ChangeKey="">
   <Mailbox/>
</DistinguishedFolderId>
```

 <span data-ttu-id="836b0-107">**DistinguishedFolderIdType**</span><span class="sxs-lookup"><span data-stu-id="836b0-107">**DistinguishedFolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="836b0-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="836b0-108">Attributes and elements</span></span>

<span data-ttu-id="836b0-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="836b0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="836b0-110">属性</span><span class="sxs-lookup"><span data-stu-id="836b0-110">Attributes</span></span>

|<span data-ttu-id="836b0-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="836b0-111">**Attribute**</span></span>|<span data-ttu-id="836b0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="836b0-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="836b0-113">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="836b0-113">**Id**</span></span> <br/> |<span data-ttu-id="836b0-114">包含一个字符串，标识默认文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-114">Contains a string that identifies a default folder.</span></span> <span data-ttu-id="836b0-115">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="836b0-115">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="836b0-116">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="836b0-116">**ChangeKey**</span></span> <br/> |<span data-ttu-id="836b0-117">包含一个字符串，标识的文件夹的**Id**属性标识的版本。</span><span class="sxs-lookup"><span data-stu-id="836b0-117">Contains a string that identifies a version of a folder that is identified by the **Id** attribute.</span></span> <span data-ttu-id="836b0-118">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="836b0-118">This attribute is optional.</span></span> <span data-ttu-id="836b0-119">使用此属性以确保正确版本的文件夹使用。</span><span class="sxs-lookup"><span data-stu-id="836b0-119">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
#### <a name="id-attribute-values"></a><span data-ttu-id="836b0-120">Id 属性值</span><span class="sxs-lookup"><span data-stu-id="836b0-120">Id attribute values</span></span>

|<span data-ttu-id="836b0-121">**值**</span><span class="sxs-lookup"><span data-stu-id="836b0-121">**Value**</span></span>|<span data-ttu-id="836b0-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="836b0-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="836b0-123">日历</span><span class="sxs-lookup"><span data-stu-id="836b0-123">calendar</span></span>  <br/> |<span data-ttu-id="836b0-124">代表日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-124">Represents the Calendar folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-125">contacts</span><span class="sxs-lookup"><span data-stu-id="836b0-125">contacts</span></span>  <br/> |<span data-ttu-id="836b0-126">代表联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-126">Represents the Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-127">DeletedItems</span><span class="sxs-lookup"><span data-stu-id="836b0-127">deleteditems</span></span>  <br/> |<span data-ttu-id="836b0-128">代表已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-128">Represents the Deleted Items folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-129">草稿</span><span class="sxs-lookup"><span data-stu-id="836b0-129">drafts</span></span>  <br/> |<span data-ttu-id="836b0-130">代表草稿文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-130">Represents the Drafts folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-131">收件箱</span><span class="sxs-lookup"><span data-stu-id="836b0-131">inbox</span></span>  <br/> |<span data-ttu-id="836b0-132">代表收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-132">Represents the Inbox folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-133">日记</span><span class="sxs-lookup"><span data-stu-id="836b0-133">journal</span></span>  <br/> |<span data-ttu-id="836b0-134">代表日记文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-134">Represents the Journal folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-135">notes</span><span class="sxs-lookup"><span data-stu-id="836b0-135">notes</span></span>  <br/> |<span data-ttu-id="836b0-136">代表便笺文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-136">Represents the Notes folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-137">发件箱</span><span class="sxs-lookup"><span data-stu-id="836b0-137">outbox</span></span>  <br/> |<span data-ttu-id="836b0-138">代表发件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-138">Represents the Outbox folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-139">sentitems</span><span class="sxs-lookup"><span data-stu-id="836b0-139">sentitems</span></span>  <br/> |<span data-ttu-id="836b0-140">代表已发送邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-140">Represents the Sent Items folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-141">tasks</span><span class="sxs-lookup"><span data-stu-id="836b0-141">tasks</span></span>  <br/> |<span data-ttu-id="836b0-142">代表任务文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-142">Represents the Tasks folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-143">msgfolderroot</span><span class="sxs-lookup"><span data-stu-id="836b0-143">msgfolderroot</span></span>  <br/> |<span data-ttu-id="836b0-144">代表邮件文件夹根目录。</span><span class="sxs-lookup"><span data-stu-id="836b0-144">Represents the message folder root.</span></span>  <br/> |
|<span data-ttu-id="836b0-145">root</span><span class="sxs-lookup"><span data-stu-id="836b0-145">root</span></span>  <br/> |<span data-ttu-id="836b0-146">表示邮箱的根。</span><span class="sxs-lookup"><span data-stu-id="836b0-146">Represents the root of the mailbox.</span></span>  <br/> |
|<span data-ttu-id="836b0-147">junkemail</span><span class="sxs-lookup"><span data-stu-id="836b0-147">junkemail</span></span>  <br/> |<span data-ttu-id="836b0-148">代表垃圾邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-148">Represents the Junk Email folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-149">searchfolders</span><span class="sxs-lookup"><span data-stu-id="836b0-149">searchfolders</span></span>  <br/> |<span data-ttu-id="836b0-150">代表搜索文件夹文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-150">Represents the Search Folders folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-151">语音邮件</span><span class="sxs-lookup"><span data-stu-id="836b0-151">voicemail</span></span>  <br/> |<span data-ttu-id="836b0-152">代表语音邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-152">Represents the Voice Mail folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-153">recoverableitemsroot</span><span class="sxs-lookup"><span data-stu-id="836b0-153">recoverableitemsroot</span></span>  <br/> |<span data-ttu-id="836b0-154">代表转储程序根文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-154">Represents the dumpster root folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-155">recoverableitemsdeletions</span><span class="sxs-lookup"><span data-stu-id="836b0-155">recoverableitemsdeletions</span></span>  <br/> |<span data-ttu-id="836b0-156">代表转储程序删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-156">Represents the dumpster deletions folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-157">recoverableitemsversions</span><span class="sxs-lookup"><span data-stu-id="836b0-157">recoverableitemsversions</span></span>  <br/> |<span data-ttu-id="836b0-158">代表转储程序版本文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-158">Represents the dumpster versions folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-159">recoverableitemspurges</span><span class="sxs-lookup"><span data-stu-id="836b0-159">recoverableitemspurges</span></span>  <br/> |<span data-ttu-id="836b0-160">代表转储程序清除文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-160">Represents the dumpster purges folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-161">archiveroot</span><span class="sxs-lookup"><span data-stu-id="836b0-161">archiveroot</span></span>  <br/> |<span data-ttu-id="836b0-162">代表根存档文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-162">Represents the root archive folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-163">archivemsgfolderroot</span><span class="sxs-lookup"><span data-stu-id="836b0-163">archivemsgfolderroot</span></span>  <br/> |<span data-ttu-id="836b0-164">代表根存档邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-164">Represents the root archive message folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-165">archivedeleteditems</span><span class="sxs-lookup"><span data-stu-id="836b0-165">archivedeleteditems</span></span>  <br/> |<span data-ttu-id="836b0-166">代表存档已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-166">Represents the archive deleted items folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-167">archiveinbox</span><span class="sxs-lookup"><span data-stu-id="836b0-167">archiveinbox</span></span>  <br/> |<span data-ttu-id="836b0-168">代表存档收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-168">Represents the archive Inbox folder.</span></span> <span data-ttu-id="836b0-169">内部版本号 15.00.0913.09 开头的 Exchange 版本包括此值。</span><span class="sxs-lookup"><span data-stu-id="836b0-169">Versions of Exchange starting with build number 15.00.0913.09 include this value.</span></span>  <br/> |
|<span data-ttu-id="836b0-170">archiverecoverableitemsroot</span><span class="sxs-lookup"><span data-stu-id="836b0-170">archiverecoverableitemsroot</span></span>  <br/> |<span data-ttu-id="836b0-171">代表存档可恢复的项目根文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-171">Represents the archive recoverable items root folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-172">archiverecoverableitemsdeletions</span><span class="sxs-lookup"><span data-stu-id="836b0-172">archiverecoverableitemsdeletions</span></span>  <br/> |<span data-ttu-id="836b0-173">代表存档可恢复的项目删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-173">Represents the archive recoverable items deletions folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-174">archiverecoverableitemsversions</span><span class="sxs-lookup"><span data-stu-id="836b0-174">archiverecoverableitemsversions</span></span>  <br/> |<span data-ttu-id="836b0-175">代表存档可恢复的项目版本文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-175">Represents the archive recoverable items versions folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-176">archiverecoverableitemspurges</span><span class="sxs-lookup"><span data-stu-id="836b0-176">archiverecoverableitemspurges</span></span>  <br/> |<span data-ttu-id="836b0-177">代表存档可恢复的项目清除文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-177">Represents the archive recoverable items purges folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-178">syncissues</span><span class="sxs-lookup"><span data-stu-id="836b0-178">syncissues</span></span>  <br/> |<span data-ttu-id="836b0-179">代表同步问题文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-179">Represents the sync issues folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-180">冲突</span><span class="sxs-lookup"><span data-stu-id="836b0-180">conflicts</span></span>  <br/> |<span data-ttu-id="836b0-181">代表冲突文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-181">Represents the conflicts folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-182">localfailures</span><span class="sxs-lookup"><span data-stu-id="836b0-182">localfailures</span></span>  <br/> |<span data-ttu-id="836b0-183">代表本地故障文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-183">Represents the local failures folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-184">serverfailures</span><span class="sxs-lookup"><span data-stu-id="836b0-184">serverfailures</span></span>  <br/> |<span data-ttu-id="836b0-185">代表服务器故障文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-185">Represents the server failures folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-186">recipientcache</span><span class="sxs-lookup"><span data-stu-id="836b0-186">recipientcache</span></span>  <br/> |<span data-ttu-id="836b0-187">代表收件人缓存文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-187">Represents the recipient cache folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-188">quickcontacts</span><span class="sxs-lookup"><span data-stu-id="836b0-188">quickcontacts</span></span>  <br/> |<span data-ttu-id="836b0-189">代表快速联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-189">Represents the quick contacts folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-190">conversationhistory</span><span class="sxs-lookup"><span data-stu-id="836b0-190">conversationhistory</span></span>  <br/> |<span data-ttu-id="836b0-191">代表对话历史记录文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-191">Represents the conversation history folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-192">adminauditlogs</span><span class="sxs-lookup"><span data-stu-id="836b0-192">adminauditlogs</span></span>  <br/> |<span data-ttu-id="836b0-193">代表管理员审核日志文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-193">Represents the admin audit logs folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-194">todosearch</span><span class="sxs-lookup"><span data-stu-id="836b0-194">todosearch</span></span>  <br/> |<span data-ttu-id="836b0-195">代表 todo 搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-195">Represents the todo search folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-196">mycontacts</span><span class="sxs-lookup"><span data-stu-id="836b0-196">mycontacts</span></span>  <br/> |<span data-ttu-id="836b0-197">代表我的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-197">Represents the My Contacts folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-198">目录</span><span class="sxs-lookup"><span data-stu-id="836b0-198">directory</span></span>  <br/> |<span data-ttu-id="836b0-199">表示目录文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-199">Represents the directory folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-200">imcontactlist</span><span class="sxs-lookup"><span data-stu-id="836b0-200">imcontactlist</span></span>  <br/> |<span data-ttu-id="836b0-201">代表 IM 联系人列表文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-201">Represents the IM contact list folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-202">peopleconnect</span><span class="sxs-lookup"><span data-stu-id="836b0-202">peopleconnect</span></span>  <br/> |<span data-ttu-id="836b0-203">代表人员连接文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-203">Represents the people connect folder.</span></span>  <br/> |
|<span data-ttu-id="836b0-204">收藏夹</span><span class="sxs-lookup"><span data-stu-id="836b0-204">favorites</span></span>  <br/> |<span data-ttu-id="836b0-205">代表收藏夹文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-205">Represents the Favorites folder.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="836b0-206">子元素</span><span class="sxs-lookup"><span data-stu-id="836b0-206">Child elements</span></span>

|<span data-ttu-id="836b0-207">**元素**</span><span class="sxs-lookup"><span data-stu-id="836b0-207">**Element**</span></span>|<span data-ttu-id="836b0-208">**说明**</span><span class="sxs-lookup"><span data-stu-id="836b0-208">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="836b0-209">Mailbox</span><span class="sxs-lookup"><span data-stu-id="836b0-209">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="836b0-210">标识的主 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="836b0-210">Identifies a primary SMTP address.</span></span> <span data-ttu-id="836b0-211">不允许使用代理地址。</span><span class="sxs-lookup"><span data-stu-id="836b0-211">Proxy addresses are not allowed.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="836b0-212">父元素</span><span class="sxs-lookup"><span data-stu-id="836b0-212">Parent elements</span></span>

|<span data-ttu-id="836b0-213">**元素**</span><span class="sxs-lookup"><span data-stu-id="836b0-213">**Element**</span></span>|<span data-ttu-id="836b0-214">**说明**</span><span class="sxs-lookup"><span data-stu-id="836b0-214">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="836b0-215">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="836b0-215">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="836b0-216">指示对话操作使用文件夹的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-216">Indicates the folder that is targeted for conversation actions that use folders.</span></span>  <br/> |
|[<span data-ttu-id="836b0-217">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="836b0-217">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="836b0-218">指示副本的目标文件夹，并移动对话操作。</span><span class="sxs-lookup"><span data-stu-id="836b0-218">Indicates the destination folder for copy and move conversation actions.</span></span>  <br/> |
|[<span data-ttu-id="836b0-219">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="836b0-219">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> | <span data-ttu-id="836b0-220">标识在其中创建新的文件夹或项目的文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-220">Identifies the folder in which a new folder or item is created.</span></span>  <br/><br/><span data-ttu-id="836b0-221">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="836b0-221">The following are the XPath expressions to this element:</span></span><br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[<span data-ttu-id="836b0-222">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="836b0-222">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="836b0-223">标识要[FindItem 操作](finditem-operation.md)和[FindFolder 操作](findfolder-operation.md)搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-223">Identifies folders to search for the [FindItem operation](finditem-operation.md) and the [FindFolder operation](findfolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="836b0-224">BaseFolderIds</span><span class="sxs-lookup"><span data-stu-id="836b0-224">BaseFolderIds</span></span>](basefolderids.md) <br/> |<span data-ttu-id="836b0-225">代表将搜索以确定搜索文件夹的内容的文件夹的集合。</span><span class="sxs-lookup"><span data-stu-id="836b0-225">Represents the collection of folders that will be searched to determine the contents of a search folder.</span></span>  <br/> |
|[<span data-ttu-id="836b0-226">FolderIds</span><span class="sxs-lookup"><span data-stu-id="836b0-226">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="836b0-227">包含用于标识要复制、 移动、 获取、 删除或监视事件通知的文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="836b0-227">Contains an array of folder identifiers that are used to identify folders to copy, move, get, delete, or monitor for event notifications.</span></span>  <br/> |
|[<span data-ttu-id="836b0-228">FolderChange</span><span class="sxs-lookup"><span data-stu-id="836b0-228">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="836b0-229">表示要在单个文件夹上进行的更改的集合。</span><span class="sxs-lookup"><span data-stu-id="836b0-229">Represents a collection of changes to be performed on a single folder.</span></span>  <br/> <br/><span data-ttu-id="836b0-230">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="836b0-230">The following is the XPath expression to this element:</span></span><br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[<span data-ttu-id="836b0-231">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="836b0-231">ToFolderId</span></span>](tofolderid.md) <br/> | <span data-ttu-id="836b0-232">表示复制或移动项目或文件夹的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-232">Represents the destination folder for a copied or moved item or folder.</span></span><br/><br/><span data-ttu-id="836b0-233">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="836b0-233">The following are the XPath expressions to this element:</span></span><br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[<span data-ttu-id="836b0-234">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="836b0-234">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> | <span data-ttu-id="836b0-235">标识用于更新、 发送和在 Exchange 存储中创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-235">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span><br/><br/><span data-ttu-id="836b0-236">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="836b0-236">The following are the XPath expressions to this element:</span></span><br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[<span data-ttu-id="836b0-237">SyncFolderId</span><span class="sxs-lookup"><span data-stu-id="836b0-237">SyncFolderId</span></span>](syncfolderid.md) <br/> |<span data-ttu-id="836b0-238">代表包含要同步的项的文件夹。</span><span class="sxs-lookup"><span data-stu-id="836b0-238">Represents the folder that contains the items to synchronize.</span></span>  <br/> |
|[<span data-ttu-id="836b0-239">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="836b0-239">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="836b0-240">代表用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="836b0-240">Represents the name of a user configuration object.</span></span> <span data-ttu-id="836b0-241">用户配置对象名称为用户配置对象的标识符。</span><span class="sxs-lookup"><span data-stu-id="836b0-241">The user configuration object name is the identifier for a user configuration object.</span></span>  <br/> |
|[<span data-ttu-id="836b0-242">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="836b0-242">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="836b0-243">表示的文件夹的 ID 项将被复制到该电子邮件。</span><span class="sxs-lookup"><span data-stu-id="836b0-243">Represents the ID of the folder that email items will be copied to.</span></span>  <br/> |
|[<span data-ttu-id="836b0-244">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="836b0-244">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="836b0-245">表示的文件夹的 ID 将项目移至的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="836b0-245">Represents the ID of the folder that email items will be moved to.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="836b0-246">文本值</span><span class="sxs-lookup"><span data-stu-id="836b0-246">Text value</span></span>

<span data-ttu-id="836b0-247">无。</span><span class="sxs-lookup"><span data-stu-id="836b0-247">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="836b0-248">注解</span><span class="sxs-lookup"><span data-stu-id="836b0-248">Remarks</span></span>

<span data-ttu-id="836b0-249">**DistinguishedFolderId**解析为**文件夹 Id**。</span><span class="sxs-lookup"><span data-stu-id="836b0-249">A **DistinguishedFolderId** resolves to a **FolderId**.</span></span> 
  
<span data-ttu-id="836b0-250">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="836b0-250">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="836b0-251">元素信息</span><span class="sxs-lookup"><span data-stu-id="836b0-251">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="836b0-252">命名空间</span><span class="sxs-lookup"><span data-stu-id="836b0-252">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="836b0-253">架构名称</span><span class="sxs-lookup"><span data-stu-id="836b0-253">Schema Name</span></span>  <br/> |<span data-ttu-id="836b0-254">类型架构</span><span class="sxs-lookup"><span data-stu-id="836b0-254">Types schema</span></span>  <br/> |
|<span data-ttu-id="836b0-255">验证文件</span><span class="sxs-lookup"><span data-stu-id="836b0-255">Validation File</span></span>  <br/> |<span data-ttu-id="836b0-256">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="836b0-256">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="836b0-257">可以为空</span><span class="sxs-lookup"><span data-stu-id="836b0-257">Can be Empty</span></span>  <br/> |<span data-ttu-id="836b0-258">False</span><span class="sxs-lookup"><span data-stu-id="836b0-258">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="836b0-259">另请参阅</span><span class="sxs-lookup"><span data-stu-id="836b0-259">See also</span></span>

- [<span data-ttu-id="836b0-260">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="836b0-260">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="836b0-261">Creating Folders (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="836b0-261">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

