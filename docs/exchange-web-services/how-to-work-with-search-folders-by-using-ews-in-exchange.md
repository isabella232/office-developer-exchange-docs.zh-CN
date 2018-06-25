---
title: 在 Exchange 使用 EWS 使用搜索文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: abe703c5-6d85-46d9-bf20-230c34782a9f
description: 了解如何创建、 获取、 更新和删除使用 EWS 托管 API 或 EWS 在 Exchange 搜索文件夹。
ms.openlocfilehash: e38ff50fcdb5e42cea3f4b2e25345375f84ae6eb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752931"
---
# <a name="work-with-search-folders-by-using-ews-in-exchange"></a><span data-ttu-id="957ad-103">在 Exchange 使用 EWS 使用搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-103">Work with search folders by using EWS in Exchange</span></span>

<span data-ttu-id="957ad-104">了解如何创建、 获取、 更新和删除使用 EWS 托管 API 或 EWS 在 Exchange 搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-104">Find out how to create, get, update, and delete search folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="957ad-105">搜索文件夹代表持久"始终在"搜索用户的邮箱中。</span><span class="sxs-lookup"><span data-stu-id="957ad-105">A search folder represents a persistent "always-on" search in a user's mailbox.</span></span> <span data-ttu-id="957ad-106">搜索文件夹查找，并像常规邮箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-106">A search folder looks and acts like a regular mailbox folder.</span></span> <span data-ttu-id="957ad-107">但是，而不是包含项目，它包含从其搜索范围文件夹上设置搜索条件相匹配的任何文件夹的项目的"虚拟"副本。</span><span class="sxs-lookup"><span data-stu-id="957ad-107">However, instead of containing items, it contains a "virtual" copy of items from any folders in its search scope that match the search criteria set on the folder.</span></span> <span data-ttu-id="957ad-108">应用程序和最终用户可以使用搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-108">Both applications and end-users can use search folders.</span></span> <span data-ttu-id="957ad-109">您的应用程序是否需要多次执行相同的搜索？</span><span class="sxs-lookup"><span data-stu-id="957ad-109">Does your application need to perform the same search over and over?</span></span> <span data-ttu-id="957ad-110">搜索文件夹是此任务的绝佳工具。</span><span class="sxs-lookup"><span data-stu-id="957ad-110">Search folders are a great tool for this task.</span></span> <span data-ttu-id="957ad-111">或者也许您只想要使用户能够访问和管理您的客户端中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-111">Or maybe you just want to give your users the ability to access and manage search folders in your client.</span></span> <span data-ttu-id="957ad-112">无论您的 EWS 托管 API 和 EWS 的方案启用应用程序以与搜索文件夹的完全交互。</span><span class="sxs-lookup"><span data-stu-id="957ad-112">Whatever your scenario, the EWS Managed API and EWS enable your application to fully interact with search folders.</span></span>
  
<span data-ttu-id="957ad-113">**表 1。EWS 托管 API 方法和用于处理的 EWS 操作搜索文件夹**</span><span class="sxs-lookup"><span data-stu-id="957ad-113">**Table 1. EWS Managed API methods and EWS operations for working with search folders**</span></span>

|<span data-ttu-id="957ad-114">**如果您希望...**</span><span class="sxs-lookup"><span data-stu-id="957ad-114">**If you want to…**</span></span>|<span data-ttu-id="957ad-115">**EWS 托管 API，在使用...**</span><span class="sxs-lookup"><span data-stu-id="957ad-115">**In the EWS Managed API, use…**</span></span>|<span data-ttu-id="957ad-116">**EWS，在使用...**</span><span class="sxs-lookup"><span data-stu-id="957ad-116">**In EWS, use…**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="957ad-117">创建搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-117">Create a search folder</span></span>  <br/> |[<span data-ttu-id="957ad-118">SearchFolder.Save</span><span class="sxs-lookup"><span data-stu-id="957ad-118">SearchFolder.Save</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="957ad-119">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="957ad-119">CreateFolder operation</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="957ad-120">获取搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-120">Get a search folder</span></span>  <br/> |[<span data-ttu-id="957ad-121">SearchFolder.Bind</span><span class="sxs-lookup"><span data-stu-id="957ad-121">SearchFolder.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="957ad-122">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="957ad-122">GetFolder operation</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="957ad-123">更新搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-123">Update a search folder</span></span>  <br/> |[<span data-ttu-id="957ad-124">SearchFolder.Update</span><span class="sxs-lookup"><span data-stu-id="957ad-124">SearchFolder.Update</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="957ad-125">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="957ad-125">UpdateFolder operation</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="957ad-126">删除搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-126">Delete a search folder</span></span>  <br/> |[<span data-ttu-id="957ad-127">SearchFolder.Delete</span><span class="sxs-lookup"><span data-stu-id="957ad-127">SearchFolder.Delete</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="957ad-128">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="957ad-128">DeleteFolder operation</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
   
## <a name="core-concepts-to-know-for-working-with-search-folders"></a><span data-ttu-id="957ad-129">要了解使用搜索文件夹的核心概念</span><span class="sxs-lookup"><span data-stu-id="957ad-129">Core concepts to know for working with search folders</span></span>
<span data-ttu-id="957ad-130"><a name="bk_CoreConcepts"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-130"></span></span>

<span data-ttu-id="957ad-131">使用搜索文件夹开始使用之前，您需要熟悉搜索筛选器的工作方式。</span><span class="sxs-lookup"><span data-stu-id="957ad-131">Before you start working with search folders, you'll want to be familiar with how search filters work.</span></span> <span data-ttu-id="957ad-132">搜索文件夹依赖于搜索筛选器来表达他们的条件。</span><span class="sxs-lookup"><span data-stu-id="957ad-132">Search folders rely on search filters to express their criteria.</span></span> <span data-ttu-id="957ad-133">搜索文件夹的搜索筛选器构建中相同的方式构建该[搜索操作的搜索筛选器](how-to-use-search-filters-with-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="957ad-133">Search filters for search folders are constructed in the same way that [search filters for search operations](how-to-use-search-filters-with-ews-in-exchange.md) are constructed.</span></span> 
  
## <a name="create-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="957ad-134">使用 EWS 托管 API 创建搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-134">Create a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="957ad-135"><a name="bk_CreateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-135"></span></span>

<span data-ttu-id="957ad-136">一般情况下，您创建搜索文件夹中创建一个正则文件夹的相同方式使用 EWS 托管 API。</span><span class="sxs-lookup"><span data-stu-id="957ad-136">Basically, you create a search folder using the EWS Managed API in the same way that you create a regular folder.</span></span> <span data-ttu-id="957ad-137">但是，而不是使用[文件夹类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)，使用[SearchFolder 类](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)，并设置[SearchParameters 属性](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx)可配置的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="957ad-137">However, instead of using the [Folder class](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx), you use the [SearchFolder class](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), and set the [SearchParameters property](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) to configure the search criteria.</span></span> 
  
<span data-ttu-id="957ad-138">在以下示例中，搜索文件夹创建收件箱发送的用户的经理及其子文件夹中查找所有邮件 sadie@contoso.com。</span><span class="sxs-lookup"><span data-stu-id="957ad-138">In the following example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="957ad-139">创建作为用户的邮箱中的搜索文件夹文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-139">The folder is created as a child of the Search Folders folder in the user's mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="957ad-140">您可以创建搜索文件夹作为用户的邮箱中的任何文件夹的子元素。</span><span class="sxs-lookup"><span data-stu-id="957ad-140">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="957ad-141">但是，如果您希望显示在在 Outlook 中的搜索文件夹下，新创建的文件夹，创建它使用[WellKnownFolderName 枚举](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)的**SearchFolders**值的搜索文件夹的已知文件夹下。</span><span class="sxs-lookup"><span data-stu-id="957ad-141">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **SearchFolders** value of the [WellKnownFolderName enumeration](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx).</span></span> 
  
<span data-ttu-id="957ad-142">本示例假定已初始化**ExchangeService**对象，在[凭据](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性的有效值。</span><span class="sxs-lookup"><span data-stu-id="957ad-142">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void CreateSearchFolder(ExchangeService service)
{
    // Create the folder.
    SearchFolder searchFolder = new SearchFolder(service);
    searchFolder.DisplayName = "From Manager";
    // Create a search filter to express the criteria
    // for the folder.
    EmailAddress manager = new EmailAddress("sadie@contoso.com");
    SearchFilter.IsEqualTo fromManagerFilter =
        new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, manager);
    // Set the search filter.
    searchFolder.SearchParameters.SearchFilter = fromManagerFilter;
    // Set the folder to search.
    searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
    // Set the search traversal. Deep will search all subfolders.
    searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
    // Call Save to make the EWS call to create the folder.
    searchFolder.Save(WellKnownFolderName.SearchFolders);
}
```

## <a name="create-a-search-folder-by-using-ews"></a><span data-ttu-id="957ad-143">使用 EWS 创建搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-143">Create a search folder by using EWS</span></span>
<span data-ttu-id="957ad-144"><a name="bk_CreateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-144"></span></span>

<span data-ttu-id="957ad-145">如果您使用 EWS，使用[SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx)元素[CreateFolder 操作](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)创建搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-145">If you are using EWS, use the [CreateFolder operation](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) with a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to create a search folder.</span></span> <span data-ttu-id="957ad-146">在下面的请求示例中，搜索文件夹创建收件箱发送的用户的经理及其子文件夹中查找所有邮件 sadie@contoso.com。</span><span class="sxs-lookup"><span data-stu-id="957ad-146">In the following request example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="957ad-147">用户的邮箱中的搜索文件夹文件夹中创建文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-147">The folder is created in the Search Folders folder in the user's mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="957ad-148">您可以创建搜索文件夹作为用户的邮箱中的任何文件夹的子元素。</span><span class="sxs-lookup"><span data-stu-id="957ad-148">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="957ad-149">但是，如果您希望显示在在 Outlook 中的搜索文件夹下，新创建的文件夹，创建它使用[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)元素的**Id**属性中的**searchfolders**值的搜索文件夹的已知文件夹下。</span><span class="sxs-lookup"><span data-stu-id="957ad-149">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **searchfolders** value in the **Id** attribute of the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) element.</span></span> 
  
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
    <m:CreateFolder>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="searchfolders" />
      </m:ParentFolderId>
      <m:Folders>
        <t:SearchFolder>
          <t:DisplayName>From Manager</t:DisplayName>
          <t:SearchParameters Traversal="Deep">
            <t:Restriction>
              <t:IsEqualTo>
                <t:FieldURI FieldURI="message:Sender" />
                <t:FieldURIOrConstant>
                  <t:Constant Value="sadie@contoso.com" />
                </t:FieldURIOrConstant>
              </t:IsEqualTo>
            </t:Restriction>
            <t:BaseFolderIds>
              <t:DistinguishedFolderId Id="inbox" />
            </t:BaseFolderIds>
          </t:SearchParameters>
        </t:SearchFolder>
      </m:Folders>
    </m:CreateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="957ad-150">服务器响应[CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx)消息，其中包括**NoError**，它指示成功[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="957ad-150">The server responds with a [CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="get-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="957ad-151">通过使用 EWS 托管 API 获取搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-151">Get a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="957ad-152"><a name="bk_RetrieveEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-152"></span></span>

<span data-ttu-id="957ad-153">使用[ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) EWS 托管 API 方法找到搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-153">Use the [ExchangeService.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) EWS Managed API method to find search folders.</span></span> <span data-ttu-id="957ad-154">但请注意，您不能限制搜索结果仅包括搜索文件夹;您需要记住的时处理结果。</span><span class="sxs-lookup"><span data-stu-id="957ad-154">Note, however, that you can't limit your results to only include search folders; you'll want to keep that in mind when you process the results.</span></span> <span data-ttu-id="957ad-155">[SearchFolder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx)方法用于获取搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-155">Use the [SearchFolder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) method to get search folders.</span></span> 
  
<span data-ttu-id="957ad-156">下面的示例在搜索文件夹文件夹中找到的前 10 的文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-156">The following example finds the first 10 folders in the Search Folders folder.</span></span> <span data-ttu-id="957ad-157">检查以确定是否每个搜索文件夹，并且如果是，获取搜索文件夹，并显示多少目标文件夹搜索。</span><span class="sxs-lookup"><span data-stu-id="957ad-157">It checks to determine whether each one is a search folder, and if so, it gets the search folder and displays how many target folders it searches.</span></span>
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void GetSearchFolders(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You can't request only search folders in 
            // a FindFolders request, so other search folders might also be present.
            if (folder is SearchFolder)
            {
                Console.WriteLine("{0} is a search folder.", folder.DisplayName);
                // In order to access the SearchParameters property,
                // you have to bind to the folder. SearchParameters are not
                // returned in FindFolders results.
                SearchFolder searchFolder = SearchFolder.Bind(service, folder.Id);
                Console.WriteLine("Number of folders searched: {0}.",
                    searchFolder.SearchParameters.RootFolderIds.Count);
            }
            else
            {
                Console.WriteLine("{0} is NOT a search folder.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="get-a-search-folder-by-using-ews"></a><span data-ttu-id="957ad-158">通过使用 EWS 获取搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-158">Get a search folder by using EWS</span></span>
<span data-ttu-id="957ad-159"><a name="bk_RetrieveEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-159"></span></span>

<span data-ttu-id="957ad-160">如果您正在使用 EWS，使用[FindFolder 操作](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)以查找搜索文件夹和[GetFolder 操作](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)以获取搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-160">If you're using EWS, use the [FindFolder operation](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) to find search folders, and the [GetFolder operation](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get search folders.</span></span> <span data-ttu-id="957ad-161">搜索文件夹的成功**GetFolder**响应将包含[SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="957ad-161">A successful **GetFolder** response for a search folder will contain a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="957ad-162">下面的请求示例在搜索文件夹文件夹中找到的前 10 的文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-162">The following request example finds the first 10 folders in the Search Folders folder.</span></span> 
  
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
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="searchfolders" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="957ad-163">服务器将返回以下响应，其中显示一个搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-163">The server returns the following response, which shows one search folder.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="3" TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Folders>
              <t:SearchFolder>
                <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
                <t:DisplayName>From Manager</t:DisplayName>
              </t:SearchFolder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="957ad-164">下面的示例请求的**GetFolder**操作请求中使用从以前响应[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)元素的值，若要获取的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-164">The following example of a request uses the value of the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) element from the previous response in a **GetFolder** operation request to get the search folder.</span></span> 
  
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
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="957ad-165">服务器将返回以下响应与搜索文件夹的所有一类的属性。</span><span class="sxs-lookup"><span data-stu-id="957ad-165">The server returns the following response with all the first-class properties for the search folder.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:SearchFolder>
              <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
              <t:ParentFolderId Id="AQMkAGM2..." ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>From Manager</t:DisplayName>
              <t:TotalCount>8</t:TotalCount>
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
              <t:SearchParameters Traversal="Deep">
                <t:Restriction>
                  <t:IsEqualTo>
                    <t:FieldURI FieldURI="message:Sender" />
                    <t:FieldURIOrConstant>
                      <t:Constant Value="/o=First Organization/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=8d84a3f4cbb34d48838a3aecf99795c0-Sadie" />
                    </t:FieldURIOrConstant>
                  </t:IsEqualTo>
                </t:Restriction>
                <t:BaseFolderIds>
                  <t:FolderId Id="AQMkAGM2..." ChangeKey="AQAAAA==" />
                </t:BaseFolderIds>
              </t:SearchParameters>
            </t:SearchFolder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="update-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="957ad-166">使用 EWS 托管 API 更新搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-166">Update a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="957ad-167"><a name="bk_UpdateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-167"></span></span>

<span data-ttu-id="957ad-168">使用**SearchFolder**对象上[Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) EWS 托管 API 方法更新搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-168">Use the [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to update a search folder.</span></span> <span data-ttu-id="957ad-169">下面的示例更新搜索文件夹上的搜索条件的显示名称"从管理器"。</span><span class="sxs-lookup"><span data-stu-id="957ad-169">The following example updates the search criteria on a search folder with the display name "From Manager".</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void UpdateSearchFolder(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You cannot request only search folders in 
            // a FindFolders request, so other search folders might also be present.
            if (folder is SearchFolder &amp;&amp; folder.DisplayName.Equals("From Manager"))
            {
                Console.WriteLine("\"{0}\" folder found.", folder.DisplayName);
                SearchFolder searchFolder = folder as SearchFolder;
                EmailAddress newManager = new EmailAddress("hope@contoso.com");
                SearchFilter.IsEqualTo newManagerFilter =
                    new SearchFilter.IsEqualTo(EmailMessageSchema.Sender, newManager);
                searchFolder.SearchParameters.SearchFilter = newManagerFilter;
                searchFolder.SearchParameters.RootFolderIds.Add(WellKnownFolderName.Inbox);
                searchFolder.SearchParameters.Traversal = SearchFolderTraversal.Deep;
                searchFolder.Update();
                Console.WriteLine("\"{0}\" folder updated.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="update-a-search-folder-by-using-ews"></a><span data-ttu-id="957ad-170">使用 EWS 更新搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-170">Update a search folder by using EWS</span></span>
<span data-ttu-id="957ad-171"><a name="bk_UpdateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-171"></span></span>

<span data-ttu-id="957ad-172">如果您正在使用 EWS，使用[SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx)元素[UpdateFolder 操作](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)更新搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-172">If you're using EWS, use the [UpdateFolder operation](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) with a [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to update a search folder.</span></span> <span data-ttu-id="957ad-173">下面的请求示例更新"从管理器"搜索文件夹上的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="957ad-173">The following request example updates the search criteria on the "From Manager" search folder.</span></span> 
  
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
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:SearchParameters" />
              <t:SearchFolder>
                <t:SearchParameters Traversal="Deep">
                  <t:Restriction>
                    <t:IsEqualTo>
                      <t:FieldURI FieldURI="message:Sender" />
                      <t:FieldURIOrConstant>
                        <t:Constant Value="hope@contoso.com" />
                      </t:FieldURIOrConstant>
                    </t:IsEqualTo>
                  </t:Restriction>
                  <t:BaseFolderIds>
                    <t:DistinguishedFolderId Id="inbox" />
                  </t:BaseFolderIds>
                </t:SearchParameters>
              </t:SearchFolder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="957ad-174">服务器响应包含**NoError**，它指示成功[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值[UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)消息。</span><span class="sxs-lookup"><span data-stu-id="957ad-174">The server responds with an [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="delete-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="957ad-175">使用 EWS 托管 API 删除搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-175">Delete a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="957ad-176"><a name="bk_DeleteEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-176"></span></span>

<span data-ttu-id="957ad-177">使用**SearchFolder**对象上[Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) EWS 托管 API 方法删除搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-177">Use the [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to delete a search folder.</span></span> <span data-ttu-id="957ad-178">下面的示例删除搜索文件夹显示名称为"从管理器"。</span><span class="sxs-lookup"><span data-stu-id="957ad-178">The following example deletes a search folder with the display name "From Manager".</span></span> <span data-ttu-id="957ad-179">删除的搜索文件夹移至已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-179">The deleted search folder is moved to the Deleted Items folder.</span></span> 
  
```cs
using Microsoft.Exchange.WebServices.Data;
static void DeleteSearchFolder(ExchangeService service)
{
    FolderView folderView = new FolderView(10);
    folderView.PropertySet = new PropertySet(FolderSchema.DisplayName);
    try
    {
        FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.SearchFolders, folderView);
        foreach (Folder folder in findResults.Folders)
        {
            // You cannot request only search folders in 
            // a FindFolders request, so other folders might also be present.
            if (folder is SearchFolder &amp;&amp; folder.DisplayName.Equals("From Manager"))
            {
                Console.WriteLine("\"{0}\" folder found.", folder.DisplayName);
                folder.Delete(DeleteMode.MoveToDeletedItems);
                Console.WriteLine("\"{0}\" folder deleted.", folder.DisplayName);
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

## <a name="delete-a-search-folder-by-using-ews"></a><span data-ttu-id="957ad-180">使用 EWS 删除搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="957ad-180">Delete a search folder by using EWS</span></span>
<span data-ttu-id="957ad-181"><a name="bk_DeleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="957ad-181"></span></span>

<span data-ttu-id="957ad-182">如果您正在使用 EWS，使用[DeleteFolder 操作](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)删除搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-182">If you're using EWS, use the [DeleteFolder operation](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) to delete a search folder.</span></span> <span data-ttu-id="957ad-183">下面的示例删除搜索文件夹，并将其移到已删除邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="957ad-183">The following example deletes a search folder and moves it to the Deleted Items folder.</span></span> 
  
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
    <m:DeleteFolder DeleteType="MoveToDeletedItems">
      <m:FolderIds>
        <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
      </m:FolderIds>
    </m:DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="957ad-184">服务器响应[DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx)消息，其中包括**NoError**，它指示成功[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="957ad-184">The server responds with a [DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="957ad-185">另请参阅</span><span class="sxs-lookup"><span data-stu-id="957ad-185">See also</span></span>


- [<span data-ttu-id="957ad-186">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="957ad-186">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)
    
- [<span data-ttu-id="957ad-187">在 Exchange 中使用 EWS 使用搜索筛选器</span><span class="sxs-lookup"><span data-stu-id="957ad-187">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)
    
- [<span data-ttu-id="957ad-188">SearchFolder 类</span><span class="sxs-lookup"><span data-stu-id="957ad-188">SearchFolder class</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="957ad-189">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="957ad-189">CreateFolder operation</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)
    
- [<span data-ttu-id="957ad-190">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="957ad-190">FindFolder operation</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)
    
- [<span data-ttu-id="957ad-191">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="957ad-191">GetFolder operation</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)
    
- [<span data-ttu-id="957ad-192">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="957ad-192">UpdateFolder operation</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)
    
- [<span data-ttu-id="957ad-193">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="957ad-193">DeleteFolder operation</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)
    

