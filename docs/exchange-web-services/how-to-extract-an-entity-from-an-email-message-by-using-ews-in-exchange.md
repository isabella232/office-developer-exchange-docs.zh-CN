---
title: 在 Exchange 使用 EWS 从电子邮件提取实体
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6396b009-5f6e-41eb-a75a-224d43e864ae
description: 了解如何使用 EWS 托管 API 或 EWS 在 Exchange 中从电子邮件的正文中提取信息。
ms.openlocfilehash: d3d5c4b756347a4cedede184709884d5ed8f08b4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752775"
---
# <a name="extract-an-entity-from-an-email-message-by-using-ews-in-exchange"></a><span data-ttu-id="6b8ac-103">在 Exchange 使用 EWS 从电子邮件提取实体</span><span class="sxs-lookup"><span data-stu-id="6b8ac-103">Extract an entity from an email message by using EWS in Exchange</span></span>

<span data-ttu-id="6b8ac-104">了解如何使用 EWS 托管 API 或 EWS 在 Exchange 中从电子邮件的正文中提取信息。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-104">Learn how to extract information from the body of an email message by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="6b8ac-105">您可以使用 EWS 托管 API 的 EWS 访问地址、 联系人、 电子邮件地址、 会议建议、 电话号码、 任务和 Exchange 服务器中提取电子邮件中的 Url。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-105">You can use the EWS Managed API or EWS to access the addresses, contacts, email addresses, meeting suggestions, phone numbers, tasks, and URLs that an Exchange server extracts from email messages.</span></span> <span data-ttu-id="6b8ac-106">对新应用程序或建议跟进现有应用程序中的操作，然后可以使用此信息。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-106">You can then use this information for new applications or to suggest follow up actions in existing applications.</span></span> <span data-ttu-id="6b8ac-107">例如，如果电子邮件中标识的 contact 实体，会议建议或任务建议，您的应用程序可以建议，创建一个新项预填充的信息。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-107">For example, if a contact entity, meeting suggestion, or task suggestion is identified in an email, your application can suggest that a new item with prepopulated information be created.</span></span> <span data-ttu-id="6b8ac-108">您可以通过使用提取的实体，将大写后面数据用途 — 并帮助用户将其电子邮件消息内容无缝集成到可操作的结果。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-108">By using extracted entities, you can capitalize on the intent behind the data — and help users seamlessly integrate their email message content into actionable results.</span></span>
  
<span data-ttu-id="6b8ac-109">Exchange 存储中的每个项目中已经内置实体提取的地址、 联系人、 电子邮件地址、 会议建议、 电话号码、 任务和 Url。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-109">Entity extraction for addresses, contacts, email addresses, meeting suggestions, phone numbers, tasks, and URLs is already built in to every item in the Exchange store.</span></span> <span data-ttu-id="6b8ac-110">如果您正在使用 EWS 托管 API， [Item.EntityExtractionResult](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx)属性会检索实体为您在[Item.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法调用中。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-110">If you're using the EWS Managed API, the [Item.EntityExtractionResult](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx) property retrieves the entities for you in an [Item.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method call.</span></span> <span data-ttu-id="6b8ac-111">如果您正在使用 EWS， [EntityExtractionResult](http://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx)元素获取您具有[GetItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)操作调用中提取所有实体。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-111">If you're using EWS, the [EntityExtractionResult](http://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx) element gets all the extracted entities for you in a [GetItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation call.</span></span> <span data-ttu-id="6b8ac-112">检索已提取实体的结果后，您可以引导每个实体集收集相关信息。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-112">After you retrieve the results of the extracted entities, you can walk through each entity collection to gather pertinent information.</span></span> <span data-ttu-id="6b8ac-113">例如，如果已提取会议建议，可以检索建议的会议主题、 与会者列表、 开始时间和结束时间。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-113">For example, if a meeting suggestion was extracted, you can retrieve the suggested meeting subject, attendee list, start time, and end time.</span></span> 
  
<span data-ttu-id="6b8ac-114">**表 1。EWS 托管 API 属性和包含提取的实体的 EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="6b8ac-114">**Table 1. EWS Managed API properties and EWS elements that contain extracted entities**</span></span>

|<span data-ttu-id="6b8ac-115">**提取的实体**</span><span class="sxs-lookup"><span data-stu-id="6b8ac-115">**Extracted entity**</span></span>|<span data-ttu-id="6b8ac-116">**EWS 托管 API 属性**</span><span class="sxs-lookup"><span data-stu-id="6b8ac-116">**EWS Managed API property**</span></span>|<span data-ttu-id="6b8ac-117">**EWS 元素**</span><span class="sxs-lookup"><span data-stu-id="6b8ac-117">**EWS element**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b8ac-118">地址</span><span class="sxs-lookup"><span data-stu-id="6b8ac-118">Addresses</span></span>  <br/> |[<span data-ttu-id="6b8ac-119">EntityExtractionResult.Addresses</span><span class="sxs-lookup"><span data-stu-id="6b8ac-119">EntityExtractionResult.Addresses</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b8ac-120">地址</span><span class="sxs-lookup"><span data-stu-id="6b8ac-120">Addresses</span></span>](http://msdn.microsoft.com/library/0c1f3fd3-1b78-46ee-8dd4-b2aff51e767e%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="6b8ac-121">联系人</span><span class="sxs-lookup"><span data-stu-id="6b8ac-121">Contacts</span></span>  <br/> |[<span data-ttu-id="6b8ac-122">EntityExtractionResult.Contacts</span><span class="sxs-lookup"><span data-stu-id="6b8ac-122">EntityExtractionResult.Contacts</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.entityextractionresult.contacts%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b8ac-123">联系人</span><span class="sxs-lookup"><span data-stu-id="6b8ac-123">Contacts</span></span>](http://msdn.microsoft.com/library/a2c1e833-5f8c-438d-bad7-bb5dcc29ca9e%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="6b8ac-124">电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="6b8ac-124">Email addresses</span></span>  <br/> |[<span data-ttu-id="6b8ac-125">EntityExtractionResult.EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="6b8ac-125">EntityExtractionResult.EmailAddresses</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.entityextractionresult.emailaddresses%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b8ac-126">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="6b8ac-126">EmailAddresses</span></span>](http://msdn.microsoft.com/library/2fc4a8e8-5377-4059-8fb4-3fdabfd30fe3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="6b8ac-127">会议建议</span><span class="sxs-lookup"><span data-stu-id="6b8ac-127">Meeting suggestions</span></span>  <br/> |[<span data-ttu-id="6b8ac-128">EntityExtractionResult.MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="6b8ac-128">EntityExtractionResult.MeetingSuggestions</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.entityextractionresult.meetingsuggestions%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b8ac-129">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="6b8ac-129">MeetingSuggestions</span></span>](http://msdn.microsoft.com/library/c99e9a60-9e38-425d-ad03-47c8917f41da%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="6b8ac-130">电话号码</span><span class="sxs-lookup"><span data-stu-id="6b8ac-130">Phone numbers</span></span>  <br/> |[<span data-ttu-id="6b8ac-131">EntityExtractionResult.PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="6b8ac-131">EntityExtractionResult.PhoneNumbers</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.entityextractionresult.phonenumbers%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b8ac-132">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="6b8ac-132">PhoneNumbers</span></span>](http://msdn.microsoft.com/library/9ff6ae98-34a1-47f7-bde5-608251a789f7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="6b8ac-133">任务建议</span><span class="sxs-lookup"><span data-stu-id="6b8ac-133">Task suggestions</span></span>  <br/> |[<span data-ttu-id="6b8ac-134">EntityExtractionResult.TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="6b8ac-134">EntityExtractionResult.TaskSuggestions</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b8ac-135">TaskSuggestions</span><span class="sxs-lookup"><span data-stu-id="6b8ac-135">TaskSuggestions</span></span>](http://msdn.microsoft.com/library/7d3c6314-2a5c-4fc3-b5f9-ae6d4946aac3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="6b8ac-136">URL</span><span class="sxs-lookup"><span data-stu-id="6b8ac-136">URLs</span></span>  <br/> |[<span data-ttu-id="6b8ac-137">EntityExtractionResult.Urls</span><span class="sxs-lookup"><span data-stu-id="6b8ac-137">EntityExtractionResult.Urls</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="6b8ac-138">Urls</span><span class="sxs-lookup"><span data-stu-id="6b8ac-138">Urls</span></span>](http://msdn.microsoft.com/library/c39744ea-0cee-4954-8653-8279d6b10161%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="6b8ac-139">由于实体提取依赖于自然语言识别，可能非确定性的实体的识别和成功有时依赖的上下文。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-139">Because entity extraction relies on natural language recognition, the recognition of entities can be non-deterministic and success sometimes relies on the context.</span></span> <span data-ttu-id="6b8ac-140">若要演示自然语言中识别的工作原理，本文中的示例时，可使用以下电子邮件作为输入。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-140">To demonstrate how natural language recognition works, the examples in this article use the following email as input.</span></span>
  
 `From: Ronnie Sturgis`
  
 `To: Sadie Daniels`
  
 `Subject: Dinner party`
  
 `Hi Sadie`
  
 `Are you free this Friday at 7 to join us for a dinner party at our house?`
  
 `We're at 789 International Blvd, St Paul MN 55104.`
  
 `Our number is 612-555-0158 if you have trouble finding it.`
  
 `Please RSVP to either myself or Mara (mara@contoso.com) before Friday morning. Best for you organics (http://www.bestforyouorganics.com) will be catering so we can fully enjoy ourselves!`
  
 `Also, can you forward this to Magdalena? I don't have her contact information.`
  
 `See you then!`
  
 `Ronnie`
  
## <a name="extract-all-entities-from-an-email-by-using-the-ews-managed-api"></a><span data-ttu-id="6b8ac-141">从电子邮件中提取所有实体，通过使用 EWS 托管 API</span><span class="sxs-lookup"><span data-stu-id="6b8ac-141">Extract all entities from an email by using the EWS Managed API</span></span>
<span data-ttu-id="6b8ac-142"><a name="bk_extractewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="6b8ac-142"></span></span>

<span data-ttu-id="6b8ac-143">下面的代码示例演示如何显示提取的服务器上，通过使用[Item.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法，并通过提取的实体及其属性的每个然后枚举中的所有实体。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-143">The following code example shows how to display all the entities extracted by the server, by using the [Item.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method, and then enumerating through each of the extracted entities and their properties.</span></span> 
  
<span data-ttu-id="6b8ac-144">本示例假定**服务**是有效的[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且该**ItemId**是[Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)的电子邮件移动或复制。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-144">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, and that **ItemId** is the [Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the email message to move or copy.</span></span> 
  
```cs
public static void ExtractEntities(ExchangeService service, ItemId ItemId)
{
    // Create a property set that limits the properties returned 
    // by the Bind method to only those that are required.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.EntityExtractionResult);
    // Get the item from the server.
    // This method call results in an GetItem call to EWS.
    Item item = Item.Bind(service, ItemId, propSet);
    Console.WriteLine("The following entities have been extracted from the message:");
    Console.WriteLine(" ");
    // If address entities are extracted from the message, print the results.
    if (item.EntityExtractionResult != null)
    {
        if (item.EntityExtractionResult.Addresses != null)
        {
            Console.WriteLine("--------------------Addresses---------------------------");
            foreach (AddressEntity address in item.EntityExtractionResult.Addresses)
            {
                Console.WriteLine("Address: {0}", address.Address);
            }
            Console.WriteLine(" ");
        }
        // If contact entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.Contacts != null)
        {
            Console.WriteLine("--------------------Contacts----------------------------");
            foreach (ContactEntity contact in item.EntityExtractionResult.Contacts)
            {
                Console.WriteLine("Addresses:       {0}", contact.Addresses);
                Console.WriteLine("Business name:   {0}", contact.BusinessName);
                Console.WriteLine("Contact string:  {0}", contact.ContactString);
                Console.WriteLine("Email addresses: {0}", contact.EmailAddresses);
                Console.WriteLine("Person name:     {0}", contact.PersonName);
                Console.WriteLine("Phone numbers:   {0}", contact.PhoneNumbers);
                Console.WriteLine("URLs:            {0}", contact.Urls);
            }
            Console.WriteLine(" ");
        }
        // If email address entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.EmailAddresses != null)
        {
            Console.WriteLine("--------------------Email addresses---------------------");
            foreach (EmailAddressEntity email in item.EntityExtractionResult.EmailAddresses)
            {
                Console.WriteLine("Email addresses: {0}", email.EmailAddress);
            }
            Console.WriteLine(" ");
        }
        // If meeting suggestion entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.MeetingSuggestions != null)
        {
            Console.WriteLine("--------------------Meeting suggestions-----------------");
            foreach (MeetingSuggestion meetingSuggestion in item.EntityExtractionResult.MeetingSuggestions)
            {
                Console.WriteLine("Meeting subject:  {0}", meetingSuggestion.Subject);
                Console.WriteLine("Meeting string:   {0}", meetingSuggestion.MeetingString);
                foreach (EmailUserEntity attendee in meetingSuggestion.Attendees)
                {
                    Console.WriteLine("Attendee name:    {0}", attendee.Name);
                    Console.WriteLine("Attendee user ID: {0}", attendee.UserId);
                }
                Console.WriteLine("Start time:       {0}", meetingSuggestion.StartTime);
                Console.WriteLine("End time:         {0}", meetingSuggestion.EndTime);
                Console.WriteLine("Location:         {0}", meetingSuggestion.Location);
            }
            Console.WriteLine(" ");
        }
        // If phone number entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.PhoneNumbers != null)
        {
            Console.WriteLine("--------------------Phone numbers-----------------------");
            foreach (PhoneEntity phone in item.EntityExtractionResult.PhoneNumbers)
            {
                Console.WriteLine("Original phone string:  {0}", phone.OriginalPhoneString);
                Console.WriteLine("Phone string:           {0}", phone.PhoneString);
                Console.WriteLine("Type:                   {0}", phone.Type);
            }
            Console.WriteLine(" ");
        }
        // If task suggestion entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.TaskSuggestions != null)
        {
            Console.WriteLine("--------------------Task suggestions--------------------");
            foreach (TaskSuggestion task in item.EntityExtractionResult.TaskSuggestions)
            {
                foreach (EmailUserEntity assignee in task.Assignees)
                {
                    Console.WriteLine("Assignee name:    {0}", assignee.Name);
                    Console.WriteLine("Assignee user ID: {0}", assignee.UserId);
                }
                Console.WriteLine("Task string:      {0}", task.TaskString);
            }
            Console.WriteLine(" ");
        }
        // If URL entities are extracted from the message, print the results.
        if (item.EntityExtractionResult.Urls != null)
        {
            Console.WriteLine("--------------------URLs--------------------------------");
            foreach (UrlEntity url in item.EntityExtractionResult.Urls)
            {
                Console.WriteLine("URL: {0}", url.Url);
            }
            Console.WriteLine(" ");
        }
    }
    // If no entities are extracted from the message, print the result.
    else if (item.EntityExtractionResult == null)
    {
        Console.WriteLine("No entities extracted");
    }
}
```

<span data-ttu-id="6b8ac-145">在控制台上显示以下输出。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-145">The following output is displayed on the console.</span></span>
  
```text
The following entities have been extracted from the message:
 
--------------------Addresses---------------------------
Address: 789 International Blvd, St Paul MN 55104
 
--------------------Contacts----------------------------
Addresses:       
Business name:   
Contact string:  Mara (mara@contoso.com)
Email addresses: mara@contoso.com
Person name:     Mara
Phone numbers:   
URLs:            
 
--------------------Email addresses---------------------
Email addresses: mara@contoso.com
 
--------------------Meeting suggestions-----------------
Meeting subject:  dinner party
Meeting string:   Are you free this Friday at 7 to join us for a dinner party at our house?
Attendee name:    Ronnie Sturgis
Attendee user ID: ronnie@contoso.com
Attendee name:    Sadie Daniels
Attendee user ID: sadie@cntoso.com
Start time:       10/1/0104 2:00:00 PM
End time:         10/1/0104 2:30:00 PM
Location:         
 
--------------------Phone numbers-----------------------
Original phone string:  612-555-0158
Phone string:           6125550158
Type:                   Unspecified
 
--------------------Task suggestions--------------------
Assignee name:    Sadie Daniels
Assignee user ID: sadie@contoso.com
Task string:      Also, can you forward this to Magdalena?
 
--------------------URLs--------------------------------
URL: http://www.bestforyouorganics.com
```

<span data-ttu-id="6b8ac-146">请注意预期的提取所有地址、 联系人、 电子邮件地址、 电话号码、 任务和 Url。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-146">Notice that all addresses, contacts, email addresses, phone numbers, tasks, and URLs were extracted as expected.</span></span> <span data-ttu-id="6b8ac-147">但是，会议建议，是更复杂的。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-147">The meeting suggestion, however, is a bit more complex.</span></span> <span data-ttu-id="6b8ac-148">注意的开始时间和会议建议结束时间的是不是您可能预期。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-148">Notice the start time and end time of the meeting suggestion are not what you might expect.</span></span> <span data-ttu-id="6b8ac-149">电子邮件中的开始时间"7 在此星期五"，但在开始时间值的已提取处于 10/1/0104年 2:00:00。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-149">The start time in the email is "this Friday at 7", but the extracted value for the start time is 10/1/0104 2:00:00 PM.</span></span> <span data-ttu-id="6b8ac-150">这是因为的开始时间和结束时间服务器提取经过编码的日期。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-150">This is because the start time and end time extracted by the server are encoded dates.</span></span> <span data-ttu-id="6b8ac-151">有关如何解释会议建议中的**日期时间**值的详细信息，请参阅[[MS OXCEXT]: 客户端扩展消息对象协议](http://msdn.microsoft.com/zh-cn/library/hh968601%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-151">For more information about how to interpret **dateTime** values in meeting suggestions, see [[MS-OXCEXT]: Client Extension Message Object Protocol](http://msdn.microsoft.com/zh-cn/library/hh968601%28v=exchg.80%29.aspx).</span></span>
  
## <a name="extract-all-entities-from-an-email-by-using-ews"></a><span data-ttu-id="6b8ac-152">通过使用 EWS 从电子邮件中提取所有实体</span><span class="sxs-lookup"><span data-stu-id="6b8ac-152">Extract all entities from an email by using EWS</span></span>
<span data-ttu-id="6b8ac-153"><a name="bk_extractews"> </a></span><span class="sxs-lookup"><span data-stu-id="6b8ac-153"></span></span>

<span data-ttu-id="6b8ac-154">下面的代码示例演示如何使用[GetItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)操作和[EntityExtractionResult](http://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx)元素从项目中检索的已提取的实体。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-154">The following code example shows how to use the [GetItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) operation and the [EntityExtractionResult](http://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx) element to retrieve the extracted entities from an item.</span></span> 
  
<span data-ttu-id="6b8ac-155">这也是 XML 请求发送的 EWS 托管 API 时您使用**绑定**到[提取所有实体使用 EWS 托管 API 电子邮件从](#bk_extractewsma)方法。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-155">This is also the XML request that is sent by the EWS Managed API when you use the **Bind** method to [Extract all entities from an email by using the EWS Managed API](#bk_extractewsma).</span></span>
  
<span data-ttu-id="6b8ac-156">为便于阅读将被截[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-156">The value of the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) element is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:EntityExtractionResult" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="sVC5AAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

服务器响应包含[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，这表明已成功检索电子邮件的[GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)消息的**GetItem**请求。 <span data-ttu-id="6b8ac-158">响应还包括**EntityExtractionResult**为每个已提取实体。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-158">The response also includes the **EntityExtractionResult** for each extracted entity.</span></span> 
  
<span data-ttu-id="6b8ac-159">为便于阅读将被截**ItemId**元素的值。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-159">The value of the **ItemId** element is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="883"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="sVC5AAA="
                        ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAOOqJN" />
              <t:EntityExtractionResult>
                <t:Addresses>
                  <t:AddressEntity>
                    <t:Position>LatestReply</t:Position>
                    <t:Address>789 International Blvd, St Paul MN 55104</t:Address>
                  </t:AddressEntity>
                </t:Addresses>
                <t:MeetingSuggestions>
                  <t:MeetingSuggestion>
                    <t:Position>LatestReply</t:Position>
                    <t:Attendees>
                      <t:EmailUser>
                        <t:Name>Ronnie Sturgis</t:Name>
                        <t:UserId>ronnie@contoso.com</t:UserId>
                      </t:EmailUser>
                      <t:EmailUser>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:UserId>sadie@contoso.com</t:UserId>
                      </t:EmailUser>
                    </t:Attendees>
                    <t:Subject>dinner party</t:Subject>
                    <t:MeetingString>Are you free this Friday at 7 to join us for a dinner party at our house?</t:MeetingString>
                    <t:StartTime>0104-10-01T19:00:00Z</t:StartTime>
                    <t:EndTime>0104-10-01T19:30:00Z</t:EndTime>
                  </t:MeetingSuggestion>
                </t:MeetingSuggestions>
                <t:TaskSuggestions>
                  <t:TaskSuggestion>
                    <t:Position>LatestReply</t:Position>
                    <t:TaskString>Also, can you forward this to Magdalena?</t:TaskString>
                    <t:Assignees>
                      <t:EmailUser>
                        <t:Name>Sadie Daniels</t:Name>
                        <t:UserId>sadie@contoso.com</t:UserId>
                      </t:EmailUser>
                    </t:Assignees>
                  </t:TaskSuggestion>
                </t:TaskSuggestions>
                <t:EmailAddresses>
                  <t:EmailAddressEntity>
                    <t:Position>LatestReply</t:Position>
                    <t:EmailAddress>mara@contoso.com</t:EmailAddress>
                  </t:EmailAddressEntity>
                </t:EmailAddresses>
                <t:Contacts>
                  <t:Contact>
                    <t:Position>LatestReply</t:Position>
                    <t:PersonName>Mara</t:PersonName>
                    <t:EmailAddresses>
                      <t:EmailAddress>mara@contoso.com</t:EmailAddress>
                    </t:EmailAddresses>
                    <t:ContactString>Mara (mara@contoso.com</t:ContactString>
                  </t:Contact>
                </t:Contacts>
                <t:Urls>
                  <t:UrlEntity>
                    <t:Position>LatestReply</t:Position>
                    <t:Url>http://www.bestforyouorganics.com</t:Url>
                  </t:UrlEntity>
                </t:Urls>
                <t:PhoneNumbers>
                  <t:Phone>
                    <t:Position>LatestReply</t:Position>
                    <t:OriginalPhoneString>612-555-0158</t:OriginalPhoneString>
                    <t:PhoneString>6125550158</t:PhoneString>
                    <t:Type>Unspecified</t:Type>
                  </t:Phone>
                </t:PhoneNumbers>
              </t:EntityExtractionResult>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="6b8ac-160">请注意预期的提取所有地址、 联系人、 电子邮件地址、 电话号码、 任务和 Url。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-160">Notice that all addresses, contacts, email addresses, phone numbers, tasks, and URLs were extracted as expected.</span></span> <span data-ttu-id="6b8ac-161">但是，会议建议，是更复杂的。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-161">The meeting suggestion, however, is a bit more complex.</span></span> <span data-ttu-id="6b8ac-162">注意的开始时间和会议建议结束时间的是不是您可能预期。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-162">Notice the start time and end time of the meeting suggestion are not what you might expect.</span></span> <span data-ttu-id="6b8ac-163">电子邮件中的开始时间"7 在此星期五"，但的开始时间的已提取的值是 10/1/0104年 2:00:00。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-163">The start time in the email was "this Friday at 7", but the extracted value for the start time is 10/1/0104 2:00:00 PM.</span></span> <span data-ttu-id="6b8ac-164">这是因为的开始时间和结束时间服务器提取经过编码的日期。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-164">This is because the start time and end time extracted by the server are encoded dates.</span></span> <span data-ttu-id="6b8ac-165">有关解释会议建议中的**日期时间**值的详细信息，请参阅[[MS OXCEXT]: 客户端扩展消息对象协议](http://msdn.microsoft.com/zh-cn/library/hh968601%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6b8ac-165">For more information about interpreting **dateTime** values in meeting suggestions, see [[MS-OXCEXT]: Client Extension Message Object Protocol](http://msdn.microsoft.com/zh-cn/library/hh968601%28v=exchg.80%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b8ac-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6b8ac-166">See also</span></span>

- [<span data-ttu-id="6b8ac-167">电子邮件和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="6b8ac-167">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
- [<span data-ttu-id="6b8ac-168">Item.EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="6b8ac-168">Item.EntityExtractionResult</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx)    
- [<span data-ttu-id="6b8ac-169">EntityExtractionResult</span><span class="sxs-lookup"><span data-stu-id="6b8ac-169">EntityExtractionResult</span></span>](http://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx)
    

