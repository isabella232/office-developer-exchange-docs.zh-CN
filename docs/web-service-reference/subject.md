---
title: 主题
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Subject
api_type:
- schema
ms.assetid: c140d6c2-deb1-4f67-a908-9397197c4ae7
description: Subject 元素表示存储项目Exchange主题属性。 主题限制为 255 个字符。
ms.openlocfilehash: 95e165de80388a8ae691a894f38e669d204a46f4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509306"
---
# <a name="subject"></a>主题

**Subject** 元素表示存储项目Exchange主题属性。 主题限制为 255 个字符。 
  
```XML
<Subject/>
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
|[CalendarItem](calendaritem.md) <br/> |表示 Exchange 日历项。  <br/> |
|[CancelCalendarItem](cancelcalendaritem.md) <br/> |代表取消日历项目响应对象。  <br/> |
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
|[DistributionList](distributionlist.md) <br/> |表示通讯组列表。  <br/> |
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |指定要查找的邮件类型的条件。  <br/> |
|[ForwardItem](forwarditem.md) <br/> |表示转发项目智能响应对象。  <br/> |
|[项目](item.md) <br/> |表示 Exchange 存储中的项。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示 Exchange 存储中的会议取消。  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |表示会议存储中的Exchange消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示 Exchange 存储中的会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示 Exchange 存储中的会议响应。  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |代表邮件存储Exchange电子邮件。  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |包含 [FindMessageTrackingReportResponse](findmessagetrackingreportresponse.md) 元素的单个邮件结果。  <br/> |
|[RemoveItem](removeitem.md) <br/> |代表删除项目响应对象。  <br/> |
|[ReplyAllToItem](replyalltoitem.md) <br/> |代表"全部答复"智能响应对象。  <br/> |
|[ReplyToItem](replytoitem.md) <br/> |表示答复到项目的智能响应对象。  <br/> |
|[任务](task.md) <br/> |表示 Exchange 存储中的任务。  <br/> |
   
## <a name="text-value"></a>文本值

包含项目主题的文本值Exchange项。
  
## <a name="remarks"></a>说明

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

