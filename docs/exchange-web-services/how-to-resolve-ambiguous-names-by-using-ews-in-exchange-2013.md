---
title: 模糊名称解析使用 EWS 在 Exchange 2013
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1ba21c54-ecd2-4a1e-80d4-0f4171dea84f
description: 了解如何使用 EWS 托管 API 或 EWS 通过从 Active Directory 域服务 (AD DS) 或用户的邮箱中的联系人文件夹中获取可能的匹配项来解析模糊名称。
ms.openlocfilehash: 05a88043083a27d2e6d445cd71e5f3919c5a775d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752873"
---
# <a name="resolve-ambiguous-names-by-using-ews-in-exchange-2013"></a>模糊名称解析使用 EWS 在 Exchange 2013

了解如何使用 EWS 托管 API 或 EWS 通过从 Active Directory 域服务 (AD DS) 或用户的邮箱中的联系人文件夹中获取可能的匹配项来解析模糊名称。
  
您的组织中的用户参加培训课程的员工提供手写的名称和地址列表。 所需的某些其他信息的电子邮件发送给人员在列表中，但他们不能读取每个人的电子邮件地址。 如果您想要解决此问题，供您的应用程序中的用户，可以帮助 EWS。 您可以使用[ExchangeService.ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS 操作返回的文本，如最后一个名称的一部分的选定内容的潜在匹配项的列表。 返回的项可以是公共用户邮箱、 通讯组和联系人。 
  
请注意，Exchange 保存与前缀的路由类型，如 smtp 或 sip，多值数组中的电子邮件地址。 无法解析的名称，例如"sip: User1"的开头添加路由类型时， **ResolveName**方法和**ResolveNames**操作执行针对该数组的每个值的部分匹配。 如果不指定传送类型，该方法或操作将默认为 smtp、 匹配到主 smtp 地址属性，以及不搜索多值数组。 例如，如果您搜索 User1，不包括 sip 前缀，您将不接收 sip:User1@Contoso.com 结果是，即使这是有效的邮箱。 
  
您只能在单个请求中指定一个模糊名称。 如果您有一组不明确的名称解析，您将需要循环访问列表，并调用该方法或为每个项的操作。 从用户的联系人文件夹的候选人将具有一个非空项目 ID 值，该值可然后用于[Contact.Bind](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.contact.bind%28v=exchg.80%29.aspx)方法调用或[GetItem](http://msdn.microsoft.com/library/769df8eb-9c72-48b5-a49f-82c6b86bc5fc%28Office.15%29.aspx)操作请求中检索的其他信息。 如果候选通讯组，可以使用[ExpandGroup(ItemId)](http://msdn.microsoft.com/en-us/library/office/ee356407%28v=exchg.80%29.aspx) EWS 托管 API 方法或[ExpandDL](http://msdn.microsoft.com/library/affe84a5-ad98-4aba-83f4-8732938b763d%28Office.15%29.aspx) EWS 操作来获取成员的列表。 如果_returnContactDetails_参数或**ReturnFullContactData** EWS 属性设置为 true，通过**ResolveName**方法返回 Active Directory 条目或**ResolveNames**操作将包含其他属性用于描述联系人。 _ReturnContactDetails_参数或**ReturnFullContactData**属性不影响联系人返回的数据和联系人组。 
  
## <a name="resolve-ambiguous-names-by-using-ews-managed-api"></a>模糊名称解析使用 EWS 托管 API
<a name="bk_EWSMA"> </a>

可以使用[ResolveName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx)方法查找与传递的模糊名称匹配的候选人。 可以使用**ResolveName**方法的重载的候选项搜索五个不同的方式。 
  
**表 1。重载的 ResolveName 方法**

|**方法**|**工作原理**|
|:-----|:-----|
|[ResolveName(String)](http://msdn.microsoft.com/en-us/library/dd635548%28v=exchg.80%29.aspx) <br/> |在用户的联系人文件夹和全局地址列表 (GAL) 中查找联系人 — 该顺序。 字符串变量是您试图解析的不明确名称。  <br/> |
|[ResolveName （字符串，ResolveNameSearchLocation，布尔值）](http://msdn.microsoft.com/en-us/library/dd634595%28v=exchg.80%29.aspx) <br/> |在默认联系人文件夹和/或全局地址列表 (GAL) 中查找联系人。 字符串值不明确的名称，搜索位置指定联系人文件夹和/或 GAL，并且布尔值，该值指示是否返回完整的联系信息。  <br/> |
|[ResolveName (字符串，ResolveNameSearchLocation，Boolean、 属性集)](http://msdn.microsoft.com/en-us/library/hh532803%28v=exchg.80%29.aspx) <br/> |在默认联系人文件夹和/或全局地址列表 (GAL) 中查找联系人。 此方法可设置所返回的属性。  <br/> |
|[ResolveName (String、 IEnumerable\<文件夹 Id\>，ResolveNameSearchLocation、 Boolean)](http://msdn.microsoft.com/en-us/library/dd636014%28v=exchg.80%29.aspx) <br/> |在指定的联系人文件夹和/或全局地址列表 (GAL) 中查找联系人。 您可以使用此方法将传递的搜索文件夹集合。 这使您可以查找联系人文件夹之外的默认联系人文件夹中。  <br/> |
|[ResolveName (String、 IEnumerable\<文件夹 Id\>，ResolveNameSearchLocation、 Boolean、 属性集)](http://msdn.microsoft.com/en-us/library/hh532581%28v=exchg.80%29.aspx) <br/> |在全局地址列表 (GAL) 和/或特定的联系人文件夹中查找联系人。 此方法可设置所返回的属性。  <br/> |
   
让我们开始一个简单示例。 下面的示例演示如何解决"dan"的文本字符串和输出找到的每个应聘者的姓名和电子邮件地址。 此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。 
  
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

响应返回最多 100 候选人，尽管可能有 100 多个潜在候选人。 若要确定是否已返回仅更多的候选人的前 100 个候选，检查[IncludesAllResolutions](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.includesallresolutions%28v=exchg.80%29.aspx) [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx)对象中的值。 如果值为 true，没有其他可能候选人;如果值为 false，该方法仅返回前 100 的更多的潜在的候选人。 
  
如果您工作的大型组织，很可能的名称，如"dan"将返回 100 的候选项的最大数量。 为了减少返回的候选项的数量，限制了您在其中搜索。 下一个示例使用[ResolveNameSearchLocation](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.resolvenamesearchlocation%28v=exchg.80%29.aspx)枚举指定搜索范围以解析不明确名称。 
  
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

如果您将您的联系人存储中已知的联系人文件夹之外的文件夹中，使用重载的方法之一指定位置查找候选人。 下面的示例创建文件夹列表**ResolveName**方法基于文件夹 id。 为便于阅读缩短了**文件夹 Id** 。 
  
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

如果应用筛选器并返回无候选人， [NameResolutionCollection](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection%28v=exchg.80%29.aspx)将包含零个条目。 您可以通过查看集合的[Count](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.nameresolutioncollection.count%28v=exchg.80%29.aspx)属性进行验证。 
  
## <a name="resolve-ambiguous-names-by-using-ews"></a>使用 EWS 解析模糊名称
<a name="bk_EWSMA"> </a>

可以使用[ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) EWS 操作来标识可能适合的不明确名称。 [UnresolvedEntry](http://msdn.microsoft.com/library/5ac6116a-3b24-40f8-a877-dbe9a6935919%28Office.15%29.aspx)元素包含您想要解析的不明确名称。 下面的示例演示如何以解析名称 Sadie。 这也是 EWS 托管 API 时您[使用 ResolveName 方法](#bk_EWSMA)，但前者使用不同的有效输出示例名称所使用的 XML 请求。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>Sadie</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

响应返回最多 100 候选人，尽管可能有 100 个以上的潜在候选人，可确定是否已返回仅更多的候选人的前 100 个候选，检查[IncludesLastItemInRange](http://msdn.microsoft.com/library/e7d6c7d3-548e-48b0-a313-bfef81e4832a%28Office.15%29.aspx)的值[ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx)元素的属性。 如果值为 true，没有其他可能候选人;如果值为 false，该操作将仅返回前 100 的更多的潜在的候选人。 
  
下面的示例演示 XML 响应时找到一个候选。 请记住， [ResolutionSet](http://msdn.microsoft.com/library/43d5b876-0e87-4414-9b1d-bff1c1ec825c%28Office.15%29.aspx)可以包含最多 100 个候选人，每个由[解决方案](http://msdn.microsoft.com/library/573bed4b-d7b1-4baf-b16f-0795cdebf1a7%28Office.15%29.aspx)元素和及其子元素。 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

您不总是将附带的不明确名称的候选人。 下面的示例演示 XML 响应中，为错误，，没有候选发现时。
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
    
- [通过使用 EWS 在 Exchange 2013 中展开通讯组](how-to-expand-distribution-groups-by-using-ews-in-exchange-2013.md)
    

