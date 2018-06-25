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
ms.openlocfilehash: 078bec85e1ca1530137f9935365d7dd3e530ea34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827005"
---
# <a name="recurrenceid"></a>RecurrenceId

**RecurrenceId**元素用于标识定期日历项目的特定实例。 
  
```xml
<RecurrenceId/>
```

 **dateTime**
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
|[MeetingMessage](meetingmessage.md) <br/> |表示会议消息。  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |表示一个会议请求。  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |代表会议响应。  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |表示会议取消。  <br/> |
   
## <a name="text-value"></a>文本值

文本值表示标识日历匹配项的日期/时间值。
  
## <a name="remarks"></a>注解

此属性与[UID](uid.md)属性用于确定定期日历项目的特定实例。 
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

