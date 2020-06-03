---
title: QueryString （QueryStringType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: QueryString 元素包含基于高级查询语法（AQS）的邮箱查询字符串。
localization_priority: Priority
ms.openlocfilehash: eafbbab6de8d191197fb4b80e2b8e3cea80ab800
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459186"
---
# <a name="querystring-querystringtype"></a><span data-ttu-id="f6fcb-103">QueryString （QueryStringType）</span><span class="sxs-lookup"><span data-stu-id="f6fcb-103">QueryString (QueryStringType)</span></span>

<span data-ttu-id="f6fcb-104">**QueryString**元素包含基于高级查询语法（AQS）的邮箱查询字符串。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-104">The **QueryString** element contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span> 
  
```XML
<QueryString/>
```

 <span data-ttu-id="f6fcb-105">**QueryStringType**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-105">**QueryStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f6fcb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f6fcb-106">Attributes and elements</span></span>

<span data-ttu-id="f6fcb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f6fcb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f6fcb-108">Attributes</span></span>

|<span data-ttu-id="f6fcb-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-109">**Attribute**</span></span>|<span data-ttu-id="f6fcb-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6fcb-111">ResetCache</span><span class="sxs-lookup"><span data-stu-id="f6fcb-111">ResetCache</span></span>  <br/> |<span data-ttu-id="f6fcb-112">指示应重置缓存。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-112">Indicates that the cache should be reset.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-113">ReturnDeletedItems</span><span class="sxs-lookup"><span data-stu-id="f6fcb-113">ReturnDeletedItems</span></span>  <br/> |<span data-ttu-id="f6fcb-114">指示应返回已删除的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-114">Indicates that deleted items should be returned.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-115">ReturnHighlightTerms</span><span class="sxs-lookup"><span data-stu-id="f6fcb-115">ReturnHighlightTerms</span></span>  <br/> |<span data-ttu-id="f6fcb-116">指示应返回突出显示的术语。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-116">Indicates that highlighted terms should be returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f6fcb-117">子元素</span><span class="sxs-lookup"><span data-stu-id="f6fcb-117">Child elements</span></span>

<span data-ttu-id="f6fcb-118">无。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f6fcb-119">父元素</span><span class="sxs-lookup"><span data-stu-id="f6fcb-119">Parent elements</span></span>

|<span data-ttu-id="f6fcb-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-120">**Element**</span></span>|<span data-ttu-id="f6fcb-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f6fcb-122">FindItem</span><span class="sxs-lookup"><span data-stu-id="f6fcb-122">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="f6fcb-123">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-123">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="f6fcb-124">以下是此元素的 XPath 表达式：/FindItem。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-124">The following is the XPath expression to this element: /FindItem.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f6fcb-125">文本值</span><span class="sxs-lookup"><span data-stu-id="f6fcb-125">Text value</span></span>

<span data-ttu-id="f6fcb-126">**QueryString**元素 text 值代表使用[高级查询语法（AQS）](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx)的子集进行的邮箱查询。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-126">The **QueryString** element text value represents a mailbox query that is made by using a subset of [Advanced Query Syntax (AQS)](https://msdn.microsoft.com/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="f6fcb-127">有关查询字符串支持的语法选项的信息，请参阅 "备注" 部分。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-127">See the remarks section for information about the supported syntax options for query strings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6fcb-128">备注</span><span class="sxs-lookup"><span data-stu-id="f6fcb-128">Remarks</span></span>

<span data-ttu-id="f6fcb-129">在 Exchange Server 2010 中，此元素是 XML 架构字符串类型。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-129">In Exchange Server 2010, this element is an XML schema string type.</span></span> <span data-ttu-id="f6fcb-130">在从 Exchange Server 2013 开始的 Exchange 版本（包括 Exchange Online）中，此元素的类型为**QueryStringType**。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-130">In versions of Exchange starting with Exchange Server 2013, including Exchange Online, the type for this element is **QueryStringType**.</span></span> <span data-ttu-id="f6fcb-131">此更改不会中断任何现有客户端，因为它会添加三个新的可选属性。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-131">This change does not break any existing clients because it adds three new optional attributes.</span></span> 
  
<span data-ttu-id="f6fcb-132">**QueryString**元素不包括使用 EWS 限制。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-132">The **QueryString** element excludes the use of EWS restrictions.</span></span> <span data-ttu-id="f6fcb-133">EWS 中的 AQS 支持三种类型的限制：单词阶段限制、日期范围限制和邮件类型限制。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-133">AQS in EWS supports three types of restrictions: word phase restriction, date range restriction, and message type restriction.</span></span> <span data-ttu-id="f6fcb-134">下表列出了每种限制类型支持的搜索属性。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-134">The following tables list the supported search properties for each restriction type.</span></span> 
  
<span data-ttu-id="f6fcb-135">**Word 阶段限制**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-135">**Word phase restriction**</span></span>

|<span data-ttu-id="f6fcb-136">**Property**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-136">**Property**</span></span>|<span data-ttu-id="f6fcb-137">**示例**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-137">**Example**</span></span>|<span data-ttu-id="f6fcb-138">**Function**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-138">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6fcb-139">发件人</span><span class="sxs-lookup"><span data-stu-id="f6fcb-139">from</span></span>  <br/> |<span data-ttu-id="f6fcb-140">发件人： Dean</span><span class="sxs-lookup"><span data-stu-id="f6fcb-140">From:Dean</span></span>  <br/> <span data-ttu-id="f6fcb-141">发件人： "Dean Halstead"</span><span class="sxs-lookup"><span data-stu-id="f6fcb-141">From:"Dean Halstead"</span></span>  <br/> |<span data-ttu-id="f6fcb-142">搜索从 Dean 发送的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-142">Search items sent from Dean.</span></span>  <br/> <span data-ttu-id="f6fcb-143">从 Dean Halstead 发送的搜索项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-143">Search items sent from Dean Halstead.</span></span> <span data-ttu-id="f6fcb-144">发件人必须正好是 "Dean Halstead"。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-144">The sender must be exactly "Dean Halstead".</span></span>  <br/> |
|<span data-ttu-id="f6fcb-145">更改为</span><span class="sxs-lookup"><span data-stu-id="f6fcb-145">to</span></span>  <br/> |<span data-ttu-id="f6fcb-146">To： Dean</span><span class="sxs-lookup"><span data-stu-id="f6fcb-146">To:Dean</span></span>  <br/> |<span data-ttu-id="f6fcb-147">搜索发送到 Dean 的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-147">Search items sent to Dean.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-148">cc</span><span class="sxs-lookup"><span data-stu-id="f6fcb-148">cc</span></span>  <br/> |<span data-ttu-id="f6fcb-149">抄送： Dean</span><span class="sxs-lookup"><span data-stu-id="f6fcb-149">Cc:Dean</span></span>  <br/> |<span data-ttu-id="f6fcb-150">在 "抄送" 行中搜索带有 Dean 的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-150">Search for items with Dean on the Cc line.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-151">bcc</span><span class="sxs-lookup"><span data-stu-id="f6fcb-151">bcc</span></span>  <br/> |<span data-ttu-id="f6fcb-152">密件抄送： Dean</span><span class="sxs-lookup"><span data-stu-id="f6fcb-152">Bcc:Dean</span></span>  <br/> |<span data-ttu-id="f6fcb-153">搜索 "密件抄送" 行中带有 Dean 的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-153">Search for items with Dean on the Bcc line.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-154">Participants</span><span class="sxs-lookup"><span data-stu-id="f6fcb-154">Participants</span></span>  <br/> |<span data-ttu-id="f6fcb-155">参与者： Dean</span><span class="sxs-lookup"><span data-stu-id="f6fcb-155">Participants:Dean</span></span>  <br/> |<span data-ttu-id="f6fcb-156">在 "收件人"、"抄送" 或 "密件抄送" 字段中搜索带有 Dean 的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-156">Search for items with Dean in the To, Cc, or Bcc fields.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-157">Subject</span><span class="sxs-lookup"><span data-stu-id="f6fcb-157">Subject</span></span>  <br/> |<span data-ttu-id="f6fcb-158">Subject： product</span><span class="sxs-lookup"><span data-stu-id="f6fcb-158">Subject:product</span></span>  <br/> <span data-ttu-id="f6fcb-159">主题：（产品开发）</span><span class="sxs-lookup"><span data-stu-id="f6fcb-159">Subject:(product development)</span></span>  <br/> <span data-ttu-id="f6fcb-160">主题： "产品开发"</span><span class="sxs-lookup"><span data-stu-id="f6fcb-160">Subject:"product development"</span></span>  <br/> |<span data-ttu-id="f6fcb-161">在主题中搜索带有产品的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-161">Search for items with product in the subject.</span></span>  <br/> <span data-ttu-id="f6fcb-162">在主题中搜索带有产品和开发的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-162">Search for items with product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-163">正文</span><span class="sxs-lookup"><span data-stu-id="f6fcb-163">Body</span></span>  <br/> <span data-ttu-id="f6fcb-164">内容</span><span class="sxs-lookup"><span data-stu-id="f6fcb-164">Content</span></span>  <br/> |<span data-ttu-id="f6fcb-165">正文：进度</span><span class="sxs-lookup"><span data-stu-id="f6fcb-165">Body:progress</span></span>  <br/> <span data-ttu-id="f6fcb-166">内容：进度</span><span class="sxs-lookup"><span data-stu-id="f6fcb-166">Content:progress</span></span>  <br/> |<span data-ttu-id="f6fcb-167">在正文中搜索具有进度的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-167">Search for items with progress in the body.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-168">Attachment</span><span class="sxs-lookup"><span data-stu-id="f6fcb-168">Attachment</span></span>  <br/> |<span data-ttu-id="f6fcb-169">附件：报表</span><span class="sxs-lookup"><span data-stu-id="f6fcb-169">Attachment:report</span></span>  <br/> |<span data-ttu-id="f6fcb-170">在附件文件名或文件正文中搜索带有报告的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-170">Search for items with report in the attachment file name or file body.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-171">（未指定属性）</span><span class="sxs-lookup"><span data-stu-id="f6fcb-171">(property is not specified)</span></span>  <br/> |<span data-ttu-id="f6fcb-172">产品开发</span><span class="sxs-lookup"><span data-stu-id="f6fcb-172">Product Development</span></span>  <br/> |<span data-ttu-id="f6fcb-173">在所有 word 阶段属性中搜索包含产品和开发的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-173">Search for items that contain both product and development in all word phase properties.</span></span>  <br/> |
   
<span data-ttu-id="f6fcb-174">Word 阶段限制匹配始终不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-174">Word phase restriction match is always case insensitive.</span></span> <span data-ttu-id="f6fcb-175">Word 阶段限制支持两种匹配类型：前缀匹配或完全匹配。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-175">Word phase restriction supports two match types: prefix match or exact match.</span></span> <span data-ttu-id="f6fcb-176">前缀 match 是默认的匹配行为。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-176">Prefix match is the default match behavior.</span></span> <span data-ttu-id="f6fcb-177">如果需要完全匹配，请使用双引号。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-177">If you want exact match, use double quotes.</span></span> <span data-ttu-id="f6fcb-178">例如，subject： "product" 与主题中的 "product" 匹配，而不是 "生产"。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-178">For example, subject:"product" matches 'product' but not 'production' in the subject.</span></span> <span data-ttu-id="f6fcb-179">双引号中的多个单词将同时限制 word 阶段及其顺序。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-179">Multiple words in double quotes restrict both word phases and their order.</span></span> <span data-ttu-id="f6fcb-180">例如 "win product" 仅与 "win product" 匹配，而不是 "win95 产品" 或 "获奖的产品"。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-180">For example "win product" matches only 'win product', not 'win95 product' or 'product of win'.</span></span> <span data-ttu-id="f6fcb-181">您可以使用星号（ \* ）来定义带限制顺序的前缀匹配项。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-181">You can use an asterisk (\*) to define a prefix match with order restricted.</span></span> <span data-ttu-id="f6fcb-182">例如，"win product" \* 与 "win95 产品"、"windows 生产订单行" 而不是 "windows 新产品" 或 "胜产品" 相匹配。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-182">For example, "win product"\* matches 'win95 product', 'windows production line' but not 'windows new product' or 'product of win'.</span></span> <span data-ttu-id="f6fcb-183">您可以搜索从或发送到域的所有邮件。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-183">You can search all messages sent from or to a domain.</span></span> <span data-ttu-id="f6fcb-184">例如，从： "@hotmail" 返回从 hotmail.com 发送的所有邮件。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-184">For example, from:"@hotmail.com" returns all messages sent from hotmail.com.</span></span>
  
<span data-ttu-id="f6fcb-185">下表介绍了日期范围限制。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-185">The following table describes date range restrictions.</span></span>
  
<span data-ttu-id="f6fcb-186">**日期范围限制**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-186">**Date range restriction**</span></span>

|<span data-ttu-id="f6fcb-187">**Property**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-187">**Property**</span></span>|<span data-ttu-id="f6fcb-188">**示例**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-188">**Example**</span></span>|<span data-ttu-id="f6fcb-189">**Function**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-189">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6fcb-190">发件箱</span><span class="sxs-lookup"><span data-stu-id="f6fcb-190">Sent</span></span>  <br/> |<span data-ttu-id="f6fcb-191">已发送：上周</span><span class="sxs-lookup"><span data-stu-id="f6fcb-191">Sent:last week</span></span>  <br/> <span data-ttu-id="f6fcb-192">已发送： 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="f6fcb-192">Sent:01/01/2001</span></span>  <br/> <span data-ttu-id="f6fcb-193">发送： 01/01/2001. 01/15/2001</span><span class="sxs-lookup"><span data-stu-id="f6fcb-193">Sent:01/01/2001..01/15/2001</span></span>  <br/> |<span data-ttu-id="f6fcb-194">搜索上一周发送的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-194">Search items sent last week.</span></span>  <br/> <span data-ttu-id="f6fcb-195">搜索在1月1日（2001）发送的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-195">Search items sent on January 1st, 2001.</span></span>  <br/> <span data-ttu-id="f6fcb-196">搜索在1月1日、2001和1月 2001 15 日之间发送的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-196">Search items sent between January 1st, 2001 and January 15th, 2001.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-197">接收时间</span><span class="sxs-lookup"><span data-stu-id="f6fcb-197">Received</span></span>  <br/> |<span data-ttu-id="f6fcb-198">已接收：今天</span><span class="sxs-lookup"><span data-stu-id="f6fcb-198">Received:today</span></span>  <br/> <span data-ttu-id="f6fcb-199">已接收： 01/01/2001</span><span class="sxs-lookup"><span data-stu-id="f6fcb-199">Received:01/01/2001</span></span>  <br/> |<span data-ttu-id="f6fcb-200">搜索今天收到的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-200">Search items received today.</span></span>  <br/> <span data-ttu-id="f6fcb-201">搜索在1月1日（2001）收到的项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-201">Search items received on January 1st, 2001.</span></span>  <br/> |
   
<span data-ttu-id="f6fcb-202">这两个点（...）是一个区域运算符。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-202">The two dots (..) is a range operator.</span></span> <span data-ttu-id="f6fcb-203">它可用于定义具有开始日期和结束日期的范围。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-203">It can be used to define a range with a start and an end date.</span></span> <span data-ttu-id="f6fcb-204">若要指定日期，可以使用相对日期。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-204">To specify a date, you can use relative dates.</span></span> <span data-ttu-id="f6fcb-205">支持以下相对日期：</span><span class="sxs-lookup"><span data-stu-id="f6fcb-205">The following relative dates are supported:</span></span>
  
- <span data-ttu-id="f6fcb-206">相对日期：今天、明天、昨天</span><span class="sxs-lookup"><span data-stu-id="f6fcb-206">Relative dates: Today, tomorrow, yesterday</span></span>
    
- <span data-ttu-id="f6fcb-207">Multiword 相对日期：本周、下个月、上一周、上月或明年</span><span class="sxs-lookup"><span data-stu-id="f6fcb-207">Multiword relative dates: This week, next month, last week, past month, or coming year</span></span>
    
- <span data-ttu-id="f6fcb-208">天：星期日、星期一、星期二、星期三、星期四、星期五、星期六</span><span class="sxs-lookup"><span data-stu-id="f6fcb-208">Days: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday</span></span>
    
- <span data-ttu-id="f6fcb-209">一月份、二月、三月份、四月、六月、六月、七月、八月、九月、十月、十一月、十二月</span><span class="sxs-lookup"><span data-stu-id="f6fcb-209">January, February, March, April, May, June, July, August, September, October, November, December</span></span>
    
<span data-ttu-id="f6fcb-210">下表介绍了邮件类型限制。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-210">The following table describes message type restrictions.</span></span> 
  
<span data-ttu-id="f6fcb-211">**邮件类型限制**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-211">**Message type restriction**</span></span>

|<span data-ttu-id="f6fcb-212">**Property**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-212">**Property**</span></span>|<span data-ttu-id="f6fcb-213">**示例**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-213">**Example**</span></span>|<span data-ttu-id="f6fcb-214">**Function**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-214">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6fcb-215">Kind</span><span class="sxs-lookup"><span data-stu-id="f6fcb-215">Kind</span></span>  <br/> |<span data-ttu-id="f6fcb-216">种类：任务</span><span class="sxs-lookup"><span data-stu-id="f6fcb-216">Kind:tasks</span></span>  <br/> |<span data-ttu-id="f6fcb-217">搜索所有任务项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-217">Search all task items.</span></span>  <br/> |
   
<span data-ttu-id="f6fcb-218">EWS 中的 AQS 使用**Kind**属性指定邮件类型。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-218">AQS in EWS uses the **Kind** property to specify the message type.</span></span> <span data-ttu-id="f6fcb-219">Kind 属性可以与以下项目类型一起使用：</span><span class="sxs-lookup"><span data-stu-id="f6fcb-219">The Kind property can be used with the following item types:</span></span> 
  
- <span data-ttu-id="f6fcb-220">email</span><span class="sxs-lookup"><span data-stu-id="f6fcb-220">email</span></span>
    
- <span data-ttu-id="f6fcb-221">会议</span><span class="sxs-lookup"><span data-stu-id="f6fcb-221">meetings</span></span>
    
- <span data-ttu-id="f6fcb-222">tasks</span><span class="sxs-lookup"><span data-stu-id="f6fcb-222">tasks</span></span>
    
- <span data-ttu-id="f6fcb-223">注释</span><span class="sxs-lookup"><span data-stu-id="f6fcb-223">notes</span></span>
    
- <span data-ttu-id="f6fcb-224">文档</span><span class="sxs-lookup"><span data-stu-id="f6fcb-224">docs</span></span>
    
- <span data-ttu-id="f6fcb-225">日志</span><span class="sxs-lookup"><span data-stu-id="f6fcb-225">journals</span></span>
    
- <span data-ttu-id="f6fcb-226">contacts</span><span class="sxs-lookup"><span data-stu-id="f6fcb-226">contacts</span></span>
    
- <span data-ttu-id="f6fcb-227">即时消息</span><span class="sxs-lookup"><span data-stu-id="f6fcb-227">im</span></span>
    
<span data-ttu-id="f6fcb-228">下表介绍了分组逻辑连接器。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-228">The following table describes grouping logical connectors.</span></span>
  
<span data-ttu-id="f6fcb-229">**分组逻辑连接器**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-229">**Grouping logical connectors**</span></span>

|<span data-ttu-id="f6fcb-230">**Connector**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-230">**Connector**</span></span>|<span data-ttu-id="f6fcb-231">**示例**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-231">**Example**</span></span>|<span data-ttu-id="f6fcb-232">**Function**</span><span class="sxs-lookup"><span data-stu-id="f6fcb-232">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f6fcb-233">AND</span><span class="sxs-lookup"><span data-stu-id="f6fcb-233">AND</span></span>  <br/> |<span data-ttu-id="f6fcb-234">主题：产品和主题：开发</span><span class="sxs-lookup"><span data-stu-id="f6fcb-234">Subject:product AND subject:development</span></span>  <br/> <span data-ttu-id="f6fcb-235">主题：（产品和开发）</span><span class="sxs-lookup"><span data-stu-id="f6fcb-235">Subject:(product AND development)</span></span>  <br/> <span data-ttu-id="f6fcb-236">主题：（产品开发）</span><span class="sxs-lookup"><span data-stu-id="f6fcb-236">Subject:(product development)</span></span>  <br/> |<span data-ttu-id="f6fcb-237">在主题的产品和开发中搜索项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-237">Search items with both product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-238">OR</span><span class="sxs-lookup"><span data-stu-id="f6fcb-238">OR</span></span>  <br/> |<span data-ttu-id="f6fcb-239">正文：项目或正文：建议</span><span class="sxs-lookup"><span data-stu-id="f6fcb-239">Body:project OR body:proposal</span></span>  <br/> <span data-ttu-id="f6fcb-240">正文：（项目或建议）</span><span class="sxs-lookup"><span data-stu-id="f6fcb-240">Body:(project OR proposal)</span></span>  <br/> |<span data-ttu-id="f6fcb-241">使用正文中的产品或开发搜索项目。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-241">Search items with either product or development in the body.</span></span>  <br/> |
|<span data-ttu-id="f6fcb-242">NOT</span><span class="sxs-lookup"><span data-stu-id="f6fcb-242">NOT</span></span>  <br/> |<span data-ttu-id="f6fcb-243">非正文：建议</span><span class="sxs-lookup"><span data-stu-id="f6fcb-243">NOT body:proposal</span></span>  <br/> <span data-ttu-id="f6fcb-244">正文：（不建议）</span><span class="sxs-lookup"><span data-stu-id="f6fcb-244">Body:(NOT proposal)</span></span>  <br/> |<span data-ttu-id="f6fcb-245">搜索正文中没有建议的邮件。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-245">Search messages without proposal in the body.</span></span>  <br/> |
   
<span data-ttu-id="f6fcb-246">始终是默认的连接器。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-246">AND is always the default connector.</span></span> <span data-ttu-id="f6fcb-247">例如，subject： project 和 body：提案与 subject： project body：提案。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-247">For example, subject:project AND body:proposal is the same as subject:project body:proposal.</span></span> <span data-ttu-id="f6fcb-248">逻辑连接器区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-248">Logical connectors are case sensitive.</span></span> <span data-ttu-id="f6fcb-249">例如，body：（项目或建议）在正文中搜索带有 "项目"、"或" 和 "建议" 的邮件，而不是 "项目" 或 "建议"。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-249">For example, body:(project Or proposal) searches messages with 'project', 'or', and 'proposal' in the body instead of 'project' or 'proposal'.</span></span> <span data-ttu-id="f6fcb-250">加号符号（+）等效于和。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-250">The plus symbol (+) is equivalent to AND.</span></span> <span data-ttu-id="f6fcb-251">连字符符号（-）等效于 NOT。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-251">The hyphen symbol (-) is equivalent to NOT.</span></span> <span data-ttu-id="f6fcb-252">例如，body：（项目建议）在正文中搜索 "project" 但不包含 "提案" 的邮件。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-252">For example, body:(project - proposal) searches messages with 'project' but without 'proposal' in the body.</span></span> 
  
<span data-ttu-id="f6fcb-253">查询字符串还可以包含用于搜索的非索引属性。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-253">The query string can also contain nonindexed properties for search.</span></span> <span data-ttu-id="f6fcb-254">如果查询字符串中包含非索引属性，则搜索可能会对索引属性执行 Exchange 搜索，并对非索引属性执行存储搜索。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-254">If the query string contains nonindexed properties, the search might perform an Exchange search on the indexed properties and a store search on the nonindexed properties.</span></span> 
  
<span data-ttu-id="f6fcb-255">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-255">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="f6fcb-256">示例</span><span class="sxs-lookup"><span data-stu-id="f6fcb-256">Example</span></span>

<span data-ttu-id="f6fcb-257">下面的示例演示使用主题中的自动发现在收件箱中搜索邮件的请求。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-257">The following example shows a request to search for messages in the Inbox with Autodiscover in the subject.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
      <m:QueryString>subject:Autodiscover</m:QueryString>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="f6fcb-258">下面的示例演示对请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="f6fcb-258">The following example shows a successful response to the request.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1" 
                        TotalItemsInView="5" 
                        IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkADEzOTExYjJkLTYx" ChangeKey="CQAAABY" />
                <t:Subject>How to use Autodiscover</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>

```

## <a name="element-information"></a><span data-ttu-id="f6fcb-259">元素信息</span><span class="sxs-lookup"><span data-stu-id="f6fcb-259">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6fcb-260">命名空间</span><span class="sxs-lookup"><span data-stu-id="f6fcb-260">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f6fcb-261">架构名称</span><span class="sxs-lookup"><span data-stu-id="f6fcb-261">Schema name</span></span>  <br/> |<span data-ttu-id="f6fcb-262">消息架构</span><span class="sxs-lookup"><span data-stu-id="f6fcb-262">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f6fcb-263">验证文件</span><span class="sxs-lookup"><span data-stu-id="f6fcb-263">Validation file</span></span>  <br/> |<span data-ttu-id="f6fcb-264">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f6fcb-264">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f6fcb-265">可以为空</span><span class="sxs-lookup"><span data-stu-id="f6fcb-265">Can be empty</span></span>  <br/> |<span data-ttu-id="f6fcb-266">False</span><span class="sxs-lookup"><span data-stu-id="f6fcb-266">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f6fcb-267">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f6fcb-267">See also</span></span>



[<span data-ttu-id="f6fcb-268">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="f6fcb-268">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="f6fcb-269">FindConversation 操作</span><span class="sxs-lookup"><span data-stu-id="f6fcb-269">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="f6fcb-270">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f6fcb-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

