---
title: ResolveNames 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: 6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb
description: ResolveNames 操作可解析不明确的电子邮件地址和显示名称。
ms.openlocfilehash: f5ab0e3ee23cc085d8aa425c6eeb0ac7c392b9bb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509446"
---
# <a name="resolvenames-operation"></a>ResolveNames 操作

**ResolveNames** 操作可解析不明确的电子邮件地址和显示名称。 
  
## <a name="using-the-resolvenames-operation"></a>使用 ResolveNames 操作

此操作可用于验证别名，以及将显示名称解析为相应的邮箱用户。 如果存在不明确的名称 **，ResolveNames** 操作响应会提供有关每个邮箱用户的信息，以便客户端应用程序可以解析这些名称。 
  
## <a name="remarks"></a>注解

ResolveNames 响应最多返回 100 个候选项。 返回的 100 个候选项是查找操作中遇到的前 100 个候选项。
  
前缀路由类型（如 smtp 或 sip）的电子邮件地址保存在多值数组中。 当您在未解析名称的开头添加路由类型（如"sip:User1@Contoso.com"时 **，ResolveNames** 操作会针对该数组的每个值执行部分匹配。 如果不指定路由类型 **，ResolveNames** 将默认为 smtp 的路由类型，将它与主 smtp 地址属性匹配，而不是搜索多值数组。 
  
一个请求中只能指定一个不明确的名称。 首先搜索 Active Directory，然后搜索用户的联系人文件夹。 用户的联系人文件夹中解析的条目具有非 null **ItemId** 属性，然后可在 GetItem 请求中使用该属性。 如果它是专用通讯组列表的 ID，则它可以在 ExpandDL 操作 [中使用](expanddl-operation.md)。 如果 **ReturnFullContactData** 属性设置为 **true**，则使用 **ResolveNames** 操作找到的 Active Directory 条目将返回描述联系人 的其他 [属性](contact.md)。 **ReturnFullContactData** 属性不会影响从用户的联系人文件夹返回的联系人和专用通讯组列表的数据。 
  
## <a name="resolvenames-request-example"></a>ResolveNames 请求示例

### <a name="description"></a>Description

**ResolveNames** 请求的以下示例显示如何解析 User 条目。
  
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

对此请求的响应将返回以"Jo"或"Mi"开始的所有条目。 返回的项目为公共邮箱、公用和专用通讯组列表以及联系人。
  
> [!NOTE]
> 仅搜索默认个人"联系人"文件夹中的联系人。 
  
以下是 **ResolveNames** 请求的可能结果： 
  
- 不包含已解析实体的响应将返回等于 Error 的 **ResponseClass** **属性值**。 **MessageText** 元素将包含"**未找到任何结果"。**
    
- 包含单个已解析实体的响应将返回等于 Success 的 **ResponseClass** **属性值**。
    
- 包含多个可能实体的响应将返回等于 Warning 的 **ResponseClass** **属性值**。 在这种情况下，无法将实体解析为唯一标识。 **MessageText** 元素将包含"找到多个结果"。 
    
### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [ResolveNames](resolvenames.md)
    
- [UnresolvedEntry](unresolvedentry.md)
    
## <a name="successful-resolvenames-operation-response-example"></a>成功的 ResolveNames 操作响应示例

### <a name="description"></a>Description

以下示例显示了对 **ResolveNames** 请求的成功响应。 
  
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

响应中会使用下列元素：
  
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
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
- [联系人](contact.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
- [EmailAddresses](emailaddresses.md)
    
- [Entry (EmailAddress)](entry-emailaddress.md)
    
- [ContactSource](contactsource.md)
    
## <a name="resolvenames-operation-error-response"></a>ResolveNames 操作错误响应

### <a name="description"></a>Description

以下示例显示对 **ResolveNames** 请求的错误响应。 此错误由尝试解析无法解析的名称导致。 
  
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

错误响应中会使用下列元素：
  
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

