---
title: 查询字符串 (QueryStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- QueryString
api_type:
- schema
ms.assetid: cadbf9a5-b87e-4d7f-b488-b76fb0ee7150
description: QueryString 元素包含基于上高级查询语法 (AQS) 邮箱查询字符串。
ms.openlocfilehash: 410405638b3f8628dc589049873cfea1f153310c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826943"
---
# <a name="querystring-querystringtype"></a><span data-ttu-id="aa7de-103">查询字符串 (QueryStringType)</span><span class="sxs-lookup"><span data-stu-id="aa7de-103">QueryString (QueryStringType)</span></span>

<span data-ttu-id="aa7de-104">**QueryString**元素包含基于上高级查询语法 (AQS) 邮箱查询字符串。</span><span class="sxs-lookup"><span data-stu-id="aa7de-104">The **QueryString** element contains a mailbox query string based on Advanced Query Syntax (AQS).</span></span> 
  
```XML
<QueryString/>
```

 <span data-ttu-id="aa7de-105">**QueryStringType**</span><span class="sxs-lookup"><span data-stu-id="aa7de-105">**QueryStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa7de-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa7de-106">Attributes and elements</span></span>

<span data-ttu-id="aa7de-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa7de-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa7de-108">属性</span><span class="sxs-lookup"><span data-stu-id="aa7de-108">Attributes</span></span>

|<span data-ttu-id="aa7de-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="aa7de-109">**Attribute**</span></span>|<span data-ttu-id="aa7de-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa7de-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa7de-111">ResetCache</span><span class="sxs-lookup"><span data-stu-id="aa7de-111">ResetCache</span></span>  <br/> |<span data-ttu-id="aa7de-112">指示应重置缓存。</span><span class="sxs-lookup"><span data-stu-id="aa7de-112">Indicates that the cache should be reset.</span></span>  <br/> |
|<span data-ttu-id="aa7de-113">ReturnDeletedItems</span><span class="sxs-lookup"><span data-stu-id="aa7de-113">ReturnDeletedItems</span></span>  <br/> |<span data-ttu-id="aa7de-114">指示应返回已删除的项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-114">Indicates that deleted items should be returned.</span></span>  <br/> |
|<span data-ttu-id="aa7de-115">ReturnHighlightTerms</span><span class="sxs-lookup"><span data-stu-id="aa7de-115">ReturnHighlightTerms</span></span>  <br/> |<span data-ttu-id="aa7de-116">指示应返回突出显示的术语。</span><span class="sxs-lookup"><span data-stu-id="aa7de-116">Indicates that highlighted terms should be returned.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aa7de-117">子元素</span><span class="sxs-lookup"><span data-stu-id="aa7de-117">Child elements</span></span>

<span data-ttu-id="aa7de-118">无。</span><span class="sxs-lookup"><span data-stu-id="aa7de-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aa7de-119">父元素</span><span class="sxs-lookup"><span data-stu-id="aa7de-119">Parent elements</span></span>

|<span data-ttu-id="aa7de-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa7de-120">**Element**</span></span>|<span data-ttu-id="aa7de-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa7de-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa7de-122">FindItem</span><span class="sxs-lookup"><span data-stu-id="aa7de-122">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="aa7de-123">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="aa7de-123">Defines a request to find items in a mailbox.</span></span>  <br/> <span data-ttu-id="aa7de-124">下面是此元素的 XPath 表达式： /FindItem。</span><span class="sxs-lookup"><span data-stu-id="aa7de-124">The following is the XPath expression to this element: /FindItem.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aa7de-125">文本值</span><span class="sxs-lookup"><span data-stu-id="aa7de-125">Text value</span></span>

<span data-ttu-id="aa7de-126">**QueryString**元素文本值表示由使用[高级查询语法 (AQS)](http://msdn.microsoft.com/zh-cn/library/aa965711%28VS.85%29.aspx)的子集的邮箱查询。</span><span class="sxs-lookup"><span data-stu-id="aa7de-126">The **QueryString** element text value represents a mailbox query that is made by using a subset of [Advanced Query Syntax (AQS)](http://msdn.microsoft.com/zh-cn/library/aa965711%28VS.85%29.aspx).</span></span> <span data-ttu-id="aa7de-127">请参阅备注部分的有关支持的语法查询字符串选项的信息。</span><span class="sxs-lookup"><span data-stu-id="aa7de-127">See the remarks section for information about the supported syntax options for query strings.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa7de-128">注解</span><span class="sxs-lookup"><span data-stu-id="aa7de-128">Remarks</span></span>

<span data-ttu-id="aa7de-129">在 Exchange Server 2010 中，此元素是 XML 架构 string 类型。</span><span class="sxs-lookup"><span data-stu-id="aa7de-129">In Exchange Server 2010, this element is an XML schema string type.</span></span> <span data-ttu-id="aa7de-130">在版本的 Exchange 开头 Exchange Server 2013，包括 Exchange Online，此元素的类型是**QueryStringType**。</span><span class="sxs-lookup"><span data-stu-id="aa7de-130">In versions of Exchange starting with Exchange Server 2013, including Exchange Online, the type for this element is **QueryStringType**.</span></span> <span data-ttu-id="aa7de-131">此更改不会将任何现有的客户端，因为它将添加三个新的可选属性。</span><span class="sxs-lookup"><span data-stu-id="aa7de-131">This change does not break any existing clients because it adds three new optional attributes.</span></span> 
  
<span data-ttu-id="aa7de-132">**QueryString**元素不包括使用 EWS 限制。</span><span class="sxs-lookup"><span data-stu-id="aa7de-132">The **QueryString** element excludes the use of EWS restrictions.</span></span> <span data-ttu-id="aa7de-133">Ews AQS 支持三种类型的限制： word 阶段限制、 日期范围限制和消息类型限制。</span><span class="sxs-lookup"><span data-stu-id="aa7de-133">AQS in EWS supports three types of restrictions: word phase restriction, date range restriction, and message type restriction.</span></span> <span data-ttu-id="aa7de-134">下表列出了每种限制类型的支持的搜索属性。</span><span class="sxs-lookup"><span data-stu-id="aa7de-134">The following tables list the supported search properties for each restriction type.</span></span> 
  
<span data-ttu-id="aa7de-135">**Word 阶段限制**</span><span class="sxs-lookup"><span data-stu-id="aa7de-135">**Word phase restriction**</span></span>

|<span data-ttu-id="aa7de-136">**属性**</span><span class="sxs-lookup"><span data-stu-id="aa7de-136">**Property**</span></span>|<span data-ttu-id="aa7de-137">**示例**</span><span class="sxs-lookup"><span data-stu-id="aa7de-137">**Example**</span></span>|<span data-ttu-id="aa7de-138">**函数**</span><span class="sxs-lookup"><span data-stu-id="aa7de-138">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa7de-139">发件人</span><span class="sxs-lookup"><span data-stu-id="aa7de-139">from</span></span>  <br/> |<span data-ttu-id="aa7de-140">从： Dean</span><span class="sxs-lookup"><span data-stu-id="aa7de-140">From:Dean</span></span>  <br/> <span data-ttu-id="aa7de-141">从:"Dean Halstead"</span><span class="sxs-lookup"><span data-stu-id="aa7de-141">From:"Dean Halstead"</span></span>  <br/> |<span data-ttu-id="aa7de-142">搜索从 Dean 发送的项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-142">Search items sent from Dean.</span></span>  <br/> <span data-ttu-id="aa7de-143">搜索从 Dean Halstead 发送项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-143">Search items sent from Dean Halstead.</span></span> <span data-ttu-id="aa7de-144">发件人必须完全"Dean Halstead"。</span><span class="sxs-lookup"><span data-stu-id="aa7de-144">The sender must be exactly "Dean Halstead".</span></span>  <br/> |
|<span data-ttu-id="aa7de-145">更改为</span><span class="sxs-lookup"><span data-stu-id="aa7de-145">to</span></span>  <br/> |<span data-ttu-id="aa7de-146">到： Dean</span><span class="sxs-lookup"><span data-stu-id="aa7de-146">To:Dean</span></span>  <br/> |<span data-ttu-id="aa7de-147">搜索发送给 Dean 项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-147">Search items sent to Dean.</span></span>  <br/> |
|<span data-ttu-id="aa7de-148">cc</span><span class="sxs-lookup"><span data-stu-id="aa7de-148">cc</span></span>  <br/> |<span data-ttu-id="aa7de-149">Cc:Dean</span><span class="sxs-lookup"><span data-stu-id="aa7de-149">Cc:Dean</span></span>  <br/> |<span data-ttu-id="aa7de-150">搜索与 Dean Cc 行上的项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-150">Search for items with Dean on the Cc line.</span></span>  <br/> |
|<span data-ttu-id="aa7de-151">bcc</span><span class="sxs-lookup"><span data-stu-id="aa7de-151">bcc</span></span>  <br/> |<span data-ttu-id="aa7de-152">Bcc:Dean</span><span class="sxs-lookup"><span data-stu-id="aa7de-152">Bcc:Dean</span></span>  <br/> |<span data-ttu-id="aa7de-153">搜索与 Dean 密件抄送行上的项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-153">Search for items with Dean on the Bcc line.</span></span>  <br/> |
|<span data-ttu-id="aa7de-154">参与者</span><span class="sxs-lookup"><span data-stu-id="aa7de-154">Participants</span></span>  <br/> |<span data-ttu-id="aa7de-155">参与者： Dean</span><span class="sxs-lookup"><span data-stu-id="aa7de-155">Participants:Dean</span></span>  <br/> |<span data-ttu-id="aa7de-156">搜索 Dean 项目中的收件人、 抄送或密件抄送字段。</span><span class="sxs-lookup"><span data-stu-id="aa7de-156">Search for items with Dean in the To, Cc, or Bcc fields.</span></span>  <br/> |
|<span data-ttu-id="aa7de-157">主题</span><span class="sxs-lookup"><span data-stu-id="aa7de-157">Subject</span></span>  <br/> |<span data-ttu-id="aa7de-158">主题： 产品</span><span class="sxs-lookup"><span data-stu-id="aa7de-158">Subject:product</span></span>  <br/> <span data-ttu-id="aa7de-159">主题:(product development)</span><span class="sxs-lookup"><span data-stu-id="aa7de-159">Subject:(product development)</span></span>  <br/> <span data-ttu-id="aa7de-160">使用者:"产品开发"</span><span class="sxs-lookup"><span data-stu-id="aa7de-160">Subject:"product development"</span></span>  <br/> |<span data-ttu-id="aa7de-161">搜索项目的主题中的产品。</span><span class="sxs-lookup"><span data-stu-id="aa7de-161">Search for items with product in the subject.</span></span>  <br/> <span data-ttu-id="aa7de-162">搜索与产品开发主题中的项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-162">Search for items with product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="aa7de-163">正文</span><span class="sxs-lookup"><span data-stu-id="aa7de-163">Body</span></span>  <br/> <span data-ttu-id="aa7de-164">内容</span><span class="sxs-lookup"><span data-stu-id="aa7de-164">Content</span></span>  <br/> |<span data-ttu-id="aa7de-165">正文： 进度</span><span class="sxs-lookup"><span data-stu-id="aa7de-165">Body:progress</span></span>  <br/> <span data-ttu-id="aa7de-166">内容： 进度</span><span class="sxs-lookup"><span data-stu-id="aa7de-166">Content:progress</span></span>  <br/> |<span data-ttu-id="aa7de-167">搜索项目的正文中的进度。</span><span class="sxs-lookup"><span data-stu-id="aa7de-167">Search for items with progress in the body.</span></span>  <br/> |
|<span data-ttu-id="aa7de-168">附件</span><span class="sxs-lookup"><span data-stu-id="aa7de-168">Attachment</span></span>  <br/> |<span data-ttu-id="aa7de-169">附件： 报告</span><span class="sxs-lookup"><span data-stu-id="aa7de-169">Attachment:report</span></span>  <br/> |<span data-ttu-id="aa7de-170">搜索项目的附件文件的名称或文件正文中的报告。</span><span class="sxs-lookup"><span data-stu-id="aa7de-170">Search for items with report in the attachment file name or file body.</span></span>  <br/> |
|<span data-ttu-id="aa7de-171">（未指定属性）</span><span class="sxs-lookup"><span data-stu-id="aa7de-171">(property is not specified)</span></span>  <br/> |<span data-ttu-id="aa7de-172">产品开发</span><span class="sxs-lookup"><span data-stu-id="aa7de-172">Product Development</span></span>  <br/> |<span data-ttu-id="aa7de-173">搜索的项目包含产品和所有 word 阶段属性中的开发。</span><span class="sxs-lookup"><span data-stu-id="aa7de-173">Search for items that contain both product and development in all word phase properties.</span></span>  <br/> |
   
<span data-ttu-id="aa7de-174">始终 Word 阶段限制匹配是区分大小写。</span><span class="sxs-lookup"><span data-stu-id="aa7de-174">Word phase restriction match is always case insensitive.</span></span> <span data-ttu-id="aa7de-175">Word 阶段限制支持两种匹配类型： 前缀匹配或完全匹配。</span><span class="sxs-lookup"><span data-stu-id="aa7de-175">Word phase restriction supports two match types: prefix match or exact match.</span></span> <span data-ttu-id="aa7de-176">前缀匹配是默认匹配行为。</span><span class="sxs-lookup"><span data-stu-id="aa7de-176">Prefix match is the default match behavior.</span></span> <span data-ttu-id="aa7de-177">如果您希望完全匹配，则使用双引号。</span><span class="sxs-lookup"><span data-stu-id="aa7de-177">If you want exact match, use double quotes.</span></span> <span data-ttu-id="aa7de-178">例如，使用者:"产品"匹配产品但不是生产主题中的。</span><span class="sxs-lookup"><span data-stu-id="aa7de-178">For example, subject:"product" matches 'product' but not 'production' in the subject.</span></span> <span data-ttu-id="aa7de-179">用双引号括起来的多个词语限制 word 阶段和它们的顺序。</span><span class="sxs-lookup"><span data-stu-id="aa7de-179">Multiple words in double quotes restrict both word phases and their order.</span></span> <span data-ttu-id="aa7de-180">例如"产品 win"匹配仅 win 产品，不 win95 产品或产品的 win。</span><span class="sxs-lookup"><span data-stu-id="aa7de-180">For example "win product" matches only 'win product', not 'win95 product' or 'product of win'.</span></span> <span data-ttu-id="aa7de-181">您可以使用星号 (\*) 定义与受限制的订单的前缀匹配。</span><span class="sxs-lookup"><span data-stu-id="aa7de-181">You can use an asterisk (\*) to define a prefix match with order restricted.</span></span> <span data-ttu-id="aa7de-182">例如，"win 产品"\*匹配 win95 产品、 windows 生产线但不是 windows 新产品或产品的 win。</span><span class="sxs-lookup"><span data-stu-id="aa7de-182">For example, "win product"\* matches 'win95 product', 'windows production line' but not 'windows new product' or 'product of win'.</span></span> <span data-ttu-id="aa7de-183">您可以搜索来自或发送到域的所有邮件。</span><span class="sxs-lookup"><span data-stu-id="aa7de-183">You can search all messages sent from or to a domain.</span></span> <span data-ttu-id="aa7de-184">例如，from:"@hotmail.com"返回从 hotmail.com 发送的所有邮件。</span><span class="sxs-lookup"><span data-stu-id="aa7de-184">For example, from:"@hotmail.com" returns all messages sent from hotmail.com.</span></span>
  
<span data-ttu-id="aa7de-185">下表介绍日期范围限制。</span><span class="sxs-lookup"><span data-stu-id="aa7de-185">The following table describes date range restrictions.</span></span>
  
<span data-ttu-id="aa7de-186">**日期范围限制**</span><span class="sxs-lookup"><span data-stu-id="aa7de-186">**Date range restriction**</span></span>

|<span data-ttu-id="aa7de-187">**属性**</span><span class="sxs-lookup"><span data-stu-id="aa7de-187">**Property**</span></span>|<span data-ttu-id="aa7de-188">**示例**</span><span class="sxs-lookup"><span data-stu-id="aa7de-188">**Example**</span></span>|<span data-ttu-id="aa7de-189">**函数**</span><span class="sxs-lookup"><span data-stu-id="aa7de-189">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa7de-190">发送时间</span><span class="sxs-lookup"><span data-stu-id="aa7de-190">Sent</span></span>  <br/> |<span data-ttu-id="aa7de-191">发送： 上周</span><span class="sxs-lookup"><span data-stu-id="aa7de-191">Sent:last week</span></span>  <br/> <span data-ttu-id="aa7de-192">发送： 2001-01-01</span><span class="sxs-lookup"><span data-stu-id="aa7de-192">Sent:01/01/2001</span></span>  <br/> <span data-ttu-id="aa7de-193">Sent:01/01/2001..01/15/2001</span><span class="sxs-lookup"><span data-stu-id="aa7de-193">Sent:01/01/2001..01/15/2001</span></span>  <br/> |<span data-ttu-id="aa7de-194">搜索项目发送最后一个星期。</span><span class="sxs-lookup"><span data-stu-id="aa7de-194">Search items sent last week.</span></span>  <br/> <span data-ttu-id="aa7de-195">搜索 2001 年 1 月 1st，发送项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-195">Search items sent on January 1st, 2001.</span></span>  <br/> <span data-ttu-id="aa7de-196">搜索 2001 年 1 月 1 日和 2001 年 1 月 15 日之间发送的项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-196">Search items sent between January 1st, 2001 and January 15th, 2001.</span></span>  <br/> |
|<span data-ttu-id="aa7de-197">接收时间</span><span class="sxs-lookup"><span data-stu-id="aa7de-197">Received</span></span>  <br/> |<span data-ttu-id="aa7de-198">接收： 立即</span><span class="sxs-lookup"><span data-stu-id="aa7de-198">Received:today</span></span>  <br/> <span data-ttu-id="aa7de-199">接收： 2001-01-01</span><span class="sxs-lookup"><span data-stu-id="aa7de-199">Received:01/01/2001</span></span>  <br/> |<span data-ttu-id="aa7de-200">搜索收到今天的项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-200">Search items received today.</span></span>  <br/> <span data-ttu-id="aa7de-201">搜索 2001 年 1 月 1st，收到的项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-201">Search items received on January 1st, 2001.</span></span>  <br/> |
   
<span data-ttu-id="aa7de-202">两个点 （.） 是一个范围运算符。</span><span class="sxs-lookup"><span data-stu-id="aa7de-202">The two dots (..) is a range operator.</span></span> <span data-ttu-id="aa7de-203">它可以用于定义开始和结束日期范围。</span><span class="sxs-lookup"><span data-stu-id="aa7de-203">It can be used to define a range with a start and an end date.</span></span> <span data-ttu-id="aa7de-204">若要指定的日期，您可以使用相对日期。</span><span class="sxs-lookup"><span data-stu-id="aa7de-204">To specify a date, you can use relative dates.</span></span> <span data-ttu-id="aa7de-205">支持以下相对日期：</span><span class="sxs-lookup"><span data-stu-id="aa7de-205">The following relative dates are supported:</span></span>
  
- <span data-ttu-id="aa7de-206">相对日期： 今天、 明天、 昨天</span><span class="sxs-lookup"><span data-stu-id="aa7de-206">Relative dates: Today, tomorrow, yesterday</span></span>
    
- <span data-ttu-id="aa7de-207">多词相对日期： 本周下个月，过去的月或明年上周</span><span class="sxs-lookup"><span data-stu-id="aa7de-207">Multiword relative dates: This week, next month, last week, past month, or coming year</span></span>
    
- <span data-ttu-id="aa7de-208">天数： 星期日和星期一、 星期二、 星期三、 星期四和星期五和星期六</span><span class="sxs-lookup"><span data-stu-id="aa7de-208">Days: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday</span></span>
    
- <span data-ttu-id="aa7de-209">年 1 月、 年 2 月、 March、 April、 May，年 6 月、 年 7 月、 年 8 月、 年 9 月、 年 10 月、 年 11 月、 年 12 月</span><span class="sxs-lookup"><span data-stu-id="aa7de-209">January, February, March, April, May, June, July, August, September, October, November, December</span></span>
    
<span data-ttu-id="aa7de-210">下表描述了消息类型限制。</span><span class="sxs-lookup"><span data-stu-id="aa7de-210">The following table describes message type restrictions.</span></span> 
  
<span data-ttu-id="aa7de-211">**消息类型限制**</span><span class="sxs-lookup"><span data-stu-id="aa7de-211">**Message type restriction**</span></span>

|<span data-ttu-id="aa7de-212">**属性**</span><span class="sxs-lookup"><span data-stu-id="aa7de-212">**Property**</span></span>|<span data-ttu-id="aa7de-213">**示例**</span><span class="sxs-lookup"><span data-stu-id="aa7de-213">**Example**</span></span>|<span data-ttu-id="aa7de-214">**函数**</span><span class="sxs-lookup"><span data-stu-id="aa7de-214">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa7de-215">类型</span><span class="sxs-lookup"><span data-stu-id="aa7de-215">Kind</span></span>  <br/> |<span data-ttu-id="aa7de-216">类型： 任务</span><span class="sxs-lookup"><span data-stu-id="aa7de-216">Kind:tasks</span></span>  <br/> |<span data-ttu-id="aa7de-217">搜索所有任务项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-217">Search all task items.</span></span>  <br/> |
   
<span data-ttu-id="aa7de-218">AQS EWS 中的使用的**类型**属性来指定消息类型。</span><span class="sxs-lookup"><span data-stu-id="aa7de-218">AQS in EWS uses the **Kind** property to specify the message type.</span></span> <span data-ttu-id="aa7de-219">Kind 属性可用于以下类型的项：</span><span class="sxs-lookup"><span data-stu-id="aa7de-219">The Kind property can be used with the following item types:</span></span> 
  
- <span data-ttu-id="aa7de-220">email</span><span class="sxs-lookup"><span data-stu-id="aa7de-220">email</span></span>
    
- <span data-ttu-id="aa7de-221">会议</span><span class="sxs-lookup"><span data-stu-id="aa7de-221">meetings</span></span>
    
- <span data-ttu-id="aa7de-222">tasks</span><span class="sxs-lookup"><span data-stu-id="aa7de-222">tasks</span></span>
    
- <span data-ttu-id="aa7de-223">notes</span><span class="sxs-lookup"><span data-stu-id="aa7de-223">notes</span></span>
    
- <span data-ttu-id="aa7de-224">文档</span><span class="sxs-lookup"><span data-stu-id="aa7de-224">docs</span></span>
    
- <span data-ttu-id="aa7de-225">日志</span><span class="sxs-lookup"><span data-stu-id="aa7de-225">journals</span></span>
    
- <span data-ttu-id="aa7de-226">contacts</span><span class="sxs-lookup"><span data-stu-id="aa7de-226">contacts</span></span>
    
- <span data-ttu-id="aa7de-227">im</span><span class="sxs-lookup"><span data-stu-id="aa7de-227">im</span></span>
    
<span data-ttu-id="aa7de-228">下表介绍分组逻辑连接器。</span><span class="sxs-lookup"><span data-stu-id="aa7de-228">The following table describes grouping logical connectors.</span></span>
  
<span data-ttu-id="aa7de-229">**分组逻辑连接器**</span><span class="sxs-lookup"><span data-stu-id="aa7de-229">**Grouping logical connectors**</span></span>

|<span data-ttu-id="aa7de-230">**连接器**</span><span class="sxs-lookup"><span data-stu-id="aa7de-230">**Connector**</span></span>|<span data-ttu-id="aa7de-231">**示例**</span><span class="sxs-lookup"><span data-stu-id="aa7de-231">**Example**</span></span>|<span data-ttu-id="aa7de-232">**函数**</span><span class="sxs-lookup"><span data-stu-id="aa7de-232">**Function**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="aa7de-233">AND</span><span class="sxs-lookup"><span data-stu-id="aa7de-233">AND</span></span>  <br/> |<span data-ttu-id="aa7de-234">主题： 产品和主题： 开发</span><span class="sxs-lookup"><span data-stu-id="aa7de-234">Subject:product AND subject:development</span></span>  <br/> <span data-ttu-id="aa7de-235">主题:(product AND development)</span><span class="sxs-lookup"><span data-stu-id="aa7de-235">Subject:(product AND development)</span></span>  <br/> <span data-ttu-id="aa7de-236">主题:(product development)</span><span class="sxs-lookup"><span data-stu-id="aa7de-236">Subject:(product development)</span></span>  <br/> |<span data-ttu-id="aa7de-237">搜索主题中的产品和开发项目。</span><span class="sxs-lookup"><span data-stu-id="aa7de-237">Search items with both product and development in the subject.</span></span>  <br/> |
|<span data-ttu-id="aa7de-238">OR</span><span class="sxs-lookup"><span data-stu-id="aa7de-238">OR</span></span>  <br/> |<span data-ttu-id="aa7de-239">正文： 项目或项目正文的建议：</span><span class="sxs-lookup"><span data-stu-id="aa7de-239">Body:project OR body:proposal</span></span>  <br/> <span data-ttu-id="aa7de-240">正文:(project OR proposal)</span><span class="sxs-lookup"><span data-stu-id="aa7de-240">Body:(project OR proposal)</span></span>  <br/> |<span data-ttu-id="aa7de-241">搜索项目产品或在正文中的开发。</span><span class="sxs-lookup"><span data-stu-id="aa7de-241">Search items with either product or development in the body.</span></span>  <br/> |
|<span data-ttu-id="aa7de-242">NOT</span><span class="sxs-lookup"><span data-stu-id="aa7de-242">NOT</span></span>  <br/> |<span data-ttu-id="aa7de-243">不建议正文：</span><span class="sxs-lookup"><span data-stu-id="aa7de-243">NOT body:proposal</span></span>  <br/> <span data-ttu-id="aa7de-244">正文:(NOT proposal)</span><span class="sxs-lookup"><span data-stu-id="aa7de-244">Body:(NOT proposal)</span></span>  <br/> |<span data-ttu-id="aa7de-245">搜索不建议在正文中的邮件。</span><span class="sxs-lookup"><span data-stu-id="aa7de-245">Search messages without proposal in the body.</span></span>  <br/> |
   
<span data-ttu-id="aa7de-246">并且始终是默认连接器。</span><span class="sxs-lookup"><span data-stu-id="aa7de-246">AND is always the default connector.</span></span> <span data-ttu-id="aa7de-247">例如，主题： project AND body： 建议是主题： 项目正文： 建议相同。</span><span class="sxs-lookup"><span data-stu-id="aa7de-247">For example, subject:project AND body:proposal is the same as subject:project body:proposal.</span></span> <span data-ttu-id="aa7de-248">逻辑连接器是区分大小写。</span><span class="sxs-lookup"><span data-stu-id="aa7de-248">Logical connectors are case sensitive.</span></span> <span data-ttu-id="aa7de-249">例如，正文:(project Or proposal) 搜索邮件的项目，或，和而不是项目或建议在正文中的建议。</span><span class="sxs-lookup"><span data-stu-id="aa7de-249">For example, body:(project Or proposal) searches messages with 'project', 'or', and 'proposal' in the body instead of 'project' or 'proposal'.</span></span> <span data-ttu-id="aa7de-250">加号 （+） 等同于成和。</span><span class="sxs-lookup"><span data-stu-id="aa7de-250">The plus symbol (+) is equivalent to AND.</span></span> <span data-ttu-id="aa7de-251">连字符符号 （-） 相当于不。</span><span class="sxs-lookup"><span data-stu-id="aa7de-251">The hyphen symbol (-) is equivalent to NOT.</span></span> <span data-ttu-id="aa7de-252">例如，正文:(project-proposal) 正文中搜索项目但不包含建议的消息。</span><span class="sxs-lookup"><span data-stu-id="aa7de-252">For example, body:(project - proposal) searches messages with 'project' but without 'proposal' in the body.</span></span> 
  
<span data-ttu-id="aa7de-253">查询字符串还可以包含用于搜索的非索引属性。</span><span class="sxs-lookup"><span data-stu-id="aa7de-253">The query string can also contain nonindexed properties for search.</span></span> <span data-ttu-id="aa7de-254">如果查询字符串中包含非索引属性，搜索可能执行 Exchange 搜索索引的属性和存储搜索索引的属性。</span><span class="sxs-lookup"><span data-stu-id="aa7de-254">If the query string contains nonindexed properties, the search might perform an Exchange search on the indexed properties and a store search on the nonindexed properties.</span></span> 
  
<span data-ttu-id="aa7de-255">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="aa7de-255">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="aa7de-256">示例</span><span class="sxs-lookup"><span data-stu-id="aa7de-256">Example</span></span>

<span data-ttu-id="aa7de-257">下面的示例演示请求来搜索使用自动发现收件箱中主题中的邮件。</span><span class="sxs-lookup"><span data-stu-id="aa7de-257">The following example shows a request to search for messages in the Inbox with Autodiscover in the subject.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
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

<span data-ttu-id="aa7de-258">下面的示例演示请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="aa7de-258">The following example shows a successful response to the request.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="aa7de-259">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa7de-259">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa7de-260">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa7de-260">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aa7de-261">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa7de-261">Schema name</span></span>  <br/> |<span data-ttu-id="aa7de-262">消息架构</span><span class="sxs-lookup"><span data-stu-id="aa7de-262">Messages schema</span></span>  <br/> |
|<span data-ttu-id="aa7de-263">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa7de-263">Validation file</span></span>  <br/> |<span data-ttu-id="aa7de-264">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="aa7de-264">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aa7de-265">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa7de-265">Can be empty</span></span>  <br/> |<span data-ttu-id="aa7de-266">False</span><span class="sxs-lookup"><span data-stu-id="aa7de-266">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa7de-267">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa7de-267">See also</span></span>



[<span data-ttu-id="aa7de-268">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="aa7de-268">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="aa7de-269">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="aa7de-269">FindConversation operation</span></span>](findconversation-operation.md)


- [<span data-ttu-id="aa7de-270">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="aa7de-270">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

