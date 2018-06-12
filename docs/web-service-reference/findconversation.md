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
description: FindConversation 元素定义查找邮箱中的对话的请求。
ms.openlocfilehash: 990e15f468f836d51977329c524acb439014da95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754323"
---
# <a name="findconversation"></a><span data-ttu-id="9db5a-103">FindConversation</span><span class="sxs-lookup"><span data-stu-id="9db5a-103">FindConversation</span></span>

<span data-ttu-id="9db5a-104">**FindConversation**元素定义查找邮箱中的对话的请求。</span><span class="sxs-lookup"><span data-stu-id="9db5a-104">The **FindConversation** element defines a request to find conversations in a mailbox.</span></span> 
  
[<span data-ttu-id="9db5a-105">FindConversation</span><span class="sxs-lookup"><span data-stu-id="9db5a-105">FindConversation</span></span>](findconversation.md)
  
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

 <span data-ttu-id="9db5a-106">**FindConversationType**</span><span class="sxs-lookup"><span data-stu-id="9db5a-106">**FindConversationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9db5a-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9db5a-107">Attributes and elements</span></span>

<span data-ttu-id="9db5a-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9db5a-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9db5a-109">属性</span><span class="sxs-lookup"><span data-stu-id="9db5a-109">Attributes</span></span>

****

|<span data-ttu-id="9db5a-110">**属性**</span><span class="sxs-lookup"><span data-stu-id="9db5a-110">**Attribute**</span></span>|<span data-ttu-id="9db5a-111">**说明**</span><span class="sxs-lookup"><span data-stu-id="9db5a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9db5a-112">遍历</span><span class="sxs-lookup"><span data-stu-id="9db5a-112">Traversal</span></span>  <br/> |<span data-ttu-id="9db5a-113">标识子树遍历的类型。</span><span class="sxs-lookup"><span data-stu-id="9db5a-113">Identifies the types of sub-tree traversal.</span></span> <span data-ttu-id="9db5a-114">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="9db5a-114">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="9db5a-115">过滤</span><span class="sxs-lookup"><span data-stu-id="9db5a-115">ViewFilter</span></span>  <br/> |<span data-ttu-id="9db5a-116">标识类型视图筛选器。</span><span class="sxs-lookup"><span data-stu-id="9db5a-116">Identifies the types view filters.</span></span> <span data-ttu-id="9db5a-117">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="9db5a-117">This attribute is optional.</span></span>  <br/> |
   
#### <a name="traversal-attribute-values"></a><span data-ttu-id="9db5a-118">遍历属性值</span><span class="sxs-lookup"><span data-stu-id="9db5a-118">Traversal attribute values</span></span>

****

|<span data-ttu-id="9db5a-119">**值**</span><span class="sxs-lookup"><span data-stu-id="9db5a-119">**Value**</span></span>|<span data-ttu-id="9db5a-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="9db5a-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9db5a-121">浅</span><span class="sxs-lookup"><span data-stu-id="9db5a-121">Shallow</span></span>  <br/> |<span data-ttu-id="9db5a-122">指示浅遍历。</span><span class="sxs-lookup"><span data-stu-id="9db5a-122">Indicates a shallow traversal.</span></span>  <br/> |
|<span data-ttu-id="9db5a-123">深</span><span class="sxs-lookup"><span data-stu-id="9db5a-123">Deep</span></span>  <br/> |<span data-ttu-id="9db5a-124">指示遍历。</span><span class="sxs-lookup"><span data-stu-id="9db5a-124">Indicates a deep traversal.</span></span>  <br/> |
   
#### <a name="viewfilter-attribute-values"></a><span data-ttu-id="9db5a-125">过滤属性值</span><span class="sxs-lookup"><span data-stu-id="9db5a-125">ViewFilter attribute values</span></span>

****

|<span data-ttu-id="9db5a-126">**值**</span><span class="sxs-lookup"><span data-stu-id="9db5a-126">**Value**</span></span>|<span data-ttu-id="9db5a-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="9db5a-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9db5a-128">所有</span><span class="sxs-lookup"><span data-stu-id="9db5a-128">All</span></span>  <br/> |<span data-ttu-id="9db5a-129">查找所有对话。</span><span class="sxs-lookup"><span data-stu-id="9db5a-129">Find all conversations.</span></span>  <br/> |
|<span data-ttu-id="9db5a-130">标记</span><span class="sxs-lookup"><span data-stu-id="9db5a-130">Flagged</span></span>  <br/> |<span data-ttu-id="9db5a-131">查找已标记的对话。</span><span class="sxs-lookup"><span data-stu-id="9db5a-131">Find flagged conversations.</span></span>  <br/> |
|<span data-ttu-id="9db5a-132">HasAttachment</span><span class="sxs-lookup"><span data-stu-id="9db5a-132">HasAttachment</span></span>  <br/> |<span data-ttu-id="9db5a-133">查找与附件的对话。</span><span class="sxs-lookup"><span data-stu-id="9db5a-133">Find conversations with attachments.</span></span>  <br/> |
|<span data-ttu-id="9db5a-134">ToOrCcMe</span><span class="sxs-lookup"><span data-stu-id="9db5a-134">ToOrCcMe</span></span>  <br/> |<span data-ttu-id="9db5a-135">发送的对话或抄送将我的查找。</span><span class="sxs-lookup"><span data-stu-id="9db5a-135">Find conversations addressed or cc'd to me.</span></span>  <br/> |
|<span data-ttu-id="9db5a-136">Unread</span><span class="sxs-lookup"><span data-stu-id="9db5a-136">Unread</span></span>  <br/> |<span data-ttu-id="9db5a-137">查找未读的对话。</span><span class="sxs-lookup"><span data-stu-id="9db5a-137">Find unread conversations.</span></span>  <br/> |
|<span data-ttu-id="9db5a-138">TaskActive</span><span class="sxs-lookup"><span data-stu-id="9db5a-138">TaskActive</span></span>  <br/> |<span data-ttu-id="9db5a-139">了解活动的任务。</span><span class="sxs-lookup"><span data-stu-id="9db5a-139">Find active tasks.</span></span>  <br/> |
|<span data-ttu-id="9db5a-140">TaskOverdue</span><span class="sxs-lookup"><span data-stu-id="9db5a-140">TaskOverdue</span></span>  <br/> |<span data-ttu-id="9db5a-141">查找过期任务。</span><span class="sxs-lookup"><span data-stu-id="9db5a-141">Find overdue tasks.</span></span>  <br/> |
|<span data-ttu-id="9db5a-142">TaskCompleted</span><span class="sxs-lookup"><span data-stu-id="9db5a-142">TaskCompleted</span></span>  <br/> |<span data-ttu-id="9db5a-143">查找已完成的任务。</span><span class="sxs-lookup"><span data-stu-id="9db5a-143">Find completed tasks.</span></span>  <br/> |
|<span data-ttu-id="9db5a-144">NoClutter</span><span class="sxs-lookup"><span data-stu-id="9db5a-144">NoClutter</span></span>  <br/> |<span data-ttu-id="9db5a-145">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="9db5a-145">For internal use only.</span></span>  <br/> |
|<span data-ttu-id="9db5a-146">混乱</span><span class="sxs-lookup"><span data-stu-id="9db5a-146">Clutter</span></span>  <br/> |<span data-ttu-id="9db5a-147">仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="9db5a-147">For internal use only.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9db5a-148">子元素</span><span class="sxs-lookup"><span data-stu-id="9db5a-148">Child elements</span></span>

|<span data-ttu-id="9db5a-149">**元素**</span><span class="sxs-lookup"><span data-stu-id="9db5a-149">**Element**</span></span>|<span data-ttu-id="9db5a-150">**说明**</span><span class="sxs-lookup"><span data-stu-id="9db5a-150">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9db5a-151">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="9db5a-151">IndexedPageItemView</span></span>](indexedpageitemview.md) <br/> |<span data-ttu-id="9db5a-152">介绍如何分页的对话将返回的信息。</span><span class="sxs-lookup"><span data-stu-id="9db5a-152">Describes how paged conversation information is returned.</span></span>  <br/> |
|[<span data-ttu-id="9db5a-153">SeekToConditionPageItemView</span><span class="sxs-lookup"><span data-stu-id="9db5a-153">SeekToConditionPageItemView</span></span>](seektoconditionpageitemview.md) <br/> |<span data-ttu-id="9db5a-154">指定用于标识的末尾搜索、 搜索、 返回，最大条目和**FindItem**或**FindConversation**搜索的搜索方向的起始索引的条件。</span><span class="sxs-lookup"><span data-stu-id="9db5a-154">Specifies the condition that is used to identify the end of a search, the starting index of a search, the maximum entries to return, and the search directions for a **FindItem** or **FindConversation** search.</span></span>  <br/> |
|[<span data-ttu-id="9db5a-155">SortOrder</span><span class="sxs-lookup"><span data-stu-id="9db5a-155">SortOrder</span></span>](sortorder.md) <br/> |<span data-ttu-id="9db5a-156">定义项[FindConversation 操作](findconversation-operation.md)请求中的排序方式。</span><span class="sxs-lookup"><span data-stu-id="9db5a-156">Defines how items are sorted in a [FindConversation operation](findconversation-operation.md) request.</span></span> <span data-ttu-id="9db5a-157">**对话： LastDeliveryTime**属性是排序使用**FindConversation**操作时支持的唯一属性。</span><span class="sxs-lookup"><span data-stu-id="9db5a-157">The **conversation:LastDeliveryTime** property is the only property that is supported for sorting when the **FindConversation** operation is used.</span></span>  <br/> |
|[<span data-ttu-id="9db5a-158">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="9db5a-158">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="9db5a-159">标识要搜索的对话的文件夹。</span><span class="sxs-lookup"><span data-stu-id="9db5a-159">Identifies the folder to search for conversations.</span></span>  <br/> |
|[<span data-ttu-id="9db5a-160">MailboxScope</span><span class="sxs-lookup"><span data-stu-id="9db5a-160">MailboxScope</span></span>](mailboxscope.md) <br/> |<span data-ttu-id="9db5a-161">指定搜索或进行对话的提取是否应跨越主邮箱、 存档邮箱或两个主要和存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="9db5a-161">Specifies whether a search or fetch for a conversation should span either the primary mailbox, archive mailbox, or both the primary and archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="9db5a-162">查询字符串 (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="9db5a-162">QueryString (QueryStringType)</span></span>](querystring-querystringtype.md) <br/> |<span data-ttu-id="9db5a-163">指定基于上高级查询语法 (AQS) 的邮箱查询字符串。</span><span class="sxs-lookup"><span data-stu-id="9db5a-163">Specifies a mailbox query string based on Advanced Query Syntax (AQS).</span></span>  <br/> |
|[<span data-ttu-id="9db5a-164">ConversationShape</span><span class="sxs-lookup"><span data-stu-id="9db5a-164">ConversationShape</span></span>](conversationshape.md) <br/> |<span data-ttu-id="9db5a-165">标识设置[FindConversation 操作](findconversation-operation.md)响应中返回的属性。</span><span class="sxs-lookup"><span data-stu-id="9db5a-165">Identifies the property set to return in a [FindConversation operation](findconversation-operation.md) response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9db5a-166">父元素</span><span class="sxs-lookup"><span data-stu-id="9db5a-166">Parent elements</span></span>

<span data-ttu-id="9db5a-167">无。</span><span class="sxs-lookup"><span data-stu-id="9db5a-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9db5a-168">备注</span><span class="sxs-lookup"><span data-stu-id="9db5a-168">Remarks</span></span>

<span data-ttu-id="9db5a-169">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9db5a-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9db5a-170">元素信息</span><span class="sxs-lookup"><span data-stu-id="9db5a-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9db5a-171">命名空间</span><span class="sxs-lookup"><span data-stu-id="9db5a-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9db5a-172">架构名称</span><span class="sxs-lookup"><span data-stu-id="9db5a-172">Schema Name</span></span>  <br/> |<span data-ttu-id="9db5a-173">消息架构</span><span class="sxs-lookup"><span data-stu-id="9db5a-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9db5a-174">验证文件</span><span class="sxs-lookup"><span data-stu-id="9db5a-174">Validation File</span></span>  <br/> |<span data-ttu-id="9db5a-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9db5a-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9db5a-176">可以为空</span><span class="sxs-lookup"><span data-stu-id="9db5a-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="9db5a-177">False</span><span class="sxs-lookup"><span data-stu-id="9db5a-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9db5a-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9db5a-178">See also</span></span>



[<span data-ttu-id="9db5a-179">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="9db5a-179">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="9db5a-180">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9db5a-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="9db5a-181">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="9db5a-181">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

