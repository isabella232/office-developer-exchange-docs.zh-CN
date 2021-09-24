---
title: 路由公用文件夹内容请求
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: 需要将涉及公用文件夹内容的公用文件夹信息的所有请求路由到包含目标文件夹内容的公用文件夹邮箱。 若要将请求路由到该邮箱，您需要将 X-AnchorMailbox 和 X-PublicFolderMailbox 标头设置为特定值。
ms.openlocfilehash: d5a066a63d9bc3b48c41473545343125538d856b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521100"
---
# <a name="route-public-folder-content-requests"></a>路由公用文件夹内容请求

需要将涉及公用文件夹内容的公用文件夹信息的所有请求路由到包含目标文件夹内容的公用文件夹邮箱。 若要将请求路由到该邮箱，您需要将 **X-AnchorMailbox** 和 **X-PublicFolderMailbox** 标头设置为特定值。 
  
下表概述了此过程：
  
**公用文件夹概述**

|标头|我需要什么？|如何获取它？|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |1. 公用文件夹层次结构邮箱的 [X-AnchorMailbox 和 X-PublicFolderInformation ](how-to-route-public-folder-hierarchy-requests.md) 值。<br/><br/>2. 包含邮箱内容的公用文件夹邮箱的 GUID，将发送到自动发现服务。<br/><br/>  自动 **发现响应中的 AutoDiscoverSMTPAddress** 将成为 **X-AnchorMailbox** 标头的值。  <br/> ![TODO](media/Ex15_PF_PFContent.png)| 1. 使用本文中的代码示例，它 [实现 EWS 托管 API](#bk_determineguidewsma)。 或使用 [EWS](#bk_determineguidews) 并转换结果以获取 GUID。<br/><br/>[2. 使用](#bk_makeautodrequest)GUID 和域名进行自动发现请求。<br/><br/>3. 使用自动发现响应中返回的 **AutoDiscoverSMTPAddress** 元素的值填充标头 [的值](#bk_setheadervalues)。  <br/> |
|**X-PublicFolderMailbox** <br/> |你的工作已完成，X-PublicFolderMailbox 值与 X-AnchorMailbox 值相同！  <br/> |你已拥有它！  <br/> |
   
确定邮件头值后，当您进行公用文件夹内容请求 [时，请包含这些值](#bk_setheadervalues)。
  
本文中的步骤特定于公用文件夹内容请求。 若要确定请求是公用文件夹层次结构还是内容请求，请参阅传送 [公用文件夹请求](public-folder-access-with-ews-in-exchange.md#bk_routing)。

<a name="bk_determineguidewsma"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 确定公用文件夹邮箱的 GUID


若要确定公用文件夹内容邮箱的 GUID，请使用以下代码示例，它执行下列操作： 
  
- 使用通过路由公用文件夹层次结构请求检索到的 **X-AnchorMailbox** 和 **X-PublicFolderInformation** [标头](how-to-route-public-folder-hierarchy-requests.md)。
    
- 调用 EWS 托管 API [FindFolders](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)方法，并包含对 PR_REPLICA_LIST (0x66980102) 属性的请求 
    
the **PR_REPLICA_LIST** value identifies the mailbox GUID of the public folder mailbox that has the content for the folder. the **PR_REPLICA_LIST** property is a byte array， but is cast as a GUID for this scenario. 连接 GUID 和域名以形成要调用自动发现的地址。 
  
此示例假定是邮箱用户的 ExchangeService 对象，是 `service` [](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) `PFHAnchorHeader` `PFHMailboxHeader` **X-AnchorMailbox** 和 **X-PublicFolderMailbox** 标头的值，domain 是租户使用的域名。 
  
```cs
public static string GetMailboxGuidAddress(ExchangeService service, String PFHAnchorHeader, String PFHMailboxHeader, String domain)
{
    // Create a new folder view, and pass in the maximum number of folders to return.
    FolderView view = new FolderView(10);
    // Create an extended property definition for the PR_REPLICA_LIST property.
    ExtendedPropertyDefinition PR_REPLICA_LIST = new ExtendedPropertyDefinition(0x6698, MapiPropertyType.Binary);
    // As a best practice, limit the properties returned to only those required.
    // In this case, return the folder ID, the folder display name, and 
    // the value of the PR_REPLICA_LIST extended property definition.
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, PR_REPLICA_LIST);
    service.HttpHeaders.Add("X-AnchorMailbox", PFHAnchorHeader);
    service.HttpHeaders.Add("X-PublicFolderMailbox", PFHMailboxHeader);
    // Add a call to the CertificateValidationCallback method here if needed.
    // ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;
    // Call FindFolders to retrieve the folder hierarchy, starting with the PublicFolderRoot folder.
    // This method call results in a FindFolder call to EWS.
    FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.PublicFoldersRoot, view);
    string GuidAsString = null;
    List<string> Guids = new List<string>();
    // For each folder under the root, display the name, and copy the value of the 
    // PR_REPLICA_LIST byte array to a string value. 
    foreach (Folder folder in findResults.Folders)
    {
        Console.WriteLine("Public folder display name: {0}", folder.DisplayName);
        byte[] ByteArr = (byte[])folder.ExtendedProperties[0].Value;
        GuidAsString = System.Text.Encoding.ASCII.GetString(ByteArr, 0, 36);
        Guids.Add(GuidAsString);
        Console.WriteLine("Address for Autodiscover: {0}.{1}\r\n", GuidAsString, domain);
    }
    // Concatenate the GUID value of the PR_REPLICA_LIST with the domain name to generate the 
    // SMTP address to use for the AutoDiscover request for the public folder content mailbox.
    string AutoDSMTPAddress = GuidAsString + "@" + domain;
    // Check that all folders have the same GUID value. If they do not, use the GUID value of the
    // folder that you're requesting content for.
    string commonGuid = CompareGuidsForEquality(Guids);
    if (commonGuid == "Not Equal")
    {
        Console.WriteLine("The GUIDs for all the folders in the hierarchy are not the same. Run the Autodiscover sample using the address returned above that is associated with the folder in your hierarchy request.", AutoDSMTPAddress);
        return null;
    }
    else
    {
        Console.WriteLine("The GUIDs for all public folders in the hierarchy are the same. Run the Autodiscover sample using the {0} address.", AutoDSMTPAddress);
        return AutoDSMTPAddress;
    }
}
// Method to compare the GUID for each folder under the public folder root.
// If each GUID is the same, return the GUID.
// If the GUIDs are not the same, return "Not equal".
public static string CompareGuidsForEquality(List<string> list)
{
    string NotEqual = "Not equal";
    string first = list.First();
    return list.All(x => x == first) ? first : NotEqual;
}
```

如果您收到错误"请求失败。 基础连接已关闭：无法为 SSL/TLS 安全通道建立信任关系"，您需要添加对验证 [回调方法的调用](how-to-validate-a-server-certificate-for-the-ews-managed-api.md)。 该方法的占位符和注释包含在代码示例中。
  
如果公用文件夹根目录下的所有公用文件夹的邮箱 GUID 都相同，该示例将指示在控制台输出中调用 [自动](#bk_makeautodrequest) 发现时要用作返回值的地址。 如果公用文件夹根目录下的所有公用文件夹的邮箱 GUID 不相同，则需要对与内容[](#bk_makeautodrequest)请求中的文件夹关联的地址进行自动发现请求。 

<a name="bk_determineguidews"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a>使用 EWS 确定公用文件夹邮箱的 GUID

下面的代码示例演示如何使用 EWS [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)操作检索 PR_REPLICA_LIST (0x66980102) 属性的值。  对于 [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx)元素 **，PropertyTag** 属性设置为 PR_REPLICA_LIST 属性的十进制值 (26264  **) ，PropertyType** 属性设置为 **Binary**。
  
这也是当您使用 **FindFolders** 方法通过使用 EWS 托管 API 确定公用文件夹邮箱 [的 GUID 时，EWS 托管 API](#bk_determineguidewsma)发送的 XML 请求。
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0913.015
Accept-Encoding: gzip,deflate
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Cookie: ClientId=KZPBLKA9ZMPXAQDW
Content-Length: 1005
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="26264" PropertyType="Binary" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

服务器使用 [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx)消息响应 **FindFolder** 请求，其中包含 **PR_REPLICA_LIST属性的值。** 请注意，该属性的值在 EWS 响应中显示为 base-64 编码字节数组的字符串格式。 为可读性，缩短了响应中的某些标头值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="1019" MinorBuildNumber="15" Version="V2_17" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body>
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="2" TotalItemsInView="2" IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="AAEuAAAAAADL8shaNEKnQYVvRbpoY9vDAQBGDloItRzyTrAt+XVzRr/YAABdofPkAAA=" ChangeKey="AwAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/2h"/>
                <t:DisplayName>My Public Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAxEAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/W/"/>
                <t:DisplayName>SampleFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

为了使用 XML 中返回的 **PR_REPLICA_LIST** 值，MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA=，若要确定邮箱 GUID，该值必须转换为 GUID 的格式，格式类似于 [在 EWS 托管 API](#bk_determineguidewsma)代码示例中转换值的方式。 然后，将 GUID 与域名连接以创建 SMTP 地址，该地址包含在自动 [发现请求 中](#bk_makeautodrequest)。
  
## <a name="make-an-autodiscover-request"></a>提出自动发现请求
<a name="bk_makeautodrequest"> </a>

使用 方法返回  `GetMailboxGuidAddress` 的地址来调用自动发现。 我们建议您使用[Exchange 2013：](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e)使用自动发现代码示例获取用户设置来调用自动发现服务，因为它简化了自动发现过程。 此代码示例使用下表中列出的命令行参数调用 POX 自动发现服务以检索与邮箱 GUID 关联的 [AutoDiscoverSMTPAddress](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) 值。 

  
|**参数**|**说明**|
|:-----|:-----|
|emailAddress  <br/> |方法在 确定公用  `GetMailboxGuidAddress` 文件夹邮箱 [的 GUID 中返回的地址](#bk_determineguidewsma)。  <br/> |
|-skipSOAP  <br/> |指示需要 POX 自动发现请求。  <br/> |
|-auth authEmailAddress  <br/> |邮箱用户的电子邮件地址，用于身份验证。 运行示例时，系统将提示您输入邮箱用户的密码。  <br/> |
   
例如，命令行参数应如下所示：
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

其中 `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` 是 **GetMailboxGuidAddress** 方法返回的地址， `sonyaf@contoso.com` 是邮箱用户。 
  
运行 **"Exchange 2013： 使用** 自动发现获取用户设置"示例时，最后一个自动发现响应应该成功，并包含与邮箱 GUID 关联的所有用户设置。 将 **AutoDiscoverSMTPAddress** 用户设置保存在本地，因为您将在下一步中使用该设置。 
  
或者，如果不想使用 **Exchange 2013： 使用** 自动发现获取用户设置示例，可以生成自动发现终结点列表，然后向每个 URL 发送以下 POX 自动发现 [](how-to-generate-a-list-of-autodiscover-endpoints.md)请求，直到收到成功响应，从而获取 **AutoDiscoverSMTPAddress** 用户设置。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

有关自动发现过程的信息，请参阅[Autodiscover for Exchange、Generate](autodiscover-for-exchange.md)a [list of Autodiscover endpoints](how-to-generate-a-list-of-autodiscover-endpoints.md)和[Get user settings from Exchange by using Autodiscover](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)。
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>设置 X-AnchorMailbox 和 X-PublicFolderMailbox 标头的值
<a name="bk_setheadervalues"> </a>

使用在进行自动发现请求中获取的 **AutoDiscoverSMTPAddress** 的值，设置公用文件夹内容请求中的 **X-AnchorMailbox** 和 **X-PublicFolderMailbox** 标头的值。 [](#bk_makeautodrequest) 
  
例如，给定一个 AutoDiscoverSMTPAddress NewPublicFolder@contoso.com，在调用以下方法或操作时，请包含以下标头。
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

**需要 X-AncorMailbox 和 X-PublicFolder 标头的公用文件夹调用**

|**EWS 托管 API**|**EWS 操作**|
|:-----|:-----|
|[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item.Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
若要使用 EWS 托管 API 添加这些标头，请使用 [HttpHeaders.Add](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) 方法。 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

以下代码显示了一个 [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) 请求，其中 **X-AnchorMailbox** 和 **X-PublicFolderMailbox** 标头设置为本文示例中检索的值。 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
User-Agent: SoapSender1.0
X-AnchorMailbox: NewPublicFolder@contoso.com
X-PublicFolderMailbox: NewPublicFolder@contoso.com
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Content-Length: 688
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>另请参阅

- [使用 EWS 在 Exchange 公用文件夹访问。](public-folder-access-with-ews-in-exchange.md)    
- [Exchange 自动发现](autodiscover-for-exchange.md)    
- [生成自动发现终结点列表](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [使用自动发现从 Exchange 获取用户设置](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  
