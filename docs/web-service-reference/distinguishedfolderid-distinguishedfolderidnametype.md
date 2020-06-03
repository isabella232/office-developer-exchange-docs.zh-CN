---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: DistinguishedFolderId 元素标识可通过名称引用的文件夹。
ms.openlocfilehash: ac239ec63f78322f6c82ab4be269d6fe4380dd8d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456190"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a><span data-ttu-id="00ada-103">DistinguishedFolderId (DistinguishedFolderIdNameType)</span><span class="sxs-lookup"><span data-stu-id="00ada-103">DistinguishedFolderId (DistinguishedFolderIdNameType)</span></span>

<span data-ttu-id="00ada-104">**DistinguishedFolderId**元素标识可通过名称引用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="00ada-104">The **DistinguishedFolderId** element identifies folders that can be referenced by name.</span></span> 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 <span data-ttu-id="00ada-105">**DistinguishedFolderIdNameType**</span><span class="sxs-lookup"><span data-stu-id="00ada-105">**DistinguishedFolderIdNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="00ada-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="00ada-106">Attributes and elements</span></span>

<span data-ttu-id="00ada-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="00ada-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00ada-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="00ada-108">Attributes</span></span>

<span data-ttu-id="00ada-109">无。</span><span class="sxs-lookup"><span data-stu-id="00ada-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="00ada-110">子元素</span><span class="sxs-lookup"><span data-stu-id="00ada-110">Child elements</span></span>

<span data-ttu-id="00ada-111">无</span><span class="sxs-lookup"><span data-stu-id="00ada-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="00ada-112">父元素</span><span class="sxs-lookup"><span data-stu-id="00ada-112">Parent elements</span></span>

|<span data-ttu-id="00ada-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="00ada-113">**Element**</span></span>|<span data-ttu-id="00ada-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="00ada-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00ada-115">Folder</span><span class="sxs-lookup"><span data-stu-id="00ada-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="00ada-116">指定一个通用文件夹。</span><span class="sxs-lookup"><span data-stu-id="00ada-116">Specifies a generic folder.</span></span>  <br/> |
|[<span data-ttu-id="00ada-117">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="00ada-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="00ada-118">指定 "日历" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="00ada-118">Specifies a calendar folder.</span></span>  <br/> |
|[<span data-ttu-id="00ada-119">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="00ada-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="00ada-120">指定 "联系人" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="00ada-120">Specifies a contacts folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="00ada-121">文本值</span><span class="sxs-lookup"><span data-stu-id="00ada-121">Text value</span></span>

<span data-ttu-id="00ada-122">**DistinguishedFolderId 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="00ada-122">**DistinguishedFolderId element text values**</span></span>

|<span data-ttu-id="00ada-123">**值**</span><span class="sxs-lookup"><span data-stu-id="00ada-123">**Value**</span></span>|<span data-ttu-id="00ada-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="00ada-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00ada-125">日历</span><span class="sxs-lookup"><span data-stu-id="00ada-125">calendar</span></span>  <br/> |<span data-ttu-id="00ada-126">指示 "日历" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-126">Indicates the URL of the calendar folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-127">contacts</span><span class="sxs-lookup"><span data-stu-id="00ada-127">contacts</span></span>  <br/> |<span data-ttu-id="00ada-128">指示 "联系人" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-128">Indicates the URL of the contacts folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-129">deleteditems</span><span class="sxs-lookup"><span data-stu-id="00ada-129">deleteditems</span></span>  <br/> |<span data-ttu-id="00ada-130">指示 "已删除邮件" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-130">Indicates the URL of the deleted items folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-131">drafts</span><span class="sxs-lookup"><span data-stu-id="00ada-131">drafts</span></span>  <br/> |<span data-ttu-id="00ada-132">指示 "草稿" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-132">Indicates the URL of the drafts folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-133">inbox</span><span class="sxs-lookup"><span data-stu-id="00ada-133">inbox</span></span>  <br/> |<span data-ttu-id="00ada-134">指示 "收件箱" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-134">Indicates the URL of the inbox folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-135">日志</span><span class="sxs-lookup"><span data-stu-id="00ada-135">journal</span></span>  <br/> |<span data-ttu-id="00ada-136">指示日记文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-136">Indicates the URL of the journal folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-137">注释</span><span class="sxs-lookup"><span data-stu-id="00ada-137">notes</span></span>  <br/> |<span data-ttu-id="00ada-138">指示 "便笺" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-138">Indicates the URL of the notes folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-139">outbox</span><span class="sxs-lookup"><span data-stu-id="00ada-139">outbox</span></span>  <br/> |<span data-ttu-id="00ada-140">指示 "发件箱" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-140">Indicates the URL of the outbox folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-141">sentitems</span><span class="sxs-lookup"><span data-stu-id="00ada-141">sentitems</span></span>  <br/> |<span data-ttu-id="00ada-142">指示 "已发送邮件" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-142">Indicates the URL of the sent items folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-143">tasks</span><span class="sxs-lookup"><span data-stu-id="00ada-143">tasks</span></span>  <br/> |<span data-ttu-id="00ada-144">指示 "任务" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-144">Indicates the URL of the tasks folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-145">msgfolderroot</span><span class="sxs-lookup"><span data-stu-id="00ada-145">msgfolderroot</span></span>  <br/> |<span data-ttu-id="00ada-146">指示邮件根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-146">Indicates the URL of the message root folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-147">publicfoldersroot</span><span class="sxs-lookup"><span data-stu-id="00ada-147">publicfoldersroot</span></span>  <br/> |<span data-ttu-id="00ada-148">指示公用文件夹根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-148">Indicates the URL of the public folders root folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-149">root</span><span class="sxs-lookup"><span data-stu-id="00ada-149">root</span></span>  <br/> |<span data-ttu-id="00ada-150">指示根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-150">Indicates the URL of the root folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-151">junkemail</span><span class="sxs-lookup"><span data-stu-id="00ada-151">junkemail</span></span>  <br/> |<span data-ttu-id="00ada-152">指示 "垃圾邮件" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-152">Indicates the URL of the junk email folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-153">searchfolders</span><span class="sxs-lookup"><span data-stu-id="00ada-153">searchfolders</span></span>  <br/> |<span data-ttu-id="00ada-154">指示搜索文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-154">Indicates the URL of the search folders.</span></span>  <br/> |
|<span data-ttu-id="00ada-155">语音邮件</span><span class="sxs-lookup"><span data-stu-id="00ada-155">voicemail</span></span>  <br/> |<span data-ttu-id="00ada-156">指示语音邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-156">Indicates the URL of the voice-mail folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-157">recoverableitemsroot</span><span class="sxs-lookup"><span data-stu-id="00ada-157">recoverableitemsroot</span></span>  <br/> |<span data-ttu-id="00ada-158">指示 "可恢复项目" 根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-158">Indicates the URL of the recoverable items root folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-159">recoverableitemsdeletions</span><span class="sxs-lookup"><span data-stu-id="00ada-159">recoverableitemsdeletions</span></span>  <br/> |<span data-ttu-id="00ada-160">指示 "已删除的可恢复项目" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-160">Indicates the URL of the deleted recoverable items folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-161">recoverableitemsversions</span><span class="sxs-lookup"><span data-stu-id="00ada-161">recoverableitemsversions</span></span>  <br/> |<span data-ttu-id="00ada-162">指示 "可恢复的项目版本" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-162">Indicates the URL of the recoverable item versions folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-163">recoverableitemspurges</span><span class="sxs-lookup"><span data-stu-id="00ada-163">recoverableitemspurges</span></span>  <br/> |<span data-ttu-id="00ada-164">指示清除的 "可恢复项目" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-164">Indicates the URL of the purged recoverable items folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-165">archiveroot</span><span class="sxs-lookup"><span data-stu-id="00ada-165">archiveroot</span></span>  <br/> |<span data-ttu-id="00ada-166">指示存档根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-166">Indicates the URL of the archive root folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-167">archivemsgfolderroot</span><span class="sxs-lookup"><span data-stu-id="00ada-167">archivemsgfolderroot</span></span>  <br/> |<span data-ttu-id="00ada-168">指示存档的邮件文件夹根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-168">Indicates the URL of the archived message folder root folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-169">archivedeleteditems</span><span class="sxs-lookup"><span data-stu-id="00ada-169">archivedeleteditems</span></span>  <br/> |<span data-ttu-id="00ada-170">指示存档的 "已删除邮件" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-170">Indicates the URL of the archived deleted items folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-171">archiverecoverableitemsroot</span><span class="sxs-lookup"><span data-stu-id="00ada-171">archiverecoverableitemsroot</span></span>  <br/> |<span data-ttu-id="00ada-172">指示已存档的 "可恢复项目" 根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-172">Indicates the URL of the archived recoverable items root folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-173">archiverecoverableitemsdeletions</span><span class="sxs-lookup"><span data-stu-id="00ada-173">archiverecoverableitemsdeletions</span></span>  <br/> |<span data-ttu-id="00ada-174">指示 "已存档的可恢复已删除邮件" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-174">Indicates the URL of the archived recoverable deleted items folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-175">archiverecoverableitemsversions</span><span class="sxs-lookup"><span data-stu-id="00ada-175">archiverecoverableitemsversions</span></span>  <br/> |<span data-ttu-id="00ada-176">指示存档的可恢复项目版本文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-176">Indicates the URL of the archived recoverable items versions folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-177">archiverecoverableitemspurges</span><span class="sxs-lookup"><span data-stu-id="00ada-177">archiverecoverableitemspurges</span></span>  <br/> |<span data-ttu-id="00ada-178">指示存档清除的 "可恢复的项目" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-178">Indicates the URL of the archived purged recoverable items folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-179">syncissues</span><span class="sxs-lookup"><span data-stu-id="00ada-179">syncissues</span></span>  <br/> |<span data-ttu-id="00ada-180">指示同步问题文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-180">Indicates the URL of the synchronization issues folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-181">conflicts</span><span class="sxs-lookup"><span data-stu-id="00ada-181">conflicts</span></span>  <br/> |<span data-ttu-id="00ada-182">指示 "冲突" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-182">Indicates the URL of the conflicts folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-183">localfailures</span><span class="sxs-lookup"><span data-stu-id="00ada-183">localfailures</span></span>  <br/> |<span data-ttu-id="00ada-184">指示本地故障文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-184">Indicates the URL of the local failures folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-185">serverfailures</span><span class="sxs-lookup"><span data-stu-id="00ada-185">serverfailures</span></span>  <br/> |<span data-ttu-id="00ada-186">指示 "服务器故障" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-186">Indicates the URL of the server failures folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-187">recipientcache</span><span class="sxs-lookup"><span data-stu-id="00ada-187">recipientcache</span></span>  <br/> |<span data-ttu-id="00ada-188">指示收件人缓存文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-188">Indicates the URL of the recipient cache folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-189">quickcontacts</span><span class="sxs-lookup"><span data-stu-id="00ada-189">quickcontacts</span></span>  <br/> |<span data-ttu-id="00ada-190">指示 "快速联系人" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-190">Indicates the URL of the quick contacts folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-191">conversationhistory</span><span class="sxs-lookup"><span data-stu-id="00ada-191">conversationhistory</span></span>  <br/> |<span data-ttu-id="00ada-192">指示对话历史记录文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-192">Indicates the URL of the conversation history folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-193">adminauditlogs</span><span class="sxs-lookup"><span data-stu-id="00ada-193">adminauditlogs</span></span>  <br/> |<span data-ttu-id="00ada-194">指示管理审核日志文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-194">Indicates the URL of the administrative audit log folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-195">todosearch</span><span class="sxs-lookup"><span data-stu-id="00ada-195">todosearch</span></span>  <br/> |<span data-ttu-id="00ada-196">指示 "要执行的搜索" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-196">Indicates the URL of the search to-do folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-197">mycontacts</span><span class="sxs-lookup"><span data-stu-id="00ada-197">mycontacts</span></span>  <br/> |<span data-ttu-id="00ada-198">指示 "我的联系人" 文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-198">Indicates the URL of the my contacts folder.</span></span>  <br/> |
|<span data-ttu-id="00ada-199">文件夹</span><span class="sxs-lookup"><span data-stu-id="00ada-199">directory</span></span>  <br/> |<span data-ttu-id="00ada-200">指示目录文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="00ada-200">Indicates a URL of the directory folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00ada-201">备注</span><span class="sxs-lookup"><span data-stu-id="00ada-201">Remarks</span></span>

<span data-ttu-id="00ada-202">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="00ada-202">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="00ada-203">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="00ada-203">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00ada-204">元素信息</span><span class="sxs-lookup"><span data-stu-id="00ada-204">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00ada-205">命名空间</span><span class="sxs-lookup"><span data-stu-id="00ada-205">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="00ada-206">架构名称</span><span class="sxs-lookup"><span data-stu-id="00ada-206">Schema Name</span></span>  <br/> |<span data-ttu-id="00ada-207">类型架构</span><span class="sxs-lookup"><span data-stu-id="00ada-207">Type schema</span></span>  <br/> |
|<span data-ttu-id="00ada-208">验证文件</span><span class="sxs-lookup"><span data-stu-id="00ada-208">Validation File</span></span>  <br/> |<span data-ttu-id="00ada-209">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="00ada-209">types.xsd</span></span>  <br/> |
|<span data-ttu-id="00ada-210">可以为空</span><span class="sxs-lookup"><span data-stu-id="00ada-210">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="00ada-211">另请参阅</span><span class="sxs-lookup"><span data-stu-id="00ada-211">See also</span></span>

- [<span data-ttu-id="00ada-212">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="00ada-212">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

