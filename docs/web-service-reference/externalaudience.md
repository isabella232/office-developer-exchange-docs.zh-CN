---
title: ExternalAudience
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ExternalAudience
api_type:
- schema
ms.assetid: 79dc2a4c-f7dd-46d1-8f31-149116e1f76e
description: ExternalAudience 元素设置或包含一个值，该值确定 OOF 邮件Office (外部) 发送到谁。
ms.openlocfilehash: da318bfcf4a43d880b86379364c6e40aa9861f83
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545137"
---
# <a name="externalaudience"></a>ExternalAudience

**ExternalAudience** 元素设置或包含一个值，该值确定 OOF 邮件Office (外部) 发送到谁。 
  
```xml
<ExternalAudience>None or Known or All</ExternalAudience>
```

 **ExternalAudience**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |指定 OOF 设置。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |包含 OOF 设置。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetUserOofSettingsResponse/OofSettings` <br/> |
   
## <a name="text-value"></a>文本值

此元素需要文本值。 下表列出了此元素的可能值。
  
|**值**|**说明**|
|:-----|:-----|
|**无** <br/> |向用户发送邮件的邮箱用户组织外部的电子邮件发件人不会收到外部 OOF 邮件响应。  <br/> |
|**已知** <br/> |向用户发送邮件的邮箱用户组织外部的电子邮件发件人将仅收到外部 OOF 邮件响应（如果发件人位于用户的 Exchange 存储联系人列表中）。  <br/> |
|**全部** <br/> |向用户发送邮件的邮箱用户组织外部的电子邮件发件人将收到外部 OOF 邮件响应。  <br/> |
   
## <a name="remarks"></a>注解

此元素与 [AllowExternalOof](allowexternaloof.md) 元素共享同一类型。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

SetUserOofSettings 请求的以下示例将 OoFState 设置为 **Enabled，** 将外部访问群体设置为 **All，** 将 OOF 的持续时间设置为 10 天，并设置内部和外部 OOF 邮件。
  
```
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



[GetUserOofSettings 操作](getuseroofsettings-operation.md)
  
[SetUserOofSettings 操作](setuseroofsettings-operation.md)

