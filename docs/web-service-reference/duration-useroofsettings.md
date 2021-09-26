---
title: Duration (UserOofSettings)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: Duration 元素指定当 OofState 元素设置为 Scheduled 时 (外出或 OOF) 状态启用的持续时间。
ms.openlocfilehash: cb6529bfe3799ff41550d7fe3ce2c79b8a4197e2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544155"
---
# <a name="duration-useroofsettings"></a>Duration (UserOofSettings)

**Duration** 元素指定当 [OofState](oofstate.md)元素设置为 Scheduled 时 (外出 OOF) 状态 **启用的持续时间**。
  
```XML
<Duration>
   <StartTime/>
   <EndTime/> 
</Duration>
```

 **Duration**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |代表使用 OOF 状态设置的时间跨度的开始时间。 此元素是必需的。  <br/> |
|[EndTime](endtime.md) <br/> |表示使用 OOF 状态设置的结束时间跨度。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |指定 OOF 设置。  <br/><br/>下面是此元素的 XPath 表达式： <br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |包含 OOF 设置。<br/><br/>下面是此元素的 XPath 表达式： <br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[OutOfOffice](outofoffice.md) <br/> |定义 Out of Office (OOF) 响应邮件和发送邮箱响应邮件的持续时间。  <br/> |
   
## <a name="remarks"></a>注解

**Duration** 类型也是 [DetailedSuggestionsWindow、TimeWindow](detailedsuggestionswindow.md)[](timewindow.md)和 [OutOfOffice 元素](outofoffice.md)的类型。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

[SetUserOofSettings](setuseroofsettings-operation.md)操作请求的以下示例将 [OofState](oofstate.md)设置为 **Enabled、** 内部和外部 OOF 邮件，并设置 OOF 的持续时间为 10 天。
  
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
        <SetByLegacyClient>false</SetByLegacyClient>
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

- [GetUserOofSettings 操作](getuseroofsettings-operation.md)  
- [SetUserOofSettings 操作](setuseroofsettings-operation.md)

