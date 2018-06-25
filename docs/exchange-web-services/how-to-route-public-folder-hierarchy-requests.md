---
title: 将公用文件夹层次结构请求路由
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: 需要知道公用文件夹层次结构，如移动、 更新、 删除或查找公用文件夹的所有公用文件夹信息请求需要路由到给定用户的默认公用文件夹层次结构邮箱。 若要将请求路由到该邮箱，您需要设置为自动发现服务返回的特定值的 X AnchorMailbox 和 X PublicFolderMailbox 标头。
ms.openlocfilehash: 983431864729edbb040a7206dae416d10bfb2b7a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752884"
---
# <a name="route-public-folder-hierarchy-requests"></a>将公用文件夹层次结构请求路由

需要知道公用文件夹层次结构，如移动、 更新、 删除或查找公用文件夹的所有公用文件夹信息请求需要路由到给定用户的默认公用文件夹层次结构邮箱。 若要将请求路由到该邮箱，您需要设置为自动发现服务返回的特定值的**X AnchorMailbox**和**X PublicFolderMailbox**标头。 
  
**公用文件夹的概述**

|标头|我需要什么？|如何获得它？|
|:-----|:-----|:-----|
|**X AnchorMailbox** <br/> |从[GetUserSettings](http://msdn.microsoft.com/en-us/library/office/dd877096%28v=exchg.150%29.aspx)自动发现 SOAP 响应， **X AnchorMailbox**头的值，则将变成[PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx)值。<br/><br/> ![TODO](media/Ex15_PF_PFH_Anchor.png)| 1.发送**GetUserSetting**请求为用户的邮箱的 SMTP 地址。<br/><br/>2.缓存**PublicFolderInformation**元素的自动发现服务返回的值。 这可以是从代码中，或新[EWS 托管 API GetUserSettings 呼叫](#bk_getpfinfoewsma)或[GetUserSettings SOAP 请求](#bk_getpfinfoews)中的现有自动发现调用缓存。  <br/><br/>3.使用**PublicFolderInformation**元素来填充**X AnchorMailbox**标头的值。 **PublicFolderInformation**元素的值是 SMTP 地址。  <br/> |
|**X PublicFolderMailbox** <br/> |从[POX 自动发现响应](http://msdn.microsoft.com/en-us/library/bb204082%28v=exchg.150%29.aspx)， **X PublicFolderMailbox**头的值，则将变成[服务器](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx)值。<br/><br/> ![TODO](media/Ex15_PF_PFH_PFMailbox.png)|1。[呼叫 POX 自动发现](#bk_makeautodrequest)服务使用的**X AnchorMailbox**电子邮件地址。  <br/><br/>2.使用自动发现服务返回的**服务器**元素来填充**X PublicFolderMailbox**标头的值。 **X PublicFolderMailbox**值为 SMTP 地址，其中 username 是一个 GUID。  <br/> |

<br/>

您已确定的标头值后，请[进行的公用文件夹层次结构请求时](#bk_setheadervalues)进行包括。
  
本文中的步骤是特定于公用文件夹层次结构请求。 若要确定您的请求是公用文件夹层次结构或内容的请求，请参阅[路由的公用文件夹请求](public-folder-access-with-ews-in-exchange.md#bk_routing)。
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a>通过使用 EWS 托管 API 来确定 X AnchorMailbox 头的值
<a name="bk_getpfinfoewsma"> </a>

若要使用 EWS 托管 API 检索[PublicFolderInformation (POX)](http://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx)值，您可以缓存返回对自动发现服务的现有调用， **PublicFolderInformation**元素的值或发起新呼叫。 
  
如果您要发起新呼叫，您可以[获取用户设置使用 EWS 托管 API](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)[获取使用 EWS 托管 API 的用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)您的代码中，然后调用**GetUserSettings**示例通过使用下面的代码检索方法仅**PublicFolderInformation**元素的值。 作为输入参数中包括邮箱用户的 SMTP 的地址。 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

运行代码后, 控制台上显示以下信息：
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

既然您已经**PublicFolderInformation**值，包括作为所有公用文件夹层次结构请求中的 X AnchorMailbox 标头的值。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a>确定使用 SOAP 的 X AnchorMailbox 标头的值
<a name="bk_getpfinfoews"> </a>

下面的代码示例演示如何使用[GetUserSettings](http://msdn.microsoft.com/en-us/library/dd877096%28v=exchg.150%29.aspx) SOAP 操作检索**PublicFolderInformation**值。 在[邮箱](http://msdn.microsoft.com/en-us/library/dd877076%28v=exchg.150%29.aspx)元素中，指定邮箱用户和[RequestedSettings](http://msdn.microsoft.com/en-us/library/office/dd877107%28v=exchg.150%29.aspx)元素限制对[PublicFolderInformation](http://msdn.microsoft.com/en-us/library/dn751006%28v=exchg.150%29.aspx)值的响应。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>http://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
    <wsa:To>https://pod51042.outlook.com/autodiscover/autodiscover.svc</wsa:To>
  </soap:Header>
  <soap:Body>
    <a:GetUserSettingsRequestMessage xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover">
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

既然您已经**PublicFolderInformation**值，包括作为所有公用文件夹层次结构请求中的 X AnchorMailbox 标头的值。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a>发出的自动发现请求，以确定 X PublicFolderInformation 值
<a name="bk_makeautodrequest"> </a>

发起的自动发现请求的**PublicFolderInformation** SMTP 地址，现在用作**X AnchorMailbox**值。 使用[Exchange 2013： 获取使用自动发现的用户设置](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e)调用自动发现服务，因为它简化的自动发现过程为您的代码示例。 此代码示例使用下表中列出的命令行参数来调用 POX 自动发现服务**PublicFolderInformation** SMTP 地址。 
  
|**命令行参数**|**说明**|
|:-----|:-----|
|emailAddress  <br/> |**PublicFolderInformation** SMTP 地址。  <br/> |
|-skipSOAP  <br/> | 对于此方案中使用 POX 自动发现请求。  <br/> |
|身份验证 authEmailAddress  <br/> |邮箱用户的电子邮件地址，用于进行身份验证。 系统将提示您输入邮箱用户的密码，当您运行示例。  <br/> |
   
例如，如果 SharedPublicFolder@contoso.com 是**PublicFolderInformation**元素中，SMTP 地址且 sonyaf@contoso.com 是邮箱用户，命令行参数应如下所示。 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

当您运行**Exchange 2013： 获取使用自动发现的用户设置**示例的最后一个自动发现响应应成功和包含邮箱的邮箱 GUID 与关联的所有用户设置。 与 EXCH[协议](http://msdn.microsoft.com/en-us/library/bb204278%28v=exchg.150%29.aspx)[类型](http://msdn.microsoft.com/en-us/library/office/bb204223%28v=exchg.150%29.aspx)元素关联的[服务器](http://msdn.microsoft.com/en-us/library/bb204084%28v=exchg.150%29.aspx)值是**X PublicFolderInformation**标头值。 
  
```XML
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/responseschema/2006">
  <Response xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a">
    …
    <Account>
      <AccountType>email</AccountType>
      <Action>settings</Action>
      <Protocol>
        <Type>EXCH</Type>
        <Server>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</Server>

```

此外，如果不想使用**Exchange 2013： 获取使用自动发现的用户设置**示例中，您可以获取**服务器**值通过[生成的自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)，然后发送以下 POX 自动发现对每个 URL 的请求直到收到成功响应。 SharedPublicFolder@contoso.com 是**X PublicFolderMailbox**标头的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

有关自动发现过程的详细信息，请参阅[exchange 自动发现](autodiscover-for-exchange.md)和[生成的自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)中，[获取使用自动发现 Exchange 中的用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)。
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>X AnchorMailbox 和 X PublicFolderMailbox 标头的值
<a name="bk_setheadervalues"> </a>

使用的值来[确定使用 EWS 托管 API 的 X AnchorMailbox 标头的值](#bk_getpfinfoewsma)或[确定使用 SOAP 的 X AnchorMailbox 标头的值](#bk_getpfinfoews)和**服务器中获得的**PublicFolderInformation** SMTP 地址**值收购中[发出的自动发现请求，以确定 X PublicFolderInformation 值](#bk_makeautodrequest)，请将公用文件夹内容请求中的**X AnchorMailbox**和**X PublicFolderMailbox**标头的值。 
  
进行以下呼叫时，例如，就给定 SharedPublicFolder@contoso.com **PublicFolderInformation** SMTP 地址和 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com**服务器**值，包括以下标头操作或方法。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**需要 X AnchorMailbox 和 X PublicFolder 标头的公用文件夹呼叫**

|**EWS 托管 API 方法**|**EWS 操作**|
|:-----|:-----|
|[Folder.FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](http://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
若要使用 EWS 托管 API 添加这些标头，请使用[HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx)方法。 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

例如，下面的代码演示[FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)请求**X AnchorMailbox**和**X PublicFolderMailbox**标头设置为在本文中的示例中检索值。 
  
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
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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
- [将公用文件夹内容请求路由](how-to-route-public-folder-content-requests.md)    
- [通过使用 EWS 托管 API 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

