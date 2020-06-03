---
title: FindConversation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindConversation
api_type:
- schema
ms.assetid: 94b7083c-60cf-478b-a9af-a88f7acb30fb
description: FindConversation 元素定义在邮箱中查找对话的请求。
ms.openlocfilehash: 98d692132ed9375d981c95d24600b0e2c4b1d8c1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462645"
---
# <a name="findconversation"></a><span data-ttu-id="1b2af-103">FindConversation</span><span class="sxs-lookup"><span data-stu-id="1b2af-103">FindConversation</span></span>

<span data-ttu-id="1b2af-104">**FindConversation**元素定义在邮箱中查找对话的请求。</span><span class="sxs-lookup"><span data-stu-id="1b2af-104">The **FindConversation** element defines a request to find conversations in a mailbox.</span></span> 
  
[<span data-ttu-id="1b2af-105">FindConversation</span><span class="sxs-lookup"><span data-stu-id="1b2af-105">FindConversation</span></span>](findconversation.md)
  
```XML
<FindConversation Traversal="" ViewFilter="">
   <IndexedPageItemView/>
   <SeekToConditionPageItemView/>
   <SortOrder/>
   <ParentFolderId/>
   <MailboxScope/>
   <QueryString/>
   <ConversationShape/>
</FindConversation>
```

 <span data-ttu-id="1b2af-106">**FindConversationType**</span><span class="sxs-lookup"><span data-stu-id="1b2af-106">**FindConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b2af-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1b2af-107">Attributes and elements</span></span>

<span data-ttu-id="1b2af-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1b2af-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b2af-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="1b2af-109">Attributes</span></span>

****

|<span data-ttu-id="1b2af-110">**属性**</span><span class="sxs-lookup"><span data-stu-id="1b2af-110">**Attribute**</span></span>|<span data-ttu-id="1b2af-111">**说明**</span><span class="sxs-lookup"><span data-stu-id="1b2af-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b2af-112">遍历</span><span class="sxs-lookup"><span data-stu-id="1b2af-112">Traversal</span></span>  <br/> |<span data-ttu-id="1b2af-113">标识子树遍历的类型。</span><span class="sxs-lookup"><span data-stu-id="1b2af-113">Identifies the types of sub-tree traversal.</span></span> <span data-ttu-id="1b2af-114">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="1b2af-114">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="1b2af-115">ViewFilter</span><span class="sxs-lookup"><span data-stu-id="1b2af-115">ViewFilter</span></span>  <br/> |<span data-ttu-id="1b2af-116">标识类型视图筛选器。</span><span class="sxs-lookup"><span data-stu-id="1b2af-116">Identifies the types view filters.</span></span> <span data-ttu-id="1b2af-117">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="1b2af-117">This attribute is optional.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="1b2af-118">遍历属性值</span><span class="sxs-lookup"><span data-stu-id="1b2af-118">Traversal attribute values</span></span>

****

|<span data-ttu-id="1b2af-119">**值**</span><span class="sxs-lookup"><span data-stu-id="1b2af-119">**Value**</span></span>|<span data-ttu-id="1b2af-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="1b2af-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b2af-121">浅</span><span class="sxs-lookup"><span data-stu-id="1b2af-121">Shallow</span></span>  <br/> |<span data-ttu-id="1b2af-122">指示浅遍历。</span><span class="sxs-lookup"><span data-stu-id="1b2af-122">Indicates a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="1b2af-123">深</span><span class="sxs-lookup"><span data-stu-id="1b2af-123">Deep</span></span>  <br/> |<span data-ttu-id="1b2af-124">指示深度遍历。</span><span class="sxs-lookup"><span data-stu-id="1b2af-124">Indicates a deep traversal.</span></span>  <br/> |
   
#### <a name="viewfilter-attribute-values"></a><span data-ttu-id="1b2af-125">ViewFilter 属性值</span><span class="sxs-lookup"><span data-stu-id="1b2af-125">ViewFilter attribute values</span></span>

****

|<span data-ttu-id="1b2af-126">**值**</span><span class="sxs-lookup"><span data-stu-id="1b2af-126">**Value**</span></span>|<span data-ttu-id="1b2af-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="1b2af-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b2af-128">所有</span><span class="sxs-lookup"><span data-stu-id="1b2af-128">All</span></span>  <br/> |<span data-ttu-id="1b2af-129">查找所有对话。</span><span class="sxs-lookup"><span data-stu-id="1b2af-129">Find all conversations.</span></span>  <br/> |
|<span data-ttu-id="1b2af-130">带</span><span class="sxs-lookup"><span data-stu-id="1b2af-130">Flagged</span></span>  <br/> |<span data-ttu-id="1b2af-131">查找已标记的对话。</span><span class="sxs-lookup"><span data-stu-id="1b2af-131">Find flagged conversations.</span></span>  <br/> |
|<span data-ttu-id="1b2af-132">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="1b2af-132">HasAttachment</span></span>  <br/> |<span data-ttu-id="1b2af-133">查找有关附件的对话。</span><span class="sxs-lookup"><span data-stu-id="1b2af-133">Find conversations with attachments.</span></span>  <br/> |
|<span data-ttu-id="1b2af-134">ToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="1b2af-134">ToOrCcMe</span></span>  <br/> |<span data-ttu-id="1b2af-135">查找解决或抄送给我的对话。</span><span class="sxs-lookup"><span data-stu-id="1b2af-135">Find conversations addressed or cc'd to me.</span></span>  <br/> |
|<span data-ttu-id="1b2af-136">未读</span><span class="sxs-lookup"><span data-stu-id="1b2af-136">Unread</span></span>  <br/> |<span data-ttu-id="1b2af-137">查找未读对话。</span><span class="sxs-lookup"><span data-stu-id="1b2af-137">Find unread conversations.</span></span>  <br/> |
|<span data-ttu-id="1b2af-138">TaskActive</span><span class="sxs-lookup"><span data-stu-id="1b2af-138">TaskActive</span></span>  <br/> |<span data-ttu-id="1b2af-139">查找活动任务。</span><span class="sxs-lookup"><span data-stu-id="1b2af-139">Find active tasks.</span></span>  <br/> |
|<span data-ttu-id="1b2af-140">TaskOverdue</span><span class="sxs-lookup"><span data-stu-id="1b2af-140">TaskOverdue</span></span>  <br/> |<span data-ttu-id="1b2af-141">查找过期的任务。</span><span class="sxs-lookup"><span data-stu-id="1b2af-141">Find overdue tasks.</span></span>  <br/> |
|<span data-ttu-id="1b2af-142">TaskCompleted</span><span class="sxs-lookup"><span data-stu-id="1b2af-142">TaskCompleted</span></span>  <br/> |<span data-ttu-id="1b2af-143">查找已完成的任务。</span><span class="sxs-lookup"><span data-stu-id="1b2af-143">Find completed tasks.</span></span>  <br/> |
|<span data-ttu-id="1b2af-144">NoClutter</span><span class="sxs-lookup"><span data-stu-id="1b2af-144">NoClutter</span></span>  <br/> |<span data-ttu-id="1b2af-145">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="1b2af-145">For internal use only.</span></span>  <br/> |
|<span data-ttu-id="1b2af-146">混乱邮件</span><span class="sxs-lookup"><span data-stu-id="1b2af-146">Clutter</span></span>  <br/> |<span data-ttu-id="1b2af-147">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="1b2af-147">For internal use only.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1b2af-148">子元素</span><span class="sxs-lookup"><span data-stu-id="1b2af-148">Child elements</span></span>

|<span data-ttu-id="1b2af-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="1b2af-149">**Element**</span></span>|<span data-ttu-id="1b2af-150">**描述**</span><span class="sxs-lookup"><span data-stu-id="1b2af-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1b2af-151">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="1b2af-151">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="1b2af-152">介绍如何返回分页对话信息。</span><span class="sxs-lookup"><span data-stu-id="1b2af-152">Describes how paged conversation information is returned.</span></span>  <br/> |
|[<span data-ttu-id="1b2af-153">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="1b2af-153">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="1b2af-154">指定用于标识搜索的结束的条件、搜索的起始索引、要返回的最大项数以及**FindItem**或**FindConversation**搜索的搜索说明。</span><span class="sxs-lookup"><span data-stu-id="1b2af-154">Specifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span>  <br/> |
|[<span data-ttu-id="1b2af-155">SortOrder</span><span class="sxs-lookup"><span data-stu-id="1b2af-155">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="1b2af-156">定义如何在[FindConversation 操作](findconversation-operation.md)请求中对项目进行排序。</span><span class="sxs-lookup"><span data-stu-id="1b2af-156">Defines how items are sorted in a [FindConversation operation](findconversation-operation.md) request.</span></span> <span data-ttu-id="1b2af-157">**对话： LastDeliveryTime**属性是在使用**FindConversation**操作时，支持排序的唯一属性。</span><span class="sxs-lookup"><span data-stu-id="1b2af-157">The **conversation:LastDeliveryTime** property is the only property that is supported for sorting when the **FindConversation** operation is used.</span></span>  <br/> |
|[<span data-ttu-id="1b2af-158">ParentFolderId （TargetFolderIdType）</span><span class="sxs-lookup"><span data-stu-id="1b2af-158">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="1b2af-159">标识用于搜索对话的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1b2af-159">Identifies the folder to search for conversations.</span></span>  <br/> |
|[<span data-ttu-id="1b2af-160">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="1b2af-160">MailboxScope</span></span>](mailboxscope.md) <br/> |<span data-ttu-id="1b2af-161">指定对话的搜索或获取是否应跨越主邮箱、存档邮箱或同时位于主邮箱和存档邮箱中。</span><span class="sxs-lookup"><span data-stu-id="1b2af-161">Specifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="1b2af-162">QueryString （QueryStringType）</span><span class="sxs-lookup"><span data-stu-id="1b2af-162">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="1b2af-163">指定基于高级查询语法（AQS）的邮箱查询字符串。</span><span class="sxs-lookup"><span data-stu-id="1b2af-163">Specifies a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
|[<span data-ttu-id="1b2af-164">ConversationShape</span><span class="sxs-lookup"><span data-stu-id="1b2af-164">ConversationShape</span></span>](conversationshape.md) <br/> |<span data-ttu-id="1b2af-165">标识设置为在[FindConversation 操作](findconversation-operation.md)响应中返回的属性。</span><span class="sxs-lookup"><span data-stu-id="1b2af-165">Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1b2af-166">父元素</span><span class="sxs-lookup"><span data-stu-id="1b2af-166">Parent elements</span></span>

<span data-ttu-id="1b2af-167">无。</span><span class="sxs-lookup"><span data-stu-id="1b2af-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1b2af-168">说明</span><span class="sxs-lookup"><span data-stu-id="1b2af-168">Remarks</span></span>

<span data-ttu-id="1b2af-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1b2af-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b2af-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="1b2af-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b2af-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="1b2af-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1b2af-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="1b2af-172">Schema Name</span></span>  <br/> |<span data-ttu-id="1b2af-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="1b2af-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1b2af-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="1b2af-174">Validation File</span></span>  <br/> |<span data-ttu-id="1b2af-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1b2af-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1b2af-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="1b2af-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="1b2af-177">False</span><span class="sxs-lookup"><span data-stu-id="1b2af-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1b2af-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1b2af-178">See also</span></span>



[<span data-ttu-id="1b2af-179">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="1b2af-179">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="1b2af-180">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1b2af-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1b2af-181">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="1b2af-181">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

