---
title: ExpandDL 操作
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: ExpandDL 操作将公开通讯组列表的完整成员身份。
ms.openlocfilehash: 8edaf057538e2c1136465f0ff7937c14477b2c47
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44454048"
---
# <a name="expanddl-operation"></a>ExpandDL 操作

ExpandDL 操作将公开通讯组列表的完整成员身份。
  
## <a name="using-the-expanddl-web-method"></a>使用 ExpandDL Web 方法

ExpandDL 操作使用位于位于 .asmx 中的 Web 服务。 此 Web 服务方法接受一个[邮箱](mailbox.md)元素，该元素可包含一个[EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)子元素，用于扩展公共通讯组列表或用于扩展专用通讯组列表的[ItemId](itemid.md)子元素。 
  
可以使用以下任一项扩展公用通讯组列表：
  
1. 通讯组列表别名
    
2. 简单邮件传输协议 (SMTP) 地址
    
3. X400
    
4. X500
    
5. Exchange 旧地址
    
6. 通讯组列表名称
    
7. 显示名称
    
> [!IMPORTANT]
> 显示名称不是唯一的。 多个帐户可以共享同一个显示名称。 
  
## <a name="remarks"></a>备注

不支持递归展开。 一次调用只能扩展一个通讯组列表。 如果有多个通讯组列表匹配条件，Web 服务会报告错误。 客户端应用程序可以使用不明确的名称解析（ANR）来查找不明确的通讯组列表，然后选择所需通讯组列表的正确电子邮件地址作为[ExpandDL 操作](expanddl-operation.md)的参数。 有关详细信息，请参阅[ResolveNames operation](resolvenames-operation.md)。
  
公用通讯组列表位于 Active Directory 中。 可以是任何启用邮件的通讯组或动态通讯组。 在地址列表中不应隐藏该组，并且每个成员都应具有非空电子邮件地址。 通讯组列表的成员可以是启用邮件的用户和联系人、公用文件夹以及启用邮件的通讯组列表和动态组。
  
专用通讯组列表位于用户邮箱的 "联系人" 文件夹中。 专用通讯组列表不具有电子邮件地址，因此在 ExpandDL 请求中使用其存储项目标识符。 私有通讯组列表的成员可以是任何启用邮件的用户、联系人或来自 Active Directory 的联系人或通讯组列表，或者来自用户的联系人文件夹的联系人或个人通讯组列表。
  
对于联系人或专用通讯组列表，将在响应中返回项目标识符。 这可用于获取有关对象的信息或展开私有通讯组列表中的成员资格。
  
## <a name="expanddl-private-distribution-list-request-example"></a>ExpandDL 私有通讯组列表请求示例

### <a name="description"></a>说明

以下示例的 ExpandDL 请求显示如何构成展开私有通讯组列表的请求。
  
### <a name="code"></a>代码

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:ExpandDL>
      <m:Mailbox>
       <t:EmailAddress>test</t:EmailAddress>
      </m:Mailbox>
    </m:ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

若要展开私有通讯组列表，[邮箱](mailbox.md)元素将包含用于标识用户邮箱中的专用通讯组列表的[ItemId](itemid.md)元素。 
  
## <a name="expanddl-public-distribution-list-request-example"></a>ExpandDL 公共通讯组列表请求示例

### <a name="description"></a>说明

以下示例的 ExpandDL 请求显示如何构成展开公共通讯组列表的请求。 该示例演示如何使用显示名称展开通讯组列表。
  
### <a name="code"></a>代码

```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

对此请求的响应将包含标识通讯组列表中的每个邮箱的**邮箱**元素。 如果通讯组列表中包含通讯组列表，则必须对嵌入的通讯组列表执行单独的通讯组列表展开。 如果通讯组列表没有成员或请求的通讯组列表不存在，则**ResponseClass**属性将包含一个等于 "成功" 的值。 
  
### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [ExpandDL](expanddl.md)
    
- [邮箱](mailbox.md)
    
- [EmailAddress （NonEmptyStringType）](emailaddress-nonemptystringtype.md)用于标识公用通讯组列表。 [ItemId](itemid.md)元素用于标识私有通讯组列表。 
    
> [!NOTE]
> 描述这些元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。 
  
## <a name="successful-expanddl-response-example"></a>成功的 ExpandDL 响应示例

### <a name="description"></a>说明

下面的 ExpandDL 响应示例显示对上面所述请求的响应。 通讯组列表扩展介绍了以下内容： 
  
- 响应中返回的通讯组列表的成员数。
    
- 响应是否包含通讯组列表的所有成员。
    
- 邮箱的名称。
    
- 邮箱的电子邮件地址。
    
- 邮箱的路由类型。
    
- 邮箱的类型。
    
> [!NOTE]
> 响应中不包含通讯组列表名称;因此，必须跟踪请求中的名称。 
  
### <a name="code"></a>代码

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:DLExpansion TotalItemsInView="3" IncludesLastItemInRange="true">
            <t:Mailbox>
              <t:Name>Dan Park</t:Name>
              <t:EmailAddress>dpark@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Jeff Price</t:Name>
              <t:EmailAddress>jprice@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
            <t:Mailbox>
              <t:Name>Tanja Plate</t:Name>
              <t:EmailAddress>tplate@exampledomain.com</t:EmailAddress>
              <t:RoutingType>SMTP</t:RoutingType>
              <t:MailboxType>Mailbox</t:MailboxType>
            </t:Mailbox>
          </m:DLExpansion>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [DLExpansion](dlexpansion.md)
    
- [邮箱](mailbox.md)
    
- [名称 (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType （EmailAddressType）](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
若要查找 ExpandDL 操作的响应邮件的其他选项，请浏览架构层次结构。 从[ExpandDLResponse](expanddlresponse.md)元素开始。 
  
## <a name="expanddl-error-response"></a>ExpandDL 错误响应

### <a name="description"></a>说明

下面的示例演示对 ExpandDL 请求的错误响应。
  
### <a name="code"></a>代码

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:ExpandDLResponseMessage ResponseClass="Error">
          <m:MessageText>No results are found.</m:MessageText>
          <m:ResponseCode>ErrorNameResolutionNoResults</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:ExpandDLResponseMessage>
      </m:ResponseMessages>
    </ExpandDLResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
若要查找 ExpandDL 操作的响应邮件的其他选项，请浏览架构层次结构。 从[ExpandDLResponse](expanddlresponse.md)元素开始。 
  
## <a name="see-also"></a>另请参阅

- [ResolveNames 操作](resolvenames-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

