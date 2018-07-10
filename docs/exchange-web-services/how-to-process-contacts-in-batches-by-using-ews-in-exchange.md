---
title: 在 Exchange 使用 EWS 的批次中的过程联系人
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 455f475b-cb19-4e7a-8ff3-92f7028fceb0
description: 了解如何创建、 获取、 更新和删除使用 EWS 托管 API 或 EWS 在 Exchange 中单个呼叫的联系人的批次。
ms.openlocfilehash: 7dfbda7fe5e077f92bcf7ebd40af40d76c2d2d22
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752872"
---
# <a name="process-contacts-in-batches-by-using-ews-in-exchange"></a><span data-ttu-id="4b76c-103">在 Exchange 使用 EWS 的批次中的过程联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-103">Process contacts in batches by using EWS in Exchange</span></span>

<span data-ttu-id="4b76c-104">了解如何创建、 获取、 更新和删除使用 EWS 托管 API 或 EWS 在 Exchange 中单个呼叫的联系人的批次。</span><span class="sxs-lookup"><span data-stu-id="4b76c-104">Learn how to create, get, update, and delete batches of contacts in a single call by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="4b76c-105">您可以使用 EWS 托管 API 或 EWS 以使用客户端的联系人，以降低的呼叫数的批次向 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="4b76c-105">You can use the EWS Managed API or EWS to work with batches of contacts to reduce the number of calls a client makes to an Exchange server.</span></span> <span data-ttu-id="4b76c-106">当您使用 EWS 托管 API 创建、 获取、 更新和删除批次中的联系人时，您将使用[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象方法，而与单个联系人时，您使用[联系人](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx)对象的方法。</span><span class="sxs-lookup"><span data-stu-id="4b76c-106">When you use the EWS Managed API to create, get, update, and delete contacts in batches, you use [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object methods, whereas when you work with single contacts, you use [Contact](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) object methods.</span></span> <span data-ttu-id="4b76c-107">如果您使用 EWS，使用相同的操作以使用单个联系人和联系人的批次。</span><span class="sxs-lookup"><span data-stu-id="4b76c-107">If you are using EWS, you use the same operations to work with both a single contact and batches of contacts.</span></span> 
  
<span data-ttu-id="4b76c-108">**表 1。EWS 托管 API 方法和用于处理的联系人的批次的 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="4b76c-108">**Table 1. EWS Managed API methods and EWS operations for working with batches of contacts**</span></span>

|<span data-ttu-id="4b76c-109">**若要...**</span><span class="sxs-lookup"><span data-stu-id="4b76c-109">**In order to…**</span></span>|<span data-ttu-id="4b76c-110">**使用此 EWS 托管 API 方法**</span><span class="sxs-lookup"><span data-stu-id="4b76c-110">**Use this EWS Managed API method**</span></span>|<span data-ttu-id="4b76c-111">**使用此 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="4b76c-111">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b76c-112">创建批处理中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-112">Create contacts in batches</span></span>  <br/> |[<span data-ttu-id="4b76c-113">ExchangeService.CreateItems</span><span class="sxs-lookup"><span data-stu-id="4b76c-113">ExchangeService.CreateItems</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b76c-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="4b76c-114">CreateItem</span></span>](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4b76c-115">获取批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-115">Get contacts in batches</span></span>  <br/> |<span data-ttu-id="4b76c-116">[ExchangeService.BindToItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx)或[ExchangeService.LoadPropertiesForItems](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b76c-116">[ExchangeService.BindToItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) or [ExchangeService.LoadPropertiesForItems](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx)</span></span> <br/> |[<span data-ttu-id="4b76c-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="4b76c-117">GetItem</span></span>](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4b76c-118">更新批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-118">Update contacts in batches</span></span>  <br/> |[<span data-ttu-id="4b76c-119">ExchangeService.UpdateItems</span><span class="sxs-lookup"><span data-stu-id="4b76c-119">ExchangeService.UpdateItems</span></span>](http://msdn.microsoft.com/zh-cn/library/dd634705%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b76c-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="4b76c-120">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4b76c-121">删除批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-121">Delete contacts in batches</span></span>  <br/> |[<span data-ttu-id="4b76c-122">ExchangeService.DeleteItems</span><span class="sxs-lookup"><span data-stu-id="4b76c-122">ExchangeService.DeleteItems</span></span>](http://msdn.microsoft.com/zh-cn/library/dd635460%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="4b76c-123">删除项</span><span class="sxs-lookup"><span data-stu-id="4b76c-123">DeleteItem</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="4b76c-124">在本文中，您将了解如何通过使用 EWS 托管 API 或 EWS 完成的联系人的批次的基本任务。</span><span class="sxs-lookup"><span data-stu-id="4b76c-124">In this article, you'll learn how to complete basic tasks for batches of contacts by using the EWS Managed API or EWS.</span></span>
  
## <a name="create-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4b76c-125">通过使用 EWS 托管 API 批次中创建联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-125">Create contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4b76c-126"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-126"></span></span>

<span data-ttu-id="4b76c-127">下面的示例中所示，可以创建批次中使用 EWS 托管 API [CreateItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)方法的联系人。</span><span class="sxs-lookup"><span data-stu-id="4b76c-127">You can create contacts in batches by using the EWS Managed API [CreateItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="4b76c-128">本示例创建三个[联系人](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx)对象本地，将每个联系人添加到集合中，然后调用**CreateItems**方法在联系人的集合。</span><span class="sxs-lookup"><span data-stu-id="4b76c-128">This example creates three [Contact](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) objects locally, adds each contact to a collection, then calls the **CreateItems** method on the collection of contacts.</span></span> 
  
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

## <a name="create-contacts-in-batches-by-using-ews"></a><span data-ttu-id="4b76c-129">通过使用 EWS 批次中创建联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-129">Create contacts in batches by using EWS</span></span>
<span data-ttu-id="4b76c-130"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-130"></span></span>

<span data-ttu-id="4b76c-131">您可以通过使用[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS 操作的批次中创建联系人下面的代码示例中所示。</span><span class="sxs-lookup"><span data-stu-id="4b76c-131">You can create contacts in batches by using the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="4b76c-132">这也是 EWS 托管 API 时您使用 EWS 托管 API 创建[批次中的联系人](#bk_EWSMA)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="4b76c-132">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [create contacts in batches](#bk_EWSMA).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="4b76c-133">服务器对每个新联系人，这表明已创建的每个联系人，并已将其保存包括**NoError** [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值[CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)消息的**CreateItem**请求的响应成功。</span><span class="sxs-lookup"><span data-stu-id="4b76c-133">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new contacts, which indicates that each contact was created and saved successfully.</span></span> 
  
## <a name="get-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4b76c-134">通过使用 EWS 托管 API 获取批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-134">Get contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4b76c-135"><a name="bk_EWSMAGet"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-135"></span></span>

<span data-ttu-id="4b76c-136">您可以通过使用 EWS 托管 API [BindToItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx)方法的批次中获取联系人下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="4b76c-136">You can get contacts in batches by using the EWS Managed API [BindToItems](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="4b76c-137">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4b76c-137">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="get-contacts-in-batches-by-using-ews"></a><span data-ttu-id="4b76c-138">通过使用 EWS 获取批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-138">Get contacts in batches by using EWS</span></span>
<span data-ttu-id="4b76c-139"><a name="bk_EWSMAGet"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-139"></span></span>

<span data-ttu-id="4b76c-140">您可以通过在下面的示例使用[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作和代码批次中获取联系人。</span><span class="sxs-lookup"><span data-stu-id="4b76c-140">You can get contacts in batches by using the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation and the code in the following example.</span></span> <span data-ttu-id="4b76c-141">这也是 EWS 托管 API 时您使用 EWS 托管 API[获取批次中的联系人](#bk_EWSMAGet)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="4b76c-141">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get contacts in batches](#bk_EWSMAGet).</span></span> <span data-ttu-id="4b76c-142">为便于阅读缩短了**ItemId**属性。</span><span class="sxs-lookup"><span data-stu-id="4b76c-142">The **ItemId** attribute has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="4b76c-143">服务器响应**GetItem**请求[GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件包含 ID 和的每个请求的联系人的显示名称。</span><span class="sxs-lookup"><span data-stu-id="4b76c-143">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes the ID and the display name for each of the requested contacts.</span></span> 
  
## <a name="update-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4b76c-144">使用 EWS 托管 API 更新批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-144">Update contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4b76c-145"><a name="bk_EWSMAUpdate"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-145"></span></span>

<span data-ttu-id="4b76c-146">下面的示例中所示，您可以通过使用 EWS 托管 API [UpdateItems](http://msdn.microsoft.com/zh-cn/library/dd634705%28v=exchg.80%29.aspx)方法中，更新批次中的联系人。</span><span class="sxs-lookup"><span data-stu-id="4b76c-146">You can update contacts in batches by using the EWS Managed API [UpdateItems](http://msdn.microsoft.com/zh-cn/library/dd634705%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> <span data-ttu-id="4b76c-147">上面的示例创建该联系人，但不指定他们的工作。</span><span class="sxs-lookup"><span data-stu-id="4b76c-147">The previous example creates the contact but does not specify who they work for.</span></span> <span data-ttu-id="4b76c-148">可以在此示例中使用代码更新所有联系人同时包括其公司名称。</span><span class="sxs-lookup"><span data-stu-id="4b76c-148">You can use the code in this example to update all your contacts at once to include their company name.</span></span> 
  
<span data-ttu-id="4b76c-149">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4b76c-149">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="update-contacts-in-batches-by-using-ews"></a><span data-ttu-id="4b76c-150">使用 EWS 更新批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-150">Update contacts in batches by using EWS</span></span>
<span data-ttu-id="4b76c-151"><a name="bk_EWSMAUpdate"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-151"></span></span>

<span data-ttu-id="4b76c-152">下面的代码示例中所示，您可以通过使用[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS 操作，更新批次中的联系人。</span><span class="sxs-lookup"><span data-stu-id="4b76c-152">You can update contacts in batches by using the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation, as shown in following code example.</span></span> <span data-ttu-id="4b76c-153">这也是 EWS 托管 API 时您使用 EWS 托管 API 更新[批次中的联系人](#bk_EWSMAUpdate)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="4b76c-153">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [update contacts in batches](#bk_EWSMAUpdate).</span></span> <span data-ttu-id="4b76c-154">为便于阅读缩短了**ItemId**属性。</span><span class="sxs-lookup"><span data-stu-id="4b76c-154">The **ItemId** attribute has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="4b76c-155">服务器响应**UpdateItem**请求使用[UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx)消息，其中包括[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError**，这表明，每个更新已成功保存在服务器上的值。</span><span class="sxs-lookup"><span data-stu-id="4b76c-155">The server responds to the **UpdateItem** request with an [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that each of the updates was saved successfully on the server.</span></span> <span data-ttu-id="4b76c-156">[ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx)元素中报告的所有冲突。</span><span class="sxs-lookup"><span data-stu-id="4b76c-156">Any conflicts are reported in the [ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) element.</span></span> 
  
## <a name="delete-contacts-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="4b76c-157">使用 EWS 托管 API 删除批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-157">Delete contacts in batches by using the EWS Managed API</span></span>
<span data-ttu-id="4b76c-158"><a name="bk_EWSMADelete"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-158"></span></span>

<span data-ttu-id="4b76c-159">下面的示例中所示，您可以使用[DeleteItems](http://msdn.microsoft.com/zh-cn/library/dd635460%28v=exchg.80%29.aspx) EWS 托管 API 方法中，删除批次中的联系人。</span><span class="sxs-lookup"><span data-stu-id="4b76c-159">You can delete contacts in batches by using the [DeleteItems](http://msdn.microsoft.com/zh-cn/library/dd635460%28v=exchg.80%29.aspx) EWS Managed API method, as shown in the following example.</span></span> <span data-ttu-id="4b76c-160">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="4b76c-160">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="delete-contacts-in-batches-by-using-ews"></a><span data-ttu-id="4b76c-161">使用 EWS 删除批次中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-161">Delete contacts in batches by using EWS</span></span>
<span data-ttu-id="4b76c-162"><a name="bk_EWSMADelete"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-162"></span></span>

<span data-ttu-id="4b76c-163">下面的代码示例中所示，您可以使用[删除项](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx)EWS 操作中，删除批次中的联系人。</span><span class="sxs-lookup"><span data-stu-id="4b76c-163">You can delete contacts in batches by using the [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="4b76c-164">这也是 EWS 托管 API 时您使用 EWS 托管 API 到[删除批次中的联系人](#bk_EWSMADelete)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="4b76c-164">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [delete contacts in batches](#bk_EWSMADelete).</span></span> <span data-ttu-id="4b76c-165">为便于阅读缩短了**ItemId**属性。</span><span class="sxs-lookup"><span data-stu-id="4b76c-165">The **ItemId** attribute has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope 
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="4b76c-166">服务器响应[DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx)邮件包含已删除的每个项目**NoError** [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**删除项**要求。</span><span class="sxs-lookup"><span data-stu-id="4b76c-166">The server responds to the **DeleteItem** request with a [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each item that was removed.</span></span> <span data-ttu-id="4b76c-167">请注意，此操作还返回成功是否找不到的项 ID。</span><span class="sxs-lookup"><span data-stu-id="4b76c-167">Note that the operation also returns success if the item ID could not be found.</span></span> 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a><span data-ttu-id="4b76c-168">验证批处理已成功完成</span><span class="sxs-lookup"><span data-stu-id="4b76c-168">Verifying that a batch process completed successfully</span></span>
<span data-ttu-id="4b76c-169"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="4b76c-169"></span></span>

<span data-ttu-id="4b76c-170">时无法处理批处理请求中的一个或多个联系人，如请求，每个联系人，失败，则返回错误，并按预期方式处理的批次中的联系人的其他试。</span><span class="sxs-lookup"><span data-stu-id="4b76c-170">When one or more contacts in a batched request can't be processed as requested, an error is returned for each contact that failed, and the rest of the contacts in the batch are processed as expected.</span></span> <span data-ttu-id="4b76c-171">在批处理中可能会出现故障如果项目已删除，因此无法检索到，或更新，或者如果项目移动到另一个文件夹，因此使用新的项目 id，并且不能使用发送的项目 ID 修改。</span><span class="sxs-lookup"><span data-stu-id="4b76c-171">Failures in batch processing can occur if the item was deleted, and therefore can't be retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID, and cannot be modified with the item ID sent.</span></span> <span data-ttu-id="4b76c-172">本节中的信息显示如何获取有关失败的错误详细信息中的联系人的批处理。</span><span class="sxs-lookup"><span data-stu-id="4b76c-172">The information in this section shows how to get error details about failures in batch processing of contacts.</span></span>
  
<span data-ttu-id="4b76c-173">使用 EWS 托管 API 验证成功的批处理过程，您可以检查[ServiceResponseCollection](http://msdn.microsoft.com/zh-cn/library/dd633715%28v=exchg.80%29.aspx)的[OverallResult](http://msdn.microsoft.com/zh-cn/library/dd634515%28v=exchg.80%29.aspx)属性等于[ServiceResult.Success](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4b76c-173">To verify the success of a batch process by using the EWS Managed API, you can check that the [OverallResult](http://msdn.microsoft.com/zh-cn/library/dd634515%28v=exchg.80%29.aspx) property of the [ServiceResponseCollection](http://msdn.microsoft.com/zh-cn/library/dd633715%28v=exchg.80%29.aspx) is equal to [ServiceResult.Success](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="4b76c-174">如果是这样，所有联系人都已成功都处理。</span><span class="sxs-lookup"><span data-stu-id="4b76c-174">If so, all the contacts were processed successfully.</span></span> <span data-ttu-id="4b76c-175">如果**OverallResult**不等于**ServiceResult.Success**，一个或多个联系人未成功处理。</span><span class="sxs-lookup"><span data-stu-id="4b76c-175">If the **OverallResult** is not equal to **ServiceResult.Success**, one or more of the contacts were not processed successfully.</span></span> <span data-ttu-id="4b76c-176">每个**ServiceResponseCollection**中返回的对象包含以下属性：</span><span class="sxs-lookup"><span data-stu-id="4b76c-176">Each of the objects returned in the **ServiceResponseCollection** contains the following properties:</span></span> 
  
- [<span data-ttu-id="4b76c-177">错误代码</span><span class="sxs-lookup"><span data-stu-id="4b76c-177">ErrorCode</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4b76c-178">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="4b76c-178">ErrorDetails</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4b76c-179">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="4b76c-179">ErrorMessage</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4b76c-180">ErrorProperties</span><span class="sxs-lookup"><span data-stu-id="4b76c-180">ErrorProperties</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="4b76c-181">结果</span><span class="sxs-lookup"><span data-stu-id="4b76c-181">Result</span></span>](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
<span data-ttu-id="4b76c-182">这些属性包含有关为什么联系人错误而无法处理所要求的信息。</span><span class="sxs-lookup"><span data-stu-id="4b76c-182">These properties contain information about why the contacts could not be processed as requested.</span></span> <span data-ttu-id="4b76c-183">本文中的示例打印**结果**，**错误代码**，并且每个**ErrorMessage**失败联系人。</span><span class="sxs-lookup"><span data-stu-id="4b76c-183">The examples in this article print out the **Result**, **ErrorCode**, and **ErrorMessage** for each failed contact.</span></span> <span data-ttu-id="4b76c-184">您可以使用这些结果调查问题。</span><span class="sxs-lookup"><span data-stu-id="4b76c-184">You can use these results to investigate the issue.</span></span> 
  
<span data-ttu-id="4b76c-185">Ews，若要验证成功批处理过程，检查正在处理每个项目的[ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="4b76c-185">For EWS, to verify the success of a batched process, check the [ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) attribute for each item being processed.</span></span> <span data-ttu-id="4b76c-186">下面是**ResponseMessageType**，派生的所有响应消息的基类型的基本结构。</span><span class="sxs-lookup"><span data-stu-id="4b76c-186">The following is the basic structure of the **ResponseMessageType**, the base type from which all response messages are derived.</span></span> 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

<span data-ttu-id="4b76c-187">如果联系人未成功处理**ResponseClass**属性设置为**成功**如果已成功处理该联系人或**错误**。</span><span class="sxs-lookup"><span data-stu-id="4b76c-187">The **ResponseClass** attribute is set to **Success** if the contact was processed successfully, or **Error** if the contact was not processed successfully.</span></span> <span data-ttu-id="4b76c-188">为联系人，不会批处理过程中遇到**警告**。</span><span class="sxs-lookup"><span data-stu-id="4b76c-188">For contacts, you will not encounter a **Warning** during batch processing.</span></span> <span data-ttu-id="4b76c-189">如果**ResponseClass**为**成功**，后面的[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素也始终设置为**NoError**。</span><span class="sxs-lookup"><span data-stu-id="4b76c-189">If the **ResponseClass** is **Success**, the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element that follows is also always set to **NoError**.</span></span> <span data-ttu-id="4b76c-190">如果**ResponseClass** **错误**，您需要检查[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)、 **ResponseCode**和[MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx)元素以确定问题的原因的值。</span><span class="sxs-lookup"><span data-stu-id="4b76c-190">If the **ResponseClass** is **Error**, you need to check the values of the [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**, and [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) elements to determine what caused the problem.</span></span> <span data-ttu-id="4b76c-191">当前未使用[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="4b76c-191">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) is currently unused.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4b76c-192">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b76c-192">See also</span></span>


- [<span data-ttu-id="4b76c-193">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="4b76c-193">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)
    
- [<span data-ttu-id="4b76c-194">在 Exchange 中使用 EWS 的批次中的过程电子邮件</span><span class="sxs-lookup"><span data-stu-id="4b76c-194">Process email messages in batches by using EWS in Exchange</span></span>](how-to-process-email-messages-in-batches-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="4b76c-195">在 Exchange 处理批次中的日历项目</span><span class="sxs-lookup"><span data-stu-id="4b76c-195">Process calendar items in batches in Exchange</span></span>](how-to-process-calendar-items-in-batches-in-exchange.md)
    

