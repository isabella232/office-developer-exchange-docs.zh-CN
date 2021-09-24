---
title: 使用 2013 中的 EWS 解析不明确Exchange名称
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: 了解如何通过从 Active Directory 域服务 (AD DS) 或用户邮箱中的联系人文件夹中获取可能的匹配项，使用 EWS 托管 API 或 EWS 解析不明确的名称。
ms.openlocfilehash: 5946dad32639b454b3961eaa172b6069ce118b58
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521121"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>使用 2013 中的 EWS 解析不明确Exchange名称

了解如何通过从 Active Directory 域服务 (AD DS) 或用户邮箱中的联系人文件夹中获取可能的匹配项，使用 EWS 托管 API 或 EWS 解析不明确的名称。
  
为贵组织的用户提供参加培训课程的员工的姓名和地址的手写列表。 他们希望向列表中的用户发送包含其他一些信息的电子邮件，但他们无法读取每个人的电子邮件地址。 如果要为应用程序中的用户解决此问题，EWS 可以提供帮助。 可以使用 [ExchangeService.ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS 托管 API 方法或 [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS 操作返回选定文本（如姓氏的一部分）的潜在匹配项列表。 返回的项目可以是公共用户邮箱、通讯组和联系人。 
  
请注意，Exchange前缀路由类型（如 smtp 或 sip）的电子邮件地址保存在多值数组中。 当您在未解析名称的开头添加路由类型（如"sip：User1"）时 **，ResolveName** 方法和 **ResolveNames** 操作会针对该数组的每个值执行部分匹配。 如果不指定路由类型，则方法或操作将默认为 smtp，将该方法或操作与主 smtp 地址属性匹配，而不是搜索多值数组。 例如，如果您搜索 User1，但不包括 sip 前缀，您将不会 sip:User1@Contoso.com，即使这是一个有效的邮箱。 
  
一个请求中只能指定一个不明确的名称。 如果您有一个要解析的不明确名称的列表，则需要循环访问该列表并调用每个条目的方法或操作。 用户的"联系人"文件夹中的候选项将具有非 null 项目 ID 值，然后可在 [Contact.Bind](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx) 方法调用或 [GetItem](https://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx) 操作请求中用于检索其他信息。 如果候选组是通讯组，可以使用 [ExpandGroup (ItemId) ](https://msdn.microsoft.com/library/office/ee356407%28v=exchg.80%29.aspx) EWS 托管 API 方法或 [ExpandDL](https://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS 操作获取成员列表。 如果 _returnContactDetails_ 参数或 **ReturnFullContactData** EWS 属性设置为 true，则通过 ResolveName 方法或 **ResolveNames** 操作返回的 Active Directory 条目将包括描述联系人的其他属性。  _returnContactDetails_ 参数或 **ReturnFullContactData** 属性不会影响为联系人和联系人组返回的数据。 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>使用 EWS 托管 API 解析不明确的名称
<a name="bk_EWSMA"> </a>

您可以使用 [ResolveName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) 方法查找与传递的不明确名称匹配的候选项。 您可以使用 **ResolveName** 方法的重载以五种不同的方式搜索候选项。 
  
**表 1.重载的 ResolveName 方法**

|**方法**|**工作原理**|
|:-----|:-----|
|[ResolveName (String) ](https://msdn.microsoft.com/library/dd635548%28v=exchg.80%29.aspx) <br/> |按该顺序查找用户的"联系人"文件夹中的联系人和 GAL (全局) 列表。 字符串变量是试图解析的不明确名称。  <br/> |
|[ResolveName (String、ResolveNameSearchLocation、Boolean) ](https://msdn.microsoft.com/library/dd634595%28v=exchg.80%29.aspx) <br/> |在默认联系人文件夹和/或全局地址列表或 GAL 文件夹中 (联系人) 。 字符串值是不明确的名称，搜索位置指定联系人文件夹和/或 GAL，布尔值指示是否返回完整的联系人信息。  <br/> |
|[ResolveName (String、ResolveNameSearchLocation、Boolean、PropertySet) ](https://msdn.microsoft.com/library/hh532803%28v=exchg.80%29.aspx) <br/> |查找默认联系人文件夹和/或全球通讯簿 GAL (联系人) 。 此方法使您能够设置返回的属性。  <br/> |
|[ResolveName (\<FolderId\> String、IEnumerable、ResolveNameSearchLocation、Boolean) ](https://msdn.microsoft.com/library/dd636014%28v=exchg.80%29.aspx) <br/> |查找指定的联系人文件夹中的联系人和/或全局地址列表 (GAL) 。 可以使用此方法传递要搜索的文件夹集合。 这使您能够查找非默认"联系人"文件夹的联系人文件夹。  <br/> |
|[ResolveName (\<FolderId\> String、IEnumerable、ResolveNameSearchLocation、Boolean、PropertySet) ](https://msdn.microsoft.com/library/hh532581%28v=exchg.80%29.aspx) <br/> |查找全局地址列表中的联系人 (GAL) 和/或特定联系人文件夹中。 此方法使您能够设置返回的属性。  <br/> |
   
让我们从一个简单的示例开始。 以下示例演示如何解析文本字符串"dan"，并输出找到的每个候选项的名称和电子邮件地址。 此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。 
  
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

该响应最多返回 100 个候选项，但可能多于 100 个候选项。 若要确定是否仅返回更多候选项的前 100 个候选项，请检查[NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx)对象中的[IncludesAllResolutions](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx)的值。 如果值为 true，则没有更多可能的候选项;如果值为 false，则该方法仅返回更多潜在候选项中的前 100 个。 
  
如果你在大型组织中工作，则像"dan"这样的名称将返回最多 100 个候选人。 若要减少返回的候选项数，请限制搜索位置。 下一个示例使用 [ResolveNameSearchLocation](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx) 枚举指定在何处搜索以解析不明确的名称。 
  
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

如果将联系人存储在已知"联系人"文件夹外的其他文件夹中，请使用重载的方法之一指定在何处查找候选项。 下面的示例基于文件夹 ID 为 **ResolveName** 方法创建文件夹列表。 为可读性，已缩短 **FolderId。** 
  
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

如果应用筛选器并且未返回任何候选项，则 [NameResolutionCollection](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx) 将包含零个条目。 可以通过查看集合的 [Count](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx) 属性来验证这一点。 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>使用 EWS 解析不明确的名称
<a name="bk_EWSMA"> </a>

可以使用 [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS 操作来标识不明确名称的可能候选项。 [UnresolvedEntry](https://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx)元素包含要解析的不明确名称。 以下示例显示如何解析名称将一个名称为"一对一"。 这也是 EWS 托管 API 在使用 [ResolveName](#bk_EWSMA)方法时使用的 XML 请求，不同方面是它使用不同的名称作为有效输出示例。
  
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

该响应最多返回 100 个候选项，但可能多于 100 个候选项 若要确定是否仅返回了更多候选项的前 100 个候选项，请检查[ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx)元素[的 IncludesLastItemInRange](https://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx)属性的值。 如果值为 true，则没有更多可能的候选项;如果值为 false，则操作仅返回更多潜在候选项中的前 100 个。 
  
以下示例显示找到一个候选项时 XML 响应。 请记住 [，ResolutionSet](https://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx) 可以包含最多 100 个候选项，每个候选项都由 [Resolution](https://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx) 元素及其子元素表示。 
  
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

你并不总是会为不明确的名称提供候选项。 下面的示例在未找到候选项时将 XML 响应作为错误显示。
  
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
    
- [在 2013 年 10 月Exchange EWS 展开通讯组](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

