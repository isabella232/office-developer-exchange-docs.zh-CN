---
title: 主题
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subject
api_type:
- schema
ms.assetid: c140d6c2-deb1-4f67-a908-9397197c4ae7
description: Subject 元素表示 Exchange 存储项目的 subject 属性。 主题被限制为 255 个字符。
ms.openlocfilehash: b93d64c6f517c1cc990d697061c8dad478eb3a3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827612"
---
# <a name="subject"></a>主题

**Subject**元素表示 Exchange 存储项目的 subject 属性。 主题被限制为 255 个字符。 
  
```XML
<Subject/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[日历项目](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |代表取消日历项响应对象。  <br/> |
|[联系人](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |指定条件的邮件，以查找的类型。  <br/> |
|[ForwardItem](forwarditem.md) <br/> |代表转发项目智能响应对象。  <br/> |
|[项目](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |代表 Exchange 存储中的会议消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |代表 Exchange 存储中的电子邮件。  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |包含单个邮件结果[FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md)元素。  <br/> |
|[RemoveItem](removeitem.md) <br/> |代表一个删除项响应对象。  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |代表全部答复智能响应对象。  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |代表答复到项智能响应对象。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

包含一个 Exchange 项目的主题文本值为 required。
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

