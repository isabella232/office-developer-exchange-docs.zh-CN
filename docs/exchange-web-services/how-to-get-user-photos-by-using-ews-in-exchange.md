---
title: 要在 Exchange 使用 EWS 获取用户照片
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f86d1099-1f57-47dc-abf2-4d5ae4e900a9
description: 了解如何获取与邮箱关联或联系在 Exchange 使用 EWS 托管 API 或 EWS 的用户照片。
ms.openlocfilehash: f0f5cddd41fc563fb9ed38e75b505830a3992411
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752813"
---
# <a name="get-user-photos-by-using-ews-in-exchange"></a>要在 Exchange 使用 EWS 获取用户照片

了解如何获取与邮箱关联或联系在 Exchange 使用 EWS 托管 API 或 EWS 的用户照片。
  
很不错将一个脸放到一个名称。 如果用户希望将名称放到正面，您的应用程序可以请求图像，通常照片，从 Exchange 表示的电子邮件帐户。 您可以获取用户照片存储邮箱的 Exchange 服务器上或可以存储在您的邮箱中的联系人中获取联系人的照片。
  
您可以使用几个不同的技术获得邮箱或 Active Directory 域服务 (AD DS) 的照片。 若要获取照片的最佳方式取决于您希望获取从照片的联系人的类型。 
  
**表 1。技术，可用于获取基于联系人类型的用户照片**

|**联系人类型**|**若要使用的技术**|
|:-----|:-----|
|邮箱用户照片  <br/> |[获取使用 REST 的邮箱用户照片](#bk_REST)<br/><br/> [通过使用 EWS 获取用户照片](#bk_EWS) <br/> |
|联系人的用户照片  <br/> |[通过使用 EWS 托管 API 获取联系人的用户照片](#bk_EWSMA)<br/><br/> [通过使用 EWS 获取用户照片](#bk_EWS) <br/> |

<a name="bk_REST"> </a>

## <a name="get-a-mailbox-user-photo-by-using-rest"></a>获取使用 REST 的邮箱用户照片

通过使用标准的 HTTPS **GET**请求，您可以从 Exchange 服务器请求用户照片。 在请求中，指定的电子邮件帐户地址和图像，大小代码在下面的示例所示。 
  
```HTML
https://Exchange Server/ews/Exchange.asmx/s/GetUserPhoto?email=email address&amp;size=size code
```

使用自动发现服务[GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)操作可以检索**ExternalEwsUrl**设置，其中包含的 Exchange Web Services (EWS) 终结点的 URL 和返回**Exchange.asmx** HTTP 处理程序的位置用户照片。 
  
每个大小代码指示的高度和宽度以像素为单位的图像。 例如，大小代码**HR48x48**返回 48 像素高 x 48 像素宽的图像。 大小代码参数的可能值是[SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)元素的可能值相同。 如果请求指定不可用的大小，将返回的最大可用照片。 如果没有照片存储在 Exchange 服务器上，将返回存储在 AD DS 帐户的缩略图图像。 
  
> [!NOTE]
> 如果可用，则**HR48x48**大小代码将始终返回的 AD DS 缩略图图像。 
  
下面的示例演示如何使用 GET 请求 Sadie 检索用户照片，并将其保存到本地计算机。
  
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

请求将返回的 HTTP 响应。 
  
**表 2。GetUserPhoto 请求的响应代码**

|**响应代码**|**说明**|
|:-----|:-----|
|200  <br/> |图像是可用于指定电子邮件帐户，在响应中包含的二进制图像。  <br/> |
|304  <br/> |最后一次**ETag**返回到应用程序未更改的图像。  <br/> |
|404  <br/> |可用于指定电子邮件帐户没有图像。  <br/> |

<a name="bk_REST"> </a>

## <a name="cache-user-photos"></a>缓存用户照片

Exchange 返回的数据的内容类型为 image/jpeg，以及标头值的集合。 类似于更改密钥**ETag**标头。 值为一个字符串，表示的上次更新照片。 **ETag**保持不变的用户照片直到照片被更改。 您可以向 HTTPS **GET**请求中**无-If-match**标头中的服务器发送此**ETag**值。 如果自上次请求以来未更改的照片，服务器将响应 HTTP 304 响应，因为这指示。 这意味着，您可以使用您以前请求并保存的用户照片而不是一个新的处理。 

<a name="bk_EWSMA"> </a>

## <a name="get-a-contact-user-photo-by-using-ews-managed-api"></a>通过使用 EWS 托管 API 获取联系人的用户照片

应用程序可以使用 EWS 托管 API 检索联系人的照片如果联系人存储在用户的邮箱中的联系人文件夹。 若要执行此操作，首先，查找**ItemId**联系人您希望使用。 然后，您将绑定到该联系人后，则加载到的 attachments 集合。 如果联系人的照片，照片将其中一个附件。 循环访问的 attachments 集合，检查**IsContactPhoto**属性的值。 时您查找联系人的照片，可以将其保存到本地计算机，并且您的应用程序可以访问它。 
  
下面的示例演示此过程。 此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。 
  
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

## <a name="get-a-user-photo-by-using-ews"></a>通过使用 EWS 获取用户照片

如果您正在从 AD DS 获取用户照片，您可以使用[GetUserPhoto](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)操作 （如果您知道电子邮件地址） 或[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作，（如果您不知道的电子邮件地址）。 如果您正在从邮箱中的联系人文件夹中获取用户照片，使用[GetItem](http://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) operation 后, 跟[GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)操作。 在任一情况下，作为 Base64 编码的字符串，在 XML 响应中返回的照片。 
  
### <a name="get-a-mailbox-user-photo-by-using-the-getuserphoto-operation"></a>要使用 GetUserPhoto 操作获取邮箱用户照片

使用**GetUserPhoto**操作非常简单。 在 XML 请求中，指定用户，并返回 （在[SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)元素中）[的照片大小](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)的电子邮件地址。 下面的 XML 请求示例演示如何获取 Sadie Daniels 360 像素宽 x 360 像素高的照片。 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

下面是 XML 响应。 [PictureData](http://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx)元素 （内容已缩短为便于阅读） 中包含的 Base64 编码的照片。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetUserPhotoResponse ResponseClass="Success" 
         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <HasChanged>true</HasChanged>
      <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg... wATRRRSuB//2Q==</PictureData>
    </GetUserPhotoResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-mailbox-user-photo-by-using-the-resolvenames-operation"></a>要使用 ResolveNames 操作获取邮箱用户照片

如果您不知道您正在为其获取照片的用户的电子邮件地址，则可以[使用 ResolveNames 操作](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)候选人获得可能的匹配项。 如果[ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx)元素的**ContactDataShape**属性指定"AllProperties"，将为每个候选返回大量数据，包括用户照片。 下面的示例演示 XML 请求以解析名称"Sadie"并为每个候选返回所有属性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

将在响应中返回大量数据。 下面的示例演示仅与用户照片相关的数据。 **照片**元素包含 （内容已缩短为便于阅读） 的 Base64 编码的用户照片。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="get-a-contact-user-photo-by-using-the-getattachment-operation"></a>要使用 GetAttachment 操作获取联系人的用户照片

您可以使用 EWS 获取来自存储在您的邮箱中的联系人的照片。 首先，您可以使用**GetItem**操作，您可以查找照片，以便返回所有属性。 下面的示例演示 XML 请求以获取联系人项目。 为便于阅读缩短了项目 ID。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
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

查找[HasPicture](http://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx)元素以验证联系人都有关联的照片。 然后查找的附件的值为 true，则[IsContactPhoto](http://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx)元素的集合。 以下响应示例显示了相关的数据。 为便于阅读缩短的 ID 值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

接下来，使用与**AttachmentId** **GetAttachment**操作请求附件已联系人的照片。 下面的示例演示 XML 请求以获取附件。 为便于阅读将被截 ID。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
         <t:AttachmentId Id="1LGlhgpgoA="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>

```

下面的示例演示 XML 响应与您请求的附件有关的信息。 [内容](http://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx)元素包含在此示例中为便于阅读缩短的用户照片的 Base64 编码字符串。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="decode-a-base64-encoded-string"></a>对 Base64 编码字符串进行解码

无论您使用获取用户照片的操作，您需要对该字符串进行解码，以便您可以在您的应用程序中使用它。 下面的示例演示如何解码字符串，然后将其保存到本地计算机，使您应用程序能够更高版本访问它。
  
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
- [模糊名称解析使用 EWS 在 Exchange 2013](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)    
- [在 Exchange 使用 EWS 的批次中的过程联系人](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    

