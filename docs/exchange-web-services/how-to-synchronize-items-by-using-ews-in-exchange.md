---
title: 使用 EWS 在 Exchange 同步的项目
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 886e7d35-9096-480b-8a8c-a7db27da06c2
description: 了解如何使用 EWS 托管 API 或 EWS 获取中的列表的所有项目的文件夹或已发生更改的列表在文件夹中，以便同步您的客户端。
ms.openlocfilehash: ce29a77cee595c2358441e4a22d32d45e78c6e60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752886"
---
# <a name="synchronize-items-by-using-ews-in-exchange"></a><span data-ttu-id="c42fb-103">使用 EWS 在 Exchange 同步的项目</span><span class="sxs-lookup"><span data-stu-id="c42fb-103">Synchronize items by using EWS in Exchange</span></span>

<span data-ttu-id="c42fb-104">了解如何使用 EWS 托管 API 或 EWS 获取中的列表的所有项目的文件夹或已发生更改的列表在文件夹中，以便同步您的客户端。</span><span class="sxs-lookup"><span data-stu-id="c42fb-104">Find out how to use the EWS Managed API or EWS to get a list of all items in a folder, or a list of changes that have occurred in a folder, in order to synchronize your client.</span></span>
  
<span data-ttu-id="c42fb-105">Exchange 中的 EWS 使用项目同步和文件夹同步到客户端和服务器之间同步邮箱内容。</span><span class="sxs-lookup"><span data-stu-id="c42fb-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="c42fb-106">项目同步文件夹中获取项目的初始列表，然后随时间推移，获取已对这些项目并获取新的项的更改。</span><span class="sxs-lookup"><span data-stu-id="c42fb-106">Item synchronization gets the initial list of items in a folder and then, over time, gets changes that have been made to those items and gets new items as well.</span></span>
  
<span data-ttu-id="c42fb-107">请注意，您可以同步到客户端的项目之前，首先必须同步[文件夹层次结构](how-to-synchronize-folders-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="c42fb-107">Note that before you can sync items to a client, you first have to [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="c42fb-108">后文件夹层次结构是就地客户端，如果您正在使用 EWS 托管 API，您第一个[获取收件箱中项目的初始列表](#bk_cesyncongoingewsma)使用[ExchangeService.SyncFolderItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)方法执行项目同步。</span><span class="sxs-lookup"><span data-stu-id="c42fb-108">After the folder hierarchy is in place on the client, if you're performing item synchronization by using the EWS Managed API, you first [get the initial list of items in the Inbox](#bk_cesyncongoingewsma) by using the [ExchangeService.SyncFolderItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="c42fb-109">您然后过程后续呼叫，以获取已更改项目的列表中的收件箱中更新_cSyncState_参数的值。</span><span class="sxs-lookup"><span data-stu-id="c42fb-109">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of changed items in the Inbox.</span></span> 
  
<span data-ttu-id="c42fb-110">若要执行项目同步使用 EWS，[同步文件夹层次结构](how-to-synchronize-folders-by-using-ews-in-exchange.md)后，您请求[的收件箱中项目的初始列表](#bk_ewsexamplea)使用[SyncFolderItems 操作](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)中，分析响应，然后在某个点，在将来[邮箱中获取项目更改的](#bk_ewsexamplec)，并分析响应。</span><span class="sxs-lookup"><span data-stu-id="c42fb-110">To perform item synchronization by using EWS, after you [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md), you request the [initial list of items in the Inbox](#bk_ewsexamplea) by using the [SyncFolderItems operation](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx), parse the response, and then at some point in the future [get the changes to the items in the mailbox](#bk_ewsexamplec), and parse the response.</span></span> <span data-ttu-id="c42fb-111">客户端接收初始或已更改项目的列表后，它[使本地更新](#bk_nextsteps)。</span><span class="sxs-lookup"><span data-stu-id="c42fb-111">After the client receives the list of initial or changed items, it [makes updates locally](#bk_nextsteps).</span></span> <span data-ttu-id="c42fb-112">如何以及何时将来检索更改取决于您的应用程序正在使用[同步设计模式](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns)。</span><span class="sxs-lookup"><span data-stu-id="c42fb-112">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-items-or-changed-items-by-using-the-ews-managed-api"></a><span data-ttu-id="c42fb-113">使用 EWS 托管 API 获取所有项或已更改的项的列表</span><span class="sxs-lookup"><span data-stu-id="c42fb-113">Get the list of all items or changed items by using the EWS Managed API</span></span>
<span data-ttu-id="c42fb-114"><a name="bk_cesyncongoingewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="c42fb-114"></span></span>

<span data-ttu-id="c42fb-115">下面的代码示例演示如何获取收件箱文件夹中的所有项目的初始列表，然后自上次同步后发生的收件箱文件夹中获取列表项的更改。</span><span class="sxs-lookup"><span data-stu-id="c42fb-115">The following code example shows how to get an initial list of all items in the Inbox folder and then get a list of changes to items in the Inbox folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="c42fb-116">初始呼叫期间[SyncFolderItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)方法，将_cSyncState_值设置为 null。</span><span class="sxs-lookup"><span data-stu-id="c42fb-116">During the initial call to the [SyncFolderItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="c42fb-117">该方法完成后，保存_cSyncState_值本地以在下一个**SyncFolderItems**方法调用中使用。</span><span class="sxs-lookup"><span data-stu-id="c42fb-117">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderItems** method call.</span></span> <span data-ttu-id="c42fb-118">在初始调用和后续呼叫，批次的 10，直到没有更多更改保持使用连续**SyncFolderItems**方法调用中检索项目。</span><span class="sxs-lookup"><span data-stu-id="c42fb-118">In both the initial call and the subsequent calls, the items are retrieved in batches of ten, by using successive calls to the **SyncFolderItems** method, until no more changes remain.</span></span> 
  
<span data-ttu-id="c42fb-119">本示例将_属性集_参数设置为 IdOnly 以减少与 Exchange 数据库，这是一种[同步的最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c42fb-119">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="c42fb-120">本示例中，我们假定**服务**是一个有效的**ExchangeService**对象绑定并该_cSyncState_代表已由以前**SyncFolderItems**调用返回的同步状态。</span><span class="sxs-lookup"><span data-stu-id="c42fb-120">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderItems**.</span></span> 
  
```cs
// Track whether there are more items available for download on the server.
bool moreChangesAvailable = false;
do
{
    // Get a list of all items in the Inbox by calling SyncFolderHierarchy repeatedly until no more changes are available.
    // The folderId parameter must be set to the root folder to synchronize,
    // and must be same folder ID as used in previous synchronization calls. 
    // The propertySet parameter is set to IdOnly to reduce calls to the Exchange database,
    // because any additional properties result in additional calls to the Exchange database. 
    // The ignoredItemIds parameter is set to null, so that no items are ignored.
    // The maxChangesReturned parameter is set to return a maximum of 10 items (512 is the maximum).
    // The syncScope parameter is set to Normal items, so that associated items will not be returned.
    // The syncState parameter is set to cSyncState, which should be null in the initial call, 
    // and should be set to the sync state returned by the 
    // previous SyncFolderItems call in subsequent calls.
    ChangeCollection<ItemChange> icc = service.SyncFolderItems(new FolderId(WellKnownFolderName.Inbox), PropertySet.IdOnly, null, 10, SyncFolderItemsScope.NormalItems, cSyncState);
    // If the count of changes is zero, there are no changes to synchronize.
    if (icc.Count == 0)
    {
        Console.WriteLine("There are no item changes to synchronize.");
    }
    // Otherwise, write all the changes included in the response 
    // to the console. 
    else
    {
        foreach (ItemChange ic in icc)
        {
            Console.WriteLine("ChangeType: " + ic.ChangeType.ToString());
            Console.WriteLine("ItemId: " + ic.ItemId);
            Console.WriteLine("===========");
        }
    }
    // Save the sync state for use in future SyncFolderContent requests.
    // The sync state is used by the server to determine what changes to report
    // to the client.
    string sSyncState = icc.SyncState;
   // Determine whether more changes are available on the server.
   moreChangesAvailable = icc.MoreChangesAvailable;
}
while (moreChangesAvailable);

```

它不能返回属性，如[正文](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx)或[附件](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.attachments%28v=exchg.80%29.aspx) **SyncFolderItems**方法类似于[FindItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法。 <span data-ttu-id="c42fb-122">如果您需要无法由**SyncFolderItems**方法返回的属性，指定时调用**SyncFolderItems**，然后使用[ExchangeService.LoadPropertiesForItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)方法以获取设置的[IdOnly](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx)属性您需要**SyncFolderItems**方法已返回的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="c42fb-122">If you need properties that cannot be returned by the **SyncFolderItems** method, specify the [IdOnly](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.propertyset.idonly%28v=exchg.80%29.aspx) property set when you call **SyncFolderItems**, and then use the [ExchangeService.LoadPropertiesForItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) method to get the properties you require for the items that were returned by the **SyncFolderItems** method.</span></span> 
  
<span data-ttu-id="c42fb-123">后检索新的或更改在服务器上，[创建或更新客户端上的项目](#bk_nextsteps)的项目的列表。</span><span class="sxs-lookup"><span data-stu-id="c42fb-123">After you retrieve the list of new or changed items on the server, [create or update the items on the client](#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-items-by-using-ews"></a><span data-ttu-id="c42fb-124">使用 EWS 获取项目的初始列表</span><span class="sxs-lookup"><span data-stu-id="c42fb-124">Get the initial list of items by using EWS</span></span>
<span data-ttu-id="c42fb-125"><a name="bk_ewsexamplea"> </a></span><span class="sxs-lookup"><span data-stu-id="c42fb-125"></span></span>

<span data-ttu-id="c42fb-126">下面的示例演示 XML 请求使用[SyncFolderItems 操作](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)获取收件箱中项目的初始列表。</span><span class="sxs-lookup"><span data-stu-id="c42fb-126">The following example shows the XML request to get the initial list of items in the Inbox by using the [SyncFolderItems operation](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx).</span></span> <span data-ttu-id="c42fb-127">这也是 XML 请求 EWS 托管 API 发送时[检索使用 SyncFolderItems 方法的项目的列表](#bk_cesyncongoingewsma)。</span><span class="sxs-lookup"><span data-stu-id="c42fb-127">This is also the XML request that the EWS Managed API sends when [retrieving the list of items by using the SyncFolderItems method](#bk_cesyncongoingewsma).</span></span> <span data-ttu-id="c42fb-128">**SyncFolderItems**操作的[SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素不包含，因为这是初始同步。</span><span class="sxs-lookup"><span data-stu-id="c42fb-128">The [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the **SyncFolderItems** operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="c42fb-129">本示例将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly**以减少与 Exchange 数据库，这是一种[同步的最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c42fb-129">This example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderItems>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:ItemShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:SyncFolderId>
      <m:MaxChangesReturned>10</m:MaxChangesReturned>
      <m:SyncScope>NormalItems</m:SyncScope>
    </m:SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c42fb-130">下面的示例演示后处理来自客户端的**SyncFolderItems**操作请求服务器返回的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="c42fb-130">The following example shows the XML response that is returned by the server after it processes the **SyncFolderItems** operation request from the client.</span></span> <span data-ttu-id="c42fb-131">初始响应包括[创建](http://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx)元素的五个项目，因为所有项目被都视为新期间初始同步。</span><span class="sxs-lookup"><span data-stu-id="c42fb-131">The initial response includes [Create](http://msdn.microsoft.com/library/cb5e64a2-66a5-4447-921e-7c13efb8f6bf%28Office.15%29.aspx) elements for five items because all items are considered new during an initial synchronization.</span></span> <span data-ttu-id="c42fb-132">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="c42fb-132">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q04QAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdC"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q07AAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdB"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="q1AwAAAA=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVdA"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AAMkADBh=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVc5"/>
              </t:Message>
            </t:Create>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AAMkADBh=="
                          ChangeKey="CQAAABYAAABhFfgM7MNwSYx0VZ0GoBMJAAAATVc4"/>
              </t:Message>
            </t:Create>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderItemsResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="c42fb-133">后检索在服务器上，[创建客户端上的项目](#bk_nextsteps)的新项目的列表。</span><span class="sxs-lookup"><span data-stu-id="c42fb-133">After you retrieve the list of new items on the server, [create the items on the client](#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="c42fb-134">使用 EWS 获取上次同步后所做的更改</span><span class="sxs-lookup"><span data-stu-id="c42fb-134">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="c42fb-135"><a name="bk_ewsexamplec"> </a></span><span class="sxs-lookup"><span data-stu-id="c42fb-135"></span></span>

<span data-ttu-id="c42fb-136">下面的示例演示 XML 请求收件箱中获取项目的更改的列表，使用[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="c42fb-136">The following example shows the XML request to get the list of changes to items in the Inbox by using the [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="c42fb-137">这也是 XML 请求 EWS 托管 API 发送时[检索到收件箱的更改的列表](#bk_cesyncongoingewsma)。</span><span class="sxs-lookup"><span data-stu-id="c42fb-137">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the Inbox](#bk_cesyncongoingewsma).</span></span> <span data-ttu-id="c42fb-138">本示例将[SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素的值设置为在[以前的响应](http://msdn.microsoft.com/library/886e7d35-9096-480b-8a8c-a7db27da06c2bk_ewsexamplea%28Office.15%29.aspx)中返回的值。</span><span class="sxs-lookup"><span data-stu-id="c42fb-138">This example sets the [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the [previous response](http://msdn.microsoft.com/library/886e7d35-9096-480b-8a8c-a7db27da06c2bk_ewsexamplea%28Office.15%29.aspx).</span></span> <span data-ttu-id="c42fb-139">并用于演示，本示例将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**AllProperties**而不是**IdOnly**显示返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="c42fb-139">And for demonstration purposes, this example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="c42fb-140">[同步的最佳做法](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)是将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly** 。</span><span class="sxs-lookup"><span data-stu-id="c42fb-140">Setting the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="c42fb-141">为便于阅读缩短了**SyncState**的值。</span><span class="sxs-lookup"><span data-stu-id="c42fb-141">The value of **SyncState** has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
      <t:RequestServerVersion Version="Exchange2010_SP2" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderItems>
      <m:ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:ItemShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAAA==</m:SyncState>
      <m:MaxChangesReturned>10</m:MaxChangesReturned>
      <m:SyncScope>NormalItems</m:SyncScope>
    </m:SyncFolderItems>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="c42fb-142">下面的示例演示后处理来自客户端的**SyncFolderItems**操作请求服务器返回的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="c42fb-142">The following example shows the XML response that is returned by the server after it processes the **SyncFolderItems** operation request from the client.</span></span> <span data-ttu-id="c42fb-143">此响应指示一项已更新，创建两个项目，一个项目的读取的标记已更改，并且以前同步后已删除一个项目。</span><span class="sxs-lookup"><span data-stu-id="c42fb-143">This response indicates that one item was updated, two items were created, the read flag of one item was changed, and one item was deleted since the prior synchronization.</span></span> <span data-ttu-id="c42fb-144">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="c42fb-144">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="731" MinorBuildNumber="10" Version="V2_3"
                 xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAAAAAAEAO29B2AcSZY==</m:SyncState>
          <m:IncludesLastItemInRange>true</m:IncludesLastItemInRange>
          <m:Changes>
            <t:Update>
                <t:Message>
                  <t:ItemId Id="q04QAAAA==" ChangeKey="CQAAABYAAADZGACZQpSgSpyNkexYe2b7AAAAird/" />
                  <t:ParentFolderId Id=" AgENAAAA" ChangeKey="AQAAAA==" />
                  <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Company Soccer Team</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T15:22:10Z</t:DateTimeReceived>
                  <t:Size>23110</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;8e084ea1a5b64f97b95fa8a863a5869d@CH1SR01MB001.namsdf01.sdf.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T15:22:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:38Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>All Employees</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara  Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T16:53:35Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQACAi+NTh0F5Eg5YDwpJsXPE=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Alfred  Welker </t:Name>
                      <t:EmailAddress>Alfred.Welker@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5V/ZICL41OHQXkSDlgPCkmxc8ZYxA3I4gAAP5UeAANHpbIAAEE+0gAABYhSAACGYTIAAA2+vgAAE81qAkhv0Eg==</t:ConversationIndex>
                  <t:ConversationTopic>Company Soccer Team</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Alfred  Welker </t:Name>
                      <t:EmailAddress>Alfred.Welker@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;e5919a09c8fc4d64b6ffd3542e194fc3@BY2SR01MB609.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>namsdf01.sdf.contoso.com&amp;gt;</t:References>
                </t:Message>
            </t:Update>
            <t:Create>
              <t:Message>
                <t:ItemId Id="AQMkAD+" />
                <t:ParentFolderId Id="AQMkA==" ChangeKey="AQAAAA==" />
                <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Review Proposal for Contoso</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T16:20:10Z</t:DateTimeReceived>
                  <t:Size>32515</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;e52a4de6b98d484887e141da094a2ce6@SN2SR01MB006.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T16:20:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:33Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>Legal Team; Executives</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara  Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T04:07:35Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQAIsBEZp25UpElByLLUQFH6Q=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Hope Gross</t:Name>
                      <t:EmailAddress>Hope.Gross@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5WBRiwERmnblSkSUHIstRAUfpJYw9fbSgAAAdm2AAAB6koAAAHTDgAADl6+AAAbxCYAABm5PgAACSA+AANx034AAEKGQgAAAfsiAAB7m3IAABG+ngAABPZyAAASUzoAAA2DNgAAAfKE=</t:ConversationIndex>
                  <t:ConversationTopic>Review Proposal for Contoso</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Hope Gross</t:Name>
                      <t:EmailAddress>Hope.Gross@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;bcdb185495834370a874a1e7ebedbb96@SN2SR01MB005.namsdf01.sdf.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>&amp;lt;2d4d7d…</t:References>
                </t:Message>
              </t:Create>
              <t:Create>
                <t:Message>
                  <t:ItemId Id="Q04AAAAA==" ChangeKey="AAAirbnd" />
                  <t:ParentFolderId Id="AgENAAAA" ChangeKey="AQAAAA==" />
                  <t:ItemClass>IPM.Note</t:ItemClass>
                  <t:Subject>RE: Review Proposal for Contoso</t:Subject>
                  <t:Sensitivity>Normal</t:Sensitivity>
                  <t:DateTimeReceived>2013-08-29T15:30:10Z</t:DateTimeReceived>
                  <t:Size>29518</t:Size>
                  <t:Importance>Normal</t:Importance>
                  <t:InReplyTo>&amp;lt;f0db3ead01db4fe087d98022149aa16f@SN2SR01MB001.namsdf01.sdf.contoso.com&amp;gt;</t:InReplyTo>
                  <t:IsSubmitted>false</t:IsSubmitted>
                  <t:IsDraft>false</t:IsDraft>
                  <t:IsFromMe>false</t:IsFromMe>
                  <t:IsResend>false</t:IsResend>
                  <t:IsUnmodified>false</t:IsUnmodified>
                  <t:DateTimeSent>2013-08-29T15:30:10Z</t:DateTimeSent>
                  <t:DateTimeCreated>2013-08-28T04:07:36Z</t:DateTimeCreated>
                  <t:DisplayCc />
                  <t:DisplayTo>Legal Team; Executives</t:DisplayTo>
                  <t:HasAttachments>false</t:HasAttachments>
                  <t:Culture>en-US</t:Culture>
                  <t:EffectiveRights>
                    <t:CreateAssociated>false</t:CreateAssociated>
                    <t:CreateContents>false</t:CreateContents>
                    <t:CreateHierarchy>false</t:CreateHierarchy>
                    <t:Delete>true</t:Delete>
                    <t:Modify>true</t:Modify>
                    <t:Read>true</t:Read>
                    <t:ViewPrivateItems>true</t:ViewPrivateItems>
                  </t:EffectiveRights>
                  <t:LastModifiedName>Mara Whitley</t:LastModifiedName>
                  <t:LastModifiedTime>2013-08-28T04:07:38Z</t:LastModifiedTime>
                  <t:IsAssociated>false</t:IsAssociated>
                  <t:WebClientReadFormQueryString>?ae=Item&amp;amp;a=Open&amp;amp;t=IPM.Note&amp;amp;id=&amp;amp;exvsurl=1</t:WebClientReadFormQueryString>
                  <t:ConversationId Id="AAQkADkzNjJjODUzLWZhMDMtNDVkMS05ZDdjLWVmMDlkYjQ1Zjc4MwAQAIsBEZp25UpElByLLUQFH6Q=" />
                  <t:Sender>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:Sender>
                  <t:IsReadReceiptRequested>false</t:IsReadReceiptRequested>
                  <t:ConversationIndex>AQHM5WBRiwERmnblSkSUHIstRAUfpJYw9fbSgAAAdm2AAAB6koAAAHTDgAADl6+AAAbxCYAABm5PgAACSA+AANx034AAEKGQgAAAfsiAAB7m3IAABG+ngAABPZyAAASUzoAAA2DN</t:ConversationIndex>
                  <t:ConversationTopic>Review Proposal for Contoso</t:ConversationTopic>
                  <t:From>
                    <t:Mailbox>
                      <t:Name>Mack Chaves</t:Name>
                      <t:EmailAddress>Mack.Chaves@contoso.com</t:EmailAddress>
                      <t:RoutingType>SMTP</t:RoutingType>
                      <t:MailboxType>Mailbox</t:MailboxType>
                    </t:Mailbox>
                  </t:From>
                  <t:InternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6@SN2SR01MB006.namsdf01.sdf.contoso.com&amp;gt;</t:InternetMessageId>
                  <t:IsRead>true</t:IsRead>
                  <t:References>namsdf01.sdf.contoso.com&amp;gt;</t:References>
                </t:Message>
              </t:Create>
              <t:ReadFlagChange>
                <t:ItemId Id=" q07AAAAA==" ChangeKey="CQAAAA==" />
                <t:IsRead>true</t:IsRead>
              </t:ReadFlagChange>
              <t:Delete>
                <t:ItemId Id=" q1AwAAAA==" ChangeKey="CQAAAA==" />
              </t:Delete>
          </m:Changes>
        </m:SyncFolderItemsResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderItemsResponse>
  </s:Body>
</s:Envelope>
```

它不能返回元素，例如[正文](http://msdn.microsoft.com/library/7851ea9b-9f87-4adc-a26f-7a27df4a9bca%28Office.15%29.aspx)或[附件](http://msdn.microsoft.com/library/b470e614-34bb-44f0-8790-7ddbdcbbd29d%28Office.15%29.aspx)元素，因此**SyncFolderItems**操作是类似于[FindItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法。 <span data-ttu-id="c42fb-146">如果您需要无法由**SyncFolderItems**操作返回的属性， [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素的值时设置为 IdOnly 呼叫**SyncFolderItems**，然后使用[GetItem 操作](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)获取属性您需要**SyncFolderItems**操作返回的项目。</span><span class="sxs-lookup"><span data-stu-id="c42fb-146">If you need properties that cannot be returned by the **SyncFolderItems** operation, set the value of the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to IdOnly when you call **SyncFolderItems**, and then use the [GetItem operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) to get the properties you require for the items that were returned by the **SyncFolderItems** operation.</span></span> 
  
<span data-ttu-id="c42fb-147">后检索在服务器上，[更新客户端上的项目](#bk_nextsteps)更改的项目的列表。</span><span class="sxs-lookup"><span data-stu-id="c42fb-147">After you retrieve the list of changed items on the server, [update the items on the client](#bk_nextsteps).</span></span>
  
## <a name="update-the-client"></a><span data-ttu-id="c42fb-148">更新客户端</span><span class="sxs-lookup"><span data-stu-id="c42fb-148">Update the client</span></span>
<span data-ttu-id="c42fb-149"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="c42fb-149"></span></span>

<span data-ttu-id="c42fb-150">如果您使用 EWS 托管 API 获取新的或更改项目的列表后，，使用[LoadPropertiesForItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)方法以获取对新的或更改项目的属性、 比较属性设置为本地值，并更新客户端上的项目。</span><span class="sxs-lookup"><span data-stu-id="c42fb-150">If you're using the EWS Managed API, after you get the list of new or changed items, use the [LoadPropertiesForItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update the items on the client.</span></span> 
  
<span data-ttu-id="c42fb-151">如果您正在使用 EWS，使用[GetItem 操作](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx)获取新的或更改项目的属性和更新客户端上的项目。</span><span class="sxs-lookup"><span data-stu-id="c42fb-151">If you're using EWS, use the [GetItem operation](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) to get properties on the new or changed items and update the items on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c42fb-152">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c42fb-152">See also</span></span>


- [<span data-ttu-id="c42fb-153">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="c42fb-153">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    
- [<span data-ttu-id="c42fb-154">使用 EWS 在 Exchange 同步文件夹</span><span class="sxs-lookup"><span data-stu-id="c42fb-154">Synchronize folders by using EWS in Exchange</span></span>](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="c42fb-155">在 Exchange 处理同步相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="c42fb-155">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="c42fb-156">Notification subscriptions, mailbox events, and EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="c42fb-156">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    

