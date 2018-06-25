---
title: 使用 EWS 在 Exchange 同步文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: 了解如何使用 EWS 托管 API 或 EWS 获取文件夹的列表或已更改，以便同步您的客户端的文件夹的列表。
ms.openlocfilehash: 4b0686134d642da34b2890a0e692e3d03e4a9fb1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752892"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a><span data-ttu-id="6e37a-103">使用 EWS 在 Exchange 同步文件夹</span><span class="sxs-lookup"><span data-stu-id="6e37a-103">Synchronize folders by using EWS in Exchange</span></span>

<span data-ttu-id="6e37a-104">了解如何使用 EWS 托管 API 或 EWS 获取文件夹的列表或已更改，以便同步您的客户端的文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="6e37a-104">Find out how to use the EWS Managed API or EWS to get a list of folders, or a list of folders that have changed, in order to synchronize your client.</span></span>
  
<span data-ttu-id="6e37a-105">Exchange 中的 EWS 使用项目同步和文件夹同步到客户端和服务器之间同步邮箱内容。</span><span class="sxs-lookup"><span data-stu-id="6e37a-105">EWS in Exchange uses item synchronization and folder synchronization to sync mailbox content between the client and server.</span></span> <span data-ttu-id="6e37a-106">文件夹同步从根文件夹中获取的文件夹的初始列表，然后随时间推移，获取对这些文件夹所做的更改以及获取新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="6e37a-106">Folder synchronization gets the initial list of folders from a root folder and then, over time, gets changes that were made to those folders and gets new folders as well.</span></span>
  
<span data-ttu-id="6e37a-107">如果您正在使用 EWS 托管 API，您第一个[获取文件夹的根文件夹中的初始列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)使用[ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法执行文件夹同步。</span><span class="sxs-lookup"><span data-stu-id="6e37a-107">If you're performing folder synchronization by using the EWS Managed API, you first [get the initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) by using the [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="6e37a-108">然后您要获取的新的和更改的文件夹的列表的后续呼叫过程中更新_cSyncState_参数的值。</span><span class="sxs-lookup"><span data-stu-id="6e37a-108">You then update the value of the  _cSyncState_ parameter during subsequent calls to get the list of new and changed folders.</span></span> 
  
<span data-ttu-id="6e37a-109">若要使用 EWS 执行文件夹同步，您请求[的根文件夹中的文件夹的初始列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest)使用[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作、 分析响应，然后某些点将来[到的文件夹中获取所做的更改根](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)，并分析响应。</span><span class="sxs-lookup"><span data-stu-id="6e37a-109">To perform folder synchronization by using EWS, you request the [initial list of folders in the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest) by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation, parse the response, and then at some point in the future [get the changes to the folders in the root](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews), and parse the response.</span></span> <span data-ttu-id="6e37a-110">客户端接收的初始或已更改文件夹的列表后，它[使本地更新](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)。</span><span class="sxs-lookup"><span data-stu-id="6e37a-110">After the client receives the list of initial or changed folders, it [makes updates locally](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="6e37a-111">如何以及何时将来检索更改取决于您的应用程序正在使用[同步设计模式](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns)。</span><span class="sxs-lookup"><span data-stu-id="6e37a-111">How and when you retrieve changes in the future depends on the [synchronization design pattern](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) your application is using.</span></span> 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a><span data-ttu-id="6e37a-112">使用 EWS 托管 API 获取所有文件夹或已更改的文件夹的列表</span><span class="sxs-lookup"><span data-stu-id="6e37a-112">Get the list of all folders or changed folders by using the EWS Managed API</span></span>
<span data-ttu-id="6e37a-113"><a name="bk_cesyncinitialewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="6e37a-113"></span></span>

<span data-ttu-id="6e37a-114">下面的代码示例演示如何获取根文件夹中的文件夹的初始列表，然后获取文件夹的根文件夹中的自上次同步后发生更改的列表。</span><span class="sxs-lookup"><span data-stu-id="6e37a-114">The following code example shows how to get an initial list of folders in a root folder and then get a list of changes to folders in the root folder that have occurred since the previous synchronization.</span></span> <span data-ttu-id="6e37a-115">初始呼叫期间[ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法，将_cSyncState_值设置为 null。</span><span class="sxs-lookup"><span data-stu-id="6e37a-115">During the initial call to the [ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) method, set the  _cSyncState_ value to null.</span></span> <span data-ttu-id="6e37a-116">该方法完成后，保存_cSyncState_值本地以在下一个**SyncFolderHierarchy**方法调用中使用。</span><span class="sxs-lookup"><span data-stu-id="6e37a-116">When the method completes, save the  _cSyncState_ value locally to use in the next **SyncFolderHierarchy** method call.</span></span> <span data-ttu-id="6e37a-117">在初始调用和后续呼叫，文件夹将检索批次的 10，直到没有更多更改保持使用连续**SyncFolderHierarchy**方法调用中。</span><span class="sxs-lookup"><span data-stu-id="6e37a-117">In both the initial call and the subsequent calls, the folders are retrieved in batches of ten, by using successive calls to the **SyncFolderHierarchy** method, until no more changes remain.</span></span> <span data-ttu-id="6e37a-118">本示例将_属性集_参数设置为 IdOnly 以减少与 Exchange 数据库，这是一种[同步的最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="6e37a-118">This example sets the  _propertySet_ parameter to IdOnly to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="6e37a-119">本示例中，我们假定**服务**是一个有效的**ExchangeService**对象绑定并该_cSyncState_代表已由以前**SyncFolderHierarchy**调用返回的同步状态。</span><span class="sxs-lookup"><span data-stu-id="6e37a-119">In this example, we assume that **service** is a valid **ExchangeService** object binding and that  _cSyncState_ represents the sync state that was returned by a prior call to **SyncFolderHierarchy**.</span></span> 
  
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

<span data-ttu-id="6e37a-120">后检索的在服务器上，[创建或更新客户端上的文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)的新的或更改文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="6e37a-120">After you retrieve the list of new or changed folders on the server, [create or update the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a><span data-ttu-id="6e37a-121">使用 EWS 获取文件夹的初始的列表</span><span class="sxs-lookup"><span data-stu-id="6e37a-121">Get the initial list of folders by using EWS</span></span>
<span data-ttu-id="6e37a-122"><a name="bk_cesyncewsrequest"> </a></span><span class="sxs-lookup"><span data-stu-id="6e37a-122"></span></span>

<span data-ttu-id="6e37a-123">下面的示例演示 XML 请求，若要使用[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作获取初始文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="6e37a-123">The following example shows an XML request to get the initial folder hierarchy by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="6e37a-124">这也是 XML 请求 EWS 托管 API 发送时[检索的使用 SyncFolderHierarchy 方法的初始文件夹的列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)。</span><span class="sxs-lookup"><span data-stu-id="6e37a-124">This is also the XML request that the EWS Managed API sends when [retrieving the list of initial folders by using the SyncFolderHierarchy method](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="6e37a-125">[SyncFolderHierarchy](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)操作的[SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素不包含，因为这是初始同步。</span><span class="sxs-lookup"><span data-stu-id="6e37a-125">The [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element of the [SyncFolderHierarchy](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operation is not included because this is the initial synchronization.</span></span> <span data-ttu-id="6e37a-126">本示例将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly**以减少与 Exchange 数据库，这是一种[同步的最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="6e37a-126">This example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** to reduce calls to the Exchange database, which is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span>
  
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

<span data-ttu-id="6e37a-127">下面的示例演示它处理[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作请求之后，服务器返回的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="6e37a-127">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation request.</span></span> <span data-ttu-id="6e37a-128">初始响应包括[创建](http://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx)元素的所有文件夹，因为所有文件夹被都视为新期间初始同步。</span><span class="sxs-lookup"><span data-stu-id="6e37a-128">The initial response includes [Create](http://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) elements for all folders because all folders are considered new during an initial synchronization.</span></span> <span data-ttu-id="6e37a-129">为了提高可读性，变短了某些属性和元素的值和部分**创建**元素块已删除了明了。</span><span class="sxs-lookup"><span data-stu-id="6e37a-129">The values of some attributes and elements have been shortened for readability, and some **Create** element blocks were removed for brevity.</span></span> 
  
```xml
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
    <m:SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="6e37a-130">后检索的在服务器上，[创建客户端上的文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)的新文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="6e37a-130">After you retrieve the list of new folders on the server, [create the folders on the client](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a><span data-ttu-id="6e37a-131">使用 EWS 获取上次同步后所做的更改</span><span class="sxs-lookup"><span data-stu-id="6e37a-131">Get the changes since the last sync by using EWS</span></span>
<span data-ttu-id="6e37a-132"><a name="bk_cesyncrespews"> </a></span><span class="sxs-lookup"><span data-stu-id="6e37a-132"></span></span>

<span data-ttu-id="6e37a-133">下面的示例演示 XML 请求以获取根文件夹中的文件夹的更改的列表，使用[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="6e37a-133">The following example shows the XML request to get the list of changes to folders in the root folder by using the [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="6e37a-134">这也是 XML 请求 EWS 托管 API 发送时[检索到的根文件夹的更改的列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)。</span><span class="sxs-lookup"><span data-stu-id="6e37a-134">This is also the XML request that the EWS Managed API sends when [retrieving the list of changes to the root folder](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma).</span></span> <span data-ttu-id="6e37a-135">本示例将[SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素的值设置为以前的响应中返回的值。</span><span class="sxs-lookup"><span data-stu-id="6e37a-135">This example sets the [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element value to the value returned in the previous response.</span></span> <span data-ttu-id="6e37a-136">并用于演示，本示例将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**AllProperties**而不是**IdOnly**显示返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="6e37a-136">And for demonstration purposes, this example sets the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **AllProperties** instead of **IdOnly** to show the additional properties returned.</span></span> <span data-ttu-id="6e37a-137">[同步的最佳做法](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)是将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly** 。</span><span class="sxs-lookup"><span data-stu-id="6e37a-137">Setting the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element to **IdOnly** is a [synchronization best practice](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices).</span></span> <span data-ttu-id="6e37a-138">为便于阅读缩短了**SyncState**的值。</span><span class="sxs-lookup"><span data-stu-id="6e37a-138">The value of **SyncState** has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="6e37a-139">下面的示例演示后处理来自客户端的[SyncFolderHierarchy 操作](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)请求服务器返回的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="6e37a-139">The following example shows the XML response that is returned by the server after it processes the [SyncFolderHierarchy operation](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) request from the client.</span></span> <span data-ttu-id="6e37a-140">此响应指示已更新一个文件夹，创建一个文件夹，并且以前同步后已删除一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="6e37a-140">This response indicates that one folder was updated, one folder was created, and one folder was deleted since the prior synchronization.</span></span> <span data-ttu-id="6e37a-141">为便于阅读变短了[SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素、 **Id**属性和**更改密钥**属性的值。</span><span class="sxs-lookup"><span data-stu-id="6e37a-141">The value of the [SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) element, **Id** attributes, and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
<span data-ttu-id="6e37a-142">请记住请求包含**AllProperties**[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6e37a-142">Remember that the request included the **AllProperties**[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx).</span></span> <span data-ttu-id="6e37a-143">这是只是为了演示。</span><span class="sxs-lookup"><span data-stu-id="6e37a-143">This is just for demonstration purposes.</span></span> <span data-ttu-id="6e37a-144">建议在生产中将**BaseShape**元素设置为**IdOnly** 。</span><span class="sxs-lookup"><span data-stu-id="6e37a-144">We recommend that you set the **BaseShape** element to **IdOnly** in production.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="update-the-client"></a><span data-ttu-id="6e37a-145">更新客户端</span><span class="sxs-lookup"><span data-stu-id="6e37a-145">Update the client</span></span>
<span data-ttu-id="6e37a-146"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="6e37a-146"></span></span>

<span data-ttu-id="6e37a-147">如果您使用 EWS 托管 API 获取新的或更改的文件夹的列表、 [Folder.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx)方法用于获取对新的或更改项目的属性、 比较属性设置为本地值，并更新或客户端上创建文件夹之后。</span><span class="sxs-lookup"><span data-stu-id="6e37a-147">If you're using the EWS Managed API, after you get the list of new or changed folders, use the [Folder.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) method to get properties on the new or changed items, compare the properties to the local values, and update or create the folders on the client.</span></span> 
  
<span data-ttu-id="6e37a-148">如果您正在使用 EWS，使用[GetFolder 操作](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)获取新的或更改的文件夹的属性和更新或客户端上创建文件夹。</span><span class="sxs-lookup"><span data-stu-id="6e37a-148">If you're using EWS, use the [GetFolder operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get properties on the new or changed folders and update or create the folders on the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e37a-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6e37a-149">See also</span></span>

- [<span data-ttu-id="6e37a-150">邮箱同步和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="6e37a-150">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)   
- [<span data-ttu-id="6e37a-151">使用 EWS 在 Exchange 同步的项目</span><span class="sxs-lookup"><span data-stu-id="6e37a-151">Synchronize items by using EWS in Exchange</span></span>](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="6e37a-152">在 Exchange 处理同步相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="6e37a-152">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

