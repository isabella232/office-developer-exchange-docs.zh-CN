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
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a><span data-ttu-id="f8b91-103">使用 Exchange 2013 中的 EWS 展开通讯组</span><span class="sxs-lookup"><span data-stu-id="f8b91-103">Expand distribution groups by using EWS in Exchange 2013</span></span>

<span data-ttu-id="f8b91-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 来扩展通讯组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-104">Learn how to expand a distribution group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="f8b91-105">您可以使用[ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) ews 操作展开通讯组以标识所有收件人。</span><span class="sxs-lookup"><span data-stu-id="f8b91-105">You can use the [ExchangeService.ExpandGroup](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS operation to expand a distribution group to identify all recipients.</span></span> 
  
<span data-ttu-id="f8b91-106">由于[ExpandGroup](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx)方法已重载，因此可以通过以下几种方式调用它：</span><span class="sxs-lookup"><span data-stu-id="f8b91-106">Because the [ExpandGroup](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) method is overloaded, you can call it in several ways:</span></span> 
  
- <span data-ttu-id="f8b91-107">[ExpandGroup （字符串）](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) -展开由 SMTP 地址标识的组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-107">[ExpandGroup(String)](https://msdn.microsoft.com/library/office/ee343988%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address.</span></span> 
    
- <span data-ttu-id="f8b91-108">[ExpandGroup （EmailAddress）](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) -展开一个由电子邮件地址标识的组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-108">[ExpandGroup(EmailAddress)](https://msdn.microsoft.com/library/office/ee344007%28v=exchg.80%29.aspx) - Expands a group identified by an email address.</span></span> 
    
- <span data-ttu-id="f8b91-109">[ExpandGroup （ItemId）](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) -展开由组 ID 标识的组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-109">[ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) - Expands a group identified by a group ID.</span></span> 
    
- <span data-ttu-id="f8b91-110">[ExpanGroup （string，string）](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) -展开由 SMTP 地址和该地址的路由类型标识的组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-110">[ExpanGroup(String, String)](https://msdn.microsoft.com/library/office/ee356468%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address and the routing type of that address.</span></span> 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a><span data-ttu-id="f8b91-111">使用 EWS 托管 API 展开通用通讯组或安全组</span><span class="sxs-lookup"><span data-stu-id="f8b91-111">Expand a universal distribution group or security group by using EWS Managed API</span></span>
<span data-ttu-id="f8b91-112"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="f8b91-112"><a name="bk_ExpandDGEWSMA"> </a></span></span>

<span data-ttu-id="f8b91-113">下面的示例演示如何使用电子邮件地址扩展通用通讯组或安全组，这是最简单的方法。</span><span class="sxs-lookup"><span data-stu-id="f8b91-113">The following example shows how to expand a universal distribution group or security group by using an email address, which is the simplest approach.</span></span> <span data-ttu-id="f8b91-114">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="f8b91-114">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

<span data-ttu-id="f8b91-115">这并不是很多代码，但它也非常基本，可能无法为你提供要查找的内容。</span><span class="sxs-lookup"><span data-stu-id="f8b91-115">That's not a lot of code, but it's also pretty basic and might not give you what you are looking for.</span></span> <span data-ttu-id="f8b91-116">现在，让我们进一步介绍一下。</span><span class="sxs-lookup"><span data-stu-id="f8b91-116">So let's take it a step further.</span></span> <span data-ttu-id="f8b91-117">通讯组也可以包含其他通讯组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-117">Distribution groups can also contain other distribution groups.</span></span> <span data-ttu-id="f8b91-118">只需展开它，即可输出包含的通讯组的电子邮件地址，但不会将其展开。</span><span class="sxs-lookup"><span data-stu-id="f8b91-118">Simply expanding it will output the email address of the contained distribution groups but not expand them.</span></span> <span data-ttu-id="f8b91-119">通过添加几行代码，可以递归方式展开组以输出每个联系人。</span><span class="sxs-lookup"><span data-stu-id="f8b91-119">By adding a few more lines of code, you can recursively expand the groups to output every contact.</span></span>
  
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

<span data-ttu-id="f8b91-120">现在，您可以在代码中调用此新函数，并展开第一个中包含的所有公用通讯组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-120">And now you can call this new function in the your code and expand all the public distribution groups contained within the first one.</span></span>
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a><span data-ttu-id="f8b91-121">使用 EWS 托管 API 展开联系人组</span><span class="sxs-lookup"><span data-stu-id="f8b91-121">Expand a contact group by using EWS Managed API</span></span>
<span data-ttu-id="f8b91-122"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="f8b91-122"><a name="bk_ExpandDGEWSMA"> </a></span></span>

<span data-ttu-id="f8b91-123">由于联系人组没有关联的电子邮件地址，因此您需要使用[ExpandGroup （ItemId）](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx)方法根据 ItemId 展开该组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-123">Because contact groups do not have an associated email address, you need to expand the group based on the ItemId by using the [ExpandGroup(ItemId)](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="f8b91-124">您可以创建一个函数（如前面的示例所示），并将第二个参数类型从一个字符串更改为[ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="f8b91-124">You can create a function, as shown in the previous example, and change the second parameter type from a string to an [ItemId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).</span></span>
  
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

<span data-ttu-id="f8b91-125">现在，您可以使用 Exchange 服务对象和联系人组的**ItemId**来调用此函数。</span><span class="sxs-lookup"><span data-stu-id="f8b91-125">Now you can call this function by using the Exchange service object and the **ItemId** of the contact group.</span></span> <span data-ttu-id="f8b91-126">请注意，示例中的**ItemId**是为了提高可读性而缩短的。</span><span class="sxs-lookup"><span data-stu-id="f8b91-126">Note that the **ItemId** in the example is shortened for readability.</span></span> 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a><span data-ttu-id="f8b91-127">使用 EWS 展开通用通讯组或安全组</span><span class="sxs-lookup"><span data-stu-id="f8b91-127">Expand a universal distribution group or security group by using EWS</span></span>
<span data-ttu-id="f8b91-128"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="f8b91-128"><a name="bk_ExpandDGEWSMA"> </a></span></span>

<span data-ttu-id="f8b91-129">下面的示例演示在使用[ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx)操作时，从客户端发送到服务器的 XML 请求消息。</span><span class="sxs-lookup"><span data-stu-id="f8b91-129">The following example shows the XML request message that is sent from the client to the server when you use the [ExpandDL](https://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="f8b91-130">这也是当您使用 EWS 托管 API[展开通用通讯组](#bk_ExpandDGEWSMA)时，EWS 托管 api 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="f8b91-130">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [expand a universal distribution group](#bk_ExpandDGEWSMA).</span></span> 
  
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

<span data-ttu-id="f8b91-131">下面的示例演示从服务器发送到客户端的 XML 响应消息。</span><span class="sxs-lookup"><span data-stu-id="f8b91-131">The following example shows the XML response message that is sent from the server to the client.</span></span> <span data-ttu-id="f8b91-132">请注意，同时返回邮箱和通用通讯组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-132">Notice that both mailboxes and universal distribution groups are returned.</span></span>
  
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

<span data-ttu-id="f8b91-133">与使用 EWS 托管 API 时不同，在使用 EWS 展开通用通讯组时，无法以递归方式展开返回的通讯组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-133">Unlike when you use the EWS Managed API, when you use EWS to expand a universal distribution group, you can't recursively expand the distribution groups that are returned.</span></span> <span data-ttu-id="f8b91-134">您将需要发送其他请求，以展开响应中包含的每个通讯组。</span><span class="sxs-lookup"><span data-stu-id="f8b91-134">You will need to send an additional request to expand each of the distribution groups included in the response.</span></span>
  
## <a name="expand-a-contact-group-by-using-ews"></a><span data-ttu-id="f8b91-135">使用 EWS 展开联系人组</span><span class="sxs-lookup"><span data-stu-id="f8b91-135">Expand a contact group by using EWS</span></span>
<span data-ttu-id="f8b91-136"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="f8b91-136"><a name="bk_ExpandDGEWSMA"> </a></span></span>

<span data-ttu-id="f8b91-137">展开联系人组的 XML 请求类似于扩展通讯组的请求。</span><span class="sxs-lookup"><span data-stu-id="f8b91-137">The XML request to expand a contact group is similar to a request to expand a distribution group.</span></span> <span data-ttu-id="f8b91-138">使用联系人组的[ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) ，而不是电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f8b91-138">Instead of an email address, you use the [ItemId](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the contact group.</span></span> <span data-ttu-id="f8b91-139">为了提高可读性，此示例中的**ItemId**已缩短。</span><span class="sxs-lookup"><span data-stu-id="f8b91-139">The **ItemId** in this example is shortened for readability.</span></span> 
  
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

<span data-ttu-id="f8b91-140">对展开联系人组的请求的 XML 响应结构与对扩展通用通讯组的请求的响应相同。</span><span class="sxs-lookup"><span data-stu-id="f8b91-140">The structure of the XML response to a request to expand a contact group is the same as the response to a request to expand a universal distribution group.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f8b91-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f8b91-141">See also</span></span>


- [<span data-ttu-id="f8b91-142">通讯组和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="f8b91-142">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="f8b91-143">使用 Exchange 中的 EWS 创建联系人组</span><span class="sxs-lookup"><span data-stu-id="f8b91-143">Create contact groups by using EWS in Exchange</span></span>](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

