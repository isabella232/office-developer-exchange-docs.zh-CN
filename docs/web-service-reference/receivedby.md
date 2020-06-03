---
title: ReceivedBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReceivedBy
api_type:
- schema
ms.assetid: ac84c9c5-d2fe-4b6f-bf4d-0444131d835b
description: ReceivedBy 元素标识代理访问方案中的委派。
ms.openlocfilehash: 7cee996c15e81f77d71f42e052b14b1d21772ba1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468248"
---
# <a name="receivedby"></a>ReceivedBy

**ReceivedBy**元素标识代理访问方案中的委派。 
  
```xml
<ReceivedBy>
   <Mailbox/>
</ReceivedBy>
```

 **SingleRecipientType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Message](message-ex15websvcsotherref.md) <br/> |表示 Exchange 电子邮件。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示 Exchange 存储中的会议。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[AcceptItem](acceptitem.md) <br/> |表示接受答复会议要求。  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |表示一个暂定答复会议要求。  <br/> |
|[DeclineItem](declineitem.md) <br/> |表示谢绝答复会议要求。  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |包含对 Exchange 存储中的项的创建者的答复。  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |包含对所有确定收件人的 Exchange 存储中的项的答复。  <br/> |
|[ForwardItem](forwarditem.md) <br/> |包含要转发给收件人的 Exchange 存储区项。  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |表示用于取消会议的响应对象。  <br/> |
   
## <a name="remarks"></a>备注

**ReceivedRepresenting**元素与代理访问方案中的**From**和**ReceivedBy**元素一起使用。 下表列出了这些元素在代理访问方案中表示的实体。 
  
**代理访问方案中的元素**

|**元素**|**元素所表示的实体**|
|:-----|:-----|
|[From](from.md) <br/> |ThirdParty  <br/> |
|[ReceivedBy](receivedby.md) <br/> |委派用户  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |校长  <br/> |
   
在代理访问方案中，如果 ThirdParty 向具有代理的主体发送会议请求，则代理将看到一个新的会议请求。 这些元素使代理能够区分直接发送给他们的邮件和发送给他们的邮件，因为它是一个代理转发规则。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

