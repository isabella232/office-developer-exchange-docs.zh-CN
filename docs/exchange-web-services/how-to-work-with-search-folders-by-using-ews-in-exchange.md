---
title: 使用 Exchange 中的 EWS 处理搜索文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: abe703c5-6d85-46d9-bf20-230c34782a9f
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建、获取、更新和删除搜索文件夹。
ms.openlocfilehash: 880c14bc99c4f6c674d4f7566036c4b8f5f19e55
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456365"
---
# <a name="work-with-search-folders-by-using-ews-in-exchange"></a><span data-ttu-id="5746e-103">使用 Exchange 中的 EWS 处理搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-103">Work with search folders by using EWS in Exchange</span></span>

<span data-ttu-id="5746e-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建、获取、更新和删除搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-104">Find out how to create, get, update, and delete search folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="5746e-105">"搜索文件夹" 表示用户邮箱中的持续 "永不开" 搜索。</span><span class="sxs-lookup"><span data-stu-id="5746e-105">A search folder represents a persistent "always-on" search in a user's mailbox.</span></span> <span data-ttu-id="5746e-106">搜索文件夹的外观和行为类似于常规邮箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-106">A search folder looks and acts like a regular mailbox folder.</span></span> <span data-ttu-id="5746e-107">但是，它包含的搜索范围中的任何文件夹中的项目的 "虚拟" 副本与文件夹中设置的搜索条件相匹配，而不是包含项目。</span><span class="sxs-lookup"><span data-stu-id="5746e-107">However, instead of containing items, it contains a "virtual" copy of items from any folders in its search scope that match the search criteria set on the folder.</span></span> <span data-ttu-id="5746e-108">应用程序和最终用户都可以使用 "搜索文件夹"。</span><span class="sxs-lookup"><span data-stu-id="5746e-108">Both applications and end-users can use search folders.</span></span> <span data-ttu-id="5746e-109">您的应用程序是否需要同时执行相同的搜索？</span><span class="sxs-lookup"><span data-stu-id="5746e-109">Does your application need to perform the same search over and over?</span></span> <span data-ttu-id="5746e-110">搜索文件夹是此任务的一个非常有用的工具。</span><span class="sxs-lookup"><span data-stu-id="5746e-110">Search folders are a great tool for this task.</span></span> <span data-ttu-id="5746e-111">或者，您可能只希望让用户能够访问和管理客户端中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-111">Or maybe you just want to give your users the ability to access and manage search folders in your client.</span></span> <span data-ttu-id="5746e-112">无论在什么情况下，EWS 托管 API 和 EWS 都使应用程序能够与搜索文件夹完全交互。</span><span class="sxs-lookup"><span data-stu-id="5746e-112">Whatever your scenario, the EWS Managed API and EWS enable your application to fully interact with search folders.</span></span>

> [!NOTE] 
> <span data-ttu-id="5746e-113">本文仅适用于在联机模式下使用 Outlook 的情况。</span><span class="sxs-lookup"><span data-stu-id="5746e-113">This article applies only when using Outlook in online mode.</span></span> <span data-ttu-id="5746e-114">搜索文件夹不同步;因此，在联机模式下创建的搜索文件夹不会显示在缓存模式中。</span><span class="sxs-lookup"><span data-stu-id="5746e-114">Search folders do not sync; therefore, search folders created in online mode will not appear in cached mode.</span></span>
  
<span data-ttu-id="5746e-115">**表1。使用 "搜索文件夹" 的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="5746e-115">**Table 1. EWS Managed API methods and EWS operations for working with search folders**</span></span>

|<span data-ttu-id="5746e-116">如果您想要 .。。</span><span class="sxs-lookup"><span data-stu-id="5746e-116">If you want to…</span></span>|<span data-ttu-id="5746e-117">在 EWS 托管 API 中，使用 .。。</span><span class="sxs-lookup"><span data-stu-id="5746e-117">In the EWS Managed API, use…</span></span>|<span data-ttu-id="5746e-118">在 EWS 中，使用 .。。</span><span class="sxs-lookup"><span data-stu-id="5746e-118">In EWS, use…</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5746e-119">创建搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-119">Create a search folder</span></span>  <br/> |[<span data-ttu-id="5746e-120">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="5746e-120">SearchFolder.Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="5746e-121">CreateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-121">CreateFolder operation</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="5746e-122">获取搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-122">Get a search folder</span></span>  <br/> |[<span data-ttu-id="5746e-123">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="5746e-123">SearchFolder.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="5746e-124">GetFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-124">GetFolder operation</span></span>](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="5746e-125">更新搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-125">Update a search folder</span></span>  <br/> |[<span data-ttu-id="5746e-126">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="5746e-126">SearchFolder.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="5746e-127">UpdateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-127">UpdateFolder operation</span></span>](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="5746e-128">删除搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-128">Delete a search folder</span></span>  <br/> |[<span data-ttu-id="5746e-129">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="5746e-129">SearchFolder.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="5746e-130">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-130">DeleteFolder operation</span></span>](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
   
## <a name="core-concepts-to-know-for-working-with-search-folders"></a><span data-ttu-id="5746e-131">使用 "搜索文件夹" 时要了解的核心概念</span><span class="sxs-lookup"><span data-stu-id="5746e-131">Core concepts to know for working with search folders</span></span>
<span data-ttu-id="5746e-132"><a name="bk_CoreConcepts"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-132"><a name="bk_CoreConcepts"> </a></span></span>

<span data-ttu-id="5746e-133">在开始使用 "搜索文件夹" 之前，您需要熟悉搜索筛选器的工作方式。</span><span class="sxs-lookup"><span data-stu-id="5746e-133">Before you start working with search folders, you'll want to be familiar with how search filters work.</span></span> <span data-ttu-id="5746e-134">搜索文件夹依赖搜索筛选器来表达其条件。</span><span class="sxs-lookup"><span data-stu-id="5746e-134">Search folders rely on search filters to express their criteria.</span></span> <span data-ttu-id="5746e-135">搜索文件夹的搜索筛选器的构造方式与搜索操作的搜索[筛选器](how-to-use-search-filters-with-ews-in-exchange.md)的构造方式相同。</span><span class="sxs-lookup"><span data-stu-id="5746e-135">Search filters for search folders are constructed in the same way that [search filters for search operations](how-to-use-search-filters-with-ews-in-exchange.md) are constructed.</span></span> 
  
## <a name="create-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="5746e-136">使用 EWS 托管 API 创建搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-136">Create a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="5746e-137"><a name="bk_CreateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-137"><a name="bk_CreateEWSMA"> </a></span></span>

<span data-ttu-id="5746e-138">基本上来说，使用 EWS 托管 API 创建搜索文件夹的方式与创建常规文件夹的方式相同。</span><span class="sxs-lookup"><span data-stu-id="5746e-138">Basically, you create a search folder using the EWS Managed API in the same way that you create a regular folder.</span></span> <span data-ttu-id="5746e-139">但是，您可以使用[SearchFolder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)，并将[SearchParameters 属性](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx)设置为配置搜索条件，而不是使用[Folder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5746e-139">However, instead of using the [Folder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx), you use the [SearchFolder class](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), and set the [SearchParameters property](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) to configure the search criteria.</span></span> 
  
<span data-ttu-id="5746e-140">在下面的示例中，将创建一个搜索文件夹，以查找收件箱中的所有邮件及其子文件夹中由用户的经理（sadie@contoso.com）发送的所有邮件。</span><span class="sxs-lookup"><span data-stu-id="5746e-140">In the following example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="5746e-141">该文件夹创建为用户邮箱中 "搜索文件夹" 文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-141">The folder is created as a child of the Search Folders folder in the user's mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5746e-142">您可以将搜索文件夹创建为用户邮箱中的任何文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-142">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="5746e-143">但是，如果您希望新创建的文件夹显示在 Outlook 中的 "搜索文件夹" 下，请使用[WellKnownFolderName 枚举](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)的**SearchFolders**值在 "搜索文件夹" 的已知文件夹下创建该文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-143">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **SearchFolders** value of the [WellKnownFolderName enumeration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx).</span></span> 
  
<span data-ttu-id="5746e-144">此示例假定已使用[凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)和[Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx)属性中的有效值对**ExchangeService**对象进行了初始化。</span><span class="sxs-lookup"><span data-stu-id="5746e-144">This example assumes that the **ExchangeService** object has been initialized with valid values in the [Credentials](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx) and [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) properties.</span></span> 
  
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

## <a name="create-a-search-folder-by-using-ews"></a><span data-ttu-id="5746e-145">使用 EWS 创建搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-145">Create a search folder by using EWS</span></span>
<span data-ttu-id="5746e-146"><a name="bk_CreateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-146"><a name="bk_CreateEWS"> </a></span></span>

<span data-ttu-id="5746e-147">如果使用 EWS，请将[CreateFolder 操作](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)与[SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx)元素一起使用，以创建搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-147">If you are using EWS, use the [CreateFolder operation](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) with a [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to create a search folder.</span></span> <span data-ttu-id="5746e-148">在下面的请求示例中，将创建一个搜索文件夹，以查找收件箱中的所有邮件及其子文件夹中由用户的经理（sadie@contoso.com）发送的所有邮件。</span><span class="sxs-lookup"><span data-stu-id="5746e-148">In the following request example, a search folder is created to find all messages in the Inbox and its subfolders that were sent by the user's manager, sadie@contoso.com.</span></span> <span data-ttu-id="5746e-149">该文件夹在用户邮箱的 "搜索文件夹" 文件夹中创建。</span><span class="sxs-lookup"><span data-stu-id="5746e-149">The folder is created in the Search Folders folder in the user's mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5746e-150">您可以将搜索文件夹创建为用户邮箱中的任何文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-150">You can create a search folder as a child of any folder in the user's mailbox.</span></span> <span data-ttu-id="5746e-151">但是，如果您希望新创建的文件夹显示在 Outlook 中的 "搜索文件夹" 下，请使用[DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)元素的**Id**属性中的**Searchfolders**值在 "搜索文件夹" 的已知文件夹下创建它。</span><span class="sxs-lookup"><span data-stu-id="5746e-151">However, if you want the newly created folder to show up under Search Folders in Outlook, create it under the Search Folders well-known folder, using the **searchfolders** value in the **Id** attribute of the [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) element.</span></span> 
  
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

<span data-ttu-id="5746e-152">服务器使用包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**的[CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx)消息进行响应，指示成功。</span><span class="sxs-lookup"><span data-stu-id="5746e-152">The server responds with a [CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="get-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="5746e-153">使用 EWS 托管 API 获取搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-153">Get a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="5746e-154"><a name="bk_RetrieveEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-154"><a name="bk_RetrieveEWSMA"> </a></span></span>

<span data-ttu-id="5746e-155">使用 FindFolders EWS 托管 API 方法查找搜索文件夹[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="5746e-155">Use the [ExchangeService.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) EWS Managed API method to find search folders.</span></span> <span data-ttu-id="5746e-156">但请注意，您无法将结果限制为仅包含搜索文件夹;您需要在处理结果时记住这一点。</span><span class="sxs-lookup"><span data-stu-id="5746e-156">Note, however, that you can't limit your results to only include search folders; you'll want to keep that in mind when you process the results.</span></span> <span data-ttu-id="5746e-157">使用[SearchFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx)方法获取搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-157">Use the [SearchFolder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) method to get search folders.</span></span> 
  
<span data-ttu-id="5746e-158">下面的示例查找 "搜索文件夹" 文件夹中的前10个文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-158">The following example finds the first 10 folders in the Search Folders folder.</span></span> <span data-ttu-id="5746e-159">它会检查以确定每个是否是一个搜索文件夹，如果是，它将获取搜索文件夹，并显示它搜索的目标文件夹数。</span><span class="sxs-lookup"><span data-stu-id="5746e-159">It checks to determine whether each one is a search folder, and if so, it gets the search folder and displays how many target folders it searches.</span></span>
  
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

## <a name="get-a-search-folder-by-using-ews"></a><span data-ttu-id="5746e-160">使用 EWS 获取搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-160">Get a search folder by using EWS</span></span>
<span data-ttu-id="5746e-161"><a name="bk_RetrieveEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-161"><a name="bk_RetrieveEWS"> </a></span></span>

<span data-ttu-id="5746e-162">如果使用的是 EWS，请使用[FindFolder 操作](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)查找搜索文件夹，并使用[GetFolder 操作](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)获取搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-162">If you're using EWS, use the [FindFolder operation](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) to find search folders, and the [GetFolder operation](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) to get search folders.</span></span> <span data-ttu-id="5746e-163">搜索文件夹的成功的**GetFolder**响应将包含[SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="5746e-163">A successful **GetFolder** response for a search folder will contain a [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="5746e-164">下面的请求示例查找 "搜索文件夹" 文件夹中的前10个文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-164">The following request example finds the first 10 folders in the Search Folders folder.</span></span> 
  
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

<span data-ttu-id="5746e-165">服务器返回以下响应，其中显示一个搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-165">The server returns the following response, which shows one search folder.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="5746e-166">下面的请求示例使用**GetFolder**操作请求中的上一个响应中的[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)元素的值来获取搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-166">The following example of a request uses the value of the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) element from the previous response in a **GetFolder** operation request to get the search folder.</span></span> 
  
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

<span data-ttu-id="5746e-167">服务器将返回搜索文件夹的所有第一类属性的以下响应。</span><span class="sxs-lookup"><span data-stu-id="5746e-167">The server returns the following response with all the first-class properties for the search folder.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="712" MinorBuildNumber="22" Version="V2_3" 
        xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="update-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="5746e-168">使用 EWS 托管 API 更新搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-168">Update a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="5746e-169"><a name="bk_UpdateEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-169"><a name="bk_UpdateEWSMA"> </a></span></span>

<span data-ttu-id="5746e-170">使用文件夹的**SearchFolder**对象[更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)EWS 托管 API 方法以更新搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-170">Use the [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to update a search folder.</span></span> <span data-ttu-id="5746e-171">下面的示例使用显示名称 "From Manager" 更新搜索文件夹中的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="5746e-171">The following example updates the search criteria on a search folder with the display name "From Manager".</span></span> 
  
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

## <a name="update-a-search-folder-by-using-ews"></a><span data-ttu-id="5746e-172">使用 EWS 更新搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-172">Update a search folder by using EWS</span></span>
<span data-ttu-id="5746e-173"><a name="bk_UpdateEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-173"><a name="bk_UpdateEWS"> </a></span></span>

<span data-ttu-id="5746e-174">如果使用的是 EWS，请将[UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)与[SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx)元素一起使用，以更新搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-174">If you're using EWS, use the [UpdateFolder operation](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) with a [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) element to update a search folder.</span></span> <span data-ttu-id="5746e-175">下面的请求示例更新 "发件人经理" 搜索文件夹中的搜索条件。</span><span class="sxs-lookup"><span data-stu-id="5746e-175">The following request example updates the search criteria on the "From Manager" search folder.</span></span> 
  
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

<span data-ttu-id="5746e-176">服务器响应包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值为**NoError**的[UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)消息，指示成功。</span><span class="sxs-lookup"><span data-stu-id="5746e-176">The server responds with an [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="delete-a-search-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="5746e-177">使用 EWS 托管 API 删除搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-177">Delete a search folder by using the EWS Managed API</span></span>
<span data-ttu-id="5746e-178"><a name="bk_DeleteEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-178"><a name="bk_DeleteEWSMA"> </a></span></span>

<span data-ttu-id="5746e-179">使用[文件夹删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) **SearchFolder**对象上的 EWS 托管 API 方法可删除搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-179">Use the [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) EWS Managed API method on a **SearchFolder** object to delete a search folder.</span></span> <span data-ttu-id="5746e-180">下面的示例将删除显示名称为 "From Manager" 的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-180">The following example deletes a search folder with the display name "From Manager".</span></span> <span data-ttu-id="5746e-181">"已删除的搜索文件夹" 将移至 "已删除邮件" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-181">The deleted search folder is moved to the Deleted Items folder.</span></span> 
  
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

## <a name="delete-a-search-folder-by-using-ews"></a><span data-ttu-id="5746e-182">使用 EWS 删除搜索文件夹</span><span class="sxs-lookup"><span data-stu-id="5746e-182">Delete a search folder by using EWS</span></span>
<span data-ttu-id="5746e-183"><a name="bk_DeleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5746e-183"><a name="bk_DeleteEWS"> </a></span></span>

<span data-ttu-id="5746e-184">如果您使用的是 EWS，请使用[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)删除搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="5746e-184">If you're using EWS, use the [DeleteFolder operation](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) to delete a search folder.</span></span> <span data-ttu-id="5746e-185">下面的示例删除 "搜索文件夹" 并将其移动到 "已删除邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="5746e-185">The following example deletes a search folder and moves it to the Deleted Items folder.</span></span> 
  
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
    <m:DeleteFolder DeleteType="MoveToDeletedItems">
      <m:FolderIds>
        <t:FolderId Id="AAMkAGM2..." ChangeKey="CAAAABYA..." />
      </m:FolderIds>
    </m:DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="5746e-186">服务器使用包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**的[DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx)消息进行响应，指示成功。</span><span class="sxs-lookup"><span data-stu-id="5746e-186">The server responds with a [DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates success.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5746e-187">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5746e-187">See also</span></span>

- [<span data-ttu-id="5746e-188">搜索和交换中的 EWS</span><span class="sxs-lookup"><span data-stu-id="5746e-188">Search and EWS in Exchange</span></span>](search-and-ews-in-exchange.md)   
- [<span data-ttu-id="5746e-189">在 Exchange 中将搜索筛选器与 EWS 结合使用</span><span class="sxs-lookup"><span data-stu-id="5746e-189">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)    
- [<span data-ttu-id="5746e-190">SearchFolder 类</span><span class="sxs-lookup"><span data-stu-id="5746e-190">SearchFolder class</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="5746e-191">CreateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-191">CreateFolder operation</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)    
- [<span data-ttu-id="5746e-192">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-192">FindFolder operation</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [<span data-ttu-id="5746e-193">GetFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-193">GetFolder operation</span></span>](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)    
- [<span data-ttu-id="5746e-194">UpdateFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-194">UpdateFolder operation</span></span>](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)    
- [<span data-ttu-id="5746e-195">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5746e-195">DeleteFolder operation</span></span>](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)
    

