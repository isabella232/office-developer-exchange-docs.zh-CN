---
title: 在搜索文件夹中使用 EWS 处理Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: abe703c5-6d85-46d9-bf20-230c34782a9f
description: 了解如何使用 EWS 托管 API 或 EWS 在搜索文件夹中创建、获取、更新和删除Exchange。
ms.openlocfilehash: abbbe10341b86910991b885f73c40575f6f6078e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521074"
---
# <a name="work-with-search-folders-by-using-ews-in-exchange"></a>在搜索文件夹中使用 EWS 处理Exchange

了解如何使用 EWS 托管 API 或 EWS 在搜索文件夹中创建、获取、更新和删除Exchange。
  
搜索文件夹表示用户邮箱中的持久"始终打开"搜索。 搜索文件夹的外观和作用类似于常规邮箱文件夹。 但是，它不包含项目，而是包含来自其搜索范围内任何文件夹的项目的"虚拟"副本，该副本与文件夹上设置的搜索条件匹配。 应用程序和最终用户都可以使用搜索文件夹。 应用程序是否需要一次又一次地执行相同的搜索？ 搜索文件夹是执行此任务的一种很好的工具。 或者，您可能只是希望让用户能够访问和管理客户端中的搜索文件夹。 无论使用何种方案，EWS 托管 API 和 EWS 都支持应用程序与搜索文件夹完全交互。

> [!NOTE] 
> 本文仅在联机模式下使用Outlook应用。 搜索文件夹不同步;因此，联机模式下创建的搜索文件夹将不会在缓存模式下显示。
  
**表 1.用于处理搜索文件夹的 EWS 托管 API 方法和 EWS 操作**

|如果你想要...|在 EWS 托管 API 中，使用…|在 EWS 中，使用…|
|:-----|:-----|:-----|
|创建搜索文件夹  <br/> |[SearchFolder.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder 操作](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|获取搜索文件夹  <br/> |[SearchFolder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) <br/> |[GetFolder 操作](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|更新搜索文件夹  <br/> |[SearchFolder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|删除搜索文件夹  <br/> |[SearchFolder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |
   
## <a name="core-concepts-to-know-for-working-with-search-folders"></a>使用搜索文件夹需要知道的核心概念
<a name="bk_CoreConcepts"> </a>

开始使用搜索文件夹之前，你需要熟悉搜索筛选器如何工作。 搜索文件夹依赖搜索筛选器来表示其条件。 搜索文件夹的搜索筛选器的构建方式与搜索操作 [搜索](how-to-use-search-filters-with-ews-in-exchange.md) 筛选器的构造方式相同。 
  
## <a name="create-a-search-folder-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建搜索文件夹
<a name="bk_CreateEWSMA"> </a>

基本上，使用 EWS 托管 API 创建搜索文件夹的方式与创建常规文件夹的方法相同。 但是，不使用 Folder [类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)，而是使用 [SearchFolder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)，并设置 [SearchParameters](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.searchparameters%28v=exchg.80%29.aspx) 属性来配置搜索条件。 
  
在下面的示例中，将创建一个搜索文件夹，以查找收件箱及其子文件夹中由用户的经理发送的所有邮件，sadie@contoso.com。 该文件夹创建为用户邮箱中"搜索文件夹"文件夹的子文件夹。
  
> [!NOTE]
> 可以将搜索文件夹创建为用户邮箱中任何文件夹的子级。 但是，如果希望新创建的文件夹显示在 Outlook 中的"搜索文件夹"下，则使用 [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx)枚举的 **SearchFolders** 值在"搜索文件夹"已知文件夹下创建该文件夹。 
  
此示例假定 **ExchangeService** 对象已使用 [凭据](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.credentials%28v=exchg.80%29.aspx)的有效值和 [Url](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.url%28v=exchg.80%29.aspx) 属性进行了初始化。 
  
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

## <a name="create-a-search-folder-by-using-ews"></a>使用 EWS 创建搜索文件夹
<a name="bk_CreateEWS"> </a>

如果使用的是 EWS，请对 [SearchFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) 元素使用 [CreateFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) 操作来创建搜索文件夹。 在下面的请求示例中，将创建一个搜索文件夹，以查找"收件箱"中由用户的经理（即用户）发送的所有邮件及其子 sadie@contoso.com。 该文件夹是在用户邮箱的"搜索文件夹"文件夹中创建的。 
  
> [!NOTE]
> 可以将搜索文件夹创建为用户邮箱中任何文件夹的子级。 但是，如果您希望新创建的文件夹显示在 Outlook 中的搜索文件夹下，则使用 [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)元素 **的 Id** 属性中的 **searchfolders** 值在"搜索文件夹已知文件夹"下创建它。 
  
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

服务器响应一条 [CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx)消息，其中包含 **NoError**[的 ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值，指示成功。
  
## <a name="get-a-search-folder-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 获取搜索文件夹
<a name="bk_RetrieveEWSMA"> </a>

使用 [ExchangeService.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) EWS 托管 API 方法来查找搜索文件夹。 但是请注意，不能将结果限制为仅包含搜索文件夹;处理结果时，需要牢记这一点。 使用 [SearchFolder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder.bind%28v=exchg.80%29.aspx) 方法可获取搜索文件夹。 
  
以下示例在"搜索文件夹"文件夹中查找前 10 个文件夹。 它将检查以确定每个文件夹是否是搜索文件夹，如果是，它将获取搜索文件夹并显示它搜索的目标文件夹。
  
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

## <a name="get-a-search-folder-by-using-ews"></a>使用 EWS 获取搜索文件夹
<a name="bk_RetrieveEWS"> </a>

如果使用的是 EWS，请使用 [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) 操作查找搜索文件夹，使用 [GetFolder 操作](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) 获取搜索文件夹。 搜索文件夹 **的成功 GetFolder** 响应将包含 [SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) 元素。 以下请求示例在"搜索文件夹"文件夹中查找前 10 个文件夹。 
  
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

服务器返回以下响应，其中显示一个搜索文件夹。
  
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

下面的请求示例使用 **GetFolder** 操作请求中上一响应中的 [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)元素的值获取搜索文件夹。 
  
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

服务器返回以下响应，该响应包含搜索文件夹的所有一级属性。
  
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

## <a name="update-a-search-folder-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 更新搜索文件夹
<a name="bk_UpdateEWSMA"> </a>

对 **SearchFolder** 对象使用 [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) EWS 托管 API 方法更新搜索文件夹。 下面的示例使用"From Manager"显示名称搜索文件夹上的搜索条件。 
  
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

## <a name="update-a-search-folder-by-using-ews"></a>使用 EWS 更新搜索文件夹
<a name="bk_UpdateEWS"> </a>

如果使用的是 EWS，请对 [SearchFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) 元素使用 [UpdateFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) 操作来更新搜索文件夹。 以下请求示例更新"From Manager"搜索文件夹上的搜索条件。 
  
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

服务器响应 [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)消息，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值，指示成功。
  
## <a name="delete-a-search-folder-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除搜索文件夹
<a name="bk_DeleteEWSMA"> </a>

使用 **SearchFolder** 对象的 [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) EWS 托管 API 方法可删除搜索文件夹。 以下示例删除搜索文件夹，该文件夹显示名称"From Manager"。 已删除的搜索文件夹将移动到"已删除邮件"文件夹。 
  
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

## <a name="delete-a-search-folder-by-using-ews"></a>使用 EWS 删除搜索文件夹
<a name="bk_DeleteEWS"> </a>

如果使用的是 EWS，请使用 [DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) 删除搜索文件夹。 以下示例删除搜索文件夹，并移动到"已删除邮件"文件夹。 
  
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

服务器响应一条 [DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx)消息，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值，指示成功。
  
## <a name="see-also"></a>另请参阅

- [搜索和交换中的 EWS](search-and-ews-in-exchange.md)   
- [将搜索筛选器与 EWS 一Exchange](how-to-use-search-filters-with-ews-in-exchange.md)    
- [SearchFolder 类](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)    
- [CreateFolder 操作](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)    
- [FindFolder 操作](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)   
- [GetFolder 操作](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)    
- [UpdateFolder 操作](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)    
- [DeleteFolder 操作](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)
    

