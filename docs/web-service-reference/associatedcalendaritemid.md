---
title: AssociatedCalendarItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AssociatedCalendarItemId
api_type:
- schema
ms.assetid: 5b29898c-ea59-4e6a-914c-c011ec754032
description: AssociatedCalendarItemId 元素表示与 MeetingMessage、MeetingRequest、MeetingResponse、MeetingCancellation 或 ReminderMessageData 关联的日历项目。
ms.openlocfilehash: 5a51c5e3e43a25ebe676bc85e80c2a6ab3705c4d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543686"
---
# <a name="associatedcalendaritemid"></a>AssociatedCalendarItemId

**AssociatedCalendarItemId** 元素表示与 [MeetingMessage](meetingmessage.md)、 [MeetingRequest](meetingrequest.md)、 [MeetingResponse](meetingresponse.md)、 [MeetingCancellation](meetingcancellation.md)或 [ReminderMessageData](remindermessagedata.md)相关联的日历项目。
  
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
|**ChangeKey** <br/> |标识与会议关联的日历项目的特定版本。  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

[MeetingMessage](meetingmessage.md)  | [MeetingRequest](meetingrequest.md)  | [MeetingResponse](meetingresponse.md)  | [MeetingCancellation](meetingcancellation.md)  | [ReminderMessageData](remindermessagedata.md)
  
## <a name="remarks"></a>注解

从Exchange号 15.00.0913.09 开始的版本可以包含 **AssociatedCalendarItemId** 元素作为 **ReminderMessageData** 元素的子元素。 
  
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

