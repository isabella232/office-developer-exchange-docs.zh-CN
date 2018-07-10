---
title: 通过使用 EWS 在 Exchange 2013 中展开通讯组
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 25ee84e7-63bc-4f51-9b7d-e7f46fd574d5
description: 了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中展开通讯组。
ms.openlocfilehash: 0f9186fb71b3005c71a70e89aafb674ae15e4814
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752768"
---
# <a name="expand-distribution-groups-by-using-ews-in-exchange-2013"></a><span data-ttu-id="79580-103">通过使用 EWS 在 Exchange 2013 中展开通讯组</span><span class="sxs-lookup"><span data-stu-id="79580-103">Expand distribution groups by using EWS in Exchange 2013</span></span>

<span data-ttu-id="79580-104">了解如何通过使用 EWS 的 EWS 托管 API 在 Exchange 中展开通讯组。</span><span class="sxs-lookup"><span data-stu-id="79580-104">Learn how to expand a distribution group by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="79580-105">您可以使用[ExchangeService.ExpandGroup](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS 操作以展开通讯组来标识所有收件人。</span><span class="sxs-lookup"><span data-stu-id="79580-105">You can use the [ExchangeService.ExpandGroup](http://msdn.microsoft.com/zh-cn/library/office/microsoft.exchange.webservices.data.exchangeservice.expandgroup%28v=exchg.80%29.aspx) EWS Managed API method or the [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) EWS operation to expand a distribution group to identify all recipients.</span></span> 
  
<span data-ttu-id="79580-106">因为过载[ExpandGroup](http://msdn.microsoft.com/zh-cn/library/office/ee344007%28v=exchg.80%29.aspx)方法，可以调用它以多种方式：</span><span class="sxs-lookup"><span data-stu-id="79580-106">Because the [ExpandGroup](http://msdn.microsoft.com/zh-cn/library/office/ee344007%28v=exchg.80%29.aspx) method is overloaded, you can call it in several ways:</span></span> 
  
- <span data-ttu-id="79580-107">[ExpandGroup(String)](http://msdn.microsoft.com/zh-cn/library/office/ee343988%28v=exchg.80%29.aspx) -展开 SMTP 地址由标识的组。</span><span class="sxs-lookup"><span data-stu-id="79580-107">[ExpandGroup(String)](http://msdn.microsoft.com/zh-cn/library/office/ee343988%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address.</span></span> 
    
- <span data-ttu-id="79580-108">[ExpandGroup(EmailAddress)](http://msdn.microsoft.com/zh-cn/library/office/ee344007%28v=exchg.80%29.aspx) -扩展的电子邮件地址由标识的组。</span><span class="sxs-lookup"><span data-stu-id="79580-108">[ExpandGroup(EmailAddress)](http://msdn.microsoft.com/zh-cn/library/office/ee344007%28v=exchg.80%29.aspx) - Expands a group identified by an email address.</span></span> 
    
- <span data-ttu-id="79580-109">[ExpandGroup(ItemId)](http://msdn.microsoft.com/zh-cn/library/office/ee356407%28v=exchg.80%29.aspx) -展开组 id 标识的组</span><span class="sxs-lookup"><span data-stu-id="79580-109">[ExpandGroup(ItemId)](http://msdn.microsoft.com/zh-cn/library/office/ee356407%28v=exchg.80%29.aspx) - Expands a group identified by a group ID.</span></span> 
    
- <span data-ttu-id="79580-110">[ExpanGroup （字符串、 字符串）](http://msdn.microsoft.com/zh-cn/library/office/ee356468%28v=exchg.80%29.aspx) -展开 SMTP 地址，该地址路由类型由标识的组。</span><span class="sxs-lookup"><span data-stu-id="79580-110">[ExpanGroup(String, String)](http://msdn.microsoft.com/zh-cn/library/office/ee356468%28v=exchg.80%29.aspx) - Expands a group identified by an SMTP address and the routing type of that address.</span></span> 
    
## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews-managed-api"></a><span data-ttu-id="79580-111">通过使用 EWS 托管 API 展开通用通讯组或安全组</span><span class="sxs-lookup"><span data-stu-id="79580-111">Expand a universal distribution group or security group by using EWS Managed API</span></span>
<span data-ttu-id="79580-112"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="79580-112"></span></span>

<span data-ttu-id="79580-113">下面的示例演示如何通过使用一个电子邮件地址，这是最简单的方法中展开的通用通讯组或安全组。</span><span class="sxs-lookup"><span data-stu-id="79580-113">The following example shows how to expand a universal distribution group or security group by using an email address, which is the simplest approach.</span></span> <span data-ttu-id="79580-114">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="79580-114">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Return the expanded group.
   ExpandGroupResults myGroupMembers = service.ExpandGroup("employees@contoso.com");
// Display the group members.
   foreach (EmailAddress address in myGroupMembers.Members)
   {
      Console.WriteLine("Email Address: {0}", address);
   }

```

<span data-ttu-id="79580-115">不是大量的代码，但它也是非常基本和可能不为您提供您要查找的。</span><span class="sxs-lookup"><span data-stu-id="79580-115">That's not a lot of code, but it's also pretty basic and might not give you what you are looking for.</span></span> <span data-ttu-id="79580-116">因此，我们来看它步骤进一步。</span><span class="sxs-lookup"><span data-stu-id="79580-116">So let's take it a step further.</span></span> <span data-ttu-id="79580-117">通讯组还可以包含其他通讯组。</span><span class="sxs-lookup"><span data-stu-id="79580-117">Distribution groups can also contain other distribution groups.</span></span> <span data-ttu-id="79580-118">只需展开将输出包含的通讯组的电子邮件地址，但不是将其展开。</span><span class="sxs-lookup"><span data-stu-id="79580-118">Simply expanding it will output the email address of the contained distribution groups but not expand them.</span></span> <span data-ttu-id="79580-119">可以通过添加几行代码，以递归方式展开要输出的每个联系人的组。</span><span class="sxs-lookup"><span data-stu-id="79580-119">By adding a few more lines of code, you can recursively expand the groups to output every contact.</span></span>
  
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

<span data-ttu-id="79580-120">现在您可以在调用此新的函数和您的代码和扩展中的第一个包含的所有公共通讯组。</span><span class="sxs-lookup"><span data-stu-id="79580-120">And now you can call this new function in the your code and expand all the public distribution groups contained within the first one.</span></span>
  
```cs
ExpandDistributionLists(service, "employees@contoso.com");

```

## <a name="expand-a-contact-group-by-using-ews-managed-api"></a><span data-ttu-id="79580-121">通过使用 EWS 托管 API 展开联系人组</span><span class="sxs-lookup"><span data-stu-id="79580-121">Expand a contact group by using EWS Managed API</span></span>
<span data-ttu-id="79580-122"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="79580-122"></span></span>

<span data-ttu-id="79580-123">联系人组没有关联的电子邮件地址，因为需要以展开基于通过使用[ExpandGroup(ItemId)](http://msdn.microsoft.com/zh-cn/library/office/ee356407%28v=exchg.80%29.aspx)方法的 ItemId 组。</span><span class="sxs-lookup"><span data-stu-id="79580-123">Because contact groups do not have an associated email address, you need to expand the group based on the ItemId by using the [ExpandGroup(ItemId)](http://msdn.microsoft.com/zh-cn/library/office/ee356407%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="79580-124">您可以创建一个函数，如上面的示例中所示，并将第二个参数类型从字符串更改为[ItemId](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="79580-124">You can create a function, as shown in the previous example, and change the second parameter type from a string to an [ItemId](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.itemid%28v=exchg.80%29.aspx).</span></span>
  
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

<span data-ttu-id="79580-125">现在您可以使用 Exchange 服务对象和联系人组**ItemId**调用此函数。</span><span class="sxs-lookup"><span data-stu-id="79580-125">Now you can call this function by using the Exchange service object and the **ItemId** of the contact group.</span></span> <span data-ttu-id="79580-126">请注意**ItemId**在示例中将缩短为便于阅读。</span><span class="sxs-lookup"><span data-stu-id="79580-126">Note that the **ItemId** in the example is shortened for readability.</span></span> 
  
```cs
ExpandContactGroup(service, new ItemId("AAMkADBlY…");

```

## <a name="expand-a-universal-distribution-group-or-security-group-by-using-ews"></a><span data-ttu-id="79580-127">通过使用 EWS 展开通用通讯组或安全组</span><span class="sxs-lookup"><span data-stu-id="79580-127">Expand a universal distribution group or security group by using EWS</span></span>
<span data-ttu-id="79580-128"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="79580-128"></span></span>

<span data-ttu-id="79580-129">下面的示例演示 XML 请求发送的邮件是从客户端到服务器时使用[ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="79580-129">The following example shows the XML request message that is sent from the client to the server when you use the [ExpandDL](http://msdn.microsoft.com/library/1f7837e7-9eff-4e10-9577-c40f7ed6af94%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="79580-130">这也是 EWS 托管 API 时您使用 EWS 托管 API 到[展开通用通讯组](#bk_ExpandDGEWSMA)发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="79580-130">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [expand a universal distribution group](#bk_ExpandDGEWSMA).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
        <t:EmailAddress>employees@contoso.com</t:EmailAddress>
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="79580-131">下面的示例演示从服务器发送到客户端的 XML 响应消息。</span><span class="sxs-lookup"><span data-stu-id="79580-131">The following example shows the XML response message that is sent from the server to the client.</span></span> <span data-ttu-id="79580-132">请注意，返回邮箱和通用通讯组。</span><span class="sxs-lookup"><span data-stu-id="79580-132">Notice that both mailboxes and universal distribution groups are returned.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
     xmlns:xsd="http://www.w3.org/2001/XMLSchema">
<ExpandDLResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                      xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <ExpandDLResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <DLExpansion IncludesLastItemInRange="true" TotalItemsInView="4">
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Sadie Daniels</Name>
          <EmailAddress>sadie@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Alfred Welker</Name>
          <EmailAddress>alfred@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>Mailbox</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Name>Contoso Sales</Name>
          <EmailAddress>sales@contoso.com</EmailAddress>
          <RoutingType>SMTP</RoutingType>
          <MailboxType>PublicDL</MailboxType>
        </Mailbox>
        <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="79580-133">与不同当您使用 EWS 托管 API 时您使用 EWS 展开通用通讯组，则不能以递归方式扩展返回通讯组。</span><span class="sxs-lookup"><span data-stu-id="79580-133">Unlike when you use the EWS Managed API, when you use EWS to expand a universal distribution group, you can't recursively expand the distribution groups that are returned.</span></span> <span data-ttu-id="79580-134">您将需要发送以展开每个通讯组的响应中包括的其他请求。</span><span class="sxs-lookup"><span data-stu-id="79580-134">You will need to send an additional request to expand each of the distribution groups included in the response.</span></span>
  
## <a name="expand-a-contact-group-by-using-ews"></a><span data-ttu-id="79580-135">通过使用 EWS 展开联系人组</span><span class="sxs-lookup"><span data-stu-id="79580-135">Expand a contact group by using EWS</span></span>
<span data-ttu-id="79580-136"><a name="bk_ExpandDGEWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="79580-136"></span></span>

<span data-ttu-id="79580-137">类似于请求展开通讯组展开联系人组的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="79580-137">The XML request to expand a contact group is similar to a request to expand a distribution group.</span></span> <span data-ttu-id="79580-138">而不是电子邮件地址，您可以使用[ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)的联系人组。</span><span class="sxs-lookup"><span data-stu-id="79580-138">Instead of an email address, you use the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the contact group.</span></span> <span data-ttu-id="79580-139">**ItemId**在此示例将缩短为便于阅读。</span><span class="sxs-lookup"><span data-stu-id="79580-139">The **ItemId** in this example is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <Mailbox>
         <ItemId xmlns="http://schemas.microsoft.com/exchange/services/2006/types" Id="AAMkADBlY…" />
      </Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="79580-140">展开通用通讯组的请求的响应相同的 XML 响应展开联系人组的请求的结构。</span><span class="sxs-lookup"><span data-stu-id="79580-140">The structure of the XML response to a request to expand a contact group is the same as the response to a request to expand a universal distribution group.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="79580-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79580-141">See also</span></span>


- [<span data-ttu-id="79580-142">通讯组和 Exchange 中的 EWS</span><span class="sxs-lookup"><span data-stu-id="79580-142">Distribution groups and EWS in Exchange</span></span>](distribution-groups-and-ews-in-exchange.md)
    
- [<span data-ttu-id="79580-143">使用 EWS 在 Exchange 中创建联系人组</span><span class="sxs-lookup"><span data-stu-id="79580-143">Create contact groups by using EWS in Exchange</span></span>](how-to-create-contact-groups-by-using-ews-in-exchange.md)
    

