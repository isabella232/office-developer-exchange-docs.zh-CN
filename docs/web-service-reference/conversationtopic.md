---
title: ConversationTopic
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationTopic
api_type:
- schema
ms.assetid: 46cacf42-4039-4c8a-9b20-c42cdd9f2760
description: ConversationTopic 元素均表示对话主题。
ms.openlocfilehash: 30b919dec3e65ca1961aac3f9c11c72cf97d707f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753597"
---
# <a name="conversationtopic"></a>ConversationTopic

**ConversationTopic**元素均表示对话主题。 
  
```xml
<ConversationTopic/>
```

 **字符串**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[RemoveItem](removeitem.md) <br/> |从 Exchange 存储中删除一个项目。  <br/> |
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
|[PostItem](postitem.md) <br/> |代表一个 Exchange 存储中的公告项目。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。  <br/> |
|[对话 (ConversationType)](conversation-conversationtype.md) <br/> |表示单个对话。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示对话线程的主题。
  
## <a name="remarks"></a>注解

对话主题通常是线程中的第一个电子邮件的主题。
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindConversation Operation](findconversation-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
