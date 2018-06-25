---
title: 在 Exchange 使用 EWS 设置另一个用户的文件夹权限
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: 了解如何使用 EWS 的 EWS 托管 API 在 Exchange 文件夹上设置权限级别。
ms.openlocfilehash: 5bf570612d6349628e7f3abf858daa33daa13745
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752888"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a>在 Exchange 使用 EWS 设置另一个用户的文件夹权限

了解如何使用 EWS 的 EWS 托管 API 在 Exchange 文件夹上设置权限级别。
  
文件夹级权限允许用户访问另一个用户的邮箱中的一个或多个文件夹。 文件夹权限类似委派访问权限，但它们按以下方式有所区别： 
  
- 文件夹权限不启用用户"代表发送"或"发送为"另一个用户。 它们仅允许访问文件夹。 用户可以在这些文件夹中，创建项目，但他们不能向他们发送。
    
- 您可以设置邮箱中的任何文件夹文件夹权限，但仅可以将代理添加到的日历、 联系人、 收件箱、 日记、 备注和任务文件夹。
    
- 您可以设置多个[特定文件夹的权限](#bk_folderperms)。 在添加代理时，您可以指定一个仅[五个权限级别](delegate-access-and-ews-in-exchange.md#bk_delegateperms)。
    
- 您可以设置文件夹权限匿名和默认用户。 您只能授予给已启用邮件的帐户的代理访问。
    
如果您熟悉访问控制项 (Ace) 和随机访问控制列表 (Dacl)，您就会知道用户只能有一个每个文件夹的权限集。 如果您尝试添加一组权限的用户，他们已有一组权限，您将收到错误。 当添加、 删除或更新的文件夹的权限时，您获取的当前 DACL、 添加或删除任何 Ace，，然后发送更新的 DACL。 不能添加多个相同的用户的 Ace。 使用 EWS 托管 API 更新权限时，您需要删除的用户的当前 ACE，然后将其新的 ACE 添加到集合。 如果您正在使用 EWS，您只需替换 Ace 前一组新的。
  
如果您发出多个权限更改一个文件夹，您可以批量添加、 删除或更新 — 仅请注意，您不能批处理用户更新多个文件夹。 在单个文件夹，获取权限所需的一个呼叫和第二个呼叫需要更新该文件夹的权限。 当添加、 删除或更新用户权限时，您可以使用相同的两种方法调用或为每项任务的操作。
  
**表 1。EWS 托管 API 方法和 EWS 操作设置文件夹权限**

|如果您希望...|使用此 EWS 托管 API 方法...|使用此 EWS 操作...|
|:-----|:-----|:-----|
|启用、 删除或更新文件夹权限  <br/> |[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)跟[Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> |[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)跟[UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|创建一个文件夹，并定义文件夹权限  <br/> |[Folder.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a>文件夹权限
<a name="bk_folderperms"> </a>

当谈到在特定文件夹上设置文件夹权限，您有很多的选项。 您可以在文件夹权限级别设置为每个用户，将一组预定义的单个权限添加到 DACL，也可以在文件夹设置单个权限，但不能混合和匹配。
  
可用单个权限如下：
  
- 可以创建
- 可以创建子文件夹    
- 为文件夹所有者    
- 是可见的文件夹    
- 是文件夹联系人    
- 编辑项目    
- 删除项目    
- 读取项目
    
此外，下列权限级别提供了，其定义子集单个权限和值，如表 2 中所示：
  
- 无    
- Owner    
- PublishingEditor    
- Editor    
- PublishingAuthor    
- 作者    
- NoneditingAuthor    
- Reviewer    
- 参与者   
- 自定义-无法由应用程序设置此值。 如果应用程序包括自定义集合的单个权限，则服务器将设置此值。    
- FreeBusyTimeOnly-这可以仅在上设置日历文件夹。   
- FreeBusyTimeAndSubjectAndLocation-这可以仅在上设置日历文件夹。
    
下表显示的单个权限所应用的默认基于权限级别。
  
**表 2。由权限级别的单个权限**

|权限级别|可以创建项目|可以创建子文件夹|为文件夹所有者|是可见的文件夹|是文件夹联系人|编辑项目|删除项目|可以阅读项目|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|无  <br/> |False  <br/> |False  <br/> |False  <br/> |False  <br/> |False  <br/> |无  <br/> |无  <br/> |无  <br/> |
|Owner  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |所有  <br/> |所有  <br/> |FullDetails  <br/> |
|PublishingEditor  <br/> |True  <br/> |True  <br/> |False  <br/> |True  <br/> |False  <br/> |所有  <br/> |所有  <br/> |FullDetails  <br/> |
|Editor  <br/> |True  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |所有  <br/> |所有  <br/> |FullDetails  <br/> |
|PublishingAuthor  <br/> |True  <br/> |True  <br/> |False  <br/> |True  <br/> |False  <br/> |拥有  <br/> |拥有  <br/> |FullDetails  <br/> |
|作者  <br/> |True  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |拥有  <br/> |拥有  <br/> |FullDetails  <br/> |
|NoneditingAuthor  <br/> |True  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |无  <br/> |拥有  <br/> |FullDetails  <br/> |
|Reviewer  <br/> |False  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |无  <br/> |无  <br/> |FullDetails  <br/> |
|参与者  <br/> |True  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |无  <br/> |无  <br/> |无  <br/> |
   
如果文件夹级权限请求中指定非自定义权限级别，您无需指定单个权限设置。 如果您指定单个权限设置的权限级别时，将在响应中返回**ErrorInvalidPermissionSettings**错误。 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 中添加文件夹权限
<a name="bk_enableewsma"> </a>

下面的代码示例演示如何使用 EWS 托管 API 为： 
  
- 创建新的[FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx)对象的新用户。 
    
- 通过使用[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法获取当前文件夹的权限。 
    
- 将新**FolderPermissions**添加到[Folder.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx)属性。 
    
- 调用[Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)方法以保存到服务器的新权限。 
    
此示例假定该**服务**的邮箱所有者是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和用户已经过身份验证到 Exchange 服务器。 
  
```cs
static void EnableFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.Permissions);
    // Specify the SMTP address of the new user and the folder permissions level.
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
    
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, WellKnownFolderName.SentItems, propSet);
 
    // Add the permissions for the new user to the Sent Items DACL.
    sentItemsFolder.Permissions.Add(fldperm);
    // This call results in a UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

下面的代码行指定的权限级别。
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

如果您想要使用自定义权限级别，请改为使用此代码。
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

使用自定义权限级别创建**FolderPermission**对象时，可以设置任何或所有可写[FolderPermission 属性](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx)。 但请注意， [FolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx)从不显式设置为**自定义**应用程序。 **FolderPermissionLevel**设置为自定义中，仅当您创建**FolderPermission**对象并设置单个权限。 
  
## <a name="adding-folder-permissions-by-using-ews"></a>使用 EWS 添加文件夹权限
<a name="bk_enableews"> </a>

下面的 EWS 代码示例演示如何通过检索当前权限，然后提交新的权限的列表添加到特定文件夹的权限。
  
第一步是发送[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)请求，其中[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)值指定要在其中添加权限 （在此示例中的已发送邮件文件夹） 的文件夹和[FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)值包含文件夹： PermissionSet。 此请求将检索指定的文件夹的权限设置。 
  
这也是 EWS 托管 API 将调用**绑定**到[添加文件夹权限](#bk_enableewsma)方法时发送的 XML 请求。
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:GetFolder>
        <m:FolderShape>
          <t:BaseShape>IdOnly</t:BaseShape>
          <t:AdditionalProperties>
            <t:FieldURI FieldURI="folder:PermissionSet" />
          </t:AdditionalProperties>
        </m:FolderShape>
        <m:FolderIds>
          <t:DistinguishedFolderId Id="sentitems" />
        </m:FolderIds>
      </m:GetFolder>
    </soap:Body>
  </soap:Envelope>
```

服务器响应包含**NoError**，这表明该文件夹已成功检索[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的[GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)消息的**GetFolder**请求。 为便于阅读变短了[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)和[ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx)值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="CgAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

接下来，使用**UpdateFolder**操作发送更新的[PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)，其中包括新的用户[权限](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx)。 请注意[UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)操作中包括各自的文件夹的[SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx)元素将覆盖所有文件夹的权限设置。 同样，包括**UpdateFolder**操作的[DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx)选项也将删除所有文件夹的权限设置。 
  
这也是在调用**Update**方法中添加[文件夹权限](#bk_enableewsma)时，将发送 EWS 托管 API 的 XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="CgAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
                      </t:UserId>
                      <t:PermissionLevel>Editor</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

下面的代码行指定的权限级别。
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

如果您想要使用自定义权限级别，请改为使用此代码。
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress> sadie@contoso.com </t:PrimarySmtpAddress>
    </t:UserId>
    <t:CanCreateItems>true</t:CanCreateItems>
    <t:CanCreateSubFolders>true</t:CanCreateSubFolders>
    <t:IsFolderOwner>false</t:IsFolderOwner>
    <t:IsFolderVisible>false</t:IsFolderVisible>
    <t:IsFolderContact>false</t:IsFolderContact>
    <t:EditItems>None</t:EditItems>
    <t:DeleteItems>None</t:DeleteItems>
    <t:ReadItems>None</t:ReadItems>
    <t:PermissionLevel>Custom</t:PermissionLevel>
</t:Permission>
```

服务器响应**UpdateFolder**请求使用[UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)消息，其中包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，这表明已成功更新文件夹。
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除文件夹权限
<a name="bk_removeewsma"> </a>

下面的代码示例演示如何使用 EWS 托管 API 删除特定的文件夹，除了默认选中并且是匿名的权限，对所有用户权限：
  
1. 使用**Bind**方法获取当前文件夹的权限。 
    
2. 循环访问**权限**集合并删除单个用户的权限。 
    
3. 在调用**Update**方法保存所做的更改。 
    
此示例删除所有用户权限的文件夹。 如果您想要修改此示例删除仅为某个特定用户的权限，更改以下代码来标识显示名称的行或 SMTP 地址的用户。
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

此示例假定该**服务**的邮箱所有者是有效的[ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和用户已经过身份验证到 Exchange 服务器。 
  
```cs
static void RemoveFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.FirstClassProperties, FolderSchema.Permissions);
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, new FolderId(WellKnownFolderName.SentItems, "primary@contoso.com"), propSet);
    // Iterate through the collection of permissions and remove permissions for any 
    // user with a display name or SMTP address. This leaves the anonymous and 
    // default user permissions unchanged. 
    if (sentItemsFolder.Permissions.Count != 0)
    {
        for (int t = 0; t < sentItemsFolder.Permissions.Count; t++)
        {
            // Find any permissions associated with the specified user and remove them from the DACL
            if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
            {
                sentItemsFolder.Permissions.Remove(sentItemsFolder.Permissions[t]);
            }
        }
    }
    // This call results in an UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

## <a name="removing-folder-permissions-by-using-ews"></a>使用 EWS 删除文件夹权限
<a name="bk_removeews"> </a>

下面的 EWS 代码示例演示如何删除所有的特定的文件夹，除了默认选中并且是匿名权限的用户权限。
  
首先，将其中[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)值指定要删除的权限 （在此示例中的已发送邮件文件夹） 的文件夹和[FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)值包含文件夹： PermissionSet [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)请求发送。 此请求将检索[PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)为指定的文件夹。 
  
这也是 EWS 托管 API 将调用**绑定**到[删除文件夹权限](#bk_removeewsma)方法时发送的 XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:PermissionSet" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

服务器响应包含**NoError**，这表明该文件夹已成功检索[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值的[GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)消息的**GetFolder**请求。 为便于阅读变短了**文件夹 Id**和**ParentFolderId**元素的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="EAAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
              <t:ParentFolderId Id="CQAAAA=="
                                ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>Drafts</t:DisplayName>
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
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
                      <t:PrimarySmtpAddress>sadie@Contoso.com</t:PrimarySmtpAddress>
                      <t:DisplayName>Sadie Daniels</t:DisplayName>
                    </t:UserId>
                    <t:CanCreateItems>true</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>true</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>All</t:EditItems>
                    <t:DeleteItems>All</t:DeleteItems>
                    <t:ReadItems>FullDetails</t:ReadItems>
                    <t:PermissionLevel>Editor</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
              <t:UnreadCount>0</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

接下来，使用**UpdateFolder**操作发送更新的**PermissionSet**，其中不包含对已删除的用户的**权限**。 
  
这也是在调用**Update**方法删除[文件夹权限](#bk_removeewsma)时，将发送 EWS 托管 API 的 XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="EAAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

服务器响应**UpdateFolder**请求使用**UpdateFolderResponse**消息，其中包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，这表明已成功更新。
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 更新文件夹权限
<a name="bk_updateewsma"> </a>

您还可以通过使用 EWS 托管 API 更新文件夹特定文件夹的权限。 若要更新的权限： 
  
1. [删除文件夹权限](#bk_removeewsma)的过时的权限，但不是调用**Update**方法 （尚未）。 
    
2. [添加新的或更改用户的文件夹权限](#bk_enableewsma)。
    
3. 调用**Update**方法以保存所做的更改。 
    
如果您尝试添加两个相同的用户的权限集，您将收到带有以下描述**ServiceResponseException**错误:"指定的权限集包含重复 UserIds"。 在这种情况下，从**Permission**集合中，删除当前的权限，然后**Permission**集合中添加新的权限。 
  
## <a name="updating-folder-permissions-by-using-ews"></a>使用 EWS 更新文件夹权限
<a name="bk_updateews"> </a>

您可以使用 EWS 通过组合的删除和添加过程来更新文件夹为特定的文件夹的权限。 若要更新的权限： 
  
1. 通过使用**GetFolder**操作来检索文件夹的当前权限。 
    
2. 通过使用**UpdateFolder**操作发送更新的列表的权限。 
    
这些是相同的两个操作通过 EWS 使用到[启用](#bk_enableews)或[删除的访问](#bk_removeews)。 唯一的区别是当您收到**GetFolder**响应，它将包含一个为用户设置的**权限**。 只需将该现有**权限**元素替换为新的**权限**元素，然后再发送的新**权限**值或值的**UpdateFolder**操作。 
  
如果您尝试添加两个相同的用户的权限集，您将收到**ErrorDuplicateUserIdsSpecified** **ResponseCode**值。 在这种情况下，请求中删除过时的用户权限值，然后重试该请求。

## <a name="next-steps"></a>后续步骤

授予用户对特定文件夹的权限后，用户可以访问文件夹作为代理人。 有关详细信息，请参阅：
  
- [作为 Exchange 中使用 EWS 代理人的访问电子邮件](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [在 Exchange 中使用 EWS 作为代理人访问日历](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [作为代理人在 Exchange 使用 EWS 访问联系人](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [代理访问和 Exchange 中的 EWS](delegate-access-and-ews-in-exchange.md)   
- [添加和删除代理人，在 Exchange 使用 EWS](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    

