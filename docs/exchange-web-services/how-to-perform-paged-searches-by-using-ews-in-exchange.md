---
title: 在 Exchange 使用 EWS 执行分页的搜索
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: 了解如何在您的 EWS 托管 API 或 Exchange 的 EWS 应用程序执行分页的搜索。
ms.openlocfilehash: 3f82f46d0582b0b7ff8be63de8a7054b5f3cacab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752864"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a><span data-ttu-id="12ce0-103">在 Exchange 使用 EWS 执行分页的搜索</span><span class="sxs-lookup"><span data-stu-id="12ce0-103">Perform paged searches by using EWS in Exchange</span></span>

<span data-ttu-id="12ce0-104">了解如何在您的 EWS 托管 API 或 Exchange 的 EWS 应用程序执行分页的搜索。</span><span class="sxs-lookup"><span data-stu-id="12ce0-104">Find out how to perform paged searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="12ce0-105">分页是使您能够控制搜索结果的大小的 EWS 中的功能。</span><span class="sxs-lookup"><span data-stu-id="12ce0-105">Paging is a feature in EWS that enables you to control the size of the results of a search.</span></span> <span data-ttu-id="12ce0-106">而不是检索整个结果集一个 EWS 响应中，您可以检索在多个 EWS 响应中较小的集。</span><span class="sxs-lookup"><span data-stu-id="12ce0-106">Rather than retrieve the entire result set in one EWS response, you can retrieve smaller sets in multiple EWS responses.</span></span> <span data-ttu-id="12ce0-107">例如，假设有 10,000 其收件箱中的电子邮件的用户。</span><span class="sxs-lookup"><span data-stu-id="12ce0-107">For example, consider a user with 10,000 email messages in their Inbox.</span></span> <span data-ttu-id="12ce0-108">假设您无法检索一个非常大的响应，所有 10,000 电子邮件，但您可能想要的拆分到更易于管理的区块带宽或性能原因。</span><span class="sxs-lookup"><span data-stu-id="12ce0-108">Hypothetically, you could retrieve all 10,000 emails in one very large response, but you might want to break that up into more manageable chunks for bandwidth or performance reasons.</span></span> <span data-ttu-id="12ce0-109">分页为您提供的工具，做到这一点。</span><span class="sxs-lookup"><span data-stu-id="12ce0-109">Paging gives you the tools to do just that.</span></span>
  
> [!NOTE]
> <span data-ttu-id="12ce0-110">时您可以假定 10,000 以检索项目一个请求，实际上，这是由于 EWS 限制太。</span><span class="sxs-lookup"><span data-stu-id="12ce0-110">While you can hypothetically retrieve 10,000 items in one request, in reality, this is unlikely due to EWS throttling.</span></span> <span data-ttu-id="12ce0-111">若要了解更多信息，请参阅[EWS 限制在 Exchange](ews-throttling-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="12ce0-111">To find out more, see [EWS throttling in Exchange](ews-throttling-in-exchange.md).</span></span> 
  
<span data-ttu-id="12ce0-112">**表 1。EWS 托管 API 和 EWS 中的分页参数**</span><span class="sxs-lookup"><span data-stu-id="12ce0-112">**Table 1. Paging parameters in the EWS Managed API and EWS**</span></span>

|<span data-ttu-id="12ce0-113">**若要配置或检索...**</span><span class="sxs-lookup"><span data-stu-id="12ce0-113">**To configure or retrieve the…**</span></span>|<span data-ttu-id="12ce0-114">**EWS 托管 API，在使用...**</span><span class="sxs-lookup"><span data-stu-id="12ce0-114">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="12ce0-115">**EWS，在使用...**</span><span class="sxs-lookup"><span data-stu-id="12ce0-115">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="12ce0-116">项目或文件夹的响应中的最大数量</span><span class="sxs-lookup"><span data-stu-id="12ce0-116">Maximum number of items or folders in a response</span></span>  <br/> |<span data-ttu-id="12ce0-117">[属性查看构造函数](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx)或[FolderView 构造函数](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx) **pageSize**参数</span><span class="sxs-lookup"><span data-stu-id="12ce0-117">The **pageSize** parameter to the [ItemView constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) or the [FolderView constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span></span> <br/> <span data-ttu-id="12ce0-118">或</span><span class="sxs-lookup"><span data-stu-id="12ce0-118">Or</span></span>  <br/> <span data-ttu-id="12ce0-119">[PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-119">The [PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="12ce0-120">有关[IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)元素的**MaxEntriesReturned**属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-120">The **MaxEntriesReturned** attribute on the [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="12ce0-121">项目或文件夹的列表中的起始点</span><span class="sxs-lookup"><span data-stu-id="12ce0-121">Starting point in the list of items or folders</span></span>  <br/> |<span data-ttu-id="12ce0-122">**属性查看**构造函数或**FolderView**构造函数**offsetBasePoint**参数</span><span class="sxs-lookup"><span data-stu-id="12ce0-122">The **offsetBasePoint** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="12ce0-123">或</span><span class="sxs-lookup"><span data-stu-id="12ce0-123">Or</span></span>  <br/> <span data-ttu-id="12ce0-124">[PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-124">The [PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="12ce0-125">有关**IndexedPageItemView**元素或**IndexedPageFolderView**元素的**基点**属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-125">The **BasePoint** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="12ce0-126">偏移的起始点</span><span class="sxs-lookup"><span data-stu-id="12ce0-126">Offset from the starting point</span></span>  <br/> |<span data-ttu-id="12ce0-127">**Offset**参数**属性查看**构造函数或**FolderView**构造函数</span><span class="sxs-lookup"><span data-stu-id="12ce0-127">The **offset** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="12ce0-128">或</span><span class="sxs-lookup"><span data-stu-id="12ce0-128">Or</span></span>  <br/> <span data-ttu-id="12ce0-129">[PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-129">The [PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="12ce0-130">**IndexedPageItemView**元素或**IndexedPageFolderView**元素上的**偏移**属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-130">The **Offset** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="12ce0-131">在服务器上的结果的总数</span><span class="sxs-lookup"><span data-stu-id="12ce0-131">Total number of results on the server</span></span>  <br/> |<span data-ttu-id="12ce0-132">[FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx)属性或[FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-132">The [FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx) property or the [FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="12ce0-133">有关[RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)元素或[RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)元素的**TotalItemsInView**属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-133">The **TotalItemsInView** attribute on the [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="12ce0-134">第一项或文件夹不包含在当前响应的偏移量</span><span class="sxs-lookup"><span data-stu-id="12ce0-134">Offset of first item or folder not included in current response</span></span>  <br/> |<span data-ttu-id="12ce0-135">[FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx)属性或[FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-135">The [FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx) property or the [FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="12ce0-136">**RootFolder** element 的**IndexedPagingOffset**属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-136">The **IndexedPagingOffset** attribute on the **RootFolder** element</span></span>  <br/> |
|<span data-ttu-id="12ce0-137">响应包括最后一项或文件夹列表中的标记</span><span class="sxs-lookup"><span data-stu-id="12ce0-137">Indicator that response includes the last item or folder in the list</span></span>  <br/> |<span data-ttu-id="12ce0-138">[FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx)属性或[FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-138">The [FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx) property or the [FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="12ce0-139">**RootFolder** element 的**IncludesLastItemInRange**属性</span><span class="sxs-lookup"><span data-stu-id="12ce0-139">The **IncludesLastItemInRange** attribute on the **RootFolder** element</span></span>  <br/> |
   
## <a name="how-paging-works"></a><span data-ttu-id="12ce0-140">分页的工作原理</span><span class="sxs-lookup"><span data-stu-id="12ce0-140">How paging works</span></span>
<span data-ttu-id="12ce0-141"><a name="bk_HowPagingWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="12ce0-141"></span></span>

<span data-ttu-id="12ce0-142">若要了解分页的工作原理，最好可视化为广告牌对齐并排您住宅之外的字段中的文件夹中的邮件。</span><span class="sxs-lookup"><span data-stu-id="12ce0-142">To understand how paging works, it's helpful to visualize the messages in a folder as billboards lined up side by side in a field outside your house.</span></span> <span data-ttu-id="12ce0-143">您可以看到一些这些广告牌通过神奇窗口。</span><span class="sxs-lookup"><span data-stu-id="12ce0-143">You can see some of these billboards through a magical window.</span></span> <span data-ttu-id="12ce0-144">您可以更改窗口 （以同时查看更多或更少广告牌） 的大小和移动窗口 （来控制您可以查看哪些广告牌）。</span><span class="sxs-lookup"><span data-stu-id="12ce0-144">You have the ability to change the size of the window (to see more or fewer billboards at once) and to move the window (to control which billboards you can see).</span></span> <span data-ttu-id="12ce0-145">此操作的窗口进行分页。</span><span class="sxs-lookup"><span data-stu-id="12ce0-145">This manipulation of the window is paging.</span></span> 
  
<span data-ttu-id="12ce0-146">当您的请求发送到 Exchange 服务器上时，您指定要返回的项目数方面窗口的大小。</span><span class="sxs-lookup"><span data-stu-id="12ce0-146">When you send your request to the Exchange server, you specify the size of your window in terms of how many items to return.</span></span> <span data-ttu-id="12ce0-147">您可以通过指定的起始点是 （行的开头） 或行末尾和从该表示中的项目数的起点的偏移量设置窗口的位置。</span><span class="sxs-lookup"><span data-stu-id="12ce0-147">You set the position of the window by specifying a starting point (either the beginning of the line or the end of the line) and an offset from that starting point, expressed in a number of items.</span></span> <span data-ttu-id="12ce0-148">窗口的开头是从起始点的偏移量由指定的项目数。</span><span class="sxs-lookup"><span data-stu-id="12ce0-148">The beginning of the window is the number of items specified by the offset from the starting point.</span></span>
  
<span data-ttu-id="12ce0-149">分页获取更感兴趣的位置是服务器的响应，以及如何应用程序可以使用该响应形状及其下一个请求中。</span><span class="sxs-lookup"><span data-stu-id="12ce0-149">Where paging gets a bit more interesting is in the server's response, and how your application can use that response to shape its next request.</span></span> <span data-ttu-id="12ce0-150">服务器为您提供了三个可用来确定如何配置您在下一个请求"窗口"的信息：</span><span class="sxs-lookup"><span data-stu-id="12ce0-150">The server gives you three pieces of information that you can use to determine how to configure your "window" for your next request:</span></span> 
  
- <span data-ttu-id="12ce0-151">是否在响应中的结果在服务器上设置的总体结果中包括的最后一项。</span><span class="sxs-lookup"><span data-stu-id="12ce0-151">Whether the results in the response include the last item in the overall result set on the server.</span></span>
    
- <span data-ttu-id="12ce0-152">在结果集中在服务器上的项目总数。</span><span class="sxs-lookup"><span data-stu-id="12ce0-152">The total number of items in the result set on the server.</span></span>
    
- <span data-ttu-id="12ce0-153">下一步的偏移的值应是什么，如果您想要前进到当前响应中不包括在结果集中的下一项，您的窗口。</span><span class="sxs-lookup"><span data-stu-id="12ce0-153">What the next offset value should be, if you want to advance your window to the next item in the result set that isn't included in the current response.</span></span>
    
<span data-ttu-id="12ce0-154">让我们看一下简单示例。</span><span class="sxs-lookup"><span data-stu-id="12ce0-154">Let's look at a simple example.</span></span> <span data-ttu-id="12ce0-155">假设包含 15 中的邮件收件箱。</span><span class="sxs-lookup"><span data-stu-id="12ce0-155">Imagine an Inbox with 15 messages in it.</span></span> <span data-ttu-id="12ce0-156">您的应用程序发送初始请求检索最多 10 个项目，开头的列表的邮件 （因此偏移量为零）。</span><span class="sxs-lookup"><span data-stu-id="12ce0-156">Your application sends an initial request to retrieve a maximum of 10 items, starting at the beginning of the list of messages (so the offset is zero).</span></span> <span data-ttu-id="12ce0-157">服务器响应前 10 的消息，并指示响应不包括最后一项，有 15 项的汇总和下一个偏移应为 10。</span><span class="sxs-lookup"><span data-stu-id="12ce0-157">The server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10.</span></span>
  
<span data-ttu-id="12ce0-158">**图 1。请求 10 个项目，在偏移量为 0 列表从头 15 个项目**</span><span class="sxs-lookup"><span data-stu-id="12ce0-158">**Figure 1. Requesting 10 items at offset 0 from the beginning of a list of 15 items**</span></span>

![此图显示从包含 15 个项目的列表开始，在偏移量为 0 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_FirstPage.png)
  
<span data-ttu-id="12ce0-160">在于偏移量现在是 10，则您的应用程序然后重新发送到服务器，更改只使用相同的请求。</span><span class="sxs-lookup"><span data-stu-id="12ce0-160">Your application then resends the same request to the server, with the only change being that the offset is now 10.</span></span> <span data-ttu-id="12ce0-161">服务器返回最近五项，并指示响应，包括最后一项，有 15 项的汇总和下一个偏移应为 15，（尽管当然，您已达到结束时，因此不会有下偏移量。）</span><span class="sxs-lookup"><span data-stu-id="12ce0-161">The server returns the last five items, and indicates that the response does include the last item, that there are a total of 15 items, and that the next offset should be 15 (though of course, you've reached the end, so there won't be a next offset.)</span></span>
  
<span data-ttu-id="12ce0-162">**图 2。请求 10 个项目，在偏移量为 10 列表从头 15 个项目**</span><span class="sxs-lookup"><span data-stu-id="12ce0-162">**Figure 2. Requesting 10 items at offset 10 from the beginning of a list of 15 items**</span></span>

![此图显示从包含 15 个项目的列表开始，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a><span data-ttu-id="12ce0-164">分页的设计注意事项</span><span class="sxs-lookup"><span data-stu-id="12ce0-164">Design considerations for paging</span></span>
<span data-ttu-id="12ce0-165"><a name="bk_DesignConsiderations"> </a></span><span class="sxs-lookup"><span data-stu-id="12ce0-165"></span></span>

<span data-ttu-id="12ce0-166">在您的应用程序中进行最有效地使用分页确实需要一些注意事项。</span><span class="sxs-lookup"><span data-stu-id="12ce0-166">Making the most out of paging in your application does require some consideration.</span></span> <span data-ttu-id="12ce0-167">例如，如何大型使您的"窗口"？</span><span class="sxs-lookup"><span data-stu-id="12ce0-167">For example, how large do you make your "window"?</span></span> <span data-ttu-id="12ce0-168">如果在服务器上的结果时移动您"窗口"更改，则该怎么办？</span><span class="sxs-lookup"><span data-stu-id="12ce0-168">What do you do if the results on the server change while you're moving your "window"?</span></span>
  
### <a name="determine-the-size-of-your-window"></a><span data-ttu-id="12ce0-169">确定您的窗口的大小</span><span class="sxs-lookup"><span data-stu-id="12ce0-169">Determine the size of your window</span></span>

<span data-ttu-id="12ce0-170">最大没有"通用的"所有应用程序应使用的条目数。</span><span class="sxs-lookup"><span data-stu-id="12ce0-170">There is no "one-size-fits-all" maximum number of entries that all applications should use.</span></span> <span data-ttu-id="12ce0-171">确定适合您的应用程序的数量取决于多个不同的因素。</span><span class="sxs-lookup"><span data-stu-id="12ce0-171">Determining the number that's right for your application depends on several different factors.</span></span> <span data-ttu-id="12ce0-172">但是，最好请记住以下准则：</span><span class="sxs-lookup"><span data-stu-id="12ce0-172">However, it's helpful to keep the following guidelines in mind:</span></span>
  
- <span data-ttu-id="12ce0-173">默认情况下，Exchange 限制为 1000年可以在单个请求返回的项的最大数目。</span><span class="sxs-lookup"><span data-stu-id="12ce0-173">By default, Exchange limits the maximum number of items that can be returned in a single request to 1000.</span></span>
    
- <span data-ttu-id="12ce0-174">设置为无需发送较少的请求以获取所有项，但无需再等待响应较大数字会产生的最大项数。</span><span class="sxs-lookup"><span data-stu-id="12ce0-174">Setting the maximum number of entries to a larger number results in having to send fewer requests to get all items, at the cost of having to wait longer for responses.</span></span>
    
- <span data-ttu-id="12ce0-175">更快地响应时间，但无需发送多个请求以获取所有项较小的数字结果设置的最大项数。</span><span class="sxs-lookup"><span data-stu-id="12ce0-175">Setting the maximum number of entries to a smaller number results in quicker response times, at the cost of having to send more requests to get all items.</span></span>
    
### <a name="handling-changes-to-the-result-set"></a><span data-ttu-id="12ce0-176">对结果集的处理更改</span><span class="sxs-lookup"><span data-stu-id="12ce0-176">Handling changes to the result set</span></span>

<span data-ttu-id="12ce0-177">在本文前面的简单示例中，用户的收件箱中的项的数目保持不变。</span><span class="sxs-lookup"><span data-stu-id="12ce0-177">In the simple example earlier in this article, the number of items in the user's Inbox remained constant.</span></span> <span data-ttu-id="12ce0-178">但是，在实际情况下，收件箱中的项目数可以经常更改。</span><span class="sxs-lookup"><span data-stu-id="12ce0-178">However, in reality, the number of items in an Inbox can change frequently.</span></span> <span data-ttu-id="12ce0-179">新邮件可以到达，可以删除或移动随时项。</span><span class="sxs-lookup"><span data-stu-id="12ce0-179">New messages can arrive and items can be deleted or moved at any time.</span></span> <span data-ttu-id="12ce0-180">但此影响分页原理？</span><span class="sxs-lookup"><span data-stu-id="12ce0-180">But how does this impact paging?</span></span> <span data-ttu-id="12ce0-181">我们来修改前面的示例方案，以找出。</span><span class="sxs-lookup"><span data-stu-id="12ce0-181">Let's modify the earlier example scenario to find out.</span></span>
  
<span data-ttu-id="12ce0-182">我们将再次开头的 15 项中用户的收件箱，并发送了相同的初始请求。</span><span class="sxs-lookup"><span data-stu-id="12ce0-182">We'll start again with the 15 items in the user's Inbox, and send the same initial request.</span></span> <span data-ttu-id="12ce0-183">前，服务器将响应前 10 的消息，并指示的响应不包括最后一项，有 15 项的汇总和下一个偏移应为 10，如图 1 中所示。</span><span class="sxs-lookup"><span data-stu-id="12ce0-183">As before, the server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10, as shown in Figure 1.</span></span>
  
<span data-ttu-id="12ce0-184">现在，在您的应用程序处理这些 10 个项目时，新邮件到达收件箱，并添加到服务器上设置的结果。</span><span class="sxs-lookup"><span data-stu-id="12ce0-184">Now, while your application is processing those 10 items, a new message arrives in the Inbox and is added to the result set on the server.</span></span> <span data-ttu-id="12ce0-185">您的应用程序 （仅与偏移量设置为 10） 重新发送到服务器相同的请求。</span><span class="sxs-lookup"><span data-stu-id="12ce0-185">Your application resends the same request to the server (only with the offset set to 10).</span></span> <span data-ttu-id="12ce0-186">这次服务器获取后六个项目，并指示在结果集中的 16 项的汇总。</span><span class="sxs-lookup"><span data-stu-id="12ce0-186">This time the server gets back six items, and indicates that there are a total of 16 items in the result set.</span></span>
  
<span data-ttu-id="12ce0-187">此时您可能想知道是否这甚至一个问题。</span><span class="sxs-lookup"><span data-stu-id="12ce0-187">At this point you might be wondering if this is even a problem.</span></span> <span data-ttu-id="12ce0-188">毕竟，您获取 16 项后通过两种响应，那么，为什么所有都能够轻松处理？</span><span class="sxs-lookup"><span data-stu-id="12ce0-188">After all, you got 16 items back over the two responses, so why all the fuss?</span></span> <span data-ttu-id="12ce0-189">答案取决于新项目的列表中放置位置。</span><span class="sxs-lookup"><span data-stu-id="12ce0-189">The answer depends on where in the list the new item is placed.</span></span> <span data-ttu-id="12ce0-190">对列表进行排序，以便 （通过接收日期/时间） 最早的项目的第一个，在此方案中的问题的任何原因。</span><span class="sxs-lookup"><span data-stu-id="12ce0-190">If the list is sorted so that the oldest items (by received date/time) are first, there's no cause for concern in this scenario.</span></span> <span data-ttu-id="12ce0-191">新项的列表的结尾处，将会发出，并将第二个响应中包括。</span><span class="sxs-lookup"><span data-stu-id="12ce0-191">The new item will be placed at the end of the list, and will be included in the second response.</span></span>
  
<span data-ttu-id="12ce0-192">**图 3。请求 10 个项目在偏移量为 10 16 项目列表的从头与正在新列表中的第 16 项**</span><span class="sxs-lookup"><span data-stu-id="12ce0-192">**Figure 3. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the 16th item in the list being new**</span></span>

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表结束位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
<span data-ttu-id="12ce0-194">如果对列表进行排序，以便最新的项目的第一个，则不同的文章。</span><span class="sxs-lookup"><span data-stu-id="12ce0-194">If the list is sorted so that the newest items are first, it's a different story.</span></span> <span data-ttu-id="12ce0-195">在这种情况下，从以前的请求的最后一项以及从原始 15 剩余的五个项目，将为第二个请求中的第一项。</span><span class="sxs-lookup"><span data-stu-id="12ce0-195">In this case, the first item in the second request would be the last item from the previous request plus the remaining five items from the original 15.</span></span> <span data-ttu-id="12ce0-196">若要将其放在我们虚神奇窗口中，您移动窗口的位置 10，但广告牌本身也移动 1。</span><span class="sxs-lookup"><span data-stu-id="12ce0-196">To put it in terms of our imaginary magical window, you shifted your window's position by 10, but the billboards themselves also shifted by 1.</span></span>
  
<span data-ttu-id="12ce0-197">**图 4。请求在偏移量为 10 16 项目列表的从头正在新列表中的第一项的 10 个项目**</span><span class="sxs-lookup"><span data-stu-id="12ce0-197">**Figure 4. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the first item in the list being new**</span></span>

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表开始位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
<span data-ttu-id="12ce0-199">检测到的服务器上的结果的更改的一种方法是使用定位项目的概念。</span><span class="sxs-lookup"><span data-stu-id="12ce0-199">One way to detect a change to the results on the server is to use the concept of an anchor item.</span></span> <span data-ttu-id="12ce0-200">定位项是您的未处理以及其余的结果，但用于与下一个结果来了解是否具有多项本身进行比较的响应中的其他项。</span><span class="sxs-lookup"><span data-stu-id="12ce0-200">An anchor item is an additional item in your response that is not processed along with the rest of the results, but is used to compare with the next results to see if the items themselves have shifted.</span></span> <span data-ttu-id="12ce0-201">再次在生成简单的示例中，如果您的应用程序使用的"窗口"大小为 10，实际上设置以返回到 11 最大项数。</span><span class="sxs-lookup"><span data-stu-id="12ce0-201">Building again on our simple example, if your application is using a "window" size of 10, you actually set the maximum number of items to return to 11.</span></span> <span data-ttu-id="12ce0-202">您的应用程序像往常一样处理的响应中的前 10 项。</span><span class="sxs-lookup"><span data-stu-id="12ce0-202">Your application processes the first 10 items in the response as usual.</span></span> <span data-ttu-id="12ce0-203">对于最后一项，您的定位点，保存项目的标识符，然后发出下一个请求和偏移量为 10。</span><span class="sxs-lookup"><span data-stu-id="12ce0-203">For the last item, you save the item's identifier as an anchor, then issue the next request with an offset of 10.</span></span> <span data-ttu-id="12ce0-204">如果尚未更改数据，第二个响应中的第一项应匹配定位标记的项标识符。</span><span class="sxs-lookup"><span data-stu-id="12ce0-204">If the data has not changed, the first item in the second response should have an item identifier that matches the anchor.</span></span> <span data-ttu-id="12ce0-205">不匹配的项标识符，如果您知道通过已删除或插入您具有已"分页"列表中的部分数据。</span><span class="sxs-lookup"><span data-stu-id="12ce0-205">If the item identifiers don't match, you know that the data has been removed or inserted in the parts of the list you have already "paged" over.</span></span>
  
<span data-ttu-id="12ce0-206">即使时您知道数据发生更改，仍需要决定如何做出反应。</span><span class="sxs-lookup"><span data-stu-id="12ce0-206">Even when you know that the data has changed, you still need to decide how to react.</span></span> <span data-ttu-id="12ce0-207">没有此问题的通用应答也。</span><span class="sxs-lookup"><span data-stu-id="12ce0-207">There isn't a one-size-fits-all answer for this question either.</span></span> <span data-ttu-id="12ce0-208">您的操作将取决于您的应用程序和捕获所有项目所旨在的关键程度的特性。</span><span class="sxs-lookup"><span data-stu-id="12ce0-208">Your actions will depend on the nature of your application and how critical it is to capture all items.</span></span> <span data-ttu-id="12ce0-209">您可能完全忽略，重新启动从开头、 过程或备份跟踪并尝试检测更改发生了变化。</span><span class="sxs-lookup"><span data-stu-id="12ce0-209">You might ignore it altogether, restart the process from the beginning, or back track and try to detect where the change happened.</span></span>
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a><span data-ttu-id="12ce0-210">示例： 使用 EWS 托管 API 执行分页的搜索</span><span class="sxs-lookup"><span data-stu-id="12ce0-210">Example: Perform a paged search by using the EWS Managed API</span></span>
<span data-ttu-id="12ce0-211"><a name="bk_PagedSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="12ce0-211"></span></span>

<span data-ttu-id="12ce0-212">通过下列 EWS 托管 API 方法支持分页：</span><span class="sxs-lookup"><span data-stu-id="12ce0-212">Paging is supported by the following EWS Managed API methods:</span></span>
  
- [<span data-ttu-id="12ce0-213">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="12ce0-213">ExchangeService.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="12ce0-214">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="12ce0-214">ExchangeService.FindItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="12ce0-215">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="12ce0-215">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="12ce0-216">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="12ce0-216">Folder.FindFolders</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="12ce0-217">如果您使用 EWS 托管 API，您的应用程序与[属性查看](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx)或[FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx)类配置分页，并从服务器接收信息关于从[FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx)或[FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx)分页类。</span><span class="sxs-lookup"><span data-stu-id="12ce0-217">If you are using the EWS Managed API, your application configures paging with the [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) or [FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class and receives information from the server regarding paging from the [FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx) or [FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) class.</span></span> 
  
<span data-ttu-id="12ce0-218">以下示例检索使用每个响应中返回五个项目的分页的搜索文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="12ce0-218">The following example retrieves all the items in a folder using a paged search that returns five items in each response.</span></span> <span data-ttu-id="12ce0-219">它还将检索其他项用作定位来检测到的服务器上的结果的更改。</span><span class="sxs-lookup"><span data-stu-id="12ce0-219">It also retrieves an additional item to serve as an anchor to detect changes to the results on the server.</span></span> 
  
<span data-ttu-id="12ce0-220">本示例假定已初始化**ExchangeService**对象，在[凭据](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。</span><span class="sxs-lookup"><span data-stu-id="12ce0-220">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void PageSearchItems(ExchangeService service, WellKnownFolderName folder)
{
    int pageSize = 5;
    int offset = 0;
    // Request one more item than your actual pageSize.
    // This will be used to detect a change to the result
    // set while paging.
    ItemView view = new ItemView(pageSize + 1, offset);
    view.PropertySet = new PropertySet(ItemSchema.Subject);
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    view.Traversal = ItemTraversal.Shallow;
    bool moreItems = true;
    ItemId anchorId = null;
    while (moreItems)
    {
        try
        {
            FindItemsResults<Item> results = service.FindItems(folder, view);
            moreItems = results.MoreAvailable;
            if (moreItems &amp;&amp; anchorId != null)
            {
                // Check the first result to make sure it matches
                // the last result (anchor) from the previous page.
                // If it doesn't, that means that something was added
                // or deleted since you started the search.
                if (results.Items.First<Item>().Id != anchorId)
                {
                    Console.WriteLine("The collection has changed while paging. Some results may be missed.");
                }
            }
            if (moreItems)
                view.Offset += pageSize;
            anchorId = results.Items.Last<Item>().Id;
            // Because you're including an additional item on the end of your results
            // as an anchor, you don't want to display it.
            // Set the number to loop as the smaller value between
            // the number of items in the collection and the page size.
            int displayCount = results.Items.Count > pageSize ? pageSize : results.Items.Count;
            for (int i = 0; i < displayCount; i++)
            {
                Item item = results.Items[i];
                Console.WriteLine("Subject: {0}", item.Subject);
                Console.WriteLine("Id: {0}\n", item.Id.ToString());
            }
        }
        catch (Exception ex)
        {
            Console.WriteLine("Exception while paging results: {0}", ex.Message);
        }
    }
}
```

## <a name="example-perform-a-paged-search-by-using-ews"></a><span data-ttu-id="12ce0-221">示例： 使用 EWS 执行分页的搜索</span><span class="sxs-lookup"><span data-stu-id="12ce0-221">Example: Perform a paged search by using EWS</span></span>
<span data-ttu-id="12ce0-222"><a name="bk_PagedSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="12ce0-222"></span></span>

<span data-ttu-id="12ce0-223">分页支持以下 EWS 操作：</span><span class="sxs-lookup"><span data-stu-id="12ce0-223">Paging is supported by the following EWS operations:</span></span>
  
- [<span data-ttu-id="12ce0-224">FindFolder</span><span class="sxs-lookup"><span data-stu-id="12ce0-224">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="12ce0-225">FindItem</span><span class="sxs-lookup"><span data-stu-id="12ce0-225">FindItem</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="12ce0-226">如果您正在使用 EWS，您的应用程序将页面配置与[IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)元素，并从服务器接收信息关于从[RootFolder (分页FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)元素或[RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="12ce0-226">If you're using EWS, your application configures paging with the [IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element and receives information from the server regarding paging from the [RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="12ce0-227">在此请求示例中， **FindItem**请求发送的六个项目，在偏移量的用户的收件箱中项目的列表开始从零开始的最大值。</span><span class="sxs-lookup"><span data-stu-id="12ce0-227">In this request example, a **FindItem** request is sent for a maximum of six items, starting at an offset of zero from the beginning of the list of items in the user's Inbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="6" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="12ce0-228">服务器将返回以下响应，其中包含六个项目。</span><span class="sxs-lookup"><span data-stu-id="12ce0-228">The server returns the following response, which contains six items.</span></span> <span data-ttu-id="12ce0-229">响应还指示不存在的服务器上，在结果中的八个项的汇总，并且在结果列表中的最后一项不存在此响应。</span><span class="sxs-lookup"><span data-stu-id="12ce0-229">The response also indicates that there are a total of eight items in the results on the server, and that the last item in the results list is not present in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="6" TotalItemsInView="8" IncludesLastItemInRange="false">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Query</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Update</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Planning resources</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Timeline</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>For your perusal</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="12ce0-230">本示例中，发送了相同的请求，但这次，**偏移量**属性更改为 5，这表明，服务器应返回最多五个从头开始的偏移量处开始六个项。</span><span class="sxs-lookup"><span data-stu-id="12ce0-230">In this example, the same request is sent, but this time, the **Offset** attribute is changed to five, which indicates that the server should return at most six items starting at offset five from the beginning.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Eastern Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="6" Offset="5" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="12ce0-231">服务器发送以下的响应，其中包含三个项目。</span><span class="sxs-lookup"><span data-stu-id="12ce0-231">The server sends the following response, which contains three items.</span></span> <span data-ttu-id="12ce0-232">响应还指示在结果中的服务器上的项目总数仍 8 个，以及该的最后一项在结果列表包含在此响应。</span><span class="sxs-lookup"><span data-stu-id="12ce0-232">The response also indicates that the total number of items in the results on the server is still eight, and that the last item in the results list is included in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>meeting notes</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>Meeting notes</t:Subject>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAMkAGM2..." ChangeKey="CQAAABYA..." />
                <t:Subject>This cat is hilarious!</t:Subject>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="12ce0-233">另请参阅</span><span class="sxs-lookup"><span data-stu-id="12ce0-233">See also</span></span>


- [<span data-ttu-id="12ce0-234">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="12ce0-234">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="12ce0-235">ExchangeService.FindFolders 方法</span><span class="sxs-lookup"><span data-stu-id="12ce0-235">ExchangeService.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="12ce0-236">ExchangeService.FindItems 方法</span><span class="sxs-lookup"><span data-stu-id="12ce0-236">ExchangeService.FindItems method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="12ce0-237">Folder.FindFolders 方法</span><span class="sxs-lookup"><span data-stu-id="12ce0-237">Folder.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="12ce0-238">Folder.FindFolders 方法</span><span class="sxs-lookup"><span data-stu-id="12ce0-238">Folder.FindFolders method</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="12ce0-239">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="12ce0-239">FindFolder operation</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="12ce0-240">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="12ce0-240">FindItem operation</span></span>](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [<span data-ttu-id="12ce0-241">限制在 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="12ce0-241">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

