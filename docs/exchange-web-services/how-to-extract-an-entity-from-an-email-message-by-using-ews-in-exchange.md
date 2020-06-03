---
title: 使用 Exchange 中的 EWS 从电子邮件中提取实体
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 6396b009-5f6e-41eb-a75a-224d43e864ae
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 从电子邮件正文中提取信息。
localization_priority: Priority
ms.openlocfilehash: fb90eb05441667e6b327b09d568117f5040e6fd8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528109"
---
# <a name="extract-an-entity-from-an-email-message-by-using-ews-in-exchange"></a>使用 Exchange 中的 EWS 从电子邮件中提取实体

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 从电子邮件正文中提取信息。
  
可以使用 EWS 托管 API 或 EWS 访问 Exchange server 从电子邮件中提取的地址、联系人、电子邮件地址、会议建议、电话号码、任务和 Url。 然后，可以将此信息用于新的应用程序或建议在现有应用程序中执行后续操作。 例如，如果电子邮件中标识了联系人实体、会议建议或任务建议，则应用程序可以建议创建具有预填充信息的新项目。 通过使用提取的实体，可以实现数据的用途，并帮助用户将其电子邮件内容无缝集成到可操作的结果中。
  
地址、联系人、电子邮件地址、会议建议、电话号码、任务和 Url 的实体提取已内置到 Exchange 存储中的每个项目中。 如果您使用的是 EWS 托管 API，则[EntityExtractionResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx)属性在项目中检索实体。[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法调用。 如果使用 EWS，则[EntityExtractionResult](https://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx)元素将在[GetItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)操作调用中获取所有提取的实体。 检索提取的实体的结果后，可以遍历每个实体集合以收集相关信息。 例如，如果已提取会议建议，则可以检索建议的会议主题、与会者列表、开始时间和结束时间。 
  
**表1。包含提取实体的 EWS 托管 API 属性和 EWS 元素**

|**提取的实体**|**EWS 托管 API 属性**|**EWS 元素**|
|:-----|:-----|:-----|
|地址  <br/> |[EntityExtractionResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[地址](https://msdn.microsoft.com/library/0c1f3fd3-1b78-46ee-8dd4-b2aff51e767e%28Office.15%29.aspx) <br/> |
|联系人  <br/> |[EntityExtractionResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.contacts%28v=exchg.80%29.aspx) <br/> |[联系人](https://msdn.microsoft.com/library/a2c1e833-5f8c-438d-bad7-bb5dcc29ca9e%28Office.15%29.aspx) <br/> |
|电子邮件地址  <br/> |[EntityExtractionResult。 EmailAddresses](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.emailaddresses%28v=exchg.80%29.aspx) <br/> |[EmailAddresses](https://msdn.microsoft.com/library/2fc4a8e8-5377-4059-8fb4-3fdabfd30fe3%28Office.15%29.aspx) <br/> |
|会议建议  <br/> |[EntityExtractionResult。 MeetingSuggestions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.meetingsuggestions%28v=exchg.80%29.aspx) <br/> |[MeetingSuggestions](https://msdn.microsoft.com/library/c99e9a60-9e38-425d-ad03-47c8917f41da%28Office.15%29.aspx) <br/> |
|电话号码  <br/> |[EntityExtractionResult。 PhoneNumbers](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.phonenumbers%28v=exchg.80%29.aspx) <br/> |[PhoneNumbers](https://msdn.microsoft.com/library/9ff6ae98-34a1-47f7-bde5-608251a789f7%28Office.15%29.aspx) <br/> |
|任务建议  <br/> |[EntityExtractionResult。 TaskSuggestions](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[TaskSuggestions](https://msdn.microsoft.com/library/7d3c6314-2a5c-4fc3-b5f9-ae6d4946aac3%28Office.15%29.aspx) <br/> |
|URL  <br/> |[EntityExtractionResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.entityextractionresult.addresses%28v=exchg.80%29.aspx) <br/> |[Urls](https://msdn.microsoft.com/library/c39744ea-0cee-4954-8653-8279d6b10161%28Office.15%29.aspx) <br/> |
   
由于实体提取依赖于自然语言识别，因此实体的识别可以是非确定性的，且成功有时依赖上下文。 为了演示自然语言识别的工作方式，本文中的示例使用以下电子邮件作为输入。
  
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
  
## <a name="extract-all-entities-from-an-email-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 从电子邮件中提取所有实体
<a name="bk_extractewsma"> </a>

下面的代码示例演示如何使用[Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx)方法显示服务器提取的所有实体，然后枚举每个提取的实体及其属性。 
  
此示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且**ItemId**是要移动或复制的电子邮件的[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) 。 
  
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

控制台上显示以下输出。
  
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

请注意，所有地址、联系人、电子邮件地址、电话号码、任务和 Url 都按预期方式提取。 但是，会议建议更复杂一些。 请注意会议建议的开始时间和结束时间不是你预期的。 电子邮件中的开始时间是 "此星期五位于 7"，但起始时间的提取值为 10/1/0104 2:00:00 PM。 这是因为服务器提取的开始时间和结束时间是经过编码的日期。 有关如何解释会议建议中的**日期时间**值的详细信息，请参阅[[MS-OXCEXT]：客户端扩展邮件对象协议](https://msdn.microsoft.com/library/hh968601%28v=exchg.80%29.aspx)。
  
## <a name="extract-all-entities-from-an-email-by-using-ews"></a>使用 EWS 从电子邮件中提取所有实体
<a name="bk_extractews"> </a>

下面的代码示例演示如何使用[GetItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx)操作和[EntityExtractionResult](https://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx)元素从项中检索提取的实体。 
  
这也是在使用[Ews 托管 api 从电子邮件中提取所有实体](#bk_extractewsma)时，由**Bind** EWS 托管 api 发送的 XML 请求。
  
为了提高可读性， [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值被缩短。 
  
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

服务器使用[GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx)邮件响应**GetItem**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)值**NoError**，表示电子邮件已成功检索。 该响应还包括每个提取的实体的**EntityExtractionResult** 。 
  
为了提高可读性， **ItemId**元素的值被缩短。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="883"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

请注意，所有地址、联系人、电子邮件地址、电话号码、任务和 Url 都按预期方式提取。 但是，会议建议更复杂一些。 请注意会议建议的开始时间和结束时间不是你预期的。 电子邮件中的开始时间是 "此星期五（位于7日）"，但起始时间的提取值为 10/1/0104 2:00:00 PM。 这是因为服务器提取的开始时间和结束时间是经过编码的日期。 有关解释会议建议中的**日期时间**值的详细信息，请参阅[[MS-OXCEXT]：客户端扩展邮件对象协议](https://msdn.microsoft.com/library/hh968601%28v=exchg.80%29.aspx)。
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的电子邮件和 EMS](email-and-ews-in-exchange.md)
- [EntityExtractionResult](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.entityextractionresult%28v=exchg.80%29.aspx)    
- [EntityExtractionResult](https://msdn.microsoft.com/library/643b99ab-ff90-4411-864c-1077623028d6%28Office.15%29.aspx)
    

