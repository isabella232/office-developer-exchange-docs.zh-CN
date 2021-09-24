---
title: 使用 Exchange 中的 EWS 分批处理联系人
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 455f475b-cb19-4e7a-8ff3-92f7028fceb0
description: 了解如何在单个调用中通过使用 EWS 托管 API 或 EWS 在单个调用中创建、获取、更新和删除Exchange。
ms.openlocfilehash: e70618dc0a9ea3f2d534c79fff627393ced8f1cb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522220"
---
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 分批处理联系人

了解如何在单个调用中通过使用 EWS 托管 API 或 EWS 在单个调用中创建、获取、更新和删除Exchange。
  
您可以使用 EWS 托管 API 或 EWS 处理成批联系人，以减少客户端对 Exchange 服务器进行调用的数量。 使用 EWS 托管 API 批量创建、获取、更新和删除联系人时，可使用 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象方法，而使用单个联系人时，可使用 [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) 对象方法。 如果使用的是 EWS，则使用相同的操作处理单个联系人和成批联系人。 
  
**表 1.用于处理联系人批处理的 EWS 托管 API 方法和 EWS 操作**

|**若要...**|**使用此 EWS 托管 API 方法**|**使用此 EWS 操作**|
|:-----|:-----|:-----|
|分批创建联系人  <br/> |[ExchangeService.CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|分批获取联系人  <br/> |[ExchangeService.BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) 或 [ExchangeService.LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|分批更新联系人  <br/> |[ExchangeService.UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|批量删除联系人  <br/> |[ExchangeService.DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
本文将了解如何使用 EWS 托管 API 或 EWS 完成批量联系人的基本任务。
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 分批创建联系人
<a name="bk_EWSMA"> </a>

您可以使用 EWS 托管 API [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) 方法分批创建联系人，如以下示例所示。 本示例在本地创建三 [个 Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) 对象，将每个联系人添加到集合中，然后对联系人集合调用 **CreateItems** 方法。 
  
```cs
public static Collection<ItemId> CreateContactsInBatch(ExchangeService service)
{
    // These are unsaved local instances of a Contact object.
    // Despite the required parameter of an ExchangeService object (service), no call
    // to an Exchange server is made when the objects are instantiated.
    // A call to the Exchange server is made when the service.CreateItems() method is called.
    Contact contact1 = new Contact(service);
    Contact contact2 = new Contact(service);
    Contact contact3 = new Contact(service);
    // Set the properties on the first contact.
    contact1.DisplayName = "Sadie Daniels";
    contact1.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("sadie@contoso.com");
    
    // Set the properties on the second contact.
    contact2.DisplayName = "Alfred Welker";
    contact2.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("alfred@contoso.com");
    // Set the properties on the third contact.
    contact3.DisplayName = "Hope Gross";
    contact3.EmailAddresses[EmailAddressKey.EmailAddress1] = new EmailAddress("hope@contoso.com");
    // Add the Contact objects to a collection.
    Collection<Contact> contactItems = new Collection<Contact>() { contact1, contact2, contact3 };
    // Create the batch of contacts on the server.
    // This method call results in an CreateItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.CreateItems(contactItems, WellKnownFolderName.Contacts, null, null);
    // Instantiate a collection of item IDs to populate from the values that are returned by the Exchange server.
    Collection<ItemId> itemIds = new Collection<ItemId>();
    // Collect the item IDs from the created contacts.
    foreach (Contact contact in contactItems)
    {
        try
        {
            itemIds.Add(contact.Id);
            Console.WriteLine("Contact '{0}' created successfully.", contact.DisplayName);
        }
        catch (Exception ex)
        {
            // Print out the exception and the last eight characters of the item ID.
            Console.WriteLine("Exception while creating contact {0}: {1}", contact.Id.ToString().Substring(144), ex.Message);
        }
    }
    // Determine whether the CreateItems method call completed successfully.
    if (response.OverallResult == ServiceResult.Success)
    {
            Console.WriteLine("All locally created contacts were successfully created in the Contacts folder.");
            Console.WriteLine("\r\n");
    }
   
    // If the method did not return success, print the result message for each contact.
    else
    {
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            // Print out the result and the last eight characters of the item ID.
            Console.WriteLine("Result (contact {0}), id {1}: {2}", counter, itemIds[counter - 1].ToString().Substring(144), resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            Console.WriteLine("\r\n");
            counter++;
        }
    }
    return itemIds;
}
```

## <a name="create-contacts-in-batches-by-using-ews"></a>使用 EWS 成批创建联系人
<a name="bk_EWSMA"> </a>

可以使用 [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS 操作分批创建联系人，如下面的代码示例所示。 这也是当您使用 EWS 托管 API 批量创建联系人时，EWS 托管 API 发送的 XML [请求](#bk_EWSMA)。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:CreateItem>
        <m:SavedItemFolderId>
          <t:DistinguishedFolderId Id="contacts" />
        </m:SavedItemFolderId>
        <m:Items>
          <t:Contact>
            <t:DisplayName>Sadie Daniels</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">sadie@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
          <t:Contact>
            <t:DisplayName>Alfred Welker</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">alfred@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
          <t:Contact>
            <t:DisplayName>Hope Gross</t:DisplayName>
            <t:EmailAddresses>
              <t:Entry Key="EmailAddress1">hope@contoso.com</t:Entry>
            </t:EmailAddresses>
          </t:Contact>
        </m:Items>
      </m:CreateItem>
    </soap:Body>
  </soap:Envelope>
```

服务器使用 [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应 **CreateItem** 请求，其中包含每个新联系人的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值 **NoError，** 指示已成功创建和保存每个联系人。 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 成批获取联系人
<a name="bk_EWSMAGet"> </a>

您可以使用 EWS 托管 API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) 方法分批获取联系人，如以下示例所示。 此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
public static Collection<Contact> BatchGetContactItems(ExchangeService service, Collection<ItemId> itemIds)
        {
            // Create a property set that limits the properties returned by the Bind method to only those that are required.
            PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ContactSchema.DisplayName);
            // Get the items from the server.
            // This method call results in a GetItem call to EWS.
            ServiceResponseCollection<GetItemResponse> response = service.BindToItems(itemIds, propSet);
            // Instantiate a collection of Contact objects to populate from the values that are returned by the Exchange server.
            Collection<Contact> contactItems = new Collection<Contact>();
            foreach (GetItemResponse getItemResponse in response)
            {
                try
                {
                    Item item = getItemResponse.Item;
                    Contact contact = (Contact)item;
                    contactItems.Add(contact);
                    // Print out confirmation and the last eight characters of the item ID.
                    Console.WriteLine("Found item {0}.", contact.Id.ToString().Substring(144));
                }
                catch (Exception ex)
                {
                    Console.WriteLine("Exception while getting a contact: {0}", ex.Message);
                }
            }
            // Check for success of the BindToItems method call.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("All contacts retrieved successfully.");
                Console.WriteLine("\r\n");
            }
            return contactItems;
        }

```

## <a name="get-contacts-in-batches-by-using-ews"></a>使用 EWS 成批获取联系人
<a name="bk_EWSMAGet"> </a>

您可以使用 [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作和以下示例中的代码分批获取联系人。 这也是当您使用 EWS 托管 API 批量获取联系人时，EWS 托管 API 发送的 XML [请求](#bk_EWSMAGet)。 **ItemId** 属性已缩短为可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
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
            <t:FieldURI FieldURI="contacts:DisplayName" />
          </t:AdditionalProperties>
        </m:ItemShape>
        <m:ItemIds>
          <t:ItemId Id="ceJwVAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yS" />
          <t:ItemId Id="ceJwWAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yT" />
          <t:ItemId Id="ceJwXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yU" />
        </m:ItemIds>
      </m:GetItem>
    </soap:Body>
  </soap:Envelope>
```

服务器使用 [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应 **GetItem** 请求，其中包含每个显示名称的 ID 和联系人 ID。 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 批量更新联系人
<a name="bk_EWSMAUpdate"> </a>

您可以使用 EWS 托管 API [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) 方法批量更新联系人，如以下示例所示。 上一个示例创建联系人，但不指定其工作人员。 可以使用此示例中的代码一次更新所有联系人，以包含其公司名称。 
  
此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
public static Collection<Contact> BatchUpdateContactItems(ExchangeService service, Collection<Contact> contactItems)
        {
            // Update the company name of each contact locally.
            foreach (Contact contact in contactItems)
            {
                // Update the company name of the contact.
                contact.CompanyName = "Contoso";
                // Print out confirmation with the last eight characters of the item ID and the contact company name.
                Console.WriteLine("Updated local contact {0} with the company name '{1}'.", contact.Id.ToString().Substring(144), contact.CompanyName);
            }
            
            // Send the item updates to the server.
            // This method call results in an UpdateItem call to EWS.
            ServiceResponseCollection<UpdateItemResponse> response = service.UpdateItems(contactItems, WellKnownFolderName.Contacts, ConflictResolutionMode.AutoResolve, null, null);
            // Verify the success of the UpdateItems method call.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("All contacts updated successfully.\r\n");
            }
            // If the method did not return success, print the result message for each contact.
            else
            {
                Console.WriteLine("All contacts were not successfully saved on the server.\r\n");
                int counter = 1;
                foreach (ServiceResponse resp in response)
                {
                    Console.WriteLine("Result for (contact {0}): {1}", counter, resp.Result);
                    Console.WriteLine("Error Code: {0}", resp.ErrorCode);
                    Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
                    counter++;
                }
            }
            return contactItems;
        }    

```

## <a name="update-contacts-in-batches-by-using-ews"></a>使用 EWS 成批更新联系人
<a name="bk_EWSMAUpdate"> </a>

您可以使用 [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作批量更新联系人，如下面的代码示例所示。 这也是当您使用 EWS 托管 API 批量更新联系人时，EWS 托管 API 发送的 XML [请求](#bk_EWSMAUpdate)。 **ItemId** 属性已缩短为可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:UpdateItem ConflictResolution="AutoResolve">
        <m:SavedItemFolderId>
          <t:DistinguishedFolderId Id="contacts" />
        </m:SavedItemFolderId>
        <m:ItemChanges>
          <t:ItemChange>
            <t:ItemId Id="ceJwVAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yS" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
          <t:ItemChange>
            <t:ItemId Id="ceJwWAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yT" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
          <t:ItemChange>
            <t:ItemId Id="ceJwXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yU" />
            <t:Updates>
              <t:SetItemField>
                <t:FieldURI FieldURI="contacts:CompanyName" />
                <t:Contact>
                  <t:CompanyName>Contoso</t:CompanyName>
                </t:Contact>
              </t:SetItemField>
            </t:Updates>
          </t:ItemChange>
        </m:ItemChanges>
      </m:UpdateItem>
    </soap:Body>
  </soap:Envelope>
```

服务器使用 [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)消息响应 **UpdateItem** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值，该值指示服务器上已成功保存每个更新。 任何冲突都报告在 [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) 元素中。 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 批量删除联系人
<a name="bk_EWSMADelete"> </a>

您可以使用 [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) EWS 托管 API 方法批量删除联系人，如以下示例所示。 此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
public static void BatchDeleteContactItems(ExchangeService service, Collection<ItemId> itemIds)
        {
            // Delete the batch of contact objects.
            // This method call results in an DeleteItem call to EWS.
            ServiceResponseCollection<ServiceResponse> response = service.DeleteItems(itemIds, DeleteMode.SoftDelete, null, AffectedTaskOccurrence.AllOccurrences);
            // Check for success of the DeleteItems method call.
            // DeleteItems returns success even if it does not find all the item IDs.
            if (response.OverallResult == ServiceResult.Success)
            {
                Console.WriteLine("Contacts deleted successfully.\r\n");
            }
            // If the method did not return success, print a message.
            else
            {
                Console.WriteLine("Not all contacts deleted successfully.\r\n");
            }
        }

```

## <a name="delete-contacts-in-batches-by-using-ews"></a>使用 EWS 批量删除联系人
<a name="bk_EWSMADelete"> </a>

您可以使用 [DeleteItem](../web-service-reference/deleteitem-operation.md) EWS 操作批量删除联系人，如下面的代码示例所示。 这也是当您使用 EWS 托管 API 批量删除联系人时，EWS 托管 API 发送的 XML [请求](#bk_EWSMADelete)。 **ItemId** 属性已缩短为可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:DeleteItem DeleteType="SoftDelete" AffectedTaskOccurrences="AllOccurrences">
        <m:ItemIds>
          <t:ItemId Id="ceJwYAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yY" />
          <t:ItemId Id="ceJwZAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51yZ" />
          <t:ItemId Id="ceJwaAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AAFc51ya" />
        </m:ItemIds>
      </m:DeleteItem>
    </soap:Body>
  </soap:Envelope>
```

服务器使用 [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx)消息响应 **DeleteItem** 请求，其中包含已删除每个项目的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值 **NoError。** 请注意，如果找不到项目 ID，操作也会返回成功。 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a>验证批处理是否成功完成
<a name="bk_successful"> </a>

当批处理请求中的一个或多个联系人无法按照请求进行处理时，将针对每个失败的联系人返回错误，并且批处理中的其余联系人将按预期进行处理。 如果项目已删除，因此无法检索或更新，或者项目移动到其他文件夹，因此具有新的项目 ID，并且无法在发送项目 ID 后进行修改，则批处理中可能发生失败。 本节中的信息演示如何获取有关联系人批处理中的失败的错误详细信息。
  
若要使用 EWS 托管 API 验证批处理是否成功，可以检查[ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx)的[OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx)属性是否等于[ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)。 如果是，则所有联系人都已成功处理。 如果 **OverallResult** 不等于 **ServiceResult.Success**，则一个或多个联系人未成功处理。 **ServiceResponseCollection** 中返回的每个对象都包含以下属性： 
  
- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [结果](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
这些属性包含有关无法根据请求处理联系人的原因的信息。 本文中的示例打印出每个失败联系人的结果 **、ErrorCode** 和 **ErrorMessage。** 您可以使用这些结果来调查问题。 
  
对于 EWS，若要验证批处理过程是否成功，请检查所处理的每个项目的 [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) 属性。 下面是 **ResponseMessageType** 的基本结构，它是派生所有响应消息的基类型。 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

如果已成功处理联系人 **，则** **ResponseClass** 属性设置为 Success;如果联系人未成功处理，则设置为 Error。 对于联系人，在批处理 **过程中不会** 遇到警告。 如果 **ResponseClass** 为 **Success**，则 [以下 ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 元素也始终设置为 **NoError**。 如果 **ResponseClass** 为 **Error，** 则需要检查 [MessageText、ResponseCode](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)和 [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx)元素的值，以确定导致该问题的原因。 [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) 当前未使用。 
  
## <a name="see-also"></a>另请参阅


- [人员和 Exchange 中的 EWS 中的联系人](people-and-contacts-in-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 批量处理电子邮件](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [在日历中分批处理日历Exchange](how-to-process-calendar-items-in-batches-in-exchange.md)
    

