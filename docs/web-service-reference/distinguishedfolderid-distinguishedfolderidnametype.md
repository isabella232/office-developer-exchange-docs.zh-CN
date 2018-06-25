---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: DistinguishedFolderId 元素标识可以通过名称引用的文件夹。
ms.openlocfilehash: 1f5b97fc7ee7b93989762c26e4b979a8dfb884be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753958"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a><span data-ttu-id="69163-103">DistinguishedFolderId (DistinguishedFolderIdNameType)</span><span class="sxs-lookup"><span data-stu-id="69163-103">DistinguishedFolderId (DistinguishedFolderIdNameType)</span></span>

<span data-ttu-id="69163-104">**DistinguishedFolderId**元素标识可以通过名称引用的文件夹。</span><span class="sxs-lookup"><span data-stu-id="69163-104">The **DistinguishedFolderId** element identifies folders that can be referenced by name.</span></span> 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 <span data-ttu-id="69163-105">**DistinguishedFolderIdNameType**</span><span class="sxs-lookup"><span data-stu-id="69163-105">**DistinguishedFolderIdNameType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69163-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="69163-106">Attributes and elements</span></span>

<span data-ttu-id="69163-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="69163-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69163-108">属性</span><span class="sxs-lookup"><span data-stu-id="69163-108">Attributes</span></span>

<span data-ttu-id="69163-109">无。</span><span class="sxs-lookup"><span data-stu-id="69163-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69163-110">子元素</span><span class="sxs-lookup"><span data-stu-id="69163-110">Child elements</span></span>

<span data-ttu-id="69163-111">无</span><span class="sxs-lookup"><span data-stu-id="69163-111">None</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="69163-112">父元素</span><span class="sxs-lookup"><span data-stu-id="69163-112">Parent elements</span></span>

|<span data-ttu-id="69163-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="69163-113">**Element**</span></span>|<span data-ttu-id="69163-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="69163-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69163-115">Folder</span><span class="sxs-lookup"><span data-stu-id="69163-115">Folder</span></span>](folder.md) <br/> |<span data-ttu-id="69163-116">指定一般文件夹。</span><span class="sxs-lookup"><span data-stu-id="69163-116">Specifies a generic folder.</span></span>  <br/> |
|[<span data-ttu-id="69163-117">CalendarFolder</span><span class="sxs-lookup"><span data-stu-id="69163-117">CalendarFolder</span></span>](calendarfolder.md) <br/> |<span data-ttu-id="69163-118">指定日历文件夹。</span><span class="sxs-lookup"><span data-stu-id="69163-118">Specifies a calendar folder.</span></span>  <br/> |
|[<span data-ttu-id="69163-119">ContactsFolder</span><span class="sxs-lookup"><span data-stu-id="69163-119">ContactsFolder</span></span>](contactsfolder.md) <br/> |<span data-ttu-id="69163-120">指定联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="69163-120">Specifies a contacts folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69163-121">文本值</span><span class="sxs-lookup"><span data-stu-id="69163-121">Text value</span></span>

<span data-ttu-id="69163-122">**DistinguishedFolderId 元素的文本值**</span><span class="sxs-lookup"><span data-stu-id="69163-122">**DistinguishedFolderId element text values**</span></span>

|<span data-ttu-id="69163-123">**值**</span><span class="sxs-lookup"><span data-stu-id="69163-123">**Value**</span></span>|<span data-ttu-id="69163-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="69163-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69163-125">日历</span><span class="sxs-lookup"><span data-stu-id="69163-125">calendar</span></span>  <br/> |<span data-ttu-id="69163-126">指示日历文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-126">Indicates the URL of the calendar folder.</span></span>  <br/> |
|<span data-ttu-id="69163-127">contacts</span><span class="sxs-lookup"><span data-stu-id="69163-127">contacts</span></span>  <br/> |<span data-ttu-id="69163-128">指示联系人文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-128">Indicates the URL of the contacts folder.</span></span>  <br/> |
|<span data-ttu-id="69163-129">DeletedItems</span><span class="sxs-lookup"><span data-stu-id="69163-129">deleteditems</span></span>  <br/> |<span data-ttu-id="69163-130">指示已删除的邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-130">Indicates the URL of the deleted items folder.</span></span>  <br/> |
|<span data-ttu-id="69163-131">草稿</span><span class="sxs-lookup"><span data-stu-id="69163-131">drafts</span></span>  <br/> |<span data-ttu-id="69163-132">指示草稿文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-132">Indicates the URL of the drafts folder.</span></span>  <br/> |
|<span data-ttu-id="69163-133">收件箱</span><span class="sxs-lookup"><span data-stu-id="69163-133">inbox</span></span>  <br/> |<span data-ttu-id="69163-134">指示收件箱文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-134">Indicates the URL of the inbox folder.</span></span>  <br/> |
|<span data-ttu-id="69163-135">日记</span><span class="sxs-lookup"><span data-stu-id="69163-135">journal</span></span>  <br/> |<span data-ttu-id="69163-136">指示日记文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-136">Indicates the URL of the journal folder.</span></span>  <br/> |
|<span data-ttu-id="69163-137">notes</span><span class="sxs-lookup"><span data-stu-id="69163-137">notes</span></span>  <br/> |<span data-ttu-id="69163-138">指示便笺文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-138">Indicates the URL of the notes folder.</span></span>  <br/> |
|<span data-ttu-id="69163-139">发件箱</span><span class="sxs-lookup"><span data-stu-id="69163-139">outbox</span></span>  <br/> |<span data-ttu-id="69163-140">指示发件箱文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-140">Indicates the URL of the outbox folder.</span></span>  <br/> |
|<span data-ttu-id="69163-141">sentitems</span><span class="sxs-lookup"><span data-stu-id="69163-141">sentitems</span></span>  <br/> |<span data-ttu-id="69163-142">指示已发送的邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-142">Indicates the URL of the sent items folder.</span></span>  <br/> |
|<span data-ttu-id="69163-143">tasks</span><span class="sxs-lookup"><span data-stu-id="69163-143">tasks</span></span>  <br/> |<span data-ttu-id="69163-144">指示任务文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-144">Indicates the URL of the tasks folder.</span></span>  <br/> |
|<span data-ttu-id="69163-145">msgfolderroot</span><span class="sxs-lookup"><span data-stu-id="69163-145">msgfolderroot</span></span>  <br/> |<span data-ttu-id="69163-146">指示邮件根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-146">Indicates the URL of the message root folder.</span></span>  <br/> |
|<span data-ttu-id="69163-147">publicfoldersroot</span><span class="sxs-lookup"><span data-stu-id="69163-147">publicfoldersroot</span></span>  <br/> |<span data-ttu-id="69163-148">指示公用文件夹根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-148">Indicates the URL of the public folders root folder.</span></span>  <br/> |
|<span data-ttu-id="69163-149">root</span><span class="sxs-lookup"><span data-stu-id="69163-149">root</span></span>  <br/> |<span data-ttu-id="69163-150">指示的根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-150">Indicates the URL of the root folder.</span></span>  <br/> |
|<span data-ttu-id="69163-151">junkemail</span><span class="sxs-lookup"><span data-stu-id="69163-151">junkemail</span></span>  <br/> |<span data-ttu-id="69163-152">指示垃圾邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-152">Indicates the URL of the junk email folder.</span></span>  <br/> |
|<span data-ttu-id="69163-153">searchfolders</span><span class="sxs-lookup"><span data-stu-id="69163-153">searchfolders</span></span>  <br/> |<span data-ttu-id="69163-154">指示搜索文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-154">Indicates the URL of the search folders.</span></span>  <br/> |
|<span data-ttu-id="69163-155">语音邮件</span><span class="sxs-lookup"><span data-stu-id="69163-155">voicemail</span></span>  <br/> |<span data-ttu-id="69163-156">指示语音邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-156">Indicates the URL of the voice-mail folder.</span></span>  <br/> |
|<span data-ttu-id="69163-157">recoverableitemsroot</span><span class="sxs-lookup"><span data-stu-id="69163-157">recoverableitemsroot</span></span>  <br/> |<span data-ttu-id="69163-158">指示可恢复邮件根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-158">Indicates the URL of the recoverable items root folder.</span></span>  <br/> |
|<span data-ttu-id="69163-159">recoverableitemsdeletions</span><span class="sxs-lookup"><span data-stu-id="69163-159">recoverableitemsdeletions</span></span>  <br/> |<span data-ttu-id="69163-160">指示已删除的可恢复邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-160">Indicates the URL of the deleted recoverable items folder.</span></span>  <br/> |
|<span data-ttu-id="69163-161">recoverableitemsversions</span><span class="sxs-lookup"><span data-stu-id="69163-161">recoverableitemsversions</span></span>  <br/> |<span data-ttu-id="69163-162">指示可恢复项目版本文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-162">Indicates the URL of the recoverable item versions folder.</span></span>  <br/> |
|<span data-ttu-id="69163-163">recoverableitemspurges</span><span class="sxs-lookup"><span data-stu-id="69163-163">recoverableitemspurges</span></span>  <br/> |<span data-ttu-id="69163-164">指示清除可恢复邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-164">Indicates the URL of the purged recoverable items folder.</span></span>  <br/> |
|<span data-ttu-id="69163-165">archiveroot</span><span class="sxs-lookup"><span data-stu-id="69163-165">archiveroot</span></span>  <br/> |<span data-ttu-id="69163-166">指示存档根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-166">Indicates the URL of the archive root folder.</span></span>  <br/> |
|<span data-ttu-id="69163-167">archivemsgfolderroot</span><span class="sxs-lookup"><span data-stu-id="69163-167">archivemsgfolderroot</span></span>  <br/> |<span data-ttu-id="69163-168">指示已存档的邮件文件夹根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-168">Indicates the URL of the archived message folder root folder.</span></span>  <br/> |
|<span data-ttu-id="69163-169">archivedeleteditems</span><span class="sxs-lookup"><span data-stu-id="69163-169">archivedeleteditems</span></span>  <br/> |<span data-ttu-id="69163-170">指示已存档的已删除的邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-170">Indicates the URL of the archived deleted items folder.</span></span>  <br/> |
|<span data-ttu-id="69163-171">archiverecoverableitemsroot</span><span class="sxs-lookup"><span data-stu-id="69163-171">archiverecoverableitemsroot</span></span>  <br/> |<span data-ttu-id="69163-172">指示已存档的可恢复项目根文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-172">Indicates the URL of the archived recoverable items root folder.</span></span>  <br/> |
|<span data-ttu-id="69163-173">archiverecoverableitemsdeletions</span><span class="sxs-lookup"><span data-stu-id="69163-173">archiverecoverableitemsdeletions</span></span>  <br/> |<span data-ttu-id="69163-174">指示存档可恢复已删除的邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-174">Indicates the URL of the archived recoverable deleted items folder.</span></span>  <br/> |
|<span data-ttu-id="69163-175">archiverecoverableitemsversions</span><span class="sxs-lookup"><span data-stu-id="69163-175">archiverecoverableitemsversions</span></span>  <br/> |<span data-ttu-id="69163-176">指示已存档的可恢复项目版本文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-176">Indicates the URL of the archived recoverable items versions folder.</span></span>  <br/> |
|<span data-ttu-id="69163-177">archiverecoverableitemspurges</span><span class="sxs-lookup"><span data-stu-id="69163-177">archiverecoverableitemspurges</span></span>  <br/> |<span data-ttu-id="69163-178">指示存档清除可恢复邮件文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-178">Indicates the URL of the archived purged recoverable items folder.</span></span>  <br/> |
|<span data-ttu-id="69163-179">syncissues</span><span class="sxs-lookup"><span data-stu-id="69163-179">syncissues</span></span>  <br/> |<span data-ttu-id="69163-180">指示同步问题文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-180">Indicates the URL of the synchronization issues folder.</span></span>  <br/> |
|<span data-ttu-id="69163-181">冲突</span><span class="sxs-lookup"><span data-stu-id="69163-181">conflicts</span></span>  <br/> |<span data-ttu-id="69163-182">指示冲突文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-182">Indicates the URL of the conflicts folder.</span></span>  <br/> |
|<span data-ttu-id="69163-183">localfailures</span><span class="sxs-lookup"><span data-stu-id="69163-183">localfailures</span></span>  <br/> |<span data-ttu-id="69163-184">指示本地故障文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-184">Indicates the URL of the local failures folder.</span></span>  <br/> |
|<span data-ttu-id="69163-185">serverfailures</span><span class="sxs-lookup"><span data-stu-id="69163-185">serverfailures</span></span>  <br/> |<span data-ttu-id="69163-186">指示服务器故障文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-186">Indicates the URL of the server failures folder.</span></span>  <br/> |
|<span data-ttu-id="69163-187">recipientcache</span><span class="sxs-lookup"><span data-stu-id="69163-187">recipientcache</span></span>  <br/> |<span data-ttu-id="69163-188">指示收件人缓存文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-188">Indicates the URL of the recipient cache folder.</span></span>  <br/> |
|<span data-ttu-id="69163-189">quickcontacts</span><span class="sxs-lookup"><span data-stu-id="69163-189">quickcontacts</span></span>  <br/> |<span data-ttu-id="69163-190">指示快速联系人文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-190">Indicates the URL of the quick contacts folder.</span></span>  <br/> |
|<span data-ttu-id="69163-191">conversationhistory</span><span class="sxs-lookup"><span data-stu-id="69163-191">conversationhistory</span></span>  <br/> |<span data-ttu-id="69163-192">指示对话历史记录文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-192">Indicates the URL of the conversation history folder.</span></span>  <br/> |
|<span data-ttu-id="69163-193">adminauditlogs</span><span class="sxs-lookup"><span data-stu-id="69163-193">adminauditlogs</span></span>  <br/> |<span data-ttu-id="69163-194">指示管理审核日志的文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-194">Indicates the URL of the administrative audit log folder.</span></span>  <br/> |
|<span data-ttu-id="69163-195">todosearch</span><span class="sxs-lookup"><span data-stu-id="69163-195">todosearch</span></span>  <br/> |<span data-ttu-id="69163-196">指示搜索待办事项文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-196">Indicates the URL of the search to-do folder.</span></span>  <br/> |
|<span data-ttu-id="69163-197">mycontacts</span><span class="sxs-lookup"><span data-stu-id="69163-197">mycontacts</span></span>  <br/> |<span data-ttu-id="69163-198">指示的 URL 联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="69163-198">Indicates the URL of the my contacts folder.</span></span>  <br/> |
|<span data-ttu-id="69163-199">目录</span><span class="sxs-lookup"><span data-stu-id="69163-199">directory</span></span>  <br/> |<span data-ttu-id="69163-200">指示目录文件夹的 URL。</span><span class="sxs-lookup"><span data-stu-id="69163-200">Indicates a URL of the directory folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69163-201">备注</span><span class="sxs-lookup"><span data-stu-id="69163-201">Remarks</span></span>

<span data-ttu-id="69163-202">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="69163-202">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="69163-203">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="69163-203">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69163-204">元素信息</span><span class="sxs-lookup"><span data-stu-id="69163-204">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69163-205">命名空间</span><span class="sxs-lookup"><span data-stu-id="69163-205">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69163-206">架构名称</span><span class="sxs-lookup"><span data-stu-id="69163-206">Schema Name</span></span>  <br/> |<span data-ttu-id="69163-207">类型架构</span><span class="sxs-lookup"><span data-stu-id="69163-207">Type schema</span></span>  <br/> |
|<span data-ttu-id="69163-208">验证文件</span><span class="sxs-lookup"><span data-stu-id="69163-208">Validation File</span></span>  <br/> |<span data-ttu-id="69163-209">types.xsd</span><span class="sxs-lookup"><span data-stu-id="69163-209">types.xsd</span></span>  <br/> |
|<span data-ttu-id="69163-210">可以为空</span><span class="sxs-lookup"><span data-stu-id="69163-210">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="69163-211">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69163-211">See also</span></span>

- [<span data-ttu-id="69163-212">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="69163-212">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

