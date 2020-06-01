---
title: 与会者
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Attendee
api_type:
- schema
ms.assetid: 393c3d7e-7416-458a-b976-270b88eaaa03
description: "\"与会者\" 元素表示会议的与会者和资源。"
ms.openlocfilehash: f376e59b27017e0a9d27692cb1a4ae759cd1af0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457646"
---
# <a name="attendee"></a>与会者

"**与会者**" 元素表示会议的与会者和资源。 
  
```xml
<Attendee>
   <Mailbox/>
   <ResponseType/>
   <LastResponseTime/>
</Attendee>
```

 **AttendeeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识完全解析的电子邮件地址。  <br/> |
|[ResponseType](responsetype.md) <br/> |表示接收会议的收件人响应的类型。 此属性仅与会议组织者的日历项目相关。  <br/> |
|[LastResponseTime](lastresponsetime.md) <br/> |表示收到的最新响应的日期和时间。  <br/> |
|[ProposedStart](proposedstart-attendeetype.md) <br/> |表示与会者为会议建议的开始时间。 <br/> |
|[ProposedEnd](proposedend-attendeetype.md) <br/> |表示与会者为会议建议的结束时间。 <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RequiredAttendees](requiredattendees.md) <br/> |表示参加会议所需的与会者。  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |表示参加会议不需要的与会者。  <br/> |
|[资源](resources.md) <br/> |表示会议的计划资源。  <br/> |
   
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

