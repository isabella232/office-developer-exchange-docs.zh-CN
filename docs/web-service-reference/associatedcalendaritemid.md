---
title: AssociatedCalendarItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AssociatedCalendarItemId
api_type:
- schema
ms.assetid: 5b29898c-ea59-4e6a-914c-c011ec754032
description: AssociatedCalendarItemId 元素均表示与 MeetingMessage、 MeetingRequest、 MeetingResponse、 MeetingCancellation 或 ReminderMessageData 相关联的日历项目。
ms.openlocfilehash: 4445da88d6fec42c1e02cd8de4d2e423485a4472
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753274"
---
# <a name="associatedcalendaritemid"></a>AssociatedCalendarItemId

**AssociatedCalendarItemId**元素均表示与[MeetingMessage](meetingmessage.md)、 [MeetingRequest](meetingrequest.md)、 [MeetingResponse](meetingresponse.md)、 [MeetingCancellation](meetingcancellation.md)或[ReminderMessageData](remindermessagedata.md)相关联的日历项目。
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|
  **Id** <br/> |标识与会议相关联的日历项。  <br/> |
|**更改密钥** <br/> |标识与会议相关联的日历项目的特定版本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MeetingMessage](meetingmessage.md) | [MeetingRequest](meetingrequest.md) | [MeetingResponse](meetingresponse.md) | [MeetingCancellation](meetingcancellation.md) | [ReminderMessageData](remindermessagedata.md)
  
## <a name="remarks"></a>注解

内部版本号 15.00.0913.09 开头的 Exchange 版本可作为**ReminderMessageData**元素的子元素包括**AssociatedCalendarItemId**元素。 
  
描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

