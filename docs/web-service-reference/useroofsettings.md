---
title: UserOofSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserOofSettings
api_type:
- schema
ms.assetid: 0a95ca63-660e-4cc0-82e4-3f74fb4ae21c
description: UserOofSettings 元素指定的外出 (OOF) 设置。
ms.openlocfilehash: a035fd89387ece632d83f5f72a564e4896bc6753
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838481"
---
# <a name="useroofsettings"></a>UserOofSettings

**UserOofSettings**元素指定的外出 (OOF) 设置。 
  
[SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
  
[UserOofSettings](useroofsettings.md)
  
```xml
<UserOofSettings>
   <OofState>...</OofState>
   <ExternalAudience>...</ExternalAudience>
   <Duration>...</Duration>
   <InternalReply>...</InternalReply>
   <ExternalReply>...</ExternalReply>
</UserOofSettings>
```

 **UserOofSettings**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[OofState](oofstate.md) <br/> |设置用户的 OOF 状态。  <br/> |
|[ExternalAudience](externalaudience.md) <br/> |设置或包含一个值，确定外部 OOF 邮件发送到其。  <br/> |
|[持续时间 (UserOofSettings)](duration-useroofsettings.md) <br/> |指定如果[OofState](oofstate.md)元素设置为**计划**为其启用 OOF 状态的持续时间。 如果[OofState](oofstate.md)元素设置为**已启用**或**禁用**，则忽略此元素的值。  <br/> |
|[InternalReply](internalreply.md) <br/> |包含 OOF 响应发送给用户的域或受信任的域中的其他用户。  <br/> |
|[ExternalReply](externalreply.md) <br/> |包含 OOF 响应发送给外部收件人的域或受信任的域的地址。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[SetUserOofSettingsRequest](setuseroofsettingsrequest.md) <br/> |包含用于设置邮箱用户的 OOF 设置和消息的参数。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/SetUserOofSettingsRequest` <br/> |
   
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

SetUserOofSettings 请求的下面的示例将 OoFState 设置为**已启用**，将 OOF 的持续时间设置为 10 天，并设置内部和外部 OOF 邮件。
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |邮件架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [SetUserOofSettings 操作](setuseroofsettings-operation.md)

