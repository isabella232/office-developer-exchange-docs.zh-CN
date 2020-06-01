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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462645"
---
# <a name="findconversation"></a><span data-ttu-id="fc5b4-103">FindConversation</span><span class="sxs-lookup"><span data-stu-id="fc5b4-103">FindConversation</span></span>

<span data-ttu-id="fc5b4-104">**FindConversation**元素定义在邮箱中查找对话的请求。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-104">The **FindConversation** element defines a request to find conversations in a mailbox.</span></span> 
  
[<span data-ttu-id="fc5b4-105">FindConversation</span><span class="sxs-lookup"><span data-stu-id="fc5b4-105">FindConversation</span></span>](findconversation.md)
  
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

 <span data-ttu-id="fc5b4-106">**FindConversationType**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-106">**FindConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fc5b4-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fc5b4-107">Attributes and elements</span></span>

<span data-ttu-id="fc5b4-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc5b4-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="fc5b4-109">Attributes</span></span>

****

|<span data-ttu-id="fc5b4-110">**属性**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-110">**Attribute**</span></span>|<span data-ttu-id="fc5b4-111">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc5b4-112">遍历</span><span class="sxs-lookup"><span data-stu-id="fc5b4-112">Traversal</span></span>  <br/> |<span data-ttu-id="fc5b4-113">标识子树遍历的类型。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-113">Identifies the types of sub-tree traversal.</span></span> <span data-ttu-id="fc5b4-114">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-114">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-115">ViewFilter</span><span class="sxs-lookup"><span data-stu-id="fc5b4-115">ViewFilter</span></span>  <br/> |<span data-ttu-id="fc5b4-116">标识类型视图筛选器。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-116">Identifies the types view filters.</span></span> <span data-ttu-id="fc5b4-117">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-117">This attribute is optional.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="fc5b4-118">遍历属性值</span><span class="sxs-lookup"><span data-stu-id="fc5b4-118">Traversal attribute values</span></span>

****

|<span data-ttu-id="fc5b4-119">**值**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-119">**Value**</span></span>|<span data-ttu-id="fc5b4-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc5b4-121">浅</span><span class="sxs-lookup"><span data-stu-id="fc5b4-121">Shallow</span></span>  <br/> |<span data-ttu-id="fc5b4-122">指示浅遍历。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-122">Indicates a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-123">深</span><span class="sxs-lookup"><span data-stu-id="fc5b4-123">Deep</span></span>  <br/> |<span data-ttu-id="fc5b4-124">指示深度遍历。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-124">Indicates a deep traversal.</span></span>  <br/> |
   
#### <a name="viewfilter-attribute-values"></a><span data-ttu-id="fc5b4-125">ViewFilter 属性值</span><span class="sxs-lookup"><span data-stu-id="fc5b4-125">ViewFilter attribute values</span></span>

****

|<span data-ttu-id="fc5b4-126">**值**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-126">**Value**</span></span>|<span data-ttu-id="fc5b4-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc5b4-128">所有</span><span class="sxs-lookup"><span data-stu-id="fc5b4-128">All</span></span>  <br/> |<span data-ttu-id="fc5b4-129">查找所有对话。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-129">Find all conversations.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-130">带</span><span class="sxs-lookup"><span data-stu-id="fc5b4-130">Flagged</span></span>  <br/> |<span data-ttu-id="fc5b4-131">查找已标记的对话。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-131">Find flagged conversations.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-132">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="fc5b4-132">HasAttachment</span></span>  <br/> |<span data-ttu-id="fc5b4-133">查找有关附件的对话。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-133">Find conversations with attachments.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-134">ToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="fc5b4-134">ToOrCcMe</span></span>  <br/> |<span data-ttu-id="fc5b4-135">查找解决或抄送给我的对话。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-135">Find conversations addressed or cc'd to me.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-136">未读</span><span class="sxs-lookup"><span data-stu-id="fc5b4-136">Unread</span></span>  <br/> |<span data-ttu-id="fc5b4-137">查找未读对话。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-137">Find unread conversations.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-138">TaskActive</span><span class="sxs-lookup"><span data-stu-id="fc5b4-138">TaskActive</span></span>  <br/> |<span data-ttu-id="fc5b4-139">查找活动任务。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-139">Find active tasks.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-140">TaskOverdue</span><span class="sxs-lookup"><span data-stu-id="fc5b4-140">TaskOverdue</span></span>  <br/> |<span data-ttu-id="fc5b4-141">查找过期的任务。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-141">Find overdue tasks.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-142">TaskCompleted</span><span class="sxs-lookup"><span data-stu-id="fc5b4-142">TaskCompleted</span></span>  <br/> |<span data-ttu-id="fc5b4-143">查找已完成的任务。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-143">Find completed tasks.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-144">NoClutter</span><span class="sxs-lookup"><span data-stu-id="fc5b4-144">NoClutter</span></span>  <br/> |<span data-ttu-id="fc5b4-145">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-145">For internal use only.</span></span>  <br/> |
|<span data-ttu-id="fc5b4-146">混乱邮件</span><span class="sxs-lookup"><span data-stu-id="fc5b4-146">Clutter</span></span>  <br/> |<span data-ttu-id="fc5b4-147">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-147">For internal use only.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fc5b4-148">子元素</span><span class="sxs-lookup"><span data-stu-id="fc5b4-148">Child elements</span></span>

|<span data-ttu-id="fc5b4-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-149">**Element**</span></span>|<span data-ttu-id="fc5b4-150">**描述**</span><span class="sxs-lookup"><span data-stu-id="fc5b4-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc5b4-151">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="fc5b4-151">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="fc5b4-152">介绍如何返回分页对话信息。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-152">Describes how paged conversation information is returned.</span></span>  <br/> |
|[<span data-ttu-id="fc5b4-153">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="fc5b4-153">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="fc5b4-154">指定用于标识搜索的结束的条件、搜索的起始索引、要返回的最大项数以及**FindItem**或**FindConversation**搜索的搜索说明。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-154">Specifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span>  <br/> |
|[<span data-ttu-id="fc5b4-155">SortOrder</span><span class="sxs-lookup"><span data-stu-id="fc5b4-155">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="fc5b4-156">定义如何在[FindConversation 操作](findconversation-operation.md)请求中对项目进行排序。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-156">Defines how items are sorted in a [FindConversation operation](findconversation-operation.md) request.</span></span> <span data-ttu-id="fc5b4-157">**对话： LastDeliveryTime**属性是在使用**FindConversation**操作时，支持排序的唯一属性。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-157">The **conversation:LastDeliveryTime** property is the only property that is supported for sorting when the **FindConversation** operation is used.</span></span>  <br/> |
|[<span data-ttu-id="fc5b4-158">ParentFolderId （TargetFolderIdType）</span><span class="sxs-lookup"><span data-stu-id="fc5b4-158">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="fc5b4-159">标识用于搜索对话的文件夹。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-159">Identifies the folder to search for conversations.</span></span>  <br/> |
|[<span data-ttu-id="fc5b4-160">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="fc5b4-160">MailboxScope</span></span>](mailboxscope.md) <br/> |<span data-ttu-id="fc5b4-161">指定对话的搜索或获取是否应跨越主邮箱、存档邮箱或同时位于主邮箱和存档邮箱中。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-161">Specifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="fc5b4-162">QueryString （QueryStringType）</span><span class="sxs-lookup"><span data-stu-id="fc5b4-162">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="fc5b4-163">指定基于高级查询语法（AQS）的邮箱查询字符串。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-163">Specifies a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
|[<span data-ttu-id="fc5b4-164">ConversationShape</span><span class="sxs-lookup"><span data-stu-id="fc5b4-164">ConversationShape</span></span>](conversationshape.md) <br/> |<span data-ttu-id="fc5b4-165">标识设置为在[FindConversation 操作](findconversation-operation.md)响应中返回的属性。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-165">Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fc5b4-166">父元素</span><span class="sxs-lookup"><span data-stu-id="fc5b4-166">Parent elements</span></span>

<span data-ttu-id="fc5b4-167">无。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fc5b4-168">说明</span><span class="sxs-lookup"><span data-stu-id="fc5b4-168">Remarks</span></span>

<span data-ttu-id="fc5b4-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fc5b4-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc5b4-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="fc5b4-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc5b4-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="fc5b4-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fc5b4-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="fc5b4-172">Schema Name</span></span>  <br/> |<span data-ttu-id="fc5b4-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="fc5b4-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fc5b4-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="fc5b4-174">Validation File</span></span>  <br/> |<span data-ttu-id="fc5b4-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fc5b4-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fc5b4-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="fc5b4-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="fc5b4-177">False</span><span class="sxs-lookup"><span data-stu-id="fc5b4-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc5b4-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fc5b4-178">See also</span></span>



[<span data-ttu-id="fc5b4-179">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="fc5b4-179">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="fc5b4-180">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fc5b4-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="fc5b4-181">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="fc5b4-181">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

