---
title: 路由公用文件夹层次结构请求
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: 需要了解公用文件夹层次结构的所有公用文件夹信息请求，如移动、更新、删除或查找公用文件夹，需要将其路由到给定用户的默认公用文件夹层次结构邮箱。 若要将请求路由到该邮箱，您需要将 X-anchormailbox 和 PublicFolderMailbox 标头设置为自动发现服务返回的特定值。
ms.openlocfilehash: 2773aa3ab29868c69d1fb088deb6c8a96dfb9ecc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455690"
---
# <a name="route-public-folder-hierarchy-requests"></a>路由公用文件夹层次结构请求

需要了解公用文件夹层次结构的所有公用文件夹信息请求，如移动、更新、删除或查找公用文件夹，需要将其路由到给定用户的默认公用文件夹层次结构邮箱。 若要将请求路由到该邮箱，您需要将**x-anchormailbox**和**PublicFolderMailbox**标头设置为自动发现服务返回的特定值。 
  
**公用文件夹概述**

|标头|我需要什么？|如何获取？|
|:-----|:-----|:-----|
|**X-X-anchormailbox** <br/> |[GetUserSettings](https://msdn.microsoft.com/library/office/dd877096%28v=exchg.150%29.aspx)自动发现 SOAP 响应中的[PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx)值，它将成为**X x-anchormailbox**标头的值。<br/><br/> ![TODO](media/Ex15_PF_PFH_Anchor.png)| 1. 向用户邮箱的 SMTP 地址发送**GetUserSetting**请求。<br/><br/>2. 缓存自动发现服务返回的**PublicFolderInformation**元素的值。 这可以是您的代码中现有的自动发现调用的缓存，也可以是新的[EWS 托管 API GetUserSettings 调用](#bk_getpfinfoewsma)或[GetUserSettings SOAP 请求](#bk_getpfinfoews)。  <br/><br/>3. 使用**PublicFolderInformation**元素填充**X x-anchormailbox**标头的值。 **PublicFolderInformation**元素的值是 SMTP 地址。  <br/> |
|**X-PublicFolderMailbox** <br/> |来自[POX 自动发现响应](https://msdn.microsoft.com/library/bb204082%28v=exchg.150%29.aspx)的[服务器](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx)值，它将成为**PublicFolderMailbox**标头的值。<br/><br/> ![TODO](media/Ex15_PF_PFH_PFMailbox.png)|1. 使用**X-x-anchormailbox**电子邮件地址[调用 POX 自动发现](#bk_makeautodrequest)服务。  <br/><br/>2. 使用自动发现服务返回的**Server**元素来填充**PublicFolderMailbox**标头的值。 **X-PublicFolderMailbox**的值是一个 SMTP 地址，其中 username 是一个 GUID。  <br/> |

<br/>

确定了标头值后，在[发出公用文件夹层次结构请求时](#bk_setheadervalues)，请将它们包括在内。
  
本文中的步骤特定于公用文件夹层次结构请求。 若要确定您的请求是否为公用文件夹层次结构或内容请求，请参阅[路由公用文件夹请求](public-folder-access-with-ews-in-exchange.md#bk_routing)。
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 确定 X-X-anchormailbox 标头的值
<a name="bk_getpfinfoewsma"> </a>

若要使用 EWS 托管 API 检索[PublicFolderInformation （POX）](https://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx)值，您可以缓存对自动发现服务的现有调用返回的**PublicFolderInformation**元素的值，或发出新的呼叫。 
  
如果要进行新的呼叫，可以使用[ews](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)托管 api 获取用户设置，方法是[使用 ews 托管 api 通过代码获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)，然后使用下面的代码调用**GetUserSettings**示例方法，该代码仅检索**PublicFolderInformation**元素的值。 将邮箱用户的 SMTP 地址包含为输入参数。 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

运行代码后，会在控制台上显示以下信息：
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

现在，您已拥有**PublicFolderInformation**值，在所有公用文件夹层次结构请求中将其作为 X-x-anchormailbox 标头的值包括在内。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a>使用 SOAP 确定 X-X-anchormailbox 标头的值
<a name="bk_getpfinfoews"> </a>

下面的代码示例演示如何使用[GetUserSettings](https://msdn.microsoft.com/library/dd877096%28v=exchg.150%29.aspx) SOAP 操作检索**PublicFolderInformation**值。 邮箱用户在[邮箱](https://msdn.microsoft.com/library/dd877076%28v=exchg.150%29.aspx)元素中指定， [RequestedSettings](https://msdn.microsoft.com/library/office/dd877107%28v=exchg.150%29.aspx)元素将响应限制为[PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx)值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://pod51042.outlook.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="https://schemas.microsoft.com/exchange/2010/Autodiscover">
      <a:Request>
        <a:Users>
          <a:User>
            <a:Mailbox>sonyaf@contoso.com</a:Mailbox>
          </a:User>
        </a:Users>
        <a:RequestedSettings>
          <a:Setting>PublicFolderInformation</a:Setting>
        </a:RequestedSettings>
      </a:Request>
    </a:GetUserSettingsRequestMessage>
  </soap:Body>
</soap:Envelope>
```

响应包括**PublicFolderInformation**值。 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

现在，您已拥有**PublicFolderInformation**值，在所有公用文件夹层次结构请求中将其作为 X-x-anchormailbox 标头的值包括在内。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a>发出自动发现请求以确定 X PublicFolderInformation 值
<a name="bk_makeautodrequest"> </a>

使用**PublicFolderInformation** SMTP 地址生成自动发现请求，该地址现在被用作**X x-anchormailbox**值。 使用[Exchange 2013：使用自动发现代码示例获取用户设置](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e)，以调用自动发现服务，因为它可简化自动发现过程。 此代码示例使用下表中列出的命令行参数调用**PublicFolderInformation** SMTP 地址上的 POX 自动发现服务。 
  
|**命令行参数**|**说明**|
|:-----|:-----|
|emailAddress  <br/> |**PublicFolderInformation** SMTP 地址。  <br/> |
|-skipSOAP  <br/> | 对此方案使用 POX 自动发现请求。  <br/> |
|-auth authEmailAddress  <br/> |邮箱用户的电子邮件地址，用于进行身份验证。 在运行此示例时，系统将提示您输入邮箱用户的密码。  <br/> |
   
例如，如果 SharedPublicFolder@contoso.com 是**PublicFolderInformation**元素的 SMTP 地址，而 sonyaf@contoso.com 是邮箱用户，则命令行参数应如下所示。 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

当您运行**Exchange 2013：使用自动发现示例获取用户设置**时，最后一个自动发现响应应成功，并包含与邮箱 GUID 关联的所有用户设置。 与 EXCH[协议](https://msdn.microsoft.com/library/bb204278%28v=exchg.150%29.aspx)[Type](https://msdn.microsoft.com/library/office/bb204223%28v=exchg.150%29.aspx)元素相关联的[服务器](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx)值为**PublicFolderInformation**标头值。 
  
```XML
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    …
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</Server>

```

或者，如果您不想使用**Exchange 2013：使用自动发现示例获取用户设置**，则可以通过[生成自动发现终结点的列表](how-to-generate-a-list-of-autodiscover-endpoints.md)来获取**服务器**值，然后向每个 URL 发送以下 POX 自动发现请求，直到您收到成功的响应。 SharedPublicFolder@contoso.com 是**X-PublicFolderMailbox**标头的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="https://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

有关自动发现过程的详细信息，请参阅[exchange 的自动发现](autodiscover-for-exchange.md)，[生成自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)，并[使用自动发现获取 Exchange 中的用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)。
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>设置 X-anchormailbox 和 PublicFolderMailbox 标头的值
<a name="bk_setheadervalues"> </a>

在使用[EWS 托管 API 确定 x x-anchormailbox 标头的值时](#bk_getpfinfoewsma)，使用**PublicFolderInformation** SMTP 地址的值，或使用[SOAP 确定 x x-anchormailbox 标头](#bk_getpfinfoews)的值，以及在[建立自动发现请求以确定 x PublicFolderInformation 值时](#bk_makeautodrequest)获取的**服务器**值，在公用文件夹内容请求中设置**x-x-anchormailbox**和**PublicFolderMailbox**标头的值。 
  
例如，假设**PublicFolderInformation** SMTP 地址为 SharedPublicFolder@contoso.com，**服务器**值为1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com，则在调用以下方法或操作时，请包含以下标头。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**需要 X-anchormailbox 和 Set-publicfolder 头的公用文件夹调用**

|**EWS 托管 API 方法**|**EWS 操作**|
|:-----|:-----|
|[FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [文件夹。删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [文件夹。更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder。 Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
若要使用 EWS 托管 API 添加这些邮件头，请使用[HttpHeaders](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx)方法。 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

例如，下面的代码显示[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)请求，其中**x-X-anchormailbox**和**x PublicFolderMailbox**标头设置为本文示例中检索到的值。 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
User-Agent: SoapSender1.0
X-AnchorMailbox: SharedPublicFolder@contoso.com
X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com
Host: outlook.office365.com
Content-Length: 1174
Expect: 100-continue
Connection: Keep-Alive
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="1" Offset="0" BasePoint="Beginning" />
      <m:Restriction>
        <t:IsEqualTo>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:FieldURIOrConstant>
            <t:Constant Value="My Public Contacts" />
          </t:FieldURIOrConstant>
        </t:IsEqualTo>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAwIAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/XB" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅

- [使用 EWS 在 Exchange 公用文件夹访问。](public-folder-access-with-ews-in-exchange.md)    
- [路由公用文件夹内容请求](how-to-route-public-folder-content-requests.md)    
- [使用 EWS 托管 API 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

