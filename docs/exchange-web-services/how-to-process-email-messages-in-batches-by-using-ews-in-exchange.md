---
title: 使用 Exchange 中的 EWS 批量处理电子邮件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 96390f92-cab1-4de6-9ec2-a55678fc20af
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，在单个呼叫中创建、获取、更新和删除电子邮件的批量。
localization_priority: Priority
ms.openlocfilehash: 2592076c9c5b57356d96872f006dd7b0abfc328a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527773"
---
# <a name="process-email-messages-in-batches-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 批量处理电子邮件

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，在单个呼叫中创建、获取、更新和删除电子邮件的批量。

您可以使用 EWS 托管 API 或 EWS 来处理批处理电子邮件，以减少客户端对 Exchange 服务器进行的呼叫数。 当您使用 EWS 托管 API 以批处理方式创建、获取、更新、删除和发送邮件时，您可以使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象方法，而在处理单个电子邮件时，使用[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象方法。 如果使用 EWS，则可以使用相同的操作来处理单个电子邮件和一批电子邮件。

**表1。用于处理批处理电子邮件的 EWS 托管 API 方法和 EWS 操作**

|**若要...**|**使用此 EWS 托管 API 方法**|**使用此 EWS 操作**|
|:-----|:-----|:-----|
|批量创建电子邮件  <br/> |[ExchangeService。 CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|批量获取电子邮件  <br/> |[ExchangeService。 BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|批量更新电子邮件  <br/> |[ExchangeService。 UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|批量删除电子邮件  <br/> |[ExchangeService。 DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |

在本文中，您将了解如何使用 EWS 托管 API 或 EWS 完成批量电子邮件的基本任务。

## <a name="create-email-messages-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 成批创建电子邮件
<a name="bk_createewsma"> </a>

您可以使用 EWS 托管 API **CreateItems**方法成批创建邮件，如下面的示例所示。 本示例在本地创建三个[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)对象，将每封邮件添加到一个集合，然后对邮件集合调用**CreateItems**方法。

此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。

```cs
public static Collection<ItemId> CreateDraftEmailInBatch(ExchangeService service)
{
    // These are unsaved local instances of an EmailMessage object.
    // Despite the required parameter of an ExchangeService object (service), no call
    // to an Exchange server is made when the objects are instantiated.
    // A call to the Exchange server is made when the service.CreateItems() method is called.
    EmailMessage message1 = new EmailMessage(service);
    EmailMessage message2 = new EmailMessage(service);
    EmailMessage message3 = new EmailMessage(service);
    // Set the properties on the first message.
    message1.Subject = "Project priorities";
    message1.Body = "(1) Buy pizza, (2) Eat pizza";
    message1.ToRecipients.Add("sadie@contoso.com");
    // Set the properties on the second message.
    message2.Subject = "Company Soccer Team";
    message2.Body = "Are you interested in joining?";
    message2.ToRecipients.Add("magdalena@contoso.com");
    // Set the properties on the third message.
    message3.Subject = "Code Blast";
    message3.Body = "Are you interested in getting together to finish the methods for the ContosoLive project?";
    message3.ToRecipients.Add("mack@contoso.com");
    // Add the EmailMessage objects to a collection.
    Collection<EmailMessage> messageItems = new Collection<EmailMessage>() { message1, message2, message3 };
    // Create the batch of email messages on the server.
    // This method call results in an CreateItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.Drafts, MessageDisposition.SaveOnly, null);
    // Instantiate a collection of item IDs to populate from the values that are returned by the Exchange server.
    Collection<ItemId> itemIds = new Collection<ItemId>();
    // Collect the item IDs from the created email messages.
    foreach (EmailMessage message in messageItems)
    {
        try
        {
            itemIds.Add(message.Id);
            Console.WriteLine("Email message '{0}' created successfully.", message.Subject);
        }
        catch (Exception ex)
        {
            // Print out the exception and the last eight characters of the item ID.
            Console.WriteLine("Exception while creating message {0}: {1}", message.Id.ToString().Substring(144), ex.Message);
        }
    }
    // Check for success of the CreateItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
            Console.WriteLine("All locally created messages were successfully saved to the Drafts folder.");
            Console.WriteLine("\r\n");
    }

    // If the method did not return success, print the result message for each email.
    else
    {
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            // Print out the result and the last eight characters of the item ID.
            Console.WriteLine("Result (message {0}), id {1}: {2}", counter, itemIds[counter - 1].ToString().Substring(144), resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            Console.WriteLine("\r\n");
            counter++;
        }
    }
    return itemIds;
}
```

请注意，该示例仅将邮件保存在 "草稿" 文件夹中。它不发送邮件。 有关如何发送邮件的详细信息，请参阅[使用 EWS 托管 API 以批处理方式发送电子邮件](#bk_sendewsma)。

## <a name="create-email-messages-in-batches-by-using-ews"></a>使用 EWS 以批处理方式创建电子邮件
<a name="bk_createews"> </a>

您可以使用[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS 操作以批处理方式创建电子邮件，如下面的代码示例所示。 这也是当您使用 EWS 托管 API[成批创建电子](#bk_createewsma)邮件时，EWS 托管 api 发送的 XML 请求。

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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Project priorities</t:Subject>
          <t:Body BodyType="HTML">(1) Buy pizza, (2) Eat pizza</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>magdalena@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
        <t:Message>
          <t:Subject>Code Blast</t:Subject>
          <t:Body BodyType="HTML">Are you interested in getting together to finish the methods for the ContosoLive project?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>mack@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含每个新邮件的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError** ，这表明已成功创建并保存每封电子邮件。

请注意，该示例仅将邮件保存在 "草稿" 文件夹中。它不发送邮件。 有关如何发送邮件的详细信息，请参阅[使用 EWS 以批处理方式发送电子邮件](#bk_sendews)。

## <a name="send-email-messages-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 成批发送电子邮件
<a name="bk_sendewsma"> </a>

您可以使用相同的代码以批处理方式发送电子邮件，以批量创建电子邮件，只是几个[CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)方法参数发生了更改。 因此，若要使用 EWS 托管 API 发送电子邮件，请使用用于[成批创建电子](#bk_createewsma)邮件的代码，并将对**CreateItems**方法的调用替换为以下示例中的调用。 在此示例中，将在 "已发送邮件" 文件夹中创建邮件，并将邮件处置更改为[MessageDisposition SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx)，以便发送邮件，而不是仅在本地保存。

```cs
// Create and send the batch of email messages on the server.
// This method call results in an CreateItem call to EWS.
ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.SentItems, MessageDisposition.SendAndSaveCopy, null);
```

## <a name="send-email-messages-in-batches-by-using-ews"></a>使用 EWS 以批处理方式发送电子邮件
<a name="bk_sendews"> </a>

使用相同的代码以批处理的形式发送电子邮件，以批量创建电子邮件，只是**CreateItem**操作的一些属性值发生了更改。 因此，若要使用 EWS 发送电子邮件，请使用用于[成批创建电子](#bk_createews)邮件的代码，并将**MessageDisposition**值更改为 "SendAndSaveCopy"，并将[DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx)更改为 "已发送邮件"，如下面的代码示例所示。

```XML
<m:CreateItem MessageDisposition="SendAndSaveCopy">
  <m:SavedItemFolderId>
    <t:DistinguishedFolderId Id="sentitems" />
  </m:SavedItemFolderId>
```

服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含每个新邮件的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError** ，这表明已成功创建并发送了每封电子邮件。

## <a name="get-email-messages-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 批量获取电子邮件
<a name="bk_getewsma"> </a>

您可以使用 EWS 托管 API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx)方法成批获取电子邮件，如下面的示例所示。

此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。

```cs
public static Collection<EmailMessage> BatchGetEmailItems(ExchangeService service, Collection<ItemId> itemIds)
{
    // Create a property set that limits the properties returned by the Bind method to only those that are required.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
    // Get the items from the server.
    // This method call results in a GetItem call to EWS.
    ServiceResponseCollection<GetItemResponse> response = service.BindToItems(itemIds, propSet);

    // Instantiate a collection of EmailMessage objects to populate from the values that are returned by the Exchange server.
    Collection<EmailMessage> messageItems = new Collection<EmailMessage>();
    foreach (GetItemResponse getItemResponse in response)
    {
        try
        {
            Item item = getItemResponse.Item;
            EmailMessage message = (EmailMessage)item;
            messageItems.Add(message);
            // Print out confirmation and the last eight characters of the item ID.
            Console.WriteLine("Found item {0}.", message.Id.ToString().Substring(144));
        }
        catch (Exception ex)
        {
           Console.WriteLine("Exception while getting a message: {0}", ex.Message);
        }
    }
    // Check for success of the BindToItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("All email messages retrieved successfully.");
        Console.WriteLine("\r\n");
    }
        return messageItems;
}
```

## <a name="get-email-messages-in-batches-by-using-ews"></a>使用 EWS 以批处理方式获取电子邮件
<a name="bk_getews"> </a>

您可以通过使用[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作和以下示例中的代码批量获取电子邮件。 这也是当您使用 EWS 托管 API[批量获取电子](#bk_getewsma)邮件时，EWS 托管 api 发送的 XML 请求。

为了提高可读性， **ItemId**和**ChangeKey**属性已缩短。

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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="message:ToRecipients" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="m4NxAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB0" />
        <t:ItemId Id="m4NyAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB1" />
        <t:ItemId Id="m4NzAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB2" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应**GetItem**请求，其中包含每个请求的邮件的[第一个类属性](email-properties-and-elements-in-ews-in-exchange.md)。

## <a name="update-email-messages-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 成批更新电子邮件
<a name="bk_updateewsma"> </a>

您可以使用 EWS 托管 API [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx)方法成批获取电子邮件，如下面的示例所示。

有关可写电子邮件属性的列表，请参阅[Exchange 中的电子邮件属性和 EWS](email-properties-and-elements-in-ews-in-exchange.md)中的元素。

有关如何在更新后发送草稿邮件的详细信息，请参阅[使用 EWS 托管 API 发送电子邮件](#bk_sendewsma)。

此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。

```cs
public static Collection<EmailMessage> BatchUpdateEmailItems(ExchangeService service, Collection<EmailMessage> messageItems)
{
    // Update the subject of each message locally.
    foreach (EmailMessage message in messageItems)
    {
        // Update the Subject of the email.
        message.Subject = "Updated subject at " + DateTime.Now;
        // Print out confirmation with the last eight characters of the item ID and the email subject.
        Console.WriteLine("Updated local email message {0} with the subject '{1}'.", message.Id.ToString().Substring(144), message.Subject);
    }
    // Send the item updates to the server.
    // This method call results in an UpdateItem call to EWS.
    ServiceResponseCollection<UpdateItemResponse> response = service.UpdateItems(messageItems, WellKnownFolderName.Drafts, ConflictResolutionMode.AutoResolve, MessageDisposition.SaveOnly, null);
    // Check for success of the UpdateItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("All email messages updated successfully.\r\n");
    }
    // If the method did not return success, print the result message for each email.
    else
    {
        Console.WriteLine("All emails were not successfully saved on the server.\r\n");
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            Console.WriteLine("Result for (message {0}): {1}", counter, resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            counter++;
        }
    }
    return messageItems;
}
```

## <a name="update-email-messages-in-batches-by-using-ews"></a>使用 EWS 更新批处理中的电子邮件
<a name="bk_updateews"> </a>

您可以使用[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作批量更新电子邮件，如下面的代码示例所示。 这也是当您使用 EWS 托管 API[成批更新电子](#bk_updateewsma)邮件时，EWS 托管 api 发送的 XML 请求。

有关可写电子邮件元素的列表，请参阅[Exchange 中的电子邮件属性和 EWS](email-properties-and-elements-in-ews-in-exchange.md)中的元素。

有关如何在更新后发送草稿邮件的详细信息，请参阅[使用 EWS 发送草稿电子](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews)邮件。

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
    <m:UpdateItem MessageDisposition="SaveOnly"
                  ConflictResolution="AutoResolve">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="m4OVAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKCy" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
        <t:ItemChange>
          <t:ItemId Id="m4OWAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKCz" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
        <t:ItemChange>
          <t:ItemId Id="m4OXAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKC0" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)邮件响应**UpdateItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，这表示每个更新在服务器上成功保存。 任何冲突都会在[ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx)元素中进行报告。

## <a name="delete-email-messages-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 成批删除电子邮件
<a name="bk_deleteewsma"> </a>

您可以使用 EWS 托管 API [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx)方法成批删除邮件，如下面的示例所示。

此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。

```cs
public static void BatchDeleteEmailItems(ExchangeService service, Collection<ItemId> itemIds)
{
    // Delete the batch of email message objects.
    // This method call results in an DeleteItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.DeleteItems(itemIds, DeleteMode.SoftDelete, null, AffectedTaskOccurrence.AllOccurrences);

    // Check for success of the DeleteItems method call.
    // DeleteItems returns success even if it does not find all the item IDs.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("Email messages deleted successfully.\r\n");
    }
    // If the method did not return success, print a message.
    else
    {
        Console.WriteLine("Not all email messages deleted successfully.\r\n");
    }
}
```

## <a name="delete-email-messages-in-batches-by-using-ews"></a>使用 EWS 按批删除电子邮件
<a name="bk_deleteews"> </a>

您可以使用[DeleteItem](../web-service-reference/deleteitem-operation.md) EWS 操作批量删除电子邮件，如下面的代码示例所示。 这也是当您使用 EWS 托管 API[成批删除电子](#bk_deleteewsma)邮件时，EWS 托管 api 发送的 XML 请求。

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
    <m:DeleteItem DeleteType="SoftDelete"
                  AffectedTaskOccurrences="AllOccurrences">
      <m:ItemIds>
        <t:ItemId Id="m4OkAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDE" />
        <t:ItemId Id="m4OlAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDF" />
        <t:ItemId Id="m4OmAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDG" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用[DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx)邮件响应**DeleteItem**请求，其中包含已删除的每个项目的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError** 。 请注意，如果找不到项目 ID，该操作也会返回 success。

## <a name="verifying-that-a-batch-process-completed-successfully"></a>验证批处理已成功完成
<a name="bk_successful"> </a>

当批处理请求中的一个或多个电子邮件无法按要求处理时，将为每封失败的电子邮件返回一个错误，并按预期处理批处理中的其余电子邮件。 如果项目已被删除、无法发送、检索或更新，或者如果将项目移到其他文件夹，并因此包含了新的项目 ID，并且无法使用已发送的项目 ID 进行修改，批处理过程中可能会发生故障。 本节中的信息演示如何获取有关批量处理电子邮件失败的错误详细信息。

若要通过使用 EWS 托管 API 验证批处理是否成功，可以检查[ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx)的[OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx)属性是否等于[ServiceResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)。 如果是这样，则所有电子邮件都已成功处理。 如果**OverallResult**不等于**ServiceResult**，则表示一个或多个电子邮件未成功处理。 **ServiceResponseCollection**中返回的每个对象都包含以下属性：

- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)

- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)

- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)

- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)

- [结果](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)

这些属性包含有关电子邮件无法按要求处理的原因的信息。 本文中的示例将输出每个失败邮件的**结果**、**错误代码**和**ErrorMessage** 。 您可以使用这些结果来调查问题。

对于 EWS，若要验证批处理过程是否成功，请检查正在处理的每个项目的[ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx)属性。 下面是**ResponseMessageType**的基本结构，它是从中派生所有响应消息的基类型。

```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

如果成功处理了电子邮件，则将**ResponseClass**属性设置为**成功**，如果未成功处理电子邮件，则设置为 "**出错**"。 对于电子邮件，在批处理过程中不会出现**警告**。 如果**ResponseClass**是**成功**的，则后面的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素也始终设置为**NoError**。 如果**ResponseClass**为**错误**，则需要检查[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)、 **ResponseCode**和[MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx)元素的值，以确定导致该问题的原因。 [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx)当前未使用。

## <a name="see-also"></a>另请参阅


- [Exchange 中的电子邮件和 EMS](email-and-ews-in-exchange.md)

- [使用 Exchange 中的 EWS 发送电子邮件](how-to-send-email-messages-by-using-ews-in-exchange.md)

- [使用 Exchange 中的 EWS 响应电子邮件](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)

- [使用 Exchange 中的 EWS 移动和复制电子邮件](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)

- [EWS 批处理请求的限制影响](ews-throttling-in-exchange.md#throttling-implications-for-ews-batch-requests)
