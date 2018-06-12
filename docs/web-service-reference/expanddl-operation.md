---
title: ExpandDL 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: ExpandDL 操作公开完整的通讯组列表成员身份。
ms.openlocfilehash: e4654120881f81a79358e0e7c0ab016f94db3288
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754205"
---
# <a name="expanddl-operation"></a>ExpandDL 操作

ExpandDL 操作公开完整的通讯组列表成员身份。
  
## <a name="using-the-expanddl-web-method"></a>使用 ExpandDL Web 方法

ExpandDL 操作使用位于 Exchange.asmx Web 服务。 此 Web 服务方法接受是公共通讯组列表扩展的[电子邮件地址 (NonEmptyStringType)](emailaddress-nonemptystringtype.md)子元素或专用的扩展[ItemId](itemid.md)子元素可以包含一个[邮箱](mailbox.md)元素通讯组列表。 
  
公用通讯组列表可以展开使用下列选项之一：
  
1. 通讯组列表别名
    
2. 简单邮件传输协议 (SMTP) 地址
    
3. X400
    
4. X500
    
5. Exchange 旧版地址
    
6. 通讯组列表名称
    
7. 显示名称
    
> [!IMPORTANT]
> 显示名称不是唯一的。 多个帐户可以共享相同的显示名称。 
  
## <a name="remarks"></a>备注

不支持递归扩展。 可以在单个呼叫中展开只有一个通讯组列表。 如果多个通讯组列表匹配条件，Web 服务报告的错误。 客户端应用程序可以使用模糊名称解析 (ANR) 以查找不明确的通讯组列表，然后选择所需的通讯组列表的正确的电子邮件地址作为参数用于[ExpandDL 操作](expanddl-operation.md)。 有关详细信息，请参阅[ResolveNames 操作](resolvenames-operation.md)。
  
公用通讯组列表在 Active Directory 中的位置。 它们可以是任何已启用邮件的或动态通讯组。 不应从通讯簿中隐藏组和每个成员都应具有一个非空电子邮件地址。 通讯组列表的成员可以是启用邮件的用户和联系人、 公用文件夹和已启用邮件的通讯组列表和动态组。
  
私人通讯组列表位于用户邮箱的联系人文件夹中。 私人通讯组列表没有电子邮件地址，因此其存储项标识符的 ExpandDL 请求中使用。 私有通讯组列表成员可以是任何启用邮件的用户、 联系人或从 Active Directory 通讯组列表或联系人或私有通讯组列表从用户的联系人文件夹。
  
联系人或私人通讯组列表，在响应中返回的项标识符。 这可以用于获取有关对象的信息或以展开私有通讯组列表中的成员身份。
  
## <a name="expanddl-private-distribution-list-request-example"></a>ExpandDL 私有通讯组列表请求示例

### <a name="description"></a>说明

ExpandDL 请求的下面的示例演示如何以形成展开私有通讯组列表的请求。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:ItemId Id="xASUAd==" ChangeKey="AAts0Q=="/>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

若要展开私有通讯组列表，则[邮箱](mailbox.md)元素将包含该[ItemId](itemid.md)元素标识用户的邮箱中的私人通讯组列表。 
  
## <a name="expanddl-public-distribution-list-request-example"></a>ExpandDL 公用通讯组列表请求示例

### <a name="description"></a>说明

ExpandDL 请求的下面的示例演示如何以形成展开公用通讯组列表的请求。 该示例演示如何使用以展开通讯组列表的显示名称。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <ExpandDL xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <t:Mailbox>
          <t:EmailAddress>TheDistributionList</t:EmailAddress>
        </t:Mailbox>
    </ExpandDL>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

对此请求的响应将包含标识通讯组列表中的每个邮箱的**邮箱**元素。 如果通讯组列表包含在通讯组列表中，必须在单独的通讯组列表扩展执行上嵌入的通讯组列表。 如果通讯组列表不包含任何成员或请求的通讯组列表不存在， **ResponseClass**属性将不包含的值等于成功。 
  
### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [ExpandDL](expanddl.md)
    
- [Mailbox](mailbox.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)用于标识公用通讯组列表。 [ItemId](itemid.md)元素用于标识私人通讯组列表。 
    
> [!NOTE]
> 介绍这些元素的架构位于运行 MicrosoftExchange Server 2007 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。 
  
## <a name="successful-expanddl-response-example"></a>成功 ExpandDL 响应示例

### <a name="description"></a>说明

ExpandDL 响应的下面的示例演示上述请求的响应。 通讯组列表扩展介绍以下： 
  
- 通讯组列表的响应中返回的成员数。
    
- 是否则响应中包含通讯组列表的所有的成员。
    
- 邮箱的名称。
    
- 邮箱的电子邮件地址。
    
- 邮箱路由类型。
    
- 邮箱的类型。
    
> [!NOTE]
> 响应; 中不包括通讯组列表名称因此，您必须跟踪的请求的名称。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [DLExpansion](dlexpansion.md)
    
- [Mailbox](mailbox.md)
    
- [名称 (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
若要查找的响应消息 ExpandDL 操作的其他选项，浏览的架构层次结构。 启动[ExpandDLResponse](expanddlresponse.md)元素。 
  
## <a name="expanddl-error-response"></a>ExpandDL 错误响应

### <a name="description"></a>说明

下面的示例演示 ExpandDL 请求错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <ExpandDLResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
    
若要查找的响应消息 ExpandDL 操作的其他选项，浏览的架构层次结构。 启动[ExpandDLResponse](expanddlresponse.md)元素。 
  
## <a name="see-also"></a>另请参阅

- [ResolveNames 操作](resolvenames-operation.md)
- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

