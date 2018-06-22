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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19752864"
---
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a>在 Exchange 使用 EWS 执行分页的搜索

了解如何在您的 EWS 托管 API 或 Exchange 的 EWS 应用程序执行分页的搜索。
  
分页是使您能够控制搜索结果的大小的 EWS 中的功能。 而不是检索整个结果集一个 EWS 响应中，您可以检索在多个 EWS 响应中较小的集。 例如，假设有 10,000 其收件箱中的电子邮件的用户。 假设您无法检索一个非常大的响应，所有 10,000 电子邮件，但您可能想要的拆分到更易于管理的区块带宽或性能原因。 分页为您提供的工具，做到这一点。
  
> [!NOTE]
> 时您可以假定 10,000 以检索项目一个请求，实际上，这是由于 EWS 限制太。 若要了解更多信息，请参阅[EWS 限制在 Exchange](ews-throttling-in-exchange.md)。 
  
**表 1。EWS 托管 API 和 EWS 中的分页参数**

|**若要配置或检索...**|**EWS 托管 API，在使用...**|**EWS，在使用...**|
|:-----|:-----|:-----|
|项目或文件夹的响应中的最大数量  <br/> |[属性查看构造函数](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx)或[FolderView 构造函数](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx) **pageSize**参数 <br/> 或  <br/> [PagedView.PageSize](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx)属性  <br/> |有关[IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)元素的**MaxEntriesReturned**属性  <br/> |
|项目或文件夹的列表中的起始点  <br/> |**属性查看**构造函数或**FolderView**构造函数**offsetBasePoint**参数  <br/> 或  <br/> [PagedView.OffsetBasePoint](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx)属性  <br/> |有关**IndexedPageItemView**元素或**IndexedPageFolderView**元素的**基点**属性  <br/> |
|偏移的起始点  <br/> |**Offset**参数**属性查看**构造函数或**FolderView**构造函数  <br/> 或  <br/> [PagedView.Offset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx)属性  <br/> |**IndexedPageItemView**元素或**IndexedPageFolderView**元素上的**偏移**属性  <br/> |
|在服务器上的结果的总数  <br/> |[FindItemsResults.TotalCount](http://msdn.microsoft.com/en-us/library/dd635348%28v=exchg.80%29.aspx)属性或[FindFoldersResults.TotalCount](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx)属性  <br/> |有关[RootFolder (FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)元素或[RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)元素的**TotalItemsInView**属性  <br/> |
|第一项或文件夹不包含在当前响应的偏移量  <br/> |[FindItemsResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/ee693014%28v=exchg.80%29.aspx)属性或[FindFoldersResults.NextPageOffset](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx)属性  <br/> |**RootFolder** element 的**IndexedPagingOffset**属性  <br/> |
|响应包括最后一项或文件夹列表中的标记  <br/> |[FindItemsResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/dd635477%28v=exchg.80%29.aspx)属性或[FindFoldersResults.MoreAvailable](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx)属性  <br/> |**RootFolder** element 的**IncludesLastItemInRange**属性  <br/> |
   
## <a name="how-paging-works"></a>分页的工作原理
<a name="bk_HowPagingWorks"> </a>

若要了解分页的工作原理，最好可视化为广告牌对齐并排您住宅之外的字段中的文件夹中的邮件。 您可以看到一些这些广告牌通过神奇窗口。 您可以更改窗口 （以同时查看更多或更少广告牌） 的大小和移动窗口 （来控制您可以查看哪些广告牌）。 此操作的窗口进行分页。 
  
当您的请求发送到 Exchange 服务器上时，您指定要返回的项目数方面窗口的大小。 您可以通过指定的起始点是 （行的开头） 或行末尾和从该表示中的项目数的起点的偏移量设置窗口的位置。 窗口的开头是从起始点的偏移量由指定的项目数。
  
分页获取更感兴趣的位置是服务器的响应，以及如何应用程序可以使用该响应形状及其下一个请求中。 服务器为您提供了三个可用来确定如何配置您在下一个请求"窗口"的信息： 
  
- 是否在响应中的结果在服务器上设置的总体结果中包括的最后一项。
    
- 在结果集中在服务器上的项目总数。
    
- 下一步的偏移的值应是什么，如果您想要前进到当前响应中不包括在结果集中的下一项，您的窗口。
    
让我们看一下简单示例。 假设包含 15 中的邮件收件箱。 您的应用程序发送初始请求检索最多 10 个项目，开头的列表的邮件 （因此偏移量为零）。 服务器响应前 10 的消息，并指示响应不包括最后一项，有 15 项的汇总和下一个偏移应为 10。
  
**图 1。请求 10 个项目，在偏移量为 0 列表从头 15 个项目**

![此图显示从包含 15 个项目的列表开始，在偏移量为 0 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_FirstPage.png)
  
在于偏移量现在是 10，则您的应用程序然后重新发送到服务器，更改只使用相同的请求。 服务器返回最近五项，并指示响应，包括最后一项，有 15 项的汇总和下一个偏移应为 15，（尽管当然，您已达到结束时，因此不会有下偏移量。）
  
**图 2。请求 10 个项目，在偏移量为 10 列表从头 15 个项目**

![此图显示从包含 15 个项目的列表开始，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a>分页的设计注意事项
<a name="bk_DesignConsiderations"> </a>

在您的应用程序中进行最有效地使用分页确实需要一些注意事项。 例如，如何大型使您的"窗口"？ 如果在服务器上的结果时移动您"窗口"更改，则该怎么办？
  
### <a name="determine-the-size-of-your-window"></a>确定您的窗口的大小

最大没有"通用的"所有应用程序应使用的条目数。 确定适合您的应用程序的数量取决于多个不同的因素。 但是，最好请记住以下准则：
  
- 默认情况下，Exchange 限制为 1000年可以在单个请求返回的项的最大数目。
    
- 设置为无需发送较少的请求以获取所有项，但无需再等待响应较大数字会产生的最大项数。
    
- 更快地响应时间，但无需发送多个请求以获取所有项较小的数字结果设置的最大项数。
    
### <a name="handling-changes-to-the-result-set"></a>对结果集的处理更改

在本文前面的简单示例中，用户的收件箱中的项的数目保持不变。 但是，在实际情况下，收件箱中的项目数可以经常更改。 新邮件可以到达，可以删除或移动随时项。 但此影响分页原理？ 我们来修改前面的示例方案，以找出。
  
我们将再次开头的 15 项中用户的收件箱，并发送了相同的初始请求。 前，服务器将响应前 10 的消息，并指示的响应不包括最后一项，有 15 项的汇总和下一个偏移应为 10，如图 1 中所示。
  
现在，在您的应用程序处理这些 10 个项目时，新邮件到达收件箱，并添加到服务器上设置的结果。 您的应用程序 （仅与偏移量设置为 10） 重新发送到服务器相同的请求。 这次服务器获取后六个项目，并指示在结果集中的 16 项的汇总。
  
此时您可能想知道是否这甚至一个问题。 毕竟，您获取 16 项后通过两种响应，那么，为什么所有都能够轻松处理？ 答案取决于新项目的列表中放置位置。 对列表进行排序，以便 （通过接收日期/时间） 最早的项目的第一个，在此方案中的问题的任何原因。 新项的列表的结尾处，将会发出，并将第二个响应中包括。
  
**图 3。请求 10 个项目在偏移量为 10 16 项目列表的从头与正在新列表中的第 16 项**

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表结束位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
如果对列表进行排序，以便最新的项目的第一个，则不同的文章。 在这种情况下，从以前的请求的最后一项以及从原始 15 剩余的五个项目，将为第二个请求中的第一项。 若要将其放在我们虚神奇窗口中，您移动窗口的位置 10，但广告牌本身也移动 1。
  
**图 4。请求在偏移量为 10 16 项目列表的从头正在新列表中的第一项的 10 个项目**

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表开始位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
检测到的服务器上的结果的更改的一种方法是使用定位项目的概念。 定位项是您的未处理以及其余的结果，但用于与下一个结果来了解是否具有多项本身进行比较的响应中的其他项。 再次在生成简单的示例中，如果您的应用程序使用的"窗口"大小为 10，实际上设置以返回到 11 最大项数。 您的应用程序像往常一样处理的响应中的前 10 项。 对于最后一项，您的定位点，保存项目的标识符，然后发出下一个请求和偏移量为 10。 如果尚未更改数据，第二个响应中的第一项应匹配定位标记的项标识符。 不匹配的项标识符，如果您知道通过已删除或插入您具有已"分页"列表中的部分数据。
  
即使时您知道数据发生更改，仍需要决定如何做出反应。 没有此问题的通用应答也。 您的操作将取决于您的应用程序和捕获所有项目所旨在的关键程度的特性。 您可能完全忽略，重新启动从开头、 过程或备份跟踪并尝试检测更改发生了变化。
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a>示例： 使用 EWS 托管 API 执行分页的搜索
<a name="bk_PagedSearchEWSMA"> </a>

通过下列 EWS 托管 API 方法支持分页：
  
- [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
如果您使用 EWS 托管 API，您的应用程序与[属性查看](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx)或[FolderView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx)类配置分页，并从服务器接收信息关于从[FindItemsResults](http://msdn.microsoft.com/en-us/library/dd635381%28v=exchg.80%29.aspx)或[FindFoldersResults](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx)分页类。 
  
以下示例检索使用每个响应中返回五个项目的分页的搜索文件夹中的所有项目。 它还将检索其他项用作定位来检测到的服务器上的结果的更改。 
  
本示例假定已初始化**ExchangeService**对象，在[凭据](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。 
  
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

## <a name="example-perform-a-paged-search-by-using-ews"></a>示例： 使用 EWS 执行分页的搜索
<a name="bk_PagedSearchEWS"> </a>

分页支持以下 EWS 操作：
  
- [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
如果您正在使用 EWS，您的应用程序将页面配置与[IndexedPageItemView](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx)元素或[IndexedPageFolderView](http://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx)元素，并从服务器接收信息关于从[RootFolder (分页FindItemResponseMessage)](http://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx)元素或[RootFolder (FindFolderResponseMessage)](http://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx)元素。 
  
在此请求示例中， **FindItem**请求发送的六个项目，在偏移量的用户的收件箱中项目的列表开始从零开始的最大值。 
  
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

服务器将返回以下响应，其中包含六个项目。 响应还指示不存在的服务器上，在结果中的八个项的汇总，并且在结果列表中的最后一项不存在此响应。
  
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

本示例中，发送了相同的请求，但这次，**偏移量**属性更改为 5，这表明，服务器应返回最多五个从头开始的偏移量处开始六个项。 
  
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

服务器发送以下的响应，其中包含三个项目。 响应还指示在结果中的服务器上的项目总数仍 8 个，以及该的最后一项在结果列表包含在此响应。
  
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

## <a name="see-also"></a>另请参阅


- [搜索和交换中的 EWS](search-and-ews-in-exchange.md)
    
- [ExchangeService.FindFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders 方法](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [FindFolder Operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem 操作](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [限制在 Exchange 中的 EWS](ews-throttling-in-exchange.md)
    

