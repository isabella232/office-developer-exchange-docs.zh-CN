---
title: 使用 Exchange 中的 EWS 执行分页搜索
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 64ed70e4-32eb-4c25-bfc4-43d1477296e5
description: 了解如何在面向 Exchange 的 EWS 托管 API 或 EWS 应用程序中执行分页搜索。
localization_priority: Priority
ms.openlocfilehash: fa36a2ce77150f29e5a62876138c9693a3b4ab1f
ms.sourcegitcommit: 37d4ecd4f469690ba1de87baad2f2f58c40c96ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "49348820"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a><span data-ttu-id="21c3a-103">使用 Exchange 中的 EWS 执行分页搜索</span><span class="sxs-lookup"><span data-stu-id="21c3a-103">Perform paged searches by using EWS in Exchange</span></span>

<span data-ttu-id="21c3a-104">了解如何在面向 Exchange 的 EWS 托管 API 或 EWS 应用程序中执行分页搜索。</span><span class="sxs-lookup"><span data-stu-id="21c3a-104">Find out how to perform paged searches in your EWS Managed API or EWS application that targets Exchange.</span></span>
  
<span data-ttu-id="21c3a-105">分页是 EWS 中的一项功能，可用于控制搜索结果的大小。</span><span class="sxs-lookup"><span data-stu-id="21c3a-105">Paging is a feature in EWS that enables you to control the size of the results of a search.</span></span> <span data-ttu-id="21c3a-106">无需通过 EWS 响应检索整个结果集，可通过多个 EWS 响应检索小型集。</span><span class="sxs-lookup"><span data-stu-id="21c3a-106">Rather than retrieve the entire result set in one EWS response, you can retrieve smaller sets in multiple EWS responses.</span></span> <span data-ttu-id="21c3a-107">例如，如果用户的收件箱中有 10,000 封电子邮件。</span><span class="sxs-lookup"><span data-stu-id="21c3a-107">For example, consider a user with 10,000 email messages in their Inbox.</span></span> <span data-ttu-id="21c3a-108">理论上你可以在一个极大的响应中检索所有 10,000 封电子邮件，但出于带宽或性能原因，可能需要将其分解为更易管理的区块。</span><span class="sxs-lookup"><span data-stu-id="21c3a-108">Hypothetically, you could retrieve all 10,000 emails in one very large response, but you might want to break that up into more manageable chunks for bandwidth or performance reasons.</span></span> <span data-ttu-id="21c3a-109">分页为你提供了执行此操作的工具。</span><span class="sxs-lookup"><span data-stu-id="21c3a-109">Paging gives you the tools to do just that.</span></span>
  
> [!NOTE]
> <span data-ttu-id="21c3a-110">虽然理论上你可以在一个请求中检索 10,000 个项，但实际上，由于 EWS 限制，这不太可能发生。</span><span class="sxs-lookup"><span data-stu-id="21c3a-110">While you can hypothetically retrieve 10,000 items in one request, in reality, this is unlikely due to EWS throttling.</span></span> <span data-ttu-id="21c3a-111">若要了解详细信息，请参阅 [Exchange 中的 EWS 限制](ews-throttling-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="21c3a-111">To find out more, see [EWS throttling in Exchange](ews-throttling-in-exchange.md).</span></span> 
  
<span data-ttu-id="21c3a-112">**表1. EWS 托管 API 和 EWS 中的分页参数**</span><span class="sxs-lookup"><span data-stu-id="21c3a-112">**Table 1. Paging parameters in the EWS Managed API and EWS**</span></span>

|<span data-ttu-id="21c3a-113">**若要配置或检索…**</span><span class="sxs-lookup"><span data-stu-id="21c3a-113">**To configure or retrieve the…**</span></span>|<span data-ttu-id="21c3a-114">**在 EWS 托管 API 中，使用…**</span><span class="sxs-lookup"><span data-stu-id="21c3a-114">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="21c3a-115">**在 EWS 中，使用…**</span><span class="sxs-lookup"><span data-stu-id="21c3a-115">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="21c3a-116">响应中项目或文件夹的最大数量</span><span class="sxs-lookup"><span data-stu-id="21c3a-116">Maximum number of items or folders in a response</span></span>  <br/> |<span data-ttu-id="21c3a-117">[ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) 构造函数或 [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx) 构造函数的 **pageSize** 参数</span><span class="sxs-lookup"><span data-stu-id="21c3a-117">The **pageSize** parameter to the [ItemView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) or the [FolderView constructor](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx)</span></span> <br/> <span data-ttu-id="21c3a-118">或</span><span class="sxs-lookup"><span data-stu-id="21c3a-118">Or</span></span>  <br/> <span data-ttu-id="21c3a-119">[PagedView PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-119">The [PagedView.PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="21c3a-120">[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) 元素或 [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) 元素上的 **MaxEntriesReturned** 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-120">The **MaxEntriesReturned** attribute on the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="21c3a-121">项目或文件夹列表中的起始点</span><span class="sxs-lookup"><span data-stu-id="21c3a-121">Starting point in the list of items or folders</span></span>  <br/> |<span data-ttu-id="21c3a-122">**ItemView** 构造函数或 **FolderView** 构造函数的 **offsetBasePoint** 参数</span><span class="sxs-lookup"><span data-stu-id="21c3a-122">The **offsetBasePoint** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="21c3a-123">或</span><span class="sxs-lookup"><span data-stu-id="21c3a-123">Or</span></span>  <br/> <span data-ttu-id="21c3a-124">[PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-124">The [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="21c3a-125">**IndexedPageItemView** 元素或 **IndexedPageFolderView** 元素上的 **BasePoint** 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-125">The **BasePoint** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="21c3a-126">起始点偏移</span><span class="sxs-lookup"><span data-stu-id="21c3a-126">Offset from the starting point</span></span>  <br/> |<span data-ttu-id="21c3a-127">**ItemView** 构造函数或 **FolderView** 构造函数的 **offset** 参数</span><span class="sxs-lookup"><span data-stu-id="21c3a-127">The **offset** parameter to the **ItemView** constructor or the **FolderView** constructor</span></span>  <br/> <span data-ttu-id="21c3a-128">或</span><span class="sxs-lookup"><span data-stu-id="21c3a-128">Or</span></span>  <br/> <span data-ttu-id="21c3a-129">[PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-129">The [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="21c3a-130">**IndexedPageItemView** 元素或 **IndexedPageFolderView** 元素上的 **Offset** 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-130">The **Offset** attribute on the **IndexedPageItemView** element or the **IndexedPageFolderView** element</span></span>  <br/> |
|<span data-ttu-id="21c3a-131">服务器上的总结果数</span><span class="sxs-lookup"><span data-stu-id="21c3a-131">Total number of results on the server</span></span>  <br/> |<span data-ttu-id="21c3a-132">[FindItemsResults TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) 属性或 [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-132">The [FindItemsResults.TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) property or the [FindFoldersResults.TotalCount](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="21c3a-133">[RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) 元素或 [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) 元素上的 **TotalItemsInView** 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-133">The **TotalItemsInView** attribute on the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element</span></span>  <br/> |
|<span data-ttu-id="21c3a-134">当前响应中未包含的第一个项目或文件夹的偏移量</span><span class="sxs-lookup"><span data-stu-id="21c3a-134">Offset of first item or folder not included in current response</span></span>  <br/> |<span data-ttu-id="21c3a-135">[FindItemsResults NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) 属性或 [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-135">The [FindItemsResults.NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) property or the [FindFoldersResults.NextPageOffset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="21c3a-136">**RootFolder** 元素上的 **IndexedPagingOffset** 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-136">The **IndexedPagingOffset** attribute on the **RootFolder** element</span></span>  <br/> |
|<span data-ttu-id="21c3a-137">响应包括列表中的最后一个项目或文件夹的指示器</span><span class="sxs-lookup"><span data-stu-id="21c3a-137">Indicator that response includes the last item or folder in the list</span></span>  <br/> |<span data-ttu-id="21c3a-138">[FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) 属性或 [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-138">The [FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) property or the [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) property</span></span>  <br/> |<span data-ttu-id="21c3a-139">**RootFolder** 元素上的 **IncludesLastItemInRange** 属性</span><span class="sxs-lookup"><span data-stu-id="21c3a-139">The **IncludesLastItemInRange** attribute on the **RootFolder** element</span></span>  <br/> |
   
## <a name="how-paging-works"></a><span data-ttu-id="21c3a-140">分页工作方式</span><span class="sxs-lookup"><span data-stu-id="21c3a-140">How paging works</span></span>
<span data-ttu-id="21c3a-141"><a name="bk_HowPagingWorks"> </a></span><span class="sxs-lookup"><span data-stu-id="21c3a-141"><a name="bk_HowPagingWorks"> </a></span></span>

<span data-ttu-id="21c3a-142">为了理解分页的工作方式，可以将文件夹中的邮件想象成户外并排排列的广告牌。</span><span class="sxs-lookup"><span data-stu-id="21c3a-142">To understand how paging works, it's helpful to visualize the messages in a folder as billboards lined up side by side in a field outside your house.</span></span> <span data-ttu-id="21c3a-143">你可以透过一扇神奇的窗口看到这些广告牌。</span><span class="sxs-lookup"><span data-stu-id="21c3a-143">You can see some of these billboards through a magical window.</span></span> <span data-ttu-id="21c3a-144">你可以更改窗口的大小（一次看到更多或更少的广告牌），也可以移动窗口（控制你可以看到哪些广告牌）。</span><span class="sxs-lookup"><span data-stu-id="21c3a-144">You have the ability to change the size of the window (to see more or fewer billboards at once) and to move the window (to control which billboards you can see).</span></span> <span data-ttu-id="21c3a-145">窗口的这种操作就是分页。</span><span class="sxs-lookup"><span data-stu-id="21c3a-145">This manipulation of the window is paging.</span></span> 
  
<span data-ttu-id="21c3a-146">将请求发送到 Exchange 服务器时，可根据要返回的项目数来指定窗口的大小。</span><span class="sxs-lookup"><span data-stu-id="21c3a-146">When you send your request to the Exchange server, you specify the size of your window in terms of how many items to return.</span></span> <span data-ttu-id="21c3a-147">可以通过指定起始点（行首或行尾）和从起始点的偏移量（用许多项表示）来设置窗口的位置。</span><span class="sxs-lookup"><span data-stu-id="21c3a-147">You set the position of the window by specifying a starting point (either the beginning of the line or the end of the line) and an offset from that starting point, expressed in a number of items.</span></span> <span data-ttu-id="21c3a-148">窗口开头是指从起始点到偏移量指定的项目数。</span><span class="sxs-lookup"><span data-stu-id="21c3a-148">The beginning of the window is the number of items specified by the offset from the starting point.</span></span>
  
<span data-ttu-id="21c3a-149">分页的有趣之处在于服务器的响应，以及应用程序如何使用该响应来形成它的下一个请求。</span><span class="sxs-lookup"><span data-stu-id="21c3a-149">Where paging gets a bit more interesting is in the server's response, and how your application can use that response to shape its next request.</span></span> <span data-ttu-id="21c3a-150">服务器提供了三种信息，可用于确定如何为下一次请求配置“窗口”：</span><span class="sxs-lookup"><span data-stu-id="21c3a-150">The server gives you three pieces of information that you can use to determine how to configure your "window" for your next request:</span></span> 
  
- <span data-ttu-id="21c3a-151">响应中的结果是否包含服务器上总体结果集中的最后一项。</span><span class="sxs-lookup"><span data-stu-id="21c3a-151">Whether the results in the response include the last item in the overall result set on the server.</span></span>
    
- <span data-ttu-id="21c3a-152">服务器上的结果集中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="21c3a-152">The total number of items in the result set on the server.</span></span>
    
- <span data-ttu-id="21c3a-153">如果你想将窗口推进到未包含在当前响应中的结果集中的下一个项目，下一个偏移值应该是什么。</span><span class="sxs-lookup"><span data-stu-id="21c3a-153">What the next offset value should be, if you want to advance your window to the next item in the result set that isn't included in the current response.</span></span>
    
<span data-ttu-id="21c3a-154">让我们看一个简单的示例。</span><span class="sxs-lookup"><span data-stu-id="21c3a-154">Let's look at a simple example.</span></span> <span data-ttu-id="21c3a-155">假设出收件箱中有 15 封邮件。</span><span class="sxs-lookup"><span data-stu-id="21c3a-155">Imagine an Inbox with 15 messages in it.</span></span> <span data-ttu-id="21c3a-156">应用程序将初始请求检索到最多 10 个项目，从邮件列表的开头开始（因此偏移量为零）。</span><span class="sxs-lookup"><span data-stu-id="21c3a-156">Your application sends an initial request to retrieve a maximum of 10 items, starting at the beginning of the list of messages (so the offset is zero).</span></span> <span data-ttu-id="21c3a-157">服务器响应前 10 封邮件，显示该响应不包括最后一个项目，共有 15 个项目，下一个偏移量应为 10。</span><span class="sxs-lookup"><span data-stu-id="21c3a-157">The server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10.</span></span>
  
<span data-ttu-id="21c3a-158">**图 1. 从包含 15 个项目的列表开头处开始，以偏移量 0 请求 10 个项目**</span><span class="sxs-lookup"><span data-stu-id="21c3a-158">**Figure 1. Requesting 10 items at offset 0 from the beginning of a list of 15 items**</span></span>

![此图显示从包含 15 个项目的列表开始，在偏移量为 0 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_FirstPage.png)
  
<span data-ttu-id="21c3a-160">然后，你的应用程序将相同的请求重新发送到服务器，唯一的变化是偏移量现在是10。</span><span class="sxs-lookup"><span data-stu-id="21c3a-160">Your application then resends the same request to the server, with the only change being that the offset is now 10.</span></span> <span data-ttu-id="21c3a-161">服务器返回最后 5 个项目，并指示响应包含最后一个条目，总共有 15 个项目，下一个偏移量应该是 15（当然，已经到达了末尾，所以不会有下一个偏移量）。</span><span class="sxs-lookup"><span data-stu-id="21c3a-161">The server returns the last five items, and indicates that the response does include the last item, that there are a total of 15 items, and that the next offset should be 15 (though of course, you've reached the end, so there won't be a next offset.)</span></span>
  
<span data-ttu-id="21c3a-162">**图 2. 从包含 15 个项目的列表开头处开始，以偏移量 10 请求 10 个项目**</span><span class="sxs-lookup"><span data-stu-id="21c3a-162">**Figure 2. Requesting 10 items at offset 10 from the beginning of a list of 15 items**</span></span>

![此图显示从包含 15 个项目的列表开始，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a><span data-ttu-id="21c3a-164">分页的设计注意事项</span><span class="sxs-lookup"><span data-stu-id="21c3a-164">Design considerations for paging</span></span>
<span data-ttu-id="21c3a-165"><a name="bk_DesignConsiderations"> </a></span><span class="sxs-lookup"><span data-stu-id="21c3a-165"><a name="bk_DesignConsiderations"> </a></span></span>

<span data-ttu-id="21c3a-166">若要在应用程序中充分利用分页，需要考虑一些事项。</span><span class="sxs-lookup"><span data-stu-id="21c3a-166">Making the most out of paging in your application does require some consideration.</span></span> <span data-ttu-id="21c3a-167">例如，将“窗口”设置为多大？</span><span class="sxs-lookup"><span data-stu-id="21c3a-167">For example, how large do you make your "window"?</span></span> <span data-ttu-id="21c3a-168">如果在移动“窗口”时服务器上的结果发生变化，该怎么办？</span><span class="sxs-lookup"><span data-stu-id="21c3a-168">What do you do if the results on the server change while you're moving your "window"?</span></span>
  
### <a name="determine-the-size-of-your-window"></a><span data-ttu-id="21c3a-169">确定窗口的大小</span><span class="sxs-lookup"><span data-stu-id="21c3a-169">Determine the size of your window</span></span>

<span data-ttu-id="21c3a-170">没有所有应用程序都可使用的“一刀切”的最大条目数。</span><span class="sxs-lookup"><span data-stu-id="21c3a-170">There is no "one-size-fits-all" maximum number of entries that all applications should use.</span></span> <span data-ttu-id="21c3a-171">确定适合你的应用程序的数目取决于几个不同的因素。</span><span class="sxs-lookup"><span data-stu-id="21c3a-171">Determining the number that's right for your application depends on several different factors.</span></span> <span data-ttu-id="21c3a-172">但是，请牢记以下准则，这很有帮助：</span><span class="sxs-lookup"><span data-stu-id="21c3a-172">However, it's helpful to keep the following guidelines in mind:</span></span>
  
- <span data-ttu-id="21c3a-173">默认情况下，Exchange 将单个请求中可以返回的最大项数限制为 1000。</span><span class="sxs-lookup"><span data-stu-id="21c3a-173">By default, Exchange limits the maximum number of items that can be returned in a single request to 1000.</span></span>
    
- <span data-ttu-id="21c3a-174">将条目的最大数量设置得越大，获取所有条目要发送的请求就越少，而响应时间会更长。</span><span class="sxs-lookup"><span data-stu-id="21c3a-174">Setting the maximum number of entries to a larger number results in having to send fewer requests to get all items, at the cost of having to wait longer for responses.</span></span>
    
- <span data-ttu-id="21c3a-175">将条目的最大数量设置得越小，响应时间会越快，为了获取所有条目就要发送更多请求。</span><span class="sxs-lookup"><span data-stu-id="21c3a-175">Setting the maximum number of entries to a smaller number results in quicker response times, at the cost of having to send more requests to get all items.</span></span>
    
### <a name="handling-changes-to-the-result-set"></a><span data-ttu-id="21c3a-176">处理对结果集所做的更改</span><span class="sxs-lookup"><span data-stu-id="21c3a-176">Handling changes to the result set</span></span>

<span data-ttu-id="21c3a-177">在本文前面的简单示例中，用户的收件箱中的项目数保持不变。</span><span class="sxs-lookup"><span data-stu-id="21c3a-177">In the simple example earlier in this article, the number of items in the user's Inbox remained constant.</span></span> <span data-ttu-id="21c3a-178">但是，实际上，收件箱中的项目数可能会频繁更改。</span><span class="sxs-lookup"><span data-stu-id="21c3a-178">However, in reality, the number of items in an Inbox can change frequently.</span></span> <span data-ttu-id="21c3a-179">随时可能收到新邮件，删除或移动项目。</span><span class="sxs-lookup"><span data-stu-id="21c3a-179">New messages can arrive and items can be deleted or moved at any time.</span></span> <span data-ttu-id="21c3a-180">这会对分页有何影响？</span><span class="sxs-lookup"><span data-stu-id="21c3a-180">But how does this impact paging?</span></span> <span data-ttu-id="21c3a-181">我们修改前面的示例场景来找出答案。</span><span class="sxs-lookup"><span data-stu-id="21c3a-181">Let's modify the earlier example scenario to find out.</span></span>
  
<span data-ttu-id="21c3a-182">再从用户收件箱中的 15 个项目开始，然后发送相同的初始请求。</span><span class="sxs-lookup"><span data-stu-id="21c3a-182">We'll start again with the 15 items in the user's Inbox, and send the same initial request.</span></span> <span data-ttu-id="21c3a-183">与前面一样，服务器响应前 10 封邮件，显示该响应不包括最后一个项目，共有 15 个项目，下一个偏移量应为 10，如图 1 所示。</span><span class="sxs-lookup"><span data-stu-id="21c3a-183">As before, the server responds with the first 10 messages, and indicates that the response does not include the last item, that there are a total of 15 items, and that the next offset should be 10, as shown in Figure 1.</span></span>
  
<span data-ttu-id="21c3a-184">现在，当你的应用程序处理这 10 个项目时，收件箱收到了一封新邮件，并将其添加到服务器上的结果集中。</span><span class="sxs-lookup"><span data-stu-id="21c3a-184">Now, while your application is processing those 10 items, a new message arrives in the Inbox and is added to the result set on the server.</span></span> <span data-ttu-id="21c3a-185">应用程序将同一请求重发到服务器（仅使用设置为 10 的偏移量）。</span><span class="sxs-lookup"><span data-stu-id="21c3a-185">Your application resends the same request to the server (only with the offset set to 10).</span></span> <span data-ttu-id="21c3a-186">这一次，服务器将返回六个项目，并显示结果集内共 16 个项目。</span><span class="sxs-lookup"><span data-stu-id="21c3a-186">This time the server gets back six items, and indicates that there are a total of 16 items in the result set.</span></span>
  
<span data-ttu-id="21c3a-187">此时，你可能不确定这是否有问题。</span><span class="sxs-lookup"><span data-stu-id="21c3a-187">At this point you might be wondering if this is even a problem.</span></span> <span data-ttu-id="21c3a-188">毕竟，在两个响应中，你收到了 16 条回复，那么为什么要大惊小怪呢？</span><span class="sxs-lookup"><span data-stu-id="21c3a-188">After all, you got 16 items back over the two responses, so why all the fuss?</span></span> <span data-ttu-id="21c3a-189">答案取决于列表中新项目的放置位置。</span><span class="sxs-lookup"><span data-stu-id="21c3a-189">The answer depends on where in the list the new item is placed.</span></span> <span data-ttu-id="21c3a-190">如果已对列表进行排序，将最先收到的项目（按接收日期/时间）排在前面，在这种情况下不会有任何问题。</span><span class="sxs-lookup"><span data-stu-id="21c3a-190">If the list is sorted so that the oldest items (by received date/time) are first, there's no cause for concern in this scenario.</span></span> <span data-ttu-id="21c3a-191">新项目将位于列表的末尾，包含在第二个响应中。</span><span class="sxs-lookup"><span data-stu-id="21c3a-191">The new item will be placed at the end of the list, and will be included in the second response.</span></span>
  
<span data-ttu-id="21c3a-192">**图 3. 从包含 16 个项目的列表开头处开始，以偏移量 10 请求 10 个项目，新项目排在列表第 16 项**</span><span class="sxs-lookup"><span data-stu-id="21c3a-192">**Figure 3. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the 16th item in the list being new**</span></span>

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表结束位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
<span data-ttu-id="21c3a-194">如果已对列表排序，使最新项目排在首位，会造成不同的结果。</span><span class="sxs-lookup"><span data-stu-id="21c3a-194">If the list is sorted so that the newest items are first, it's a different story.</span></span> <span data-ttu-id="21c3a-195">在这种情况下，第二个请求中的第一个项目是上次请求的最后一个项目加上最初 15 个项目中中剩下的五个。</span><span class="sxs-lookup"><span data-stu-id="21c3a-195">In this case, the first item in the second request would be the last item from the previous request plus the remaining five items from the original 15.</span></span> <span data-ttu-id="21c3a-196">就我们想象中的神奇窗口而言，你将窗口的位置移动了 10 个位置，但广告牌本身也移动了 1 个位置。</span><span class="sxs-lookup"><span data-stu-id="21c3a-196">To put it in terms of our imaginary magical window, you shifted your window's position by 10, but the billboards themselves also shifted by 1.</span></span>
  
<span data-ttu-id="21c3a-197">**图 4. 从包含 16 个项目的列表开头处开始，以偏移量 10 请求 10 个项目，新项目排在列表第 1 项**</span><span class="sxs-lookup"><span data-stu-id="21c3a-197">**Figure 4. Requesting 10 items at offset 10 from the beginning of a list of 16 items, with the first item in the list being new**</span></span>

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表开始位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
<span data-ttu-id="21c3a-199">使用定位项的概念可以检测服务器上的结果更改。</span><span class="sxs-lookup"><span data-stu-id="21c3a-199">One way to detect a change to the results on the server is to use the concept of an anchor item.</span></span> <span data-ttu-id="21c3a-200">定位项是你的响应中的一个附加项，与其余的结果不一起处理，而是用于与下一个结果进行比较，以确定项本身是否发生了移位。</span><span class="sxs-lookup"><span data-stu-id="21c3a-200">An anchor item is an additional item in your response that is not processed along with the rest of the results, but is used to compare with the next results to see if the items themselves have shifted.</span></span> <span data-ttu-id="21c3a-201">还是这个简单的示例，如果你的应用程序使用的“窗口”大小为 10，实际上，你设置要返回的最大项目数为 11。</span><span class="sxs-lookup"><span data-stu-id="21c3a-201">Building again on our simple example, if your application is using a "window" size of 10, you actually set the maximum number of items to return to 11.</span></span> <span data-ttu-id="21c3a-202">应用程序照常处理响应中的前 10 个项目。</span><span class="sxs-lookup"><span data-stu-id="21c3a-202">Your application processes the first 10 items in the response as usual.</span></span> <span data-ttu-id="21c3a-203">对于最后一个项目，将项目的标识符保存为一定位标记，然后使用偏移量 10 发出下一个请求。</span><span class="sxs-lookup"><span data-stu-id="21c3a-203">For the last item, you save the item's identifier as an anchor, then issue the next request with an offset of 10.</span></span> <span data-ttu-id="21c3a-204">如果数据未更改，则第二个响应中的第一项应具有与定位标记匹配的项目标识符。</span><span class="sxs-lookup"><span data-stu-id="21c3a-204">If the data has not changed, the first item in the second response should have an item identifier that matches the anchor.</span></span> <span data-ttu-id="21c3a-205">如果项目标识符不匹配，你知道数据已被删除或插入到“分页”的列表部分。</span><span class="sxs-lookup"><span data-stu-id="21c3a-205">If the item identifiers don't match, you know that the data has been removed or inserted in the parts of the list you have already "paged" over.</span></span>
  
<span data-ttu-id="21c3a-206">即使知道数据已更改，仍需决定如何作出反应。</span><span class="sxs-lookup"><span data-stu-id="21c3a-206">Even when you know that the data has changed, you still need to decide how to react.</span></span> <span data-ttu-id="21c3a-207">这个问题也没有一个放之四海而皆准的答案。</span><span class="sxs-lookup"><span data-stu-id="21c3a-207">There isn't a one-size-fits-all answer for this question either.</span></span> <span data-ttu-id="21c3a-208">操作取决于应用程序的特性，以及捕获所有项目的关键程度。</span><span class="sxs-lookup"><span data-stu-id="21c3a-208">Your actions will depend on the nature of your application and how critical it is to capture all items.</span></span> <span data-ttu-id="21c3a-209">你可以完全忽略它，从开始处重新启动进程，或返回跟踪并尝试检测变化发生的位置。</span><span class="sxs-lookup"><span data-stu-id="21c3a-209">You might ignore it altogether, restart the process from the beginning, or back track and try to detect where the change happened.</span></span>
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a><span data-ttu-id="21c3a-210">示例：使用 EWS 托管 API 执行分页搜索</span><span class="sxs-lookup"><span data-stu-id="21c3a-210">Example: Perform a paged search by using the EWS Managed API</span></span>
<span data-ttu-id="21c3a-211"><a name="bk_PagedSearchEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="21c3a-211"><a name="bk_PagedSearchEWSMA"> </a></span></span>

<span data-ttu-id="21c3a-212">以下 EWS 托管 API 方法支持分页：</span><span class="sxs-lookup"><span data-stu-id="21c3a-212">Paging is supported by the following EWS Managed API methods:</span></span>
  
- [<span data-ttu-id="21c3a-213">ExchangeService.FindFolders</span><span class="sxs-lookup"><span data-stu-id="21c3a-213">ExchangeService.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="21c3a-214">ExchangeService.FindItems</span><span class="sxs-lookup"><span data-stu-id="21c3a-214">ExchangeService.FindItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="21c3a-215">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="21c3a-215">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="21c3a-216">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="21c3a-216">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
<span data-ttu-id="21c3a-217">如果你使用的是 EWS 托管 API，你的应用程序将使用 [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) 或 [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) 类配置分页，并从服务器上收到有关从 [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) 或 [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) 类中分页的信息。</span><span class="sxs-lookup"><span data-stu-id="21c3a-217">If you are using the EWS Managed API, your application configures paging with the [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) or [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class and receives information from the server regarding paging from the [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) or [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) class.</span></span> 
  
<span data-ttu-id="21c3a-218">下面的示例使用分页搜索检索文件夹中的所有项目，将在每个响应中返回五个项目。</span><span class="sxs-lookup"><span data-stu-id="21c3a-218">The following example retrieves all the items in a folder using a paged search that returns five items in each response.</span></span> <span data-ttu-id="21c3a-219">此外，它还将检索另一个项目，用作定位标记，以检测对服务器上的结果所做的更改。</span><span class="sxs-lookup"><span data-stu-id="21c3a-219">It also retrieves an additional item to serve as an anchor to detect changes to the results on the server.</span></span> 
  
<span data-ttu-id="21c3a-220">此示例假定 **ExchangeService** 对象已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)的有效值和 [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) 属性进行了初始化。</span><span class="sxs-lookup"><span data-stu-id="21c3a-220">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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
            if (moreItems && anchorId != null)
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
            int displayCount = 0;
            if ((results.MoreAvailable == false && results.Items.Count > pageSize) || (results.Items.Count < pageSize))
            {
                displayCount = results.Items.Count;
            }
            else
            {
                displayCount = pageSize;
            }
            
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

## <a name="example-perform-a-paged-search-by-using-ews"></a><span data-ttu-id="21c3a-221">示例：使用 EWS 执行分页搜索</span><span class="sxs-lookup"><span data-stu-id="21c3a-221">Example: Perform a paged search by using EWS</span></span>
<span data-ttu-id="21c3a-222"><a name="bk_PagedSearchEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="21c3a-222"><a name="bk_PagedSearchEWS"> </a></span></span>

<span data-ttu-id="21c3a-223">以下 EWS 操作支持分页：</span><span class="sxs-lookup"><span data-stu-id="21c3a-223">Paging is supported by the following EWS operations:</span></span>
  
- [<span data-ttu-id="21c3a-224">FindFolder</span><span class="sxs-lookup"><span data-stu-id="21c3a-224">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="21c3a-225">FindItem</span><span class="sxs-lookup"><span data-stu-id="21c3a-225">FindItem</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
<span data-ttu-id="21c3a-226">如果你使用的是 EWS，你的应用程序将使用 [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) 元素或 [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) 元素配置分页，并从服务器上接收关从 [RootFolder （FindItemResponseMessage）](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) 元素或 [RootFolder （FindFolderResponseMessage）](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) 元素分页的信息。</span><span class="sxs-lookup"><span data-stu-id="21c3a-226">If you're using EWS, your application configures paging with the [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) element or the [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) element and receives information from the server regarding paging from the [RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) element or the [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) element.</span></span> 
  
<span data-ttu-id="21c3a-227">在这个请求示例中，**FindItem** 请求最多发送六个项目，从用户收件箱中项目列表开头零偏移量开始。</span><span class="sxs-lookup"><span data-stu-id="21c3a-227">In this request example, a **FindItem** request is sent for a maximum of six items, starting at an offset of zero from the beginning of the list of items in the user's Inbox.</span></span> 
  
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

<span data-ttu-id="21c3a-228">服务器返回以下响应，其中包含六个项目。</span><span class="sxs-lookup"><span data-stu-id="21c3a-228">The server returns the following response, which contains six items.</span></span> <span data-ttu-id="21c3a-229">该响应还表明服务器上的结果中共有八个项目，并且结果列表中的最后一项未出现在此响应中。</span><span class="sxs-lookup"><span data-stu-id="21c3a-229">The response also indicates that there are a total of eight items in the results on the server, and that the last item in the results list is not present in this response.</span></span>
  
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

<span data-ttu-id="21c3a-230">在此示例中，发送了同一请求，但这一次， **Offset** 属性被更改为五，这表示服务器从开始的偏移量五开始，最多可返回六个项目。</span><span class="sxs-lookup"><span data-stu-id="21c3a-230">In this example, the same request is sent, but this time, the **Offset** attribute is changed to five, which indicates that the server should return at most six items starting at offset five from the beginning.</span></span> 
  
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

<span data-ttu-id="21c3a-231">服务器发送以下响应，其中包含三个项目。</span><span class="sxs-lookup"><span data-stu-id="21c3a-231">The server sends the following response, which contains three items.</span></span> <span data-ttu-id="21c3a-232">该响应还表明服务器上的结果中的项目总数仍为八个，并且结果列表中的最后一项包含在此响应中。</span><span class="sxs-lookup"><span data-stu-id="21c3a-232">The response also indicates that the total number of items in the results on the server is still eight, and that the last item in the results list is included in this response.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="21c3a-233">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21c3a-233">See also</span></span>


- [<span data-ttu-id="21c3a-234">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="21c3a-234">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="21c3a-235">ExchangeService.FindFolders 方法</span><span class="sxs-lookup"><span data-stu-id="21c3a-235">ExchangeService.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="21c3a-236">ExchangeService.FindItems 方法</span><span class="sxs-lookup"><span data-stu-id="21c3a-236">ExchangeService.FindItems method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="21c3a-237">Folder.FindFolders 方法</span><span class="sxs-lookup"><span data-stu-id="21c3a-237">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="21c3a-238">Folder.FindFolders 方法</span><span class="sxs-lookup"><span data-stu-id="21c3a-238">Folder.FindFolders method</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="21c3a-239">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="21c3a-239">FindFolder operation</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="21c3a-240">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="21c3a-240">FindItem operation</span></span>](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [<span data-ttu-id="21c3a-241">Exchange 中的 EWS 限制</span><span class="sxs-lookup"><span data-stu-id="21c3a-241">EWS throttling in Exchange</span></span>](ews-throttling-in-exchange.md)
    

