---
title: 使用 EWS 设置其他用户的文件夹Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: 了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 设置文件夹的权限Exchange。
ms.openlocfilehash: 15288af0448a48c176529912604f628ae9bc2f19
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513085"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a>使用 EWS 设置其他用户的文件夹Exchange

了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 设置文件夹的权限Exchange。
  
文件夹级别的权限使用户能够访问其他用户邮箱中的一个或多个文件夹。 文件夹权限类似于委派访问权限，但它们在以下方面有所不同： 
  
- 文件夹权限不允许用户"代表"或"代理发送"其他用户。 它们仅允许访问文件夹。 用户可以在这些文件夹中创建项目，但他们无法发送它们。
    
- 您可以设置邮箱中任何文件夹的文件夹权限，但只能将代理添加到日历、联系人、收件箱、日记、便笺和任务文件夹。
    
- 您可以设置特定 [文件夹上的多个权限](#bk_folderperms)。 添加代理时，只能分配五个权限 [级别之一](delegate-access-and-ews-in-exchange.md#bk_delegateperms)。
    
- 您可以为匿名用户和默认用户设置文件夹权限。 只能向启用邮件的帐户授予委派访问权限。
    
如果您熟悉访问控制项 (ACL) 和任意访问控制列表 (DACLs) ，则你知道用户只能拥有每个文件夹的一组权限。 如果您尝试为用户添加一组权限，并且他们已有一组权限，您将看到错误消息。 在文件夹上添加、删除或更新权限时，会获取当前的 DACL，添加或删除任何 ACL，然后发送更新的 DACL。 不能为同一个用户添加多个 AES。 使用 EWS 托管 API 更新权限时，需要删除用户的当前 ACE，然后将他们新的 ACE 添加到集合中。 如果使用的是 EWS，只需将上一组 AS 替换为新 AES。
  
如果要对单个文件夹进行多个权限更改，可以批量添加、删除或更新 ，只需注意，不能对多个文件夹进行用户更新批处理。 一次调用需要获取单个文件夹的权限，第二次调用需要更新该文件夹的权限。 添加、删除或更新用户权限时，将针对每个任务使用相同的两个方法调用或操作。
  
**表 1.用于设置文件夹权限的 EWS 托管 API 方法和 EWS 操作**

|如果你想要...|使用此 EWS 托管 API 方法...|使用此 EWS 操作...|
|:-----|:-----|:-----|
|启用、删除或更新文件夹权限  <br/> |[Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) 后跟 [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> |[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) 后跟 [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|创建文件夹并定义文件夹权限  <br/> |[Folder.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a>文件夹权限
<a name="bk_folderperms"> </a>

在设置特定文件夹的文件夹权限时，你具有很多选项。 您可以为每个用户设置文件夹的权限级别，这将向 DACL 添加一组预定义的单个权限，也可以对文件夹设置单个权限，但无法混合和匹配。
  
以下各个权限可用：
  
- 可以创建
- 可以创建子文件夹    
- 是文件夹所有者    
- 文件夹是否可见    
- 是文件夹联系人    
- 编辑项目    
- 删除项目    
- 读取项目
    
此外，以下权限级别可用，可定义单个权限和值的子集，如表 2 所示：
  
- 无    
- 所有者    
- PublishingEditor    
- 编辑器    
- PublishingAuthor    
- 作者    
- NoneditingAuthor    
- Reviewer    
- 参与者   
- Custom - 应用程序无法设置此值。 如果应用程序包含单个权限的自定义集合，则服务器将设置此值。    
- FreeBusyTimeOnly - 只能在日历文件夹上设置。   
- FreeBusyTimeAndSubjectAndLocation - 只能在日历文件夹上设置。
    
下表显示了默认情况下根据权限级别应用哪些单个权限。
  
**表 2.按权限级别表示的单个权限**

|权限级别|可以创建项目|可以创建子文件夹|是文件夹所有者|文件夹是否可见|是文件夹联系人|编辑项目|删除项目|可读取项目|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|无  <br/> |错误  <br/> |错误  <br/> |错误  <br/> |错误  <br/> |错误  <br/> |无  <br/> |无  <br/> |无  <br/> |
|所有者  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |所有  <br/> |全部  <br/> |FullDetails  <br/> |
|PublishingEditor  <br/> |True  <br/> |True  <br/> |False  <br/> |True  <br/> |错误  <br/> |所有  <br/> |全部  <br/> |FullDetails  <br/> |
|编辑器  <br/> |True  <br/> |错误  <br/> |False  <br/> |True  <br/> |错误  <br/> |全部  <br/> |全部  <br/> |FullDetails  <br/> |
|PublishingAuthor  <br/> |True  <br/> |True  <br/> |False  <br/> |True  <br/> |错误  <br/> |拥有  <br/> |拥有  <br/> |FullDetails  <br/> |
|作者  <br/> |True  <br/> |错误  <br/> |False  <br/> |True  <br/> |错误  <br/> |拥有  <br/> |拥有  <br/> |FullDetails  <br/> |
|NoneditingAuthor  <br/> |True  <br/> |错误  <br/> |False  <br/> |True  <br/> |错误  <br/> |无  <br/> |拥有  <br/> |FullDetails  <br/> |
|Reviewer  <br/> |错误  <br/> |错误  <br/> |False  <br/> |True  <br/> |错误  <br/> |无  <br/> |无  <br/> |FullDetails  <br/> |
|参与者  <br/> |True  <br/> |错误  <br/> |False  <br/> |True  <br/> |错误  <br/> |无  <br/> |无  <br/> |无  <br/> |
   
如果在文件夹级权限请求中指定非自定义权限级别，则不需要指定单个权限设置。 如果在设置权限级别时指定了单个权限，响应中将返回 **ErrorInvalidPermissionSettings** 错误。 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 添加文件夹权限
<a name="bk_enableewsma"> </a>

以下代码示例演示如何使用 EWS 托管 API 执行以下操作： 
  
- 为新 [用户创建新的 FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) 对象。 
    
- 使用 Bind 方法获取文件夹[的当前权限。](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) 
    
- 将新的 **FolderPermissions** 添加到 [Folder.Permissions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) 属性。 
    
- 调用 [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) 方法以将新权限保存到服务器。 
    
本示例 **假定服务是** 邮箱所有者的有效 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户已通过身份验证Exchange服务器。 
  
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

以下代码行指定权限级别。
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

如果要使用自定义权限级别，请改为使用此代码。
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

创建具有自定义权限级别的 [FolderPermission](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) 对象时，可以设置任意或所有可写 **FolderPermission** 属性。 但是请注意 [，FolderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx)从不由应用程序显式设置为 **Custom。** 只有在 **创建 FolderPermission** 对象并设置单个权限时 **，FolderPermissionLevel** 才设置为 Custom。 
  
## <a name="adding-folder-permissions-by-using-ews"></a>使用 EWS 添加文件夹权限
<a name="bk_enableews"> </a>

以下 EWS 代码示例显示如何检索当前权限，然后提交新权限列表，以向特定文件夹添加权限。
  
第一步是发送 [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) 请求， [其中 DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) 值指定要添加权限的文件夹 (本示例中的"已发送邮件"文件夹) [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) 值包括 folder：PermissionSet。 此请求将检索指定文件夹的权限设置。 
  
这也是调用 Bind 方法以添加文件夹权限时 EWS 托管 API发送的 XML[请求](#bk_enableewsma)。
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

服务器使用 [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)消息响应 **GetFolder** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值，指示已成功检索文件夹。 [为可读性，已缩短 FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)和[ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx)值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

接下来，使用 **UpdateFolder** 操作发送更新的 [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)，其中包括 [新用户的权限](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) 。 请注意，在 [UpdateFolder](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) 操作中将相应文件夹的 [SetFolderField](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) 元素包含将覆盖文件夹上的所有权限设置。 同样，包括[UpdateFolder 操作 DeleteFolderField](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx)选项也将删除文件夹上的所有权限设置。 
  
这也是调用 **Update** 方法以添加文件夹权限时 EWS 托管 API 发送的 XML [请求](#bk_enableewsma)。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

以下代码行指定权限级别。
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

如果要使用自定义权限级别，请改为使用此代码。
  
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

服务器使用 [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)消息响应 **UpdateFolder** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值，指示已成功更新文件夹。
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除文件夹权限
<a name="bk_removeewsma"> </a>

以下代码示例演示如何使用 EWS 托管 API 删除特定文件夹上的用户权限，默认权限和匿名权限除外，方法如下：
  
1. 使用 **Bind** 方法获取文件夹的当前权限。 
    
2. 对 **Permissions** 集合进行访问并删除单个用户的权限。 
    
3. 调用 **Update** 方法来保存更改。 
    
本示例删除文件夹上的用户权限。 如果要修改此示例以仅删除特定用户的权限，请更改以下代码行以标识用户的 显示名称 或 SMTP 地址。
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

本示例 **假定服务是** 邮箱所有者的有效 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户已通过身份验证Exchange服务器。 
  
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

以下 EWS 代码示例显示如何删除特定文件夹上的用户权限，默认权限和匿名权限除外。
  
首先，发送一个 [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) 请求， [其中 DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) 值指定要从中删除权限的文件夹 (本示例中的"已发送邮件"文件夹) [FieldURI](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) 值包括 folder：PermissionSet。 此请求将检索[指定文件夹的 PermissionSet。](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) 
  
这也是调用 Bind 方法以删除文件夹权限时 EWS 托管 API发送的 XML[请求](#bk_removeewsma)。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

服务器使用 [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)消息响应 **GetFolder** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值，指示已成功检索文件夹。 为可读性，已缩短 **FolderId** 和 **ParentFolderId** 元素的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

接下来，使用 **UpdateFolder** 操作发送更新的 **PermissionSet**，其中不包括已删除用户的权限。 
  
这也是 EWS 托管 API 在调用 **Update** 方法以删除文件夹权限时 [发送的](#bk_removeewsma)XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

服务器使用 **UpdateFolderResponse** 消息响应 **UpdateFolder** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值，指示更新成功。
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 更新文件夹权限
<a name="bk_updateewsma"> </a>

您还可以使用 EWS 托管 API 更新特定文件夹的文件夹权限。 若要更新权限，请执行以下操作： 
  
1. [删除过期权限](#bk_removeewsma) 的文件夹权限，但不要调用 **Update** 方法 () 。 
    
2. [为新的或已更改的用户添加文件夹权限](#bk_enableewsma)。
    
3. 调用 **Update** 方法以保存更改。 
    
如果您尝试为同一用户添加两组权限，您将收到 **ServiceResponseException** 错误，说明如下："指定的权限集包含重复的 UserIds"。 在这种情况下，从 **Permission** 集合中删除当前权限，然后将新权限添加到 **Permission** 集合。 
  
## <a name="updating-folder-permissions-by-using-ews"></a>使用 EWS 更新文件夹权限
<a name="bk_updateews"> </a>

您还可以通过结合删除和添加过程，使用 EWS 更新特定文件夹的文件夹权限。 若要更新权限，请执行以下操作： 
  
1. 使用 **GetFolder** 操作检索文件夹的当前权限。 
    
2. 使用 **UpdateFolder** 操作发送更新后的权限列表。 
    
这些操作与使用 EWS [启用](#bk_enableews) 或删除 [访问](#bk_removeews) 使用的两个操作相同。 唯一的区别是，当您收到 **GetFolder** 响应时，它将包含用户 **的权限** 集。 只需将现有的 **Permission** 元素替换为新的 **Permission** 元素，然后使用新的 **Permission** 值发送 **UpdateFolder** 操作。 
  
如果您尝试为同一用户添加两组权限，您将收到 **ErrorDuplicateUserIdsSpecified** 的 **ResponseCode** 值。 在这种情况下，请从请求中删除用户过时的 Permission 值，然后重试请求。

## <a name="next-steps"></a>后续步骤

向用户授予对特定文件夹的权限后，用户可以作为代理访问该文件夹。 有关详细信息，请参阅：
  
- [使用 EWS 在电子邮件中以代理Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [在日历中通过使用 EWS 以代理Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [在代理中通过使用 EWS 访问联系人Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅

- [Exchange 中的代理访问和 EWS](delegate-access-and-ews-in-exchange.md)   
- [使用 Exchange 中的 EWS 添加和删除Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [文件夹和交换中的 EWS 中的项目](folders-and-items-in-ews-in-exchange.md)
    

