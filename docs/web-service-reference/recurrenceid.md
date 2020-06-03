---
title: RecurrenceId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: RecurrenceId 元素用于标识定期日历项目的特定实例。
ms.openlocfilehash: 58a379f2cffa7ff37181e93ad1c45c9752e84f1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461609"
---
# <a name="recurrenceid"></a>RecurrenceId

**RecurrenceId**元素用于标识定期日历项目的特定实例。 
  
```xml
<RecurrenceId/>
```

 **dateTime**
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
|[MeetingMessage](meetingmessage.md) <br/> |表示会议邮件。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |表示会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示会议取消。  <br/> |
   
## <a name="text-value"></a>文本值

该文本值表示用于标识日历发生情况的日期/时间值。
  
## <a name="remarks"></a>备注

此属性与[UID](uid.md)属性一起用来标识定期日历项目的特定实例。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

