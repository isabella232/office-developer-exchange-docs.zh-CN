---
title: ResolveNames 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: ResolveNames 操作可解析不明确的电子邮件地址和显示名称。
ms.openlocfilehash: 51728addddd2bfb9d35b874ae8c11e83a4c8629b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468276"
---
# <a name="resolvenames-operation"></a>ResolveNames 操作

**ResolveNames**操作可解析不明确的电子邮件地址和显示名称。 
  
## <a name="using-the-resolvenames-operation"></a>使用 ResolveNames 操作

此操作可用于验证别名并将显示名称解析为相应的邮箱用户。 如果存在不明确的名称， **ResolveNames**操作响应将提供有关每个邮箱用户的信息，以便客户端应用程序可以解析这些名称。 
  
## <a name="remarks"></a>备注

ResolveNames 响应将返回最大为100个候选人。 返回的100候选项是在查找操作中遇到的第一个100。
  
带有前缀路由类型（如 smtp 或 sip）的电子邮件地址保存在多值数组中。 当您在未解析名称的开头添加路由类型（如 "sip:User1@Contoso.com"）时， **ResolveNames**操作将对该数组的每个值执行部分匹配。 如果不指定路由类型， **ResolveNames**将默认为 smtp 的路由类型，将其与主 smtp 地址属性相匹配，而不会搜索多值数组。 
  
在一个请求中只能指定一个不明确的名称。 先搜索 Active Directory，然后再搜索用户的 "联系人" 文件夹。 从用户的联系人文件夹解析的条目具有非 null 的**ItemId**属性，该属性随后可在 GetItem 请求中使用。 如果是私有通讯组列表的 ID，则可在[ExpandDL 操作](expanddl-operation.md)中使用。 如果将**ReturnFullContactData**属性设置为**true**，则使用**ResolveNames**操作找到的 Active Directory 条目将返回描述[联系人](contact.md)的其他属性。 **ReturnFullContactData**属性不会影响用户的联系人文件夹中的联系人和私有通讯组列表返回的数据。 
  
## <a name="resolvenames-request-example"></a>ResolveNames 请求示例

### <a name="description"></a>说明

以下示例的**ResolveNames**请求显示如何解析用户的输入。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ResolveNames xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                  ReturnFullContactData="true">
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

对此请求的响应将返回以 "Jo" 或 "Mi" 开头的所有条目。 返回的项目为公用邮箱、公用和私人通讯组列表和联系人。
  
> [!NOTE]
> 仅搜索默认 "个人联系人" 文件夹中的联系人。 
  
以下是**ResolveNames**请求的可能结果： 
  
- 不包含已解析实体的响应将返回**ResponseClass**属性值等于**Error**。 **MessageText**元素将包含 "**找不到任何结果**"。
    
- 包含单个已解析实体的响应将返回一个等于**Success**的**ResponseClass**属性值。
    
- 包含多个可能的实体的响应将返回一个等于**警告**的**ResponseClass**属性值。 在这种情况下，无法将实体解析为唯一标识。 **MessageText**元素将包含 "找到多个结果"。 
    
### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>成功的 ResolveNames 操作响应示例

### <a name="description"></a>说明

下面的示例演示对**ResolveNames**请求的成功响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
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
                <t:Name>User2</t:Name>
                <t:EmailAddress>User2@example.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>User2</t:DisplayName>
                <t:EmailAddresses>
                  <t:Entry Key="EmailAddress1">SMTP:User2@example.com</t:Entry>
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

### <a name="successful-resolvenames-response-elements"></a>成功的 ResolveNames 响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [ResolutionSet](resolutionset.md)
    
- [解决方案](resolution.md)
    
- [邮箱](mailbox.md)
    
- [名称 (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType （EmailAddressType）](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
- [联系人](contact.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [条目（EmailAddress）](entry-emailaddress.md)
    
- [ContactSource](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a>ResolveNames 操作错误响应

### <a name="description"></a>说明

下面的示例演示对**ResolveNames**请求的错误响应。 错误是由尝试解析无法解析的名称导致的。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
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

### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>另请参阅



[ExpandDL 操作](expanddl-operation.md)


[使用名称解析](https://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

