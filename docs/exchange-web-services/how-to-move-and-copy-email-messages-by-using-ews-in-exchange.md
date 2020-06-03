---
title: 使用 Exchange 中的 EWS 移动和复制电子邮件
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4771668f-5623-4397-a5c0-b75a7ba01698
description: 了解如何在 Exchange 中使用 EWS 托管 API 或 EWS 移动和复制电子邮件。
localization_priority: Priority
ms.openlocfilehash: d13e84648f194dd4f431cf128396daf016addb22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527934"
---
# <a name="move-and-copy-email-messages-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 移动和复制电子邮件

了解如何在 Exchange 中使用 EWS 托管 API 或 EWS 移动和复制电子邮件。
  
您可以使用 EWS 托管 API 或 EWS 在邮箱中移动和复制电子邮件。
  
**表1。用于移动和复制电子邮件的 EWS 托管 API 方法和 EWS 操作**

|**任务**|**EWS 托管的 API 方法**|**EWS 操作**|
|:-----|:-----|:-----|
|移动电子邮件  <br/> |[EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx) <br/> |[MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> |
|复制电子邮件  <br/> |[EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx) <br/> |[CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
   
请务必注意，当您将电子邮件移动或复制到另一个文件夹中时，将会在具有唯一项目 ID 的新文件夹中创建一个新项目，并删除原始邮件。 如果要在同一邮箱中的两个文件夹之间移动或复制电子邮件，则会在响应中返回新项目，从而使您可以访问新的项目 ID。 但是，如果要在两个邮箱之间或邮箱与公用文件夹之间移动或复制电子邮件，响应中不会返回新项目。 若要在该方案中访问移动的邮件，请使用 EWS 托管 API [FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法或 EWS [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作，为[PidTagSearchKey](https://msdn.microsoft.com/library/cc839918.aspx) （0x300B0102）属性[创建扩展属性定义](properties-and-extended-properties-in-ews-in-exchange.md)，或者创建和设置自定义扩展属性，然后在新文件夹中搜索自定义扩展属性。 
  
删除电子邮件与将项目移动到 "已删除邮件" 文件夹中的邮件不同。 如果使用 EWS 托管 API[项。 Delete](https://msdn.microsoft.com/library/office/dd635072%28v=exchg.80%29.aspx)方法或 EWS [DeleteItem](../web-service-reference/deleteitem-operation.md)操作，将从原始文件夹中删除在请求中指定的项目，并将副本放在 "已删除邮件" 文件夹中，同时包含一个新的项目 ID。 与移动或复制任何项不同时， **Delete**方法或**DeleteItem**操作响应中不会返回新项。 [使用 EWS 托管 API 或 EWS 删除电子邮件](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma)所涉及的步骤与[EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews)从 Exchange 存储中删除任何通用项的步骤相同。 
  
## <a name="move-an-email-message-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 移动电子邮件
<a name="bk_moveewsma"> </a>

下面的代码示例演示如何使用[EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx)方法将现有电子邮件从一个文件夹移动到另一个文件夹。 
  
此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且**ItemId**是要移动或复制的电子邮件的[Id](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) 。 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage beforeMessage = EmailMessage.Bind(service, ItemId, propSet);
// Move the specified mail to the JunkEmail folder and store the returned item.
Item item = beforeMessage.Move(WellKnownFolderName.JunkEmail);
// Check that the item was moved by binding to the moved email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage movedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + beforeMessage.Subject + "' has been moved from the '" + beforeMessage.ParentFolderId + "' folder to the '" + movedMessage.ParentFolderId + "' folder.");
```

## <a name="move-an-email-message-by-using-ews"></a>使用 EWS 移动电子邮件
<a name="bk_moveews"> </a>

下面的代码示例演示如何使用[MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)操作将电子邮件移动到 "垃圾邮件" 文件夹。 
  
这也是在调用[Move](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.move%28v=exchg.80%29.aspx)方法时由 EWS 托管 API 发送的 XML 请求。 为了方便读取，已缩短一些属性和元素的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:MoveItem>
      <m:ToFolderId>
        <t:DistinguishedFolderId Id="junkemail" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="AfwDoAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF25sM1" />
      </m:ItemIds>
    </m:MoveItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[MoveItemResponse](https://msdn.microsoft.com/library/77be5104-1e09-4d50-abec-4fadb3a230e5%28Office.15%29.aspx)邮件响应**MoveItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，表示电子邮件已成功移动。 该响应还包括新文件夹中电子邮件的**ItemId** ，这一点对于存储很重要，因为新文件夹中的**ItemId**是不同的。 
  
## <a name="copy-an-email-message-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 复制电子邮件
<a name="bk_copyewsma"> </a>

下面的代码示例演示如何使用[EmailMessage](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx)方法将现有电子邮件从一个文件夹复制到另一个文件夹。 
  
此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且**ItemId**是要复制的电子邮件的[Id](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) 。 为了提高可读性，某些参数的值已缩短。 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ParentFolderId);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage originalMessage = EmailMessage.Bind(service, ItemId, propSet);
// Copy the orignal message into another folder in the mailbox and store the returned item.
Item item = originalMessage.Copy("epQ/3AAA=");
// Check that the item was copied by binding to the copied email message 
// and retrieving the new ParentFolderId.
// This method call results in a GetItem call to EWS.
EmailMessage copiedMessage = EmailMessage.Bind(service, item.Id, propSet);
Console.WriteLine("An email message with the subject '" + originalMessage.Subject + "' has been copied from the '" + originalMessage.ParentFolderId + "' folder to the '" + copiedMessage.ParentFolderId + "' folder.");
```

## <a name="copy-an-email-message-by-using-ews"></a>使用 EWS 复制电子邮件
<a name="bk_copyews"> </a>

下面的代码示例演示如何使用[CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx)操作将电子邮件复制到同一邮箱中的不同文件夹中，方法是发送要移动的电子邮件的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) ，并在[ToFolderId](https://msdn.microsoft.com/library/bd6a4265-ad40-43f6-bcc4-0bf5df4e984c%28Office.15%29.aspx)元素中指定目标文件夹。 
  
这也是在调用[Copy](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.emailmessage.copy%28v=exchg.80%29.aspx)方法时由 EWS 托管 API 发送的 XML 请求。 为了方便读取，已缩短一些属性和元素的值。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:CopyItem>
      <m:ToFolderId>
        <t:FolderId Id="pQ/3AAA=" />
      </m:ToFolderId>
      <m:ItemIds>
        <t:ItemId Id="2TSeSAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF2d+3+" />
      </m:ItemIds>
    </m:CopyItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[CopyItemResponse](https://msdn.microsoft.com/library/ae402bc1-4589-45e0-a929-f368c916a7e4%28Office.15%29.aspx)邮件响应**CopyItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，表示电子邮件已成功复制。 该响应还包括新文件夹中电子邮件的**ItemId** ，这一点对于存储很重要，因为新文件夹中的**ItemId**是不同的。 
  
## <a name="see-also"></a>另请参阅


- [Exchange 中的电子邮件和 EMS](email-and-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 发送电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

