---
title: 使用 Exchange 中的 EWS 在批处理中处理联系人
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 455f475b-cb19-4e7a-8ff3-92f7028fceb0
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，在单个呼叫中创建、获取、更新和删除联系人的批量。
ms.openlocfilehash: 2e122f67693b4ba46120104d9a1f6d36b4d86f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527801"
---
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a><span data-ttu-id="89e7b-103">使用 Exchange 中的 EWS 在批处理中处理联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-103">Process contacts in batches by using EWS in Exchange</span></span>

<span data-ttu-id="89e7b-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，在单个呼叫中创建、获取、更新和删除联系人的批量。</span><span class="sxs-lookup"><span data-stu-id="89e7b-104">Learn how to create, get, update, and delete batches of contacts in a single call by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="89e7b-105">您可以使用 EWS 托管 API 或 EWS 来处理批量联系人，以减少客户端对 Exchange 服务器进行的调用次数。</span><span class="sxs-lookup"><span data-stu-id="89e7b-105">You can use the EWS Managed API or EWS to work with batches of contacts to reduce the number of calls a client makes to an Exchange server.</span></span> <span data-ttu-id="89e7b-106">当您使用 EWS 托管 API 在批处理中创建、获取、更新和删除联系人时，可以使用[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象方法，而在处理单个联系人时使用的是[Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx)对象方法。</span><span class="sxs-lookup"><span data-stu-id="89e7b-106">When you use the EWS Managed API to create, get, update, and delete contacts in batches, you use [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object methods, whereas when you work with single contacts, you use [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) object methods.</span></span> <span data-ttu-id="89e7b-107">如果使用 EWS，则可以使用相同的操作来处理单个联系人和批次联系人。</span><span class="sxs-lookup"><span data-stu-id="89e7b-107">If you are using EWS, you use the same operations to work with both a single contact and batches of contacts.</span></span> 
  
<span data-ttu-id="89e7b-108">**表1。用于处理批处理联系人的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="89e7b-108">**Table 1. EWS Managed API methods and EWS operations for working with batches of contacts**</span></span>

|<span data-ttu-id="89e7b-109">**若要...**</span><span class="sxs-lookup"><span data-stu-id="89e7b-109">**In order to…**</span></span>|<span data-ttu-id="89e7b-110">**使用此 EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="89e7b-110">**Use this EWS Managed API method**</span></span>|<span data-ttu-id="89e7b-111">**使用此 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="89e7b-111">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89e7b-112">批量创建联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-112">Create contacts in batches</span></span>  <br/> |[<span data-ttu-id="89e7b-113">ExchangeService。 CreateItems</span><span class="sxs-lookup"><span data-stu-id="89e7b-113">ExchangeService.CreateItems</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="89e7b-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="89e7b-114">CreateItem</span></span>](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="89e7b-115">批量获取联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-115">Get contacts in batches</span></span>  <br/> |<span data-ttu-id="89e7b-116">[BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx)或[ExchangeService LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx) ExchangeService</span><span class="sxs-lookup"><span data-stu-id="89e7b-116">[ExchangeService.BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) or [ExchangeService.LoadPropertiesForItems](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="89e7b-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="89e7b-117">GetItem</span></span>](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="89e7b-118">批量更新联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-118">Update contacts in batches</span></span>  <br/> |[<span data-ttu-id="89e7b-119">ExchangeService。 UpdateItems</span><span class="sxs-lookup"><span data-stu-id="89e7b-119">ExchangeService.UpdateItems</span></span>](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="89e7b-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="89e7b-120">UpdateItem</span></span>](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="89e7b-121">批量删除联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-121">Delete contacts in batches</span></span>  <br/> |[<span data-ttu-id="89e7b-122">ExchangeService。 DeleteItems</span><span class="sxs-lookup"><span data-stu-id="89e7b-122">ExchangeService.DeleteItems</span></span>](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="89e7b-123">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="89e7b-123">DeleteItem</span></span>](../web-service-reference/deleteitem-operation.md) <br/> |
   
<span data-ttu-id="89e7b-124">在本文中，您将了解如何使用 EWS 托管 API 或 EWS 完成批量联系人的基本任务。</span><span class="sxs-lookup"><span data-stu-id="89e7b-124">In this article, you'll learn how to complete basic tasks for batches of contacts by using the EWS Managed API or EWS.</span></span>
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="89e7b-125">使用 EWS 托管 API 以批处理方式创建联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-125">Create contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="89e7b-126"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-126"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="89e7b-127">您可以使用 EWS 托管 API [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)方法在批处理中创建联系人，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="89e7b-127">You can create contacts in batches by using the EWS Managed API [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="89e7b-128">本示例在本地创建三个[contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx)对象，将每个联系人添加到一个集合，然后对联系人集合调用**CreateItems**方法。</span><span class="sxs-lookup"><span data-stu-id="89e7b-128">This example creates three [Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) objects locally, adds each contact to a collection, then calls the **CreateItems** method on the collection of contacts.</span></span> 
  
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

## <a name="create-contacts-in-batches-by-using-ews"></a><span data-ttu-id="89e7b-129">使用 EWS 以批处理方式创建联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-129">Create contacts in batches by using EWS</span></span>
<span data-ttu-id="89e7b-130"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-130"><a name="bk_EWSMA"> </a></span></span>

<span data-ttu-id="89e7b-131">您可以使用[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS 操作在批处理中创建联系人，如下面的代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="89e7b-131">You can create contacts in batches by using the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="89e7b-132">这也是当您使用 EWS 托管 API 以批处理的形式[创建联系人](#bk_EWSMA)时，EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="89e7b-132">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [create contacts in batches](#bk_EWSMA).</span></span>
  
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

<span data-ttu-id="89e7b-133">服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含每个新联系人的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError** ，这表示每个联系人都已成功创建和保存。</span><span class="sxs-lookup"><span data-stu-id="89e7b-133">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new contacts, which indicates that each contact was created and saved successfully.</span></span> 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="89e7b-134">使用 EWS 托管 API 以批处理方式获取联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-134">Get contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="89e7b-135"><a name="bk_EWSMAGet"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-135"><a name="bk_EWSMAGet"> </a></span></span>

<span data-ttu-id="89e7b-136">您可以使用 EWS 托管 API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx)方法在批处理中获取联系人，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="89e7b-136">You can get contacts in batches by using the EWS Managed API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="89e7b-137">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="89e7b-137">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="get-contacts-in-batches-by-using-ews"></a><span data-ttu-id="89e7b-138">使用 EWS 通过批获取联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-138">Get contacts in batches by using EWS</span></span>
<span data-ttu-id="89e7b-139"><a name="bk_EWSMAGet"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-139"><a name="bk_EWSMAGet"> </a></span></span>

<span data-ttu-id="89e7b-140">您可以通过使用[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作和以下示例中的代码，在批处理中获取联系人。</span><span class="sxs-lookup"><span data-stu-id="89e7b-140">You can get contacts in batches by using the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation and the code in the following example.</span></span> <span data-ttu-id="89e7b-141">这也是当您使用 EWS 托管 API 以批处理的形式[获取联系人](#bk_EWSMAGet)时，EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="89e7b-141">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get contacts in batches](#bk_EWSMAGet).</span></span> <span data-ttu-id="89e7b-142">为了提高可读性， **ItemId**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="89e7b-142">The **ItemId** attribute has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="89e7b-143">服务器使用[GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应**GetItem**请求，其中包含每个请求的联系人的 ID 和显示名称。</span><span class="sxs-lookup"><span data-stu-id="89e7b-143">The server responds to the **GetItem** request with a [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes the ID and the display name for each of the requested contacts.</span></span> 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="89e7b-144">使用 EWS 托管 API 以批处理方式更新联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-144">Update contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="89e7b-145"><a name="bk_EWSMAUpdate"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-145"><a name="bk_EWSMAUpdate"> </a></span></span>

<span data-ttu-id="89e7b-146">您可以使用 EWS 托管 API [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx)方法在批处理中更新联系人，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="89e7b-146">You can update contacts in batches by using the EWS Managed API [UpdateItems](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="89e7b-147">上面的示例创建了联系人，但未指定其工作人员。</span><span class="sxs-lookup"><span data-stu-id="89e7b-147">The previous example creates the contact but does not specify who they work for.</span></span> <span data-ttu-id="89e7b-148">您可以使用此示例中的代码来一次更新所有联系人，以包含其公司名称。</span><span class="sxs-lookup"><span data-stu-id="89e7b-148">You can use the code in this example to update all your contacts at once to include their company name.</span></span> 
  
<span data-ttu-id="89e7b-149">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="89e7b-149">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="update-contacts-in-batches-by-using-ews"></a><span data-ttu-id="89e7b-150">使用 EWS 更新批次联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-150">Update contacts in batches by using EWS</span></span>
<span data-ttu-id="89e7b-151"><a name="bk_EWSMAUpdate"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-151"><a name="bk_EWSMAUpdate"> </a></span></span>

<span data-ttu-id="89e7b-152">您可以使用[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作在批处理中更新联系人，如下面的代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="89e7b-152">You can update contacts in batches by using the [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation, as shown in following code example.</span></span> <span data-ttu-id="89e7b-153">这也是当您使用 EWS 托管 API 以批处理的形式[更新联系人](#bk_EWSMAUpdate)时，EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="89e7b-153">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [update contacts in batches](#bk_EWSMAUpdate).</span></span> <span data-ttu-id="89e7b-154">为了提高可读性， **ItemId**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="89e7b-154">The **ItemId** attribute has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="89e7b-155">服务器使用[UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)邮件响应**UpdateItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，这表示每个更新在服务器上成功保存。</span><span class="sxs-lookup"><span data-stu-id="89e7b-155">The server responds to the **UpdateItem** request with an [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that each of the updates was saved successfully on the server.</span></span> <span data-ttu-id="89e7b-156">任何冲突都会在[ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx)元素中进行报告。</span><span class="sxs-lookup"><span data-stu-id="89e7b-156">Any conflicts are reported in the [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) element.</span></span> 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="89e7b-157">使用 EWS 托管 API 批量删除联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-157">Delete contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="89e7b-158"><a name="bk_EWSMADelete"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-158"><a name="bk_EWSMADelete"> </a></span></span>

<span data-ttu-id="89e7b-159">您可以使用[DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) EWS 托管 API 方法成批删除联系人，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="89e7b-159">You can delete contacts in batches by using the [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) EWS Managed API method, as shown in the following example.</span></span> <span data-ttu-id="89e7b-160">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="89e7b-160">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="delete-contacts-in-batches-by-using-ews"></a><span data-ttu-id="89e7b-161">使用 EWS 按批删除联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-161">Delete contacts in batches by using EWS</span></span>
<span data-ttu-id="89e7b-162"><a name="bk_EWSMADelete"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-162"><a name="bk_EWSMADelete"> </a></span></span>

<span data-ttu-id="89e7b-163">您可以使用[DeleteItem](../web-service-reference/deleteitem-operation.md) EWS 操作在批处理中删除联系人，如下面的代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="89e7b-163">You can delete contacts in batches by using the [DeleteItem](../web-service-reference/deleteitem-operation.md) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="89e7b-164">这也是当您使用 EWS 托管 API 以批处理的形式[删除联系人](#bk_EWSMADelete)时，EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="89e7b-164">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [delete contacts in batches](#bk_EWSMADelete).</span></span> <span data-ttu-id="89e7b-165">为了提高可读性， **ItemId**属性已缩短。</span><span class="sxs-lookup"><span data-stu-id="89e7b-165">The **ItemId** attribute has been shortened for readability.</span></span> 
  
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

<span data-ttu-id="89e7b-166">服务器使用[DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx)邮件响应**DeleteItem**请求，其中包含已删除的每个项目的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError** 。</span><span class="sxs-lookup"><span data-stu-id="89e7b-166">The server responds to the **DeleteItem** request with a [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each item that was removed.</span></span> <span data-ttu-id="89e7b-167">请注意，如果找不到项目 ID，该操作也会返回 success。</span><span class="sxs-lookup"><span data-stu-id="89e7b-167">Note that the operation also returns success if the item ID could not be found.</span></span> 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a><span data-ttu-id="89e7b-168">验证批处理已成功完成</span><span class="sxs-lookup"><span data-stu-id="89e7b-168">Verifying that a batch process completed successfully</span></span>
<span data-ttu-id="89e7b-169"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="89e7b-169"><a name="bk_successful"> </a></span></span>

<span data-ttu-id="89e7b-170">当批处理请求中的一个或多个联系人无法按要求处理时，将为每个失败的联系人返回一个错误，并按预期处理批处理中的其余联系人。</span><span class="sxs-lookup"><span data-stu-id="89e7b-170">When one or more contacts in a batched request can't be processed as requested, an error is returned for each contact that failed, and the rest of the contacts in the batch are processed as expected.</span></span> <span data-ttu-id="89e7b-171">如果项目已被删除、无法检索或更新，或者如果将项目移到其他文件夹，并因此包含了新的项目 ID，并且无法使用已发送的项目 ID 进行修改，则可能会发生批处理故障。</span><span class="sxs-lookup"><span data-stu-id="89e7b-171">Failures in batch processing can occur if the item was deleted, and therefore can't be retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID, and cannot be modified with the item ID sent.</span></span> <span data-ttu-id="89e7b-172">本节中的信息演示如何获取有关批量处理联系人的故障的错误详细信息。</span><span class="sxs-lookup"><span data-stu-id="89e7b-172">The information in this section shows how to get error details about failures in batch processing of contacts.</span></span>
  
<span data-ttu-id="89e7b-173">若要通过使用 EWS 托管 API 验证批处理是否成功，可以检查[ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx)的[OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx)属性是否等于[ServiceResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="89e7b-173">To verify the success of a batch process by using the EWS Managed API, you can check that the [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) property of the [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) is equal to [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="89e7b-174">如果是这样，则已成功处理所有联系人。</span><span class="sxs-lookup"><span data-stu-id="89e7b-174">If so, all the contacts were processed successfully.</span></span> <span data-ttu-id="89e7b-175">如果**OverallResult**不等于**ServiceResult**，则表示未成功处理一个或多个联系人。</span><span class="sxs-lookup"><span data-stu-id="89e7b-175">If the **OverallResult** is not equal to **ServiceResult.Success**, one or more of the contacts were not processed successfully.</span></span> <span data-ttu-id="89e7b-176">**ServiceResponseCollection**中返回的每个对象都包含以下属性：</span><span class="sxs-lookup"><span data-stu-id="89e7b-176">Each of the objects returned in the **ServiceResponseCollection** contains the following properties:</span></span> 
  
- [<span data-ttu-id="89e7b-177">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="89e7b-177">ErrorCode</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="89e7b-178">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="89e7b-178">ErrorDetails</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="89e7b-179">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="89e7b-179">ErrorMessage</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="89e7b-180">ErrorProperties</span><span class="sxs-lookup"><span data-stu-id="89e7b-180">ErrorProperties</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="89e7b-181">结果</span><span class="sxs-lookup"><span data-stu-id="89e7b-181">Result</span></span>](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
<span data-ttu-id="89e7b-182">这些属性包含有关无法按要求处理联系人的原因的信息。</span><span class="sxs-lookup"><span data-stu-id="89e7b-182">These properties contain information about why the contacts could not be processed as requested.</span></span> <span data-ttu-id="89e7b-183">本文中的示例将输出每个失败联系人的**结果**、**错误代码**和**ErrorMessage** 。</span><span class="sxs-lookup"><span data-stu-id="89e7b-183">The examples in this article print out the **Result**, **ErrorCode**, and **ErrorMessage** for each failed contact.</span></span> <span data-ttu-id="89e7b-184">您可以使用这些结果来调查问题。</span><span class="sxs-lookup"><span data-stu-id="89e7b-184">You can use these results to investigate the issue.</span></span> 
  
<span data-ttu-id="89e7b-185">对于 EWS，若要验证批处理过程是否成功，请检查正在处理的每个项目的[ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="89e7b-185">For EWS, to verify the success of a batched process, check the [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) attribute for each item being processed.</span></span> <span data-ttu-id="89e7b-186">下面是**ResponseMessageType**的基本结构，它是从中派生所有响应消息的基类型。</span><span class="sxs-lookup"><span data-stu-id="89e7b-186">The following is the basic structure of the **ResponseMessageType**, the base type from which all response messages are derived.</span></span> 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

<span data-ttu-id="89e7b-187">如果成功处理了联系人，则将**ResponseClass**属性设置为**成功**，如果未成功处理联系人，则设置为 "**出错**"。</span><span class="sxs-lookup"><span data-stu-id="89e7b-187">The **ResponseClass** attribute is set to **Success** if the contact was processed successfully, or **Error** if the contact was not processed successfully.</span></span> <span data-ttu-id="89e7b-188">对于联系人，在批处理过程中不会遇到**警告**。</span><span class="sxs-lookup"><span data-stu-id="89e7b-188">For contacts, you will not encounter a **Warning** during batch processing.</span></span> <span data-ttu-id="89e7b-189">如果**ResponseClass**是**成功**的，则后面的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素也始终设置为**NoError**。</span><span class="sxs-lookup"><span data-stu-id="89e7b-189">If the **ResponseClass** is **Success**, the [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element that follows is also always set to **NoError**.</span></span> <span data-ttu-id="89e7b-190">如果**ResponseClass**为**错误**，则需要检查[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)、 **ResponseCode**和[MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx)元素的值，以确定导致该问题的原因。</span><span class="sxs-lookup"><span data-stu-id="89e7b-190">If the **ResponseClass** is **Error**, you need to check the values of the [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**, and [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) elements to determine what caused the problem.</span></span> <span data-ttu-id="89e7b-191">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx)当前未使用。</span><span class="sxs-lookup"><span data-stu-id="89e7b-191">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) is currently unused.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89e7b-192">另请参阅</span><span class="sxs-lookup"><span data-stu-id="89e7b-192">See also</span></span>


- [<span data-ttu-id="89e7b-193">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="89e7b-193">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="89e7b-194">使用 Exchange 中的 EWS 批量处理电子邮件</span><span class="sxs-lookup"><span data-stu-id="89e7b-194">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="89e7b-195">在 Exchange 中批量处理日历项目</span><span class="sxs-lookup"><span data-stu-id="89e7b-195">Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    

