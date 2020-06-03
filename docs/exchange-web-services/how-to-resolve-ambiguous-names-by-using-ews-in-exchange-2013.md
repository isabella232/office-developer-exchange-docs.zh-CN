---
title: 使用 Exchange 2013 中的 EWS 解析不明确的名称
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: 了解如何使用 EWS 托管 API 或 EWS 通过从 Active Directory 域服务（AD DS）或用户邮箱中的联系人文件夹中获取可能的匹配项来解析不明确的名称。
ms.openlocfilehash: 5e30e268f54e6ca257e188592e49d168e64332ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527745"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>使用 Exchange 2013 中的 EWS 解析不明确的名称

了解如何使用 EWS 托管 API 或 EWS 通过从 Active Directory 域服务（AD DS）或用户邮箱中的联系人文件夹中获取可能的匹配项来解析不明确的名称。
  
您的组织中的用户将获得参加培训会话的员工的姓名和地址的手写填写列表。 他们希望向列表中的人员发送包含一些其他信息的电子邮件，但不能读取每个人的电子邮件地址。 如果要为您的应用程序中的用户解决此问题，则 EWS 可以提供帮助。 您可以使用[ExchangeService](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) ews 操作返回所选文本的潜在匹配项的列表，如姓的一部分。 返回的项可以是公共用户邮箱、通讯组和联系人。 
  
请注意，Exchange 会在多值数组中保存带有前缀路由类型（如 smtp 或 sip）的电子邮件地址。 当您在未解析名称的开头添加路由类型（如 "sip： User1"）时， **ResolveName**方法和**ResolveNames**操作将对该数组的每个值执行部分匹配。 如果不指定路由类型，则方法或操作将默认为 smtp，将其与主 smtp 地址属性相匹配，而不搜索多值数组。 例如，如果搜索 User1 而不包含 sip 前缀，则将不会收到 sip:User1@Contoso.com，即使这是有效邮箱也是如此。 
  
只能在一个请求中指定一个不明确的名称。 如果您有一个要解析的不明确名称的列表，则需要循环访问该列表并为每个条目调用方法或操作。 用户的 "联系人" 文件夹中的候选人将具有一个非 null 的 "项目 ID" 值，可在联系人中使用此值[。 Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx)方法 Call 或[GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx)操作请求以检索其他信息。 如果候选项是通讯组，则可以使用[ExpandGroup （ItemId）](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS 操作来获取成员列表。 如果将_returnContactDetails_参数或**ReturnFullContactData** EWS 属性设置为 True，则通过**ResolveName**方法或**ResolveNames**操作返回的 Active Directory 条目将包含描述该联系人的其他属性。 _ReturnContactDetails_参数或**ReturnFullContactData**属性不会影响为 "联系人" 和 "联系人" 组返回的数据。 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>使用 EWS 托管 API 解析模糊的名称
<a name="bk_EWSMA"> </a>

您可以使用[ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx)方法来查找与您传递的多义性名称相匹配的候选人。 您可以使用**ResolveName**方法的重载以五种不同的方式搜索候选人。 
  
**表1。重载的 ResolveName 方法**

|**方法**|**工作原理**|
|:-----|:-----|
|[ResolveName （字符串）](https://msdn.microsoft.com/library/dd635548%28v=exchg.80%29.aspx) <br/> |按此顺序在用户的 "联系人" 文件夹和全局地址列表（GAL）中查找联系人。 字符串变量是您尝试解析的不明确名称。  <br/> |
|[ResolveName （String，ResolveNameSearchLocation，Boolean）](https://msdn.microsoft.com/library/dd634595%28v=exchg.80%29.aspx) <br/> |在默认的 "联系人" 文件夹和/或全局地址列表（GAL）中查找联系人。 该字符串值是不明确的名称，搜索位置指定 "联系人" 文件夹和/或 GAL，布尔值指示是否返回完整的联系人信息。  <br/> |
|[ResolveName （String，ResolveNameSearchLocation，Boolean，PropertySet）](https://msdn.microsoft.com/library/hh532803%28v=exchg.80%29.aspx) <br/> |在默认的 "联系人" 文件夹和/或全局地址列表（GAL）中查找联系人。 此方法使您能够设置返回的属性。  <br/> |
|[ResolveName （String、IEnumerable \<FolderId\> 、ResolveNameSearchLocation、Boolean）](https://msdn.microsoft.com/library/dd636014%28v=exchg.80%29.aspx) <br/> |在指定的联系人文件夹和/或全局地址列表（GAL）中查找联系人。 您可以使用此方法将文件夹集合传递到搜索。 这使您可以查看联系人文件夹，而不是默认的 "联系人" 文件夹。  <br/> |
|[ResolveName （String、IEnumerable \<FolderId\> 、ResolveNameSearchLocation、Boolean、PropertySet）](https://msdn.microsoft.com/library/hh532581%28v=exchg.80%29.aspx) <br/> |在全局地址列表（GAL）和/或特定联系人文件夹中查找联系人。 此方法使您能够设置返回的属性。  <br/> |
   
让我们从一个简单的示例开始。 下面的示例演示如何解析文本字符串 "dan"，并输出找到的每个候选项的名称和电子邮件地址。 此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
```cs
// Resolve the ambiguous name "dan".
   NameResolutionCollection resolvedNames = service.ResolveName("dan");
   // Output the list of candidates.
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

尽管可能有超过100个潜在候选人，响应的最大返回值为100候选人。 若要确定是否仅返回更多候选项的前100个候选项，请检查[NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx)对象中的[IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx)的值。 如果值为 true，则没有其他可能的候选项;如果该值为 false，则该方法仅返回较多的潜在候选项的前100个。 
  
如果您在大型组织中工作，类似于 "dan" 的名称可能会返回最大数量的100候选人。 若要减少返回的候选人数，请限制搜索的位置。 下一个示例使用[ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx)枚举指定在何处搜索以解析不明确的名称。 
  
```cs
// Resolve the ambiguous name "dan".
// Only use the Contacts folder.
   NameResolutionCollection resolvedNames = service.ResolveName("dan", ResolveNameSearchLocation.ContactsOnly, false);
   // Output the list of candidates.   
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

如果将联系人存储在 "已知的联系人" 文件夹之外的文件夹中，请使用重载方法之一来指定要在何处查找候选人。 下面的示例将基于文件夹 ID 为**ResolveName**方法创建一个文件夹列表。 为了提高可读性， **FolderId**已缩短。 
  
```cs
// Create a list to store folders to search.
List<FolderId> folders = new List<FolderId>();
// Add a folder to the list based on the FolderId.
folders.Add(new FolderId("AABR8mboAAA="));
// Resolve the ambiguous name "dan".
// Only use the folders specified.
NameResolutionCollection resolvedNames = service.ResolveName("dan", folders, ResolveNameSearchLocation.ContactsOnly, false);
   foreach (NameResolution nameRes in resolvedNames)
   {
      Console.WriteLine("Contact name: " + nameRes.Mailbox.Name);
      Console.WriteLine("Contact e-mail address: " + nameRes.Mailbox.Address);
      Console.WriteLine("Mailbox type: " + nameRes.Mailbox.MailboxType);
   }

```

如果您应用筛选器，但未返回任何候选项，则[NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx)将包含零个条目。 您可以通过查看集合的[Count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx)属性来验证这一点。 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>使用 EWS 解析模糊名称
<a name="bk_EWSMA"> </a>

您可以使用[ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS 操作来标识不明确名称的可能候选项。 [UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx)元素包含要解析的不明确名称。 下面的示例演示如何解析名称 Sadie。 这也是在[使用 ResolveName 方法](#bk_EWSMA)时，EWS 托管 API 使用的 XML 请求，不同之处在于，它对有效的输出示例使用不同的名称。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

响应返回的最大值为100，但可能有多于100个潜在的候选项，以确定是否仅返回更多候选项的第一个100候选项，请检查[ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx)元素的[IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx)属性的值。 如果值为 true，则没有其他可能的候选项;如果该值为 false，则操作仅返回较多的潜在候选项的前100。 
  
下面的示例演示找到一个候选项时的 XML 响应。 请记住， [ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx)最多可以包含100个候选人，每个候选项由[解析](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx)元素及其子元素表示。 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>Sadie@Contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:Sadie@Contoso.com</t:Entry>
                </t:EmailAddresses>
                <t:ContactSource>ActiveDirectory</t:ContactSource>
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>
```

你不一定总是会遇到不明确名称的候选人。 下面的示例显示在没有找到候选项时，为错误的 XML 响应。
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Error">
          <m:MessageText>No results were found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </ResolveNamesResponse>
  </soap:Body>
</soap:Envelope>

```

## <a name="see-also"></a>另请参阅


- [人员和 Exchange 中的 EWS 中的联系人](people-and-contacts-in-ews-in-exchange.md)
    
- [使用 Exchange 2013 中的 EWS 展开通讯组](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

