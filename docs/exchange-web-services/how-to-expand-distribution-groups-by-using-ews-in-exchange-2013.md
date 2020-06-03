---
title: 使用 Exchange 2013 中的 EWS 展开通讯组
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25ee84e7-63bc-4f51-9b7d-e7f46fd574d5
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来扩展通讯组。
ms.openlocfilehash: 2cbeb65b5a722bce4d5cab8fd716230874a6afca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528116"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a>使用 Exchange 2013 中的 EWS 展开通讯组

了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来扩展通讯组。
  
您可以使用[ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) ews 操作展开通讯组以标识所有收件人。 
  
由于[ExpandGroup](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx)方法已重载，因此可以通过以下几种方式调用它： 
  
- [ExpandGroup （字符串）](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) -展开由 SMTP 地址标识的组。 
    
- [ExpandGroup （EmailAddress）](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) -展开一个由电子邮件地址标识的组。 
    
- [ExpandGroup （ItemId）](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) -展开由组 ID 标识的组。 
    
- [ExpanGroup （string，string）](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) -展开由 SMTP 地址和该地址的路由类型标识的组。 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a>使用 EWS 托管 API 展开通用通讯组或安全组
<a name="bk_ExpandDGEWSMA"> </a>

下面的示例演示如何使用电子邮件地址扩展通用通讯组或安全组，这是最简单的方法。 此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

这并不是很多代码，但它也非常基本，可能无法为你提供要查找的内容。 现在，让我们进一步介绍一下。 通讯组也可以包含其他通讯组。 只需展开它，即可输出包含的通讯组的电子邮件地址，但不会将其展开。 通过添加几行代码，可以递归方式展开组以输出每个联系人。
  
```cs
private static void ExpandDistributionLists(ExchangeService service, string Mailbox)
{
   // Return the expanded group.
      ExpandGroupResults myGroupMembers = service.ExpandGroup(Mailbox);
   // Display the group members.
      foreach (EmailAddress address in myGroupMembers.Members)
      {
         // Check to see if the mailbox is a public group
         if (address.MailboxType == MailboxType.PublicGroup)
      {
         // Call the function again to expand the contained
         // distribution group.
         ExpandDistributionLists(service, address.Address);
      }
      else
      {
         // Output the address of the mailbox.
         Console.WriteLine("Email Address: {0}", address);
      }
   }
}

```

现在，您可以在代码中调用此新函数，并展开第一个中包含的所有公用通讯组。
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a>使用 EWS 托管 API 展开联系人组
<a name="bk_ExpandDGEWSMA"> </a>

由于联系人组没有关联的电子邮件地址，因此您需要使用[ExpandGroup （ItemId）](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx)方法根据 ItemId 展开该组。 您可以创建一个函数（如前面的示例所示），并将第二个参数类型从一个字符串更改为[ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)。
  
```cs
private static void ExpandContactGroup(ExchangeService service, ItemId groupID)
{
   // Return the expanded group.
      ExpandGroupResults myGroupMembers = service.ExpandGroup(groupID);
   // Display the group members.
      foreach (EmailAddress address in myGroupMembers.Members)
      {
         if (address.MailboxType == MailboxType.PublicGroup)
         {
            ExpandDistributionLists(service, address.Address);
         }
         else
         {
            Console.WriteLine("Email Address: {0}", address);
         }
      }
}
```

现在，您可以使用 Exchange 服务对象和联系人组的**ItemId**来调用此函数。 请注意，示例中的**ItemId**是为了提高可读性而缩短的。 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a>使用 EWS 展开通用通讯组或安全组
<a name="bk_ExpandDGEWSMA"> </a>

下面的示例演示在使用[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx)操作时，从客户端发送到服务器的 XML 请求消息。 这也是当您使用 EWS 托管 API[展开通用通讯组](#bk_ExpandDGEWSMA)时，EWS 托管 api 发送的 XML 请求。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>employees@contoso.com</t:EmailAddress>
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

下面的示例演示从服务器发送到客户端的 XML 响应消息。 请注意，同时返回邮箱和通用通讯组。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:xsd="http://www.w3.org/2001/XMLSchema">
<ExpandDLResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                      xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <ExpandDLResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <DLExpansion IncludesLastItemInRange="true" TotalItemsInView="4">
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Sadie Daniels</Name>
          <EmailAddress>sadie@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Alfred Welker</Name>
          <EmailAddress>alfred@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Sales</Name>
          <EmailAddress>sales@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
        <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Support</Name>
          <EmailAddress>support@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
      </DLExpansion>
    </ExpandDLResponseMessage>
  </ResponseMessages>
</ExpandDLResponse>
</s:Body>
</s:Envelope>
```

与使用 EWS 托管 API 时不同，在使用 EWS 展开通用通讯组时，无法以递归方式展开返回的通讯组。 您将需要发送其他请求，以展开响应中包含的每个通讯组。
  
## <a name="expand-a-contact-group-by-using-ews"></a>使用 EWS 展开联系人组
<a name="bk_ExpandDGEWSMA"> </a>

展开联系人组的 XML 请求类似于扩展通讯组的请求。 使用联系人组的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) ，而不是电子邮件地址。 为了提高可读性，此示例中的**ItemId**已缩短。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
         <ItemId xmlns="https://schemas.microsoft.com/exchange/services/2006/types" Id="AAMkADBlY…" />
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

对展开联系人组的请求的 XML 响应结构与对扩展通用通讯组的请求的响应相同。
  
## <a name="see-also"></a>另请参阅


- [通讯组和 Exchange 中的 EWS](distribution-groups-and-ews-in-exchange.md)
    
- [使用 Exchange 中的 EWS 创建联系人组](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

