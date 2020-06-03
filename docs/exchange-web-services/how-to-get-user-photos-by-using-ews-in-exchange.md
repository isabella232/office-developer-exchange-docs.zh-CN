---
title: 使用 Exchange 中的 EWS 获取用户照片
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: f86d1099-1f57-47dc-abf2-4d5ae4e900a9
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 获取与邮箱或联系人相关联的用户照片。
localization_priority: Priority
ms.openlocfilehash: 14f2bc6bef1ce3c3529f03e213e3ada7c45a5a71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455784"
---
# <a name="get-user-photos-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 获取用户照片

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 获取与邮箱或联系人相关联的用户照片。
  
将面孔放在某个名称上是很好的。 如果您的用户希望将名称放在面孔中，应用程序可以从 Exchange 中请求一个代表电子邮件帐户的图像（通常为照片）。 您可以获取存储在邮箱的 Exchange 服务器上的用户照片，也可以从邮箱中存储的联系人处获取联系人照片。
  
您可以使用多种不同的技术从邮箱或 Active Directory 域服务（AD DS）获取照片。 获取照片的最佳方式取决于要从中获取照片的联系人的类型。 
  
**表1。用于基于联系人类型获取用户照片的技术**

|**联系人类型**|**要使用的技术**|
|:-----|:-----|
|邮箱用户照片  <br/> |[使用 REST 获取邮箱用户照片](#bk_REST)<br/><br/> [使用 EWS 获取用户照片](#bk_EWS) <br/> |
|联系用户照片  <br/> |[使用 EWS 托管 API 获取联系人用户照片](#bk_EWSMA)<br/><br/> [使用 EWS 获取用户照片](#bk_EWS) <br/> |

<a name="bk_REST"> </a>

## <a name="get-a-mailbox-user-photo-by-using-rest"></a>使用 REST 获取邮箱用户照片

您可以使用标准的 HTTPS **GET**请求从 Exchange 服务器请求用户照片。 在请求中，指定电子邮件帐户地址和图像的大小代码，如下面的示例所示。 
  
```HTML
https://Exchange Server/ews/Exchange.asmx/s/GetUserPhoto?email=email address&amp;size=size code
```

使用自动发现服务[GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)操作检索**ExternalEwsUrl**设置，该设置包含 EXCHANGE Web 服务（EWS）终结点的 URL 和返回用户照片的**exchange**的 HTTP 处理程序的位置。 
  
每个大小代码指示的图像的高度和宽度（以像素为单位）。 例如，大小代码**HR48x48**返回一个高度为48像素、宽48像素的图像。 Size 代码参数的可能值与[SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)元素的可能值相同。 如果请求指定的大小不可用，则将返回最大可用照片。 如果 Exchange 服务器上未存储任何照片，则将返回存储在 AD DS 中的帐户的缩略图图像。 
  
> [!NOTE]
> **HR48x48**大小代码始终返回 AD DS 缩略图（如果可用）。 
  
下面的示例演示如何使用 GET 请求检索 Sadie 的用户照片并将其保存到本地计算机。
  
```cs
// Create the web request with the REST URL.
HttpWebRequest request = 
   WebRequest.Create("https://www.contoso.com/ews/exchange.asmx/s/GetUserPhoto?email=sadie@contoso.com&amp;size=HR240x240") 
   as HttpWebRequest;
// Submit the request.
using (HttpWebResponse resp = request.GetResponse() as HttpWebResponse)
{
   // Take the response and save it as an image.
   Bitmap image = new Bitmap(resp.GetResponseStream());
   image.Save("Sadie.jpg");
}

```

请求将返回 HTTP 响应。 
  
**表2。GetUserPhoto 请求的响应代码**

|**响应代码**|**说明**|
|:-----|:-----|
|200  <br/> |图像可用于指定的电子邮件帐户，而二进制图像包含在响应中。  <br/> |
|304  <br/> |自上次将**ETag**返回到应用程序后，图像尚未更改。  <br/> |
|404  <br/> |没有可用于指定的电子邮件帐户的图像。  <br/> |

<a name="bk_REST"> </a>

## <a name="cache-user-photos"></a>缓存用户照片

Exchange 将返回内容类型为 image/jpeg 的数据以及标头值的集合。 **ETag**标头类似于更改键。 值是一个字符串，表示上次更新照片的时间。 在照片发生更改之前，该**ETag**对用户照片保持不变。 可以在 "**如果-无匹配**" 标头中将此**ETag**值发送到 HTTPS **GET**请求中的服务器。 如果自上次请求以来，该照片尚未更改，则服务器将使用 HTTP 304 响应进行响应，以指示这样。 这意味着您可以使用以前请求和保存的用户照片，而不是处理新照片。 

<a name="bk_EWSMA"> </a>

## <a name="get-a-contact-user-photo-by-using-ews-managed-api"></a>使用 EWS 托管 API 获取联系人用户照片

如果联系人存储在用户邮箱的联系人文件夹中，则您的应用程序可以使用 EWS 托管 API 检索联系人的照片。 若要执行此操作，首先请查找您想要使用的联系人的**ItemId** 。 然后，在绑定到该联系人后，将其加载到 "附件" 集合。 如果联系人有照片，则照片将是附件之一。 依次通过 "附件" 集合，检查**IsContactPhoto**属性的值。 当您找到联系人照片时，您可以将其保存到本地计算机，应用程序可以对其进行访问。 
  
下面的示例演示了此过程。 此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
private static void GetContactPhoto(ExchangeService service, string ItemId)
{
   // Bind to an existing contact by using the ItemId passed into this function.
   Contact contact = Contact.Bind(service, ItemId);
   // Load the contact to get access to the collection of attachments.
   contact.Load(new PropertySet(ContactSchema.Attachments));
   // Loop through the attachments looking for a contact photo.
   foreach (Attachment attachment in contact.Attachments)
   {
      if ((attachment as FileAttachment).IsContactPhoto)
      {
         // Load the attachment to access the content.
         attachment.Load();
      }
   }
   FileAttachment photo = contact.GetContactPictureAttachment();
   // Create a file stream and save the contact photo to your computer.
   using (FileStream file = new FileStream(photo.Name, FileMode.Create, System.IO.FileAccess.Write))
   {
      photo.Load(file);
   }
}

```

<a name="bk_EWS"> </a>

## <a name="get-a-user-photo-by-using-ews"></a>使用 EWS 获取用户照片

如果从 AD DS 获取用户照片，则可以使用[GetUserPhoto](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)操作（如果您知道电子邮件地址）或[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作（如果您不知道电子邮件地址）。 如果要从邮箱的 "联系人" 文件夹中获取用户照片，请使用[GetItem](https://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx)操作，后跟[GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)操作。 在这两种情况下，照片在 XML 响应中作为 Base64 编码的字符串返回。 
  
### <a name="get-a-mailbox-user-photo-by-using-the-getuserphoto-operation"></a>使用 GetUserPhoto 操作获取邮箱用户照片

使用**GetUserPhoto**操作非常简单。 在 XML 请求中，指定用户的电子邮件地址和要返回的[照片的大小](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)（在[SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)元素中）。 下面的 XML 请求示例演示如何获取 Sadie Daniels 的照片，该照片的宽度为360像素，高为360像素。 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013 "/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>sadie@contoso.com</m:Email>
         <m:SizeRequested>HR360x360</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>

```

下面是 XML 响应。 Base64 编码的照片包含在[PictureData](https://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx)元素中（内容已缩短以提高可读性）。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetUserPhotoResponse ResponseClass="Success" 
         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <HasChanged>true</HasChanged>
      <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg... wATRRRSuB//2Q==</PictureData>
    </GetUserPhotoResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-mailbox-user-photo-by-using-the-resolvenames-operation"></a>使用 ResolveNames 操作获取邮箱用户照片

如果您不知道要获取其照片的用户的电子邮件地址，则可以[使用 ResolveNames 操作](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)获取可能的匹配项的候选人。 如果为[ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx)元素的**ContactDataShape**属性指定 "AllProperties"，则会为每个候选人返回大量数据（包括用户照片）。 下面的示例演示对解析名称 "Sadie" 的 XML 请求，并返回每个候选项的所有属性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
<soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>  
<soap:Body>
  <m:ResolveNames ReturnFullContactData="true" ContactDataShape="AllProperties">
      <m:UnresolvedEntry>sadie</m:UnresolvedEntry>
    </m:ResolveNames>
  </soap:Body>
</soap:Envelope>
```

响应中将返回大量数据。 以下示例仅显示与用户照片相关的数据。 **Photo**元素包含 Base64 编码的用户照片（内容已缩短以提高可读性）。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:GivenName>Sadie</t:GivenName>
                <t:Initials/>
                <t:CompanyName>CONTOSO</t:CompanyName>
......
                <t:Photo>/9j/4AAQSkZJRgABAQE...qKKKAP/2Q==</t:Photo>
......
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </m:ResolveNamesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-contact-user-photo-by-using-the-getattachment-operation"></a>使用 GetAttachment 操作获取联系人用户照片

您可以使用 EWS 获取存储在邮箱中的联系人的照片。 首先，使用**GetItem**操作返回所有属性，以便您可以查找照片。 下面的示例展示了获取联系人项目的 XML 请求。 为了提高可读性，项目 ID 已缩短。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAAGECXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AABLzXRv"/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>

```

查找 " [HasPicture](https://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx) " 元素以验证联系人是否有关联的照片。 然后，查看[IsContactPhoto](https://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx)元素的值为 true 的附件的集合。 以下响应示例仅显示相关数据。 为了提高可读性，可缩短 ID 值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAAGECXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AABLzXRv"/>
              <t:ParentFolderId Id="nIxIAAA=" ChangeKey="AQAAAA=="/>
              <t:ItemClass>IPM.Contact</t:ItemClass>
              <t:Subject>Hope Gross</t:Subject>
              <t:Sensitivity>Normal</t:Sensitivity>
......
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="1LGlhgpgoA="/>
                  <t:Name>ContactPicture.jpg</t:Name>
                  <t:Size>6260</t:Size>
                  <t:LastModifiedTime>2011-03-09T16:55:55</t:LastModifiedTime>
                  <t:IsInline>false</t:IsInline>
                  <t:IsContactPhoto>true</t:IsContactPhoto>
                </t:FileAttachment>
              </t:Attachments>
......
              <t:HasPicture>true</t:HasPicture>
            </t:Contact>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>

```

接下来，将**GetAttachment**操作与**AttachmentId**结合使用，以请求具有联系人照片的附件。 下面的示例展示了获取附件的 XML 请求。 为了提高可读性，将缩短 ID。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
         <t:AttachmentId Id="1LGlhgpgoA="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>

```

下面的示例显示包含有关您请求的附件的信息的 XML 响应。 [Content](https://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx)元素包含用户照片的 Base64 编码字符串，在此示例中缩短了可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="+KsDBEr1LGlhgpgoA="/>
              <t:Name>ContactPicture.jpg</t:Name>
              <t:Content>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg...D//2Q==</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:GetAttachmentResponse>
  </s:Body>
</s:Envelope>

```

<a name="bk_EWS"> </a>

## <a name="decode-a-base64-encoded-string"></a>对 Base64 编码的字符串进行解码

无论您用于获取用户照片的操作如何，您都需要对该字符串进行解码，以便您可以在应用程序中使用它。 下面的示例演示如何对字符串进行解码，然后将其保存到本地计算机，以便应用程序稍后对其进行访问。
  
```cs
// Convert the encoded string into a byte array.
byte[] data = System.Convert.FromBase64String(Photo);
// Create a memory stream to read the data.
MemoryStream ms = new MemoryStream(data);
// Save the data on your local computer as a JPG image.
using (FileStream file = new FileStream(ContactName + ".jpg", FileMode.Create, System.IO.FileAccess.Write))
{
   byte[] bytes = new byte[ms.Length];
   ms.Read(bytes, 0, (int)ms.Length);
   file.Write(bytes, 0, bytes.Length);
   ms.Close();
}

```

## <a name="see-also"></a>另请参阅

- [人员和 Exchange 中的 EWS 中的联系人](people-and-contacts-in-ews-in-exchange.md)    
- [使用 Exchange 2013 中的 EWS 解析不明确的名称](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)    
- [使用 Exchange 中的 EWS 在批处理中处理联系人](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    

