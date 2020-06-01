---
title: 使用 Exchange 中的 EWS 同步文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: 了解如何使用 EWS 托管 API 或 EWS 获取文件夹列表或已更改的文件夹列表，以便同步客户端。
ms.openlocfilehash: e49fdaf2faf97c2369f2ad7dbb141c5ac3100884
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455861"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a><span data-ttu-id="3c4ad-103">使用 Exchange 中的 EWS 同步文件夹</span><span class="sxs-lookup"><span data-stu-id="3c4ad-103">Synchronize folders by using EWS in Exchange</span></span>

<span data-ttu-id="3c4ad-104">了解如何使用 EWS 托管 API 或 EWS 获取文件夹列表或已更改的文件夹列表，以便同步客户端。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-104">Find out how to use the EWS Managed API or EWS to get a list of folders, or a list of folders that have changed, in order to synchronize your client.</span></span>
  
<span data-ttu-id="3c4ad-105">Exchange 中的 EWS 使用项目同步和文件夹同步来同步客户端和服务器之间的邮箱内容。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="3c4ad-106">文件夹同步从根文件夹获取文件夹的初始列表，然后随着时间的推移，获取对这些文件夹所做的更改，并获取新文件夹。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-106">Folder synchronization gets the initial list of folders from a root folder and then, over time, gets changes that were made to those folders and gets new folders as well.</span></span>
  
<span data-ttu-id="3c4ad-107">如果要使用 EWS 托管 API 执行文件夹同步，首先使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法[获取根文件夹中的文件夹的初始列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-107">If you're performing folder synchronization by using the EWS Managed API, you first [get the initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) by using the [ExchangeService.SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="3c4ad-108">然后，在随后的调用过程中更新_cSyncState_参数的值，以获取新文件夹和已更改文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-108">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of new and changed folders.</span></span> 
  
<span data-ttu-id="3c4ad-109">若要使用 EWS 执行文件夹同步，请使用[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作请求[根文件夹中的文件夹的初始列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest)，分析响应，然后在将来某一时间[获取对根文件夹的更改](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)，并分析响应。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-109">To perform folder synchronization by using EWS, you request the [initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) by using the [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation, parse the response, and then at some point in the future [get the changes to the folders in the root](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews), and parse the response.</span></span> <span data-ttu-id="3c4ad-110">客户端收到初始或更改的文件夹列表后，会在[本地进行更新](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-110">After the client receives the list of initial or changed folders, it [makes updates locally](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="3c4ad-111">在将来检索更改的方式和时间取决于应用程序使用的[同步设计模式](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns)。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-111">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a><span data-ttu-id="3c4ad-112">使用 EWS 托管 API 获取所有文件夹或已更改的文件夹的列表</span><span class="sxs-lookup"><span data-stu-id="3c4ad-112">Get the list of all folders or changed folders by using the EWS Managed API</span></span>
<span data-ttu-id="3c4ad-113"><a name="bk_cesyncinitialewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="3c4ad-113"><a name="bk_cesyncinitialewsma"> </a></span></span>

<span data-ttu-id="3c4ad-114">下面的代码示例演示如何获取根文件夹中的文件夹的初始列表，然后获取对根文件夹中的文件夹所做更改的列表，这些文件夹在上一次同步之后发生。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-114">The following code example shows how to get an initial list of folders in a root folder and then get a list of changes to folders in the root folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="3c4ad-115">在首次调用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法过程中，将_cSyncState_值设置为 null。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-115">During the initial call to the [ExchangeService.SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="3c4ad-116">方法完成后，将_cSyncState_值保存在本地，以在下一个**SyncFolderHierarchy**方法调用中使用。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-116">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderHierarchy** method call.</span></span> <span data-ttu-id="3c4ad-117">在初始调用和后续调用中，将使用对**SyncFolderHierarchy**方法的连续调用在批处理中检索文件夹，直到不再保留所做的更改。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-117">In both the initial call and the subsequent calls, the folders are retrieved in batches of ten, by using successive calls to the **SyncFolderHierarchy** method, until no more changes remain.</span></span> <span data-ttu-id="3c4ad-118">本示例将_propertySet_参数设置为 IdOnly，以减少对 Exchange 数据库的调用，这是一种[同步最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-118">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="3c4ad-119">在此示例中，我们假定**service**是有效的**ExchangeService**对象绑定，并且_cSyncState_表示以前对**SyncFolderHierarchy**返回的同步状态。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-119">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderHierarchy**.</span></span> 
  
```cs
// Get a list of all folders in the mailbox by calling SyncFolderHierarchy.
// The folderId parameter must be set to the root folder to synchronize. 
// The propertySet parameter is set to IdOnly to reduce calls to the Exchange database
// because any additional properties result in additional calls to the Exchange database. 
// The syncState parameter is set to cSyncState, which should be null in the initial call, 
// and should be set to the sync state returned by the previous SyncFolderHierarchy call 
// in subsequent calls.
ChangeCollection<FolderChange> fcc = service.SyncFolderHierarchy(new FolderId(WellKnownFolderName.Root), PropertySet.IdOnly, cSyncState);
// If the count of changes is zero, there are no changes to synchronize.
if (fcc.Count == 0)
{
    Console.WriteLine("There are no folders to synchronize.");
}
// Otherwise, write all the changes included in the response 
// to the console. 
// For the initial synchronization, all the changes will be of type
// ChangeType.Create.
else
{
    foreach (FolderChange fc in fcc)
    {
        Console.WriteLine("ChangeType: " + fc.ChangeType.ToString());
        Console.WriteLine("FolderId: " + fc.FolderId);
        Console.WriteLine("===========");
    }
}
// Save the sync state for use in future SyncFolderItems requests.
// The sync state is used by the server to determine what changes to report
// to the client.
string fSyncState = fcc.SyncState;

```

<span data-ttu-id="3c4ad-120">在服务器上检索新的或已更改的文件夹列表后，[创建或更新客户端上的文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-120">After you retrieve the list of new or changed folders on the server, [create or update the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a><span data-ttu-id="3c4ad-121">使用 EWS 获取文件夹的初始列表</span><span class="sxs-lookup"><span data-stu-id="3c4ad-121">Get the initial list of folders by using EWS</span></span>
<span data-ttu-id="3c4ad-122"><a name="bk_cesyncewsrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="3c4ad-122"><a name="bk_cesyncewsrequest"> </a></span></span>

<span data-ttu-id="3c4ad-123">下面的示例演示使用[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作获取初始文件夹层次结构的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-123">The following example shows an XML request to get the initial folder hierarchy by using the [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="3c4ad-124">这也是在[使用 SyncFolderHierarchy 方法检索初始文件夹列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-124">This is also the XML request that the EWS Managed API sends when [retrieving the list of initial folders by using the SyncFolderHierarchy method](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="3c4ad-125">[SyncFolderHierarchy](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)操作的[SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素不包含在内，因为这是初始同步。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-125">The [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the [SyncFolderHierarchy](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="3c4ad-126">本示例将[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly** ，以减少对 Exchange 数据库的调用，这是一种[同步最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-126">This example sets the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3c4ad-127">下面的示例演示服务器在处理[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作请求后返回的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-127">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation request.</span></span> <span data-ttu-id="3c4ad-128">初始响应包括为所有文件夹[创建](https://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx)元素，因为在初始同步过程中，所有文件夹都被视为新的。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-128">The initial response includes [Create](https://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) elements for all folders because all folders are considered new during an initial synchronization.</span></span> <span data-ttu-id="3c4ad-129">为了提高可读性，某些属性和元素的值已缩短，并且为了简洁起见，删除了一些**Create** element 块。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-129">The values of some attributes and elements have been shortened for readability, and some **Create** element blocks were removed for brevity.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADM="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM="
                            ChangeKey="AQAAABY"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkAD/AAA="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADBh="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            ...
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="3c4ad-130">在服务器上检索新文件夹的列表后，在[客户端上创建文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-130">After you retrieve the list of new folders on the server, [create the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="3c4ad-131">通过使用 EWS 获取上次同步以来的更改</span><span class="sxs-lookup"><span data-stu-id="3c4ad-131">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="3c4ad-132"><a name="bk_cesyncrespews"> </a></span><span class="sxs-lookup"><span data-stu-id="3c4ad-132"><a name="bk_cesyncrespews"> </a></span></span>

<span data-ttu-id="3c4ad-133">下面的示例展示了在使用[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作获取根文件夹中的文件夹更改列表的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-133">The following example shows the XML request to get the list of changes to folders in the root folder by using the [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="3c4ad-134">这也是在[检索根文件夹的更改列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-134">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="3c4ad-135">本示例将[SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素的值设置为上一次响应中返回的值。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-135">This example sets the [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the previous response.</span></span> <span data-ttu-id="3c4ad-136">出于演示目的，本示例将[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**AllProperties** ，而不是**IdOnly**以显示返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-136">And for demonstration purposes, this example sets the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="3c4ad-137">将[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly**是一种[同步最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-137">Setting the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="3c4ad-138">为了提高可读性， **SyncState**的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-138">The value of **SyncState** has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                    xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                    xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAA==</m:SyncState>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3c4ad-139">下面的示例显示了由服务器在处理来自客户端的[SyncFolderHierarchy 操作](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)请求后返回的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-139">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy operation](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) request from the client.</span></span> <span data-ttu-id="3c4ad-140">此响应表示更新了一个文件夹，创建了一个文件夹，并在上一次同步后删除了一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-140">This response indicates that one folder was updated, one folder was created, and one folder was deleted since the prior synchronization.</span></span> <span data-ttu-id="3c4ad-141">为了提高可读性， [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素、 **Id**属性和**ChangeKey**属性的值已缩短。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-141">The value of the [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element, **Id** attributes, and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
<span data-ttu-id="3c4ad-142">请记住，请求包含在**AllProperties**[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)中。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-142">Remember that the request included the **AllProperties**[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx).</span></span> <span data-ttu-id="3c4ad-143">这仅用于演示目的。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-143">This is just for demonstration purposes.</span></span> <span data-ttu-id="3c4ad-144">建议您将**BaseShape**元素设置为生产中的**IdOnly** 。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-144">We recommend that you set the **BaseShape** element to **IdOnly** in production.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Update>
              <t:Folder>
                <t:FolderId Id="AAMkADM=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQMkADMzADI1==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Meeting Notes</t:DisplayName>
                <t:TotalCount>3</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Update>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM=" ChangeKey="AQAAABYAA" />
                <t:ParentFolderId Id="AQMkO67A==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Schedules</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
            <t:Delete>
              <t:FolderId Id="AAMkAD/AAA=" ChangeKey="AQAAAA==" />
            </t:Delete>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>

```

## <a name="update-the-client"></a><span data-ttu-id="3c4ad-145">更新客户端</span><span class="sxs-lookup"><span data-stu-id="3c4ad-145">Update the client</span></span>
<span data-ttu-id="3c4ad-146"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="3c4ad-146"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="3c4ad-147">如果使用 EWS 托管 API，在获取新的或已更改的文件夹列表后，请使用[Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx)方法获取新项或已更改项的属性，将属性与本地值进行比较，并在客户端上更新或创建文件夹。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-147">If you're using the EWS Managed API, after you get the list of new or changed folders, use the [Folder.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update or create the folders on the client.</span></span> 
  
<span data-ttu-id="3c4ad-148">如果使用的是 EWS，请使用[GetFolder 操作](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)获取新的或已更改的文件夹的属性，并更新或创建客户端上的文件夹。</span><span class="sxs-lookup"><span data-stu-id="3c4ad-148">If you're using EWS, use the [GetFolder operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get properties on the new or changed folders and update or create the folders on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c4ad-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3c4ad-149">See also</span></span>

- [<span data-ttu-id="3c4ad-150">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="3c4ad-150">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)   
- [<span data-ttu-id="3c4ad-151">使用 Exchange 中的 EWS 同步项目</span><span class="sxs-lookup"><span data-stu-id="3c4ad-151">Synchronize items by using EWS in Exchange</span></span>](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="3c4ad-152">在 Exchange 中处理 EWS 中与同步相关的错误</span><span class="sxs-lookup"><span data-stu-id="3c4ad-152">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

