---
title: 在 Exchange 中使用 EWS 以代理的形式访问电子邮件
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，将电子邮件作为代理访问。
ms.openlocfilehash: 0c26f69042c568fe7d877778c7d8f1e689e5b372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528284"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a>在 Exchange 中使用 EWS 以代理的形式访问电子邮件

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS，将电子邮件作为代理访问。
  
您可以使用 EWS 托管 API 或 EWS 为用户委派对邮箱所有者的 "收件箱" 文件夹的访问权限。 然后，代理可以代表邮箱所有者创建会议请求、搜索电子邮件、检索、更新和删除邮箱所有者的 "收件箱" 文件夹中的电子邮件，具体取决于他们的权限。
  
作为代理，您可以使用相同的方法和操作访问邮箱所有者的 "收件箱" 文件夹，而无需委派访问权限即可访问该文件夹。 主要区别在于，必须使用[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicit)来查找或创建电子邮件项目，然后在确定项目 ID 之后，可以使用[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除项目。 
  
**表1。用于将电子邮件作为代理访问的 EWS 托管 API 方法和 EWS 操作**

|**如果您想要 .。。**|**使用此 EWS 托管 API 方法 .。。**|**使用此 EWS 操作 .。。**|
|:-----|:-----|:-----|
|创建电子邮件并将其作为代理发送  <br/> |[EmailMessage](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) ， [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供对邮箱所有者的 "草稿" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)  <br/> [FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数提供对邮箱所有者的 "已发送邮件" 文件夹的[显式访问](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[SendAndSaveCopy EmailMessage](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx)  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> [SendItem](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|创建多封电子邮件作为代理  <br/> |**FolderId**参数提供对邮箱所有者的 "收件箱" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[CreateItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx)  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|搜索电子邮件或查找作为代理的电子邮件  <br/> |**FolderId**参数提供对邮箱所有者的 "收件箱" 文件夹的[显式访问权限](delegate-access-and-ews-in-exchange.md#bk_explicitewsma)的[FindItems ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx)  <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)其中[邮箱](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx)元素指定邮箱所有者的[EmailAddress](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx)  <br/> |
|将电子邮件作为代理获取  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|将电子邮件更新为代理  <br/> |[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)后接[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|删除作为代理的电子邮件  <br/> |[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)后接[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
在将电子邮件作为代理人处理时，请记住以下事项：
  
- 如果代理只需要处理会议请求和响应，则代理不需要对 "收件箱" 文件夹的访问权限。 有关详细信息，请参阅以[委派方式访问日历的先决条件任务](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq)。
    
- 当收件人收到代表邮箱所有者发送的邮件时，发件人将显示为 "代表*邮箱所有者**委派*"。 
    
> [!NOTE]
> 在本文的代码示例中，primary@contoso.com 是邮箱所有者。 
  
## <a name="prerequisite-tasks"></a>先决条件任务
<a name="bk_prereq"> </a>

在用户将邮箱所有者的 "收件箱" 文件夹作为代理进行访问之前，必须将该用户[添加为具有](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)邮箱所有者的 "收件箱" 文件夹权限的代理。 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建电子邮件并将其作为代理发送
<a name="bk_createewsma"> </a>

使用 EWS 托管 API，您可以使用代理用户的服务对象代表邮箱所有者创建和发送电子邮件。 本示例演示如何使用[save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx)方法将邮件保存到邮箱所有者的 "草稿" 文件夹中，然后使用[SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx)方法将邮件保存到邮箱所有者的 "已发送邮件" 文件夹中，并将其保存到邮箱所有者的 "已发送邮件" 文件夹中。 
  
本示例假定**服务**是代理的有效[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且已为委派授予对[邮箱所有者的 "收件箱"、"草稿" 和 "已发送邮件" 文件夹的适当权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)。
  
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

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a>使用 EWS 创建电子邮件并将其作为代理发送
<a name="bk_createews"> </a>

EWS 使您可以使用代理用户的服务对象代表邮箱所有者创建和发送电子邮件。 本示例演示如何使用[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx)操作创建电子邮件和[SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)操作，以发送时间并将其保存在邮箱所有者的 "已发送邮件" 文件夹中。 
  
这也是在使用**Save**方法[创建和发送电子邮件](#bk_createewsma)时，EWS 托管 API 发送的第一个 XML 请求。
  
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

服务器使用[CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)邮件响应**CreateItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功创建并保存了该电子邮件。 该响应还包含新创建的电子邮件的项目 ID。
  
为了提高可读性， **ItemId**值已缩短。 
  
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

接下来，使用**SendItem**操作代表邮箱所有者发送邮件，并将其保存在邮箱所有者的 "已发送邮件" 文件夹中。 
  
为了提高可读性， **ItemId**值已缩短。 
  
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

服务器使用[SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx)邮件响应**SendItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示电子邮件已成功发送并保存到邮箱所有者的 "已发送邮件" 文件夹。
  
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

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 搜索作为代理的电子邮件
<a name="bk_searchewsma"> </a>

若要搜索电子邮件，您必须使用包含[FolderId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx)参数的 FindItems 方法之一，以便您可以指定邮箱所有者的 "收件箱" 文件夹[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) 。 
  
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

在**FindItems**调用返回带有 ID 的响应后，您可以使用 id 和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除该电子邮件，而无需指定邮箱所有者的 SMTP 地址。 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a>使用 EWS 搜索作为代理的电子邮件
<a name="bk_searchews"> </a>

通过 EWS，您可以使用代理用户的服务对象搜索符合一组搜索条件的电子邮件。 本示例演示如何使用[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)操作查找所有者的 "收件箱" 文件夹中包含主题中包含 "足球" 一词的邮件。 
  
这也是在[搜索电子邮件](#bk_searchewsma)时，EWS 托管 API 发送的 XML 请求。
  
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

服务器使用[FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx)邮件响应**FindItem**请求，其中包含[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素值**NoError**，表示已成功完成搜索。 响应包含符合搜索条件的任何电子邮件的[Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx)元素。 在这种情况下，仅找到一个电子邮件。 
  
为了提高可读性， [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)元素的值已缩短。 
  
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

现在您已拥有满足条件的电子邮件的**ItemId** ，您可以通过使用**ItemId**和[隐式访问](delegate-access-and-ews-in-exchange.md#bk_implicit)来获取、更新或删除该电子邮件，而无需指定邮箱所有者的 SMTP 地址。 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 获取、更新或删除作为委派的电子邮件项目
<a name="bk_geteswma"> </a>

您可以使用 EWS 托管 API 来获取、更新或删除电子邮件，方式与您在不使用代理访问时执行这些操作的方式相同。 唯一的区别是**ExchangeService**对象是代表委派用户的。 **Bind**方法调用中包含的项目 ID 在邮箱所有者的 "收件箱" 文件夹中唯一标识邮箱存储中的项目。 
  
**表2。将电子邮件作为代理使用的 EWS 托管 API 方法**

|**任务**|**EWS 托管的 API 方法**|**代码示例**|
|:-----|:-----|:-----|
|获取电子邮件  <br/> |[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 获取项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|更新电子邮件  <br/> |先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)后接[更新](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 更新项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|删除电子邮件  <br/> |先[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)后接[删除](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[使用 EWS 托管 API 删除项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a>使用 EWS 获取、更新或删除作为代理的电子邮件项目
<a name="bk_getews"> </a>

您可以使用 EWS 托管 API 来获取、更新或删除电子邮件，方式与您在不使用代理访问时执行这些操作的方式相同。 唯一的区别是，服务对象是代表委派用户的。 **GetItem**请求中包含的项目 ID 在邮箱所有者的 "收件箱" 文件夹中唯一标识邮箱存储中的项目。 
  
**表3。将电子邮件作为代理使用的 EWS 操作**

|**任务**|**EWS 操作**|**代码示例**|
|:-----|:-----|:-----|
|获取电子邮件  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[使用 EWS 获取项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|更新电子邮件  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[使用 EWS 更新项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|删除电子邮件  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx)后接[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[使用 EWS 删除项](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a>另请参阅

- [代理访问和 Exchange 中的 EWS](delegate-access-and-ews-in-exchange.md)    
- [使用 Exchange 中的 EWS 添加和删除委派](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [使用 Exchange 中的 EWS 为另一个用户设置文件夹权限](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [Calendars and EWS in Exchange](calendars-and-ews-in-exchange.md)
    

