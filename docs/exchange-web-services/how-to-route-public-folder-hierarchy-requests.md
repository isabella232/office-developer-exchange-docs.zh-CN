---
title: 路由公用文件夹层次结构请求
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ec35df8e-4d75-4aa1-8b9c-ae1db7e05772
description: 需要了解公用文件夹层次结构（如移动、更新、删除或查找公用文件夹）的所有公用文件夹信息请求都需要路由到给定用户的默认公用文件夹层次结构邮箱。 若要将请求路由到该邮箱，您需要将 X-AnchorMailbox 和 X-PublicFolderMailbox 标头设置为自动发现服务返回的特定值。
ms.openlocfilehash: e86e1956db33b7ad8e654a22b980900b4f59dd87
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513120"
---
# <a name="route-public-folder-hierarchy-requests"></a>路由公用文件夹层次结构请求

需要了解公用文件夹层次结构（如移动、更新、删除或查找公用文件夹）的所有公用文件夹信息请求都需要路由到给定用户的默认公用文件夹层次结构邮箱。 若要将请求路由到该邮箱，您需要将 **X-AnchorMailbox** 和 **X-PublicFolderMailbox** 标头设置为自动发现服务返回的特定值。 
  
**公用文件夹概述**

|标头|我需要什么？|如何获取它？|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |[GetUserSettings](https://msdn.microsoft.com/library/office/dd877096%28v=exchg.150%29.aspx)自动发现 SOAP 响应中的 [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx)值，它将成为 **X-AnchorMailbox** 标头的值。<br/><br/> ![X-AnchorMailbox 响应](media/Ex15_PF_PFH_Anchor.png)| 1. 使用用户邮箱的 SMTP 地址发送 **GetUserSetting** 请求。<br/><br/>2. 缓存自动发现服务返回 **的 PublicFolderInformation** 元素的值。 它可以是代码中现有自动发现调用的缓存，或者是新的 [EWS 托管 API GetUserSettings](#bk_getpfinfoewsma) 调用或 [GetUserSettings SOAP 请求](#bk_getpfinfoews)。  <br/><br/>3. 使用 **PublicFolderInformation** 元素填充 **X-AnchorMailbox 标头** 的值。 **PublicFolderInformation 元素** 的值为 SMTP 地址。  <br/> |
|**X-PublicFolderMailbox** <br/> |[POX](https://msdn.microsoft.com/library/bb204082%28v=exchg.150%29.aspx)[自动发现](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx)响应中的 Server 值，它将成为 **X-PublicFolderMailbox 标头** 的值。<br/><br/> ![X-PublicFolderMailbox 响应](media/Ex15_PF_PFH_PFMailbox.png)|1. 使用 **X-AnchorMailbox** 电子邮件地址调用 [POX](#bk_makeautodrequest)自动发现服务。  <br/><br/>2. 使用 **自动** 发现服务返回的 Server 元素填充 **X-PublicFolderMailbox 标头** 的值。 **X-PublicFolderMailbox** 的值是用户名是 GUID 的 SMTP 地址。  <br/> |

<br/>

确定邮件头值后，在提出公用文件夹层次结构请求 [时，请包含这些值](#bk_setheadervalues)。
  
本文中的步骤特定于公用文件夹层次结构请求。 若要确定请求是公用文件夹层次结构还是内容请求，请参阅传送 [公用文件夹请求](public-folder-access-with-ews-in-exchange.md#bk_routing)。
  
## <a name="determine-the-value-of-the-x-anchormailbox-header-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 确定 X-AnchorMailbox 标头的值
<a name="bk_getpfinfoewsma"> </a>

若要使用 EWS 托管 API 检索 [PublicFolderInformation (POX)](https://msdn.microsoft.com/library/a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6%28Office.15%29.aspx) 值，可以缓存现有自动发现服务调用返回的 **PublicFolderInformation** 元素的值，也可以进行新调用。 
  
如果要进行新调用，可以使用 [EWS](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)托管 API 获取用户设置，方法是使用 [EWS](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)托管 API 获取代码的用户设置，然后使用下面的代码调用 **GetUserSettings** 示例方法，该代码仅检索 **PublicFolderInformation** 元素的值。 将邮箱用户的 SMTP 地址作为输入参数包含。 
  
```cs
GetUserSettingsResponse userResponse = GetUserSettings(adservice, "sonyaf@contoso.com", 3, UserSettingName.PublicFolderInformation);
Console.WriteLine("X-AnchorMailbox value for public folder hierarchy requests: {0}", userResponse.Settings[UserSettingName.PublicFolderInformation]);
```

运行代码后，控制台上将显示以下信息：
  
`X-AnchorMailbox for public folder hierarchy requests: SharedPublicFolder@contoso.com`

现在您具有 **PublicFolderInformation** 值，请包含该值作为所有公用文件夹层次结构请求中 X-AnchorMailbox 标头的值。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="determine-the-value-of-the-x-anchormailbox-header-using-soap"></a>使用 SOAP 确定 X-AnchorMailbox 标头的值
<a name="bk_getpfinfoews"> </a>

以下代码示例演示如何使用 [GetUserSettings](https://msdn.microsoft.com/library/dd877096%28v=exchg.150%29.aspx) SOAP 操作检索 **PublicFolderInformation** 值。 邮箱用户是在 [Mailbox](https://msdn.microsoft.com/library/dd877076%28v=exchg.150%29.aspx) 元素中指定的 [，RequestedSettings](https://msdn.microsoft.com/library/office/dd877107%28v=exchg.150%29.aspx) 元素将响应限制为 [PublicFolderInformation](https://msdn.microsoft.com/library/dn751006%28v=exchg.150%29.aspx) 值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:a="http://schemas.microsoft.com/exchange/2010/Autodiscover"
               xmlns:wsa="http://www.w3.org/2005/08/addressing"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <a:RequestedServerVersion>Exchange2007_SP1</a:RequestedServerVersion>
    <wsa:Action>https://schemas.microsoft.com/exchange/2010/Autodiscover/Autodiscover/GetUserSettings</wsa:Action>
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

该响应包括 **PublicFolderInformation** 值。 
  
```XML
<UserSetting i:type="StringSetting">
    <Name>PublicFolderInformation</Name>
    <Value>SharedPublicFolder@contoso.com</Value>
</UserSetting>
```

现在您具有 **PublicFolderInformation** 值，请包含该值作为所有公用文件夹层次结构请求中 X-AnchorMailbox 标头的值。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com`

## <a name="make-an-autodiscover-request-to-determine-the-x-publicfolderinformation-value"></a>创建自动发现请求以确定 X-PublicFolderInformation 值
<a name="bk_makeautodrequest"> </a>

使用 **PublicFolderInformation** SMTP 地址（现在用作 **X-AnchorMailbox** 值）进行自动发现请求。 使用[Exchange 2013：](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e)使用自动发现代码获取用户设置示例调用自动发现服务，因为它简化了自动发现过程。 此代码示例使用下表中列出的命令行参数调用 **PublicFolderInformation** SMTP 地址上的 POX 自动发现服务。 
  
|**命令行参数**|**说明**|
|:-----|:-----|
|emailAddress  <br/> |**PublicFolderInformation** SMTP 地址。  <br/> |
|-skipSOAP  <br/> | 对此方案使用 POX 自动发现请求。  <br/> |
|-auth authEmailAddress  <br/> |邮箱用户的电子邮件地址，用于身份验证。 运行示例时，系统将提示您输入邮箱用户的密码。  <br/> |
   
例如，SharedPublicFolder@contoso.com **是 PublicFolderInformation** 元素的 SMTP 地址，而 sonyaf@contoso.com 是邮箱用户时，命令行参数应如下所示。 
  
`SharedPublicFolder@contoso.com -skipSOAP -auth sonyaf@contoso.com`

运行 **"Exchange 2013： 使用** 自动发现获取用户设置"示例时，最后一个自动发现响应应该成功，并包含与邮箱 GUID 关联的所有用户设置。 与 [EXCH](https://msdn.microsoft.com/library/bb204084%28v=exchg.150%29.aspx) [协议](https://msdn.microsoft.com/library/bb204278%28v=exchg.150%29.aspx)Type 元素关联的 [Server](https://msdn.microsoft.com/library/office/bb204223%28v=exchg.150%29.aspx)值是 **X-PublicFolderInformation 标头** 值。 
  
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

或者，如果不希望使用 **Exchange 2013： 使用** 自动发现获取用户设置示例，则可以通过生成自动发现终结点列表，然后向每个 URL [](how-to-generate-a-list-of-autodiscover-endpoints.md)发送以下 POX 自动发现请求，直到收到成功响应，获取 **Server** 值。 SharedPublicFolder@contoso.com 是 **X-PublicFolderMailbox 标头** 的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>SharedPublicFolder@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

有关自动发现过程详细信息，请参阅自动发现[for Exchange、Generate](autodiscover-for-exchange.md)a list [of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md)和[Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)。
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>设置 X-AnchorMailbox 和 X-PublicFolderMailbox 标头的值
<a name="bk_setheadervalues"> </a>

使用 Determine [the value of the X-AnchorMailbox header by using the EWS Managed API](#bk_getpfinfoewsma)或 Determine the value of the [X-AnchorMailbox header using SOAP](#bk_getpfinfoews) and the **Server** value acquired in Make [an Autodiscover request to determine the X-PublicFolderInformation value中获取的 PublicFolderInformation](#bk_makeautodrequest)SMTP address 的值，设置公用文件夹内容请求中 **X-AnchorMailbox** 和 **X-PublicFolderMailbox** 标头的值。 
  
例如，给定 SharedPublicFolder@contoso.com 的 **PublicFolderInformation** SMTP 地址和 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com **的 Server** 值，在调用以下方法或操作时，请包含以下标头。 
  
`X-AnchorMailbox: SharedPublicFolder@contoso.com` <br/>
`X-PublicFolderMailbox: 1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com`

**需要 X-AnchorMailbox 和 X-PublicFolder 标头的公用文件夹调用**

|**EWS 托管 API**|**EWS 操作**|
|:-----|:-----|
|[Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> [Folder.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> [MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) <br/> |
   
若要使用 EWS 托管 API 添加这些标头，请使用 [HttpHeaders.Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) 方法。 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "SharedPublicFolder@contoso.com");service.HttpHeaders.Add("X-PublicFolderMailbox", "1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com");
```

例如，以下代码显示了一个 [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) 请求，其中 **X-AnchorMailbox** 和 **X-PublicFolderMailbox** 标头设置为本文示例中检索的值。 
  
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
- [路由公用文件夹内容请求](how-to-route-public-folder-content-requests.md)    
- [使用 EWS 托管 API 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md#bk_Managed)
    

