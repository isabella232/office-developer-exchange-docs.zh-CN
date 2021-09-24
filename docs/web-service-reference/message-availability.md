---
title: Message (Availability)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Message
api_type:
- schema
ms.assetid: 1eec24dd-c981-41f4-a2f0-c51d43f1d7c0
description: Message 元素包含 OOF Office (的) 。
ms.openlocfilehash: d5698e8eeca25d0386ccad04b36dcfbf9dfa8d14
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523942"
---
# <a name="message-availability"></a>Message (Availability)

Message 元素包含 OOF Office (响应) Out。 
  
```xml
<Message/> 
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[InternalReply](internalreply.md) <br/> | 包含发送给发件人域中其他用户的 OOF 邮件。 <br/> <br/>  以下是此元素的可能 XPath 表达式： <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/InternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/InternalReply` <br/> |
|[ExternalReply](externalreply.md) <br/> | 包含发送到发件人域外部地址的 OOF 邮件。  <br/> <br/> 以下是此元素的可能 XPath 表达式：  <br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/ExternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/ExternalReply` <br/> |
|[ReplyBody](replybody.md) <br/> |包含 OOF 邮件和用于邮件的语言。  <br/> |
   
## <a name="text-value"></a>文本值

设置 OOF 邮件需要文本值。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

[SetUserOofSettings](setuseroofsettings-operation.md)操作请求的以下示例将 [OofState](oofstate.md)设置为 **Enabled，** 将 OOF 的持续时间设置为 10 天，并设置内部和外部 OOF 邮件。
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [SetUserOofSettings 操作](setuseroofsettings-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

