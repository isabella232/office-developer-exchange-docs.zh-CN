---
title: 使用电子邮件代理中的 EWS 访问电子邮件Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: 了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 代理访问电子邮件。
ms.openlocfilehash: aa921bc36004b3a26caa514390e52249021b304f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521212"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a>使用电子邮件代理中的 EWS 访问电子邮件Exchange

了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 代理访问电子邮件。
  
可以使用 EWS 托管 API 或 EWS 向用户委派授予对邮箱所有者的"收件箱"文件夹的访问权限。 然后，代理可以代表邮箱所有者创建会议请求、搜索电子邮件，以及检索、更新和删除邮箱所有者的"收件箱"文件夹中的电子邮件，具体取决于其权限。
  
作为代理，您可以使用相同的方法和操作来访问邮箱所有者的收件箱文件夹，该文件夹用于访问收件箱文件夹，而无需委派访问权限。 主要区别在于，您必须使用显式访问来查找[](delegate-access-and-ews-in-exchange.md#bk_explicit)或创建电子邮件项目，然后在标识项目 ID 后，您可以使用隐式访问获取、更新或删除该项目。 [](delegate-access-and-ews-in-exchange.md#bk_implicit) 
  
**表 1.用于代理访问电子邮件的 EWS 托管 API 方法和 EWS 操作**

|**如果你想要...**|**使用此 EWS 托管 API 方法...**|**使用此 EWS 操作...**|
|:-----|:-----|:-----|
|创建并发送代理电子邮件  <br/> |[EmailMessage.Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) 其中 [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) 参数 [提供对](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) 邮箱所有者的"草稿"文件夹的显式访问  <br/> [EmailMessage.SendAndSaveCopy，](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx)[其中 FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数[提供对](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的"已发送邮件"文件夹的显式访问  <br/> |[CreateItem，](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)[其中 Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> [SendItem，](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx)[其中 Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|创建多个电子邮件作为代理  <br/> |[ExchangeService.CreateItems，](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)**其中 FolderId** 参数 [提供对](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的收件箱文件夹的显式访问  <br/> |[CreateItem，](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)[其中 Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|搜索或查找代理电子邮件  <br/> |[ExchangeService.FindItems，](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)**其中 FolderId** 参数 [提供对](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)邮箱所有者的收件箱文件夹的显式访问  <br/> |[FindItem，](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)[其中 Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|获取代理电子邮件  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|作为代理更新电子邮件  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 后跟 [EmailMessage.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) 后跟 [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|删除代理电子邮件  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 后跟 [EmailMessage.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) 后跟 [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
以代理方式使用电子邮件时，请记住以下事项：
  
- 如果代理只需要处理会议请求和响应，则代理不需要访问"收件箱"文件夹。 有关详细信息，请参阅以委派 [访问日历的先决条件任务](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq)。
    
- 当收件人收到代表邮箱所有者发送的邮件时，发件人将显示为"代表邮箱所有者 *的代理"。*  
    
> [!NOTE]
> 在本文的代码示例中，primary@contoso.com 是邮箱所有者。 
  
## <a name="prerequisite-tasks"></a>先决条件任务
<a name="bk_prereq"> </a>

用户必须先添加为具有邮箱所有者收件箱文件夹权限的代理，用户才能作为代理访问邮箱所有者[](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)的收件箱文件夹。 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建并发送代理电子邮件
<a name="bk_createewsma"> </a>

通过 EWS 托管 API，您可以使用代理用户的服务对象代表邮箱所有者创建和发送电子邮件。 本示例演示如何使用 [Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) 方法将邮件保存在邮箱所有者的"草稿"文件夹中，然后使用 [SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) 方法发送邮件并将邮件保存在邮箱所有者的"已发送邮件"文件夹中。 
  
本示例假定服务是代理的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且代理已被授予邮箱所有者的收件箱、草稿和已发送邮件文件夹的适当[权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)。
  
```cs
public static void DelegateAccessCreateEmail(ExchangeService service)
{
    // Create an email message and provide it with connection 
    // configuration information by using an ExchangeService 
    // object named service.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Company Soccer Team";
    message.Body = "Are you interested in joining?";
    message.ToRecipients.Add("sadie@contoso.com");
    // Save the email to the mailbox owner's Drafts folder.
    // This method call results in a CreateItem call to EWS.
    // The FolderId parameter contains the context for the 
    // mailbox owner's Inbox folder. Any additional actions 
    // taken on this message will be performed in the mailbox 
    // owner's mailbox. 
    message.Save(new FolderId(WellKnownFolderName.Drafts, new Mailbox("primary@contoso.com")));
    // Send the email and save the message in the mailbox owner's 
    // Sent Items folder.
    // This method call results in a SendItem call to EWS.
    message.SendAndSaveCopy(new FolderId(WellKnownFolderName.SentItems, new Mailbox("primary@contoso.com")));
    Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" 
    + message.ToRecipients[0] + "' and saved in the Sent Items folder of the mailbox owner.");
}
```

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a>使用 EWS 创建并发送代理电子邮件
<a name="bk_createews"> </a>

EWS 使您能够使用代理用户的服务对象代表邮箱所有者创建和发送电子邮件。 此示例演示如何使用 [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) 操作创建电子邮件和 [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) 操作来发送时间并将其保存在邮箱所有者的"已发送邮件"文件夹中。 
  
这也是在使用 **Save** 方法创建和发送电子邮件时 EWS 托管 API 发送的第一个 XML [请求](#bk_createewsma)。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应 **CreateItem** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值，该值指示电子邮件已成功创建和保存。 该响应还包含新创建的电子邮件的项目 ID。
  
**ItemId** 值已缩短为可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="iNRaAAA="
                        ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

接下来，使用 **SendItem** 操作代表邮箱所有者发送邮件，并将其保存在邮箱所有者的"已发送邮件"文件夹中。 
  
**ItemId** 值已缩短为可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="iNRaAAA="
                  ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx)邮件响应 **SendItem** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值，该值指示电子邮件已成功发送并保存到邮箱所有者的"已发送邮件"文件夹。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 搜索代理电子邮件
<a name="bk_searchewsma"> </a>

若要搜索电子邮件，必须使用包含[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数的[ExchangeService.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)方法之一，以便指定邮箱所有者的"收件箱"文件夹。 
  
```cs
static void DelegateAccessSearchEmailWithFilter(ExchangeService service)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    // Define the search filter.
    SearchFilter.ContainsSubstring filter = new SearchFilter.ContainsSubstring(ItemSchema.Subject, 
        "soccer", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching Inbox items. 
        // The parameters of FindItems must denote the mailbox owner,
        // mailbox, and Inbox folder.
        // This call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(new 
            FolderId(WellKnownFolderName.Inbox, "primary@contoso.com"), 
            filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

**FindItems** 调用返回具有 ID 的响应后，可以使用 ID 和隐式访问获取、更新或删除该电子邮件，[](delegate-access-and-ews-in-exchange.md#bk_implicit)并且无需指定邮箱所有者的 SMTP 地址。 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a>使用 EWS 搜索作为代理的电子邮件
<a name="bk_searchews"> </a>

EWS 使您能够使用代理用户的服务对象搜索满足一组搜索条件的电子邮件。 本示例演示如何使用 [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) 操作在所有者的"收件箱"文件夹中查找主题中包含单词"inbox"的邮件。 
  
这也是当您搜索电子邮件时 EWS 托管 API 发送的 XML [请求](#bk_searchewsma)。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="soccer" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

服务器使用 [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)消息响应 **FindItem** 请求，其中包含 **NoError** 的 [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值，指示搜索已成功完成。 该响应包含满足搜索条件的任何电子邮件的 [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) 元素。 在这种情况下，只找到一封电子邮件。 
  
ItemId 元素[](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)的值已缩短为可读性。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="iNwoAAA="
                          ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQuu" />
                <t:Subject>Soccer team</t:Subject>
                <t:DateTimeReceived>2014-03-10T06:16:55Z</t:DateTimeReceived>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

现在，您具有符合条件的电子邮件的 **ItemId，** 您可以使用 **ItemId** 和隐式访问获取、更新或删除该电子邮件，并且无需指定邮箱所有者 [](delegate-access-and-ews-in-exchange.md#bk_implicit)的 SMTP 地址。 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 作为代理获取、更新或删除电子邮件项目
<a name="bk_geteswma"> </a>

您可以使用 EWS 托管 API 获取、更新或删除电子邮件，方式与不使用委派访问时执行这些操作的方式相同。 唯一的区别是 **ExchangeService** 对象用于委派用户。 Bind 方法调用中包含的项目ID 唯一标识邮箱存储中邮箱所有者的"收件箱"文件夹中的项目。 
  
**表 2.作为代理处理电子邮件的 EWS 托管 API 方法**

|**任务**|**EWS 托管的 API 方法**|**代码示例**|
|:-----|:-----|:-----|
|获取电子邮件  <br/> |[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 获取项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|更新电子邮件  <br/> |[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 后跟 [更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 更新项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|删除电子邮件  <br/> |[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) 后跟 [删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 删除项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a>使用 EWS 获取、更新或删除代理电子邮件项目
<a name="bk_getews"> </a>

您可以使用 EWS 托管 API 获取、更新或删除电子邮件，方式与不使用委派访问时执行这些操作的方式相同。 唯一的区别是服务对象用于委派用户。 **GetItem** 请求中包含的项目 ID 唯一标识邮箱所有者的"收件箱"文件夹中的邮箱存储中的项目。 
  
**表 3.用于代理处理电子邮件的 EWS 操作**

|**任务**|**EWS 操作**|**代码示例**|
|:-----|:-----|:-----|
|获取电子邮件  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[使用 EWS 获取项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|更新电子邮件  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) 后跟 [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[使用 EWS 更新项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|删除电子邮件  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) 后跟 [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[使用 EWS 删除项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的代理访问和 EWS](delegate-access-and-ews-in-exchange.md)    
- [使用 Exchange 中的 EWS 添加和删除Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [使用 EWS 设置其他用户的文件夹Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    

