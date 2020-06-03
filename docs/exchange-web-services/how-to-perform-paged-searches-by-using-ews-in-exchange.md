---
title: 使用 Exchange 中的 EWS 执行分页搜索
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: 了解如何在面向 Exchange 的 EWS 托管 API 或 EWS 应用程序中执行分页搜索。
localization_priority: Priority
ms.openlocfilehash: 2b608584918c936f62883b8b444d59c05c5952ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456826"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a><span data-ttu-id="bc155-103">使用 Exchange 中的 EWS 执行分页搜索</span><span class="sxs-lookup"><span data-stu-id="bc155-103">Perform paged searches by using EWS in Exchange</span></span>

<span data-ttu-id="bc155-104">了解如何在面向 Exchange 的 EWS 托管 API 或 EWS 应用程序中执行分页搜索。</span><span class="sxs-lookup"><span data-stu-id="bc155-104">Find out how to perform paged searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="bc155-105">分页是 EWS 中的一项功能，使您能够控制搜索结果的大小。</span><span class="sxs-lookup"><span data-stu-id="bc155-105">Paging is a feature in EWS that enables you to control the size of the results of a search.</span></span> <span data-ttu-id="bc155-106">您可以检索多个 EWS 响应中的较小集，而不是在一个 EWS 响应中检索整个结果集。</span><span class="sxs-lookup"><span data-stu-id="bc155-106">Rather than retrieve the entire result set in one EWS response, you can retrieve smaller sets in multiple EWS responses.</span></span> <span data-ttu-id="bc155-107">例如，假设用户的收件箱中有10000封电子邮件。</span><span class="sxs-lookup"><span data-stu-id="bc155-107">For example, consider a user with 10,000 email messages in their Inbox.</span></span> <span data-ttu-id="bc155-108">Hypothetically，您可以在一个非常大的响应中检索所有10000电子邮件，但由于带宽或性能原因，您可能需要将其分解为更易于管理的区块。</span><span class="sxs-lookup"><span data-stu-id="bc155-108">Hypothetically, you could retrieve all 10,000 emails in one very large response, but you might want to break that up into more manageable chunks for bandwidth or performance reasons.</span></span> <span data-ttu-id="bc155-109">分页为您提供了实现此目的的工具。</span><span class="sxs-lookup"><span data-stu-id="bc155-109">Paging gives you the tools to do just that.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bc155-110">虽然您可以 hypothetically 在一个请求中检索10000项，但实际上这不是由于 EWS 限制而造成的。</span><span class="sxs-lookup"><span data-stu-id="bc155-110">While you can hypothetically retrieve 10,000 items in one request, in reality, this is unlikely due to EWS throttling.</span></span> <span data-ttu-id="bc155-111">若要了解详细信息，请参阅[Exchange 中的 EWS 限制](ews-throttling-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="bc155-111">To find out more, see [EWS throttling in Exchange](ews-throttling-in-exchange.md).</span></span> 
  
<span data-ttu-id="bc155-112">**表1。EWS 托管 API 和 EWS 中的分页参数**</span><span class="sxs-lookup"><span data-stu-id="bc155-112">**Table 1. Paging parameters in the EWS Managed API and EWS**</span></span>

|<span data-ttu-id="bc155-113">**若要配置或检索 .。。**</span><span class="sxs-lookup"><span data-stu-id="bc155-113">**To configure or retrieve the…**</span></span>|<span data-ttu-id="bc155-114">**在 EWS 托管 API 中，使用 .。。**</span><span class="sxs-lookup"><span data-stu-id="bc155-114">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="bc155-115">**在 EWS 中，使用 .。。**</span><span class="sxs-lookup"><span data-stu-id="bc155-115">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bc155-116">响应中的最大项目数或文件夹数</span><span class="sxs-lookup"><span data-stu-id="bc155-116">Maximum number of items or folders in a response</span></span>  <br/> |<span data-ttu-id="bc155-117">[ItemView 构造函数](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx)或[FolderView 构造函数](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)的**pageSize**参数</span><span class="sxs-lookup"><span data-stu-id="bc155-117">The **pageSize** parameter to the [ItemView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) or the [FolderView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span></span> <br/> <span data-ttu-id="bc155-118">或</span><span class="sxs-lookup"><span data-stu-id="bc155-118">Or</span></span>  <br/> <span data-ttu-id="bc155-119">[PageSize 属性 PagedView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc155-119">The [PagedView.PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="bc155-120">[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)元素上的**MaxEntriesReturned**属性</span><span class="sxs-lookup"><span data-stu-id="bc155-120">The **MaxEntriesReturned** attribute on the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="bc155-121">项或文件夹列表中的起始点</span><span class="sxs-lookup"><span data-stu-id="bc155-121">Starting point in the list of items or folders</span></span>  <br/> |<span data-ttu-id="bc155-122">**ItemView**构造函数或**FolderView**构造函数的**offsetBasePoint**参数</span><span class="sxs-lookup"><span data-stu-id="bc155-122">The **offsetBasePoint** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="bc155-123">或</span><span class="sxs-lookup"><span data-stu-id="bc155-123">Or</span></span>  <br/> <span data-ttu-id="bc155-124">[OffsetBasePoint 属性 PagedView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc155-124">The [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="bc155-125">**IndexedPageItemView**元素或**IndexedPageFolderView**元素上的**BasePoint**属性</span><span class="sxs-lookup"><span data-stu-id="bc155-125">The **BasePoint** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="bc155-126">起始点的偏移量</span><span class="sxs-lookup"><span data-stu-id="bc155-126">Offset from the starting point</span></span>  <br/> |<span data-ttu-id="bc155-127">**ItemView**构造函数或**FolderView**构造函数的**offset**参数</span><span class="sxs-lookup"><span data-stu-id="bc155-127">The **offset** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="bc155-128">或</span><span class="sxs-lookup"><span data-stu-id="bc155-128">Or</span></span>  <br/> <span data-ttu-id="bc155-129">[PagedView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)属性</span><span class="sxs-lookup"><span data-stu-id="bc155-129">The [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="bc155-130">**IndexedPageItemView**元素或**IndexedPageFolderView**元素上的**Offset**属性</span><span class="sxs-lookup"><span data-stu-id="bc155-130">The **Offset** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="bc155-131">服务器上的总结果数</span><span class="sxs-lookup"><span data-stu-id="bc155-131">Total number of results on the server</span></span>  <br/> |<span data-ttu-id="bc155-132">TotalCount 属性或[FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)属性[FindItemsResults](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc155-132">The [FindItemsResults.TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) property or the [FindFoldersResults.TotalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="bc155-133">[RootFolder （FindItemResponseMessage）](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)元素或[RootFolder （FindFolderResponseMessage）](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)元素上的**TotalItemsInView**属性</span><span class="sxs-lookup"><span data-stu-id="bc155-133">The **TotalItemsInView** attribute on the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="bc155-134">当前响应中未包含的第一个项目或文件夹的偏移量</span><span class="sxs-lookup"><span data-stu-id="bc155-134">Offset of first item or folder not included in current response</span></span>  <br/> |<span data-ttu-id="bc155-135">NextPageOffset 属性或[FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)属性[FindItemsResults](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc155-135">The [FindItemsResults.NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) property or the [FindFoldersResults.NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="bc155-136">**RootFolder**元素上的**IndexedPagingOffset**属性</span><span class="sxs-lookup"><span data-stu-id="bc155-136">The **IndexedPagingOffset** attribute on the **RootFolder** element</span></span>  <br/> |
|<span data-ttu-id="bc155-137">指示符，响应包含列表中的最后一个项目或文件夹</span><span class="sxs-lookup"><span data-stu-id="bc155-137">Indicator that response includes the last item or folder in the list</span></span>  <br/> |<span data-ttu-id="bc155-138">MoreAvailable 属性或[FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)属性[FindItemsResults](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bc155-138">The [FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) property or the [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="bc155-139">**RootFolder**元素上的**IncludesLastItemInRange**属性</span><span class="sxs-lookup"><span data-stu-id="bc155-139">The **IncludesLastItemInRange** attribute on the **RootFolder** element</span></span>  <br/> |
   
## <a name="how-paging-works"></a><span data-ttu-id="bc155-140">分页的工作方式</span><span class="sxs-lookup"><span data-stu-id="bc155-140">How paging works</span></span>
<span data-ttu-id="bc155-141"><a name="bk_HowPagingWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="bc155-141"><a name="bk_HowPagingWorks"> </a></span></span>

<span data-ttu-id="bc155-142">若要了解分页的工作方式，将文件夹中的邮件直观地可视化在房屋外部的字段中，将文件夹中的邮件可视化为 billboards。</span><span class="sxs-lookup"><span data-stu-id="bc155-142">To understand how paging works, it's helpful to visualize the messages in a folder as billboards lined up side by side in a field outside your house.</span></span> <span data-ttu-id="bc155-143">您可以通过神奇窗口查看其中一些 billboards。</span><span class="sxs-lookup"><span data-stu-id="bc155-143">You can see some of these billboards through a magical window.</span></span> <span data-ttu-id="bc155-144">您可以更改窗口的大小（以同时查看更多或更少的 billboards）和移动窗口（以控制您可以查看的 billboards）。</span><span class="sxs-lookup"><span data-stu-id="bc155-144">You have the ability to change the size of the window (to see more or fewer billboards at once) and to move the window (to control which billboards you can see).</span></span> <span data-ttu-id="bc155-145">对窗口的此操作进行分页。</span><span class="sxs-lookup"><span data-stu-id="bc155-145">This manipulation of the window is paging.</span></span> 
  
<span data-ttu-id="bc155-146">当您将请求发送到 Exchange 服务器时，请根据要返回的项目数指定窗口的大小。</span><span class="sxs-lookup"><span data-stu-id="bc155-146">When you send your request to the Exchange server, you specify the size of your window in terms of how many items to return.</span></span> <span data-ttu-id="bc155-147">您可以通过指定起始点（行的开头或结尾的行的开头）和从该起始点开始的偏移量（用多个项目表示）来设置窗口的位置。</span><span class="sxs-lookup"><span data-stu-id="bc155-147">You set the position of the window by specifying a starting point (either the beginning of the line or the end of the line) and an offset from that starting point, expressed in a number of items.</span></span> <span data-ttu-id="bc155-148">窗口的开头是由起始点的偏移量指定的项目数。</span><span class="sxs-lookup"><span data-stu-id="bc155-148">The beginning of the window is the number of items specified by the offset from the starting point.</span></span>
  
<span data-ttu-id="bc155-149">在服务器的响应中，分页变得更有趣，以及应用程序如何使用该响应形状其下一个请求。</span><span class="sxs-lookup"><span data-stu-id="bc155-149">Where paging gets a bit more interesting is in the server's response, and how your application can use that response to shape its next request.</span></span> <span data-ttu-id="bc155-150">服务器提供了三个信息，可用于确定如何为下一个请求配置 "窗口"：</span><span class="sxs-lookup"><span data-stu-id="bc155-150">The server gives you three pieces of information that you can use to determine how to configure your "window" for your next request:</span></span> 
  
- <span data-ttu-id="bc155-151">响应中的结果是否包括服务器上的总体结果集中的最后一项。</span><span class="sxs-lookup"><span data-stu-id="bc155-151">Whether the results in the response include the last item in the overall result set on the server.</span></span>
    
- <span data-ttu-id="bc155-152">服务器上的结果集中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="bc155-152">The total number of items in the result set on the server.</span></span>
    
- <span data-ttu-id="bc155-153">下一个偏移值应是什么，如果您想要将窗口前进到结果集中不包含在当前响应中的下一项。</span><span class="sxs-lookup"><span data-stu-id="bc155-153">What the next offset value should be, if you want to advance your window to the next item in the result set that isn't included in the current response.</span></span>
    
<span data-ttu-id="bc155-154">我们来看看一个简单的示例。</span><span class="sxs-lookup"><span data-stu-id="bc155-154">Let's look at a simple example.</span></span> <span data-ttu-id="bc155-155">设想一下收件箱中有15封邮件。</span><span class="sxs-lookup"><span data-stu-id="bc155-155">Imagine an Inbox with 15 messages in it.</span></span> <span data-ttu-id="bc155-156">您的应用程序发送初始请求，以检索最多10个项目（从邮件列表的开头开始）（因此偏移量为零）。</span><span class="sxs-lookup"><span data-stu-id="bc155-156">Your application sends an initial request to retrieve a maximum of 10 items, starting at the beginning of the list of messages (so the offset is zero).</span></span> <span data-ttu-id="bc155-157">服务器响应前10封邮件，并指示响应不包含最后一项，共15个项目，并且下一个偏移量应为10。</span><span class="sxs-lookup"><span data-stu-id="bc155-157">The server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10.</span></span>
  
<span data-ttu-id="bc155-158">**图1。从15个项目的列表开始处偏移量0请求10个项目**</span><span class="sxs-lookup"><span data-stu-id="bc155-158">**Figure 1. Requesting 10 items at offset 0 from the beginning of a list of 15 items**</span></span>

![此图显示从包含 15 个项目的列表开始，在偏移量为 0 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_FirstPage.png)
  
<span data-ttu-id="bc155-160">然后，您的应用程序会将同一请求重新发送给服务器，只是偏移量现在为10。</span><span class="sxs-lookup"><span data-stu-id="bc155-160">Your application then resends the same request to the server, with the only change being that the offset is now 10.</span></span> <span data-ttu-id="bc155-161">服务器返回最后五个项目，并指示响应包含的最后一项，共15个项目，并且下一个偏移量应为15个（当然，您已经到达结束，因此不会出现下一个偏移量。）</span><span class="sxs-lookup"><span data-stu-id="bc155-161">The server returns the last five items, and indicates that the response does include the last item, that there are a total of 15 items, and that the next offset should be 15 (though of course, you've reached the end, so there won't be a next offset.)</span></span>
  
<span data-ttu-id="bc155-162">**图2。在偏移量10处请求10个项目，从15个项目的列表开始**</span><span class="sxs-lookup"><span data-stu-id="bc155-162">**Figure 2. Requesting 10 items at offset 10 from the beginning of a list of 15 items**</span></span>

![此图显示从包含 15 个项目的列表开始，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a><span data-ttu-id="bc155-164">页面的设计注意事项</span><span class="sxs-lookup"><span data-stu-id="bc155-164">Design considerations for paging</span></span>
<span data-ttu-id="bc155-165"><a name="bk_DesignConsiderations"> </a></span><span class="sxs-lookup"><span data-stu-id="bc155-165"><a name="bk_DesignConsiderations"> </a></span></span>

<span data-ttu-id="bc155-166">在应用程序中最大限度地进行分页确实需要考虑一些事项。</span><span class="sxs-lookup"><span data-stu-id="bc155-166">Making the most out of paging in your application does require some consideration.</span></span> <span data-ttu-id="bc155-167">例如，将 "窗口" 设置为多大？</span><span class="sxs-lookup"><span data-stu-id="bc155-167">For example, how large do you make your "window"?</span></span> <span data-ttu-id="bc155-168">如果您在移动 "窗口" 时服务器上的结果发生了变化，该怎么办？</span><span class="sxs-lookup"><span data-stu-id="bc155-168">What do you do if the results on the server change while you're moving your "window"?</span></span>
  
### <a name="determine-the-size-of-your-window"></a><span data-ttu-id="bc155-169">确定窗口的大小</span><span class="sxs-lookup"><span data-stu-id="bc155-169">Determine the size of your window</span></span>

<span data-ttu-id="bc155-170">所有应用程序都应使用的最大条目数不是 "一种大小适合"。</span><span class="sxs-lookup"><span data-stu-id="bc155-170">There is no "one-size-fits-all" maximum number of entries that all applications should use.</span></span> <span data-ttu-id="bc155-171">确定适合您的应用程序的数量取决于几个不同的因素。</span><span class="sxs-lookup"><span data-stu-id="bc155-171">Determining the number that's right for your application depends on several different factors.</span></span> <span data-ttu-id="bc155-172">但是，请牢记以下准则，这很有帮助：</span><span class="sxs-lookup"><span data-stu-id="bc155-172">However, it's helpful to keep the following guidelines in mind:</span></span>
  
- <span data-ttu-id="bc155-173">默认情况下，Exchange 会将单个请求中可返回的最大项目数限制为1000。</span><span class="sxs-lookup"><span data-stu-id="bc155-173">By default, Exchange limits the maximum number of items that can be returned in a single request to 1000.</span></span>
    
- <span data-ttu-id="bc155-174">将最大条目数设置为较大的数将导致不得不发送较少的请求来获取所有项目，代价是需要等待更长时间进行响应。</span><span class="sxs-lookup"><span data-stu-id="bc155-174">Setting the maximum number of entries to a larger number results in having to send fewer requests to get all items, at the cost of having to wait longer for responses.</span></span>
    
- <span data-ttu-id="bc155-175">将最大条目数设置为较小的数目会导致更快的响应速度，代价是需要发送更多请求来获取所有项目。</span><span class="sxs-lookup"><span data-stu-id="bc155-175">Setting the maximum number of entries to a smaller number results in quicker response times, at the cost of having to send more requests to get all items.</span></span>
    
### <a name="handling-changes-to-the-result-set"></a><span data-ttu-id="bc155-176">处理对结果集所做的更改</span><span class="sxs-lookup"><span data-stu-id="bc155-176">Handling changes to the result set</span></span>

<span data-ttu-id="bc155-177">在本文前面的简单示例中，用户的收件箱中的项目数保持不变。</span><span class="sxs-lookup"><span data-stu-id="bc155-177">In the simple example earlier in this article, the number of items in the user's Inbox remained constant.</span></span> <span data-ttu-id="bc155-178">然而，实际上，收件箱中的项目数可能会经常更改。</span><span class="sxs-lookup"><span data-stu-id="bc155-178">However, in reality, the number of items in an Inbox can change frequently.</span></span> <span data-ttu-id="bc155-179">可以随时删除或删除新邮件，也可以删除或移动项目。</span><span class="sxs-lookup"><span data-stu-id="bc155-179">New messages can arrive and items can be deleted or moved at any time.</span></span> <span data-ttu-id="bc155-180">但这对分页有何影响？</span><span class="sxs-lookup"><span data-stu-id="bc155-180">But how does this impact paging?</span></span> <span data-ttu-id="bc155-181">让我们修改更早的示例方案以了解。</span><span class="sxs-lookup"><span data-stu-id="bc155-181">Let's modify the earlier example scenario to find out.</span></span>
  
<span data-ttu-id="bc155-182">我们将再次从用户的收件箱中的15个项目开始，并发送相同的初始请求。</span><span class="sxs-lookup"><span data-stu-id="bc155-182">We'll start again with the 15 items in the user's Inbox, and send the same initial request.</span></span> <span data-ttu-id="bc155-183">与之前一样，服务器会使用前10封邮件进行响应，并指示响应不包含最后一个项目，总共有15个项目，并且下一个偏移量应为10，如图1所示。</span><span class="sxs-lookup"><span data-stu-id="bc155-183">As before, the server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10, as shown in Figure 1.</span></span>
  
<span data-ttu-id="bc155-184">现在，当您的应用程序处理这10个项目时，新邮件到达收件箱中，并添加到服务器上的结果集中。</span><span class="sxs-lookup"><span data-stu-id="bc155-184">Now, while your application is processing those 10 items, a new message arrives in the Inbox and is added to the result set on the server.</span></span> <span data-ttu-id="bc155-185">应用程序将同一请求重新发送给服务器（仅限偏移量设置为10）。</span><span class="sxs-lookup"><span data-stu-id="bc155-185">Your application resends the same request to the server (only with the offset set to 10).</span></span> <span data-ttu-id="bc155-186">这次，服务器将返回六个项目，并指示结果集中共有16个项目。</span><span class="sxs-lookup"><span data-stu-id="bc155-186">This time the server gets back six items, and indicates that there are a total of 16 items in the result set.</span></span>
  
<span data-ttu-id="bc155-187">此时，您可能会想知道这是否是一个问题。</span><span class="sxs-lookup"><span data-stu-id="bc155-187">At this point you might be wondering if this is even a problem.</span></span> <span data-ttu-id="bc155-188">毕竟，您可以通过两个响应获得16个项目，因此为什么要执行所有 fuss？</span><span class="sxs-lookup"><span data-stu-id="bc155-188">After all, you got 16 items back over the two responses, so why all the fuss?</span></span> <span data-ttu-id="bc155-189">答案取决于在列表中放置新项目的位置。</span><span class="sxs-lookup"><span data-stu-id="bc155-189">The answer depends on where in the list the new item is placed.</span></span> <span data-ttu-id="bc155-190">如果已对列表进行排序，以便首先使用最旧的项目（按接收日期/时间），则在这种情况下不会出现问题。</span><span class="sxs-lookup"><span data-stu-id="bc155-190">If the list is sorted so that the oldest items (by received date/time) are first, there's no cause for concern in this scenario.</span></span> <span data-ttu-id="bc155-191">新项将放置在列表的末尾，并将包含在第二个响应中。</span><span class="sxs-lookup"><span data-stu-id="bc155-191">The new item will be placed at the end of the list, and will be included in the second response.</span></span>
  
<span data-ttu-id="bc155-192">**图3。从16项列表的开头开始，在偏移量10处请求10个项目，列表中的第16项为新项**</span><span class="sxs-lookup"><span data-stu-id="bc155-192">**Figure 3. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the 16th item in the list being new**</span></span>

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表结束位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
<span data-ttu-id="bc155-194">如果对列表进行排序以使最新的项最先开始，则这是一个不同的情景。</span><span class="sxs-lookup"><span data-stu-id="bc155-194">If the list is sorted so that the newest items are first, it's a different story.</span></span> <span data-ttu-id="bc155-195">在这种情况下，第二个请求中的第一项是上一个请求中的最后一项加上剩余的五个项目（来自原始15个项目）。</span><span class="sxs-lookup"><span data-stu-id="bc155-195">In this case, the first item in the second request would be the last item from the previous request plus the remaining five items from the original 15.</span></span> <span data-ttu-id="bc155-196">为了使其成为我们的假想神奇窗口，您将窗口的位置移动了10，但 billboards 本身也会移动1个。</span><span class="sxs-lookup"><span data-stu-id="bc155-196">To put it in terms of our imaginary magical window, you shifted your window's position by 10, but the billboards themselves also shifted by 1.</span></span>
  
<span data-ttu-id="bc155-197">**图4。从16项列表的开头开始，在偏移量10处请求10个项目，列表中的第一个项目为新项目**</span><span class="sxs-lookup"><span data-stu-id="bc155-197">**Figure 4. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the first item in the list being new**</span></span>

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表开始位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
<span data-ttu-id="bc155-199">在服务器上检测对结果所做的更改的一种方法是使用定位项的概念。</span><span class="sxs-lookup"><span data-stu-id="bc155-199">One way to detect a change to the results on the server is to use the concept of an anchor item.</span></span> <span data-ttu-id="bc155-200">定位项是响应中未与结果的其余部分一起处理的其他项目，但用于与下一个结果进行比较，以查看这些项目本身是否发生了移位。</span><span class="sxs-lookup"><span data-stu-id="bc155-200">An anchor item is an additional item in your response that is not processed along with the rest of the results, but is used to compare with the next results to see if the items themselves have shifted.</span></span> <span data-ttu-id="bc155-201">重新构建在简单的示例中，如果您的应用程序使用的是 "窗口" 大小为10，实际上是将要返回的最大项目数设置为11。</span><span class="sxs-lookup"><span data-stu-id="bc155-201">Building again on our simple example, if your application is using a "window" size of 10, you actually set the maximum number of items to return to 11.</span></span> <span data-ttu-id="bc155-202">您的应用程序照常处理响应中的前10个项目。</span><span class="sxs-lookup"><span data-stu-id="bc155-202">Your application processes the first 10 items in the response as usual.</span></span> <span data-ttu-id="bc155-203">对于最后一个项目，将该项目的标识符另存为一个锚点，然后发出偏移量为10的下一个请求。</span><span class="sxs-lookup"><span data-stu-id="bc155-203">For the last item, you save the item's identifier as an anchor, then issue the next request with an offset of 10.</span></span> <span data-ttu-id="bc155-204">如果数据未更改，则第二个响应中的第一项应具有与定位点匹配的项标识符。</span><span class="sxs-lookup"><span data-stu-id="bc155-204">If the data has not changed, the first item in the second response should have an item identifier that matches the anchor.</span></span> <span data-ttu-id="bc155-205">如果项目标识符不匹配，则知道数据已被删除或插入到已 "分页" 的列表的部分。</span><span class="sxs-lookup"><span data-stu-id="bc155-205">If the item identifiers don't match, you know that the data has been removed or inserted in the parts of the list you have already "paged" over.</span></span>
  
<span data-ttu-id="bc155-206">即使您知道数据已更改，您仍需要决定如何反应。</span><span class="sxs-lookup"><span data-stu-id="bc155-206">Even when you know that the data has changed, you still need to decide how to react.</span></span> <span data-ttu-id="bc155-207">没有一个适用于此问题的完全不适合的答案。</span><span class="sxs-lookup"><span data-stu-id="bc155-207">There isn't a one-size-fits-all answer for this question either.</span></span> <span data-ttu-id="bc155-208">您的操作将取决于应用程序的性质以及捕获所有项目的关键程度。</span><span class="sxs-lookup"><span data-stu-id="bc155-208">Your actions will depend on the nature of your application and how critical it is to capture all items.</span></span> <span data-ttu-id="bc155-209">您可以完全忽略它，重新启动进程，或再次跟踪，并尝试检测发生更改的位置。</span><span class="sxs-lookup"><span data-stu-id="bc155-209">You might ignore it altogether, restart the process from the beginning, or back track and try to detect where the change happened.</span></span>
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a><span data-ttu-id="bc155-210">示例：使用 EWS 托管 API 执行分页搜索</span><span class="sxs-lookup"><span data-stu-id="bc155-210">Example: Perform a paged search by using the EWS Managed API</span></span>
<span data-ttu-id="bc155-211"><a name="bk_PagedSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="bc155-211"><a name="bk_PagedSearchEWSMA"> </a></span></span>

<span data-ttu-id="bc155-212">分页受以下 EWS 托管 API 方法支持：</span><span class="sxs-lookup"><span data-stu-id="bc155-212">Paging is supported by the following EWS Managed API methods:</span></span>
  
- [<span data-ttu-id="bc155-213">ExchangeService。 FindFolders</span><span class="sxs-lookup"><span data-stu-id="bc155-213">ExchangeService.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="bc155-214">ExchangeService。 FindItems</span><span class="sxs-lookup"><span data-stu-id="bc155-214">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="bc155-215">FindFolders</span><span class="sxs-lookup"><span data-stu-id="bc155-215">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="bc155-216">FindFolders</span><span class="sxs-lookup"><span data-stu-id="bc155-216">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="bc155-217">如果您使用 EWS 托管 API，应用程序将使用[ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx)或[FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx)类配置分页，并从来自[FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx)或[FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx)类的有关页面的服务器接收相关信息。</span><span class="sxs-lookup"><span data-stu-id="bc155-217">If you are using the EWS Managed API, your application configures paging with the [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) or [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class and receives information from the server regarding paging from the [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) or [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) class.</span></span> 
  
<span data-ttu-id="bc155-218">下面的示例使用分页搜索来检索文件夹中的所有项目，每个响应中返回5个项目。</span><span class="sxs-lookup"><span data-stu-id="bc155-218">The following example retrieves all the items in a folder using a paged search that returns five items in each response.</span></span> <span data-ttu-id="bc155-219">它还会检索另一个项，以用作定位点，以检测对服务器上的结果所做的更改。</span><span class="sxs-lookup"><span data-stu-id="bc155-219">It also retrieves an additional item to serve as an anchor to detect changes to the results on the server.</span></span> 
  
<span data-ttu-id="bc155-220">此示例假定已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性中的有效值对**ExchangeService**对象进行了初始化。</span><span class="sxs-lookup"><span data-stu-id="bc155-220">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="example-perform-a-paged-search-by-using-ews"></a><span data-ttu-id="bc155-221">示例：使用 EWS 执行分页搜索</span><span class="sxs-lookup"><span data-stu-id="bc155-221">Example: Perform a paged search by using EWS</span></span>
<span data-ttu-id="bc155-222"><a name="bk_PagedSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="bc155-222"><a name="bk_PagedSearchEWS"> </a></span></span>

<span data-ttu-id="bc155-223">分页由以下 EWS 操作支持：</span><span class="sxs-lookup"><span data-stu-id="bc155-223">Paging is supported by the following EWS operations:</span></span>
  
- [<span data-ttu-id="bc155-224">FindFolder</span><span class="sxs-lookup"><span data-stu-id="bc155-224">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="bc155-225">FindItem</span><span class="sxs-lookup"><span data-stu-id="bc155-225">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="bc155-226">如果使用的是 EWS，应用程序将使用[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)元素配置分页，并从来自[RootFolder （FindItemResponseMessage）](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)元素或[RootFolder （FindFolderResponseMessage）](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)元素的页面接收有关信息。</span><span class="sxs-lookup"><span data-stu-id="bc155-226">If you're using EWS, your application configures paging with the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element and receives information from the server regarding paging from the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="bc155-227">在此请求示例中， **FindItem**请求最多为6个项目发送，从用户收件箱中的项目列表的开头偏移零处开始。</span><span class="sxs-lookup"><span data-stu-id="bc155-227">In this request example, a **FindItem** request is sent for a maximum of six items, starting at an offset of zero from the beginning of the list of items in the user's Inbox.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="bc155-228">服务器返回以下响应，其中包含六个项目。</span><span class="sxs-lookup"><span data-stu-id="bc155-228">The server returns the following response, which contains six items.</span></span> <span data-ttu-id="bc155-229">该响应还指示服务器上的结果中总共有八项，并且结果列表中的最后一项不存在于此响应中。</span><span class="sxs-lookup"><span data-stu-id="bc155-229">The response also indicates that there are a total of eight items in the results on the server, and that the last item in the results list is not present in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="bc155-230">在此示例中，将发送相同的请求，但这次， **Offset**属性将更改为5，这表示服务器最多应从开头偏移量5处开始返回六个项目。</span><span class="sxs-lookup"><span data-stu-id="bc155-230">In this example, the same request is sent, but this time, the **Offset** attribute is changed to five, which indicates that the server should return at most six items starting at offset five from the beginning.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="bc155-231">服务器发送以下响应，其中包含三个项目。</span><span class="sxs-lookup"><span data-stu-id="bc155-231">The server sends the following response, which contains three items.</span></span> <span data-ttu-id="bc155-232">该响应还指示服务器上的结果中的项目总数仍为8，并且结果列表中的最后一个项目包含在此响应中。</span><span class="sxs-lookup"><span data-stu-id="bc155-232">The response also indicates that the total number of items in the results on the server is still eight, and that the last item in the results list is included in this response.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="775" MinorBuildNumber="35" Version="V2_4" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="see-also"></a><span data-ttu-id="bc155-233">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bc155-233">See also</span></span>


- [<span data-ttu-id="bc155-234">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="bc155-234">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="bc155-235">ExchangeService 方法</span><span class="sxs-lookup"><span data-stu-id="bc155-235">ExchangeService.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="bc155-236">ExchangeService 方法</span><span class="sxs-lookup"><span data-stu-id="bc155-236">ExchangeService.FindItems method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="bc155-237">FindFolders 方法</span><span class="sxs-lookup"><span data-stu-id="bc155-237">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="bc155-238">FindFolders 方法</span><span class="sxs-lookup"><span data-stu-id="bc155-238">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="bc155-239">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="bc155-239">FindFolder operation</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="bc155-240">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="bc155-240">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [<span data-ttu-id="bc155-241">Exchange 中的 EWS 限制</span><span class="sxs-lookup"><span data-stu-id="bc155-241">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

