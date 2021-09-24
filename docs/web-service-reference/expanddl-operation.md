---
title: ExpandDL 操作
manager: sethgros
ms.date: 07/27/2018
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: 1f7837e7-9eff-4e10-9577-c40f7ed6af94
description: ExpandDL 操作公开通讯组列表的完整成员身份。
ms.openlocfilehash: 9878ecff0eeee1ef386c7bb26a092eec47f471de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513778"
---
# <a name="expanddl-operation"></a>ExpandDL 操作

ExpandDL 操作公开通讯组列表的完整成员身份。
  
## <a name="using-the-expanddl-web-method"></a>使用 ExpandDL Web 方法

ExpandDL 操作使用位于 Exchange.asmx 中的 Web 服务。 此 Web 服务方法接受一个 [Mailbox](mailbox.md) 元素，该元素可以包含用于扩展公共通讯组列表的 [EmailAddress (NonEmptyStringType) ](emailaddress-nonemptystringtype.md) 子元素，也可以包含用于扩展专用通讯组列表的 [ItemId](itemid.md) 子元素。 
  
可以使用下列方法之一扩展公共通讯组列表：
  
1. 通讯组列表别名
    
2. 简单邮件传输协议 (SMTP) 地址
    
3. X400
    
4. X500
    
5. Exchange旧地址
    
6. 通讯组列表名称
    
7. the 显示名称
    
> [!IMPORTANT]
> 显示名称不是唯一的。 多个帐户可以共享同一显示名称。 
  
## <a name="remarks"></a>注解

不支持递归扩展。 在一次呼叫中只能展开一个通讯组列表。 如果多个通讯组列表与条件匹配，则 Web 服务将报告一个错误。 客户端应用程序可以使用不明确的名称解析 (ANR) 来查找不明确的通讯组列表，然后选择所需的通讯组列表的正确电子邮件地址作为 [ExpandDL](expanddl-operation.md)操作的参数。 有关详细信息，请参阅 [ResolveNames 操作](resolvenames-operation.md)。
  
公共通讯组列表位于 Active Directory 中。 它们可以是任何启用邮件的通讯组或动态通讯组。 不应在地址列表中隐藏组，并且每个成员都应有一个非空的电子邮件地址。 通讯组列表的成员可以是启用邮件的用户和联系人、公用文件夹以及启用邮件的通讯组列表和动态组。
  
专用通讯组列表位于用户邮箱的"联系人"文件夹中。 专用通讯组列表没有电子邮件地址，因此它们的存储项标识符用于 ExpandDL 请求。 专用通讯组列表的成员可以是 Active Directory 中任何启用邮件的用户、联系人或通讯组列表，或者是用户的"联系人"文件夹中的联系人或专用通讯组列表。
  
对于联系人或专用通讯组列表，在响应中返回项目标识符。 这可用于获取有关对象的信息或扩展专用通讯组列表中的成员身份。
  
## <a name="expanddl-private-distribution-list-request-example"></a>ExpandDL 专用通讯组列表请求示例

### <a name="description"></a>Description

ExpandDL 请求的以下示例显示如何形成展开专用通讯组列表的请求。
  
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

若要展开专用通讯组列表 [，Mailbox](mailbox.md) 元素将包含标识用户邮箱中的专用通讯组列表的 [ItemId](itemid.md) 元素。 
  
## <a name="expanddl-public-distribution-list-request-example"></a>ExpandDL 公共通讯组列表请求示例

### <a name="description"></a>Description

ExpandDL 请求的以下示例显示如何形成展开公用通讯组列表的请求。 该示例演示如何使用 显示名称展开通讯组列表。
  
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

对此请求的响应将包含标识通讯组列表中的每个邮箱的 **Mailbox** 元素。 如果通讯组列表包含在通讯组列表中，则必须对嵌入的通讯组列表执行单独的通讯组列表扩展。 如果通讯组列表没有成员或请求的通讯组列表不存在， **则 ResponseClass** 属性将包含一个等于 Success 的值。 
  
### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [ExpandDL](expanddl.md)
    
- [邮箱](mailbox.md)
    
- [EmailAddress (NonEmptyStringType ](emailaddress-nonemptystringtype.md)) 用于标识公用通讯组列表。 [ItemId](itemid.md)元素用于标识专用通讯组列表。 
    
> [!NOTE]
> 描述这些元素的架构位于运行安装了客户端访问服务器角色的 MicrosoftExchange Server 2007 的计算机的 EWS 虚拟目录中。 
  
## <a name="successful-expanddl-response-example"></a>成功的 ExpandDL 响应示例

### <a name="description"></a>Description

ExpandDL 响应的以下示例显示了对上述请求的响应。 通讯组列表扩展描述以下内容： 
  
- 响应中返回的通讯组列表的成员数。
    
- 响应是否包含通讯组列表的所有成员。
    
- 邮箱的名称。
    
- 邮箱的电子邮件地址。
    
- 邮箱的路由类型。
    
- 邮箱的类型。
    
> [!NOTE]
> 响应中不包含通讯组列表名称;因此，您必须跟踪请求中的名称。 
  
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

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [DLExpansion](dlexpansion.md)
    
- [邮箱](mailbox.md)
    
- [名称 (EmailAddressType)](name-emailaddresstype.md)
    
- [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)
    
- [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)
    
- [MailboxType](mailboxtype.md)
    
若要查找 ExpandDL 操作的响应消息的其他选项，请浏览架构层次结构。 从 [ExpandDLResponse 元素](expanddlresponse.md) 开始。 
  
## <a name="expanddl-error-response"></a>ExpandDL 错误响应

### <a name="description"></a>Description

以下示例显示对 ExpandDL 请求的错误响应。
  
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

错误响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [ExpandDLResponse](expanddlresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [ExpandDLResponseMessage](expanddlresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
若要查找 ExpandDL 操作的响应消息的其他选项，请浏览架构层次结构。 从 [ExpandDLResponse 元素](expanddlresponse.md) 开始。 
  
## <a name="see-also"></a>另请参阅

- [ResolveNames 操作](resolvenames-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

