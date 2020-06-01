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
description: AssociatedCalendarItemId 元素表示与 MeetingMessage、MeetingRequest、MeetingResponse、MeetingCancellation 或 ReminderMessageData 相关联的日历项目。
ms.openlocfilehash: 816372c38243ba0fe5a7606c264dd1c5107350f2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460881"
---
# <a name="associatedcalendaritemid"></a>AssociatedCalendarItemId

**AssociatedCalendarItemId**元素表示与[MeetingMessage](meetingmessage.md)、 [MeetingRequest](meetingrequest.md)、 [MeetingResponse](meetingresponse.md)、 [MeetingCancellation](meetingcancellation.md)或[ReminderMessageData](remindermessagedata.md)相关联的日历项目。
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

|**属性**|**说明**|
|:-----|:-----|
|**Id** <br/> |标识与会议关联的日历项目。  <br/> |
|**ChangeKey** <br/> |标识与会议相关联的日历项目的特定版本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [MeetingCancellation](meetingcancellation.md)  | [ReminderMessageData](remindermessagedata.md)
  
## <a name="remarks"></a>备注

从内部版本号15.00.0913.09 开始的 Exchange 版本可以将**AssociatedCalendarItemId**元素作为**ReminderMessageData**元素的子元素包括在内。 
  
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

