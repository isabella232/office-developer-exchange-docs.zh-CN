---
title: 持续时间（UserOofSettings）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Duration
api_type:
- schema
ms.assetid: 01d67af3-658e-4acd-93e3-441ae827fdd3
description: Duration 元素指定将 OofState 元素设置为 "计划" 时，"外出" （OOF）状态为 "已启用" 的持续时间。
ms.openlocfilehash: 0ba0f1ea7498781c0cccb072c7ea0fa05414764c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457296"
---
# <a name="duration-useroofsettings"></a>持续时间（UserOofSettings）

**Duration**元素指定将[OofState](oofstate.md)元素设置为 "**计划**" 时，"外出" （OOF）状态为 "已启用" 的持续时间。
  
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
|[StartTime](starttime.md) <br/> |表示具有 OOF 状态的时间范围集的开始时间。 此元素是必需的。  <br/> |
|[EndTime](endtime.md) <br/> |表示具有 OOF 状态的时间范围设置的结束时间。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[UserOofSettings](useroofsettings.md) <br/> |指定 OOF 设置。  <br/><br/>下面是此元素的 XPath 表达式： <br/><br/>`/SetUserOofSettingsRequest/UserOofSettings` <br/> |
|[OofSettings](oofsettings.md) <br/> |包含 OOF 设置。<br/><br/>下面是此元素的 XPath 表达式： <br/><br/>`/GetUserOofSettingsResponse/OofSettings` <br/> |
|[外出](outofoffice.md) <br/> |定义 "外出（OOF）" 响应消息和发送邮箱响应邮件的持续时间。  <br/> |
   
## <a name="remarks"></a>备注

**持续时间**类型也是[DetailedSuggestionsWindow](detailedsuggestionswindow.md)、 [TimeWindow](timewindow.md)和[外出](outofoffice.md)元素的类型。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="example"></a>示例

以下示例的[SetUserOofSettings 操作](setuseroofsettings-operation.md)请求将[OofState](oofstate.md)设置为 "**启用**"、"内部和外部 OOF" 邮件，并将 "oof" 的持续时间设置为10天。
  
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

