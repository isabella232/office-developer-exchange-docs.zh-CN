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
description: ResolveNames 操作解析不明确的电子邮件地址和显示名称。
ms.openlocfilehash: 8443cf834dfdf104daeaaa92fdee3742c3fa3719
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827162"
---
# <a name="resolvenames-operation"></a>ResolveNames 操作

**ResolveNames**操作解析不明确的电子邮件地址和显示名称。 
  
## <a name="using-the-resolvenames-operation"></a>使用 ResolveNames 操作

此操作可用于验证别名并解析为适当的邮箱的用户的显示名称。 如果存在不明确的名称， **ResolveNames**操作响应将提供有关每个邮箱用户的信息，以便客户端应用程序可以解析名称。 
  
## <a name="remarks"></a>备注

ResolveNames 响应返回最多 100 候选人。 返回 100 候选人应该是查找操作中遇到的第一个 100。
  
多值数组中保存前缀的路由类型，如 smtp 或 sip，与电子邮件地址。 无法解析的名称，例如"sip:User1@Contoso.com"的开头添加路由类型时， **ResolveNames**操作执行针对该数组的每个值的部分匹配。 如果不指定传送类型， **ResolveNames**将默认为 smtp 的路由类型、 匹配到主 smtp 地址属性，以及不搜索多值数组。 
  
可以在单个请求中指定只有一个不明确的名称。 首先，搜索 active Directory，然后搜索用户的联系人文件夹。 来自用户的联系人文件夹解析的项有一个非空**ItemId**属性，然后可以使用 GetItem 请求中。 如果是私人通讯组列表的 ID，然后它可在[ExpandDL 操作](expanddl-operation.md)。 如果**ReturnFullContactData**属性设置为**true**，则找到**ResolveNames**操作的 Active Directory 条目将返回描述[联系人](contact.md)的其他属性。 **ReturnFullContactData**属性不会影响的联系人和专用返回的数据从用户的联系人文件夹的通讯组列表。 
  
## <a name="resolvenames-request-example"></a>ResolveNames 请求示例

### <a name="description"></a>说明

**ResolveNames**请求的下面的示例演示如何解决用户的条目。
  
### <a name="code"></a>代码

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
      <UnresolvedEntry>User2</UnresolvedEntry>
    </ResolveNames>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

对此请求的响应将返回"Jo"或"英里。"开头的所有条目 返回的项是公用邮箱、 公共和私有通讯组列表和联系人。
  
> [!NOTE]
> 仅在默认的个人联系人文件夹中的联系人进行搜索。 
  
以下是**ResolveNames**请求的可能结果： 
  
- 不包含解析的实体的响应将返回**ResponseClass**属性值等于**错误**。 **MessageText**元素将包含"**未找到结果**"。
    
- 包含单个解析的实体的响应将返回**ResponseClass**属性值等于**成功**。
    
- 包含多个可能的实体的响应将返回**ResponseClass**属性值等于**警告**。 在这种情况下，实体无法解析为唯一标识。 **MessageText**元素将包含"找到多个结果。" 
    
### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>成功 ResolveNames 操作响应示例

### <a name="description"></a>说明

下面的示例演示对**ResolveNames**请求成功响应。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
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

### <a name="successful-resolvenames-response-elements"></a>成功 ResolveNames 响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ResolveNamesResponse](resolvenamesresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ResolveNamesResponseMessage](resolvenamesresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [ResolutionSet](resolutionset.md)
    
- [解决方法](resolution.md)
    
- [Mailbox](mailbox.md)
    
- [名称 (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
- [Contact](contact.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [条目 （电子邮件地址）](entry-emailaddress.md)
    
- [ContactSource](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a>ResolveNames 操作错误响应

### <a name="description"></a>说明

下面的示例演示对**ResolveNames**请求错误响应。 尝试解析无法解析名称被导致错误。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
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


[使用名称解析](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

