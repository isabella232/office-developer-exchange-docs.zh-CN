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
# <a name="perform-paged-searches-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 执行分页搜索

了解如何在面向 Exchange 的 EWS 托管 API 或 EWS 应用程序中执行分页搜索。
  
分页是 EWS 中的一项功能，可用于控制搜索结果的大小。 无需通过 EWS 响应检索整个结果集，可通过多个 EWS 响应检索小型集。 例如，如果用户的收件箱中有 10,000 封电子邮件。 理论上你可以在一个极大的响应中检索所有 10,000 封电子邮件，但出于带宽或性能原因，可能需要将其分解为更易管理的区块。 分页为你提供了执行此操作的工具。
  
> [!NOTE]
> 虽然理论上你可以在一个请求中检索 10,000 个项，但实际上，由于 EWS 限制，这不太可能发生。 若要了解详细信息，请参阅 [Exchange 中的 EWS 限制](ews-throttling-in-exchange.md)。 
  
**表1. EWS 托管 API 和 EWS 中的分页参数**

|**若要配置或检索…**|**在 EWS 托管 API 中，使用…**|**在 EWS 中，使用…**|
|:-----|:-----|:-----|
|响应中项目或文件夹的最大数量  <br/> |[ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview.itemview%28v=exchg.80%29.aspx) 构造函数或 [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.folderview%28v=exchg.80%29.aspx) 构造函数的 **pageSize** 参数 <br/> 或  <br/> [PagedView PageSize](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.pagesize%28v=exchg.80%29.aspx) 属性  <br/> |[IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) 元素或 [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) 元素上的 **MaxEntriesReturned** 属性  <br/> |
|项目或文件夹列表中的起始点  <br/> |**ItemView** 构造函数或 **FolderView** 构造函数的 **offsetBasePoint** 参数  <br/> 或  <br/> [PagedView.OffsetBasePoint](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offsetbasepoint%28v=exchg.80%29.aspx) 属性  <br/> |**IndexedPageItemView** 元素或 **IndexedPageFolderView** 元素上的 **BasePoint** 属性  <br/> |
|起始点偏移  <br/> |**ItemView** 构造函数或 **FolderView** 构造函数的 **offset** 参数  <br/> 或  <br/> [PagedView.Offset](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pagedview.offset%28v=exchg.80%29.aspx) 属性  <br/> |**IndexedPageItemView** 元素或 **IndexedPageFolderView** 元素上的 **Offset** 属性  <br/> |
|服务器上的总结果数  <br/> |[FindItemsResults TotalCount](https://msdn.microsoft.com/library/dd635348%28v=exchg.80%29.aspx) 属性或 [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.totalcount%28v=exchg.80%29.aspx) 属性  <br/> |[RootFolder (FindItemResponseMessage)](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) 元素或 [RootFolder (FindFolderResponseMessage)](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) 元素上的 **TotalItemsInView** 属性  <br/> |
|当前响应中未包含的第一个项目或文件夹的偏移量  <br/> |[FindItemsResults NextPageOffset](https://msdn.microsoft.com/library/ee693014%28v=exchg.80%29.aspx) 属性或 [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.nextpageoffset%28v=exchg.80%29.aspx) 属性  <br/> |**RootFolder** 元素上的 **IndexedPagingOffset** 属性  <br/> |
|响应包括列表中的最后一个项目或文件夹的指示器  <br/> |[FindItemsResults.MoreAvailable](https://msdn.microsoft.com/library/dd635477%28v=exchg.80%29.aspx) 属性或 [FindFoldersResults.MoreAvailable](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults.moreavailable%28v=exchg.80%29.aspx) 属性  <br/> |**RootFolder** 元素上的 **IncludesLastItemInRange** 属性  <br/> |
   
## <a name="how-paging-works"></a>分页工作方式
<a name="bk_HowPagingWorks"> </a>

为了理解分页的工作方式，可以将文件夹中的邮件想象成户外并排排列的广告牌。 你可以透过一扇神奇的窗口看到这些广告牌。 你可以更改窗口的大小（一次看到更多或更少的广告牌），也可以移动窗口（控制你可以看到哪些广告牌）。 窗口的这种操作就是分页。 
  
将请求发送到 Exchange 服务器时，可根据要返回的项目数来指定窗口的大小。 可以通过指定起始点（行首或行尾）和从起始点的偏移量（用许多项表示）来设置窗口的位置。 窗口开头是指从起始点到偏移量指定的项目数。
  
分页的有趣之处在于服务器的响应，以及应用程序如何使用该响应来形成它的下一个请求。 服务器提供了三种信息，可用于确定如何为下一次请求配置“窗口”： 
  
- 响应中的结果是否包含服务器上总体结果集中的最后一项。
    
- 服务器上的结果集中的项目总数。
    
- 如果你想将窗口推进到未包含在当前响应中的结果集中的下一个项目，下一个偏移值应该是什么。
    
让我们看一个简单的示例。 假设出收件箱中有 15 封邮件。 应用程序将初始请求检索到最多 10 个项目，从邮件列表的开头开始（因此偏移量为零）。 服务器响应前 10 封邮件，显示该响应不包括最后一个项目，共有 15 个项目，下一个偏移量应为 10。
  
**图 1. 从包含 15 个项目的列表开头处开始，以偏移量 0 请求 10 个项目**

![此图显示从包含 15 个项目的列表开始，在偏移量为 0 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_FirstPage.png)
  
然后，你的应用程序将相同的请求重新发送到服务器，唯一的变化是偏移量现在是10。 服务器返回最后 5 个项目，并指示响应包含最后一个条目，总共有 15 个项目，下一个偏移量应该是 15（当然，已经到达了末尾，所以不会有下一个偏移量）。
  
**图 2. 从包含 15 个项目的列表开头处开始，以偏移量 10 请求 10 个项目**

![此图显示从包含 15 个项目的列表开始，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage.png)
  
## <a name="design-considerations-for-paging"></a>分页的设计注意事项
<a name="bk_DesignConsiderations"> </a>

若要在应用程序中充分利用分页，需要考虑一些事项。 例如，将“窗口”设置为多大？ 如果在移动“窗口”时服务器上的结果发生变化，该怎么办？
  
### <a name="determine-the-size-of-your-window"></a>确定窗口的大小

没有所有应用程序都可使用的“一刀切”的最大条目数。 确定适合你的应用程序的数目取决于几个不同的因素。 但是，请牢记以下准则，这很有帮助：
  
- 默认情况下，Exchange 将单个请求中可以返回的最大项数限制为 1000。
    
- 将条目的最大数量设置得越大，获取所有条目要发送的请求就越少，而响应时间会更长。
    
- 将条目的最大数量设置得越小，响应时间会越快，为了获取所有条目就要发送更多请求。
    
### <a name="handling-changes-to-the-result-set"></a>处理对结果集所做的更改

在本文前面的简单示例中，用户的收件箱中的项目数保持不变。 但是，实际上，收件箱中的项目数可能会频繁更改。 随时可能收到新邮件，删除或移动项目。 这会对分页有何影响？ 我们修改前面的示例场景来找出答案。
  
再从用户收件箱中的 15 个项目开始，然后发送相同的初始请求。 与前面一样，服务器响应前 10 封邮件，显示该响应不包括最后一个项目，共有 15 个项目，下一个偏移量应为 10，如图 1 所示。
  
现在，当你的应用程序处理这 10 个项目时，收件箱收到了一封新邮件，并将其添加到服务器上的结果集中。 应用程序将同一请求重发到服务器（仅使用设置为 10 的偏移量）。 这一次，服务器将返回六个项目，并显示结果集内共 16 个项目。
  
此时，你可能不确定这是否有问题。 毕竟，在两个响应中，你收到了 16 条回复，那么为什么要大惊小怪呢？ 答案取决于列表中新项目的放置位置。 如果已对列表进行排序，将最先收到的项目（按接收日期/时间）排在前面，在这种情况下不会有任何问题。 新项目将位于列表的末尾，包含在第二个响应中。
  
**图 3. 从包含 16 个项目的列表开头处开始，以偏移量 10 请求 10 个项目，新项目排在列表第 16 项**

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表结束位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemEnd.png)
  
如果已对列表排序，使最新项目排在首位，会造成不同的结果。 在这种情况下，第二个请求中的第一个项目是上次请求的最后一个项目加上最初 15 个项目中中剩下的五个。 就我们想象中的神奇窗口而言，你将窗口的位置移动了 10 个位置，但广告牌本身也移动了 1 个位置。
  
**图 4. 从包含 16 个项目的列表开头处开始，以偏移量 10 请求 10 个项目，新项目排在列表第 1 项**

![此图显示从包含 16 个项目的列表开始，当第 16 个项目添加到列表开始位置时，在偏移量为 10 的情况下，请求 10 个项目的结果。](media/Ex15_PagedSearch_SecondPage_NewItemBeginning.png)
  
使用定位项的概念可以检测服务器上的结果更改。 定位项是你的响应中的一个附加项，与其余的结果不一起处理，而是用于与下一个结果进行比较，以确定项本身是否发生了移位。 还是这个简单的示例，如果你的应用程序使用的“窗口”大小为 10，实际上，你设置要返回的最大项目数为 11。 应用程序照常处理响应中的前 10 个项目。 对于最后一个项目，将项目的标识符保存为一定位标记，然后使用偏移量 10 发出下一个请求。 如果数据未更改，则第二个响应中的第一项应具有与定位标记匹配的项目标识符。 如果项目标识符不匹配，你知道数据已被删除或插入到“分页”的列表部分。
  
即使知道数据已更改，仍需决定如何作出反应。 这个问题也没有一个放之四海而皆准的答案。 操作取决于应用程序的特性，以及捕获所有项目的关键程度。 你可以完全忽略它，从开始处重新启动进程，或返回跟踪并尝试检测变化发生的位置。
  
## <a name="example-perform-a-paged-search-by-using-the-ews-managed-api"></a>示例：使用 EWS 托管 API 执行分页搜索
<a name="bk_PagedSearchEWSMA"> </a>

以下 EWS 托管 API 方法支持分页：
  
- [ExchangeService.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
如果你使用的是 EWS 托管 API，你的应用程序将使用 [ItemView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemview%28v=exchg.80%29.aspx) 或 [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) 类配置分页，并从服务器上收到有关从 [FindItemsResults](https://msdn.microsoft.com/library/dd635381%28v=exchg.80%29.aspx) 或 [FindFoldersResults](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.findfoldersresults%28v=exchg.80%29.aspx) 类中分页的信息。 
  
下面的示例使用分页搜索检索文件夹中的所有项目，将在每个响应中返回五个项目。 此外，它还将检索另一个项目，用作定位标记，以检测对服务器上的结果所做的更改。 
  
此示例假定 **ExchangeService** 对象已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)的有效值和 [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) 属性进行了初始化。 
  
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

## <a name="example-perform-a-paged-search-by-using-ews"></a>示例：使用 EWS 执行分页搜索
<a name="bk_PagedSearchEWS"> </a>

以下 EWS 操作支持分页：
  
- [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
如果你使用的是 EWS，你的应用程序将使用 [IndexedPageItemView](https://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) 元素或 [IndexedPageFolderView](https://msdn.microsoft.com/library/c6dac232-244b-4db0-9a15-5e01b8aa7a7d%28Office.15%29.aspx) 元素配置分页，并从服务器上接收关从 [RootFolder （FindItemResponseMessage）](https://msdn.microsoft.com/library/187e009f-efaa-42a8-8962-329a645213ab%28Office.15%29.aspx) 元素或 [RootFolder （FindFolderResponseMessage）](https://msdn.microsoft.com/library/5089c815-663f-46be-bc59-aed9ee20f94a%28Office.15%29.aspx) 元素分页的信息。 
  
在这个请求示例中，**FindItem** 请求最多发送六个项目，从用户收件箱中项目列表开头零偏移量开始。 
  
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

服务器返回以下响应，其中包含六个项目。 该响应还表明服务器上的结果中共有八个项目，并且结果列表中的最后一项未出现在此响应中。
  
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

在此示例中，发送了同一请求，但这一次， **Offset** 属性被更改为五，这表示服务器从开始的偏移量五开始，最多可返回六个项目。 
  
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

服务器发送以下响应，其中包含三个项目。 该响应还表明服务器上的结果中的项目总数仍为八个，并且结果列表中的最后一项包含在此响应中。
  
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

## <a name="see-also"></a>另请参阅


- [搜索和交换中的 EWS](search-and-ews-in-exchange.md)
    
- [ExchangeService.FindFolders 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)
    
- [ExchangeService.FindItems 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)
    
- [Folder.FindFolders 方法](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx)
    
- [FindFolder 操作](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [FindItem 操作](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)
    
- [Exchange 中的 EWS 限制](ews-throttling-in-exchange.md)
    

