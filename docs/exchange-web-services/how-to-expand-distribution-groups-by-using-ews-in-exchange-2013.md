---
title: 在 2013 年 10 月Exchange EWS 展开通讯组
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 25ee84e7-63bc-4f51-9b7d-e7f46fd574d5
description: 了解如何在通讯组中使用 EWS 托管 API 或 EWS 展开Exchange。
ms.openlocfilehash: 6aeebbd14604295bce46049f0e383663414c01a0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513183"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a>在 2013 年 10 月Exchange EWS 展开通讯组

了解如何在通讯组中使用 EWS 托管 API 或 EWS 展开Exchange。
  
可以使用 [ExchangeService.ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS 托管 API 方法或 [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS 操作展开通讯组以标识所有收件人。 
  
由于 [ExpandGroup](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) 方法已重载，因此您可以通过多种方式调用该方法： 
  
- [ExpandGroup (String) ](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) - 展开由 SMTP 地址标识的组。 
    
- [ExpandGroup (EmailAddress) ](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) - 展开由电子邮件地址标识的组。 
    
- [ExpandGroup (ItemId) ](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) - 展开由组 ID 标识的组。 
    
- [ExpanGroup (String， String) ](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) - 展开由 SMTP 地址和该地址的路由类型标识的组。 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a>使用 EWS 托管 API 展开通用通讯组或安全组
<a name="bk_ExpandDGEWSMA"> </a>

下面的示例演示如何使用电子邮件地址展开通用通讯组或安全组，这是最简单的方法。 此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

虽然这不是很多代码，但它也相当基本，可能不会提供您寻找的内容。 因此，让我们进一步执行一步操作。 通讯组还可以包含其他通讯组。 只需展开它，就会输出包含的通讯组的电子邮件地址，但不展开它们。 通过添加几行代码，可以递归展开组以输出每个联系人。
  
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

现在，您可以在代码中调用此新函数，并展开第一个代码中包含的所有公共通讯组。
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a>使用 EWS 托管 API 展开联系人组
<a name="bk_ExpandDGEWSMA"> </a>

由于联系人组没有关联的电子邮件地址，因此您需要使用 ExpandGroup ([ItemId) 基于 ItemId ](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) 展开组。 您可以创建一个函数，如上一示例所示，将第二个参数类型从字符串更改为 [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)。
  
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

现在，可以使用联系人组的 Exchange 和 **ItemId** 调用此函数。 请注意，为可读性，示例中的 **ItemId** 已缩短。 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a>使用 EWS 展开通用通讯组或安全组
<a name="bk_ExpandDGEWSMA"> </a>

以下示例显示使用 [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) 操作时从客户端发送到服务器的 XML 请求消息。 这也是当您使用 EWS 托管 API 展开通用通讯组时，EWS 托管 API 发送的 XML [请求](#bk_ExpandDGEWSMA)。 
  
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

以下示例显示从服务器发送到客户端的 XML 响应消息。 请注意，将返回邮箱和通用通讯组。
  
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

与使用 EWS 托管 API 时不同，在使用 EWS 展开通用通讯组时，无法以递归方式展开返回的通讯组。 您需要发送其他请求来展开响应中包含的每个通讯组。
  
## <a name="expand-a-contact-group-by-using-ews"></a>使用 EWS 展开联系人组
<a name="bk_ExpandDGEWSMA"> </a>

展开联系人组的 XML 请求类似于展开通讯组的请求。 使用联系人组的 [ItemId，而不是](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) 电子邮件地址。 为可读性，缩短了此示例中的 **ItemId。** 
  
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

对展开联系人组的请求的 XML 响应的结构与对展开通用通讯组的请求的响应相同。
  
## <a name="see-also"></a>另请参阅


- [通讯组和 Exchange 中的 EWS](distribution-groups-and-ews-in-exchange.md)
    
- [在联系人组中使用 EWS 创建Exchange](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

